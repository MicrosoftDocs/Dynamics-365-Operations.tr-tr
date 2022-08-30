---
title: Ambar yönetimi eldeki stok girişlerini temizleme işi
description: Bu makale, gerekli ancak gerekmeyen kayıtları tanımlayıp silerek sistem performansının artırılmasına yardımcı olan eldeki girişler temizleme işini açıklamaktadır.
author: perlynne
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: df20f00a639d237bf8446f24a2ad4cbbfcf36615
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334400"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Ambar yönetimi eldeki stok girişlerini temizleme işi

[!include [banner](../includes/banner.md)]

Eldeki stoğu hesaplamak için kullanılan sorguların performansı, söz konusu tablolardaki kayıt sayısından etkilenir. Performansı iyileştirmeye yardımcı olmanın bir yolu, veritabanının dikkate alınması gereken kayıt sayısını azaltmaktır.

Bu makalede, `InventSum` ve `WHSInventReserve` tablolarında gerekmeyen kayıtları silen eldeki girişler temizleme işi açıklanmaktadır. Bu tablolar, ambar yönetimi işlemleri için etkinleştirilen maddeler için eldeki bilgileri depolar. (Bu öğeler, WMS öğeleri olarak adlandırılır.) Bu kayıtların silinmesi, mevcut hesaplamaların performansını önemli ölçüde artırabilir.

## <a name="what-the-cleanup-job-does"></a>Temizleme işi ne yapar

Mevcut girişleri temizleme işi, `WHSInventReserve` ve `InventSum` tablolarındaki tüm alan değerlerinin *0* (sıfır) olduğu tüm kayıtları siler. Bu kayıtlar, eldeki bilgilere katkıda bulunmadığından silinebilir. İş, yalnızca **konum** düzeyinin altında olan kayıtları siler.

Negatif fiziksel stoka izin veriliyorsa, temizleme işi ilgili tüm girişleri silememeyebilir. Bu sınırlamanın nedeni işin, lisans kalıbının birden çok seri numarası olduğu ve bu seri numaralarından biri negatif hale geldiği özel bir senaryoya izin vermesi gerekir. Örneğin, bir lisans kalıbının -1 seri numarasından ve %2 seri numarasından 1 PC 'ye sahip olduğu durumlarda sistem, lisans levhası düzeyinde sıfır elindedir sahip olacaktır. Bu özel senaryo için iş, öncelikle daha düşük düzeylerden silmeye çalıştığı, birinci düzey silme işlemi yapar.

## <a name="schedule-and-configure-the-cleanup-job"></a>Temizleme işini zamanla ve Yapılandır

Eldeki girişler temizleme işi **Stok yönetimi \> periyodik görevler \> Temizleme\> Ambar yönetimi eldeki girişlerini temizleme**'de kullanılabilir. Kapsamı denetlemek ve işi çalıştırmak için zamanlamak üzere standart iş ayarlarını kullanın. Buna ek olarak aşağıdaki ayarlar sağlanır:

- **Bu kadar gün için güncelleştirilmemişse, Sil** – Sıfır miktara bırakılan eldeki bir girişi silmeden önce işin en az kaç gün bekleyeceğini girin. Halen kullanılmakta olan eldeki girişleri silme riskini azaltmaya yardımcı olması için bu ayarı kullanın. Temizleme işleminin olabildiğince çabuk gerçekleşmesini istiyorsanız, *0* (sıfır) girin veya alanı boş bırakın.
- **Maksimum yürütme süresi (saat)** – temizleme işinin maksimum yürütme süresini saat olarak girin. İş bu süre geçmeden önce tamamlanmadıysa, şimdiye kadar tamamladığı işi kaydeder ve sonra da kendisini kapatır. Bu yetenek özellikle yüksek stok kullanımı olan uygulamalarla ilgilidir. Bu durumlarda, işi sistem yükünün olabildiğince açık olduğu zamanlarda çalışacak şekilde planlamalısınız. Toplu işlemin tamamlanana kadar çalışmaya devam etmesini istiyorsanız, *0* (sıfır) girin ya da alanı boş bırakın. Bu ayar yalnızca, ilgili özellik [sisteminizde açılmışsa](#max-execution-time) kullanılabilir.

İşi normal iş saatlerinde çalıştırmanıza rağmen, çalışma saatleri dışında çalıştırmanızı öneririz. Bu şekilde, bir Kullanıcı temizlenebilecek bir kayıtla çalışıyorsa oluşabilecek çakışmaların engellenmesine yardımcı olabilirsiniz.

Bu kayıt başka bir kullanıcı tarafından kullanılırken, iş bir madde için kayıt silmeye çalışırsa, temizleme işi veya Kullanıcı için kilitlenme hatası oluşur.

İş çalıştığı zaman, 100 kaydetme boyutuna sahip olur. Başka bir deyişle, her 100 silme işlemi için bir kez kaydetmeyi dener. Ancak, bazı silmeler ayarlanmış olduğundan, aynı harekette 100 ' den fazla kayıt silinebilecek senaryolar olabilir. Bu nedenle, yine de kilit yürüyen da karşılaşabilirsiniz.

## <a name="possible-user-impact"></a>Olası Kullanıcı etkisi

Eldeki girişler temizleme işi belirli bir düzeydeki tüm kayıtları (örneğin, lisans levhası) silerse, kullanıcılar etkilenebilir. Bu durumda, ilgili eldeki girişler artık kullanılamadığından, lisans plakasında stokun daha önce elde mevcut olduğunu görebilmeyle ilgili işlevsellik beklendiği gibi çalışmayabilir. Örneğin bu özellik, aşağıdaki durumlarda denenebilir:

- **Eldeki listesi**'nde, kullanıcı **Miktar \<\> 0** koşulunun seçimini kaldırdığında veya **Boyutlar görünümü** ayarlarında **Kapalı hareketler** koşulunu seçtiğinde.
- Geçmiş dönemler için **Stok boyutuna göre fiziksel stok** raporında kullanıcı **Başlangıç tarihi** parametresini seçtiğinde.

Ancak, temizleme işinin sağladığı performans iyileştirmesi işlevsellikteki bu küçük kayıpları telafi etmelidir.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Maksimum yürütme zamanı ayarını kullanılabilir yap

**Maksimum yürütme zamanı** ayarı, yalnızca *Ambar yönetimi eldeki girişlerini temizleme işi için maksimum yürütme süresi* özelliği açık olduğunda kullanılabilir. Supply Chain Management sürüm 10.0.25 itibariyle, bu özellik varsayılan olarak açıktır. Yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Ambar yönetimi eldeki girişlerini temizleme işi için maksimum yürütme süresi* özelliğini bularak bu işlevi açabilir veya kapatabilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
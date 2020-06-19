---
title: Ambar yönetimi eldeki stok girişlerini temizleme işi
description: Bu konu, gerekli ancak gerekmeyen kayıtları tanımlayıp silerek sistem performansının artırılmasına yardımcı olan eldeki girişler temizleme işini açıklamaktadır.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f6d1f8a4c85c2161d1b79246d437bb3b4d223d1d
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410989"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Ambar yönetimi eldeki stok girişlerini temizleme işi

Eldeki stoğu hesaplamak için kullanılan sorguların performansı, söz konusu tablolardaki kayıt sayısından etkilenir. Performansı iyileştirmeye yardımcı olmanın bir yolu, veritabanının dikkate alınması gereken kayıt sayısını azaltmaktır.

Bu konu, InventSum ve WHSInventReserve servis tablolarında gerekmeyen kayıtları silen eldeki girişler temizleme işini açıklamaktadır. Bu tablolar, ambar yönetimi işlemleri için etkinleştirilen maddeler için eldeki bilgileri depolar. (Bu öğelere, duman maddeleri olarak başvurulur.) Bu kayıtların silinmesi, eldeki hesaplamaların performansını önemli ölçüde artırabilir.

## <a name="what-the-cleanup-job-does"></a>Temizleme işi ne yapar

Eldeki girişler temizleme işi, WHSInventReserve ve InventSum tablolarındaki tüm alan değerlerinin *0* (sıfır) olduğu tüm kayıtları siler. Bu kayıtlar, eldeki bilgilere katkıda bulunmadığından silinebilir. İş, yalnızca **konum** düzeyinin altında olan kayıtları siler.

Negatif fiziksel stoka izin veriliyorsa, temizleme işi ilgili tüm girişleri silememeyebilir. Bu sınırlamanın nedeni işin, lisans kalıbının birden çok seri numarası olduğu ve bu seri numaralarından biri negatif hale geldiği özel bir senaryoya izin vermesi gerekir. Örneğin, bir lisans kalıbının -1 seri numarasından ve %2 seri numarasından 1 PC 'ye sahip olduğu durumlarda sistem, lisans levhası düzeyinde sıfır elindedir sahip olacaktır. Bu özel senaryo için iş, öncelikle daha düşük düzeylerden silmeye çalıştığı, birinci düzey silme işlemi yapar.

## <a name="schedule-and-configure-the-cleanup-job"></a>Temizleme işini zamanla ve Yapılandır

Eldeki girişler temizleme işi **Stok yönetimi \> periyodik görevler \> Temizleme\> Ambar yönetimi eldeki girişlerini temizleme**'de kullanılabilir. Kapsamı denetlemek ve işi çalıştırmak için zamanlamak üzere standart iş ayarlarını kullanın. Buna ek olarak aşağıdaki ayarlar sağlanır:

- **Bu kadar gün için güncelleştirilmemişse, Sil** – Sıfır miktara bırakılan eldeki bir girişi silmeden önce işin en az kaç gün bekleyeceğini girin. Halen kullanılmakta olan eldeki girişleri silme riskini azaltmaya yardımcı olması için bu ayarı kullanın. Temizleme işleminin olabildiğince çabuk gerçekleşmesini istiyorsanız, *0* (sıfır) girin veya alanı boş bırakın.
- **Maksimum yürütme süresi (saat)** – temizleme işinin maksimum yürütme süresini saat olarak girin. İş bu süre geçmeden önce tamamlanmadıysa, şimdiye kadar tamamladığı işi kaydeder ve sonra da kendisini kapatır. Bu yetenek özellikle yüksek stok kullanımı olan uygulamalarla ilgilidir. Bu durumlarda, işi sistem yükünün olabildiğince açık olduğu zamanlarda çalışacak şekilde planlamalısınız. Toplu işlemin tamamlanana kadar çalışmaya devam etmesini istiyorsanız, *0* (sıfır) girin ya da alanı boş bırakın. Bu ayar yalnızca, ilgili özellik [sisteminizde açılmışsa](#max-execution-time) kullanılabilir.

İşi normal iş saatlerinde çalıştırmanıza rağmen, çalışma saatleri dışında çalıştırmanızı öneririz. Bu şekilde, bir Kullanıcı temizlenebilecek bir kayıtla çalışıyorsa oluşabilecek çakışmaların engellenmesine yardımcı olabilirsiniz.

Bu kayıt başka bir kullanıcı tarafından kullanılırken, iş bir madde için kayıt silmeye çalışırsa, temizleme işi veya Kullanıcı için kilitlenme hatası oluşur.

İş çalıştığı zaman, 100 kaydetme boyutuna sahip olur. Başka bir deyişle, her 100 silme işlemi için bir kez kaydetmeyi dener. Ancak, bazı silmeler ayarlanmış olduğundan, aynı harekette 100 ' den fazla kayıt silinebilecek senaryolar olabilir. Bu nedenle, yine de kilit yürüyen da karşılaşabilirsiniz.

## <a name="possible-user-impact"></a>Olası Kullanıcı etkisi

Eldeki girişler temizleme işi belirli bir düzeydeki tüm kayıtları (örneğin, lisans levhası) silerse, kullanıcılar etkilenebilir. Bu durumda, ilgili eldeki girişler artık kullanılamadığından, bu stoğu daha önce bir lisans kalıbına açık olarak kullanılabilir olarak görebilmeyle ilgili işlevsellik beklendiği gibi çalışmayabilir. (Bu işlev koşulu denetler Kullanıcılar eldeki bilgileri görüntülerken **Boyut görüntüleme** ayarlarına göre **Miktar \<\> 0**.) Ancak, temizleme işinin sağladığı performans iyileştirmesi bu küçük kaybı için işlev yapmalı.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Maksimum yürütme zamanı ayarını kullanılabilir yap

Varsayılan olarak **Maksimum yürütme zamanı** kullanılabilir değil. Bunu kullanmak istiyorsanız, sisteminizdeki ilgili özelliği açmak için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanmalısınız. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ambar yönetimi için maksimum yürütme süresi eldeki girişler temizleme işi*

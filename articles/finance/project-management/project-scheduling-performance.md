---
title: Proje kaynak planlaması performansı
description: Bu konuda, çok sayıda proje için kaynak planlama performansının nasıl geliştirileceği ile ilgili bilgiler sağlanır.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760689"
---
# <a name="project-resource-scheduling-performance"></a>Proje kaynak planlaması performansı

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Kaynak iş planlaması ile ilgili performans sorunları proje sayısı binlere ulaştığında oluşabilir. Kaynak planlama performansını artırmak için, kullanıcıların kaynak kullanılabilirlik formunu başlatmak için gerekli süreyi azaltmasına olanak tanıyan bir özellik sunulmuştur. Bu işlem, kaynak kapasitesi toplaması eşitleme işlemini kaldırır ve kaynak aramasını hızlandırmak için **ResProjectResource** tablosunu kullanır. **Resrollup** tablosunun artık kullanılmayacağını unutmayın.

> [!IMPORTANT]
> Kaynak kapasitesi toplaması eşitleme işleminde veya **ResProjectResource** tablosunda bir bağımlılık varsa, bu özelliği kullanmayın.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Kaynak planlama performansı geliştirme özelliğini etkinleştirme
Kaynak planlama performansı geliştirmeyi etkinleştirmek için aşağıdaki adımları tamamlayın.

1. **Özellik yönetimi** > **Tüm** seçeneğine gidin ve özellik listesinde, **Proje kaynak planlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini bulun.
2. **Şimdi etkinleştir**'i seçin.

> [!NOTE]
> Eğer özelliği listede bulamazsanız, listeyi yenilemek için **Güncelleştirmeleri denetle**'yi seçin.

3. Tarayıcınızı yenileyin ve **Proje yönetimi ve muhasebe** > **Dönemsel** > **Proje kaynakları** > **Tüm şirketler arasındaki kaynak takvimleri kapasitesini eşitle** seçeneğine gidin.
4. Önceki verileri kaldırmak için, **Var olan kapasite kayıtlarını kaldır** öğesini **Evet** olarak ayarlayın. Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.
5. **Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin. Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanması gerekmez.
6. **Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.
7. **Tamam**'ı seçin.

 > [!NOTE]
 > Bu işlem, genel verileri ortamınızdaki tüm şirketler arasında **ResCalendarCapacity** tablosuna dağıtır, bu nedenle toplu işin yalnızca bir yasal varlıkta çalıştırılması gereklidir. Bu toplu işteki veriler, kaynak kapasitesini ilişkili takvimle hesaplamak için gereklidir.

8. **Proje yönetimi ve muhasebe** > **Dönemsel** > **Proje kaynakları** > **Proje kaynaklarını tüm şirketlerde doldur** öğesine gidin **Tamam**'ı seçin. Bu; **ResProjectResource**, **ResCalendarDateTimeRange** ve **ResEffectiveDateTimeRange** tablolarındaki genel veriler için veri yükseltme kodudur. **PSAPRojSchedRole.RootActivity** alanı değerleri de güncelleştirilir. Bu çalıştırılmadıysa, kaynak planlama işlemlerini yürütmeye çalıştığınızda bir uyarı alırsınız.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Kaynak planlama performansı geliştirmeyi kapatma

1. **Özellik yönetimi** > **Tüm** seçeneğine gidin ve **Proje kaynak planlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini bulun.
2. Özelliği seçin ve **Devre dışı bırak** düğmesini seçin.
3. Tarayıcınızı yenileyin.
4. **Proje yönetimi ve muhasebe** > **Dönemsel** > **Kapasite eşitleme** > **Kaynakların kapasite toplamlarını eşitle** seçeneğine gidin.
5. **Kapasite toplama eşitleme** sayfasında, önceki verileri kaldırmak için, **Var olan kapasite kayıtlarını kaldır** seçeneğini **Evet** olarak ayarlayın. Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.
6. **Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin. Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanması gerekmez.
7. **Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.
8. **Tamam**'ı seçin.

> [!NOTE]
> Bu işlem, genel verileri ortamınızdaki tüm şirketler arasında **ResRollup** tablosuna dağıtır, bu nedenle toplu işin yalnızca bir yasal varlıkta çalıştırılması gereklidir. Bu toplu iş, tüm **Kaynak kullanılabilirliği** görünümlerinde gereklidir. Bu toplu iş çalıştırılmazsa, **ResRolluo** verileri yeniden oluşturulur ve bu işlem zaman alabilir.

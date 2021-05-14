---
title: Stok hareketlerini arşivleme
description: Bu konuda, sistem performansını artırmaya yardımcı olmak için stok hareketi verilerinin nasıl arşivleneceği açıklanmaktadır.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 0526eb42a886817d50e1ecfd252a6e971875ba92
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956070"
---
# <a name="archive-inventory-transactions"></a>Stok hareketlerini arşivleme

[!include [banner](../../includes/banner.md)]

Zamanla, stok hareketleri tablosu (`InventTrans`) büyümeye ve daha fazla veritabanı alanı tüketmeye devam eder. Bu nedenle, tabloya göre yapılan sorgular zamanla yavaşlar. Bu konuda, sistem performansını artırmaya yardımcı olmak için stok hareketleri hakkındaki verileri arşivlemek için *Stok hareketlerini arşivleme* özelliğini nasıl kullanabileceğiniz açıklanmaktadır.

> [!NOTE]
> Seçili kapalı genel muhasebe döneminde yalnızca mali olarak güncelleştirilmiş stok hareketleri arşivlenebilir. Arşivlenebilmesi için mali olarak güncelleştirilmiş gidiş stok hareketlerinin *Satıldı* çıkış durumuna sahip olması ve geliş stok hareketlerinin giriş durumunun *Satın alındı* olması gerekir.

Stok hareketlerini arşivlediğinizde, ilgili tüm hareketler `InventTransArchive` tablosuna taşınır. Stok çıkış hareketleri ve stok girişi hareketleri, madde kodu (`itemId`) ve stok boyutu kimliği (`inventDimId`) kombinasyonuna göre ayrı ayrı arşivlenir ve özetlenen çıkış ve özetlenen giriş hareketlerine yerleştirilir.

Bir `itemId` ve `inventDimId` kombinasyonu yalnızca bir giriş veya çıkış hareketi içeriyorsa hareket arşivlenmez.

## <a name="turn-on-the-feature-in-your-system"></a>Sisteminizdeki özelliği etkinleştirme

Sisteminiz bu konuda açıklanan özellikleri zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Stok hareketlerini arşivleme* özelliğini açın. Bu özelliğin etkinleştirildikten sonra devre dışı bırakılamayacağını unutmayın.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Stok hareketlerini arşivlemeden önce dikkat edilmesi gerekenler

Stok hareketlerini arşivlemeden önce, işlemden etkilenecekleri için aşağıdaki iş senaryolarını göz önünde bulundurmalısınız:

- Satın alma siparişi satırları gibi ilgili belgelerden stok hareketlerini denetlediğinizde, bunlar arşivlenmiş olarak gösterilir. Arşivlenen hareketleri gözden geçirmek için **Stok yönetimi \> Periyodik görevler \> Temizleme \> Stok hareketlerini arşivleme**'ye gitmelisiniz.
- Arşivlenen dönemler için stok kapanışı iptal edilemez. Stok kapanışını iptal etmek için önce ilgili döneme ait stok hareketi arşivini tersine çevirmeniz gerekir.
- Arşivlenen dönemler için standart maliyet dönüştürme işlemi yapılamaz. Standart maliyet dönüştürmeyi yapmadan önce, ilgili dönem için stok hareketi arşivini tersine çevirmeniz gerekir.
- Stok hareketlerini arşivlediğinizde, stok hareketlerinden elde edilen stok raporları etkilenir. Bu raporlar stok yaşlandırma raporunu ve stok değer raporlarını içerir.
- Stok tahminleri, arşivlenen dönemlerin öngörülen süreleri sırasında çalıştırılırsa etkilenebilir.

## <a name="prerequisites"></a>Önkoşullar

Stok hareketleri yalnızca aşağıdaki koşulların karşılandığı dönemlerde arşivlenebilir:

- Genel muhasebe dönemi kapatılmalıdır.
- Stok kapanışı, arşivin dönem bitiş tarihinde veya sonrasında çalıştırılmalıdır.
- Dönem, arşivin dönem tarihinden en az bir yıl önce olmalıdır.
- Mevcut stok yeniden hesaplamaları bulunmamalıdır.

## <a name="archive-inventory-transactions"></a>Stok hareketlerini arşivleme

Stok hareketlerini arşivlemek için bu adımları izleyin.

1. **Stok yönetimi** \> **Periyodik görevler** \> **Temizleme** \> **Stok hareketlerini arşivleme**’ye gidin.

    **Stok hareketlerini arşivleme** sayfası görüntülenir ve arşivlenen işlem kayıtlarının listesini gösterir.

    ![Stok hareketlerini arşivleme sayfası](media/archive-inventory-empty.png "Stok hareketlerini arşivleme sayfası")

1. Stok hareketi arşivi oluşturmak için Eylem Bölmesinde **Stok hareketlerini arşivleme**'yi seçin.
1. **Stok hareketlerini arşivleme** iletişim kutusunda, **Parametreler** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **Kapalı genel muhasebe dönemindeki başlangıç tarihi**: Arşive dahil edilecek en erken hareket tarihini seçin.
    - **Kapalı genel muhasebe dönemindeki bitiş tarihi**: Arşive dahil etmek için en son hareket tarihini seçin.

    ![Stok hareketlerini arşivleme iletişim kutusu](media/archive-inventory-dates.png "Stok hareketlerini arşivleme iletişim kutusu")

    > [!NOTE]
    > Yalnızca [ön koşulları](#prerequisites) karşılayan dönemler seçim için kullanılabilir.

1. **Arka planda çalıştır** hızlı sekmesinde, toplu işleme ayrıntılarını gerektiği gibi ayarlayın. Microsoft Dynamics 365 Supply Chain Management'taki toplu işler için tipik adımları izleyin.
1. **Tamam**'ı seçin.
1. Devam etmek istediğinizi onaylamanızı isteyen bir ileti alırsınız. İletiyi dikkatlice okuyun ve devam etmek istiyorsanız **Evet**'i seçin.

    Stok hareketlerini arşivleme işinizin toplu iş kuyruğuna eklendiğini bildiren bir ileti alırsınız. İş artık seçili dönemdeki stok hareketlerini arşivlemeye başlayacaktır.

## <a name="view-archived-inventory-transactions"></a>Arşivlenmiş stok hareketlerini görüntüle

**Stok hareketlerini arşivleme** sayfası arşivleme geçmişinizin tamamını gösterir. Kılavuzdaki her satır, arşivin oluşturulduğu tarih, oluşturan kullanıcı ve durumu gibi bilgileri gösterir.

![Stok hareketlerini arşivleme sayfasındaki arşivleme geçmişi](media/archive-inventory-full.png "Stok hareketlerini arşivleme sayfasındaki arşivleme geçmişi")

Sayfanın üst kısmında açılan listede, kılavuzda gösterilen arşivlere filtre uygulamak için aşağıdaki değerlerden birini seçin:

- **Etkin**: Ters çevrilen arşivleri değil, yalnızca etkin arşivleri göster.
- **Tümü**: Hem etkin hem de ters çevrilen tüm arşivleri gösterir.

Kılavuzdaki her arşiv için aşağıdaki bilgiler sağlanır:

- **Etkin**: Onay işareti arşivin etkin olduğunu gösterir.
- **Başlangıç tarihi**: Arşive dahil edilebilen en eski hareketin tarihi.
- **Son tarih**: Arşive dahil edilebilen en son hareketin tarihi.
- **Zamanlayan**: Arşivi oluşturan kullanıcı hesabı.
- **Yürütülme tarihi**: Arşivin oluşturulduğu tarih.
- **Ters**: Onay işareti arşivin tersine çevrildiğini gösterir.
- **Geçerli güncelleştirmeyi durdur**: Onay işareti arşivin devam ettiğini ancak duraklatıldığını gösterir.
- **Durum**: Arşivin işleme durumu. Olası değerler *Beklemede*, *Devam Ediyor* ve *Tamamlandı*'dır.

Kılavuzun üstündeki araç çubuğu, seçili bir arşivle çalışmak için kullanabileceğiniz aşağıdaki düğmeleri sağlar:

- **Arşivlenen hareketler**: Seçili arşivin tüm ayrıntılarını görüntüleyin. Görüntülenen **Arşivlenen hareketler** sayfası arşivdeki tüm hareketleri gösterir.

    ![Arşivlenen hareketler sayfası](media/archive-inventory-transactions.png "Arşivlenen hareketler sayfası")

    **Arşivlenen hareketler** sayfasında belirli bir hareket hakkında daha fazla bilgi görüntülemek için kılavuzda hareketi seçin ve sonra eylem bölmesinde **Arşivlenen işlem ayrıntıları**'nı seçin. Görüntülenen **Arşivlenen hareket ayrıntıları** sayfası, genel muhasebe deftere nakli, ilgili alt genel muhasebe referansları ve mali boyutlar gibi bilgileri gösterir.

- **Arşivlemeyi duraklat**: İşlenmekte olan seçili arşivi duraklatın. Duraklatma yalnızca arşivleme görevi oluşturulduktan sonra etkinleşir. Bu nedenle, duraklatma etkili olmadan önce kısa bir gecikme olabilir. Bir arşiv duraklatılmışsa **Geçerli güncelleştirmeyi durdur** alanında bir onay işareti görünür.
- **Arşivlemeye devam et**: Şu anda duraklatılmış olan seçili bir arşiv için işlemeyi devam ettirir.
- **Ters Çevir**: Seçili arşivi ters çevirin. Arşivi yalnızca **Durum** alanı *Tamamlandı* olarak ayarlanmışsa tersine çevirebilirsiniz. Arşiv tersine çevrilmişse **Ters** alanında bir onay işareti görünür.

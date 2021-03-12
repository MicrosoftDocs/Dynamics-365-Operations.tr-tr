---
title: Dynamics 365 Commerce'de ürün derecelendirmelerini eşitleme
description: Bu konu, Microsoft Dynamics 365 Commerce ürün derecelendirmelerinin nasıl eşitleneceğini açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7318d53535a93352425f811ec90572e65aeb696
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006297"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'de ürün derecelendirmelerini eşitleme

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce ürün derecelendirmelerinin nasıl eşitleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir satış noktasında (POS) ve çağrı merkezlerindeki gibi, çok yönlü kanallar içindeki ürün derecelendirmelerini kullanmak için, derecelendirmeler ve İncelemeler hizmetindeki ürün derecelendirmeleri Commerce kanal veritabanına alınmalıdır. Çok yönlü kanallarda ürün derecelendirmeleri sunulduklarında, müşterilerin satış ilişkileri ile etkileşimleri sırasında dolaylı olarak müşterilere yardımcı olabilirler.

Bu konuda şu görevler açıklanmıştır:

1. Ürün derecelendirmelerini **derecelendirmeler ve İncelemeler hizmetinden** eşitlemek için **ürün derecelendirmeleri eşitleme işini** bir toplu iş olarak konfigüre edin.
1. Ürün değerlendirme eşitlemesiyle ilgili toplu işin başarılı olduğunu doğrulayın.
1. Ürün derecelendirmelerini POS'ta kullanılabilir yapın.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>Ürün derecelendirmelerini eşitlemek için bir toplu işi konfigüre edin.

> [!IMPORTANT]
> Başlamadan önce, Dynamics 365 Commerce sürüm 10.0.6 veya sonraki sürümünün yüklü olduğundan emin olun.

### <a name="initialize-the-commerce-scheduler"></a>Commerce Planlayıcısını Başlat

Tiaret planlayıcısı başlatmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Genel merkez ayarı \> Commerce planlayıcısı \> Commerce planlayıcısını başlat**'a gidin. Alternatif olarak "Ticaret Planlayıcısı Başlat"ı arayın.
1. **Ticaret Planlayıcısı Başlat** iletişim kutusunda, **varolan konfigürasyonu Sil** seçeneğinin **Hayır** olarak ayarlandığından emin olun ve **Tamam**'ı seçin.

### <a name="verify-the-retailproductrating-subjob"></a>RetailProductRating alt işini doğrulayın

**RetailProductRating** alt işinin var olduğunu doğrulamak için, aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Genel merkez ayarı \> Commerce planlayıcısı \> Planlayıcı alt işleri**'ne gidin. Alternatif olarak, "Planlayıcı alt işleri"ni aratın.
1. Alt iş listesinde, **RetailProductRating** alt işini bulun veya arayın.

Aşağıdaki çizimde Commerce'de alt iş örneği gösterilmektedir.

![RetailProductRating alt işi ayrıntıları](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> **RetailProductRating** alt işi bulamazsanız, Commerce Planlayıcısını çalıştırmadan önce **ürün derecelendirmelerini Eşitle** işini ve **1040 CDX** işini zaten çalıştırılmış olabilirsiniz. Bu durumda, **tam veri eşitleme** işini çalıştırmak için aşağıdaki adımları izleyin.

> 1. **Retail ve Commerce \> Genel merkez ayarı \> Commerce planlayıcısı \> Kanal veritabanı**'na gidin. Alternatif olarak, "kanal veritabanı" için arama yapın.
> 1. Eşitlenecek kanal veritabanını seçin.
> 1. Eylem bölmesinde **tam veri eşitleme**'yi tıklatın.
> 1. **Dağıtım zamanlaması seç** açılan iletişim kutusunda **1040 ürünleri** seçin ve **Tamam** 'ı seçin.
> 1. **RetailProductRating** alt işin oluşturulduğunu doğrulamak için önceki yordamın adımlarını yineleyin.

### <a name="import-product-ratings"></a>Ürün derecelendirmelerini içeri aktar

Derecelendirmeler ve İncelemeler hizmetinden ürün derecelendirmelerini Commerce olarak içe aktarmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Yönetim Merkezi ayarı \> Commerce Planlayıcısı \> Ürün derecelendirme işini eşitle**'ye gidin. Alternatif olarak, "ürün derecelendirme işini Eşitle" yi aratın.
1. **Ürün derecelendirmelerini al** iletişim kutusunda, **arka planda çalıştır** hızlı sekmesinde **tekrarlama**'yı seçin.
1. **Tekrarı tanımla** iletişim kutusunda bir yinelenme düzeni ayarlayın. (Önerilen değer iki saattir.) Bir saatten az olan bir tekrarı planlanmayın.
1. **Tamam**'ı seçin.
1. **Toplu işleme** seçeneğini **Evet** olarak ayarlayın. Bu ayar, günlükleri denetlemenize ve toplu işin durumunu doğrulayabileceğinizi garantilemeye yarar.
1. Toplu işi planlamak için **Tamam**'ı seçin.

Aşağıdaki çizimde Commerce'de toplu iş yapılandırması gösterilmektedir.

![Ürün derecelendirmeleri eşitleme toplu işleminin konfigürasyonu](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>Ürün değerlendirme eşitlemesiyle ilgili toplu işin başarılı olduğunu doğrulayın

**Ürün derecelendirmeleri eşitleme** toplu işleminin başarılı olduğunu doğrulamak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> sistem yöneticisi \> sorgular \> toplu işler**'e gidin veya yalnızca Commerce stok tutma birimi (SKU) kullanıyorsanız **Retail ve Commerce \> Sorgular ve raporlar \> toplu işler**'e gidin. Alternatif olarak, "toplu işler"i arayın.
1. Toplu işin ayrıntılarını görüntülemek için, toplu iş listesinde, **iş açıklaması** sütununda "Ürün derecelendirmelerini al" içeren bir açıklama arayın.
1. Planlanan başlangıç tarihi/saati ve yinelenme metni gibi toplu iş ayrıntılarını görüntülemek için iş kodunu seçin.

Aşağıdaki şekil toplu iş, iki saatlik aralıklarla çalışacak şekilde zamanlandığında, toplu iş ayrıntılarının Commerce olarak bir örneğini gösterir.

![Ürün derecelendirmesi eşitleme işinin ayrıntıları](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>Ürün derecelendirmelerini POS'ta kullanılabilir yapın

Dynamics 365 Commerce'deki derecelendirmeler ve İncelemeler çözümü bir çok yönlü kanal çözümüdür. Ancak, ürün derecelendirmeleri POS'ta varsayılan olarak gösterilmez. Mağazalardaki müşterilere yardım etmek için, satış görevlileri tarafından yardım edilmekte olduğunda derecelendirmelere ve incelemelere bakın.

POS'ta ürün derecelendirmelerini açmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Commerce ayarı \> Parametreler \> Commerce parametreleri**'ne gidin. Alternatif olarak, "Commerce parametreleri"ni arayın.
1. **Konfigürasyon** parametreleri sekmesinde, **yeni**'yi seçin.
1. **RatingsAndReviews.EnableProductRatingsForRetailStores** gibi bir ad girin ve değeri **doğru** olarak ayarlayın.
1. **Kaydet**'i seçin.
1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin. Alternatif olarak, "dağıtım zamanlaması" için arama yapın.
1. İş listesinde, **1110** (**Global konfigürasyon**) öğesini seçin ve **şimdi Çalıştır**'ı seçin.
1. İş başarıyla çalıştırıldıktan sonra, ürün derecelendirmelerinin POS'ta şimdi gösterildiğini doğrulayın.

Aşağıdaki çizimde, POS'ta ürün derecelendirmelerinin açılacağı Commerce parametrelerinin konfigürasyonunda bir örnek gösterilmektedir.

![POS'ta ürün değerlendirmeleriyle ilgili Commerce parametrelerinin konfigürasyonu](media/rnr-hq-enable-ratings-in-pos.png)

Aşağıdaki çizim, POS'ta ürün derecelendirmeleri örneğini gösterir.

![POS'ta ürün derecelendirmeleri](media/rnr-pos-catalog-ratings.png)

Aşağıdaki çizim, çağrı merkezi kanallarında ürün derecelendirmeleri örneğini gösterir.

![Çağrı merkezi kanalında ürün derecelendirmeleri](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirme ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri kullanmayı kabul etme](opt-in-ratings-reviews.md)

[Derecelendirme ve incelemeleri yönetme](manage-reviews.md)

[Derecelendirme ve incelemeleri yapılandırma](configure-ratings-reviews.md)

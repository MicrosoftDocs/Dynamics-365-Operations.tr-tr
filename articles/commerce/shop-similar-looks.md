---
title: "\"Benzer görünüme sahip ürünler\" önerilerini etkinleştirme"
description: Bu makalede, Microsoft Dynamics 365 Commerce'ta "benzer görünümleri araştır" ürün önerilerinin nasıl etkinleştirileceği açıklanmaktadır.
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3024e832de5e6a60b49c5b0c8bfbe36b2c416379
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884589"
---
# <a name="enable-shop-similar-looks-recommendations"></a>"Benzer görünüme sahip ürünler" önerilerini etkinleştirme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'ta "benzer görünümleri araştır" ürün önerilerinin nasıl etkinleştirileceği açıklanmaktadır.

Dynamics 365 Commerce' taki "benzer görünümleri araştır" önerileri özelliği, müşterilere görsel olarak benzer ürünler için öneri sağlamak amacıyla yapay zeka ve makine öğreniminden (AI-ML) yararlanır. Commerce'taki tüm perakende kanallarında "benzer görünümleri araştır" önerileri kullanılabilir duruma getirildiğinde, perakendeciler müşterilerin istediklerini kolayca bulmasına yardımcı olarak müşteri memnuniyetini artırabilir.

"Benzer görünümleri araştır" önerileri için işlevsellik, perakendecinin ürün kataloğundaki görsel olarak benzer ürünleri bulmak ve önermek için çekirdek ürün varyantlarının ürün görüntülerini kullanır. 

"Benzer görünümler araştır" önerileri hem satış noktasında (POS) hem de e-ticaret deneyimlerinde kullanılabilir.

### <a name="example-scenarios"></a>Örnek senaryolar

- Müşteri siyah çizgili bir kazak görüntüler ve benzer kazağın kırmızı rengi için bir öneri alır. Müşteri, başlangıçta görüntülediği ürün yerine önerilen ürünü seçer ve kırmızı renkli benzer ürünler için öneriler alır. 
- Müşteri satın alma işlemi sırasında ilgilendiği bir yüzükle eşleşen küpeler bulmak için "benzer görünümler araştır" önerilerini kullanır.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Commerce Headquarters'da "benzer görünümler araştır" önerilerini etkinleştirme

Ürün önerileri, yalnızca depolama alanlarını depolama alanını Azure Data Lake Gen2'ye taşıyan Commerce kullanıcıları için desteklenir.

### <a name="prerequisites"></a>Önkoşullar

Perakendeciler müşterilere "benzer görünümler araştır" önerileri göstermeye başlamadan önce, iki önkoşul adımı vardır:

- Commerce Headquarters'da [ürün önerilerini etkinleştirin](enable-product-recommendations.md).
- Ortam sunucusunun HTTPS çağrılarını desteklediğini doğrulayın.

Öneriler altyapısının ürün görüntülerine erişmesi için perakendecilerin ürün URL'leri oluşturmaları gerekir. Commerce Headquarters'da ürün URL'leri oluşturmak için aşağıdaki adımları izleyin.

1. **Ürün görüntüleri**'ne gidin.
1. Eylem bölmesinde, **Medya şablonu tanımla**'yı seçin.
1. **Medya şablonu tanımla** özellikleri bölmesinde, **Medya URL'leri** altından **URL Oluştur**'u seçin.

> [!NOTE]
> "Benzer görünümleri araştır" önerileri özelliğini etkinleştirdiğinizde, ürün öneri listeleri oluşturma işlemi başlar. Bu listelerin kullanılabilmesi ve çevrimiçi olarak ve POS terminalinde görülebilmesi için bir güne kadar gerekli olabilir.

Commerce Headquarters'da "benzer görünümleri araştır" önerileri özelliğini etkinleştirmek için, aşağıdaki adımları izleyin.

1. **Özellik yönetimi**'ne gidin.
1. Kullanılabilir özellikler listesinde, **Benzer görünümleri araştır**'ı seçin.
1. Sağ bölmede, hizmeti açmak için **Etkinleştir**'i seçin.

Aşağıdaki şekilde, Commerce Headquarters'daki **Özellik Yönetimi** sayfasında bulunan **Benzer görünümleri araştır** özelliği gösterilmektedir.

![Commerce Headquarters'daki Özellik Yönetimi sayfasında bulunan Benzer görünümleri araştır özelliği.](./media/enableshopsimilarlooks.png)

Önceki görevler tamamlandıktan sonra, POS terminalleri otomatik olarak bağlamsal bir **Benzer görünümleri araştır** paneliyle geliştirilir. **Daha fazlasını gör** öğesini seçerek POS terminali kullanıcıları daha fazla filtreleme yapabilecekleri özel bir "benzer görünümleri araştır" sayfasına gidebilir.

> [!NOTE]
> "Benzer görünümleri araştır" önerileri özelliğini kapatırsanız, diğer ürün önerisi türleri etkilenmez. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Commerce site oluşturucusunu kullanarak ürün ayrıntı sayfalarına Benzer görünümleri araştır düğmesi ekleme

Commerce Headquarters'da "benzer görünümleri araştır" önerileri özelliğini etkinleştirdikten sonra, Commerce site oluşturucusundaki bir seçenek perakendecilerin herhangi bir ürün ayrıntısı sayfasındaki (PDP) satın alma kutusuna **Benzer görünümleri araştır** düğmesi eklemesine olanak tanır. Bu düğmeyi seçen bir müşteri, görsel olarak benzer ürünler döndüren özel bir "benzer görünümleri araştır" sayfasına götürülür. Burada, müşteri ürünleri daha fazla filtrelemek için seçicileri kullanabilir.

Commerce site oluşturucusunu kullanarak PDP'ye **Benzer görünümleri araştır** düğmesi eklemek için aşağıdaki adımları izleyin.

1. Satın alma kutusu modülünü içeren mevcut bir site oluşturucu sayfasını açın.
1. Soldaki gezinti bölmesinde satın alma kutusu modülünü seçin.
1. Sağ gezinti bölmesinde, **Benzer Görünümler Araştır Bağlantısını Etkinleştir** onay kutusunu seçin.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin. Sayfa yayımlandıktan sonra PDP bir **Benzer görünümler araştır** düğmesi içerir.

Aşağıdaki şekilde, **Benzer Görünümler Araştır Bağlantısını Etkinleştir** onay kutusu ve site oluşturucudaki bir PDP örneğinde bulunan **Benzer görünümler araştır** düğmesi gösterilmektedir.

![Benzer Görünümler Araştır Bağlantısını Etkinleştir onay kutusu ve site oluşturucudaki bir PDP'deki Benzer görünümler araştır düğmesi.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

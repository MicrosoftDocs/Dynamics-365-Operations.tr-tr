---
title: Ürün önerilerine genel bakış
description: Bu makalede ürün önerileri hakkında genel bilgiler verilmiştir. Ürün önerileri, müşterilerin istedikleri ürünleri ve hatta satın almayı amaçlamadıkları ürünleri kolayca ve hızlı bir şekilde bulmasına olanak tanır.
author: Moonma
ms.date: 05/26/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb62638e89dd9cd7c01739244d808f664b3f3b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867744"
---
# <a name="product-recommendations-overview"></a>Ürün önerilerine genel bakış

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce, e-ticaret Web sitesi ve satış noktası (POS) aygıtında ürün önerilerini göstermek için kullanılabilir. Ürün önerileri, bir müşterinin ilgilendiği öğelerdir. Öneriler, çevrimiçi ve fiziksel mağazalardaki diğer müşterilerin satın alma eğilimlerine dayanır.

Ürün önerileri, müşterilerin kendilerine hizmet veren bir deneyim sağlarken istedikleri ürünleri kolayca ve hızlı bir şekilde bulmasına olanak tanır. Çapraz satış ve yukarı satış, müşterilerin başlangıçta satın almayı amaçlamadıkları ek ürünler bulmasına yardımcı olmak için de kullanılabilir. Öneriler, ürün bulmayı geliştirmek için kullanıldığında, daha fazla dönüştürme fırsatı oluşturabilir, satış gelirini artırabilir ve hatta müşteri memnuniyetini ve korunmasını bile yükseltebilir.

e-Ticarette, ürün önerileri büyük ölçekli Microsoft önerileri makine öğrenme teknolojileriyle desteklenmektedir.

Bu hizmet Dynamics 365 Commerce'a bir eklentidir. Daha fazla bilgi için, en son [Microsoft Dynamics 365 Lisans kılavuzunu](https://go.microsoft.com/fwlink/?LinkId=866544) indirin.


## <a name="recommendation-service"></a>Öneri servisi

Ürün önerileri hizmeti, yapay zeka ve makine öğrenimi (AI-ML) teknolojilerini aşağıdaki şekilde kullanır:

- Öneri servisinin tarafından istenen biçimdeki veriler Commerce işlem veritabanından çıkarılması ve Azure Data Lake Storage veya Varlık deposuna göndermesi gerekir.
- Öneriler hizmeti, depolanan verileri **Bunlar da beğenildi**, **Sıklıkla birlikte satın alınan**, **Yeni**, **En çok satan** ve **Popüler** listeleri için öneri modelleri eğitmek üzere kullanır.

## <a name="scenarios"></a>Senaryolar

Ürün önerileri aşağıdaki senaryoları için etkinleştirilir.

- **E-ticaret 'da gözatma veya iniş sayfası için herhangi bir depolama sayfasında:** Müşteriler veya mağaza işbirlikçileri bir mağaza sayfasını ziyaret ederken, öneri altyapısı **yeni**, **en iyi satış** ve **trend** listelerinde ürünler önerebilir.
- **Ürün Ayrıntıları sayfasında:** müşteriler veya mağaza işbirlikçileri bir **ürün ayrıntıları** sayfasını ziyaret ederken, öneri altyapısı da büyük olasılıkla satın alınacak ek maddeleri önerir. Bu öğeler, **kişiler bunları da sevdi** listesinde görünür.
- **Hareket sayfasında veya kullanıma al sayfasında:** öneri altyapısı maddeleri sepetteki tüm madde listesine göre önerir. Bu maddeler **sık kullanılan bir arada** bulunan listesinde görünür.
- **Kişiselleştirilmiş öneriler:** Tacirler, varolan liste senaryolarının o müşteriye dayalı olarak kişiselleştirilmelerini sağlayan yeni işlevlere ek olarak, oturum açmış, **sizin için kişiselleştirilmiş** bir çekme müşterilerine olanak sağlayabilir. Daha fazla bilgi edinmek için bkz. [Kişiselleştirilmiş önerileri etkinleştirme.](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Ürün önerileri türleri

Aşağıdaki tabloda, perakendecilerin Dynamics 365 Commerce çözümlerinde [ürün koleksiyonu modülü](product-collection-module-overview.md) aracılığıyla uygulayabilecekleri için çeşitli otomatik ürün önerisi türleri açıklanmıştır. Perakendeciler site yazarı bu seçeneği seçerse, oturum açmış bir kullanıcının kişiselleştirilmiş sonuçlarını gösterebilir.

| Ürün topluluğu modülü  | Türü | Tanım |
|----------------------------|------|-------------|
| Yeni                        | Algoritmik | Bu modül, kanallarda ve kataloglarda yakın zamanda sıralanmış en yeni ürünlerin listesini gösterir. |
| En iyi satış               | Algoritmik | Bu modül, en yüksek sayıda satış ile derecelendirilen ürünlerin listesi. |
| Popüler                   | Algoritmik | Bu modül belirli bir döneme ait en yüksek performanslı ürünlerin listesini, en yüksek satış sayısına göre sıralayarak gösterir.  |
| Sıklıkla birlikte satın alınan | AI-ML | Bu modül, tüketicilerin geçerli sepet içeriğiyle birlikte yaygın olarak satın alınan ürünlerin listesini önerir. |
| Diğer sevilen ürünler           | AI-ML | Bu modül, tüketicinin satın alma modellerine dayalı olarak, belirli bir temel ürün için ürünler önerir. |
| Size özel çekmeler              | AI-ML | Bu modül, oturum açmış kullanıcının satınalma kalıplarını temel alan kişiselleştirilmiş bir ürün listesi önerir. Konuk Kullanıcı için bu liste daraltılacak. |

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

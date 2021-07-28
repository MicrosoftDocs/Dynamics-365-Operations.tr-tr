---
title: "\"Benzer ürünler açıklaması\" önerilerini etkinleştirme"
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta "benzer ürünler açıklaması" ürün önerilerinin nasıl etkinleştirileceği açıklanmaktadır.
author: bsokolov
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: baf6064fbddc3b49cfb0d950896c0b448bddb560
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357798"
---
# <a name="enable-shop-similar-description-recommendations"></a>"Benzer ürünler açıklaması" önerilerini etkinleştirme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta "benzer ürünler açıklaması" ürün önerilerinin nasıl etkinleştirileceği açıklanmaktadır.

Dynamics 365 Commerce'teki "benzer ürünler açıklaması" önerileri özelliği, müşterinin aradığı açıklamaya benzer açıklamalara sahip ürünler için öneriler sunmak üzere yapay zeka ve makine öğrenimi (AI-ML) kullanır. Commerce'teki tüm perakende kanallarında "benzer ürün açıklaması" önerileri kullanılabilir duruma getirildiğinde, perakendeciler müşterilerin istediklerini kolayca bulmasına yardımcı olabilir.

"Benzer ürün açıklaması" önerileri için işlevsellik, perakendecinin ürün kataloğundaki benzer ürünleri bulmak ve önermek için çekirdek ürünlerin ürün adını ve açıklamasını kullanır.

"Benzer ürün açıklaması" önerileri hem satış noktasında (POS) hem de e-ticaret deneyimlerinde kullanılabilir.

## <a name="example-scenarios"></a>Örnek senaryolar

Aşağıdaki örnek senaryolar, "Benzer ürün açıklaması" işlevinin sağlayabileceği öneri türlerini gösterir:

- Bir müşteri, bir dizi retro, kemik tipi gözlük görüntüler ve benzeri bir tasarıma sahip diğer gözlükler için satıcının sektörü bağlamında bir dizi öneri alır.
- Bir müşteri, daha önce perakendeciden satın aldıkları bir tadla benzerlik gösteren kahve tadlarını bulmak için "benzer ürün açıklaması" önerilerini kullanır.

## <a name="set-up-shop-similar-description-recommendations"></a>"Benzer ürünler açıklaması" önerilerini ayarlama

Ürün önerileri, yalnızca depolama alanlarını depolama alanını Azure Data Lake Storage Gen2'ye taşıyan Commerce kullanıcıları için desteklenir.

### <a name="prerequisites"></a>Önkoşullar

"Benzeri ürün açıklaması" önerilerini müşterilere göre gösterilebilmeniz için aşağıdaki önkoşulları tamamlamanız gerekir:

- Commerce Headquarters'da [ürün önerilerini etkinleştirin](enable-product-recommendations.md).
- Ortam sunucusunun HTTPS çağrılarını desteklediğini doğrulayın.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>"Benzer ürün açıklaması" önerileri özelliğini etkinleştirme

Commerce Headquarters'da "benzer ürün açıklaması" önerileri özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Özellik yönetimi** çalışma alanında, kullanılabilen özellikler listesinde, **Benzer ürün açıklaması**'nı arayıp seçin.
1. Sağdaki bölmeden **Etkinleştir**'i seçin.

> [!NOTE]
> Özelliği etkinleştirdiğinizde, sistem, ürün öneri listeleri oluşturmaya başlar. Bu listelerin kullanılabilmesi ve çevrimiçi olarak ve POS terminalinde görülebilmesi bir gün sürebilir.
>
> Bu özelliği kapatırsanız diğer ürün önerisi türleri etkilenmez. Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Ürün ayrıntıları sayfalarına, Benzer ürün açıklaması düğmesi ekleyin

Commerce Headquarters'da "benzer ürün açıklaması" önerileri özelliğini etkinleştirdikten sonra, herhangi bir ürün ayrıntısı sayfasındaki (PDP) satın alma kutusuna **Benzer ürün açıklaması** düğmesi ekleyebilirsiniz. Bu düğmeyi seçen bir müşteri, görsel olarak benzer ürünler gösteren özel bir **Benzer ürün açıklaması** sayfasına götürülür. Müşteri ürünleri daha fazla filtrelemek için seçicileri kullanabilir.

Commerce site oluşturucusunu kullanarak PDP'ye **Benzer ürün açıklaması** düğmesi eklemek için aşağıdaki adımları izleyin.

1. Satın alma kutusu modülünü içeren mevcut bir site oluşturucu sayfasını açın.
1. Soldaki gezinti bölmesinde satın alma kutusu modülünü seçin.
1. Sağ bölmede, **Benzer ürün açıklaması bağlantısını etkinleştir** onay kutusunu seçin.
1. **Kaydet**'i seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin. Sayfa yayımlandıktan sonra PDP bir **Benzer ürün açıklaması** düğmesi içerir.

Aşağıdaki şekilde, **Benzer ürün açıklaması Bağlantısını Etkinleştir** onay kutusu ve site oluşturucudaki bir PDP örneğinde bulunan **Benzer ürün açıklaması** düğmesi gösterilmektedir.

![Benzer ürün açıklaması Bağlantısını Etkinleştir onay kutusu ve site oluşturucudaki bir PDP'deki Benzer ürün açıklaması düğmesi.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

["Benzer görünümdeki mağaza" önerilerini etkinleştirme](shop-similar-looks.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Ürün önerileri SSS](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
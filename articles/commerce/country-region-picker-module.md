---
title: Ülke/bölge seçici modülü
description: Bu makalede, ülke/bölge seçici modülü kapsanmaktadır ve bu modülün Microsoft Dynamics 365 Commerce'de nasıl yapılandırılacağı açıklanmaktadır.
author: stuharg
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: d20b3be008a37b1c86e6fefe0ccc90c581e18340
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862004"
---
# <a name="countryregion-picker-module"></a>Ülke/bölge seçici modülü

[!include [banner](includes/banner.md)]

Bu makalede, ülke/bölge seçici modülü kapsanmaktadır ve bu modülün Microsoft Dynamics 365 Commerce'de nasıl yapılandırılacağı açıklanmaktadır.

Ülke/bölge seçici modülü, ülkeleri veya bölgeleri ile ilişkili olmayan bir e-ticaret sitesi URL'si isteyen müşterilere önerilen siteleri göstermek için Dynamics 365 Commerce'te [coğrafi konum algılama ve yeniden yönlendirme](geo-detection-redirection.md) özelliğini kullanır.

Örneğin, Kanada dışındaki bir ülkede yaşayan bir müşteri Kanada ile ilişkilendirilmemiş bir site URL'si isteyebilir. Bu durumda, ülke/bölge seçici modülünde Kanada ile ilişkilendirilmiş site URL'lerini öneren bir iletişim kutusu gösterilir. 

## <a name="how-it-works"></a>Nasıl çalışır

Bir site için coğrafi algılama ve yeniden yönlendirme etkinleştirildiğinde ve bir müşteri bir site URL'si istediğinde, müşteri için algılanan ülke ve müşterinin istediği URL, bu URL'nin müşterinin bulunduğu ülkeyle eşlenip eşlenmediğini belirlemek için kullanılır. URL'ler ve ülkeler arasındaki eşleme, Commerce site oluşturucudaki **Site ayarları** altında bulunan **Kanallar** sayfasında tanımlanmıştır. 

İstek URL'si müşterinin ülkesiyle eşlenen herhangi bir URL ile eşleşmiyorsa, yanıtta bu ülkeyle eşlenen bir veya daha fazla URL listesi verilir. Ülke/bölge seçicisi, listedeki her URL'yi ülke/bölge modülünde yapılandırılmış olan URL'lerle karşılaştırır. Bulunan her tam eşleşme için ülke/bölge seçicisi, ilgili URL'deki görüntü başlığını, alt başlığı ve resmi işler ve URL'yi kullanarak bu öğelere köprü oluşturur.

Müşteri, ülke/bölge seçicisindeki bir seçeneği seçtiğinde, köprü oluşturulmuş URL'ye yönlendirilir. Bu URL, müşterinin site tercihi olarak kullanılabilmesi için **\_msdyn365\_\_\_site\_** tanımlama bilgisine yazılır. Daha sonra müşteri, ülke veya bölgeyle ilişkili olmayan bir URL'yi istediğinde, bunlar otomatik olarak müşterinin tercih edilen ülkesine yönlendirilir. Bu nedenle, e-ticaret sitenizdeki [site seçicisi modülünü](site-selector.md) kullanmanızı öneririz, böylece müşteriler kendi site tercihlerini geçersiz kılabilir veya güncelleştirebilir. 

Müşteri, ülke/bölge seçicisi iletişim kutusunu kapatırsa, tanımlama bilgisi yazılmaz ve müşteri geçerli sitede kalır. 

Aşağıdaki şekilde ülke/bölge seçici iletişim kutusunun bir örneği gösterilmektedir.

![Ana sayfadaki ülke/bölge seçici iletişim kutusu örneği.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Ülke/bölge seçici modülü özellikleri

| Özellik adı              | Değer       | Tanım                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Başlık                    | Metin        | İletişim kutusunun üst kısmında görüntülenen başlık.       |
| Alt başlık                 | Metin        | Başlığın altında görüntülenen alt başlık.               |
| Ülke: Görünen dize    | Metin        | URL seçeneğinin görünen adı (örneğin, "Kanada").   |
| Ülke: Görünen alt dize | Metin        | URL seçeneğinin isteğe bağlı görünen alt dizesi (örneğin, "İngilizce" veya "Fransızca"). |
| Ülke: Ülke görüntüsü     | Ortam varlığı | URL seçeneğiyle ilişkilendirilmiş isteğe bağlı görüntü (örneğin, Kanada bayrağının görüntüsü). |
| Ülke: Ülke URL'si       | Metin        | Yapılandırılan ülke/bölgenin site URL'si. Bu URL, Commerce site oluşturucudaki **Site ayarları** altında bulunan **Kanallar** sayfasında bu ülke/bölge için belirttiğiniz URL ile tam olarak aynı olmalıdır. Ek olarak, URL'nin etki alanı, e-ticaret ortamınızı oluştururken Commerce tarafından sağlanan site çalışma adresi değil, **Kanallar** sayfasındaki **Etki alanını eşleştir** alanında belirtilen özel etki alanı olmalıdır (örneğin, `https://<yourcompany>.commerce.dynamics.com/` URL'si). |
| Eylem bağlantısı                | Eylem bağlantısı | İletişim kutusunun alt kısmında görüntülenen isteğe bağlı bağlantı. Örneğin, bu bağlantı sitenin desteklediği tüm ülke ve bölgelerin listesini sağlayan dahili bir sayfayı gösterebilir. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Sayfaya ülke/bölge seçici modülü ekleme

Ülke/bölge seçici modülü, üst bilgi modülüne doğrudan veya paylaşılan bir parça aracılığıyla eklenebilir. Üst bilgi modülleri hakkında daha fazla bilgi için bkz. [Üst bilgi modülleri](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Commerce site oluşturucuda ülke/bölge seçici modülünü yapılandırma

> [!NOTE]
> Müşterilerinize önerdiğiniz URL'ler, ülke/bölge seçici modülünde ülke nesneleri olarak yapılandırılmalıdır.

Müşterilere göstermek ve önermek istediğiniz her site URL'si için Commerce site oluşturucudaki şu adımları izleyin.

1. Ülke/bölge seçici modülü yuvasını seçin.
1. Özellikler bölmesinde, **Ülke listesi** altında **Ülke ekle**'yi seçin.
1. Yeni **Ülke** kutusunu seçin.
1. **Görünen dize** alanına, bir görünen ad girin (örneğin, **Kanada**).
1. İsteğe bağlı: **Görünen alt dize** alanına (örneğin, **Fransızca** veya **fr-ca**) bir görünen alt dize girin.
1. İsteğe bağlı: Ortam kitaplığından bir görüntü seçin.
1. **Ülke URL'si** alanına URL'yi girin. Bu URL, **Kanallar** sayfasında görüntülenen ve ülke veya bölgeyle ilişkilendirilmiş yerel ayar da dahil olmak üzere kanalla eşlenen URL ile tam olarak eşleşmelidir. 
1. **Tamam**'ı seçin.
1. Ülke/bölge seçici modülünün göstermesini istediğiniz diğer ülke URL'leri için bu adımları tekrarlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Coğrafi konum algılama ve yeniden yönlendirme özelliğini ayarlama](geo-detection-redirection.md)

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Üst bilgi modülü](author-header-module.md)

[Site seçicisi modülü](site-selector.md)

[İçerik haritası modülü](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

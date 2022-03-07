---
title: Ülke/bölge seçici modülü
description: Bu konuda, ülke/bölge seçici modülü kapsanmaktadır ve bu modülün Microsoft Dynamics 365 Commerce'de nasıl yapılandırılacağı açıklanmaktadır.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 3134e10c096525ec2d82365a25eff16a3c5d5e11
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472693"
---
# <a name="countryregion-picker-module"></a>Ülke/bölge seçici modülü

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, ülke/bölge seçici modülü kapsanmaktadır ve bu modülün Microsoft Dynamics 365 Commerce'de nasıl yapılandırılacağı açıklanmaktadır.

Ülke/bölge seçici modülü, ülkeleri veya bölgeleri ile ilişkili olmayan bir e-ticaret sitesi URL'si isteyen müşterilere önerilen URL'leri göstermek için Dynamics 365 Commerce'te [coğrafi konum algılama ve yeniden yönlendirme](geo-detection-redirection.md) özelliğini kullanır.

Örneğin, Kanada'da yaşayan bir müşteri Kanada ile ilişkilendirilmemiş bir site URL'si isteyebilir. Bu durumda, ülke/bölge seçici modülünde Kanada ile ilişkilendirilmiş site URL'lerini öneren bir iletişim kutusu gösterilir. Aşağıdaki şekilde ülke/bölge seçici iletişim kutusunun bir örneği gösterilmektedir.

![Ana sayfadaki ülke/bölge seçici iletişim kutusu örneği.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Ülke/bölge seçici modülü özellikleri

| Özellik adı              | Değer       | Tanım |
| -------------------------- | ----------- | ----------- |
| Başlık                    | Metin        | İletişim kutusunun üst kısmında görüntülenen başlık. |
| Alt başlık                 | Metin        | Başlığın altında görüntülenen alt başlık. |
| Ülke: Görünen dize    | Metin        | URL seçeneğinin görünen adı (örneğin, "Kanada"). |
| Ülke: Görünen alt dize | Metin        | URL seçeneğinin isteğe bağlı görünen alt dizesi (örneğin, "İngilizce" veya "Fransızca"). |
| Ülke: Ülke görüntüsü     | Ortam varlığı | URL seçeneğiyle ilişkilendirilmiş isteğe bağlı görüntü (örneğin, Kanada bayrağının görüntüsü). |
| Ülke: Ülke URL'si       | Metin        | Commerce site oluşturucuda (**Site ayarları \> Kanallar**) **Kanallar** sayfasında ülke veya bölge için yapılandırılmış kanala ve yerel ayara karşılık gelen URL. Bu URL, **Kanallar** sayfasında yapılandırılan URL ile tam olarak eşleşmelidir. |
| Eylem bağlantısı                | Eylem bağlantısı | İletişim kutusunun alt kısmında görüntülenen isteğe bağlı bağlantı. Örneğin, bu bağlantı sitenin desteklediği tüm ülke ve bölgelerin listesini sağlayan dahili bir sayfayı gösterebilir. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Sayfaya ülke/bölge seçici modülü ekleme

Ülke/bölge seçici modülü, üst bilgi modülüne doğrudan veya paylaşılan bir parça aracılığıyla eklenebilir. Üst bilgi modülleri hakkında daha fazla bilgi için bkz. [Üst bilgi modülleri](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Commerce site oluşturucuda ülke/bölge seçici modülünü yapılandırma

> [!NOTE]
> Müşterilerinize önerdiğiniz URL'ler, ülke/bölge seçici modülünde ülke nesneleri olarak yapılandırılmalıdır.

Müşterilere göstermek ve önermek istediğiniz her URL için Commerce site oluşturucudaki şu adımları izleyin.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Bulut destekli aramaya genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'ta bulut destekli aramanın genel görünümünü vermektedir.
author: ashishmsft
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b5182df9d45a3b5d2572a5b6b391c924ef23bf9a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800433"
---
# <a name="cloud-powered-search-overview"></a>Bulut destekli aramaya genel bakış

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta bulut destekli aramanın genel görünümünü vermektedir.

Ürün bulunabilirliği, müşterilerin kategorilerine, aramaya ve filtre uygulamasına göre hızlı ve kolay bir şekilde ürünleri bulabilmesini sağlamaya yardımcı olur. Perakendeciler, tüm kanallarda müşteri etkileşimi için ürün keşfini bir ana araç olarak kabul edin.

Müşteriler, arama terimleri yazarken, çok yönlü gezinme ve vurgulamadan, Web arama altyapılarının, gelişmiş e-ticaret web sitelerinin, sosyal uygulamaların ve otomatik önerilerin neredeyse anlık yanıt sürelerine alışkın olurlar. Müşteriler, istedikleri ürünü bir e-ticaret mağazasında hızlı bulamayacakları takdirde, farklı bir e-ticaret deposuna gitmekten çekinmeyin.

Dynamics 365 Commerce'teki bulut destekli ürün bulunabilirliği, perakendecilere, hem e-ticaret kanalları hem de satış noktası (POS) kanalları gibi tüm kanallardaki tüketici bekletmesi ve dönüştürme oranlarını artırmak için devam etmesine yardımcı olur.

Dynamics 365 Commerce arama deneyiminin, perakendecilere daha iyi ürün bulunabilirliği elde etmenize yardımcı olacak yetenekler geliştirilmiştir. Aynı zamanda, bu yetenekler e-ticaret trafiği için gerekli ölçeklenebilirliği ve performansı sağlar.

## <a name="browse-and-search"></a>Tarama ve arama

Ürün bulma işlemi öncelikle bilgi alımı ve içerik gezintisi için arama işlevleriyle ilgili olduğundan, arama ilgisi ve performansı, çoklu kanal deneyiminde önemli etkenlerdir. Etkili ve etkin bir gözatma ve arama deneyimi dönüştürmenin artmasına yardımcı olur.

Aşağıdaki çizimde, tipik gözatma ve arama işlevlerinin bir örneği gösterilmektedir.

![Arama giriş sayfası](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Çok yönlü gezinme ve seçim Özeti 

Çok yönlü gezinme, müşterilerin bir terim kümesindeki terimlerle bağlantılı iyileştiricilerin filtrelerine izin vererek içeriğe daha kolay gözatmasına yardımcı olur. Müşteri iyileştiriciler seçtikten ve uygulandıktan sonra, seçeneklerin özeti gösterilir. 

Çok yönlü gezinme kullanarak, ek sayfalar oluşturmak zorunda kalmadan terim kümesindeki farklı terimler için farklı iyileştiricileri konfigüre edebilirsiniz. 

Aşağıdaki çizimde, çok yönlü gezintinin aramada kullanıldığı bir örnek gösterilmektedir.

![Seçim özeti](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Derinlikli otomatik önerme

Geçerli otomatik öneri işlevselliği yalnızca eşleşen anahtar sözcüğü aramayı tetikleyen anahtar sözcükleri gösterir. Dynamics 365 Commerce'teki yeni geliştirmeler nedeniyle, müşteriler yazma işlemi tamamlanmadan önce ürün bağlantılarını sıkça bulabilir.

Dynamics 365 Commerce ayrıca çeşitli kategorilerdeki anahtar sözcük eşleşmeleri işlevselliğini destekler. Bu işlevsellik, müşterilerin kategoriler arasında eşleşen anahtar sözcüklerin sayısını görmesini ve diğer kategorilerdeki bir anahtar sözcükle ilgili arama tetiklemesini sağlar.

Aşağıdaki çizimde, derinlikli otomatik önerinin kullanıldığı bir örnek gösterilmektedir.

![derinlikli otomatik önerme](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sırala

Müşterilerimize, Dynamics 365 Commerce geliştirilmiş sıralama; arama sonuçlarını sıralama, arama ve gözatma ve fiyat, ürün adı ve ürün numarası gibi ölçütlere göre bunları belirginleştirme. Müşteriler Ayrıca, ürünün yeni, en çok satılan veya son eklenen bir ürün olup olmadığına göre sonuçları sıralayabilir.

>[!NOTE]
>Bu bulut destekli arama özellikleri 10.0.8 sürümünden başlayarak kullanılabilir. **Commerce parametreleri > konfigürasyon parametrelerinin** altında "ProductSearch.UseAzureSearch set to 'true'" olduğundan emin olun. 
![Bulut destekli arama için yapılandırma parametreleri](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

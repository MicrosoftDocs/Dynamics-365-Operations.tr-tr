---
title: Bulut destekli aramaya genel bakış
description: Bu makale, Microsoft Dynamics 365 Commerce'ta bulut destekli aramanın genel görünümünü vermektedir.
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273679"
---
# <a name="cloud-powered-search-overview"></a>Bulut destekli aramaya genel bakış

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'ta bulut destekli aramanın genel görünümünü vermektedir.

Ürün bulunabilirliği, müşterilerin kategorilerine, aramaya ve filtre uygulamasına göre hızlı ve kolay bir şekilde ürünleri bulabilmesini sağlamaya yardımcı olur. Perakendeciler, ürün bulmayı, e-ticaret ve satış noktası (POS) gibi Bulut Ölçek Birimi (CSU) tarafından desteklenen kanallar arasında müşteri etkileşimi için birincil araç olarak düşünür.

Müşteriler, arama terimleri yazarken, çok yönlü gezinme ve vurgulamadan, Web arama altyapılarının, gelişmiş e-ticaret web sitelerinin, sosyal uygulamaların ve otomatik önerilerin neredeyse anlık yanıt sürelerine alışkın olurlar. Müşteriler, istedikleri ürünü bir e-ticaret mağazasında hızlı bulamazsa, farklı bir e-ticaret deposuna gitmekten çekinmez.

Commerce'teki bulut destekli ürün bulunabilirliği, perakendecilere, CSU destekli tüm kanallardaki tüketici bekletmesi ve dönüştürme oranlarını artırmak için devam etmesine yardımcı olur.

Commerce arama deneyimi, perakendecilere daha iyi ürün bulunabilirliği elde etmenize yardımcı olacak yetenekler geliştirilmiştir. Aynı zamanda, bu yetenekler e-ticaret trafiği için gerekli ölçeklenebilirliği ve performansı sağlar.

## <a name="browse-and-search"></a>Tarama ve arama

Ürün bulma işlemi öncelikle bilgi alımı ve içerik gezintisi için arama işlevleriyle ilgili olduğundan, arama ilgisi ve performansı, çoklu kanal deneyiminde önemli etkenlerdir. Etkili ve etkin bir gözatma ve arama deneyimi dönüştürmenin artmasına yardımcı olur.

Aşağıdaki çizimde, tipik gözatma ve arama işlevlerinin bir örneği gösterilmektedir.

![Arama giriş sayfası.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Çok yönlü gezinme ve seçim Özeti 

Çok yönlü gezinme, müşterilerin bir terim kümesindeki terimlerle bağlantılı iyileştiricilerin filtrelerine izin vererek içeriğe daha kolay gözatmasına yardımcı olur. Müşteri iyileştiriciler seçtikten ve uygulandıktan sonra, seçeneklerin özeti gösterilir. 

Çok yönlü gezinme kullanarak, ek sayfalar oluşturmak zorunda kalmadan terim kümesindeki farklı terimler için farklı iyileştiricileri konfigüre edebilirsiniz. 

Aşağıdaki çizimde, çok yönlü gezintinin aramada kullanıldığı bir örnek gösterilmektedir.

![Seçim özeti.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Derinlikli otomatik önerme

Geçerli otomatik öneri işlevselliği eşleşen anahtar sözcüğü aramayı tetikleyen anahtar sözcükleri gösterir. Commerce'teki yeni geliştirmeler nedeniyle, müşteriler yazma işlemi tamamlanmadan önce ürün bağlantılarını sıkça bulabilir.

Commerce ayrıca çeşitli kategorilerdeki anahtar sözcük eşleşmeleri işlevselliğini destekler. Bu işlevsellik, müşterilerin kategoriler arasında eşleşen anahtar sözcüklerin sayısını görmesini ve diğer kategorilerdeki bir anahtar sözcükle ilgili arama tetiklemesini sağlar.

Aşağıdaki çizimde, derinlikli otomatik önerinin kullanıldığı bir örnek gösterilmektedir.

![derinlikli otomatik önerme.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sırala

Sıralama işlevi, müşterilerin kategori sonuçlarını sıralamasını, aramasını ve kategori sonuçlarına gözatmasını ve fiyat, ürün adı ve ürün numarası gibi ölçütlere göre bunları daraltmasını sağlar. Ortamınızda [ürün önerilerini](product-recommendations.md) etkinleştirirseniz müşteriler yeni, en çok satan ve popüler gibi gelişmiş sıralama ölçütlerine dayanan sonuçları da sıralayabilir.


> [!NOTE]
> Bu bulut destekli arama özellikleri 10.0.8 sürümünden başlayarak kullanılabilir. **Commerce parametreleri > Konfigürasyon Parametreleri** altında, "ProductSearch.UseAzureSearch" öğesinin 'doğru' olarak ayarlandığından emin olun. 
![Bulut destekli arama için yapılandırma parametreleri.](./media/CloudPoweredSearchConfigurationParameters.png)
>Yeni, en çok satan ve popüler gibi gelişmiş sıralama seçenekleri Commerce SSK sürüm 9.35+ ve Dynamics 365 Commerce 10.0.20 sürümü ile kullanılabilir.  


## <a name="additional-resources"></a>Ek kaynaklar

[Varsayılan kategori açılış sayfası ve arama sonuçları sayfasına genel bakış](category-search-page-overview.md)

[SEO meta verilerini yönetme](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]

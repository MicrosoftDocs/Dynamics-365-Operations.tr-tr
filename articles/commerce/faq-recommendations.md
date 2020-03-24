---
title: Ürün önerileri SSS
description: Bu konu, ürün önerilerle veya sonuçları ile ilgili sorunları gidermek için kullanabileceğiniz işlemler ve araçlar hakkında bilgi sağlar.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3add4e2e0d5cc16b561b808aacf5cef94fea5ae5
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127802"
---
# <a name="product-recommendations-faq"></a>Ürün önerileri SSS


[!include [banner](includes/banner.md)]

Bu konu, [ürün önerilerle](product-recommendations.md) veya sonuçları ile ilgili sorunları gidermek için kullanabileceğiniz işlemler ve araçlar hakkında bilgi sağlar.

## <a name="best-practices"></a>En iyi uygulamalar
Ürün yöneticileri ve türevleri kavramı kullanmak çok önemlidir. Değişkenlerin ana ürün yöneticisine makul gruplandırması, liste algoritmalarına ve servise daha iyi modeller oluşturmasına yardımcı olur. Ek olarak, hizmet tüm yakından ilgili varyantları bir listeye koymak yerine yalnızca bir ürünün bir örneğine hizmet edebilir. Yakından ilgili tüm varyantlar bir listeye koyulur, hatalı veya tekrarlanan sonuçlar oluşabilir.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Öneri listemdeki ürünler niçin kayboluyor?

Genel olarak, ürün öneri listesinde bir madde eksikse, bir ürün konfigürasyonu sorunu olabilir. Örneğin, yanlış bir ürün başlangıç tarihi veya bitiş tarihi olabilir, bir boyut yanlış yapılandırılmış olabilir veya ürün doğru kanal sınıflama, vs. olmayabilir.

Yapay bilgi işlem makinesi öğrenmeyi (AI-ML) temel alan öneri listesinde bir madde eksikse, bu madde öneri listesinin ölçütlerine uygun olmayabilir veya öneri listesinin göstermesi için yeterli sayıda satınalma hareketi bulunmayabilir.

Aşağıdaki adımları denetlemeniz önerilir:
1. **HQ'da ürün önerilerinin etkinleştirildiğinden emin olun.** Bu servisin nasıl etkinleştirileceği hakkında bilgi için bkz. [Ürün önerilerini etkinleştir](enable-product-recommendations.md).
1. **Önemli ürün özelliklerinin ayarlandığından emin olun.** Örneğin, ürün sınıflamalar **dahil** olarak ayarlanmalıdır.
1. **Yeni sıralanmış ürünler için, ürün yeni listede görünmeye başlamadan önce 3 saate kadar sürebilir.**
1. **Bir ürün hala, en iyi satış, örneğin benzer veya sık satın alan kişiler gibi görünmeye devam ediyorsa, bu ürünün yeterli hareketi olmayabilir.** Bu durumda, daha fazla hareketin gerçekleşmesini bekleyebilir, varsayılan öneri listesi parametrelerini güncelleştirebilir veya öneri ürün listesi sonuçlarını değiştirmek için el ile müdahale kullanabilirsiniz. Öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).
1. **Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.** Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Düşük öneri sonuçlarının geri döndürülüp döndürülmeyeceğini nasıl engelleyebilirim?

Öneri listeleri, sonuçları üretmek için büyük bir işlem hacmi gerektirir. Bu nedenle, kullanıcıların tam geçmiş hareket verileri sağlaması önemlidir.

Ek olarak, hareket içermeyen veya az sayıda hareketi olmayan ürünler, genellikle **Bunu da sevdiler** veya **sıklıkla birlikte satın almış** sonuçları içermez ve **trend** veya **en iyi satış** öneri listelerinde görünmüyor. Bu durum genellikle çok yeni ürünlerde veya az sayıda satın alma eski ürünlerde ortaya çıkabilir. Sık kullanılan yeni öğeler bu sorunu kolayca çözmek için kullanılabilir.

Aşağıdaki adımları denetlemeniz önerilir:
1. **Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.** Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. AI-ML tabanlı ürün öneri sonuçlarını düzeltme.
1. **Ürün yeni ise, ürünün daha fazla hareketi olana kadar öneri listesini değiştirmeyi düşünebilirsiniz.** Öneri liste sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).


- **Ürünün, liste için öneri ölçütüne uygun olduğundan emin olun.** Ürün öneri parametreleri hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).
- **Ürün yeni ise, ürünün daha fazla hareketi olana kadar öneri listesini değiştirmeyi düşünebilirsiniz.** Öneri liste sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Ürünü kaldırabilir, ancak yine de mağazada görebilir miyim?

Bir iş gerektiğinde algoritmik olarak oluşturulan listeleri ayarlayabilirsiniz. Ancak, bir ürün öneri listesinden kaldırılırsa, ürün depoda bulunabilir olarak kalacaktır. Ürün öneri sonuçlarını düzeltme hakkında daha fazla bilgi için, bkz. [AI-ML tabanlı ürün öneri sonuçlarını yönetme](modify-product-recommendation-results.md).

Bir maddenin depoda keşfedilmesini engellemelisiniz, **madde sınıflamalar** değerini **hariç tut** olarak değiştirmeniz gerekir.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Bir e-ticaret sayfasına nasıl liste ekleyebilirim?

E-ticaret Web sitenize ürün öneri sayfaları ekleme hakkında bilgi için, bkz [Sayfalara ürün öneri listeleri ekle](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>POS'un önerilerini nasıl etkinleştirebilirim?

Ürün önerilerini etkinleştirdikten sonra, kontrol POS ekranına öneriler panelini eklemeniz gerekir. Daha fazla bilgi için bkz. [POS cihazlarında hareket ekranına öneriler denetimi ekleme](add-recommendations-control-pos-screen.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında ADLS'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

[Kişiselleştirilmiş önerileri etkinleştirme](personalized-recommendations.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

[e-Ticaret sitesine önerisi listeleri ekleme](add-reco-list-to-page.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

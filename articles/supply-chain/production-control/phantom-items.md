---
title: Hayali maddeler
description: Bu konu, Dynamics 365 Supply Chain Management içinde Hayali satır türünün bir ürün reçetesi (BOM) satırlarında ve formülünde nasıl kullanılabileceğini açıklar.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5c9768381d35709611e4bec3d2b7793a4d896b34
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713261"
---
# <a name="phantom-items"></a>Hayali maddeler

[!include [banner](../includes/banner.md)]

Bu konu, ayrıntılı olarak Hayali hat türünün bir ürün reçetesi (BOM) satırlarında ve formülünde nasıl kullanılabileceğini açıklar.

Şekil 1'de (a), H ürünü ve F ile G parçaları için ürün reçetesidir, ve (b), H ile F ürünleri için rota tablosudur.

![Şekil 1: Mühendislik ürün reçetesi.](media/product-H-part-F.png)
*Şekil 1: Mühendislik ürün reçetesi*

Şekil 1, bir ürün reçetesi yapısını iki düzeyde gösterir. Tamamlanmış ürün H, bir makine montajı için bir ürünü temsil eder. Makine montajı iki parçadan oluşur, iki malzemeye (A ve B) sahip bir elektriksel birim (F) ve iki malzemeye sahip (C ve D) bir paketleme malzemeleri grubu (G). Başka bir malzeme (E), makinenin genel montajında kullanılır.

Şekil 1, ürün H için Mühendislik Ürün Reçetesini temsil etmektedir. Bu yapı, genel makine montajının parçaları ve bileşenlerine genel bir bakış sağlar. Ancak, ürün tasarımcıları ürün reçetesinin bu şekilde temsil edilmesini tercih etseler de, bu yapı makinenin atölyede nasıl ortaya çıkarıldığını doğru şekilde temsil etmeyebilir.

Örneğin, şekil 1'deki Mühendislik ürün reçetesi, elektriksel birim F'nin ayrı bir iş emrinde, ayrı bir parça olarak monte edildiğini göstermektedir. Ancak, atölyede, elektriksel birimi ayrı bir iş emri olarak değil, genel makine montajının bir parçası olarak monte etmek daha optimal olarak değerlendirilebilir.

Mühendislik ürün reçetesi, parça G'nin ayrı bir parça olduğunu belirtmektedir. Ancak, bu yapıda, parça G fiziksel bir parçayı değil, bir paketleme malzemeleri grubunu temsil etmektedir.

Bu nedenle, bir Mühendislik Ürün reçetesi bir ürünün tasarımı ve bu tasarımın bakımı için önemli değer sağlasa da, ürünün üretilmesi işlemini desteklemek için en mantıksal yolu sunmuyor olabilir. Bunun tersine, bir Üretim ürün reçetesi, bir ürünü oluşturmanın en iyi yolunu temsil eder.

Şekil 2, önceki Mühendislik ürün reçetesinin bir Üretim ürün reçetesine nasıl dönüştürüldüğünü gösterir. Şekil 2'de (a), H ürünü için ürün reçetesidir ve b, H ürünü için rota tablosudur.

![Şekil 2: Üretim ürün reçetesi.](media/product-H-part-B.png)
*Şekil 2: Üretim ürün reçetesi*

Bu yapıda, parçalar F ve G kavramı yoktur ve bu parçaların oluştuğu malzemeler bir sonraki ürün reçetesi seviyesine yükseltilmiştir.

İki operasyon sayfasına sahip Mühendislik ürün reçetesinin aksine, Üretim ürün reçetesi yalnızca bir operasyon sayfasına sahiptir. Parça G ile bağlantılı olan paketleme operasyonu da yükseltilmiştir ve ürün H için operasyon sayfasının parçasıdır. Elektriksel birimin montajı ilk operasyondur. Bu sıralama mantıklıdır, çünkü birim, makine montajı olan bir sonraki operasyonda kullanılacaktır. Son operasyon, paketleme operasyonudur, bu da iki paketleme malzemesi tüketir (C ve D).

Mühendislik BOM ve Üretim BOM arasındaki geçiş, Phantom BOM satır türü ile gerçekleşir. "Hayali" teriminin belirttiği gibi, parçalar F ve G iki ürün reçetesi türü arasında geçiş yapılırken ortadan kaybolmuştur. Bu örnekte, Hayali satır türü parçalar F ve G için Mühendislik ürün reçetesinde ürün reçetesi satırlarına uygulanır. Bir üretim veya toplu iş emri oluşturulduğunda, Mühendislik ürün reçetesi üretim veya toplu iş emrine kopyalanır. Daha sonra siparişin tahmini yapıldığında, Mühendislik ürün reçetesinden Üretim ürün reçetesine geçiş, şekil 2'deki gibi ortaya çıkar. Şekil 2'deki operasyonlar sayfasından, paketleme malzemeleri C ve D operasyon için dahil edilir.

## <a name="multilevel-phantom-bom-structures"></a>Çok düzeyli hayali ürün reçetesi yapıları

Hayali satır türü çok düzeyli ürün reçetesi yapıları için şekil 3'te gösterildiği gibi kullanılabilir. Şekil 3'te (a), G ürünü için ürün reçetesidir ve (b), E ile F parçaları ve G ürünü için rota tablosudur.

![Şekil 3: Mühendislik ürün reçetesi parça G.](media/product-G.png)
*Şekil 3: Mühendislik ürün reçetesi parça G*

Şekil 4, ortaya çıkan Üretim ürün reçetesi ve rota tablosunu, E ve F parçalarının ürün reçetesi satırlarının satır tipi Hayali olacak şekilde yapılandırılması durumunda gösterir. Şekil 4'te (a), G ürünü için ürün reçetesidir ve (b), G ürünü için rota tablosudur.

![Şekil 4: Üretim ürün reçetesi parça G.](media/product-G-route-sheet-G.png)
*Şekil 4: Üretim ürün reçetesi parça G*

## <a name="phantom-and-route-network"></a>Hayali ve rota ağı

Hayali ürün reçeteleri de bir rota ağına sahip bir ürün reçetesi için kullanılabilir. Bir rota ağında, bir veya daha fazla operasyon paralel olarak çalışabilir. Şekil 5, çok düzeyli bir ürün reçetesinde kullanılan bir rota ağına bir örnek göstermektedir. Şekil 5'te (a), G ürünü ve F parçası için ürün reçetesidir ve (b), bir rota ağına sahip G ürünü ve F parçası için bir rota tablosudur.

![Şekil 5: Mühendislik ürün reçetesi parça G, rota ağı.](media/product-G-part-F.png)
*Şekil 5: Mühendislik ürün reçetesi parça G, rota ağı*

Şekil 6'da (a), G ürünü ve F parçası için ürün reçetesidir ve (b), G ürünü ve F parçası için rota tablosudur.

![Şekil 6: Üretim ürün reçetesi parça G, rota ağı.](media/product-G-part-F-with-route-sheet.png)
*Şekil 6: Üretim ürün reçetesi parça G, rota ağı*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
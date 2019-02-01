---
title: Hayali maddeler
description: "Bu konu, ayrıntılı olarak Hayali hat türünün bir ürün reçetesi (BOM) satırlarında ve Microsoft Dynamics 365 for Finance and Operations formülünde nasıl kullanılabileceğini açıklar."
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: 
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.contentlocale: tr-tr
ms.lasthandoff: 10/01/2018

---

# <a name="phantom-items"></a>Hayali maddeler

[!include [banner](../includes/banner.md)]

Bu konu, ayrıntılı olarak Hayali hat türünün bir ürün reçetesi (BOM) satırlarında ve formülünde nasıl kullanılabileceğini açıklar. Aşağıdaki çizimde, (a) ürün H ve parçalar F ve G için ürün reçetesidir, ve (b), ürünler H ve parça F için rota tablosudur.

![Ürün H ve parça F](media/product-H-part-F.png)


Bu çizim, bir ürün reçetesi yapısını iki düzeyde gösterir. Tamamlanmış ürün H, bir makine montajı için bir ürünü temsil eder. Makine montajı iki parçadan oluşur, iki malzemeye (A ve B) sahip bir elektriksel birim (F) ve iki malzemeye sahip (C ve D) bir paketleme malzemeleri grubu (G). Başka bir malzeme (E), makinenin genel montajında kullanılır.

![Ürün H ve parça F](media/product-H-part-B.png)

önceki şekil, ürün H için Mühendislik Ürün Reçetesini temsil etmektedir. Bu yapı, genel makine montajının parçaları ve bileşenlerine genel bir bakış sağlar. Ancak, ürün tasarımcıları ürün reçetesinin bu şekilde temsil edilmesini tercih etseler de, bu yapı makinenin atölyede nasıl ortaya çıkarıldığını doğru şekilde temsil etmeyebilir. 

Örneğin, önceki örnekteki Mühendislik ürün reçetesi, elektriksel birim F'nin ayrı bir iş emrinde, ayrı bir parça olarak monte edildiğini göstermektedir. Ancak, atölyede, elektriksel birimi ayrı bir iş emri olarak değil, genel makine montajının bir parçası olarak monte etmek daha optimal olarak değerlendirilebilir.

Mühendislik ürün reçetesi, parça G'nin ayrı bir parça olduğunu belirtmektedir. Ancak, bu yapıda, parça G fiziksel bir parçayı değil, bir paketleme malzemeleri grubunu temsil etmektedir. 

Bu nedenle, bir Mühendislik Ürün reçetesi bir ürünün tasarımı ve bu tasarımın bakımı için önemli değer sağlasa da, ürünün üretilmesi işlemini desteklemek için en mantıksal yolu sunmuyor olabilir. Bunun tersine, bir Üretim ürün reçetesi, bir ürünü oluşturmanın en iyi yolunu temsil eder.

Aşağıdaki çizim, önceki Mühendislik ürün reçetesinin bir Üretim ürün reçetesine nasıl dönüştürüldüğünü gösterir. Bu şekilde, (a) ürün H için ürün reçetesidir ve b, ürün H için rota tablosudur.

Bu yapıda, parçalar F ve G kavramı yoktur ve bu parçaların oluştuğu malzemeler bir sonraki ürün reçetesi seviyesine yükseltilmiştir. 

İki operasyon sayfasına sahip Mühendislik ürün reçetesinin aksine, Üretim ürün reçetesi yalnızca bir operasyon sayfasına sahiptir. Parça G ile bağlantılı olan paketleme operasyonu da yükseltilmiştir ve ürün H için operasyon sayfasının parçasıdır. Elektriksel birimin montajı ilk operasyondur. Bu sıralama mantıklıdır, çünkü birim, makine montajı olan bir sonraki operasyonda kullanılacaktır. Son operasyon, paketleme operasyonudur, bu da iki paketleme malzemesi tüketir (C ve D).

Microsoft Dynamics 365 for Finance and Operations'ta, Mühendislik ürün reçetesi ve Üretim ürün reçetesi geçişi Hayali ürün reçetesi satır türü üzerinden etkinleştirilir. "Hayali" teriminin belirttiği gibi, parçalar F ve G iki ürün reçetesi türü arasında geçiş yapılırken ortadan kaybolmuştur. Bu örnekte, Hayali satır türü parçalar F ve G için Mühendislik ürün reçetesinde ürün reçetesi satırlarına uygulanır. Bir üretim veya toplu iş emri oluşturulduğunda, Mühendislik ürün reçetesi üretim veya toplu iş emrine kopyalanır. Daha sonra siparişin tahmini yapıldığında, Mühendislik ürün reçetesinden Üretim ürün reçetesine geçiş, önceden belirtilen şekillerdeki gibi ortaya çıkar. İkinci şekildeki operasyonlar sayfasından, paketleme malzemeleri C ve D operasyon için dahil edilir. 

## <a name="multilevel-phantom-bom-structures"></a>Çok düzeyli hayali ürün reçetesi yapıları
Hayali satır türü çok düzeyli ürün reçetesi yapıları için aşağıdaki şekilde gösterildiği gibi kullanılabilir. Bu şekilde, (a) ürün G için ürün reçetesidir ve (b) parçalar E ve F ve ürün G için rota tablosudur. 

![Ürün G ve parça F rota tablolarıyla](media/product-G-route-sheet-G.png)


Aşağıdaki şekil, ortaya çıkan Üretim ürün reçetesi ve rota tablosunu, parçalar E ve F için ürün reçetesi satırları satır tipinin Hayali olarak yapılandırılması durumunda gösterir. Bu şekilde, (a) ürün G için ürün reçetesidir ve (b), ürün G için rota tablosudur.

![Ürün G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Hayali ve rota ağı
Hayali ürün reçeteleri de bir rota ağına sahip bir ürün reçetesi için kullanılabilir. Bir rota ağında, bir veya daha fazla operasyon paralel olarak çalışabilir. Aşağıdaki şekil, çok düzeyli bir ürün reçetesinde kullanılan bir rota ağına bir örnek göstermektedir. Bu şekilde, (a) ürün G ve parça F için ürün reçetesidir ve (b) bir rota ağına sahip ürün G ve parça F için bir rota tablosudur.

![Ürün G ve parça F](media/product-G-part-F.png)


Aşağıdaki çizimde, (a) ürün G ve parça F ve G için ürün reçetesidir, ve (b), ürün G ve parça F için rota tablosudur.

![Ürün G ve parça F rota tablolarıyla](media/product-G-part-F-with-route-sheet.png)

---
title: "Boyuta dayalı ürün yapılandırma"
description: "Boyut tabanlı ürün yapılandırması, tek bir ana üründen ve o ürün reçetelerinden çok sayıda ürün çeşidi oluşturmak için basit bir çözümü temsil eder."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 297e60e63b88b610d0886ad16667c4f99cc74ccb
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---

# <a name="dimension-based-product-configuration"></a>Boyuta dayalı ürün yapılandırma

[!include[banner](../includes/banner.md)]


Boyut tabanlı ürün yapılandırması, tek bir ana üründen ve o ürün reçetelerinden çok sayıda ürün çeşidi oluşturmak için basit bir çözümü temsil eder.

Boyuta dayalı ürün yapılandırma, üç yerleşik ürün yapılandırma teknolojisinden biridir. Diğer iki teknoloji ön tanımlı farklara dayalı ve kısıtlamaya dayalı yapılandırmalardır. Üç teknolojinin her biri başlangıç noktası olarak bir ürün master planı kullanır ve kullanıcının bir ürün master planından çok sayıda ürün çeşidi üretmesine izin verir.

## <a name="key-concepts"></a>Kilit kavramlar
Boyuta dayalı ürün yapılandırma şu anahtar kavramlara dayanır:

-   Ana ürünler
-   Ürün boyutu yapılandırma
-   Konfigürasyon grupları
-   Ürün reçetesi (BOM)
-   Konfigürasyon rotası
-   Konfigürasyon kuralları

### <a name="product-masters"></a>Ana ürünler

Bir ürün master planı, ürün yapılandırma sürecinin başlangıç noktasıdır. Boyuta dayalı ürün yapılandırma için bu belirli yapılandırma teknolojine ve yapılandırma ürün boyutunu içeren bir ürün boyut grubuna sahip bir ürün master planına ihtiyacınız vardır.

### <a name="configuration-product-dimension"></a>Ürün boyutu yapılandırma

Yapılandırma ürün boyutu, boyuta dayalı yapılandırma teknolojisine sahip bir ürün master planı için ürün çeşitlerinin tanımlanması için kullanılır. Yapılandırma boyut değeri, kullanıcı tarafından girilir ve ayrı ürün çeşitlerinin tanımlanmasına yardımcı olur.

### <a name="configuration-groups"></a>Konfigürasyon grupları

Yapılandırma grupları bir merkezi depoda tanımlanır ve tüm boyuta dayalı ürün yapılandırma modelleri için kullanılabilir. Yapılandırma grupları ayrı BOM satırlarıyla ilişkilendirilir ve ortak olarak özel olan bir grup satırla birlikte tutulur. Bu da tek bir ürün çeşidi için bir gruptaki sadece bir satırın seçilebileceği anlamına gelir.

### <a name="bill-of-materials-bom"></a>Ürün reçetesi (BOM)

BOM, boyuta dayalı ürün yapılandırması için yapı taşlarını temsil eder. Herhangi bir ürün çeşidinde kullanılabilecek tüm farklı ürünleri içermelidir. BOM'daki her bir satır bir yapılandırma grubunu referans alabilir. Bir satır bir yapılandırma grubunu referans almıyorsa tüm ürün çeşitlerine dahil edilir.

### <a name="configuration-route"></a>Konfigürasyon rotası

Yapılandırma yolu, yapılandırma gruplarının sırasını belirler ve bunlar ürün yapılandırma süreci sırasında kullanıcıya bu sırada görüntülenir.

### <a name="configuration-rules"></a>Konfigürasyon kuralları

Yapılandırma kuralları, bir BOM'da bir yapılandırma grubuna dahil edilen bir ürünün aynı BOM'daki farklı bir yapılandırma grubundaki bir ürünü dahil etmesini veya hariç tutmasını sağlayan bir mekanizmadır.

## <a name="product-modeling-process"></a>Ürün modelleme süreci
Boyuta dayalı bir ürün için ürün modelinin oluşturulması için doğal süreç ilgili yapılandırma gruplarının tanımlanmasıyla başlar. BOM'da kullanılacak tüm ürünlerin, ürün modelinin oluşturulduğu şirket için serbest bırakılmasının sağlanması önemlidir. Bu yapı taşları yerindeyken, kullanıcılar ürün reçetesini oluşturabilir ve yapılandırma gruplarını tüm ürün reçetesi satırlarına atayabilir. Bir ürün reçetesi tamamlandığında, bir yapılandırma rotası, yapılandırma gruplarını doğru sıralamada sipariş etmek için tanımlanabilir. [![Boyuta dayanan ürün modelleme işlemi](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Farklı yapılandırma gruplarından, birlikte kullanılması veya kullanılmaması gereken çeşitli ürünler mevcutsa, bu ürün ilişkilerini zorunlu kılacak yapılandırma kurallarını oluşturabilirsiniz. BOM bir BOM sürümü üzerinden boyuta dayalı bir ürün master planıyla ilişkilendirildikten ve her ikisi onaylandıktan ve etkinleştirildikten sonra ürün yapılandırmaları oluşturabilir ve her bir yapılandırma için bir ad girebilirsiniz. Yapılandırmalar, herhangi bir hareket oluşturulmadan önce tanımlanabilir veya bu tanımlama işlemi belirli bir yapılandırma gerçekleştiğinde yapılabilir.

### <a name="suggested-use"></a>Önerilen kullanım

Boyuta dayalı yapılandırma teknolojisi en iyi, sınırlı ürün çeşitlerine ve standart ürün boyutları, boyları, renkleri, stillerinin kombinasyonuna sahip ürünler için kullanılır ve yapılandırma belirli bir ürün çeşidinin tanımlanması için uygun değildir. Kasa yüksekliği, tekerlek boyutu, fren türleri ve dişli mekanizmaları farklı bir bisiklet örnek olarak gösterilebilir.

### <a name="next-step"></a>Sonraki adım 

Aşağıdaki sekiz görev kılavuzu, tamamlamanız gereken sırada listelenmişlerdir. 

1.  [Boyut tabanlı ana ürün oluşturma (Görev kılavuzu)](tasks/create-dimension-based-product-master.md)
2.  [Boyut tabanlı ana ürünü serbest bırakma (Görev kılavuzu)](tasks/release-dimension-based-product-master.md)
3.  [Serbest bırakılan ana ürünün temel kurulumunu tamamlama (Görev kılavuzu)](tasks/complete-basic-setup-released-product-master.md)
4.  [Yapılandırma grupları tanımlama (Görev kılavuzu)](tasks/define-configuration-groups.md)
5.  [Boyut tabanlı ana ürün için ürün reçetesi oluşturma (Görev kılavuzu)](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Yapılandırma rotaları tanımlama (Görev kılavuzu)](tasks/define-configuration-route.md)
7.  [Yapılandırma kuralları oluşturma (Görev kılavuzu)](tasks/create-configuration-rules.md)
8.  [Boyut tabanlı yapılandırmalar oluşturma (Görev kılavuzu)](tasks/create-dimension-based-configurations.md)



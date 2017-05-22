---
title: "Bir yalın kuruluşu modelleme"
description: "Bu makale, bir yalın kuruluşu modellemek için kilit kavramlar hakkında bilgi sağlamaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d8975fadf2576a16c84437fcc73908c8cab0b039
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="modeling-a-lean-organization"></a>Bir yalın kuruluşu modelleme

[!include[banner](../includes/banner.md)]


Bu makale, bir yalın kuruluşu modellemek için kilit kavramlar hakkında bilgi sağlamaktadır. 

Bir yalın imalat senaryosu genellikle sadece birbiriyle alakasız kanban kurallarından veya malzeme tedarik ilkelerinden daha fazlasıdır. Malzeme ve ürünlerin, belirli bir üretim veya tedarik senaryosundaki iş hücreleri ve konumları arasındaki akışı, işlem veya hareket etkinliklerinin küçük bir ağı ya da dizisi olarak açıklanabilir. Bu sıra veya ağ, üretim akışı olarak bilinir.

## <a name="production-flows-in-lean-manufacturing"></a>Yalın imalattaki üretim akışları
Üretim siparişlerine dayalı olan üretim senaryolarda, malzeme, belirli bir üretim emrine verilir. Bir ürün reçetesi (BOM) ve rotalarına bağlı olan işlemler dizisi esnasında, ürünler oluşturulur ve sağlandıkları konumda nihai olarak alınırlar. Üretim emirlerinin üretimi zaman aralığı dakika ila hafta aralığında değişir. Tüm ilgili maliyet, malzeme ve işçilik üretim emrinde toplanır. 

Toplu üretimin sebep olduğu iş merkezleri arasındaki stok fazlasını ve teslimat sağlama sürelerini azaltmak için, yalın üretim kanban stok yenileme ve süpermarketleri üretim ve ambar yenileme içerisinde devreye sokar. Genellikle bu özellikler, kısmen bağımsız kanban döngülerinin üretimini bozar. Yarı Bitmiş ürünün bir kanban yenilemesi bitmiş bir ürün için siparişle daha fazla harekete geçmez. 

Microsoft Dynamics AX'te teklif edilmiş olan çeşitli kanban senaryoları için bir üretim ve maliyet içeriği yeniden kurmak için, etkinlik tabanlı üretim akışlarının yalın üretim omurga olarak kullanılmaya başlanmıştır. Tüm kanban kuralları önceden tanımlanmış bu yapısına başvurur. Etkinlik tabanlı model, Dynamics AX için Yalın İmalatın daha önceki sürümlerinde desteklenenden daha geniş çaplı senaryoları desteklemektedir. Ancak, tüm senaryolar aynı etkinlik tabanlı kullanıcı arabirimini kullandığı için bu model atölye çalışanlarına daha fazla karmaşıklık eklemez.

## <a name="semi-finished-products-non-bom-levels"></a>Yarı bitmiş ürünler (ürün reçetesi düzeyleri olmayan)
Dynamics AX için yalın imalat, stoklanmış ürünler ve yarı bitirilmiş ürünler için kanbanları tek bir çerçevede tümleştirir ve bu sayede tüm durumlar için bütünleştirilmiş bir kullanıcı deneyimi sunar. Bu mimari nedeniyle, yarı bitmiş ürünler için kullanılmak üzere kanbanları etkinleştirmek için ek ürün reçetelerinin dahil edilmesine gerek kalmamıştır. Ayrıca bu mimari stok hareketlerinin en aza indirilmesine yardımcı olur.

## <a name="products-and-material-in-work-in-progress"></a>Süren iş içerisindeki malzemeler ve ürünler
Toplu iş boyutlarının, yalın imalat içerisindeki tek parça akışının idealine azaltılması, stok hareketlerinde ciddi bir artışa sebep olabilir, eğer her bir çekme işlemi veya kanban kaydı tüketilen maddeler için harekete sebep oluyorsa. Üretim akışı mimarisi malzemenin üretim akışına aktarılmasını, kanbanlardan çekilmesi veya hareket yönetme birim boyutları ile birlikte sağlar. Verilen malzemenin değeri, üretim akışıyla ilişkili olan süren iş sürecini (WIP) hesabına eklenir. Bu davranış, bir üretim akışına verilen malzemenin davranışına benzemektedir. Aynı ilke, ürünler ve yarı bitmiş ürünlere de uygulanabilir. Bu ürünler oluşturulmadığı, nakledilmediği veya bir üretiim akışı içerisinde tüketilmediği takdirde, stok hareketleri isteğe bağlıdır. Ürün stoğa nakledildikten sonra, üretim akışı için süren iş hesabı ilgili standart maliyeti çıkarılarak azalır.

## <a name="value-streams-and-value-stream-mapping"></a>Değer akışları ve değer akışı eşleme
Dynamics AX için Yalın İmalat'ın mimarisi, Womack ve Jones tarafından formüle edilen beş Yalın prensipten ilham almıştır. Müşteri değeri, Değer akışı, akış, çekme ve kusursuzluk. Üretimin gerçek dünyasında yalın imalatı uygulamak için geçerli bir yöntem, değer akış eşleme (VSM) yöntemidir. Bu yöntem Rother ve Shook tarafından Yalın İmalat Enstitüsü'ndeki "Görmeyi Öğrenmek" adlı yayınlarında tanıtılmıştır. 

Dynamics AX'te, değer akışının gelecekteki durumu bir üretim akışı sürümü olarak modellenebilmektedir. Değer akışının tüm işlemleri işlem etkinlikleri olarak modellenmiştir. Eğer transfer durumunun kayıt altına alınması zorunluysa, hareketler veya transferler, transfer etkinlikleri olarak modellenebilmektedir veya stok çekme veya birleştirilmiş sevk ile tümleştirme zorunluysa. 

Değer akışı Dynamics AX'te bir işletme birimi olarak modellenmiştir. Bu nedenle, değer akışı bir mali boyut olarak kullanılabilir.

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Üretim akışını temel alan yalın üretim için maliyetlendirme
Üretim akışının maliyetin dönemsel birleştirmesi, ilgili süren iş hesabını düzeltir ve üretim tarafından tedarik edilen ürünlerin farklılıkların belirlenmesini etkinleştirir.

## <a name="continuous-improvement"></a>Sürekli gelişim
Sürekli gelişimi daha iyi desteklemek için üretim akışları zaman etkili sürümlerde uygulanır. Bu nedenle varolan bir üretim akışı sürümü, tüm ilgili kanban kurallarıyla birlikte üretim akışının gelecekteki bir sürümüne kopyalanabilir. Ayrıca, üretim akışının gelecekteki durumu, üretim için doğrulanmadan ve etkinleştirilmeden önce modellenebilir. Geçiş tarihi ve ötesine sorunsuz bir malzeme akışını garanti etmek için, eski üretim sürümlerinden mevcut kanbanlar otomatik olarak yeni sürüme ilişkilendirilir.

## <a name="simplicity"></a>Basitlik
Dynamics AX için Yalın imalat uygulamak için biz, basit ve karmaşık üretim senaryolarda tek bir ölçeklenebilir mimari modelleme sağlayan üretim akışı ve etkinlik yaklaşım seçtik. Etkinlik kavramına yakından bakmak ihtiyacı olan kullanıcılara yeni bir kolaylık ortaya çıkarır: atölye ve lojistik çalışanları. Stok hareketleri yerine etkinlik tabanlı işleri bildirerek, tüm yalın üretim çeşitleri için birleştirilmiş kullanıcı arabirimi iş karmaşıklığını kullanıcı arabiriminden ait olduğu yere aktarır: yalın imalat omurgası olarak üretim akışı.




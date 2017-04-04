---
title: "Maliyet öğesi boyutları"
description: "Maliyet muhasebesinin temel direklerinden biri olarak maliyet öğesi boyutları maliyetlerin akış gerçekleştirdiği alanları sınıflandırmak ve izlemek için kullanılır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 87c13e268ab8825e06095d24e03694cf0f271a63
ms.openlocfilehash: b07fcbfb322d58d0a7c4640777a1bd3607d4a786
ms.lasthandoff: 03/31/2017


---

# <a name="cost-element-dimensions"></a>Maliyet öğesi boyutları

Maliyet muhasebesinin temel direklerinden biri olarak maliyet öğesi boyutları maliyetlerin akış gerçekleştirdiği alanları sınıflandırmak ve izlemek için kullanılır. 

Maliyet öğesi hesap planında maliyetle ilgili bir öğeye karşılık gelir. Temel olarak, maliyetlerin akış sağlayabileceği bir işletmenin en alt düzeyindeki herhangi bir öğe türü olabilir. Genel muhasebe hesaplarından maliyetle ilgili tüm kaynaklara bir kavram aralığı olarak maliyet öğeleri. Şu anda, Maliyet muhasebesi genel muhasebe hesaplarını desteklemektedir.

## <a name="two-types-of-cost-elements"></a>İki maliyet öğesi türü
Birincil maliyet öğeleri ve ikincil maliyet öğeleri olmak üzere iki tür maliyet öğesi vardır. Aşağıdaki tabloda iki tür arasındaki fark açıklanmaktadır.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Birincil maliyet öğeleri</strong></td>
<td><strong>İkincil maliyet öğeleri</strong></td>
</tr>
<tr class="even">
<td>Birincil maliyet öğeleri, mali muhasebeden maliyet muhasebesine maliyetlerin akışını temsil eder. Maliyet öğesi yapısı, maliyet öğesinin bir ana hesaba karşılık gelebileceği, genel muhasebe defterindeki kar ve zarar hesabı yapısına karşılık gelir. Tüm ana hesaplar, iş ihtiyaçlarına göre maliyet öğeleri olarak temsil edilmek zorunda değildir. Birincil maliyet öğeleri örnekleri şunları içerir:
<ul>
<li>Satılan malların maliyeti (SMM)</li>
<li>Dolaylı malzeme maliyetleri</li>
<li>Personel maliyetleri</li>
<li>Enerji maliyetleri</li>
</ul></td>
<td>İkincil maliyet öğeleri, maliyetlerin dahili akışını temsil eder çünkü bu maliyetler yalnızca Maliyet muhasebesinde oluşturulur ve kullanılır. Bunlar, maliyetlerin kaynağının izlenebilmesini sağlamak için kullanılır. Bu maliyet öğeleri, maliyet tahsisatları ve genel gider hesaplamalarında kullanılır. İkincil maliyet öğeleri örnekleri şunları içerir:
<ul>
<li>Üretim maliyetleri</li>
<li>Üretim, malzeme ve pazarlama genel giderleri</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Maliyet öğesi boyutları ve maliyet öğesi boyut üyeleri
Maliyet öğeleri, *maliyet öğesi boyutları* olarak adlandırılır. Tek tek boyut değerleri *maliyet öğesi boyut üyeleri* olarak adlandırılır. Örneğin, yasal raporlamanızın temeli olan bir ABD hesap planı yapınız (COA) olsun. Bu COA maliyet öğesi boyutu olarak kullanılır. Birincil maliyet öğesi olan hesaplar Maliyet muhasebesinde maliyet öğesi boyut üyeleri olarak temsil edilir. Aşağıdaki ekran görüntüsünde fiili ana hesapları maliyet öğesi boyut üyesi olarak, Ana Hesapların maliyet öğesi boyutu olduğu bir örnek gösterilmektedir. 

[![Maliyet öğesi boyutları](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Veri bağlayıcıları üzerinden maliyet öğesi boyut üyelerini içe aktarma
Maliyet muhasebesinde maliyet öğesi boyut üyelerinin kurulumunu kolaylaştırmak için bir veya daha fazla kaynak sistemden birincil maliyet öğelerini almak üzere önceden inşa edilmiş veya sizin özel olarak inşa ettiğiniz veri bağlayıcılarını kullanabilirsiniz.

## <a name="implementation-considerations"></a>Uygulama ile ilgili hususlar
Maliyet öğeleri, maliyet ayrıntılarınızın en düşük düzeyini temsil ettiğinden, maliyet öğesi yapısını uygularken yönetim raporlaması yapmak için gerekli tüm maliyet öğelerinin dahil edildiğinden emin olun. Maliyet denetimi için uygun sayıda maliyet öğesi bulmak zor olabilir. Binlerce maliyet öğesi bulundurmak her maliyet öğesini denetlemeyi zorlaştırabilir. Alternatif olarak, maliyet öğelerini gruplandırabilir ve maliyet denetimini toplu düzeyde yönetebilirsiniz.



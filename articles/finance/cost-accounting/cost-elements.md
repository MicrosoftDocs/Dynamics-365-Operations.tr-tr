---
title: Maliyet öğesi boyutları
description: Maliyet muhasebesinin temel direklerinden biri olarak maliyet öğesi boyutları maliyetlerin akış gerçekleştirdiği alanları sınıflandırmak ve izlemek için kullanılır.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e67ce047d08af6d34090ee4e1dc379dd16ecce07
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448907"
---
# <a name="cost-element-dimensions"></a>Maliyet öğesi boyutları

[!include [banner](../includes/banner.md)]

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

[![Maliyet öğesi boyutu olarak Ana Hesapların ekran görüntüsü](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Veri bağlayıcıları üzerinden maliyet öğesi boyut üyelerini içe aktarma
Maliyet muhasebesinde maliyet öğesi boyut üyelerinin kurulumunu kolaylaştırmak için bir veya daha fazla kaynak sistemden birincil maliyet öğelerini almak üzere önceden inşa edilmiş veya sizin özel olarak inşa ettiğiniz veri bağlayıcılarını kullanabilirsiniz.

## <a name="implementation-considerations"></a>Uygulama ile ilgili hususlar
Maliyet öğeleri, maliyet ayrıntılarınızın en düşük düzeyini temsil ettiğinden, maliyet öğesi yapısını uygularken yönetim raporlaması yapmak için gerekli tüm maliyet öğelerinin dahil edildiğinden emin olun. Maliyet denetimi için uygun sayıda maliyet öğesi bulmak zor olabilir. Binlerce maliyet öğesi bulundurmak her maliyet öğesini denetlemeyi zorlaştırabilir. Alternatif olarak, maliyet öğelerini gruplandırabilir ve maliyet denetimini toplu düzeyde yönetebilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
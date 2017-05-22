---
title: "Bir proje için satın alma emirleri"
description: "Bu makalede bir proje için satın alma emirlerinin oluşturulmasında kullanılabilecek çeşitli yöntemler açıklanmıştır. Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2a0c21c2937600d1e31f9326970e52e3bdcff90c
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="purchase-orders-for-a-project"></a>Bir proje için satın alma emirleri

[!include[banner](../includes/banner.md)]


Bu makalede bir proje için satın alma emirlerinin oluşturulmasında kullanılabilecek çeşitli yöntemler açıklanmıştır. Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir.

Microsoft Dynamics 365 for Operations'da bir proje için satın alma emirleri oluşturmak amacıyla birden fazla sayıda yöntem kullanabilirsiniz. Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir.

### <a name="methods-for-creating-a-purchase-order"></a>Bir satın alma emri oluşturmak için yöntemler

Proje yönetimi ve hesap işlemlerinde bir satın alma emri oluşturmak için aşağıdaki yöntemlerden birini kullanabilirsiniz. Satın alma emrinin amacı, satın alma emrinin ne zaman tamamlanacağını ve buna bağlı olarak maddelerin ne zaman bir projeye gider yazılacağını belirlemektir.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Yöntem</th>
<th>Amaç</th>
<th>Maddelerin tüketimi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Doğrudan bir projeden bir satın alma emri oluşturun.</td>
<td>Bir projede tüketilmek üzere bir harici satıcıdan maddeler satın almak için bu yöntemi kullanın. Satın alma emrini iki şekilde oluşturabilirsiniz:
<ul>
<li>Projenin içinden. Bu durumda proje halihazırda satın alma emri için tanımlanmıştır.</li>
<li>Proje satın alma emrine gelerek. Hem satıcıyı hem de satın alma emrinin oluşturulacağı projeyi seçmeniz gerekir.</li>
</ul></td>
<td>Maddeler satıcı faturası güncelleştirildiğinde tüketilir.</td>
</tr>
<tr class="even">
<td>Bir satış siparişinden satınalma siparişi oluşturma.</td>
<td>Bu yöntemi, maddeleri bir projeden satış siparişi oluşturduğunuzda satın almak için kullanın.</td>
<td>Maddeler, satış siparişinin faturası müşteriye kesildiğinde tüketilir.</td>
</tr>
<tr class="odd">
<td>Bir madde gereksiniminden satınalma siparişi oluşturma.</td>
<td>Bu yöntemi, maddeleri bir projeden bir madde gereksinimi oluşturduğunuzda satın almak için kullanın.</td>
<td>Maddeler, madde gereksinimi sevk irsaliyesi güncelleştirildiğinde tüketilir.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Satıcı faturasını veya sevk irsaliyesini güncelleştirdiğinizde, sizden madde gereksinimindeki sevk irsaliyesini güncelleştirmeniz istenir.




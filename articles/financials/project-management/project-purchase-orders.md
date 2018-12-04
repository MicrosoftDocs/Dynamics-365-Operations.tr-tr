---
title: "Bir proje için satın alma emirleri"
description: "Bu makalede bir proje için satın alma emirlerinin oluşturulmasında kullanılabilecek çeşitli yöntemler açıklanmıştır. Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: dae65394a2180ccbf3317a41b635ba97034e541b
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="purchase-orders-for-a-project"></a>Bir proje için satın alma emirleri

[!include [banner](../includes/banner.md)]

Bu makalede bir proje için satın alma emirlerinin oluşturulmasında kullanılabilecek çeşitli yöntemler açıklanmıştır. Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir.

Microsoft Dynamics 365 for Finance and Operations'ta bir proje için satınalma siparişleri oluşturmak amacıyla birden fazla yöntem kullanabilirsiniz. Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir.

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

Daha fazla bilgi için bkz. [Bir madde talebinden maddeleri bir satınama siparişinden teslim alma](tasks/receive-items-purchase-order-item-requirement.md).



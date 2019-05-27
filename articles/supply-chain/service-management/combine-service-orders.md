---
title: Servis siparişlerini birleştir
description: Servis siparişlerini birleştirebilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571983"
---
# <a name="combine-service-orders"></a>Servis siparişlerini birleştir   

[!include [banner](../includes/banner.md)]


Servis siparişi satırlarını **Servis sözleşmeleri** formunda otomatik olarak oluşturduğunuzda, bunları nasıl gruplandırmak istediğinizi belirtmek için aşağıdaki seçeneklerden birini seçebilirsiniz:

  - **Servis sözleşmesine göre**

  - **Servis görevine göre**

  - **Personele göre**

  - **Servis nesnesine göre**

## <a name="example"></a>Örnek

Başlangıç tarihi 31-03-2007 olan bir servis anlaşması oluşturun. **Servis siparişlerini birleştir** alanında, **Servis nesnesine göre**'yi seçin. Ardından, aşağıdaki servis anlaşması satırlarını oluşturabilirsiniz:

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sözleşme satır numarası</p></th>
<th><p>Hareket türü</p></th>
<th><p>Tanım</p></th>
<th><p>Aralık</p></th>
<th><p>Servis nesnesi</p></th>
<th><p>Başlangıç tarihi</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Saat</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Haftalık</p></td>
<td><p>X-1</p></td>
<td><p>01-04-2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Saat</strong></p></td>
<td><p>SAL2</p></td>
<td><p>İki haftalık</p></td>
<td><p>X-2</p></td>
<td><p>01-04-2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Saat</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Haftalık</p></td>
<td><p>X-2</p></td>
<td><p>01-04-2007</p></td>
</tr>
</tbody>
</table>


Servis anlaşması satırlarından herhangi biri için zaman pencereleri belirtmezsiniz. Bu nedenle, servis siparişi satırları karşılık geldikleri hesaplanmış günden başka bir güne taşınmaz.

Daha sonra, servis siparişi satırlarını **Servis siparişleri oluştur** formunda 01-04-2007'den 30-04-2007'ye kadar oluşturabilirsiniz.

Toplam olarak 10 servis siparişi oluşturulur. Seçtiğiniz birleştirilmiş ayar **Servis nesnesine göre** olduğundan, oluşturulan tüm servis siparişlerinde yalnızca bir özel servis nesnesine sahip servis sipariş satırları bulunmaktadır. Servis anlaşmasından oluşturulan ve aynı servis tarihi ile servis nesnesine sahip olan servis siparişi satırları aynı servis siparişinde birleştirilir.


> [!NOTE]
> <P>Bu örnekte, <STRONG>Servis yönetimi parametreleri</STRONG> formunda belirtilen takvimde kapalı gün bulunmamaktadır.</P>



Servis siparişi satırlarının servis siparişlerine ayrıntılı şekilde gruplandırılması, servis sözleşmesi satırlarında belirttiğiniz zaman aralığına göre gerçekleşmektedir.

## <a name="see-also"></a>Ayrıca bkz.

[Servis siparişlerini otomatik olarak oluşturma](create-service-orders-automatically.md)

  



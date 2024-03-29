---
title: Azaltma günleri örneği
description: Azaltma günleri örneği.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e588273244c88ffa208e88b66800dc7ce20d68
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674827"
---
# <a name="reduction-days-example"></a>Azaltma günleri örneği

[!include [banner](../includes/banner.md)]

Bir müşterinin bakım aboneliği için aşağıda açıklandığı şekilde bir abonelik hareketi oluşturdunuz.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Başlangıç tarihi</p></th>
<th><p>Bitiş tarihi</p></th>
<th><p>Abonelik</p></th>
<th><p>Abonelik türü</p></th>
<th><p>Proje</p></th>
<th><p>Kategori</p></th>
<th><p>Satış para birimi</p></th>
<th><p>Satış fiyatı</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01 Mart 2011</p></td>
<td><p>31 Mart 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Normal</strong></p></td>
<td><p>9013</p></td>
<td><p>AboKat2</p></td>
<td><p>Euro</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>

Müşteri, iki gün için (19 ve 11 Mart) servis karşılama ihtiyacı olmadığını bildiriyor. Abonelikten bu iki günü düşmeyi kabul ediyorsunuz.

Aşağıdaki tabloda açıklandığı gibi **Azaltma günleri** türünde yeni bir işlem oluşturursunuz.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Başlangıç tarihi</p></th>
<th><p>Bitiş tarihi</p></th>
<th><p>Abonelik</p></th>
<th><p>Abonelik türü</p></th>
<th><p>Proje</p></th>
<th><p>Kategori</p></th>
<th><p>Satış para birimi</p></th>
<th><p>Satış fiyatı</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10 Mart 2011</p></td>
<td><p>11 Mart 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>İndirim günleri</strong></p></td>
<td><p>9013</p></td>
<td><p>AboKat2</p></td>
<td><p>Euro</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>

Mart 2011'e ait işlemler faturalandırıldığında, 200 EUR değerindeki satış fiyatından 12,90 EUR düşülür. Abonelik işlemi için borçlandırılabilir tutar bu durumda 187,10 EUR olur ve iki işlem toplam 187,10 EUR olarak faturalandırılır.

## <a name="see-also"></a>Ayrıca bkz.

[Abonelik ücretlerindeki günleri azaltma](reduce-the-days-on-subscription-fees.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
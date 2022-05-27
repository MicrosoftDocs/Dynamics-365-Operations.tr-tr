---
title: Servis durumu ve ilerleme alanı etkileşimi
description: Servis siparişleri formunda, servis siparişi başlığındaki İlerleme alanı, tüm servis siparişinin durumunu yansıtır ve Durum tek tek servis siparişi satırlarının durumlarını rapor eder.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e83df9ca8ee19b5e29d4eccf2bd883ee6ddff62
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677660"
---
# <a name="service-status-and-progress-field-interaction"></a>Servis durumu ve ilerleme alanı etkileşimi

[!include [banner](../includes/banner.md)]

**Servis siparişleri** formunda, servis siparişi başlığındaki **İlerleme** alanı, tüm servis siparişinin durumunu yansıtır ve **Durum** tek tek servis siparişi satırlarının durumlarını rapor eder.

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>İlerleme</p></th>
<th><p>Satır 1 Durumu</p></th>
<th><p>Satır 2 Durumu</p></th>
<th><p>Satır 3 Durumu</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>İşlemde</strong></p></td>
<td><p><strong>Oluşturuldu</strong></p></td>
<td><p><strong>Oluşturuldu</strong></p></td>
<td><p><strong>Oluşturuldu</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>İşlemde</strong></p></td>
<td><p><strong>İptal edildi</strong></p></td>
<td><p><strong>Oluşturuldu</strong></p></td>
<td><p><strong>Oluşturuldu</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>İşlemde</strong></p></td>
<td><p><strong>Oluşturuldu</strong></p></td>
<td><p><strong>İptal edildi</strong></p></td>
<td><p><strong>Deftere nakledildi</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>İptal edildi</strong></p></td>
<td><p><strong>İptal edildi</strong></p></td>
<td><p><strong>İptal edildi</strong></p></td>
<td><p><strong>İptal edildi</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Deftere nakledildi</strong></p></td>
<td><p><strong>Deftere nakledildi</strong></p></td>
<td><p><strong>Deftere nakledildi</strong></p></td>
<td><p><strong>Deftere nakledildi</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Deftere nakledildi</strong></p></td>
<td><p><strong>Deftere nakledildi</strong></p></td>
<td><p><strong>İptal edildi</strong></p></td>
<td><p><strong>İptal edildi</strong></p></td>
</tr>
</tbody>
</table>

Tüm satırların durumu **Oluşturuldu** ise, servis siparişinin ilerlemesi devam ediyordur; satırlardan bazısının durumu **İptal edildi** ya da **Deftere nakledildi** ise işleme devam ediyordur.

Servis siparişindeki tüm satırlar **Deftere nakledildi** olarak işaretlenmişse, sipariş durumunun ilerlemesi **Deftere nakledildi**'dir. Bazı satırlar **Deftere nakledildi** ve bazıları **İptal edildi** ise, ilerleme hala **Deftere nakledildi** şeklindedir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

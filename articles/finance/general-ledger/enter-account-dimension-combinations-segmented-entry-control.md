---
title: Hesap ve boyut kombinasyonları (segmentlere ayrılmış giriş kontrolü) girme
description: Bu makalede, hesap ve boyut birleşimlerinin veya genel muhasebe hesaplarının nasıl girileceği açıklanmaktadır. Giriş deneyimine sıklıkla bölümlenmiş giriş denetimi denir.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 872ee7812d98e6102798c3a10773176541c02c90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186659"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a>Hesap ve boyut kombinasyonları (segmentlere ayrılmış giriş kontrolü) girme

[!include [banner](../includes/banner.md)]

Bu makalede, hesap ve boyut birleşimlerinin veya genel muhasebe hesaplarının nasıl girileceği açıklanmaktadır. Giriş deneyimine sıklıkla bölümlenmiş giriş denetimi denir.

Kullanıcılar çeşitli sayfalarda, örneğin genel günlük, bütçeleme ve nakil tanımları sayfalarında hesap ve boyut kombinasyonları girebilirler. Geçerli hesap ve boyut kombinasyonları, deftere atanan hesap yapılarına ve hesap yapılarına atanan gelişmiş kurallara bağlıdır. Kullanıcılar bir kombinasyon girdiğinde değerleri el ile yazabilir veya zengin, arama deneyiminin avantajlarından yararlanabilirler. Alana girdiğinizde, yazmaya başlayabilirsiniz ve alan değeri ve açıklamayı arar. Örneğin, 180 yazarsanız, bu sayı bileşimi ile başlayan herhangi bir değeri arar. Veya nakit yazabilirsiniz ve nakit ile başlayan bir açıklamaya sahip olan herhangi bir değeri arar. Değer veya açıklamanın arama kriterini içerip içermediğini aramak için \*Nakit veya \*180 gibi bir joker de kullanabilirsiniz. 

Aşağıdaki tabloda arama kapatıldığında kullanılabilecek klavye kısayolları açıklanmaktadır.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Klavye kısayolu</th>
<th>Eylem</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alt+Aşağı Ok</td>
<td>Aramayı açar. Alt + Aşağı Ok tuşlarına ikinci defa basarsanız odak, çıkmadaki segmentlere taşınır.</td>
</tr>
<tr class="even">
<td><ul>
<li>Enter ve Shift+Enter</li>
<li>Hesap planı ayırıcısı</li>
<li>Sağ Ok ve Sol Ok</li>
</ul></td>
<td>Bir sonraki veya bir önceki segmente geçer.</td>
</tr>
<tr class="odd">
<td>Sekme</td>
<td>Izgaradaki bir sonraki alana geçer.</td>
</tr>
</tbody>
</table>

Aşağıdaki tabloda arama açıkken kullanılabilecek klavye kısayolları açıklanmaktadır.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Klavye kısayolu</th>
<th>Eylem</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Esc</td>
<td>Aramayı kapatır.</td>
</tr>
<tr class="even">
<td><ul>
<li>Yukarı Ok ve Aşağı Ok</li>
<li>Page Up ve Page Down</li>
<li>Home ve End</li>
</ul></td>
<td>Listelerdeki bir önceki veya bir sonraki değere, bir önceki veya bir sonraki değer grubuna veya aramadaki ilk veya son öğeye geçer.</td>
</tr>
<tr class="odd">
<td><ul>
<li>Hesap planı ayırıcısı</li>
<li>Sağ Ok ve Sol Ok</li>
</ul></td>
<td>Bir sonraki veya bir önceki segmente geçer.</td>
</tr>
<tr class="even">
<td>Sekme</td>
<td>Izgaradaki bir sonraki alana geçer.</td>
</tr>
<tr class="odd">
<td>Alt+W</td>
<td><strong>Tümünü göster</strong> ile <strong>Geçerli olanı göster</strong> arasında geçiş sağlar.</td>
</tr>
</tbody>
</table>





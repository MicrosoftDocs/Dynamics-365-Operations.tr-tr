---
title: "İleri tarih atılmış çekler"
description: "Bu makalede, Microsoft Dynamics 365 for Operations&quot;da ileri tarih atılmış çeklere verilen destek hakkında bilgiler verilmektedir. İleri tarih atılmış çekler, ileri bir tarihte ödeme yapmak veya almak için kesilen çeklerdir. Bu nedenle, çek belirtilen tarihe kadar nakde çevrilemez."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: acc147105779f3857ea66ace8537da133e4d3a5c
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="postdated-checks"></a>İleri tarih atılmış çekler

[!include[banner](../includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Operations'da ileri tarih atılmış çeklere verilen destek hakkında bilgiler verilmektedir. İleri tarih atılmış çekler, ileri bir tarihte ödeme yapmak veya almak için kesilen çeklerdir. Bu nedenle, çek belirtilen tarihe kadar nakde çevrilemez.

Microsoft Dynamics 365 for Operations aşağıdaki tabloda gösterildiği gibi hem Borç hesapları hem Alacak hesapları altında ileri tarih atılmış çekler için tam yönetim döngüsünü destekler.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Senaryo</th>
<th>Ayrıntılı</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vadeli çek oluşturma</td>
<td>Yeni bir ödeme yöntemi ayarlamanız, verilen çekler, alınan çekler ve stopaj vergisi kliring hesaplarının ödeme rutinini belirtmeniz gerekir.</td>
</tr>
<tr class="even">
<td>Kaydolun ve satıcının vadeli çekini nakledin.</td>
<td>Bir satıcıya kestiğiniz ileri tarih atılmış çekin ayrıntılarını kaydedin. Ödeme deftere nakledildiğinde, satıcı yükümlülüğü tanınmış, ancak banka hesabına alacak kaydedilmemiştir. Bunun yerine, bu amaçla bir kliring hesabı kullanılır.</td>
</tr>
<tr class="odd">
<td>Bir müşteri için vadeli çeki kayıt edin ve nakledin</td>
<td>Bir müşteriden alınan ileri tarih atılmış bir çekin ayrıntılarını kaydedin. Ödeme deftere nakledildiğinde, müşteri alacaklandırılmış, ancak banka hesabına borç kaydedilmemiştir. Bunun yerine, bu amaçla bir kliring hesabı kullanılır.</td>
</tr>
<tr class="even">
<td>Bir müşteri veya satıcı için ileri tarih atılmış bir yedek çeki kaydedip deftere nakletme</td>
<td>
Bir satıcıya verdiğiniz veya bir müşteriden aldığınız orijinal çek kaybolur veya hasar görürse, ileri tarih atılmış bir yedek çek yazabilirsiniz. Çek ayrıntılarını kaydederken, orijinal çeke bir referans girin ve yeni çekin o orijinalin yedeği olduğunu belirtin. Yedek çeki de deftere nakledebilirsiniz.</td>
</tr>
<tr class="odd">
<td>İleri tarih atılmış bir müşteri çekini bir satıcıya transfer etme</td>
<td>Bir müşteriden ileri tarih atılmış bir çek aldığınızda, bu çeki bir satıcıya ödeme olarak transfer edebilirsiniz.</td>
</tr>
<tr class="even">
<td>Bir müşteri veya satıcı için, ileri tarih atılmış bir çeki kapatma</td>
<td>İleri tarih atılmış bir çekin tarihi geldiğinde müşteri veya satıcı için bir bağlantı hesabına nakledilen çeki kapatın. Çek kapatılınca, daha önce kullanılan kliring hesabına karşı bankaya borç veya alacak yazılır.</td>
</tr>
<tr class="odd">
<td>Bir satıcı için, ileri tarih atılmış çeki iptal etme</td>
<td>Bu gibi durumlarda deftere nakledilen ileri tarhi atılmış bir çeki iptal edebilirsiniz: - Çek banka tarafından döndürülür.
- Çek yanlış bir faturaya uygulanmıştır.
- Çek karşılığında nakit ödeme yapılmıştır.
</td>
</tr>
<tr class="even">
<td>İleri tarih atılmış bir çekin ödemesini durdurma</td>
<td>Yetersiz fon, satıcıyla anlaşma koşullarında değişiklik, satıcıdan tedarik edilen malların kusurlu olması veya satıcıya iade edilmesi gibi nedenlerle, satıcıya verilen, ileri tarih atılmış bir çekin ödemesini durdurabilirsiniz. Yalnızca takasa girmemiş çeklerin ödemesini durdurabilirsiniz.</td>
</tr>
</tbody>
</table>








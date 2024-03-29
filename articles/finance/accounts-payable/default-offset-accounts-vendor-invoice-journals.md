---
title: Satıcı faturası ve fatura onay günlükleri için varsayılan mahsup hesaplar
description: Bu makale, fatura günlükleri için varsayılan hesapları nereye atamanız gerektiğine karar vermenize yardımcı olur.
author: abruer
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.form: LedgerJournalTable
ms.openlocfilehash: ed75e0a3b9994d061e94d07ffcc43e3b73bec55e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281687"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a>Satıcı faturası ve fatura onay günlükleri için varsayılan mahsup hesaplar

[!include [banner](../includes/banner.md)]

Varsayılan mahsup hesapları, aşağıdaki satıcı faturası günlük sayfalarında kullanılır:

-   Fatura günlüğü
-   Fatura onay günlüğü

Fatura günlükleri için varsayılan hesaplar atamanız gerekip gerekmediğine karar vermenize yardımcı olacak aşağıdaki tabloyu kullanın.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Varsayılan hesapları buradan ayarla</th>
<th>Varsayılan hesaplar nerede sağlanıyor</th>
<th>Bu seçenek işlemi nasıl etkiler</th>
<th>Ne zaman bu seçeneği kullanmalısınız</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Satıcı grubu</strong> – <strong>Varsayılan hesap ayarı</strong> sayfasında satıcı grupları için varsayılan mahsup hesapları ayarlayın. Bu sayfayı <strong>Satıcı grupları</strong> sayfasından açabilirsiniz.</td>
<td><ul>
<li>Satıcı hesabı</li>
<li>Satıcı hesapları için varsayılan hesaplar belirtilmediyse, satıcı grubundaki satıcı hesapları için günlük girişleri</li>
</ul></td>
<td>Satıcı grupları için varsayılan mahsup hesaplar <strong>Varsayılan hesap ayarı</strong> sayfasındaki satıcılar için varsayılan mahsup hesapları olarak gösterilir. Bu sayfayı <strong>Tüm satıcılar</strong> liste sayfasından açabilirsiniz.</td>
<td>Genellikle zaman içinde aynı satıcı gruplarından aynı türde maddeler için ödeme yapıyorsanız bu seçeneği kullanın.</td>
</tr>
<tr class="even">
<td><strong>Satıcı hesabı</strong> – <strong>Varsayılan hesap ayarı</strong> sayfasındaki satıcı hesapları için varsayılan hesaplar ayarlayın. Bu sayfayı <strong>Satıcılar</strong> sayfasından açabilirsiniz.</td>
<td>Satıcı hesabı için günlük girişleri</td>
<td>Satıcı hesapları için varsayılan mahsup hesaplar, satıcı hesabına ilişkin günlük girişleri için varsayılan mahsup hesapları olarak gösterilir.</td>
<td>Genellikle zaman içinde aynı satıcılara aynı türde maddeler için ödeme yapıyorsanız bu seçeneği kullanın.</td>
</tr>
<tr class="odd">
<td><strong>Günlük adları</strong> – <strong>Günlük adları</strong> sayfasında günlükler için varsayılan mahsup hesapları ayarlayın. <strong>Sabit mahsup hesap</strong> seçeneği seçin. Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük adlarında varsayılan mahsup hesapları belirtemeyeceğinizi unutmayın.</td>
<td><ul>
<li>Günlük adını kullanan günlük başlığı</li>
<li>Günlük adını kullanan günlüklerdeki günlük girişleri</li>
</ul></td>
<td><strong>Günlük adları</strong> sayfasında <strong>Sabit mahsup hesap</strong> seçeneği seçilirse, günlük adı için mahsup hesap satıcı veya satıcı grubuna ilişkin varsayılan mahsup hesabı geçersiz kılar.</td>
<td>Satıcı veya satıcının ait olduğu satıcı grubuna bakılmaksızın, belirli hesaplara borçlandırılan belirli maliyetler ve giderler için günlükleri ayarlarken bu seçeneği kullanın.</td>
</tr>
<tr class="even">
<td><strong>Günlük adları</strong> – <strong>Günlük adları</strong> sayfasında günlükler için varsayılan mahsup hesapları ayarlayın. <strong>Sabit mahsup hesap</strong> seçimini kaldırın. Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük adlarında varsayılan mahsup hesapları belirtemeyeceğinizi unutmayın.</td>
<td><ul>
<li>Günlük başlığı</li>
<li>Günlük adını kullanan günlüklerdeki günlük girişleri</li>
</ul></td>
<td>Bu varsayılan girişler günlük başlığı sayfalarında kullanılır ve günlük başlığı sayfasındaki mahsup hesap, günlük fişi sayfalarında varsayılan giriş olarak kullanılır. <strong>Günlük adları </strong>sayfasındaki varsayılan hesaplar yalnızca satıcı hesabı için varsayılan hesaplar ayarlanmadığında kullanılır.</td>
<td>Bu seçeneği, varsayılan satıcı mahsup hesabı atanmadığında kullanılan varsayılan hesaplar ayarlamak için kullanın.</td>
</tr>
<tr class="odd">
<td><strong>Günlük başlığı</strong> – Günlük fişi sayfalarındaki varsayılan giriş olarak bir günlük için varsayılan mahsup hesap ayarlayın. Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük başlığında varsayılan mahsup hesaplar belirtemeyeceğinizi unutmayın.</td>
<td>Günlükteki günlük girişleri</td>
<td>Bir günlüğe ilişkin varsayılan mahsup hesabı, günlük fişi sayfalarında varsayılan giriş olarak kullanılır.</td>
<td>Bir günlükteki girişlerin çoğu aynı mahsup hesabına sahip olduğunda veri girişini hızlandırmak için bu seçeneği kullanın.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

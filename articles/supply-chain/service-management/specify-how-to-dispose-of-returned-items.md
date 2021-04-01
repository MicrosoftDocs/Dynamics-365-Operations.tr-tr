---
title: İade edilen maddelerin nasıl elden çıkarılacağını belirtme
description: İade edilen maddelerin nasıl elden çıkarılacağını belirtin.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61bff50d55ed4c251918a327f2a033369e731bf0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242385"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>İade edilen maddelerin nasıl elden çıkarılacağını belirtme 

[!include [banner](../includes/banner.md)]


Bir iade siparişini işlerken, ürünün neden iade edildiğini tanımlamak için bir iade neden kodu belirtmeniz gerekir. Bir elden çıkarma kodu ve iade edilen ürün ile birlikte ne yapılması gerektiğini belirlemek için bir elden çıkarma eylemi de belirtmeniz gerekir.

Elden çıkarma kodu, iade siparişini oluşturduğunuzda, madde varışını kaydettiğinizde veya madde varışında sevk irsaliyesi güncelleştirmesi yaptığınızda ve bir karantina emrini bitirdiğinizde geçerlidir.

İş süreçlerini desteklemek için gereken herhangi bir elden çıkarma kodunu tanımlayabilirsiniz. Aşağıdaki tabloda iade edilen maddeyi elden çıkarma atamak için genellikle kullanılan kodlar sağlanmaktadır.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elden Çıkarma türü</p></th>
<th><p>Genel kod</p></th>
<th><p>Tanım</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Elden çıkarma</p></td>
<td><p>SC</p></td>
<td><p>Hurdaya Ayır/İmha Et</p></td>
</tr>
<tr class="even">
<td><p>Elden çıkarma</p></td>
<td><p>DC</p></td>
<td><p>Hayır Kurumuna Bağışla</p></td>
</tr>
<tr class="odd">
<td><p>Elden çıkarma</p></td>
<td><p>TD</p></td>
<td><p>Üçüncü Taraf Elden Çıkarma</p></td>
</tr>
<tr class="even">
<td><p>Elden çıkarma</p></td>
<td><p>SL</p></td>
<td><p>Kurtar</p></td>
</tr>
<tr class="odd">
<td><p>Elden çıkarma</p></td>
<td><p>TS</p></td>
<td><p>Üçüncü Taraf Satışı (İkincil Piyasalar)</p></td>
</tr>
<tr class="even">
<td><p>Onarım/Değiştirme</p></td>
<td><p>RW</p></td>
<td><p>Yeniden İşle</p></td>
</tr>
<tr class="odd">
<td><p>Onarım/Değiştirme</p></td>
<td><p>RF</p></td>
<td><p>Yeniden Üret/Yeniden Sağla</p></td>
</tr>
<tr class="even">
<td><p>Onarım/Değiştirme</p></td>
<td><p>MD</p></td>
<td><p>Değişiklik Yap</p></td>
</tr>
<tr class="odd">
<td><p>Onarım/Değiştirme</p></td>
<td><p>RP</p></td>
<td><p>Onar</p></td>
</tr>
<tr class="even">
<td><p>Onarım/Değiştirme</p></td>
<td><p>RV</p></td>
<td><p>Satıcıya İade Et</p></td>
</tr>
<tr class="odd">
<td><p>Diğer</p></td>
<td><p>AI</p></td>
<td><p>Olduğu gibi kullan</p></td>
</tr>
<tr class="even">
<td><p>Diğer</p></td>
<td><p>RS</p></td>
<td><p>Yeniden sat</p></td>
</tr>
<tr class="odd">
<td><p>Diğer</p></td>
<td><p>EX</p></td>
<td><p>Döviz</p></td>
</tr>
<tr class="even">
<td><p>Diğer</p></td>
<td><p>MS</p></td>
<td><p>Çeşitli</p></td>
</tr>
</tbody>
</table>


Tanımladığınız her elden çıkarma kodu için bir elden çıkarma eylemi seçmeniz gerekir. Elden çıkarma eylemi elden çıkarma kodlarının fiziksel ve mali etkilerini belirler. Örneğin, elden çıkarma eylemi iade edilen maddenin fiziksel olarak işlenme şeklini, iade edilen ürünün mali etkisini ve müşteriye bir değiştirme maddesi gönderilip gönderilmeyeceğini belirler. İş gereksinimlerinize göre sınırsız sayıda elden çıkarma kodu tanımlayabilirsiniz, ancak arasından seçim yapabileceğiniz yalnızca altı önceden tanımlanmış değerlendirme eylemi bulunur. Aşağıdaki tabloda değerlendirme eylemleri ve tanımlamaları verilmektedir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Elden çıkarma eylemi</p></th>
<th><p>Tanım</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alacak</strong></p></td>
<td><p>Maddeyi stoğa iade edin ve müşteriyi alacaklandırın.</p></td>
</tr>
<tr class="even">
<td><p><strong>Yalnızca alacaklandır</strong></p></td>
<td><p>Maddenin iade edilmesini talep etmeden veya beklemeden müşteriyi alacaklandırın.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Hurda</strong></p></td>
<td><p>Maddeyi hurdaya çıkarın ve müşteriyi alacaklandırın.</p></td>
</tr>
<tr class="even">
<td><p><strong>Değiştir ve alacaklandır</strong></p></td>
<td><p>Maddeyi stoğa iade edin, değişiklik siparişi oluşturun ve müşteriyi alacaklandırın.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Değiştir ve ıskartaya ayır</strong></p></td>
<td><p>Maddeyi hurdaya çıkarın, değişiklik siparişi oluşturun ve müşteriyi alacaklandırın.</p></td>
</tr>
<tr class="even">
<td><p><strong>Müşteriye iade et</strong></p></td>
<td><p>İade edilen ürünü reddedin ve müşteriye iade edin.</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Bir karantina emri için elden çıkarma kodu seçme

1.  **Stok yönetimi** \> **Periyodik** \> **Kalite yönetimi** \> **Karantina emirleri**'ne tıklayın.

2.  Mevcut bir karantina emri için **Genel bakış** sekmesindeki **Elden çıkarma kodu** alanından bir eylem seçin.



## <a name="see-also"></a>Ayrıca bkz.

[Karantina siparişi (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))

[Elden çıkarma kodları (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
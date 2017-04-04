---
title: "İleri tarih atılmış çekler"
description: "Bu makalede, Microsoft Dynamics 365 işlemleri için İleri tarih atılmış denetimlerinde desteği hakkında bilgi sağlar. İleri tarih atılmış çekler, ileri bir tarihte ödeme yapmak veya almak için kesilen çeklerdir. Bu nedenle, çek belirtilen tarihe kadar nakde çevrilemez."
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
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>İleri tarih atılmış çekler

Bu makalede, Microsoft Dynamics 365 işlemleri için İleri tarih atılmış denetimlerinde desteği hakkında bilgi sağlar. İleri tarih atılmış çekler, ileri bir tarihte ödeme yapmak veya almak için kesilen çeklerdir. Bu nedenle, çek belirtilen tarihe kadar nakde çevrilemez.

Microsoft Dynamics 365 işlemleri için tam yönetim döngüsü Alacak hesapları ve Borç hesapları, ileri tarih atılmış Çekler için aşağıdaki tabloda gösterildiği gibi destekler.
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
<td>Bir satıcıya kestiğiniz ileri tarih atılmış çekin ayrıntılarını kaydedin. Ödemeyi deftere nakledildiğinde, satıcı yükümlülük tanınıyor, ancak banka hesabı değil henüz alacak. Bunun yerine, bu amaçla bir kliring hesabı kullanılır.</td>
</tr>
<tr class="odd">
<td>Bir müşteri için vadeli çeki kayıt edin ve nakledin</td>
<td>Bir müşteriden alınan ileri tarih atılmış bir çekin ayrıntılarını kaydedin. Ödemeyi deftere nakledildiğinde alacak müşterinin kredi olmakla birlikte, banka hesabı değil henüz borç. Bunun yerine, bu amaçla bir kliring hesabı kullanılır.</td>
</tr>
<tr class="even">
<td>Kaydetmek ve deftere naklet onay bir müşteri veya satıcı için bir değiştirme ileri tarih atılmış</td>
<td>
Bir satıcıya verdiğiniz veya bir müşteriden aldığınız orijinal çek kaybolur veya hasar görürse, ileri tarih atılmış bir yedek çek yazabilirsiniz. Çek ayrıntılarını kaydederken, orijinal çeke bir referans girin ve yeni çekin o orijinalin yedeği olduğunu belirtin. Yedek çeki de deftere nakledebilirsiniz.</td>
</tr>
<tr class="odd">
<td>Bir satıcıya müşteri ileri tarih atılmış onay aktarmak</td>
<td>Bir müşteriden ileri tarih atılmış bir çek aldığınızda, bu çeki bir satıcıya ödeme olarak transfer edebilirsiniz.</td>
</tr>
<tr class="even">
<td>Bir müşteri veya satıcı için postdated onay kapatma</td>
<td>İleri tarih atılmış bir çekin tarihi geldiğinde müşteri veya satıcı için bir bağlantı hesabına nakledilen çeki kapatın. Çek kapatılınca, daha önce kullanılan kliring hesabına karşı bankaya borç veya alacak yazılır.</td>
</tr>
<tr class="odd">
<td>Bir satıcı için postdated onay iptal et</td>
<td>Bu gibi durumlarda postdated nakledilen onay iptal edebilirsiniz:-Çek Banka tarafından döndürülür.
-Çek yanlış fatura için uygulanır.
-Nakit ödeme onay karşı yapılır.
</td>
</tr>
<tr class="even">
<td>Ödeme için çek postdated Durdur</td>
<td>Yetersiz fon, satıcıyla anlaşma koşullarında değişiklik, satıcıdan tedarik edilen malların kusurlu olması veya satıcıya iade edilmesi gibi nedenlerle, satıcıya verilen, ileri tarih atılmış bir çekin ödemesini durdurabilirsiniz. Sadece temizlenmiş henüz çeklerdeki Dur ödeme kullanabilirsiniz.</td>
</tr>
</tbody>
</table>






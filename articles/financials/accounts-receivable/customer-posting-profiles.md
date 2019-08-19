---
title: Müşteri deftere nakil profilleri
description: Müşteri deftere nakil profilleri, müşteri hareketlerinin genel muhasebeye naklini kontrol eder.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bb2784d70e99c3c3443bed1b8cb040552b5b6f6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835130"
---
# <a name="customer-posting-profiles"></a>Müşteri deftere nakil profilleri

[!include [banner](../includes/banner.md)]

Müşteri deftere nakil profilleri, müşteri hareketlerinin genel muhasebeye naklini kontrol eder.

<a name="customer-posting-profiles"></a>Müşteri deftere nakil profilleri
-------------------------

Müşteri deftere nakil profilleri tüm müşterilere, bir müşteri grubuna veya tek bir müşteriye genel muhasebe hesapları ve belge ayarları atamanızı sağlar. Satış siparişleri, serbest metin faturaları, nakit ödemeler, tahsilat mektupları ve vade farkı dekontları işlemleri oluşturduğunuzda, bu ayarlar kullanılacaktır. Bazı hareketler için, bu sayfadaki hareket için ayarlanan nakil profillerinden farklılık gösteren ve bunların yerini alan bir nakil profili seçebilirsiniz. 

Varsayılan deftere nakletme profili, Alacak Hesapları sayfasındaki Genel Muhasebe ve Satış Vergisi hızlı sekmesinde tanımlanır. Varsayılan nakil profili, onu farklı nakil profiline gerekiyorsa değiştirebileceğiniz, yeni belge başlığındaki otomatik olarak eklenir.

Ayrıca, nakil tanımlarını hareket nakil türleriyle, Hareket nakil tanımları sayfasında ilişkilendirebilirsiniz. Nakil tanımları müşteri hareketlerinin, nakil profilleri yerine genel muhasebe defterine nakledilmesini denetler.

## <a name="creating-a-posting-profile"></a>Bir nakil profili oluşturmak
Seçili nakil profilini kullanan hareketlerin nakledilmesinde kullanılan genel muhasebe hesaplarını belirtin. Bir hesap kodu ve mümkün olduğu durumlarda seçili nakil profili için bir hesap veya grup numarası seçin. Deftere nakil işleminde, en uygun hesap kodu, hesap numarası veya grup veya numara birleşimini aşağıdaki öncelik sırasına göre aranarak her hareket için en uygun nakil profili bulunur.

| **Hesap kodu** alan değeri | **Hesap/Grup numarası** alan değeri            | Arama önceliği |
|------------------------------|-------------------------------------------------|-----------------|
| **Tablo**                    | Özel müşteri hesabı                       | 1               |
| **Grup**                    | Müşteriye atanmış olan müşteri grubu | 2               |
| **Tümü**                      | Boşluk                                           | 3               |

Tüm müşteri hareketlerinin aynı deftere nakil profili içermesini istiyorsanız, Hesap kodu alanında Tümü değerini içeren yalnızca bir nakil profili ayarlayın. Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin:

<table>
<thead>
<tr class="header">
<th>Alan</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Nakil profili</strong></td>
<td>Nakil profili için bir kod girin. Örneğin ulusal para birimini içeren müşteri bakiyeleri için bir hesap elde etmek üzere iki nakil profili, yabancı para birimini içeren müşteri bakiyeleri için başka bir nakil profili oluşturabilirsiniz. Birini Ulusal, diğerini Yabancı olarak adlandırabilirsiniz.</td>
</tr>
<tr class="even">
<td><strong>Açıklama</strong></td>
<td>Nakil profilinin açıklamasını girin. Bu yalnızca bu sayfada görüntülediğinizde, deftere nakil profilini daha iyi tanımlamak için kullanılır.</td>
</tr>
<tr class="odd">
<td><strong>Hesap kodu</strong></td>
<td>Nakil profilinin tek bir müşteri, bir müşteri grubu veya tüm müşteriler için mi geçerli olduğunu belirtin:
<ul>
<li><strong>Tablo</strong> – Nakil profili bir müşteri için geçerlidir. Hesap/Grup numarası alanında müşteri hesabını seçin.</li>
<li><strong>Grup</strong> – Nakil profili bir müşteri grubu geçerlidir. Hesap/Grup numarası alanında müşteri grubunu seçin.</li>
<li><strong>Tümü</strong> – Nakil profili tüm müşteriler için geçerlidir. Hesap/Grup numarası alanını boş bırakın.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Hesap/Grup numarası</strong></td>
<td>Hesap kodu alanında Tablo seçiliyse, nakil profiliyle ilişkilendirilmiş müşterinin hesap numarasını seçin. Eğer Grup seçiliyse, müşteri grubunu seçin. Tümü seçiliyse, bu alanı boş bırakın.</td>
</tr>
<tr class="odd">
<td><strong>Özet hesap</strong></td>
<td>Nakil profiliyle ilişkilendirilmiş müşteriler için müşteri özet hesabı olarak kullanılacak genel muhasebe hesabını seçin.</td>
</tr>
<tr class="even">
<td><strong>Kapatma hesabı</strong></td>
<td>Nakit akışı tahminleri için kullanılacak likidite genel muhasebe hesabını seçin. Bu alan yalnızca nakit akışı tahminleri etkinleştirilmişse görünür.</td>
</tr>
<tr class="odd">
<td><strong>Satış vergisi ön ödemeleri</strong></td>
<td>Avans olarak alınmış ödemeler için satış vergisinin hesabını seçin.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Not" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Not</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bir ödeme bir ön ödeme olarak işaretlendiğinde kullanılacak nakil profilini belirtmek için Alacak hesapları parametreleri sayfasını kullanın.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>İskonto hesabı borçları</strong></td>
<td>İskonto borçları genel muhasebe hesabını seçin.</td>
</tr>
<tr class="odd">
<td><strong>Tahsilat mektubu sırası</strong></td>
<td>Tahsilat mektubu sırasının, nakil profilinin atandığı müşteriler için kullanılacak tanımlayıcısını seçin.</td>
</tr>
<tr class="even">
<td><strong>Vade farkı kodu</strong></td>
<td>Nakil profilinin atandığı müşteriler için faizin hesaplanmasında kullanılacak faiz kodunu seçin.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Tablo kısıtlamaları**

Seçili nakil profilini içeren hareketler için hareketlerin otomatik olarak kapatılması, faiz hesaplanması ve tahsilat mektuplarının verilip verilmeyeceğini belirtin. Ayrıca, seçili nakil profilini içeren hareketler kapatıldığında kullanılan hesabı seçin seçebilirsiniz.

Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin:

| Alan                 | Açıklama                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kapatma**        | Bu nakil profilini içeren hareketlerin otomatik kapatılmasını etkinleştirmek için bu geçiş tuşunu seçin. Bu geçiş tuşu temizlenirse, hareketleri, Açık hareketleri kapat sayfasını ya da Müşteri ödemelerini girme sayfasını kullanarak elden kapatmanız gerekir. |
| **İlgi alanı**          | Bu profili kullanan müşteri hesapları için bekleyen bakiyelerdeki vade farkı hesaplanacaksa bu geçiş tuşunu seçin. Bu geçiş tuşu temizlenirse, bu müşteriler için vade farkı hesaplanmaz.                                           |
| **Tahsilat mektubu** | Bu profili kullanan müşteri hesapları için tahsilat mektupları oluşturulacaksa, bu geçiş tuşunu seçin. Bu geçiş tuşu temizlenirse, bu müşteriler için tahsilat mektupları oluşturulmaz.                                                 |
| **Kapat**             | Bu nakil profilini içeren hareketler kapatılırken değiştirmek istediğiniz nakil profilini seçin. Bir hareket tamamen kapatıldığında kapanmış kabul edilir.                                                                           |



Daha fazla bilgi için bkz. [Müşteri ödeme genel bakışı](../cash-bank-management/tasks/customer-payment-overview.md).


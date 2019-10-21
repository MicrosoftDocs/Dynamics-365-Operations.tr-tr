---
title: Satıcı deftere nakil profilleri
description: Satıcı deftere nakil profilleri, satıcı hareketlerinin genel muhasebeye naklini kontrol eder.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43450c5f7ab8295b896b591880da9d0bddd955cf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189304"
---
# <a name="vendor-posting-profiles"></a>Satıcı deftere nakil profilleri

[!include [banner](../includes/banner.md)]

Satıcı deftere nakil profilleri, satıcı hareketlerinin genel muhasebeye naklini kontrol eder.

<a name="vendor-posting-profiles"></a>Satıcı deftere nakil profilleri
-----------------------

Satıcı deftere nakil profilleri tüm satıcılara, bir satıcı grubuna veya tek bir satıcıya genel muhasebe hesapları ve belge ayarları atamanızı sağlar. Bu ayarlar satınalma siparişleri, satıcı faturaları ve nakit ödemeler oluşturduğunuzda kullanılacaktır. Bazı hareketler için, bu sayfadaki hareket için ayarlanan nakil profillerinden farklılık gösteren ve bunların yerini alan bir nakil profili seçebilirsiniz. Varsayılan deftere nakletme profili, **Borç Hesapları parametreleri** sayfasındaki **Genel Muhasebe ve Satış Vergisi** hızlı sekmesinde tanımlanır. Varsayılan nakil profili, onu farklı nakil profiline gerekiyorsa değiştirebileceğiniz, yeni belge başlığındaki otomatik olarak eklenir.

Ayrıca, nakil tanımlarını hareket nakil türleriyle, **Hareket nakil tanımları** sayfasında ilişkilendirebilirsiniz. Nakil tanımları satıcı hareketlerinin, nakil profilleri yerine genel muhasebe defterine nakledilmesini denetler.

## <a name="creating-a-posting-profile"></a>Bir nakil profili oluşturmak
### <a name="setup"></a>**Kurulum**

Seçili nakil profilini kullanan hareketlerin nakledilmesinde kullanılan genel muhasebe hesaplarını belirtin. Bir hesap kodu ve mümkün olduğu durumlarda seçili nakil profili için bir hesap veya grup numarası seçin. Deftere nakil işleminde, en uygun hesap kodu, hesap numarası veya grup veya numara birleşimini aşağıdaki öncelik sırasına göre aranarak her hareket için en uygun nakil profili bulunur:

| **Hesap kodu** alan değeri | **Hesap/Grup numarası** alan değeri        | Arama önceliği |
|------------------------------|---------------------------------------------|-----------------|
| **Tablo**                    | Belirtilmiş satıcı hesabı.                     | 1               |
| **Grup**                    | Satıcıya atanmış satıcı grubu. | 2               |
| **Tümü**                      | Boş                                       | 3               |

Tüm satıcı hareketlerinin aynı deftere nakil profili içermesini istiyorsanız, **Hesap kodu** alanında **Tümü** değerini içeren yalnızca bir nakil profili ayarlayın. Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin.

<table>
<thead>
<tr class="header">
<th>Alan</th>
<th>Tanım</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Deftere nakil profili</strong></td>
<td>Nakil profili için bir kod girin. Örneğin ulusal para birimini içeren satıcı bakiyeleri için bir hesap elde etmek üzere iki nakil profili, yabancı bir para birimini içeren satıcı bakiyeleri için başka bir nakil profili oluşturabilirsiniz. Birini Ulusal, diğerini Yabancı olarak adlandırabilirsiniz.</td>
</tr>
<tr class="even">
<td><strong>Açıklama</strong></td>
<td>Nakil profilinin açıklamasını girin.</td>
</tr>
<tr class="odd">
<td><strong>Hesap kodu</strong></td>
<td>Nakil profilinin belirli bir satıcı, bir satıcı grubu veya tüm satıcılar için mi geçerli olduğunu belirtin:
<ul>
<li><strong>Tablo</strong> – Nakil profili bir satıcı için geçerlidir. <strong>Hesap/Grup numarası</strong> alanında satıcı hesabını seçin.</li>
<li><strong>Grup</strong> – Nakil profili bir satıcı grubu geçerlidir. <strong>Hesap/Grup numarası</strong> alanında satıcı grubunu seçin.</li>
<li><strong>Tümü</strong> – Nakil profili tüm satıcılar için geçerlidir. <strong>Hesap/Grup numarası</strong> alanını boş bırakın.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Hesap/Grup numarası</strong></td>
<td><strong>Hesap kodu</strong> alanında <strong>Tablo</strong> seçiliyse, nakil profiliyle ilişkilendirilmiş satıcının hesap numarasını seçin. <strong>Grup</strong> seçiliyse bir satıcı grubu seçin. <strong>Tümü</strong> seçiliyse bu alanı boş bırakın.</td>
</tr>
<tr class="odd">
<td><strong>Özet hesap</strong></td>
<td>Nakil profilinin ilişkili olduğu satıcılar için özet hesabı olarak kullanılacak genel muhasebe hesabını seçin. Bu ana hesap için <strong> el ile girme</strong> giriş parametresine izin verme parametresi işaretlenecek. Bu hesabı sonradan hedef deftere nakit profilinden kaldırırsanız <strong>Ana hesaplar</strong> sayfasında <strong>El ile giriş yapılmasına izin verme</strong> ayarını da doğrulayın. 
<p><strong>Not:</strong> Eğer <strong>Nakil tanımlarını kullan</strong> seçeneği <strong>Genel muhasebe parametreleri</strong> sayfasında seçiliyse özet hesabı yerine satıcı faturaları için hareket nakil tanımı kullanılır.</p>
</td>
</tr>
<tr class="even">
<td><strong>Kapatma hesabı</strong></td>
<td>Nakit akışı tahminleri için kullanılacak likidite genel muhasebe hesabını seçin. Bu alan yalnızca nakit akışı tahmini etkinleştirildiğinde kullanılabilir.</td>
</tr>
<tr class="odd">
<td><strong>Satış vergisi ön ödemeleri</strong></td>
<td>Avans olarak alınmış ödemeler için satış vergisinin hesabını seçin.
<p><strong>Not:</strong> Bir ödeme, ön ödeme olarak işaretlendiğinde kullanılan <strong>Nakil</strong> profili, <strong>Borç hesapları parametreleri</strong>  sayfasının <strong>Genel muhasebe ve satış vergisi</strong>bölümündeki <strong>Ön ödeme günlüğü fişi</strong> alanında seçilir.</p>
</td>
</tr>
<tr class="even">
<td><strong>Varış</strong></td>
<td>Onaylanmayan satıcı faturaları hakkındaki bilgilerin nakledildiği genel muhasebe hesabını seçin. Bilgiler Fatura kayıt günlüğüne girilir. Örneğin, bir kullanıcı, fatura kaydına girdiklerinde satıcı faturaları hakkındaki temel bilgileri girer. Fatura kaydı nakledildiğinde, hareketler buraya ve <strong>Mahsup hesap</strong> alanına girilen hesaba nakledilir. Faturalar onaylandığında, borç varış hesabından satıcı özet hesabına nakledilir.</td>
</tr>
<tr class="odd">
<td><strong>Mahsup hesabı</strong></td>
<td>Fatura kaydını kullanarak güncelleştirilen onaylanmamış satıcı faturalarının mahsuben kullanılan genel muhasebe hesabını seçin. Mahsup hesabı Varış hesaplarına nakledilen hareketler için mahsup hesabı olarak işlev görür. Bu nedenle, hesap henüz onaylanmamış satıcı satınalma işlemleri içerir.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Tablo kısıtlamaları**

Seçili nakil profilini içeren hareketler için hareketlerin otomatik olarak kapatılması, faiz hesaplanması ve tahsilat mektuplarının verilip verilmeyeceğini belirtin. Ayrıca, seçili nakil profilini içeren hareketler kapatıldığında kullanılan hesabı seçin seçebilirsiniz.

Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin

| Alan          | Tanım                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kapatma** | Bu nakil profilini içeren hareketlerin otomatik kapatılmasını etkinleştirmek için bu seçeneği seçin. Bu seçenek temizlenirse, hareketleri, **Açık hareketleri kapat** sayfasını kullanarak elden kapatmanız gerekir. |
| **İptal**     | Bu nakil profilini içeren hareketlerin iptal edilmesi seçeneğine sahip olmak istiyorsanız bu seçeneği seçin.                                                                                                               |
| **Kapat**      | Bu nakil profilini içeren hareketler kapatılırken değiştirmek istediğiniz nakil profilini seçin. Bir hareket tamamen kapatıldığında kapanmış kabul edilir.                                       |

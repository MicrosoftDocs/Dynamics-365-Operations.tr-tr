---
title: Müşteri deftere nakil profilleri
description: Bu makalede, müşteri hareketlerinin genel muhasebe defterine nakledilmesini denetleyen müşteri deftere nakil profilleri açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04cf5b8656bccde974fb1adfdf830080e2f52436
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799585"
---
# <a name="customer-posting-profiles"></a>Müşteri deftere nakil profilleri

[!include [banner](../includes/banner.md)]

Bu makalede, müşteri hareketlerinin genel muhasebe defterine nakledilmesini denetleyen müşteri deftere nakil profilleri açıklanmaktadır.

## <a name="customer-posting-profiles"></a>Müşteri deftere nakil profilleri

Müşteri deftere nakil profilleri tüm müşterilere, bir müşteri grubuna veya tek bir müşteriye genel muhasebe hesapları ve belge ayarları atamanızı sağlar. Satış siparişleri faturaları, serbest metin faturaları, proje faturaları, ödeme günlükleri, tahsilat mektupları ve vade farkı dekontları işlemleri oluşturduğunuzda, bu ayarlar kullanılacaktır. 

Varsayılan deftere nakletme profili, **Alacak hesapları parametreleri** sayfasındaki **Genel Muhasebe ve Satış Vergisi** sekmesinde tanımlanır. Ardından otomatik olarak yeni belgelerin başlığına eklenir. Farklı bir deftere nakil profili gerekiyorsa bunu orada değiştirebilirsiniz. 

Müşterilerden ön ödemeler kabul eden kuruluşlar, ön ödemeler için ikinci bir deftere nakil profili konfigüre eder ve ön ödemeler için varsayılan deftere nakil profili olarak parametrelere bağlar. Daha fazla bilgi için bkz. [Müşteri ön ödemeleri](customer-prepayments.md).

Ayrıca, nakil tanımlarını hareket nakil türleriyle, **Hareket nakil tanımları** sayfasında ilişkilendirebilirsiniz. Deftere nakil tanımları müşteri hareketlerinin, nakil profilleri yerine genel muhasebe defterine nakledilmesini denetler. Daha fazla bilgi için bkz. [Deftere nakil tanımları](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Bir nakil profili oluşturmak
Seçili nakil profilini kullanan hareketlerin nakledilmesinde kullanılan genel muhasebe hesaplarını belirtin. Bir hesap kodu ve mümkün olduğu durumlarda seçili nakil profili için bir hesap veya grup numarası seçin. Deftere nakil işleminde, en uygun hesap kodu, hesap numarası veya grup veya numara birleşimini aşağıdaki öncelik sırasına göre aranarak her hareket için en uygun nakil profili bulunur.

| Hesap kodu alan değeri | Hesap/Grup numarası alan değeri                | Arama önceliği |
|--------------------------|-------------------------------------------------|-----------------|
| Tablo                    | Özel müşteri hesabı                       | 1               |
| Grup                    | Müşteriye atanmış olan müşteri grubu | 2               |
| Tümü                      | Boşluk                                           | 3               |

Tüm müşteri hareketlerinin aynı deftere nakil profili içermesini istiyorsanız, **Hesap kodu** alanında **Tümü** değerini içeren yalnızca bir nakil profili ayarlayın. Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin.

<table>
<thead>
<tr>
<th>Alan</th>
<th>Tanım</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Deftere nakil profili</strong></td>
<td>Nakil profili için bir kod girin. Örneğin ulusal para birimini içeren müşteri bakiyeleri için bir hesap elde etmek üzere iki nakil profili, yabancı para birimini içeren müşteri bakiyeleri için başka bir nakil profili oluşturabilirsiniz. Birini Ulusal, diğerini Yabancı olarak adlandırabilirsiniz.</td>
</tr>
<tr>
<td><strong>Açıklama</strong></td>
<td>Nakil profilinin açıklamasını girin. Bu yalnızca bu sayfada görüntülediğinizde, deftere nakil profilini daha iyi tanımlamak için kullanılır.</td>
</tr>
<tr>
<td><strong>Hesap kodu</strong></td>
<td>Nakil profilinin tek bir müşteri, bir müşteri grubu veya tüm müşteriler için mi geçerli olduğunu belirtin:
<ul>
<li><b>Tablo</b> – Nakil profili bir müşteri için geçerlidir. <b>Hesap/Grup numarası</b> alanında müşteri hesabını seçin.</li>
<li><b>Grup</b> – Nakil profili bir müşteri grubu geçerlidir. <b>Hesap/Grup numarası</b> alanında müşteri grubunu seçin.</li>
<li><b>Tümü</b> – Nakil profili tüm müşteriler için geçerlidir. <b>Hesap/Grup numarası</b> alanını boş bırakın.</li>
</ul>
</td>
</tr>
<tr>
<td><strong>Hesap/Grup numarası</strong></td>
<td><b>Hesap kodu</b> alanında <b>Tablo</b> seçiliyse, nakil profiliyle ilişkilendirilmiş müşterinin hesap numarasını seçin. Eğer <b>Grup</b> seçiliyse, müşteri grubunu seçin. <b>Tümü</b> seçiliyse bu alanı boş bırakın.</td>
</tr>
<tr>
<td><strong>Özet hesap</strong></td>
<td>Nakil profiliyle ilişkilendirilmiş müşteriler için Alacak hesapları ticari hesabı olarak kullanılacak temel hesabı seçin. Bu hesap, <b>Müşteri bakiyesi</b> deftere nakil türüne ait hesaptır.</td>
</tr>
<tr>
<td><strong>Ödemeler için likidite hesabı</strong></td>
<td>Nakit akışı tahminleri için kullanılacak <strong>Likidite genel muhasebe hesabını</strong> seçin. Bu alan yalnızca nakit akışı tahminleri etkinleştirilmişse görünür.</td>
</tr>
<tr>
<td><strong>Satış vergisi ön ödemeleri</strong></td>
<td><p>Avans olarak alınmış ödemeler için satış vergisinin hesabını seçin.</p>
<p><strong>Not:</strong> Bir ödeme bir ön ödeme olarak işaretlendiğinde kullanılacak nakil profilini belirtmek için <b>Alacak hesapları parametreleri</b> sayfasını kullanın.</p>
</td>
</tr>
<tr>
<td><strong>İskonto hesabı borçları</strong></td>
<td>İskonto borçları genel muhasebe hesabını seçin.</td>
</tr>
<tr>
<td><strong>Tahsilat mektubu sırası</strong></td>
<td>Tahsilat mektubu sırasının, nakil profilinin atandığı müşteriler için kullanılacak tanımlayıcısını seçin.</td>
</tr>
<tr>
<td><strong>Vade farkı kodu</strong></td>
<td>Nakil profilinin atandığı müşteriler için faizin hesaplanmasında kullanılacak faiz kodunu seçin.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Deftere nakil örnekleri

Aşağıdaki tabloda örnek ana hesapları ve açıklamaları olan varsayılan deftere nakil türleri örnekleri gösterilmiştir. **Borç/Alacak** sütunu, hareketin genel olarak Borç veya Alacak olduğunu ya da bazı durumlarda deftere nakledilebileceği anlamına gelir. **Temizleme hesabı** sütunu, deftere nakil türünün bir temizleme hesabı olduğunu belirtir. Bu, sonraki bir hareket deftere nakledildiğinde, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanacağını gösterir. 

| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak | Kliring hesabı | Açıklama |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Müşteri bakiyesi | 130100 | Alacak Hesapları Ticari | Varlık | İkisi birden | Hayır | **Özet hesabı** alanında hesabı belirtin.|
| Yok | 110110 | Banka hesabı | Varlık | İkisi birden | Hayır | Ana hesabı, **Ödemeler için likidite hesabı** alanına belirtin. Bu hesap deftere nakil için kullanılmaz. Yalnızca nakit akışı tahmini için kullanılır. |
| Satış vergisi ön ödemeleri | 202900 | Satış vergisi temizleme | Pasif | İkisi birden | Evet | Avans olarak alınmış ödemeler için satış vergisinin hesabını seçin. |
| İskonto hesabı borçları | 250600 | Ertelenen Gelir ve İndirimler | Pasif | İkisi birden | Evet | İskontolar borçları genel muhasebe hesabını seçin.|     

### <a name="table-restrictions"></a>Tablo kısıtlamaları

Seçili nakil profilini içeren hareketler için hareketlerin otomatik olarak kapatılması, faiz hesaplanması ve tahsilat mektuplarının verilip verilmeyeceğini belirtin. Ayrıca, seçili nakil profilini içeren hareketler kapatıldığında kullanılan hesabı seçin seçebilirsiniz.

Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin:

| Alan                 | Açıklama                                           |
|-----------------------|-------------------------------------------------------|
| Kapatma        | Bu nakil profilini içeren hareketlerin otomatik kapatılmasını etkinleştirmek için bu geçiş tuşunu seçin. Bu geçiş tuşu temizlenirse, hareketleri, **Açık hareketleri kapat** sayfasını ya da **Müşteri ödemelerini girme** sayfasını kullanarak elden kapatmanız gerekir. |
| İlgi Alanı          | Bu profili kullanan müşteri hesapları için bekleyen bakiyelerdeki vade farkı hesaplanacaksa bu geçiş tuşunu seçin. Bu geçiş tuşu temizlenirse, bu müşteriler için vade farkı hesaplanmaz.                                           |
| Tahsilat mektubu | Bu profili kullanan müşteri hesapları için tahsilat mektupları oluşturulacaksa, bu geçiş tuşunu seçin. Bu geçiş tuşu temizlenirse, bu müşteriler için tahsilat mektupları oluşturulmaz.                                                 |
| Kapat             | Bu nakil profilini içeren hareketler kapatılırken değiştirmek istediğiniz nakil profilini seçin. Bir hareket tamamen kapatıldığında kapanmış kabul edilir.             |



Daha fazla bilgi için bkz. [Müşteri ödeme genel bakışı](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

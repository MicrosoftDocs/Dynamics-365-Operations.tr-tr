---
title: Teslimat alternatifleri
description: Satış siparişi alanlar, Teslimat alternatif sayfasını, alternatif sipariş karşılama seçeneklerini bulmak için kullanabilirler.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 48cc8974cc8a8769b3d05f47f82166164e877ae5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210100"
---
# <a name="delivery-alternatives"></a>Teslimat alternatifleri

[!include [banner](../includes/banner.md)]

Satış siparişi alanlar, **Teslimat alternatifleri** sayfasını, alternatif sipariş karşılama seçeneklerini bulmak için kullanabilirler.

**Teslimat alternatifleri** sayfasının düzeni, tüm alternatif seçenekler hakkında genel bir görünüm verir. Ayrıca sipariş alanların, geçerli şirketin karşılama fırsatlarının ötesine bakmalarına izin verir. Şimdi hem şirketlerarası fırsatlar hem de harici satıcılardan fırsatları görebilirler. Seçenekleri teslimat tarihine göre dizerek, satış siparişi alanlar teslimat alternatiflerinin akıllı bir listesini görebilirler. Ek olarak, parametreler önerilen teslimatları daha iyi yönetmelerine yardımcı olur. Taşıma süresi teslimat tarihini etkileyebileceğinden, satış siparişi alanlar, taşıyıcının sunduğu çeşitli taşıma seçeneklerini keşfedebilirler. Her bir öneri için ayrıntılı bilgi sunulduğundan, sipariş alanlar **Teslimat alternatifleri** sayfasından doğrudan bilinçli kararlar verebilirler.

## <a name="open-the-delivery-alternatives-page"></a>Teslimat alternatifleri sayfasını aç
**Teslimat alternatifleri** sayfasını satış siparişi satırından açabilirsiniz.

1.  **Ürün ve tedarik** &gt; **Teslimat alternatifleri** üzerine tıklayın.
2.  **Satır ayrıntıları** &gt; **Teslimat** &gt; **Teslimat alternatifleri** üzerine tıklayın.

**Teslimat alternatifleri** sayfasını, **Satış siparişi işleme ve sorgu** çalışma alanını da açarak ve sonra **Siparişler ve favoriler** &gt; **Gecikmeli sipariş satırları** &gt; **Teslimat alternatifleri** üzerine tıklayarak açabilirsiniz **Not:** **Teslimat alternatifleri** sayfasını, yalnızca aşağıdaki koşullar yerine getiriliyorsa açabilirsiniz:

-   Tüm zorunlu satış satır bilgileri girilmiştir.
-   **Teslimat tarih denetimi** alanı, **Yok**'tan başka bir değere ayarlanmıştır.

## <a name="delivery-date-control-methods"></a>Teslimat tarihi kontrol yöntemleri
Teslimat tarihi denetim yöntemi, sistemin teslimat tarihlerini nasıl oluşturduğunu, teslimat alternatiflerinin nasıl hesaplandığını ve hangi bilginin gösterildiğini belirler. Teslimat veri denetiminin takvimleri dikkate aldığını unutmayın. Bu nedenle, aşağıdaki takvimler önerilen giriş tarihini etkileyebilir: Ambar takvimi, Taşıma takvimi, Satıcı takvimi ve Müşteri takvimi. Aşağıdaki tablo teslimat tarihi denetimi için her bir yöntemi açıklar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Yöntem</strong></td>
<td><strong>Açıklama</strong></td>
</tr>
<tr class="even">
<td><strong>Hiçbiri</strong></td>
<td><ul>
<li>Satış satırları için teslimat alternatifleri desteklenmez. Bu seçenek teslimat veri denetimini devre dışı bırakır.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Satış sağlama süresi</strong></td>
<td><ul>
<li>Teslimat alternatifleri önceden tanımlanmış satış sağlama süresinde hesaplanır. Taşıma günleri, teslimat şekline dayanarak hesaplanır.</li>
<li>Teslimat alternatifleri, eldeki stoka sahip ambarları ve arz/talep siparişlerini içerir.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>KM</strong></td>
<td><ul>
<li>Teslimat alternatifleri, karşılanabilir miktar (KM) mantığına göre hesaplanır. Geçerli kullanılabilirlik ve beklenen gelecek kullanılabilirlik dikkate alınır. Taşıma günleri, teslimat şekline dayanarak hesaplanır.</li>
<li>Teslimat alternatifleri, eldeki stoka sahip ambarları ve arz/talep siparişlerini içerir.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>KM + Çıkış marjı</strong></td>
<td><ul>
<li>Teslimat alternatifleri KM yönteminde olduğu gibi hesaplanır ancak çıkış marjı hesaplamaya dahil edilir.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>TEM</strong></td>
<td><ul>
<li>Teslimat alternatifleri, teslim edilebilir miktar (TEM) mantığına göre hesaplanır. MRP açılımı kullanılabilirliği belirlemek üzere kullanılır. En azından TEM mahsup işlemi teslimat tarihlerini satış sağlama süresine unutmayın. Taşıma günleri, teslimat şekline dayanarak hesaplanır.</li>
<li>Teslimat alternatifleri aşağıdaki ambarlar için önerileri içerir:
<ul>
<li>Geçerli ambar</li>
<li>Varsayılan ambar</li>
<li>Elde stok bulunduran tüm ambarlar</li>
<li>Tedarik emirleri olan tüm ambarlar</li>
<li>Etkin ürün reçetesi (BOM) sürümlerine sahip tüm ambarlar</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Teslimat alternatifleri hakkında bilgi görüntüle
Bu bölüm, **Teslimat alternatifleri** sayfasının her sekmesinde bulunan teslimat alternatifleri hakkında bilgileri açıklamaktadır.

### <a name="products"></a>Ürünler

Bu sekme, geçerli satış satırının ürün ve ayrıntılarının bir özetini gösterir.

### <a name="delivery-alternatives"></a>Teslimat alternatifleri

Bu sekme, giriş verisine göre sıralanan bir teslimat alternatiflerinin listesini gösterir. Listenin yukarısında, önerilerin hangi seçeneklere dayanacağını seçebilirsiniz. Ayrıca taşıma gününü belirleyen teslimat şeklini de seçebilirsiniz. Aşağıdaki seçenekler bulunur:

-   **Diğer ürün çeşitlerini dahil et** - Bu seçenek, ürün çeşitlerine sahip ürünler için kullanılabilir. Ürünün diğer çeşitlerinin teslimat alternatiflerini dahil eder. Bu seçenek TEM için kullanılamaz.
-   **Kısmi miktar dahil et** - Varsayılan olarak, yalnızca satış satırının tüm miktarını karşılayan öneriler dahil edilir. Bu seçeneği işaretleyerek, satış siparişini kısmi olarak karşılayan önerileri dahil edin. Müşteri daha erken bir teslimat tarihi talep ediyor ve kısmi teslimatı kabul ediyorsa, bu seçenek yararlıdır.
-   **Sonraki tarihleri dahil et** - Varsayılan olarak, yalnızca satış satırındaki tarihlerden daha iyi (erken) olan öneriler gösterilir. Sonraki tarihleri dahil etmek için bu seçeneği belirleyin. Bu seçenek, tarihten başka parametrelerin önceliği olduğunda yararlı olabilir. Örneğin, belirli bir satıcı veya ambar tercih edilebilir.
-   **Teslimat şekli** - Taşıma süresi ve maliyetini en iyi duruma getirmek için tercih edilen teslimat şeklini seçin. Önerilen teslimat alternatifleri üzerindeki etkisi hemen görünür. Bu nedenle, bu alternatifleri karşılaştırmak kolaydır.
-   **Tedariki dahil et** - Tedarik seçildiğinde, önerilen teslimat alternatifleri hem harici satıcıları ve hem de kuruluştaki diğer şirketleri (şirketlerarası) içerir. **Tedariki dahil et** seçeneği KM ve KM + çıkış marjı için desteklenir. Ürün için varsayılan satınalma satıcısından tüm tedarik seçenekleri ve ürün için tüm onaylanan satıcılar dahil edilir.
-   Harici satıcılar için, hesaplama satınalma sağlama süresine dayanır.
-   Hesaplama, sirketlerarası için tedarikçi şirketten nelerin kullanılabilir olduğunu, tedarikçi şirketin teslimat tarihi denetimine dayanarak dikkate alır.
-   **Teslimat türü** (Tedarik için ilgili)
    -   **Stok** - Ürünler tedarikçi ambardan, satış hattındaki tesise/ambara sevk edilir. Daha sonra bu ambardan müşteriye sevk edilir.
    -   **Doğrudan teslim** - Ürünler doğrudan tedarikçi ambardan müşteriye sevk edilir.

### <a name="availability-information"></a>Kullanılabilirlikle ilgili bilgiler

Bu sekme üzerindeki bilgi, seçilen teslimat alternatif satırıyla ilişkilidir. Satış satırındaki teslimat tarihi denetimine bağlı olarak aşağıdaki bilgiler gösterilir:

-   **Satış sağlama süresi**
    -   **Bugün kullanılabilir** - Eldeki fiziksel, fiziksel rezerve ve kullanılabilir fiziksel stoku göster.
    -   **Parametreler** - Stok birimi ve satış sağlama sürelerini göster.

-   **KM ve KM + çıkış marjı**
    -   **Bugün kullanılabilir** - Eldeki fiziksel, fiziksel rezerve ve kullanılabilir fiziksel stoku göster.
    -   **Parametreler** - Stok birimi ve satış sağlama sürelerini göster.
    -   **Gelecekteki kullanılabilirlik** - **Teslimat alternatifleri** altında seçili tesis ve ambar için mevcut ve gelecek kullanılabilirliğin görsel bir temsilini göster. Ürünün gelecekteki bulunabilirliği hakkında daha ayrıntılı bilgi görmek için grafik sütunlarına tıklayabilirsiniz. Kaydırıcı, KM zaman dilimi içerisinde ilgili arz ve talep siparişlerinin listesini gösterir.

-   **TEM**
    -   **Bugün kullanılabilir** - Eldeki fiziksel, fiziksel rezerve ve kullanılabilir fiziksel stoku göster.
    -   **Parametreler** - Stok birimi ve satış sağlama sürelerini göster.
    -   **Açılım** - Seçilen teslimat alternatifi için bir tedarik açılımı göster. Açılımda gösterilen alanları ve stok boyutlarını değiştirmek için **Kurulum**'u kullanabilirsiniz.

### <a name="impact-of-selected-alternative"></a>Seçilen alternatifin etkisi

Bu sekme, seçili teslimat alternatifinin etkisini vurgular. **Tamam** üzerine tıklarsanız, satış satırı SEÇİLİ sütunlarındaki vurgulanan değerler ile güncelleştirilir. Seçilen teslimat alternatifindeki miktar, satış satırındaki miktardan az ise, bir teslimat planının oluşturulacağını ve sipariş satırının iki satıra ayrılacağını unutmayın: bir satır seçilen miktar için ve bir satır kalan miktar için. Ticari satırı da planlı satırlar ile eşleşecek ve böylece fiyatlandırmayı etkileyecek şekilde güncelleştirebilirsiniz.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Sipariş taahhüdü](delivery-dates-available-promise-calculations.md)





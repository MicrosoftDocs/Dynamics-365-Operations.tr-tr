---
title: Gelişmiş filtreleme ve sorgu söz dizimi
description: Bu makalede, Gelişmiş filtreleme/sıralama iletişim kutusu ve Filtre bölmesindeki eşleşmeler işleci ya da ızgara sütun başlığı filtreleri için filtreleme ve sorgu seçenekleri açıklanmaktadır.
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89175763357f4309c4eb7874d0068586c5d9e726
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123963"
---
# <a name="advanced-filtering-and-query-syntax"></a>Gelişmiş filtreleme ve sorgu sözdizimi

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu makalede, Gelişmiş filtreleme/sıralama iletişim kutusunu veya Filtre bölmesindeki **eşleşmeler** işlecini ya da ızgara sütun başlığı filtrelerini kullanırken yararlanabileceğiniz filtreleme ve sorgu seçenekleri açıklanmaktadır.

## <a name="advanced-query-syntax"></a>Gelişmiş sorgu söz dizimi

<table>
<thead>
<tr>
<th>Sözdizimi</th>
<th>Karakter açıklaması</th>
<th>Tanım</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>değer</em></td>
<td>Girilen değere eşit</td>
<td>Bulmak istediğiniz değeri yazın.</td>
<td><strong>Smith</strong>, &quot;Smith&quot; değerini bulur.</td>
</tr>
<tr>
<td>!<em>değer</em> (ünlem işareti)</td>
<td>Girilen değere eşit değildir</td>
<td>Ünlem işareti ve dışlamak için bir değer yazın.</td>
<td><strong>!Smith</strong>, &quot;Smith&quot; haricindeki tüm değerleri bulur.</td>
</tr>
<tr>
<td><em>değerinden</em>..<em>değerine</em> (çift nokta)</td>
<td>Çift nokta ile ayrılan iki değer arasında</td>
<td>Başlangıç değerini girin, ardından çift nokta girin ve bitiş değerini girin.</td>
<td><strong>1..10</strong>, 1 ile 10 arasındaki tüm değerleri bulur. Ancak bir dize alanında <strong>A..C</strong>, &quot;A&quot; ve &quot;B&quot; ile başlayan tüm değerleri ve &quot;C&quot; ile tam olarak eşdeğer olan tüm değerleri bulur. Örneğin, bu sorgu &quot;Ca&quot;'yı bulmayacaktır. &quot;A<em>&quot; tipinden &quot;C</em>&quot; tipine tüm değerleri bulmak için <strong>A..D</strong> yazın.</td>
</tr>
<tr>
<td>..<em>değer</em> (çift nokta)</td>
<td>Girilen değerden az veya bu değere eşit</td>
<td>Çift noktayı ve ardından değeri girin.</td>
<td><strong>..1000</strong>, &quot;100&quot;, &quot;999,95&quot; ve &quot;1000&quot; gibi, 1000'e eşit veya ondan az tüm sayıları bulacaktır.</td>
</tr>
<tr>
<td><em>değer</em>.. (çift nokta)</td>
<td>Girilen değerden büyük veya bu değere eşit</td>
<td>Değeri ve ardından çift noktayı girin.</td>
<td><strong>1000..</strong> &quot;1.000&quot;, &quot;1.000,01&quot; ve &quot;1.000.000&quot; gibi, 1000'e eşit veya ondan büyük tüm sayıları bulacaktır.</td>
</tr>
<tr>
<td>&gt;<em>değer</em> (büyüktür işareti)</td>
<td>Girilen değerden büyüktür</td>
<td>Bir büyüktür işareti (<strong>&gt;</strong>) ve ardından değeri girin.</td>
<td><strong>&gt;1000</strong> &quot;1000,01&quot;, &quot;20.000&quot; ve &quot;1.000.000&quot; gibi 1000'den büyük sayıları bulacaktır.</td>
</tr>
<tr>
<td>&lt;<em>değer</em> (küçüktür işareti)</td>
<td>Girilen değerden küçüktür</td>
<td>Küçüktür işaretini (<strong>&lt;</strong>) ve ardından değeri girin.</td>
<td><strong>&lt;1000</strong>, &quot;999,99&quot;, &quot;1&quot; ve &quot;-200&quot; gibi 1000'den küçük sayıları bulacaktır.</td>
</tr>
<tr>
<td><em>değer</em>* (yıldız)</td>
<td>Girilen değerden başlar</td>
<td>Başlangıç değerini ve ardından yıldız yazın (<strong>*</strong>).</td>
<td><strong>S*</strong> &quot;Stockholm&quot;, &quot;Sydney&quot; ve &quot;San Francisco&quot; gibi &quot;S&quot; ile başlayan dizeleri bulacaktır.</td>
</tr>
<tr>
<td>*<em>değer</em> (yıldız)</td>
<td>Girilen değerle biten</td>
<td>Bir yıldız girin ve ardından bitiş değerini girin.</td>
<td><strong>*doğu</strong>, &quot;Kuzeydoğu&quot; ve &quot;Güneydoğu&quot; gibi &quot;doğu&quot; ile biten dizeleri bulacaktır.</td>
</tr>
<tr>
<td>*<em>değer</em>* (yıldız)</td>
<td>Girilen değeri içeren</td>
<td>Bir yıldız girin, ardından değeri girin ve daha sonra bir yıldız daha girin.</td>
<td><strong>*th*</strong>, &quot;Northeast&quot; ve &quot;Southeast&quot; gibi &quot;th&quot; içeren dizeleri bulacaktır.</td>
</tr>
<tr>
<td>? (soru işareti)</td>
<td>Bir veya birden fazla bilinmeyen karaktere sahip</td>
<td>Değerdeki bilinmeyen karakterlerin yerine soru işareti girin.</td>
<td><strong>Sm?th</strong> &quot;Smith&quot; ve &quot;Smyth&quot; değerlerini bulacaktır.</td>
</tr>
<tr>
<td><em>değer</em>,<em>değer</em> (virgül)</td>
<td>Virgülle ayrılmış değerlerle eşleşen</td>
<td>Tüm ölçütlerinizi girin ve virgülle ayırın.</td>
<td><strong>A, D, F, G</strong> tam olarak &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ve &quot;G&quot; değerlerini bulacaktır. <strong>10, 20, 30, 100</strong> tam olarak &quot;10, 20, 30, 100&quot; değerlerini bulacaktır.</td>
</tr>
<tr>
<td>"" (iki çift tırnak)</td>
<td>Boş bir değerle eşleştirme</td>
<td>Bu alandaki boş değerleri filtrelemek için art arda iki çift tırnak yazın.</td>
<td>İki ardışık çift tırnak (<strong>""</strong>), geçerli sütun için değer içermeyen satırları bulur.</td>
</tr>
<tr>
<td>(<span class="code">Finans ve operasyon sorgusu</span>) (Parantez içinde finans ve operasyon sorgusu)</td>
<td>Tanımlanan bir sorgulamayı eşleştirir.</td>
<td>Finans ve operasyon sorgu dilini kullanarak parantez içinde SQL deyimi olarak bir sorgu yazın.</td>
  <td><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong><br><br> 
       kök veri kaynağındaki bir alanda filtre koşulu için sözdizimi örneği ve farklı bir veri kaynağındaki bir alan (Tüm müşteriler sayfası için)</td>
</tr>
<tr>
<td>S</td>
<td>Bugünün tarihi</td>
<td><strong>T</strong> yazın.</td>
<td><strong>T</strong> bugünün tarihi ile eşleşir.</td>
</tr>
<tr>
<td>(methodName(parameters)) (Parantez içinde <strong>SysQueryRangeUtil</strong> yöntemi)</td>
<td><strong>SysQueryRangeUtil</strong> yöntemi parametreleri tarafından belirtilen değer veya değer aralığı ile eşleşen</td>
<td>Değeri veya değer aralığını belirten parametrelere sahip bir <strong>SysQueryRangeUtil</strong> yöntemi girin.</td>
<td>
<ol>
<li><strong>Alacak hesapları</strong> &gt; <strong>Faturalar</strong> &gt; <strong>Açık müşteri faturaları</strong> menü seçimlerine tıklayın.</li>
<li>Ctrl+Shift+F3 tuş bileşimine basarak <strong>Sorgu</strong> sayfasını açın.</li>
<li><strong>Aralık</strong> sekmesinde <strong>Ekle</strong>'ye tıklayın.</li>
<li><strong>Tablo</strong> alanında <strong>Açık müşteri hareketleri</strong>'ni seçin.</li>
<li><strong>Alan</strong> alanında <strong>Vade tarihi</strong>'ni seçin.</li>
<li><strong>Ölçüt</strong> alanına, <strong>(yearRange(-2,0))</strong> değerini girin.</li>
<li><strong>Tamam</strong> düğmesine tıklayın. Liste sayfası güncellenir ve girdiğiniz ölçüt ile eşleşen faturalar listelenir. Bu örnekte, önceki iki yıl içinde ödenecek faturalar listelenir.</li>
</ol>
<strong>SysQueryRangeUtil</strong> tarih yöntemleri hakkında ek ayrıntılar ve diğer örnekler için sonraki bölümde yer alan tabloya bakın.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>SysQueryRangeUtil yöntemleri kullanan gelişmiş tarih sorguları

<table>
<thead>
<tr>
<th>Yöntem</th>
<th>Açıklama</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr>
<td>Gün (_relativeDays=0)</td>
<td>Oturum tarihine göre bir tarih bulun. Pozitif değerler gelecekteki tarihleri, negatif değerler geçmişteki tarihleri gösterir.</td>
<td>
<ul>
<li><strong>Yarın</strong> – <strong>(Day(1))</strong> değerini girin.</li>
<li><strong>Bugün</strong> – <strong>(Day(0))</strong> değerini girin.</li>
<li><strong>Dün</strong> – <strong>(Day(-1))</strong> değerini girin.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Oturum tarihine göre tarih aralığı bulun. Pozitif değerler gelecekteki tarihleri, negatif değerler geçmişteki tarihleri gösterir.</td>
<td>
<ul>
<li><strong>Son 30 gün</strong> – <strong>(DayRange(-30,0))</strong> değerini girin.</li>
<li><strong>Önceki 30 gün ve sonraki 30 gün</strong> – <strong>(DayRange(-30,30))</strong> değerini girin.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Belirtilen göreli tarih sonrasındaki tüm tarihleri bulun.</td>
<td>
<ul>
<li><strong>Bugünden itibaren 30 günden fazla</strong> – <strong>(GreaterThanDate(30))</strong> değerini girin.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Geçerli saatten sonraki tüm tarih/saat girişlerini bulun.</td>
<td>
<ul>
<li><strong>Gelecekteki tüm tarih/saatler</strong> – <strong>(GreaterThanUtcNow())</strong> değerini girin.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Belirtilen göreli tarih öncesindeki tüm tarihleri bulun.</td>
<td>
<ul>
<li><strong>Bugünden itibaren yedi günden az</strong> – <strong>(LessThanDate(7))</strong> değerini girin.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Geçerli saatten önceki tüm tarih/saat girişlerini bulun.</td>
<td>
<ul>
<li><strong>Tüm geçmiş tarih/saatler</strong> – <strong>(LessThanUtcNow())</strong> değerini girin.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Geçerli aya göreli aylara dayalı olarak bir tarih aralığını bulun.</td>
<td>
<ul>
<li><strong>Önceki iki ay</strong> – <strong>(MonthRange(-2,0))</strong> değerini girin.</li>
<li><strong>Sonraki üç ay</strong> – <strong>(MonthRange(0,3))</strong> değerini girin.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Geçerli yıla göreli yıllara dayalı olarak bir tarih aralığını bulun.</td>
<td>
<ul>
<li><strong>Gelecek yıl</strong> – <strong>(YearRange(0, 1))</strong> değerini girin.</li>
<li><strong>Önceki yıl</strong> – <strong>(YearRange(-1,0))</strong> değerini girin.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: "Gelişmiş filtreleme ve sorgu sözdizimi"
description: "Bu makalede, Gelişmiş filtreleme/sıralama iletişim kutusundaki &quot;eşleşmeler&quot; işlecini kullanırken kullanılabilecek filtreleme ve sorgu seçenekleri açıklanmaktadır."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5ee7a04572e350a7c08d0418bade6d332aa920c6
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-filtering-and-query-syntax"></a>Gelişmiş filtreleme ve sorgu sözdizimi

Bu makalede, Gelişmiş filtreleme/sıralama iletişim kutusundaki "eşleşmeler" işlecini kullanırken kullanılabilecek filtreleme ve sorgu seçenekleri açıklanmaktadır.

<a name="advanced-query-syntax"></a>Gelişmiş sorgu sözdizimi
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Sözdizimi</th>
<th>Karakter açıklaması</th>
<th>Açıklama</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>değer</em></td>
<td>Girilen değere eşit</td>
<td>Bulmak istediğiniz değeri yazın.</td>
<td><strong>Türk</strong> bulur &quot;Türk&quot;.</td>
</tr>
<tr class="even">
<td>! <em>değeri</em> (ünlem işareti)</td>
<td>Girilen değere eşit değildir</td>
<td>Ünlem işareti ve dışlamak için bir değer yazın.</td>
<td><strong>! Türk</strong> dışındaki tüm değerleri bulur &quot;Türk&quot;.</td>
</tr>
<tr class="odd">
<td><em>değerinden</em>..<em>değerine</em> (çift nokta)</td>
<td>Çift nokta ile ayrılan iki değer arasında</td>
<td>Başlangıç değerini girin, ardından çift nokta girin ve bitiş değerini girin.</td>
<td><strong>1..10</strong> 1 ile 10 arasındaki tüm değerleri bulur. Ancak, bir dize alanı içinde <strong>A.. C</strong> ile başlayan tüm değerleri bulur &quot;A&quot; ve &quot;B&quot;ve tam olarak eşit değerler &quot;C&quot;. Örneğin, bu sorgu bulamaz &quot;Ca&quot;. Tüm değerleri bulmak için &quot;A*&quot; ile &quot;C*&quot;, türü <strong>A.. D</strong>.</td>
</tr>
<tr class="even">
<td>..<em>değer</em> (çift nokta)</td>
<td>Girilen değerden az veya bu değere eşit</td>
<td>Çift noktayı ve ardından değeri girin.</td>
<td><strong>.. 1000</strong> 1000, küçük veya eşit olduğu gibi herhangi bir sayı bulan &quot;100&quot;, &quot;999.95&quot;, ve &quot;1.000&quot;.</td>
</tr>
<tr class="odd">
<td><em>değer</em>.. (çift nokta)</td>
<td>Girilen değerden büyük veya bu değere eşit</td>
<td>Değeri ve ardından çift noktayı girin.</td>
<td><strong>1000..</strong> Büyük veya eşit 1000 olduğu gibi herhangi bir sayı bulan &quot;1.000&quot;, &quot;1,000.01&quot;, ve &quot;1000000&quot;.</td>
</tr>
<tr class="even">
<td>&gt;<em>değer</em> (büyüktür işareti)</td>
<td>Girilen değerden büyüktür</td>
<td>Büyüktür işareti türü (<strong>&gt;</strong>) ve sonra değeri.</td>
<td><strong>&gt;1000</strong> 1000'den büyük olduğu gibi herhangi bir sayı bulan &quot;1000.01&quot;, &quot;20.000&quot;, ve &quot;1000000&quot;.</td>
</tr>
<tr class="odd">
<td>&lt;<em>değer</em> (küçüktür işareti)</td>
<td>Girilen değerden küçüktür</td>
<td>Küçüktür işareti yazın (<strong>&lt;</strong>) ve sonra değeri.</td>
<td><strong>&lt;1000</strong> 1000'den küçük, olduğu gibi herhangi bir sayı bulan &quot;999.99&quot;, &quot;1&quot;, ve &quot;-200&quot;.</td>
</tr>
<tr class="even">
<td><em>değer</em>* (yıldız)</td>
<td>Girilen değerden başlar</td>
<td>Başlangıç değeri ve bir yıldız işareti yazın (<strong>*</strong>).</td>
<td><strong>S *</strong> ile başlayan tüm dize bulur &quot;S&quot;, aþaðýdaki gibi &quot;Stockholm&quot;, &quot;Samsun&quot;, ve &quot;San Francisco&quot;.</td>
</tr>
<tr class="odd">
<td>*<em>value</em> (asterisk)</td>
<td>Girilen değerle biten</td>
<td>Bir yıldız girin ve ardından bitiş değerini girin.</td>
<td><strong>* Doğu</strong> bulduğu herhangi dize ile biten &quot;Doğu&quot;, aþaðýdaki gibi &quot;Kuzeydoğu&quot; ve &quot;Güneydoğu&quot;.</td>
</tr>
<tr class="even">
<td>*<em>değer</em>* (yıldız)</td>
<td>Girilen değeri içeren</td>
<td>Bir yıldız girin, ardından değeri girin ve daha sonra bir yıldız daha girin.</td>
<td><strong>*TH*</strong> içeren tüm dize bulur &quot;th&quot;, aþaðýdaki gibi &quot;Kuzeydoğu&quot; ve &quot;Güneydoğu&quot;.</td>
</tr>
<tr class="odd">
<td>? (soru işareti)</td>
<td>Bir veya birden fazla bilinmeyen karaktere sahip</td>
<td>Değerdeki bilinmeyen karakterlerin yerine soru işareti girin.</td>
<td><strong>Sm? th</strong> bulur &quot;Türk&quot; ve &quot;cemal&quot;.</td>
</tr>
<tr class="even">
<td><em>değer</em>,<em>değer</em> (virgül)</td>
<td>Virgülle ayrılmış değerlerle eşleşen</td>
<td>Tüm ölçütlerinizi girin ve virgülle ayırın.</td>
<td><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;. <strong>10, 20, 30, 100</strong> tam olarak bulur &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr class="odd">
<td>(<span class="code">SQL deyimi</span>) (parantez içindeki SQL deyimi)</td>
<td>Tanımlanan bir sorgulamayı eşleştirir.</td>
<td>Parantez içinde SQL deyimi olarak bir sorgulama yazın.</td>
<td><strong><span class="code">(veri kaynağı. AlanAdı! = &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>S</td>
<td>Bugünün tarihi</td>
<td><strong>T</strong> yazın.</td>
<td><strong>T</strong> bugünün tarihi ile eşleşir.</td>
</tr>
<tr class="odd">
<td>(methodName(parameters)) (Parantez içinde <strong>SysQueryRangeUtil</strong> yöntemi)</td>
<td><strong>SysQueryRangeUtil</strong> yöntemi parametreleri tarafından belirtilen değer veya değer aralığı ile eşleşen</td>
<td>Değeri veya değer aralığını belirten parametrelere sahip bir <strong>SysQueryRangeUtil</strong> yöntemi girin.</td>
<td><ol>
<li>' I <strong>Alacak hesapları</strong>&gt;<strong>faturaları</strong>&gt;<strong>açık müşteri faturaları</strong>.</li>
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
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Yöntem</th>
<th>Açıklama</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gün (_relativeDays=0)</td>
<td>Oturum tarihine göre bir tarih bulun. Pozitif değerler gelecekteki tarihleri, negatif değerler geçmişteki tarihleri gösterir.</td>
<td><ul>
<li><strong>Yarın</strong> – <strong>(Day(1))</strong> değerini girin.</li>
<li><strong>Bugün</strong> – <strong>(Day(0))</strong> değerini girin.</li>
<li><strong>Dün</strong> – <strong>(Day(-1))</strong> değerini girin.</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Oturum tarihine göre tarih aralığı bulun. Pozitif değerler gelecekteki tarihleri, negatif değerler geçmişteki tarihleri gösterir.</td>
<td><ul>
<li><strong>Son 30 gün</strong> – <strong>(DayRange(-30,0))</strong> değerini girin.</li>
<li><strong>Önceki 30 gün ve sonraki 30 gün</strong> – <strong>(DayRange(-30,30))</strong> değerini girin.</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Belirtilen göreli tarih sonrasındaki tüm tarihleri bulun.</td>
<td><ul>
<li><strong>Bugünden itibaren 30 günden fazla</strong> – <strong>(GreaterThanDate(30))</strong> değerini girin.</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>Geçerli saatten sonraki tüm tarih/saat girişlerini bulun.</td>
<td><ul>
<li><strong>Gelecekteki tüm tarih/saatler</strong> – <strong>(GreaterThanUtcNow())</strong> değerini girin.</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Belirtilen göreli tarih öncesindeki tüm tarihleri bulun.</td>
<td><ul>
<li><strong>Bugünden itibaren yedi günden az</strong> – <strong>(LessThanDate(7))</strong> değerini girin.</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>Geçerli saatten önceki tüm tarih/saat girişlerini bulun.</td>
<td><ul>
<li><strong>Tüm geçmiş tarih/saatler</strong> – <strong>(LessThanUtcNow())</strong> değerini girin.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Geçerli aya göreli aylara dayalı olarak bir tarih aralığını bulun.</td>
<td><ul>
<li><strong>Önceki iki ay</strong> – <strong>(MonthRange(-2,0))</strong> değerini girin.</li>
<li><strong>Sonraki üç ay</strong> – <strong>(MonthRange(0,3))</strong> değerini girin.</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Geçerli yıla göreli yıllara dayalı olarak bir tarih aralığını bulun.</td>
<td><ul>
<li><strong>Gelecek yıl</strong> – <strong>(YearRange(0, 1))</strong> değerini girin.</li>
<li><strong>Önceki yıl</strong> – <strong>(YearRange(-1,0))</strong> değerini girin.</li>
</ul></td>
</tr>
</tbody>
</table>





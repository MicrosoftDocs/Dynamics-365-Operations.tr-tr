---
title: Gelişmiş filtreleme ve sorgu sözdizimi
description: Bu konuda, Gelişmiş filtreleme/sıralama iletişim kutusu ve Filtre bölmesindeki eşleşmeler işleci ya da ızgara sütun başlığı filtreleri için filtreleme ve sorgu seçenekleri açıklanmaktadır.
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
ms.openlocfilehash: fdb55a9552759e5f2b670a4eeb4e5d6572ebfb77
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744111"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="60905-103">Gelişmiş filtreleme ve sorgu sözdizimi</span><span class="sxs-lookup"><span data-stu-id="60905-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60905-104">Bu konuda, Gelişmiş filtreleme/sıralama iletişim kutusunu veya Filtre bölmesindeki **eşleşmeler** işlecini ya da ızgara sütun başlığı filtrelerini kullanırken yararlanabileceğiniz filtreleme ve sorgu seçenekleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="60905-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="60905-105">Gelişmiş sorgu söz dizimi</span><span class="sxs-lookup"><span data-stu-id="60905-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="60905-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="60905-106">Syntax</span></span></th>
<th><span data-ttu-id="60905-107">Karakter açıklaması</span><span class="sxs-lookup"><span data-stu-id="60905-107">Character description</span></span></th>
<th><span data-ttu-id="60905-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60905-108">Description</span></span></th>
<th><span data-ttu-id="60905-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="60905-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="60905-110"><em>değer</em></span><span class="sxs-lookup"><span data-stu-id="60905-110"><em>value</em></span></span></td>
<td><span data-ttu-id="60905-111">Girilen değere eşit</span><span class="sxs-lookup"><span data-stu-id="60905-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="60905-112">Bulmak istediğiniz değeri yazın.</span><span class="sxs-lookup"><span data-stu-id="60905-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="60905-113"><strong>Smith</strong>, &quot;Smith&quot; değerini bulur.</span><span class="sxs-lookup"><span data-stu-id="60905-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-114">!<em>değer</em> (ünlem işareti)</span><span class="sxs-lookup"><span data-stu-id="60905-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="60905-115">Girilen değere eşit değildir</span><span class="sxs-lookup"><span data-stu-id="60905-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="60905-116">Ünlem işareti ve dışlamak için bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="60905-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="60905-117"><strong>!Smith</strong>, &quot;Smith&quot; haricindeki tüm değerleri bulur.</span><span class="sxs-lookup"><span data-stu-id="60905-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-118"><em>değerinden</em>..<em>değerine</em> (çift nokta)</span><span class="sxs-lookup"><span data-stu-id="60905-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="60905-119">Çift nokta ile ayrılan iki değer arasında</span><span class="sxs-lookup"><span data-stu-id="60905-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="60905-120">Başlangıç değerini girin, ardından çift nokta girin ve bitiş değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="60905-121"><strong>1..10</strong>, 1 ile 10 arasındaki tüm değerleri bulur.</span><span class="sxs-lookup"><span data-stu-id="60905-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="60905-122">Ancak bir dize alanında <strong>A..C</strong>, &quot;A&quot; ve &quot;B&quot; ile başlayan tüm değerleri ve &quot;C&quot; ile tam olarak eşdeğer olan tüm değerleri bulur.</span><span class="sxs-lookup"><span data-stu-id="60905-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="60905-123">Örneğin, bu sorgu &quot;Ca&quot;'yı bulmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="60905-124">&quot;A<em>&quot; tipinden &quot;C</em>&quot; tipine tüm değerleri bulmak için <strong>A..D</strong> yazın.</span><span class="sxs-lookup"><span data-stu-id="60905-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-125">..<em>değer</em> (çift nokta)</span><span class="sxs-lookup"><span data-stu-id="60905-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="60905-126">Girilen değerden az veya bu değere eşit</span><span class="sxs-lookup"><span data-stu-id="60905-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="60905-127">Çift noktayı ve ardından değeri girin.</span><span class="sxs-lookup"><span data-stu-id="60905-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="60905-128"><strong>..1000</strong>, &quot;100&quot;, &quot;999,95&quot; ve &quot;1000&quot; gibi, 1000'e eşit veya ondan az tüm sayıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-129"><em>değer</em>..</span><span class="sxs-lookup"><span data-stu-id="60905-129"><em>value</em>..</span></span> <span data-ttu-id="60905-130">(çift nokta)</span><span class="sxs-lookup"><span data-stu-id="60905-130">(double period)</span></span></td>
<td><span data-ttu-id="60905-131">Girilen değerden büyük veya bu değere eşit</span><span class="sxs-lookup"><span data-stu-id="60905-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="60905-132">Değeri ve ardından çift noktayı girin.</span><span class="sxs-lookup"><span data-stu-id="60905-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="60905-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="60905-133"><strong>1000..</strong></span></span> <span data-ttu-id="60905-134">&quot;1.000&quot;, &quot;1.000,01&quot; ve &quot;1.000.000&quot; gibi, 1000'e eşit veya ondan büyük tüm sayıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-135">&gt;<em>değer</em> (büyüktür işareti)</span><span class="sxs-lookup"><span data-stu-id="60905-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="60905-136">Girilen değerden büyüktür</span><span class="sxs-lookup"><span data-stu-id="60905-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="60905-137">Bir büyüktür işareti (<strong>&gt;</strong>) ve ardından değeri girin.</span><span class="sxs-lookup"><span data-stu-id="60905-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="60905-138"><strong>&gt;1000</strong> &quot;1000,01&quot;, &quot;20.000&quot; ve &quot;1.000.000&quot; gibi 1000'den büyük sayıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-139">&lt;<em>değer</em> (küçüktür işareti)</span><span class="sxs-lookup"><span data-stu-id="60905-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="60905-140">Girilen değerden küçüktür</span><span class="sxs-lookup"><span data-stu-id="60905-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="60905-141">Küçüktür işaretini (<strong>&lt;</strong>) ve ardından değeri girin.</span><span class="sxs-lookup"><span data-stu-id="60905-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="60905-142"><strong>&lt;1000</strong>, &quot;999,99&quot;, &quot;1&quot; ve &quot;-200&quot; gibi 1000'den küçük sayıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-143"><em>değer</em>\* (yıldız)</span><span class="sxs-lookup"><span data-stu-id="60905-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="60905-144">Girilen değerden başlar</span><span class="sxs-lookup"><span data-stu-id="60905-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="60905-145">Başlangıç değerini ve ardından yıldız yazın (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="60905-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="60905-146"><strong>S\*</strong> &quot;Stockholm&quot;, &quot;Sydney&quot; ve &quot;San Francisco&quot; gibi &quot;S&quot; ile başlayan dizeleri bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-147">\*<em>değer</em> (yıldız)</span><span class="sxs-lookup"><span data-stu-id="60905-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="60905-148">Girilen değerle biten</span><span class="sxs-lookup"><span data-stu-id="60905-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="60905-149">Bir yıldız girin ve ardından bitiş değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="60905-150"><strong>\*doğu</strong>, &quot;Kuzeydoğu&quot; ve &quot;Güneydoğu&quot; gibi &quot;doğu&quot; ile biten dizeleri bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-151">*<em>değer</em>* (yıldız)</span><span class="sxs-lookup"><span data-stu-id="60905-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="60905-152">Girilen değeri içeren</span><span class="sxs-lookup"><span data-stu-id="60905-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="60905-153">Bir yıldız girin, ardından değeri girin ve daha sonra bir yıldız daha girin.</span><span class="sxs-lookup"><span data-stu-id="60905-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="60905-154"><strong>*th*</strong>, &quot;Northeast&quot; ve &quot;Southeast&quot; gibi &quot;th&quot; içeren dizeleri bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-155">?</span><span class="sxs-lookup"><span data-stu-id="60905-155">?</span></span> <span data-ttu-id="60905-156">(soru işareti)</span><span class="sxs-lookup"><span data-stu-id="60905-156">(question mark)</span></span></td>
<td><span data-ttu-id="60905-157">Bir veya birden fazla bilinmeyen karaktere sahip</span><span class="sxs-lookup"><span data-stu-id="60905-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="60905-158">Değerdeki bilinmeyen karakterlerin yerine soru işareti girin.</span><span class="sxs-lookup"><span data-stu-id="60905-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="60905-159"><strong>Sm?th</strong> &quot;Smith&quot; ve &quot;Smyth&quot; değerlerini bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-160"><em>değer</em>,<em>değer</em> (virgül)</span><span class="sxs-lookup"><span data-stu-id="60905-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="60905-161">Virgülle ayrılmış değerlerle eşleşen</span><span class="sxs-lookup"><span data-stu-id="60905-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="60905-162">Tüm ölçütlerinizi girin ve virgülle ayırın.</span><span class="sxs-lookup"><span data-stu-id="60905-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="60905-163"><strong>A, D, F, G</strong> tam olarak &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ve &quot;G&quot; değerlerini bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="60905-164"><strong>10, 20, 30, 100</strong> tam olarak &quot;10, 20, 30, 100&quot; değerlerini bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="60905-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-165">"" (iki çift tırnak)</span><span class="sxs-lookup"><span data-stu-id="60905-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="60905-166">Boş bir değerle eşleştirme</span><span class="sxs-lookup"><span data-stu-id="60905-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="60905-167">Bu alandaki boş değerleri filtrelemek için art arda iki çift tırnak yazın.</span><span class="sxs-lookup"><span data-stu-id="60905-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="60905-168">İki ardışık çift tırnak (<strong>""</strong>), geçerli sütun için değer içermeyen satırları bulur.</span><span class="sxs-lookup"><span data-stu-id="60905-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-169">(<span class="code">Finance and Operations sorgu</span>) (parantez arasında Finance and Operations sorgusu)</span><span class="sxs-lookup"><span data-stu-id="60905-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="60905-170">Tanımlanan bir sorgulamayı eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="60905-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="60905-171">Finance and Operations sorgu dilini kullanarak parantez içinde SQL deyimi olarak bir sorgu yazın.</span><span class="sxs-lookup"><span data-stu-id="60905-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="60905-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="60905-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="60905-173">kök veri kaynağındaki bir alanda filtre koşulu için sözdizimi örneği ve farklı bir veri kaynağındaki bir alan (Tüm müşteriler sayfası için)</span><span class="sxs-lookup"><span data-stu-id="60905-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-174">S</span><span class="sxs-lookup"><span data-stu-id="60905-174">T</span></span></td>
<td><span data-ttu-id="60905-175">Bugünün tarihi</span><span class="sxs-lookup"><span data-stu-id="60905-175">Today's date</span></span></td>
<td><span data-ttu-id="60905-176"><strong>T</strong> yazın.</span><span class="sxs-lookup"><span data-stu-id="60905-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="60905-177"><strong>T</strong> bugünün tarihi ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="60905-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="60905-178">(methodName(parameters)) (Parantez içinde <strong>SysQueryRangeUtil</strong> yöntemi)</span><span class="sxs-lookup"><span data-stu-id="60905-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="60905-179"><strong>SysQueryRangeUtil</strong> yöntemi parametreleri tarafından belirtilen değer veya değer aralığı ile eşleşen</span><span class="sxs-lookup"><span data-stu-id="60905-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="60905-180">Değeri veya değer aralığını belirten parametrelere sahip bir <strong>SysQueryRangeUtil</strong> yöntemi girin.</span><span class="sxs-lookup"><span data-stu-id="60905-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="60905-181"><strong>Alacak hesapları</strong> &gt; <strong>Faturalar</strong> &gt; <strong>Açık müşteri faturaları</strong> menü seçimlerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60905-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="60905-182">Ctrl+Shift+F3 tuş bileşimine basarak <strong>Sorgu</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="60905-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="60905-183"><strong>Aralık</strong> sekmesinde <strong>Ekle</strong>'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60905-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="60905-184"><strong>Tablo</strong> alanında <strong>Açık müşteri hareketleri</strong>'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="60905-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="60905-185"><strong>Alan</strong> alanında <strong>Vade tarihi</strong>'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="60905-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="60905-186"><strong>Ölçüt</strong> alanına, <strong>(yearRange(-2,0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="60905-187"><strong>Tamam</strong> düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="60905-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="60905-188">Liste sayfası güncellenir ve girdiğiniz ölçüt ile eşleşen faturalar listelenir.</span><span class="sxs-lookup"><span data-stu-id="60905-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="60905-189">Bu örnekte, önceki iki yıl içinde ödenecek faturalar listelenir.</span><span class="sxs-lookup"><span data-stu-id="60905-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="60905-190"><strong>SysQueryRangeUtil</strong> tarih yöntemleri hakkında ek ayrıntılar ve diğer örnekler için sonraki bölümde yer alan tabloya bakın.</span><span class="sxs-lookup"><span data-stu-id="60905-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="60905-191">SysQueryRangeUtil yöntemleri kullanan gelişmiş tarih sorguları</span><span class="sxs-lookup"><span data-stu-id="60905-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="60905-192">Yöntem</span><span class="sxs-lookup"><span data-stu-id="60905-192">Method</span></span></th>
<th><span data-ttu-id="60905-193">Açıklama</span><span class="sxs-lookup"><span data-stu-id="60905-193">Description</span></span></th>
<th><span data-ttu-id="60905-194">Örnek</span><span class="sxs-lookup"><span data-stu-id="60905-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="60905-195">Gün (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="60905-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="60905-196">Oturum tarihine göre bir tarih bulun.</span><span class="sxs-lookup"><span data-stu-id="60905-196">Find a date relative to the session date.</span></span> <span data-ttu-id="60905-197">Pozitif değerler gelecekteki tarihleri, negatif değerler geçmişteki tarihleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="60905-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="60905-198"><strong>Yarın</strong> – <strong>(Day(1))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="60905-199"><strong>Bugün</strong> – <strong>(Day(0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="60905-200"><strong>Dün</strong> – <strong>(Day(-1))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="60905-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="60905-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="60905-202">Oturum tarihine göre tarih aralığı bulun.</span><span class="sxs-lookup"><span data-stu-id="60905-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="60905-203">Pozitif değerler gelecekteki tarihleri, negatif değerler geçmişteki tarihleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="60905-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="60905-204"><strong>Son 30 gün</strong> – <strong>(DayRange(-30,0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="60905-205"><strong>Önceki 30 gün ve sonraki 30 gün</strong> – <strong>(DayRange(-30,30))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="60905-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="60905-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="60905-207">Belirtilen göreli tarih sonrasındaki tüm tarihleri bulun.</span><span class="sxs-lookup"><span data-stu-id="60905-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="60905-208"><strong>Bugünden itibaren 30 günden fazla</strong> – <strong>(GreaterThanDate(30))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="60905-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="60905-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="60905-210">Geçerli saatten sonraki tüm tarih/saat girişlerini bulun.</span><span class="sxs-lookup"><span data-stu-id="60905-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="60905-211"><strong>Gelecekteki tüm tarih/saatler</strong> – <strong>(GreaterThanUtcNow())</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="60905-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="60905-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="60905-213">Belirtilen göreli tarih öncesindeki tüm tarihleri bulun.</span><span class="sxs-lookup"><span data-stu-id="60905-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="60905-214"><strong>Bugünden itibaren yedi günden az</strong> – <strong>(LessThanDate(7))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="60905-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="60905-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="60905-216">Geçerli saatten önceki tüm tarih/saat girişlerini bulun.</span><span class="sxs-lookup"><span data-stu-id="60905-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="60905-217"><strong>Tüm geçmiş tarih/saatler</strong> – <strong>(LessThanUtcNow())</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="60905-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="60905-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="60905-219">Geçerli aya göreli aylara dayalı olarak bir tarih aralığını bulun.</span><span class="sxs-lookup"><span data-stu-id="60905-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="60905-220"><strong>Önceki iki ay</strong> – <strong>(MonthRange(-2,0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="60905-221"><strong>Sonraki üç ay</strong> – <strong>(MonthRange(0,3))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="60905-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="60905-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="60905-223">Geçerli yıla göreli yıllara dayalı olarak bir tarih aralığını bulun.</span><span class="sxs-lookup"><span data-stu-id="60905-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="60905-224"><strong>Gelecek yıl</strong> – <strong>(YearRange(0, 1))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="60905-225"><strong>Önceki yıl</strong> – <strong>(YearRange(-1,0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="60905-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
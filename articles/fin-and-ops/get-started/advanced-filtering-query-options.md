---
title: "Gelişmiş filtreleme ve sorgu söz dizimi"
description: "Bu makalede, Gelişmiş filtreleme/sıralama iletişim kutusunu veya Filtre bölmesindeki **eşleşmeler** işlecini ya da ızgara sütun başlığı filtrelerini kullanırken yararlanabileceğiniz filtreleme ve sorgu seçenekleri açıklanmaktadır."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: edff2fba7e231ae52abf7828d55c1fe4841ccd7f
ms.openlocfilehash: 3e7127a9412dcf9324872c06fbf6cc3cf61bf063
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="e1dfa-103">Gelişmiş filtreleme ve sorgu sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e1dfa-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1dfa-104">Bu makalede, Gelişmiş filtreleme/sıralama iletişim kutusunu veya Filtre bölmesindeki **eşleşmeler** işlecini ya da ızgara sütun başlığı filtrelerini kullanırken yararlanabileceğiniz filtreleme ve sorgu seçenekleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span> 

<a name="advanced-query-syntax"></a><span data-ttu-id="e1dfa-105">Gelişmiş sorgu söz dizimi</span><span class="sxs-lookup"><span data-stu-id="e1dfa-105">Advanced query syntax</span></span>
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
<th><span data-ttu-id="e1dfa-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e1dfa-106">Syntax</span></span></th>
<th><span data-ttu-id="e1dfa-107">Karakter açıklaması</span><span class="sxs-lookup"><span data-stu-id="e1dfa-107">Character description</span></span></th>
<th><span data-ttu-id="e1dfa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1dfa-108">Description</span></span></th>
<th><span data-ttu-id="e1dfa-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="e1dfa-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1dfa-110"><em>değer</em></span><span class="sxs-lookup"><span data-stu-id="e1dfa-110"><em>value</em></span></span></td>
<td><span data-ttu-id="e1dfa-111">Girilen değere eşit</span><span class="sxs-lookup"><span data-stu-id="e1dfa-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-112">Bulmak istediğiniz değeri yazın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="e1dfa-113"><strong>Smith</strong>, &quot;Smith&quot; değerini bulur.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-114">!<em>değer</em> (ünlem işareti)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="e1dfa-115">Girilen değere eşit değildir</span><span class="sxs-lookup"><span data-stu-id="e1dfa-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-116">Ünlem işareti ve dışlamak için bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="e1dfa-117"><strong>!Smith</strong>, &quot;Smith&quot; haricindeki tüm değerleri bulur.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-118"><em>değerinden</em>..<em>değerine</em> (çift nokta)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="e1dfa-119">Çift nokta ile ayrılan iki değer arasında</span><span class="sxs-lookup"><span data-stu-id="e1dfa-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="e1dfa-120">Başlangıç değerini girin, ardından çift nokta girin ve bitiş değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="e1dfa-121"><strong>1..10</strong>, 1 ile 10 arasındaki tüm değerleri bulur.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="e1dfa-122">Ancak bir dize alanında <strong>A..C</strong>, &quot;A&quot; ve &quot;B&quot; ile başlayan tüm değerleri ve &quot;C&quot; ile tam olarak eşdeğer olan tüm değerleri bulur.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="e1dfa-123">Örneğin, bu sorgu &quot;Ca&quot;'yı bulmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-123">For example, this query won&#39;t find &quot;Ca&quot;.</span></span> <span data-ttu-id="e1dfa-124">&quot;A<em>&quot; tipinden &quot;C</em>&quot; tipine tüm değerleri bulmak için <strong>A..D</strong> yazın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-125">..<em>değer</em> (çift nokta)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="e1dfa-126">Girilen değerden az veya bu değere eşit</span><span class="sxs-lookup"><span data-stu-id="e1dfa-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-127">Çift noktayı ve ardından değeri girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="e1dfa-128"><strong>..1000</strong>, &quot;100&quot;, &quot;999,95&quot; ve &quot;1000&quot; gibi, 1000'e eşit veya ondan az tüm sayıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-129"><em>değer</em>..</span><span class="sxs-lookup"><span data-stu-id="e1dfa-129"><em>value</em>..</span></span> <span data-ttu-id="e1dfa-130">(çift nokta)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-130">(double period)</span></span></td>
<td><span data-ttu-id="e1dfa-131">Girilen değerden büyük veya bu değere eşit</span><span class="sxs-lookup"><span data-stu-id="e1dfa-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-132">Değeri ve ardından çift noktayı girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="e1dfa-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="e1dfa-133"><strong>1000..</strong></span></span> <span data-ttu-id="e1dfa-134">&quot;1.000&quot;, &quot;1.000,01&quot; ve &quot;1.000.000&quot; gibi, 1000'e eşit veya ondan büyük tüm sayıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-135">&gt;<em>değer</em> (büyüktür işareti)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="e1dfa-136">Girilen değerden büyüktür</span><span class="sxs-lookup"><span data-stu-id="e1dfa-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-137">Bir büyüktür işareti (<strong>&gt;</strong>) ve ardından değeri girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="e1dfa-138"><strong>&gt;1000</strong> &quot;1000,01&quot;, &quot;20.000&quot; ve &quot;1.000.000&quot; gibi 1000'den büyük sayıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-139">&lt;<em>değer</em> (küçüktür işareti)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="e1dfa-140">Girilen değerden küçüktür</span><span class="sxs-lookup"><span data-stu-id="e1dfa-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-141">Küçüktür işaretini (<strong>&lt;</strong>) ve ardından değeri girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="e1dfa-142"><strong>&lt;1000</strong>, &quot;999,99&quot;, &quot;1&quot; ve &quot;-200&quot; gibi 1000'den küçük sayıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-143"><em>değer</em>\* (yıldız)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="e1dfa-144">Girilen değerden başlar</span><span class="sxs-lookup"><span data-stu-id="e1dfa-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-145">Başlangıç değerini ve ardından yıldız yazın (<strong><em></strong>).</span><span class="sxs-lookup"><span data-stu-id="e1dfa-145">Type the starting value and then an asterisk (<strong><em></strong>).</span></span></td>
<td><span data-ttu-id="e1dfa-146"><strong>S</em></strong> &quot;Stockholm&quot;, &quot;Sydney&quot; ve &quot;San Francisco&quot; gibi &quot;S&quot; ile başlayan dizeleri bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-146"><strong>S</em></strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-147"><em><em>değer</em> (yıldız)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-147"><em><em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="e1dfa-148">Girilen değerle biten</span><span class="sxs-lookup"><span data-stu-id="e1dfa-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-149">Bir yıldız girin ve ardından bitiş değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="e1dfa-150"><strong></em>doğu</strong> &quot;Kuzeydoğu&quot; ve &quot;Güneydoğu&quot; gibi &quot;doğu&quot; ile biten dizeleri bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-150"><strong></em>east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-151"><em><em>değer</em></em> (yıldız)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-151"><em><em>value</em></em> (asterisk)</span></span></td>
<td><span data-ttu-id="e1dfa-152">Girilen değeri içeren</span><span class="sxs-lookup"><span data-stu-id="e1dfa-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="e1dfa-153">Bir yıldız girin, ardından değeri girin ve daha sonra bir yıldız daha girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="e1dfa-154"><strong><em>th</em></strong>, &quot;Northeast&quot; ve &quot;Southeast&quot; gibi &quot;th&quot; içeren dizeleri bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-154"><strong><em>th</em></strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-155">?</span><span class="sxs-lookup"><span data-stu-id="e1dfa-155">?</span></span> <span data-ttu-id="e1dfa-156">(soru işareti)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-156">(question mark)</span></span></td>
<td><span data-ttu-id="e1dfa-157">Bir veya birden fazla bilinmeyen karaktere sahip</span><span class="sxs-lookup"><span data-stu-id="e1dfa-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="e1dfa-158">Değerdeki bilinmeyen karakterlerin yerine soru işareti girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="e1dfa-159"><strong>Sm?th</strong> &quot;Smith&quot; ve &quot;Smyth&quot; değerlerini bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-160"><em>değer</em>,<em>değer</em> (virgül)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="e1dfa-161">Virgülle ayrılmış değerlerle eşleşen</span><span class="sxs-lookup"><span data-stu-id="e1dfa-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="e1dfa-162">Tüm ölçütlerinizi girin ve virgülle ayırın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="e1dfa-163"><strong>A, D, F, G</strong> tam olarak &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ve &quot;G&quot; değerlerini bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="e1dfa-164"><strong>10, 20, 30, 100</strong> tam olarak &quot;10, 20, 30, 100&quot; değerlerini bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-165">(<span class="code">SQL deyimi</span>) (parantez içindeki SQL deyimi)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="e1dfa-166">Tanımlanan bir sorgulamayı eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="e1dfa-167">Parantez içinde SQL deyimi olarak bir sorgulama yazın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="e1dfa-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="e1dfa-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-169">T</span><span class="sxs-lookup"><span data-stu-id="e1dfa-169">T</span></span></td>
<td><span data-ttu-id="e1dfa-170">Bugünün tarihi</span><span class="sxs-lookup"><span data-stu-id="e1dfa-170">Today&#39;s date</span></span></td>
<td><span data-ttu-id="e1dfa-171"><strong>T</strong> yazın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="e1dfa-172"><strong>T</strong> bugünün tarihi ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-172"><strong>T</strong> matches today&#39;s date.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-173">(methodName(parameters)) (Parantez içinde <strong>SysQueryRangeUtil</strong> yöntemi)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="e1dfa-174"><strong>SysQueryRangeUtil</strong> yöntemi parametreleri tarafından belirtilen değer veya değer aralığı ile eşleşen</span><span class="sxs-lookup"><span data-stu-id="e1dfa-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="e1dfa-175">Değeri veya değer aralığını belirten parametrelere sahip bir <strong>SysQueryRangeUtil</strong> yöntemi girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td><ol>
<li><span data-ttu-id="e1dfa-176"><strong>Alacak hesapları</strong> &gt; <strong>Faturalar</strong> &gt; <strong>Açık müşteri faturaları</strong> menü seçimlerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-177">Ctrl+Shift+F3 tuş bileşimine basarak <strong>Sorgu</strong> sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="e1dfa-178"><strong>Aralık</strong> sekmesinde <strong>Ekle</strong>'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-179"><strong>Tablo</strong> alanında <strong>Açık müşteri hareketleri</strong>'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-180"><strong>Alan</strong> alanında <strong>Vade tarihi</strong>'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-181"><strong>Ölçüt</strong> alanına, <strong>(yearRange(-2,0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-182"><strong>Tamam</strong> düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="e1dfa-183">Liste sayfası güncellenir ve girdiğiniz ölçüt ile eşleşen faturalar listelenir.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="e1dfa-184">Bu örnekte, önceki iki yıl içinde ödenecek faturalar listelenir.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="e1dfa-185"><strong>SysQueryRangeUtil</strong> tarih yöntemleri hakkında ek ayrıntılar ve diğer örnekler için sonraki bölümde yer alan tabloya bakın.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="e1dfa-186">SysQueryRangeUtil yöntemleri kullanan gelişmiş tarih sorguları</span><span class="sxs-lookup"><span data-stu-id="e1dfa-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1dfa-187">Yöntem</span><span class="sxs-lookup"><span data-stu-id="e1dfa-187">Method</span></span></th>
<th><span data-ttu-id="e1dfa-188">Açıklama</span><span class="sxs-lookup"><span data-stu-id="e1dfa-188">Description</span></span></th>
<th><span data-ttu-id="e1dfa-189">Örnek</span><span class="sxs-lookup"><span data-stu-id="e1dfa-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1dfa-190">Gün (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="e1dfa-191">Oturum tarihine göre bir tarih bulun.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-191">Find a date relative to the session date.</span></span> <span data-ttu-id="e1dfa-192">Pozitif değerler gelecekteki tarihleri, negatif değerler geçmişteki tarihleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dfa-193"><strong>Yarın</strong> – <strong>(Day(1))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-194"><strong>Bugün</strong> – <strong>(Day(0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-195"><strong>Dün</strong> – <strong>(Day(-1))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="e1dfa-197">Oturum tarihine göre tarih aralığı bulun.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="e1dfa-198">Pozitif değerler gelecekteki tarihleri, negatif değerler geçmişteki tarihleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dfa-199"><strong>Son 30 gün</strong> – <strong>(DayRange(-30,0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-200"><strong>Önceki 30 gün ve sonraki 30 gün</strong> – <strong>(DayRange(-30,30))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="e1dfa-202">Belirtilen göreli tarih sonrasındaki tüm tarihleri bulun.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-202">Find all dates after the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dfa-203"><strong>Bugünden itibaren 30 günden fazla</strong> – <strong>(GreaterThanDate(30))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="e1dfa-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="e1dfa-205">Geçerli saatten sonraki tüm tarih/saat girişlerini bulun.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-205">Find all date/time entries after the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dfa-206"><strong>Gelecekteki tüm tarih/saatler</strong> – <strong>(GreaterThanUtcNow())</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="e1dfa-208">Belirtilen göreli tarih öncesindeki tüm tarihleri bulun.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-208">Find all dates before the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dfa-209"><strong>Bugünden itibaren yedi günden az</strong> – <strong>(LessThanDate(7))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="e1dfa-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="e1dfa-211">Geçerli saatten önceki tüm tarih/saat girişlerini bulun.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-211">Find all date/time entries before the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dfa-212"><strong>Tüm geçmiş tarih/saatler</strong> – <strong>(LessThanUtcNow())</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1dfa-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="e1dfa-214">Geçerli aya göreli aylara dayalı olarak bir tarih aralığını bulun.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dfa-215"><strong>Önceki iki ay</strong> – <strong>(MonthRange(-2,0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-216"><strong>Sonraki üç ay</strong> – <strong>(MonthRange(0,3))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1dfa-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="e1dfa-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="e1dfa-218">Geçerli yıla göreli yıllara dayalı olarak bir tarih aralığını bulun.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td><ul>
<li><span data-ttu-id="e1dfa-219"><strong>Gelecek yıl</strong> – <strong>(YearRange(0, 1))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="e1dfa-220"><strong>Önceki yıl</strong> – <strong>(YearRange(-1,0))</strong> değerini girin.</span><span class="sxs-lookup"><span data-stu-id="e1dfa-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>







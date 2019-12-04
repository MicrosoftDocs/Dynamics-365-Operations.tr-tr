---
title: Ürün yapılandırma modellerindeki ifade kısıtlamaları ve tablo kısıtlamaları
description: Bu konuda ifade kısıtlamalarının ve tablo kısıtlamalarının kullanımı açıklanmaktadır. Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetler. Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91eb5f166633f5be0ad68c039d3e538e4060ea0b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815077"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="23fde-105">Ürün yapılandırma modellerindeki ifade kısıtlamaları ve tablo kısıtlamaları</span><span class="sxs-lookup"><span data-stu-id="23fde-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23fde-106">Bu konuda ifade kısıtlamalarının ve tablo kısıtlamalarının kullanımı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="23fde-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="23fde-107">Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetler.</span><span class="sxs-lookup"><span data-stu-id="23fde-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="23fde-108">Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23fde-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="23fde-109">Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="23fde-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="23fde-110">Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23fde-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="23fde-111">İfade kısıtlamaları nelerdir?</span><span class="sxs-lookup"><span data-stu-id="23fde-111">What are expression constraints?</span></span>
<span data-ttu-id="23fde-112">İfade kısıtlamaları, aritmetik ve Boole işleçlerini ve işlevlerini kullanan bir ifade tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="23fde-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="23fde-113">Bir ifade kısıtlaması, ürün yapılandırma modelinde belirli bir bileşen için yazılır.</span><span class="sxs-lookup"><span data-stu-id="23fde-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="23fde-114">Başka bir bileşen tarafından yeniden kullanılamaz veya bir başka bileşenle paylaşılamaz.</span><span class="sxs-lookup"><span data-stu-id="23fde-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="23fde-115">Ancak, bir bileşen için ifade kısıtlamaları, bileşenin alt bileşenlerinin özniteliklerini referans gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="23fde-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="23fde-116">Tablo kısıtlamaları nelerdir?</span><span class="sxs-lookup"><span data-stu-id="23fde-116">What are table constraints?</span></span>
<span data-ttu-id="23fde-117">Tablo kısıtlamaları, bir ürün yapılandırdığınızda öznitelikler için izin verilen değerlerin birleşimlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="23fde-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="23fde-118">Tablo kısıtlaması tanımları genel olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="23fde-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="23fde-119">Ürün yapılandırma modelinde bir bileşen için bir tablo kısıtlaması oluşturduğunuzda, tablo kısıtlaması tanımı seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="23fde-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="23fde-120">İzin verilen birleşimleri oluşturmak için belirli türdeki öznitelikleri bileşenlere eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="23fde-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="23fde-121">Her öznitelik türü belirli bir değere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="23fde-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="23fde-122">Bir tablo kısıtlaması örneği.</span><span class="sxs-lookup"><span data-stu-id="23fde-122">Example of a table constraint</span></span>

<span data-ttu-id="23fde-123">Bu örnek, hoparlör yapılandırmasını belirli bir kabin rengi ve ön cephesiyle nasıl sınırlandırabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="23fde-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="23fde-124">İlk tablo, yapılandırma için genelde kullanılabilir olan kabin rengini ve ön cepheyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="23fde-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="23fde-125">Değerler **Kabin rengi** ve **Izgara rengi** öznitelik türleri için tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="23fde-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="23fde-126">Öznitelik türü</span><span class="sxs-lookup"><span data-stu-id="23fde-126">Attribute type</span></span> | <span data-ttu-id="23fde-127">Değerler</span><span class="sxs-lookup"><span data-stu-id="23fde-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="23fde-128">Kabin rengi</span><span class="sxs-lookup"><span data-stu-id="23fde-128">Cabinet finish</span></span> | <span data-ttu-id="23fde-129">Siyah, Meşe, Pelesenk, Beyaz,</span><span class="sxs-lookup"><span data-stu-id="23fde-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="23fde-130">Izgara rengi</span><span class="sxs-lookup"><span data-stu-id="23fde-130">Front grill</span></span>    | <span data-ttu-id="23fde-131">Siyah, Metal, Beyaz</span><span class="sxs-lookup"><span data-stu-id="23fde-131">Black, Metal, White</span></span>         |

<span data-ttu-id="23fde-132">Sonraki tablo, **Renk ve kaplama** tablo kısıtlamasıyla tanımlanan birleşimlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="23fde-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="23fde-133">Bu tablo kısıtlamasını kullanarak bir hoparlörü meşe kaplamalı ve siyah ızgaralı, pelesenk kaplamalı ve beyaz ızgaralı ve benzeri şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23fde-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="23fde-134">Son</span><span class="sxs-lookup"><span data-stu-id="23fde-134">Finish</span></span>         | <span data-ttu-id="23fde-135">Izgara</span><span class="sxs-lookup"><span data-stu-id="23fde-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="23fde-136">Meşe</span><span class="sxs-lookup"><span data-stu-id="23fde-136">Oak</span></span>            | <span data-ttu-id="23fde-137">Siyah</span><span class="sxs-lookup"><span data-stu-id="23fde-137">Black</span></span>                       |
| <span data-ttu-id="23fde-138">Venge</span><span class="sxs-lookup"><span data-stu-id="23fde-138">Rosewood</span></span>       | <span data-ttu-id="23fde-139">Beyaz</span><span class="sxs-lookup"><span data-stu-id="23fde-139">White</span></span>                       |
| <span data-ttu-id="23fde-140">Beyaz</span><span class="sxs-lookup"><span data-stu-id="23fde-140">White</span></span>          | <span data-ttu-id="23fde-141">Siyah</span><span class="sxs-lookup"><span data-stu-id="23fde-141">Black</span></span>                       |
| <span data-ttu-id="23fde-142">Beyaz</span><span class="sxs-lookup"><span data-stu-id="23fde-142">White</span></span>          | <span data-ttu-id="23fde-143">Beyaz</span><span class="sxs-lookup"><span data-stu-id="23fde-143">White</span></span>                       |
| <span data-ttu-id="23fde-144">Siyah</span><span class="sxs-lookup"><span data-stu-id="23fde-144">Black</span></span>          | <span data-ttu-id="23fde-145">Siyah</span><span class="sxs-lookup"><span data-stu-id="23fde-145">Black</span></span>                       |
| <span data-ttu-id="23fde-146">Siyah</span><span class="sxs-lookup"><span data-stu-id="23fde-146">Black</span></span>          | <span data-ttu-id="23fde-147">Metal</span><span class="sxs-lookup"><span data-stu-id="23fde-147">Metal</span></span>                       | 

<span data-ttu-id="23fde-148">Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23fde-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="23fde-149">Daha fazla bilgi için, [Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları](system-defined-user-defined-table-constraints.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="23fde-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="23fde-150">Kısıtlamaları yazmak için hangi sözdizimi kullanılmalıdır?</span><span class="sxs-lookup"><span data-stu-id="23fde-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="23fde-151">Kısıtlamaları yazarken En İyi Duruma Getirme Modelleme Dili (OML) sözdizimini kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="23fde-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="23fde-152">Sistem, kısıtlamaları çözümlemek için Microsoft Solver Foundation kısıtlama çözücüsünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="23fde-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="23fde-153">Tablo kısıtlamaları veya ifade kısıtlamaları kullanmam gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="23fde-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="23fde-154">Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını ya da tablo kısıtlamalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23fde-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="23fde-155">İfade kısıtlaması tek bir ifade olduğunda bir matris olarak tablo kısıtlaması oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="23fde-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="23fde-156">Bir ürünü yapılandırdığınızda, ne tür bir kısıtlama kullanıldığının önemi yoktur.</span><span class="sxs-lookup"><span data-stu-id="23fde-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="23fde-157">Aşağıdaki örnekte iki yöntem arasındaki fark gösterilir.</span><span class="sxs-lookup"><span data-stu-id="23fde-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="23fde-158">Bir ürünü aşağıdaki kısıtlama ayarlarını kullanarak yapılandırdığınızda bu kombinasyonlara izin verilir:</span><span class="sxs-lookup"><span data-stu-id="23fde-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="23fde-159">Siyah renkte ve boyutu 30 veya 50 olan bir ürün</span><span class="sxs-lookup"><span data-stu-id="23fde-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="23fde-160">Kırmızı renkte ve boyutu 20 olan bir ürün</span><span class="sxs-lookup"><span data-stu-id="23fde-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="23fde-161">Tablo kısıtlaması ayarı</span><span class="sxs-lookup"><span data-stu-id="23fde-161">Table constraint setup</span></span>

| <span data-ttu-id="23fde-162">Renk</span><span class="sxs-lookup"><span data-stu-id="23fde-162">Color</span></span> | <span data-ttu-id="23fde-163">Ebat</span><span class="sxs-lookup"><span data-stu-id="23fde-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="23fde-164">Siyah</span><span class="sxs-lookup"><span data-stu-id="23fde-164">Black</span></span> | <span data-ttu-id="23fde-165">30</span><span class="sxs-lookup"><span data-stu-id="23fde-165">30</span></span>   |
| <span data-ttu-id="23fde-166">Siyah</span><span class="sxs-lookup"><span data-stu-id="23fde-166">Black</span></span> | <span data-ttu-id="23fde-167">50</span><span class="sxs-lookup"><span data-stu-id="23fde-167">50</span></span>   |
| <span data-ttu-id="23fde-168">Kırmızı</span><span class="sxs-lookup"><span data-stu-id="23fde-168">Red</span></span>   | <span data-ttu-id="23fde-169">20</span><span class="sxs-lookup"><span data-stu-id="23fde-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="23fde-170">İfade kısıtlaması ayarı</span><span class="sxs-lookup"><span data-stu-id="23fde-170">Expression constraint setup</span></span>

<span data-ttu-id="23fde-171">(Renk == "Siyah" & (boyut == "30" | boyut == "50")) | (renk == "Kırmızı" & boyut = "20")</span><span class="sxs-lookup"><span data-stu-id="23fde-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="23fde-172">İfade kısıtlamaları yazarken bir işleç ya da parantezli yazım kullanmam gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="23fde-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="23fde-173">Önek operatörleri ya da parantezli yazım kullanarak bir ifade kısıtlaması yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23fde-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="23fde-174">**Min**, **Mak** ve **Mutlak** işleçleri için parantezli yazım kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="23fde-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="23fde-175">Bu işleçler, çoğu programlama dilinde standart işleçler olarak dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="23fde-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="23fde-176">İfade kısıtlamaları yazarken hangi işleçleri ve parantezli yazımı kullanabilirim?</span><span class="sxs-lookup"><span data-stu-id="23fde-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="23fde-177">Aşağıdaki tablolarda, ürün yapılandırma modelinde bir bileşen için bir ifade kısıtlaması yazarken kullanabileceğiniz işleçler ve parantezli yazım listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="23fde-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="23fde-178">İlk tablodaki örnekler parantezli yazım ya da işleçler kullanılarak bir ifadenin nasıl yazılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23fde-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23fde-179">İşleç</span><span class="sxs-lookup"><span data-stu-id="23fde-179">Operator</span></span></th>
<th><span data-ttu-id="23fde-180">Açıklama</span><span class="sxs-lookup"><span data-stu-id="23fde-180">Description</span></span></th>
<th><span data-ttu-id="23fde-181">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="23fde-181">Syntax</span></span></th>
<th><span data-ttu-id="23fde-182">Örnekler</span><span class="sxs-lookup"><span data-stu-id="23fde-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23fde-183">Implies</span><span class="sxs-lookup"><span data-stu-id="23fde-183">Implies</span></span></td>
<td><span data-ttu-id="23fde-184">İlk koşul yanlış, ikinci koşul doğru ya da her ikisi de doğru ise bu doğrudur.</span><span class="sxs-lookup"><span data-stu-id="23fde-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="23fde-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="23fde-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="23fde-186"><strong>İşleç:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="23fde-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="23fde-187"><strong>Parantezli yazım:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="23fde-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23fde-188">Ve</span><span class="sxs-lookup"><span data-stu-id="23fde-188">And</span></span></td>
<td><span data-ttu-id="23fde-189">Koşulların tümü doğru ise bu doğrudur.</span><span class="sxs-lookup"><span data-stu-id="23fde-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="23fde-190">Koşulların sayısı 0 (sıfır) ise, <strong>Doğru</strong> değeri çıkar.</span><span class="sxs-lookup"><span data-stu-id="23fde-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="23fde-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="23fde-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="23fde-192"><strong>İşleç:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="23fde-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="23fde-193"><strong>Parantezli yazım:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="23fde-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23fde-194">Veya</span><span class="sxs-lookup"><span data-stu-id="23fde-194">Or</span></span></td>
<td><span data-ttu-id="23fde-195">Herhangi bir koşul doğru ise bu doğrudur.</span><span class="sxs-lookup"><span data-stu-id="23fde-195">This is true if any condition is true.</span></span> <span data-ttu-id="23fde-196">Koşulların sayısı 0 (sıfır) ise, <strong>Yanlış</strong> değeri çıkar.</span><span class="sxs-lookup"><span data-stu-id="23fde-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="23fde-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="23fde-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="23fde-198"><strong>İşleç:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="23fde-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="23fde-199"><strong>Parantezli yazım:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="23fde-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23fde-200">Artı</span><span class="sxs-lookup"><span data-stu-id="23fde-200">Plus</span></span></td>
<td><span data-ttu-id="23fde-201">Bu, koşullarını toplar.</span><span class="sxs-lookup"><span data-stu-id="23fde-201">This sums its conditions.</span></span> <span data-ttu-id="23fde-202">Koşulların sayısı 0 (sıfır) ise, <strong>0</strong> değeri çıkar.</span><span class="sxs-lookup"><span data-stu-id="23fde-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="23fde-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="23fde-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="23fde-204"><strong>İşleç:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="23fde-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="23fde-205"><strong>Parantezli yazım:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="23fde-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23fde-206">Eksi</span><span class="sxs-lookup"><span data-stu-id="23fde-206">Minus</span></span></td>
<td><span data-ttu-id="23fde-207">Bu, çıkarımı negatif hale getirir.</span><span class="sxs-lookup"><span data-stu-id="23fde-207">This negates its argument.</span></span> <span data-ttu-id="23fde-208">Tek bir koşula sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="23fde-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="23fde-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="23fde-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="23fde-210"><strong>İşleç:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="23fde-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="23fde-211"><strong>Parantezli yazım:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="23fde-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23fde-212">Abs</span><span class="sxs-lookup"><span data-stu-id="23fde-212">Abs</span></span></td>
<td><span data-ttu-id="23fde-213">Bu, koşulunun mutlak değerini alır.</span><span class="sxs-lookup"><span data-stu-id="23fde-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="23fde-214">Tek bir koşula sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="23fde-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="23fde-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="23fde-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="23fde-216"><strong>İşleç:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="23fde-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23fde-217">Zaman</span><span class="sxs-lookup"><span data-stu-id="23fde-217">Times</span></span></td>
<td><span data-ttu-id="23fde-218">Bu, koşullarının ürününü alır.</span><span class="sxs-lookup"><span data-stu-id="23fde-218">This takes the product of its conditions.</span></span> <span data-ttu-id="23fde-219">Koşulların sayısı 0 (sıfır) ise, <strong>1</strong> değeri çıkar.</span><span class="sxs-lookup"><span data-stu-id="23fde-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="23fde-220">Times[args], infix: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="23fde-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="23fde-221"><strong>İşleç:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="23fde-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="23fde-222"><strong>Parantezli yazım:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="23fde-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23fde-223">Güç</span><span class="sxs-lookup"><span data-stu-id="23fde-223">Power</span></span></td>
<td><span data-ttu-id="23fde-224">Vu, üslü değer alır.</span><span class="sxs-lookup"><span data-stu-id="23fde-224">This takes an exponential.</span></span> <span data-ttu-id="23fde-225">Kuvveti sağdan sola uygular.</span><span class="sxs-lookup"><span data-stu-id="23fde-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="23fde-226">(Diğer bir deyişle, sağa ilişkilendirilebilir.) Bu nedenle, <strong>Power[a, b, c]</strong>, <strong>Power[, Power[b, c]]</strong> ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="23fde-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="23fde-227"><strong>Power</strong>, üs yalnızca pozitif bir sabit sayı ise kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="23fde-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="23fde-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="23fde-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="23fde-229"><strong>İşleç:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="23fde-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="23fde-230"><strong>Parantezli yazım:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="23fde-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23fde-231">Maks</span><span class="sxs-lookup"><span data-stu-id="23fde-231">Max</span></span></td>
<td><span data-ttu-id="23fde-232">Bu, en büyük koşulu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23fde-232">This produces the largest condition.</span></span> <span data-ttu-id="23fde-233">Koşulların sayısı 0 (sıfır) ise, <strong>Sonsuzluk</strong> üretir.</span><span class="sxs-lookup"><span data-stu-id="23fde-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="23fde-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="23fde-234">Max[args]</span></span></td>
<td><span data-ttu-id="23fde-235"><strong>İşleç:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="23fde-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23fde-236">Minimum</span><span class="sxs-lookup"><span data-stu-id="23fde-236">Min</span></span></td>
<td><span data-ttu-id="23fde-237">Bu, en küçük koşulu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23fde-237">This produces the smallest condition.</span></span> <span data-ttu-id="23fde-238">Koşulların sayısı 0 (sıfır) ise, <strong>Sonsuzluk</strong> üretir.</span><span class="sxs-lookup"><span data-stu-id="23fde-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="23fde-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="23fde-239">Min[args]</span></span></td>
<td><span data-ttu-id="23fde-240"><strong>İşleç:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="23fde-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23fde-241">Not</span><span class="sxs-lookup"><span data-stu-id="23fde-241">Not</span></span></td>
<td><span data-ttu-id="23fde-242">Bu, koşulunun mantıksal tersini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23fde-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="23fde-243">Tek bir koşula sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="23fde-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="23fde-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="23fde-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="23fde-245"><strong>İşleç:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="23fde-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="23fde-246"><strong>Parantezli yazım:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="23fde-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="23fde-247">Sonraki tablodaki örnekler parantezli yazımın nasıl yazılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23fde-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="23fde-248">Parantezli yazım</span><span class="sxs-lookup"><span data-stu-id="23fde-248">Infix notation</span></span>   |                                          <span data-ttu-id="23fde-249">Açıklama</span><span class="sxs-lookup"><span data-stu-id="23fde-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="23fde-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="23fde-250">x + y + z</span></span>     |                                           <span data-ttu-id="23fde-251">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="23fde-251">Addition</span></span>                                            |
|    <span data-ttu-id="23fde-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="23fde-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="23fde-253">Çarpma</span><span class="sxs-lookup"><span data-stu-id="23fde-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="23fde-254">x - y</span><span class="sxs-lookup"><span data-stu-id="23fde-254">x - y</span></span>       | <span data-ttu-id="23fde-255">İkili çıkarma, negatife düşmüş bir ikinci varsa ikili toplama ile aynı şekilde çevrilir.</span><span class="sxs-lookup"><span data-stu-id="23fde-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="23fde-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="23fde-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="23fde-257">Sağa birleşimli üs</span><span class="sxs-lookup"><span data-stu-id="23fde-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="23fde-258">!x</span><span class="sxs-lookup"><span data-stu-id="23fde-258">!x</span></span>         |                                          <span data-ttu-id="23fde-259">Boole değil</span><span class="sxs-lookup"><span data-stu-id="23fde-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="23fde-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="23fde-260">x -: y</span></span>       |                                      <span data-ttu-id="23fde-261">Boole çıkarım</span><span class="sxs-lookup"><span data-stu-id="23fde-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="23fde-262">x</span><span class="sxs-lookup"><span data-stu-id="23fde-262">x</span></span>         |                                               <span data-ttu-id="23fde-263">y</span><span class="sxs-lookup"><span data-stu-id="23fde-263">y</span></span>                                               |
|     <span data-ttu-id="23fde-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="23fde-264">x & y & z</span></span>     |                                          <span data-ttu-id="23fde-265">Boole ve</span><span class="sxs-lookup"><span data-stu-id="23fde-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="23fde-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="23fde-266">x == y == z</span></span>    |                                           <span data-ttu-id="23fde-267">Denklik</span><span class="sxs-lookup"><span data-stu-id="23fde-267">Equality</span></span>                                            |
|    <span data-ttu-id="23fde-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="23fde-268">x != y != z</span></span>    |                                           <span data-ttu-id="23fde-269">Benzersiz</span><span class="sxs-lookup"><span data-stu-id="23fde-269">Distinct</span></span>                                            |
|  <span data-ttu-id="23fde-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="23fde-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="23fde-271">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="23fde-271">Less than</span></span>                                           |
|  <span data-ttu-id="23fde-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="23fde-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="23fde-273">Büyüktür</span><span class="sxs-lookup"><span data-stu-id="23fde-273">Greater than</span></span>                                          |
| <span data-ttu-id="23fde-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="23fde-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="23fde-275">Küçüktür veya eşittir</span><span class="sxs-lookup"><span data-stu-id="23fde-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="23fde-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="23fde-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="23fde-277">Büyüktür veya eşittir</span><span class="sxs-lookup"><span data-stu-id="23fde-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="23fde-278">(x)</span><span class="sxs-lookup"><span data-stu-id="23fde-278">(x)</span></span>        |                           <span data-ttu-id="23fde-279">Parantezler varsayılan önceliği geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="23fde-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="23fde-280">İfade kısıtlamalarım neden hatasız doğrulanmıyor?</span><span class="sxs-lookup"><span data-stu-id="23fde-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="23fde-281">Ayrılmış anahtar sözcükleri, öznitelikleri, bileşenleri veya ürün yapılandırma modelinde alt bileşenleri için çözücü ad olarak kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="23fde-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="23fde-282"> Kullanamayacağınız anahtar sözcüklerin bir listesi aşağıdadır:</span><span class="sxs-lookup"><span data-stu-id="23fde-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="23fde-283">Üst</span><span class="sxs-lookup"><span data-stu-id="23fde-283">Ceiling</span></span>
-   <span data-ttu-id="23fde-284">Öğe</span><span class="sxs-lookup"><span data-stu-id="23fde-284">Element</span></span>
-   <span data-ttu-id="23fde-285">Eşit</span><span class="sxs-lookup"><span data-stu-id="23fde-285">Equal</span></span>
-   <span data-ttu-id="23fde-286">Kat</span><span class="sxs-lookup"><span data-stu-id="23fde-286">Floor</span></span>
-   <span data-ttu-id="23fde-287">Eğer</span><span class="sxs-lookup"><span data-stu-id="23fde-287">If</span></span>
-   <span data-ttu-id="23fde-288">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="23fde-288">Less</span></span>
-   <span data-ttu-id="23fde-289">Büyüktür</span><span class="sxs-lookup"><span data-stu-id="23fde-289">Greater</span></span>
-   <span data-ttu-id="23fde-290">Gösterir</span><span class="sxs-lookup"><span data-stu-id="23fde-290">Implies</span></span>
-   <span data-ttu-id="23fde-291">Hata İletileri</span><span class="sxs-lookup"><span data-stu-id="23fde-291">Log</span></span>
-   <span data-ttu-id="23fde-292">Maks.</span><span class="sxs-lookup"><span data-stu-id="23fde-292">Max</span></span>
-   <span data-ttu-id="23fde-293">Min.</span><span class="sxs-lookup"><span data-stu-id="23fde-293">Min</span></span>
-   <span data-ttu-id="23fde-294">Eksi</span><span class="sxs-lookup"><span data-stu-id="23fde-294">Minus</span></span>
-   <span data-ttu-id="23fde-295">Artı</span><span class="sxs-lookup"><span data-stu-id="23fde-295">Plus</span></span>
-   <span data-ttu-id="23fde-296">Güç</span><span class="sxs-lookup"><span data-stu-id="23fde-296">Power</span></span>
-   <span data-ttu-id="23fde-297">Zamanlar</span><span class="sxs-lookup"><span data-stu-id="23fde-297">Times</span></span>
-   <span data-ttu-id="23fde-298">Aralık</span><span class="sxs-lookup"><span data-stu-id="23fde-298">Slot</span></span>
-   <span data-ttu-id="23fde-299">Model</span><span class="sxs-lookup"><span data-stu-id="23fde-299">Model</span></span>
-   <span data-ttu-id="23fde-300">Karar</span><span class="sxs-lookup"><span data-stu-id="23fde-300">Decision</span></span>
-   <span data-ttu-id="23fde-301">Hedef</span><span class="sxs-lookup"><span data-stu-id="23fde-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="23fde-302">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="23fde-302">Additional resources</span></span>
--------

[<span data-ttu-id="23fde-303">Bir ifade kısıtlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="23fde-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="23fde-304">Ürün yapılandırma modeline hesaplama ekleme</span><span class="sxs-lookup"><span data-stu-id="23fde-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)




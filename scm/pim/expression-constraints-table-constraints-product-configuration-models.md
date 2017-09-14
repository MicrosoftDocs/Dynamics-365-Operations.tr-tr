---
title: "Ürün yapılandırma modellerindeki ifade kısıtlamaları ve tablo kısıtlamaları"
description: "Bu konuda ifade kısıtlamalarının ve tablo kısıtlamalarının kullanımı açıklanmaktadır. Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetler. Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 66d5ec61c1d69ebc8a8fc10d0b9b2a4b174729ee
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="997ea-105">Ürün yapılandırma modellerindeki ifade kısıtlamaları ve tablo kısıtlamaları</span><span class="sxs-lookup"><span data-stu-id="997ea-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="997ea-106">Bu konuda ifade kısıtlamalarının ve tablo kısıtlamalarının kullanımı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="997ea-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="997ea-107">Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetler.</span><span class="sxs-lookup"><span data-stu-id="997ea-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="997ea-108">Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="997ea-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="997ea-109">Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="997ea-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="997ea-110">Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="997ea-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="997ea-111">İfade kısıtlamaları nelerdir?</span><span class="sxs-lookup"><span data-stu-id="997ea-111">What are expression constraints?</span></span>
<span data-ttu-id="997ea-112">İfade kısıtlamaları, aritmetik ve Boole işleçlerini ve işlevlerini kullanan bir ifade tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="997ea-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="997ea-113">Bir ifade kısıtlaması, ürün yapılandırma modelinde belirli bir bileşen için yazılır.</span><span class="sxs-lookup"><span data-stu-id="997ea-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="997ea-114">Başka bir bileşen tarafından yeniden kullanılamaz veya bir başka bileşenle paylaşılamaz.</span><span class="sxs-lookup"><span data-stu-id="997ea-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="997ea-115">Ancak, bir bileşen için ifade kısıtlamaları, bileşenin alt bileşenlerinin özniteliklerini referans gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="997ea-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="997ea-116">Tablo kısıtlamaları nelerdir?</span><span class="sxs-lookup"><span data-stu-id="997ea-116">What are table constraints?</span></span>
<span data-ttu-id="997ea-117">Tablo kısıtlamaları, bir ürün yapılandırdığınızda öznitelikler için izin verilen değerlerin birleşimlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="997ea-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="997ea-118">Tablo kısıtlaması tanımları genel olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="997ea-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="997ea-119">Ürün yapılandırma modelinde bir bileşen için bir tablo kısıtlaması oluşturduğunuzda, tablo kısıtlaması tanımı seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="997ea-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="997ea-120">İzin verilen birleşimleri oluşturmak için belirli türdeki öznitelikleri bileşenlere eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="997ea-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="997ea-121">Her öznitelik türü belirli bir değere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="997ea-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="997ea-122">Bir tablo kısıtlaması örneği.</span><span class="sxs-lookup"><span data-stu-id="997ea-122">Example of a table constraint</span></span>

<span data-ttu-id="997ea-123">Bu örnek, hoparlör yapılandırmasını belirli bir kabin rengi ve ön cephesiyle nasıl sınırlandırabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="997ea-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="997ea-124">İlk tablo, yapılandırma için genelde kullanılabilir olan kabin rengini ve ön cepheyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="997ea-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="997ea-125">Değerler **Kabin rengi** ve **Izgara rengi** öznitelik türleri için tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="997ea-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="997ea-126">Öznitelik türü</span><span class="sxs-lookup"><span data-stu-id="997ea-126">Attribute type</span></span> | <span data-ttu-id="997ea-127">Değerler</span><span class="sxs-lookup"><span data-stu-id="997ea-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="997ea-128">Kabin rengi</span><span class="sxs-lookup"><span data-stu-id="997ea-128">Cabinet finish</span></span> | <span data-ttu-id="997ea-129">Siyah, Meşe, Pelesenk, Beyaz,</span><span class="sxs-lookup"><span data-stu-id="997ea-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="997ea-130">Izgara rengi</span><span class="sxs-lookup"><span data-stu-id="997ea-130">Front grill</span></span>    | <span data-ttu-id="997ea-131">Siyah, Metal, Beyaz</span><span class="sxs-lookup"><span data-stu-id="997ea-131">Black, Metal, White</span></span>         |

<span data-ttu-id="997ea-132">Sonraki tablo, **Renk ve kaplama** tablo kısıtlamasıyla tanımlanan birleşimlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="997ea-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="997ea-133">Bu tablo kısıtlamasını kullanarak bir hoparlörü meşe kaplamalı ve siyah ızgaralı, pelesenk kaplamalı ve beyaz ızgaralı ve benzeri şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="997ea-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="997ea-134">Son</span><span class="sxs-lookup"><span data-stu-id="997ea-134">Finish</span></span>         | <span data-ttu-id="997ea-135">Izgara</span><span class="sxs-lookup"><span data-stu-id="997ea-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="997ea-136">Meşe</span><span class="sxs-lookup"><span data-stu-id="997ea-136">Oak</span></span>            | <span data-ttu-id="997ea-137">Siyah</span><span class="sxs-lookup"><span data-stu-id="997ea-137">Black</span></span>                       |
| <span data-ttu-id="997ea-138">Venge</span><span class="sxs-lookup"><span data-stu-id="997ea-138">Rosewood</span></span>       | <span data-ttu-id="997ea-139">Beyaz</span><span class="sxs-lookup"><span data-stu-id="997ea-139">White</span></span>                       |
| <span data-ttu-id="997ea-140">Beyaz</span><span class="sxs-lookup"><span data-stu-id="997ea-140">White</span></span>          | <span data-ttu-id="997ea-141">Siyah</span><span class="sxs-lookup"><span data-stu-id="997ea-141">Black</span></span>                       |
| <span data-ttu-id="997ea-142">Beyaz</span><span class="sxs-lookup"><span data-stu-id="997ea-142">White</span></span>          | <span data-ttu-id="997ea-143">Beyaz</span><span class="sxs-lookup"><span data-stu-id="997ea-143">White</span></span>                       |
| <span data-ttu-id="997ea-144">Siyah</span><span class="sxs-lookup"><span data-stu-id="997ea-144">Black</span></span>          | <span data-ttu-id="997ea-145">Siyah</span><span class="sxs-lookup"><span data-stu-id="997ea-145">Black</span></span>                       |
| <span data-ttu-id="997ea-146">Siyah</span><span class="sxs-lookup"><span data-stu-id="997ea-146">Black</span></span>          | <span data-ttu-id="997ea-147">Metal</span><span class="sxs-lookup"><span data-stu-id="997ea-147">Metal</span></span>                       | 

<span data-ttu-id="997ea-148">Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="997ea-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="997ea-149">Daha fazla bilgi için, [Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları](system-defined-user-defined-table-constraints.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="997ea-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="997ea-150">Kısıtlamaları yazmak için hangi sözdizimi kullanılmalıdır?</span><span class="sxs-lookup"><span data-stu-id="997ea-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="997ea-151">Kısıtlamaları yazarken En İyi Duruma Getirme Modelleme Dili (OML) sözdizimini kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="997ea-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="997ea-152">Sistem, kısıtlamaları çözümlemek için Microsoft Solver Foundation kısıtlama çözücüsünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="997ea-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="997ea-153">Tablo kısıtlamaları veya ifade kısıtlamaları kullanmam gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="997ea-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="997ea-154">Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını ya da tablo kısıtlamalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="997ea-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="997ea-155">İfade kısıtlaması tek bir ifade olduğunda bir matris olarak tablo kısıtlaması oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="997ea-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="997ea-156">Bir ürünü yapılandırdığınızda, ne tür bir kısıtlama kullanıldığının önemi yoktur.</span><span class="sxs-lookup"><span data-stu-id="997ea-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="997ea-157">Aşağıdaki örnekte iki yöntem arasındaki fark gösterilir.</span><span class="sxs-lookup"><span data-stu-id="997ea-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="997ea-158">Bir ürünü aşağıdaki kısıtlama ayarlarını kullanarak yapılandırdığınızda bu kombinasyonlara izin verilir:</span><span class="sxs-lookup"><span data-stu-id="997ea-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="997ea-159">Siyah renkte ve boyutu 30 veya 50 olan bir ürün</span><span class="sxs-lookup"><span data-stu-id="997ea-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="997ea-160">Kırmızı renkte ve boyutu 20 olan bir ürün</span><span class="sxs-lookup"><span data-stu-id="997ea-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="997ea-161">Tablo kısıtlaması ayarı</span><span class="sxs-lookup"><span data-stu-id="997ea-161">Table constraint setup</span></span>

| <span data-ttu-id="997ea-162">Renk</span><span class="sxs-lookup"><span data-stu-id="997ea-162">Color</span></span> | <span data-ttu-id="997ea-163">Ebat</span><span class="sxs-lookup"><span data-stu-id="997ea-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="997ea-164">Siyah</span><span class="sxs-lookup"><span data-stu-id="997ea-164">Black</span></span> | <span data-ttu-id="997ea-165">30</span><span class="sxs-lookup"><span data-stu-id="997ea-165">30</span></span>   |
| <span data-ttu-id="997ea-166">Siyah</span><span class="sxs-lookup"><span data-stu-id="997ea-166">Black</span></span> | <span data-ttu-id="997ea-167">50</span><span class="sxs-lookup"><span data-stu-id="997ea-167">50</span></span>   |
| <span data-ttu-id="997ea-168">Kırmızı</span><span class="sxs-lookup"><span data-stu-id="997ea-168">Red</span></span>   | <span data-ttu-id="997ea-169">20</span><span class="sxs-lookup"><span data-stu-id="997ea-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="997ea-170">İfade kısıtlaması ayarı</span><span class="sxs-lookup"><span data-stu-id="997ea-170">Expression constraint setup</span></span>

<span data-ttu-id="997ea-171">(Renk == "Siyah" & (boyut == "30" | boyut == "50")) | (renk == "Kırmızı" & boyut = "20")</span><span class="sxs-lookup"><span data-stu-id="997ea-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="997ea-172">İfade kısıtlamaları yazarken bir işleç ya da parantezli yazım kullanmam gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="997ea-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="997ea-173">Önek operatörleri ya da parantezli yazım kullanarak bir ifade kısıtlaması yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="997ea-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="997ea-174">**Min**, **Mak** ve **Mutlak** işleçleri için parantezli yazım kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="997ea-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="997ea-175">Bu işleçler, çoğu programlama dilinde standart işleçler olarak dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="997ea-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="997ea-176">İfade kısıtlamaları yazarken hangi işleçleri ve parantezli yazımı kullanabilirim?</span><span class="sxs-lookup"><span data-stu-id="997ea-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="997ea-177">Aşağıdaki tablolarda, ürün yapılandırma modelinde bir bileşen için bir ifade kısıtlaması yazarken kullanabileceğiniz işleçler ve parantezli yazım listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="997ea-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="997ea-178">İlk tablodaki örnekler parantezli yazım ya da işleçler kullanılarak bir ifadenin nasıl yazılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="997ea-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="997ea-179">İşleç</span><span class="sxs-lookup"><span data-stu-id="997ea-179">Operator</span></span></th>
<th><span data-ttu-id="997ea-180">Açıklama</span><span class="sxs-lookup"><span data-stu-id="997ea-180">Description</span></span></th>
<th><span data-ttu-id="997ea-181">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="997ea-181">Syntax</span></span></th>
<th><span data-ttu-id="997ea-182">Örnekler</span><span class="sxs-lookup"><span data-stu-id="997ea-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="997ea-183">Implies</span><span class="sxs-lookup"><span data-stu-id="997ea-183">Implies</span></span></td>
<td><span data-ttu-id="997ea-184">İlk koşul yanlış, ikinci koşul doğru ya da her ikisi de doğru ise bu doğrudur.</span><span class="sxs-lookup"><span data-stu-id="997ea-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="997ea-185">Implies[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="997ea-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="997ea-186"><strong>İşleç:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="997ea-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="997ea-187"><strong>Parantezli yazım:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="997ea-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997ea-188">Ve</span><span class="sxs-lookup"><span data-stu-id="997ea-188">And</span></span></td>
<td><span data-ttu-id="997ea-189">Koşulların tümü doğru ise bu doğrudur.</span><span class="sxs-lookup"><span data-stu-id="997ea-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="997ea-190">Koşulların sayısı 0 (sıfır) ise, <strong>Doğru</strong> değeri çıkar.</span><span class="sxs-lookup"><span data-stu-id="997ea-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="997ea-191">And[args], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="997ea-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="997ea-192"><strong>İşleç:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="997ea-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="997ea-193"><strong>Parantezli yazım:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="997ea-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997ea-194">Veya</span><span class="sxs-lookup"><span data-stu-id="997ea-194">Or</span></span></td>
<td><span data-ttu-id="997ea-195">Herhangi bir koşul doğru ise bu doğrudur.</span><span class="sxs-lookup"><span data-stu-id="997ea-195">This is true if any condition is true.</span></span> <span data-ttu-id="997ea-196">Koşulların sayısı 0 (sıfır) ise, <strong>Yanlış</strong> değeri çıkar.</span><span class="sxs-lookup"><span data-stu-id="997ea-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="997ea-197">Or[args], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="997ea-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="997ea-198"><strong>İşleç:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="997ea-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="997ea-199"><strong>Parantezli yazım:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="997ea-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997ea-200">Artı</span><span class="sxs-lookup"><span data-stu-id="997ea-200">Plus</span></span></td>
<td><span data-ttu-id="997ea-201">Bu, koşullarını toplar.</span><span class="sxs-lookup"><span data-stu-id="997ea-201">This sums its conditions.</span></span> <span data-ttu-id="997ea-202">Koşulların sayısı 0 (sıfır) ise, <strong>0</strong> değeri çıkar.</span><span class="sxs-lookup"><span data-stu-id="997ea-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="997ea-203">Plus[args], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="997ea-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="997ea-204"><strong>İşleç:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="997ea-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="997ea-205"><strong>Parantezli yazım:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="997ea-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997ea-206">Eksi</span><span class="sxs-lookup"><span data-stu-id="997ea-206">Minus</span></span></td>
<td><span data-ttu-id="997ea-207">Bu, çıkarımı negatif hale getirir.</span><span class="sxs-lookup"><span data-stu-id="997ea-207">This negates its argument.</span></span> <span data-ttu-id="997ea-208">Tek bir koşula sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="997ea-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="997ea-209">Minus[expr], infix: -expr</span><span class="sxs-lookup"><span data-stu-id="997ea-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="997ea-210"><strong>İşleç:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="997ea-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="997ea-211"><strong>Parantezli yazım:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="997ea-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997ea-212">Abs</span><span class="sxs-lookup"><span data-stu-id="997ea-212">Abs</span></span></td>
<td><span data-ttu-id="997ea-213">Bu, koşulunun mutlak değerini alır.</span><span class="sxs-lookup"><span data-stu-id="997ea-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="997ea-214">Tek bir koşula sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="997ea-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="997ea-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="997ea-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="997ea-216"><strong>İşleç:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="997ea-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997ea-217">Zaman</span><span class="sxs-lookup"><span data-stu-id="997ea-217">Times</span></span></td>
<td><span data-ttu-id="997ea-218">Bu, koşullarının ürününü alır.</span><span class="sxs-lookup"><span data-stu-id="997ea-218">This takes the product of its conditions.</span></span> <span data-ttu-id="997ea-219">Koşulların sayısı 0 (sıfır) ise, <strong>1</strong> değeri çıkar.</span><span class="sxs-lookup"><span data-stu-id="997ea-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="997ea-220">Times[args], infix: a * b * ... * z</span><span class="sxs-lookup"><span data-stu-id="997ea-220">Times[args], infix: a * b * ... * z</span></span></td>
<td><ul>
<li><span data-ttu-id="997ea-221"><strong>İşleç:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="997ea-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="997ea-222"><strong>Parantezli yazım:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="997ea-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997ea-223">Güç</span><span class="sxs-lookup"><span data-stu-id="997ea-223">Power</span></span></td>
<td><span data-ttu-id="997ea-224">Vu, üslü değer alır.</span><span class="sxs-lookup"><span data-stu-id="997ea-224">This takes an exponential.</span></span> <span data-ttu-id="997ea-225">Kuvveti sağdan sola uygular.</span><span class="sxs-lookup"><span data-stu-id="997ea-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="997ea-226">(Diğer bir deyişle, sağa ilişkilendirilebilir.) Bu nedenle, <strong>Power[a, b, c]</strong> <strong>Power[, Power[b, c]]</strong> ile eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="997ea-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="997ea-227"><strong>Power</strong>, üs yalnızca pozitif bir sabit sayı ise kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="997ea-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="997ea-228">Power[args], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="997ea-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="997ea-229"><strong>İşleç:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="997ea-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="997ea-230"><strong>Parantezli yazım:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="997ea-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997ea-231">Maks</span><span class="sxs-lookup"><span data-stu-id="997ea-231">Max</span></span></td>
<td><span data-ttu-id="997ea-232">Bu, en büyük koşulu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="997ea-232">This produces the largest condition.</span></span> <span data-ttu-id="997ea-233">Koşulların sayısı 0 (sıfır) ise, <strong>Sonsuzluk</strong> üretir.</span><span class="sxs-lookup"><span data-stu-id="997ea-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="997ea-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="997ea-234">Max[args]</span></span></td>
<td><span data-ttu-id="997ea-235"><strong>İşleç:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="997ea-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="997ea-236">Minimum</span><span class="sxs-lookup"><span data-stu-id="997ea-236">Min</span></span></td>
<td><span data-ttu-id="997ea-237">Bu, en küçük koşulu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="997ea-237">This produces the smallest condition.</span></span> <span data-ttu-id="997ea-238">Koşulların sayısı 0 (sıfır) ise, <strong>Sonsuzluk</strong> üretir.</span><span class="sxs-lookup"><span data-stu-id="997ea-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="997ea-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="997ea-239">Min[args]</span></span></td>
<td><span data-ttu-id="997ea-240"><strong>İşleç:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="997ea-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="997ea-241">Not</span><span class="sxs-lookup"><span data-stu-id="997ea-241">Not</span></span></td>
<td><span data-ttu-id="997ea-242">Bu, koşulunun mantıksal tersini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="997ea-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="997ea-243">Tek bir koşula sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="997ea-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="997ea-244">Not[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="997ea-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="997ea-245"><strong>İşleç:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="997ea-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="997ea-246"><strong>Parantezli yazım:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="997ea-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="997ea-247">Sonraki tablodaki örnekler parantezli yazımın nasıl yazılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="997ea-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="997ea-248">Parantezli yazım</span><span class="sxs-lookup"><span data-stu-id="997ea-248">Infix notation</span></span>    | <span data-ttu-id="997ea-249">Açıklama</span><span class="sxs-lookup"><span data-stu-id="997ea-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="997ea-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="997ea-250">x + y + z</span></span>         | <span data-ttu-id="997ea-251">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="997ea-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="997ea-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="997ea-252">x \* y \* z</span></span>       | <span data-ttu-id="997ea-253">Çarpma</span><span class="sxs-lookup"><span data-stu-id="997ea-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="997ea-254">x - y</span><span class="sxs-lookup"><span data-stu-id="997ea-254">x - y</span></span>             | <span data-ttu-id="997ea-255">İkili çıkarma, negatife düşmüş bir ikinci varsa ikili toplama ile aynı şekilde çevrilir.</span><span class="sxs-lookup"><span data-stu-id="997ea-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="997ea-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="997ea-256">x ^ y ^ z</span></span>         | <span data-ttu-id="997ea-257">Sağa birleşimli üs</span><span class="sxs-lookup"><span data-stu-id="997ea-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="997ea-258">!x</span><span class="sxs-lookup"><span data-stu-id="997ea-258">!x</span></span>                | <span data-ttu-id="997ea-259">Boole değil</span><span class="sxs-lookup"><span data-stu-id="997ea-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="997ea-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="997ea-260">x -: y</span></span>            | <span data-ttu-id="997ea-261">Boole çıkarım</span><span class="sxs-lookup"><span data-stu-id="997ea-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="997ea-262"> x </span><span class="sxs-lookup"><span data-stu-id="997ea-262">x</span></span> | <span data-ttu-id="997ea-263">y</span><span class="sxs-lookup"><span data-stu-id="997ea-263">y</span></span> | <span data-ttu-id="997ea-264">z</span><span class="sxs-lookup"><span data-stu-id="997ea-264">z</span></span>         | <span data-ttu-id="997ea-265">Boole ya da</span><span class="sxs-lookup"><span data-stu-id="997ea-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="997ea-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="997ea-266">x & y & z</span></span>         | <span data-ttu-id="997ea-267">Boole ve</span><span class="sxs-lookup"><span data-stu-id="997ea-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="997ea-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="997ea-268">x == y == z</span></span>       | <span data-ttu-id="997ea-269">Denklik</span><span class="sxs-lookup"><span data-stu-id="997ea-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="997ea-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="997ea-270">x != y != z</span></span>       | <span data-ttu-id="997ea-271">Benzersiz</span><span class="sxs-lookup"><span data-stu-id="997ea-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="997ea-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="997ea-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="997ea-273">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="997ea-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="997ea-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="997ea-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="997ea-275">Büyüktür</span><span class="sxs-lookup"><span data-stu-id="997ea-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="997ea-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="997ea-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="997ea-277">Küçüktür veya eşittir</span><span class="sxs-lookup"><span data-stu-id="997ea-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="997ea-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="997ea-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="997ea-279">Büyüktür veya eşittir</span><span class="sxs-lookup"><span data-stu-id="997ea-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="997ea-280">(x)</span><span class="sxs-lookup"><span data-stu-id="997ea-280">(x)</span></span>               | <span data-ttu-id="997ea-281">Parantezler varsayılan önceliği geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="997ea-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="997ea-282">İfade kısıtlamalarım neden hatasız doğrulanmıyor?</span><span class="sxs-lookup"><span data-stu-id="997ea-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="997ea-283">Ayrılmış anahtar sözcükleri, öznitelikleri, bileşenleri veya ürün yapılandırma modelinde alt bileşenleri için çözücü ad olarak kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="997ea-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="997ea-284">Kullanamayacağınız anahtar sözcüklerin bir listesi aşağıdadır:</span><span class="sxs-lookup"><span data-stu-id="997ea-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="997ea-285">Üst</span><span class="sxs-lookup"><span data-stu-id="997ea-285">Ceiling</span></span>
-   <span data-ttu-id="997ea-286">Öğe</span><span class="sxs-lookup"><span data-stu-id="997ea-286">Element</span></span>
-   <span data-ttu-id="997ea-287">Eşit</span><span class="sxs-lookup"><span data-stu-id="997ea-287">Equal</span></span>
-   <span data-ttu-id="997ea-288">Kat</span><span class="sxs-lookup"><span data-stu-id="997ea-288">Floor</span></span>
-   <span data-ttu-id="997ea-289">Eğer</span><span class="sxs-lookup"><span data-stu-id="997ea-289">If</span></span>
-   <span data-ttu-id="997ea-290">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="997ea-290">Less</span></span>
-   <span data-ttu-id="997ea-291">Büyüktür</span><span class="sxs-lookup"><span data-stu-id="997ea-291">Greater</span></span>
-   <span data-ttu-id="997ea-292">Gösterir</span><span class="sxs-lookup"><span data-stu-id="997ea-292">Implies</span></span>
-   <span data-ttu-id="997ea-293">Hata İletileri</span><span class="sxs-lookup"><span data-stu-id="997ea-293">Log</span></span>
-   <span data-ttu-id="997ea-294">Maks</span><span class="sxs-lookup"><span data-stu-id="997ea-294">Max</span></span>
-   <span data-ttu-id="997ea-295">Min.</span><span class="sxs-lookup"><span data-stu-id="997ea-295">Min</span></span>
-   <span data-ttu-id="997ea-296">Eksi</span><span class="sxs-lookup"><span data-stu-id="997ea-296">Minus</span></span>
-   <span data-ttu-id="997ea-297">Artı</span><span class="sxs-lookup"><span data-stu-id="997ea-297">Plus</span></span>
-   <span data-ttu-id="997ea-298">Güç</span><span class="sxs-lookup"><span data-stu-id="997ea-298">Power</span></span>
-   <span data-ttu-id="997ea-299">Zamanlar</span><span class="sxs-lookup"><span data-stu-id="997ea-299">Times</span></span>
-   <span data-ttu-id="997ea-300">Aralık</span><span class="sxs-lookup"><span data-stu-id="997ea-300">Slot</span></span>
-   <span data-ttu-id="997ea-301">Model</span><span class="sxs-lookup"><span data-stu-id="997ea-301">Model</span></span>
-   <span data-ttu-id="997ea-302">Karar</span><span class="sxs-lookup"><span data-stu-id="997ea-302">Decision</span></span>
-   <span data-ttu-id="997ea-303">Hedef</span><span class="sxs-lookup"><span data-stu-id="997ea-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="997ea-304">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="997ea-304">See also</span></span>
--------

<span data-ttu-id="997ea-305">[Bir deyim sınırlaması oluşturun (Görev kılavuzu)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span><span class="sxs-lookup"><span data-stu-id="997ea-305">[Create an expression constraint (Task guide)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span></span>

[<span data-ttu-id="997ea-306">Bir ürün yapılandırma modeline hesaplama ekleme (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="997ea-306">Add a calculation to a product configuration model (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/add-calculation-product-configuration-model)





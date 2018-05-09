---
title: Numara serileri
description: "Numara serileri, ana veri kayıtları ve tanımlayıcı gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 13b47d755a122199608ece386f4f764ee580b2ed
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="number-sequences"></a><span data-ttu-id="4daf2-103">Numara serileri</span><span class="sxs-lookup"><span data-stu-id="4daf2-103">Number sequences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4daf2-104">Numara serileri, ana veri kayıtları ve tanımlayıcı gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="4daf2-105">Tanımlayıcı gerektiren bir ana veri kaydı veya hareket kaydı, *referans* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="4daf2-106">Bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="4daf2-107">Numara sıralarını ayarlamak için **Kuruluş yönetimi**'ndeki sayfaları kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="4daf2-108">Modüle özgü ayarları gerekiyorsa, bu modül içindeki referans için numara serileri belirtmek için bir modüldeki parametreleri sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="4daf2-109">Örneğin, **Alacak hesapları** ve **Borç hesapları**'nda, belirli müşteriler veya satıcılar için özel numara serileri tahsis etmek için numara serisi grupları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="4daf2-110">Bir numara sırası ayarlarsanız, hangi kuruluşun bu numara serisini kullanacağını tanımlayan bir kapsam belirtmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="4daf2-111">Kapsam **Paylaşımlı**, **Şirket**, **Tüzel kişilik** veya **İşletim birimi** olabilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="4daf2-112">**Tüzel kişilik** ve **Şirket**, **Mali takvim dönemi** kapsamları ile daha özel numara serileri oluşturmak için birleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="4daf2-113">Numara sırası biçimleri segmentlerden oluşur.</span><span class="sxs-lookup"><span data-stu-id="4daf2-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="4daf2-114">**Paylaşımlı** dışında kapsamlara sahip seriler, kapsama karşılık gelen segmentler içerebilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="4daf2-115">Örneğin, **Tüzel kişilik** kapsamını içeren bir numara serisi, bir tüzel kişilik segmenti içerebilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="4daf2-116">Sayı dizisi biçiminde bir kapsam kesimi dahil ederek, numarasına bakarak belirli bir kaydın kapsamını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="4daf2-117">Segmentlere karşılık gelen kapsamların yanı sıra, numara sırası biçimleri **Sabit** ve **Alfasayısal parçaları** içerebilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="4daf2-118">**Sabit** bir segment bir dizi değişmez harf, sayı veya simge kümesi içerir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="4daf2-119">Bir **Alfasayısal** segment, bir sayının kullanıldığı her seferde artan bir harf veya sayı kümesi içerir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="4daf2-120">Artan sayıları göstermek için (\#) ve artan harfleri göstermek için (&) simgelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4daf2-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="4daf2-121">Örneğin, \#\#\#\#\#\_2017 biçimi, 00001\_2017, 00002\_2017 sırasını ve devamını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4daf2-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="4daf2-122">Numara serisi örnekleri</span><span class="sxs-lookup"><span data-stu-id="4daf2-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="4daf2-123">Aşağıdaki örnekler sıralı sayı biçimleri oluşturmak için segmentlerin nasıl kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="4daf2-124">Bu örnekler özellikle, kapsam segmentleri kullanmanın etkilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="4daf2-125">Gider raporu numaraları.</span><span class="sxs-lookup"><span data-stu-id="4daf2-125">Expense report numbers</span></span>

<span data-ttu-id="4daf2-126">Aşağıdaki örnekte, **CS** başlıklı bir tüzel kişilik için gider raporu numaraları ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="4daf2-127">**Alan:** Seyahat ve gider</span><span class="sxs-lookup"><span data-stu-id="4daf2-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="4daf2-128">**Referans:** Gider raporu numarası</span><span class="sxs-lookup"><span data-stu-id="4daf2-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="4daf2-129">**Kapsam:** Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="4daf2-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="4daf2-130">**Tüzel kişilik:** CS</span><span class="sxs-lookup"><span data-stu-id="4daf2-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="4daf2-131">Segmentler</span><span class="sxs-lookup"><span data-stu-id="4daf2-131">Segments</span></span>  | <span data-ttu-id="4daf2-132">Segment türü</span><span class="sxs-lookup"><span data-stu-id="4daf2-132">Segment type</span></span> | <span data-ttu-id="4daf2-133">Değer</span><span class="sxs-lookup"><span data-stu-id="4daf2-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="4daf2-134">Segment 1</span><span class="sxs-lookup"><span data-stu-id="4daf2-134">Segment 1</span></span> | <span data-ttu-id="4daf2-135">Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="4daf2-135">Legal entity</span></span> | <span data-ttu-id="4daf2-136">CS</span><span class="sxs-lookup"><span data-stu-id="4daf2-136">CS</span></span>        |
| <span data-ttu-id="4daf2-137">Segment 2</span><span class="sxs-lookup"><span data-stu-id="4daf2-137">Segment 2</span></span> | <span data-ttu-id="4daf2-138">Sabit</span><span class="sxs-lookup"><span data-stu-id="4daf2-138">Constant</span></span>     | <span data-ttu-id="4daf2-139">-GİDER-</span><span class="sxs-lookup"><span data-stu-id="4daf2-139">-EXPENSE-</span></span> |
| <span data-ttu-id="4daf2-140">Segment 3</span><span class="sxs-lookup"><span data-stu-id="4daf2-140">Segment 3</span></span> | <span data-ttu-id="4daf2-141">Alfasayısal</span><span class="sxs-lookup"><span data-stu-id="4daf2-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="4daf2-142">**Biçimlendirilmiş sayı örneği**: CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="4daf2-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="4daf2-143">Diğer tüzel kişilikler için benzer bir sayı dizisi biçimi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="4daf2-144">Örneğin, **RW** adlı bir tüzel kişilik için, yalnızca tüzel kişilik segmentinin değerini değiştirirseniz, biçimlendirilmiş sayı RW-GİDER-0039 olur.</span><span class="sxs-lookup"><span data-stu-id="4daf2-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="4daf2-145">Ayrıca, diğer tüzel kişilikler için de tam sayı dizisi biçimini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="4daf2-146">Örneğin, Exp-0001 gibi biçimlendirilmiş bir sayı oluşturmak için bir tüzel kişilik kapsam segmentini atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="4daf2-147">Satış sipariş numaraları</span><span class="sxs-lookup"><span data-stu-id="4daf2-147">Sales order numbers</span></span>

<span data-ttu-id="4daf2-148">Aşağıdaki örnekte, şirket kodu **CEU** için satış siparişi numaraları ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="4daf2-149">**Alan:** Satış</span><span class="sxs-lookup"><span data-stu-id="4daf2-149">**Area:** Sales</span></span> 
- <span data-ttu-id="4daf2-150">**Referans:** Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="4daf2-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="4daf2-151">**Kapsam:** Şirket</span><span class="sxs-lookup"><span data-stu-id="4daf2-151">**Scope:** Company</span></span> 
- <span data-ttu-id="4daf2-152">**Şirket:** CEU</span><span class="sxs-lookup"><span data-stu-id="4daf2-152">**Company:** CEU</span></span>

| <span data-ttu-id="4daf2-153">Segmentler</span><span class="sxs-lookup"><span data-stu-id="4daf2-153">Segments</span></span>  | <span data-ttu-id="4daf2-154">Segment türü</span><span class="sxs-lookup"><span data-stu-id="4daf2-154">Segment type</span></span> | <span data-ttu-id="4daf2-155">Değer</span><span class="sxs-lookup"><span data-stu-id="4daf2-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="4daf2-156">Segment 1</span><span class="sxs-lookup"><span data-stu-id="4daf2-156">Segment 1</span></span> | <span data-ttu-id="4daf2-157">Sabit</span><span class="sxs-lookup"><span data-stu-id="4daf2-157">Constant</span></span>     | <span data-ttu-id="4daf2-158">SS-</span><span class="sxs-lookup"><span data-stu-id="4daf2-158">SO-</span></span>      |
| <span data-ttu-id="4daf2-159">Segment 2</span><span class="sxs-lookup"><span data-stu-id="4daf2-159">Segment 2</span></span> | <span data-ttu-id="4daf2-160">Alfasayısal</span><span class="sxs-lookup"><span data-stu-id="4daf2-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="4daf2-161">**Biçimlendirilmiş sayı örneği**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="4daf2-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="4daf2-162">Kapsam segmenti biçime dahil edilmemiş bile olsa, her şirket kimliği için numaralandırma yeniden başlar.</span><span class="sxs-lookup"><span data-stu-id="4daf2-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="4daf2-163">Tüm şirket kimlikleri için aynı biçimi kullanırsanız, her şirkette aynı numaraları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="4daf2-164">Örneğin, satış siparişi numarası SO-0029, her şirkette kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="4daf2-165">Ayrıca, diğer şirket kimlikleri için de tam sayı dizisi biçimini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="4daf2-166">Satınalma talebi numaraları</span><span class="sxs-lookup"><span data-stu-id="4daf2-166">Purchase requisition numbers</span></span>

<span data-ttu-id="4daf2-167">Aşağıdaki örnekte, satınalma talebi sayıları kuruluş çapındadır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="4daf2-168">**Alan:** Satınalma</span><span class="sxs-lookup"><span data-stu-id="4daf2-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="4daf2-169">**Referans:** Satınalma talebi</span><span class="sxs-lookup"><span data-stu-id="4daf2-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="4daf2-170">**Kapsam:** Paylaşılan</span><span class="sxs-lookup"><span data-stu-id="4daf2-170">**Scope:** Shared</span></span>

| <span data-ttu-id="4daf2-171">Segmentler</span><span class="sxs-lookup"><span data-stu-id="4daf2-171">Segments</span></span>  | <span data-ttu-id="4daf2-172">Segment türü</span><span class="sxs-lookup"><span data-stu-id="4daf2-172">Segment type</span></span> | <span data-ttu-id="4daf2-173">Değer</span><span class="sxs-lookup"><span data-stu-id="4daf2-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="4daf2-174">Segment 1</span><span class="sxs-lookup"><span data-stu-id="4daf2-174">Segment 1</span></span> | <span data-ttu-id="4daf2-175">Sabit</span><span class="sxs-lookup"><span data-stu-id="4daf2-175">Constant</span></span>     | <span data-ttu-id="4daf2-176">Gereken</span><span class="sxs-lookup"><span data-stu-id="4daf2-176">Req</span></span>      |
| <span data-ttu-id="4daf2-177">Segment 2</span><span class="sxs-lookup"><span data-stu-id="4daf2-177">Segment 2</span></span> | <span data-ttu-id="4daf2-178">Alfasayısal</span><span class="sxs-lookup"><span data-stu-id="4daf2-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="4daf2-179">**Biçimlendirilmiş sayı örneği**: Req0052</span><span class="sxs-lookup"><span data-stu-id="4daf2-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="4daf2-180">Kapsam **Paylaşılan** olduğu için numara sırası biçimi tüm organizasyonda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="4daf2-181">Kuruluşun farklı bölümleri için farklı sayı sırası biçimleri ayarlayamazsınız. </span><span class="sxs-lookup"><span data-stu-id="4daf2-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="4daf2-182">Numara serilerinde performans ile ilgili hususlar</span><span class="sxs-lookup"><span data-stu-id="4daf2-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="4daf2-183">Numara serileri yapılandırmasını ayarlamadan önce sistem performansını nasıl etkileyebileceği hakkında aşağıdaki bilgileri göz önüne alın.</span><span class="sxs-lookup"><span data-stu-id="4daf2-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="4daf2-184">Sürekli ve sürekli olmayan numara serileri</span><span class="sxs-lookup"><span data-stu-id="4daf2-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="4daf2-185">Numara serileri sürekli veya sürekli olmayan şekillerde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="4daf2-186">Sürekli bir numara sırası hiçbir sayıyı atlamaz, ancak sayılar ardışık olarak kullanılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="4daf2-187">Sürekli olmayan numara serisinden numaraları sıralı olarak kullanılır, ancak sıralama numaralar atlayabilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="4daf2-188">Örneğin, bir kullanıcı bir hareketi iptal ederse, bir sayı oluşturulur fakat kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="4daf2-189">Devamlı bir numara sırasında bu sayı daha sonra tekrar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4daf2-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="4daf2-190">Sürekli olmayan bir numara serisinde bu numara kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="4daf2-191">Sürekli numara serileri genellikle satınalma siparişleri, satış siparişleri ve faturalar gibi dış belgeler için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="4daf2-192">Ancak, sürekli numara serileri, her yeni belge veya kayıt oluşturulduğunda numara için veritabanından yeni bir talep yapılması gerekeceği için sistem yanıt sürelerini olumsuz şekilde etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="4daf2-193">Sürekli olmayan bir numara serisi kullanırsanız, **Numara serileri** sayfasındaki **Performans** hızlı sekmesi üzerinde **Ön tahsisi** etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="4daf2-194">Ön tahsis edilecek bir numara miktarı belirttiğinizde, sistem bu numaraları seçer ve bellekte depolar.</span><span class="sxs-lookup"><span data-stu-id="4daf2-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="4daf2-195">Ön tahsis edilen miktar kullanıldıktan sonra veritabanından yeni numaralar talep edilir.</span><span class="sxs-lookup"><span data-stu-id="4daf2-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="4daf2-196">Sürekli numara sıraları kullanmak bir yasal gereklilik değilse, daha iyi performans için sürekli olmayan numara serileri kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="4daf2-197">Numara serilerinin otomatik temizlemesi</span><span class="sxs-lookup"><span data-stu-id="4daf2-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="4daf2-198">Güç kesintisi, bir uygulama hatası veya diğer beklenmeyen bir hata olması durumunda, sistem sürekli numara serileri için numaraların geri dönüşünü gerçekleştiremez.</span><span class="sxs-lookup"><span data-stu-id="4daf2-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="4daf2-199">Kayıp numaraları kurtarmak için temizleme işlemini otomatik olarak veya el ile çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="4daf2-200">Temizleme işlemi planlarken sunucu kullanımını dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="4daf2-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="4daf2-201">Temizleme işlemini yoğun olmayan saatlerde toplu iş olarak gerçekleştirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="4daf2-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>







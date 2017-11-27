---
title: "Sales'teki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme"
description: "Bu konu, satış teklif başlıkları ve satırlarını Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="45d19-103">Sales'teki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="45d19-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="45d19-104">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun.</span><span class="sxs-lookup"><span data-stu-id="45d19-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="45d19-105">Bu konu, satış teklif başlıkları ve satırlarını Microsoft Dynamics 365 for Sales'tan (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a (Finance and Operations) eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="45d19-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="45d19-106">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="45d19-106">Template and tasks</span></span>

<span data-ttu-id="45d19-107">Aşağıdaki şablonlar ve altta yatan görevler, teklif başlıklarını ve satırlarını Sales'tan Finance to Operations'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="45d19-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="45d19-108">**Şablonun adı:** Satış Teklifleri (Sales'tan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="45d19-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="45d19-109">**Projedeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="45d19-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="45d19-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="45d19-110">QuoteHeader</span></span>
    - <span data-ttu-id="45d19-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="45d19-111">QuoteLine</span></span>

<span data-ttu-id="45d19-112">Aşağıdaki eşitleme görevleri, satış teklifi başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.</span><span class="sxs-lookup"><span data-stu-id="45d19-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="45d19-113">Ürünler (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="45d19-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="45d19-114">Hesaplar (Sales'tan Fin and Ops'a) (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="45d19-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="45d19-115">İlgili kişiden Müşterilere (Sales'tan Fin and Ops'a) (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="45d19-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="45d19-116">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="45d19-116">Entity set</span></span>

| <span data-ttu-id="45d19-117">Satış</span><span class="sxs-lookup"><span data-stu-id="45d19-117">Sales</span></span>        | <span data-ttu-id="45d19-118">CDS</span><span class="sxs-lookup"><span data-stu-id="45d19-118">CDS</span></span>           | <span data-ttu-id="45d19-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="45d19-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="45d19-120">Alıntılar</span><span class="sxs-lookup"><span data-stu-id="45d19-120">Quotes</span></span>       | <span data-ttu-id="45d19-121">Teklif</span><span class="sxs-lookup"><span data-stu-id="45d19-121">Quotation</span></span>     | <span data-ttu-id="45d19-122">Satış teklifi başlıkları</span><span class="sxs-lookup"><span data-stu-id="45d19-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="45d19-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="45d19-123">QuoteDetails</span></span> | <span data-ttu-id="45d19-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="45d19-124">QuotationLine</span></span> | <span data-ttu-id="45d19-125">CDS satış teklifi satırları</span><span class="sxs-lookup"><span data-stu-id="45d19-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="45d19-126">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="45d19-126">Entity flow</span></span>

<span data-ttu-id="45d19-127">Sales'ta oluşturulmuş ve Finance and Operations'a eşitlenmiş satış teklifleri.</span><span class="sxs-lookup"><span data-stu-id="45d19-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="45d19-128">Sales'taki satış teklifleri, yalnızca aşağıdaki koşullar gerçekleşirse eşitlenir:</span><span class="sxs-lookup"><span data-stu-id="45d19-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="45d19-129">Satış teklifi satırlarındaki tüm ürünler harici olarak yönetiliyor.</span><span class="sxs-lookup"><span data-stu-id="45d19-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="45d19-130">Satış teklifi etkin veya devre dışı.</span><span class="sxs-lookup"><span data-stu-id="45d19-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="45d19-131">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="45d19-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="45d19-132">**Yalnızca Harici Tutulan Ürünleri Var** alanı, satış teklifinin tümüyle harici tutulan ürünlerden oluşup oluşmadığını istikrarlı bir şekilde izlemek için Teklif varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="45d19-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="45d19-133">Bir satış teklifi yalnızca harici tutulan ürünlere sahipse, ürünler Finance and Operations'ta tutulur.</span><span class="sxs-lookup"><span data-stu-id="45d19-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="45d19-134">Bu davranış, Finance and Operations tarafından bilenmeyen ürünlerin satış teklifi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="45d19-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="45d19-135">Teklif üzerindeki tüm satırlar ve ürünler, teklif başlığından **Yalnızca Harici Tutulan Ürünlere Sahip** bilgisi ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="45d19-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="45d19-136">Bu bilgi, Teklif satırı varlığındaki **Teklif Yalnızca Harici Olarak Tutulan Ürünlere Sahip** alanında bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="45d19-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="45d19-137">**İskonto**, **Masraflar** ve **Vergi** alanları Finance and Operations'ta karmaşık bir kurulumda denetlenir.</span><span class="sxs-lookup"><span data-stu-id="45d19-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="45d19-138">Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="45d19-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="45d19-139">Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları ana kaydı üretilen ve Finance and Operations tarafından işlenendir.</span><span class="sxs-lookup"><span data-stu-id="45d19-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="45d19-140">Sales'ta, çözüm aşağıdaki alanları salt okunur yapar çünkü değerler Finance and Operations'a eşitlenmez:</span><span class="sxs-lookup"><span data-stu-id="45d19-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="45d19-141">**Satış teklifi başlığındaki okunur alanlar:** İskonto % İskonto, Navlun Tutarı</span><span class="sxs-lookup"><span data-stu-id="45d19-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="45d19-142">**Satış teklifi satırlarındaki salt okunur alanlar:** Vergi</span><span class="sxs-lookup"><span data-stu-id="45d19-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="45d19-143">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="45d19-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="45d19-144">Satış siparişlerini eşitlemeden önce, sistemleri aşağıdaki ayarla güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="45d19-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="45d19-145">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="45d19-145">Setup in Sales</span></span>

- <span data-ttu-id="45d19-146">**Ayarlar** &gt; **Yönetim** &gt; **Sistem ayarları** &gt; **Satışlar**'a gidin ve **İskonto hesaplama yöntemi** alanının **Birim başına** olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="45d19-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="45d19-147">Bu ayar, Sales'taki satır madde iskontosunun, Finance and Operations'taki ayarla eşleştiğini garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="45d19-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="45d19-148">Aksi taktirde, iskonto Finance and Operations'ta doğru olmayacaktır çünkü Finance and Operations iskontoyu, satır Sales'ta satır başına iskonto olsa da bir birim başına iskonto olarak okuyacaktır.</span><span class="sxs-lookup"><span data-stu-id="45d19-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="45d19-149">Finance and Operations'ta kurulum</span><span class="sxs-lookup"><span data-stu-id="45d19-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="45d19-150">**Alacak hesapları** &gt; **Kurulum** &gt; **Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="45d19-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="45d19-151">**Numara serisi** sekmesinde, satış teklifleri için numara serisini seçin ve **Ayrıntıları görüntüle** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="45d19-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="45d19-152">**Genel Kurulum** altında, **El ile** alanını **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45d19-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="45d19-153">**Alacak hesapları** &gt; **Kurulum** &gt; **Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="45d19-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="45d19-154">**Sevkiyatlar** sekmesinde, **Teslimat tarih denetimi** alanına **Hiçbir** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45d19-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="45d19-155">Bu ayar, eşitlemenin satış teklifleri için başarısız olmasını engellemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="45d19-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="45d19-156">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="45d19-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="45d19-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="45d19-157">QuoteHeader</span></span>

- <span data-ttu-id="45d19-158">**İstenen teslimat tarihi** alanı Finance and Operations içinde gereklidir ve eşitleme, bu alan boş bırakılırsa başarısız olacaktır.</span><span class="sxs-lookup"><span data-stu-id="45d19-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="45d19-159">Bu sorunu önlemek için alan boşsa, **Kaynak &gt; CDS**'den bir varsayılan veri alınır.</span><span class="sxs-lookup"><span data-stu-id="45d19-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="45d19-160">Tarih, tercih edilen bir değere güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="45d19-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="45d19-161">Şu anda, bugünün tarihini temsil etmek için **Bugün** gibi bir değer giremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="45d19-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="45d19-162">Belirli bir tarih girmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="45d19-162">You must enter a specific date.</span></span> <span data-ttu-id="45d19-163">**İstenen teslimat tarihi** için varsayılan şablon değeri **1/1/2020**'dir.</span><span class="sxs-lookup"><span data-stu-id="45d19-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="45d19-164">**Adres Ülke bölge kodu** alanı Finance and Operations'ta gereklidir.</span><span class="sxs-lookup"><span data-stu-id="45d19-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="45d19-165">Eşitleme hatalarını önlemek için, Sales'ta bir alan boş bırakılırsa kullanılacak bir varsayılan değer belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="45d19-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="45d19-166">Bu varsayılan değer, yerel adresler için **Ülke bölgesi** alanına el ile bir değer girmenize gerek kalmayacağı için yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="45d19-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="45d19-167">**DeliveryAddressCountryRegionISOCode** için varsayılan bir şablon değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="45d19-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="45d19-168">**CDS Kuruluş Kodu** için eşleşmeyi **Kaynak &gt; CDS** içerisinde, Kuruluş varlığında **CDS kuruluşu** ile eşleşmesi için güncelleştir:</span><span class="sxs-lookup"><span data-stu-id="45d19-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="45d19-169">**Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="45d19-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="45d19-170">**Account_Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="45d19-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="45d19-171">**InvoiceAccount_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="45d19-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="45d19-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="45d19-172">QuoteLine</span></span>

- <span data-ttu-id="45d19-173">**CDS Kuruluş Kodu** için eşleşmeyi **Kaynak &gt; CDS** içerisinde, Kuruluş varlığında **CDS kuruluşu** ile eşleşmesi için güncelleştir:</span><span class="sxs-lookup"><span data-stu-id="45d19-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="45d19-174">**Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="45d19-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="45d19-175">**Product_Organization_Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="45d19-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="45d19-176">**Quotation_Organization_Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="45d19-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="45d19-177">**İstenen teslimat tarihi** alanı Finance and Operations içinde gereklidir ve eşitleme, bu alan boş bırakılırsa başarısız olacaktır.</span><span class="sxs-lookup"><span data-stu-id="45d19-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="45d19-178">Bu sorunu önlemek için alan boşsa, **Kaynak &gt; CDS**'den bir varsayılan veri alınır.</span><span class="sxs-lookup"><span data-stu-id="45d19-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="45d19-179">Tarih, tercih edilen bir değere güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="45d19-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="45d19-180">Şu anda, bugünün tarihini temsil etmek için **Bugün** gibi bir değer giremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="45d19-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="45d19-181">Belirli bir tarih girmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="45d19-181">You must enter a specific date.</span></span> <span data-ttu-id="45d19-182">**İstenen teslimat tarihi** için varsayılan şablon değeri **1/1/2020**'dir.</span><span class="sxs-lookup"><span data-stu-id="45d19-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="45d19-183">Aşağıdaki eşleşmeleri **CDS &gt; Hedef**'ten aşağıdaki eşleşmeleri ekleyerek, teklif satırlarının müşteriden veya üründen gelen varsayılan bilgi yoksa Finance and Operations'a içe aktarılmasını garanti etmeye yardımcı olabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="45d19-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="45d19-184">**SiteId** - Finance and Operations'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="45d19-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="45d19-185">**SiteId** için varsayılan şablon değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="45d19-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="45d19-186">**WarehouseId** - Finance and Operations'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="45d19-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="45d19-187">**WarehouseId** için varsayılan şablon değeri yoktur.</span><span class="sxs-lookup"><span data-stu-id="45d19-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="45d19-188">Satış ölçü birimi (UOM) için gerekli değer eşlemesinin Finance and Operations içinde, **Quantity_UOM**'dan **SALESUNITSYMBOL**'a **CDS &gt; Hedef** eşlemesinde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="45d19-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="45d19-189">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="45d19-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="45d19-190">**İskonto**, **Masraflar** ve **Vergi** alanları Finance and Operations'ta karmaşık bir kurulumda denetlenir.</span><span class="sxs-lookup"><span data-stu-id="45d19-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="45d19-191">Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="45d19-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="45d19-192">Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları Finance and Operations tarafından işlenir.</span><span class="sxs-lookup"><span data-stu-id="45d19-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="45d19-193">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="45d19-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="45d19-194">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="45d19-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="45d19-195">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="45d19-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="45d19-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="45d19-196">QuoteHeader</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="45d19-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="45d19-199">QuoteLine</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="45d19-202">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="45d19-202">Related topics</span></span>

[<span data-ttu-id="45d19-203">Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="45d19-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="45d19-204">Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="45d19-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="45d19-205">Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="45d19-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)




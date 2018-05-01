---
title: "Field Service'taki sözleşme faturalarını Finance and Operations'taki serbest metin faturalarıyla eşitleme"
description: "Bu konu, Microsoft Dynamics 365 for Field Service'taki sözleşme faturalarını Microsoft Dynamics 365 for Finance and Operations'taki serbest metin faturalarıyla eşitlemek için temel görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: tr-tr
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="a2c55-103">Field Service'taki sözleşme faturalarını Finance and Operations'taki serbest metin faturalarıyla eşitleme</span><span class="sxs-lookup"><span data-stu-id="a2c55-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a2c55-104">Bu konu, Microsoft Dynamics 365 for Field Service'taki sözleşme faturalarını Microsoft Dynamics 365 for Finance and Operations'taki serbest metin faturalarıyla eşitlemek için temel görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="a2c55-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a2c55-105">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="a2c55-105">Templates and tasks</span></span>

<span data-ttu-id="a2c55-106">Aşağıdaki şablon ve temel görevler Field Service'taki sözleşme faturaları ile Finance and Operations'taki serbest metin faturaları eşitlemesi çalıştırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2c55-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="a2c55-107">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="a2c55-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="a2c55-108">Sözleşme faturaları (Field Service to Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a2c55-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="a2c55-109">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="a2c55-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="a2c55-110">Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="a2c55-110">Invoice headers</span></span>
- <span data-ttu-id="a2c55-111">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="a2c55-111">Invoice lines</span></span>

<span data-ttu-id="a2c55-112">Aşağıdaki eşitleme faturası faturalarının eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="a2c55-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="a2c55-113">Hesaplar (Sales'ten Fin and Ops'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="a2c55-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="a2c55-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="a2c55-114">Entity set</span></span>

| <span data-ttu-id="a2c55-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="a2c55-115">Field Service</span></span>  | <span data-ttu-id="a2c55-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a2c55-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="a2c55-117">faturalar</span><span class="sxs-lookup"><span data-stu-id="a2c55-117">invoices</span></span>       | <span data-ttu-id="a2c55-118">CDS müşteri serbest metin faturası başlıkları</span><span class="sxs-lookup"><span data-stu-id="a2c55-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="a2c55-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="a2c55-119">invoicedetails</span></span> | <span data-ttu-id="a2c55-120">CDS müşteri serbest metin faturası satırları</span><span class="sxs-lookup"><span data-stu-id="a2c55-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="a2c55-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="a2c55-121">Entity flow</span></span>

<span data-ttu-id="a2c55-122">Field Service'taki bir sözlemeden oluşturulan faturalar Common Data Service (CDS) Veri tümleştirme projesi aracılığıyla Finance and Operations ile eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="a2c55-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="a2c55-123">Bu faturalardaki güncelleştirmeler serbest metin faturaları muhasebe durumunun **İşlemde** olması durumunda Finance and Operations'taki serbest metin faturalarıyla eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="a2c55-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="a2c55-124">Serbest metin faturaları Finance and Operations'da defetere nakledildikten ve muhasebe durumu **Tamamlandı** olarak güncelleştirildikten sonra Field Service'tan güncelleştirmeleri eşitleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2c55-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="a2c55-125">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="a2c55-125">Field Service CRM solution</span></span>

<span data-ttu-id="a2c55-126">**Sözleşme Kaynaklı Satırlar Var** alanı **Fatura** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="a2c55-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="a2c55-127">Bu alan yalnızca bir sözleşmeden oluşturulan faturaların eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a2c55-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="a2c55-128">Fatura bir sözleşemeden kaynaklanan en az bir satır içeriyorsa değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="a2c55-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="a2c55-129">**Sözleşme Kaynağı Var** alanı **Fatura Satırı** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="a2c55-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="a2c55-130">Bu alan yalnızca bir sözleşmeden oluşturulan fatura satırlarının eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a2c55-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="a2c55-131">Fatura satırının kaynağı bir sözleşmeyse değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="a2c55-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="a2c55-132">**Fatura tarihi** Finance and Operations'ta zorunlu bir alandır.</span><span class="sxs-lookup"><span data-stu-id="a2c55-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="a2c55-133">Bu nedenle, eşitlemeden önce Field Service'ta alanın bir değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a2c55-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="a2c55-134">Bu gereksinimi karşılamak için aşağıdaki mantık eklenir:</span><span class="sxs-lookup"><span data-stu-id="a2c55-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="a2c55-135">**Fatura Tarihi** alanı **Fatura** varlığında boşsa (diğer bir deyişle, değer yoksa), bu alan bir sözleşmeden kaynaklanan bir fatura satırının eklendiği geçerli tarih olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a2c55-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="a2c55-136">Kullanıcı, **Fatura Tarihi** alanını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="a2c55-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="a2c55-137">Ancak, kullanıcı bir sözleşemeden kaynaklanan fatura kaydetmeye çalıştığında, faturada **Fatura Tarihi** alanının boş olması durumunda bir iş süreci hatası alır.</span><span class="sxs-lookup"><span data-stu-id="a2c55-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a2c55-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="a2c55-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="a2c55-139">Finance and Operations'ta</span><span class="sxs-lookup"><span data-stu-id="a2c55-139">In Finance and Operations</span></span>

<span data-ttu-id="a2c55-140">Field Service'ta sözleşme faturalarından oluşturulan Finance and Operations'taki serbest metin faturalarını ayırmak amacıyla tümleştirmek için bir fatura kaynağı ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a2c55-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="a2c55-141">Bir faturanın kaynağı **Sözleşme faturası tümleştirmesi** türünde olduğunda, **Harici fatura numarası** alanı **Satış faturası** başlığında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a2c55-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="a2c55-142">Fatura başlığında görünmesinin yanı sıra **Harici fatura numarası** bilgileri Filed Service'taki sözleşme faturalarından oluşturulan faturaların Finance and Operations'tan Field Service'a fatura eşitleme sırasında filtrelenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a2c55-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="a2c55-143">**Alacak hesapları** \> **Kurulum** \> **Fatura kaynağı kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a2c55-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="a2c55-144">**Yeni**'yi seçerek yeni bir fatura kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a2c55-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="a2c55-145">**Fatura kaynağı** alanına, fatura kaynağı için **FS** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a2c55-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="a2c55-146">**Açıklama** alanında, **Field Service Sözleşme Faturası** gibi bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="a2c55-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="a2c55-147">**Kaynak türü ataması** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a2c55-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="a2c55-148">**Fatura kaynağı türü** alanını **Sözleşme faturası tümleştirmesi** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a2c55-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="a2c55-149">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a2c55-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="a2c55-150">Veri Tümleştirme projesinde</span><span class="sxs-lookup"><span data-stu-id="a2c55-150">In the Data Integration project</span></span>

<span data-ttu-id="a2c55-151">Görev: **Fatura satırları**</span><span class="sxs-lookup"><span data-stu-id="a2c55-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="a2c55-152">Finance and Operations **Ana Hesap Görünen Değeri** alanı için varsayılan değerin istenen değerle eşleşmek üzere güncelleştirilmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="a2c55-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="a2c55-153">Varsayılan şablon değeri **401100**'dur.</span><span class="sxs-lookup"><span data-stu-id="a2c55-153">The default template value is **401100**.</span></span>

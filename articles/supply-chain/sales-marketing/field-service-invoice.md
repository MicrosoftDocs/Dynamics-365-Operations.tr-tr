---
title: Field Service'taki sözleşme faturalarını Finance and Operations'taki serbest metin faturalarıyla eşitleme
description: Sözleşme faturalarını Microsoft Dynamics 365 for Field Service üzerinden Microsoft Dynamics 365 for Finance and Operations içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "333266"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="c7336-103">Field Service'daki sözleşme faturalarını Finance and Operations'daki serbest metin faturalarıyla eşitleme</span><span class="sxs-lookup"><span data-stu-id="c7336-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c7336-104">Sözleşme faturalarını Microsoft Dynamics 365 for Field Service üzerinden Microsoft Dynamics 365 for Finance and Operations içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="c7336-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c7336-105">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="c7336-105">Templates and tasks</span></span>

<span data-ttu-id="c7336-106">Aşağıdaki şablon ve temel görevler Field Service'taki sözleşme faturaları ile Finance and Operations'taki serbest metin faturaları eşitlemesi çalıştırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7336-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="c7336-107">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="c7336-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="c7336-108">Sözleşme faturaları (Field Service to Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c7336-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="c7336-109">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="c7336-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="c7336-110">Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="c7336-110">Invoice headers</span></span>
- <span data-ttu-id="c7336-111">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="c7336-111">Invoice lines</span></span>

<span data-ttu-id="c7336-112">Aşağıdaki eşitleme faturası faturalarının eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="c7336-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="c7336-113">Hesaplar (Sales'ten Fin and Ops'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="c7336-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="c7336-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="c7336-114">Entity set</span></span>

| <span data-ttu-id="c7336-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="c7336-115">Field Service</span></span>  | <span data-ttu-id="c7336-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c7336-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="c7336-117">faturalar</span><span class="sxs-lookup"><span data-stu-id="c7336-117">invoices</span></span>       | <span data-ttu-id="c7336-118">CDS müşteri serbest metin faturası başlıkları</span><span class="sxs-lookup"><span data-stu-id="c7336-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="c7336-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="c7336-119">invoicedetails</span></span> | <span data-ttu-id="c7336-120">CDS müşteri serbest metin faturası satırları</span><span class="sxs-lookup"><span data-stu-id="c7336-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="c7336-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="c7336-121">Entity flow</span></span>

<span data-ttu-id="c7336-122">Field Service'taki bir sözlemeden oluşturulan faturalar Common Data Service (CDS) Veri tümleştirme projesi aracılığıyla Finance and Operations ile eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="c7336-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="c7336-123">Bu faturalardaki güncelleştirmeler serbest metin faturaları muhasebe durumunun **İşlemde** olması durumunda Finance and Operations'taki serbest metin faturalarıyla eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="c7336-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="c7336-124">Serbest metin faturaları Finance and Operations'da defetere nakledildikten ve muhasebe durumu **Tamamlandı** olarak güncelleştirildikten sonra Field Service'tan güncelleştirmeleri eşitleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7336-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c7336-125">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="c7336-125">Field Service CRM solution</span></span>

<span data-ttu-id="c7336-126">**Sözleşme Kaynaklı Satırlar Var** alanı **Fatura** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="c7336-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="c7336-127">Bu alan yalnızca bir sözleşmeden oluşturulan faturaların eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c7336-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="c7336-128">Fatura bir sözleşemeden kaynaklanan en az bir satır içeriyorsa değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="c7336-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="c7336-129">**Sözleşme Kaynağı Var** alanı **Fatura Satırı** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="c7336-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="c7336-130">Bu alan yalnızca bir sözleşmeden oluşturulan fatura satırlarının eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c7336-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="c7336-131">Fatura satırının kaynağı bir sözleşmeyse değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="c7336-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="c7336-132">**Fatura tarihi** Finance and Operations'ta zorunlu bir alandır.</span><span class="sxs-lookup"><span data-stu-id="c7336-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="c7336-133">Bu nedenle, eşitlemeden önce Field Service'ta alanın bir değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c7336-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="c7336-134">Bu gereksinimi karşılamak için aşağıdaki mantık eklenir:</span><span class="sxs-lookup"><span data-stu-id="c7336-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="c7336-135">**Fatura Tarihi** alanı **Fatura** varlığında boşsa (diğer bir deyişle, değer yoksa), bu alan bir sözleşmeden kaynaklanan bir fatura satırının eklendiği geçerli tarih olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c7336-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="c7336-136">Kullanıcı, **Fatura Tarihi** alanını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="c7336-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="c7336-137">Ancak, kullanıcı bir sözleşemeden kaynaklanan fatura kaydetmeye çalıştığında, faturada **Fatura Tarihi** alanının boş olması durumunda bir iş süreci hatası alır.</span><span class="sxs-lookup"><span data-stu-id="c7336-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c7336-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="c7336-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="c7336-139">Finance and Operations'ta</span><span class="sxs-lookup"><span data-stu-id="c7336-139">In Finance and Operations</span></span>

<span data-ttu-id="c7336-140">Field Service'ta sözleşme faturalarından oluşturulan Finance and Operations'taki serbest metin faturalarını ayırmak amacıyla tümleştirmek için bir fatura kaynağı ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c7336-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="c7336-141">Bir faturanın kaynağı **Sözleşme faturası tümleştirmesi** türünde olduğunda, **Harici fatura numarası** alanı **Satış faturası** başlığında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c7336-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="c7336-142">Fatura başlığında görünmesinin yanı sıra **Harici fatura numarası** bilgileri Filed Service'taki sözleşme faturalarından oluşturulan faturaların Finance and Operations'tan Field Service'a fatura eşitleme sırasında filtrelenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c7336-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="c7336-143">**Alacak hesapları** \> **Kurulum** \> **Fatura kaynağı kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c7336-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="c7336-144">**Yeni**'yi seçerek yeni bir fatura kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c7336-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="c7336-145">**Fatura kaynağı** alanına, fatura kaynağı için **FS** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="c7336-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="c7336-146">**Açıklama** alanında, **Field Service Sözleşme Faturası** gibi bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c7336-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="c7336-147">**Kaynak türü ataması** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c7336-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="c7336-148">**Fatura kaynağı türü** alanını **Sözleşme faturası tümleştirmesi** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c7336-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="c7336-149">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7336-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="c7336-150">Veri Tümleştirme projesinde</span><span class="sxs-lookup"><span data-stu-id="c7336-150">In the Data Integration project</span></span>

<span data-ttu-id="c7336-151">Görev: **Fatura satırları**</span><span class="sxs-lookup"><span data-stu-id="c7336-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="c7336-152">Finance and Operations **Ana Hesap Görünen Değeri** alanı için varsayılan değerin istenen değerle eşleşmek üzere güncelleştirilmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="c7336-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="c7336-153">Varsayılan şablon değeri **401100**'dur.</span><span class="sxs-lookup"><span data-stu-id="c7336-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c7336-154">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="c7336-154">Template mapping in Data integration</span></span>

<span data-ttu-id="c7336-155">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7336-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a><span data-ttu-id="c7336-156">Sözleşme faturaları (Field Service'tan Fin and Ops'a): Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="c7336-156">Agreement invoices (Field Service to Fin and Ops): Invoice headers</span></span>

<span data-ttu-id="c7336-157">[![Veri tümleştirmede şablon eşleme](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="c7336-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a><span data-ttu-id="c7336-158">Sözleşme faturaları (Field Service'tan Fin and Ops'a): Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="c7336-158">Agreement invoices (Field Service to Fin and Ops): Invoice lines</span></span>

<span data-ttu-id="c7336-159">[![Veri tümleştirmede şablon eşleme](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="c7336-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>

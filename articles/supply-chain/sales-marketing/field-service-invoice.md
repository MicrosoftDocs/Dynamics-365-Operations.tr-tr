---
title: Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme
description: Sözleşme faturalarını Dynamics 365 Field Service üzerinden Dynamics 365 Supply Chain Management içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
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
ms.openlocfilehash: 3ca0014dc8bc1c70670a3cf85527eee0ef44865f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249877"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="9de6c-103">Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme</span><span class="sxs-lookup"><span data-stu-id="9de6c-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9de6c-104">Sözleşme faturalarını Dynamics 365 Field Service üzerinden Dynamics 365 Supply Chain Management içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="9de6c-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9de6c-105">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="9de6c-105">Templates and tasks</span></span>

<span data-ttu-id="9de6c-106">Aşağıdaki şablon ve temel görevler Field Service'taki sözleşme faturaları ile Supply Chain Management'taki serbest metin faturaları eşitlemesi çalıştırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9de6c-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="9de6c-107">**Veri tümleştirmesindeki şablonun adı**</span><span class="sxs-lookup"><span data-stu-id="9de6c-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="9de6c-108">Sözleşme faturaları (Field Service'tan Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="9de6c-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="9de6c-109">**Veri tümleştirme projesindeki görevlerin adları**</span><span class="sxs-lookup"><span data-stu-id="9de6c-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="9de6c-110">Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="9de6c-110">Invoice headers</span></span>
- <span data-ttu-id="9de6c-111">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="9de6c-111">Invoice lines</span></span>

<span data-ttu-id="9de6c-112">Aşağıdaki eşitleme faturası faturalarının eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="9de6c-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="9de6c-113">Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="9de6c-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="9de6c-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="9de6c-114">Entity set</span></span>

| <span data-ttu-id="9de6c-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="9de6c-115">Field Service</span></span>  | <span data-ttu-id="9de6c-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9de6c-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="9de6c-117">faturalar</span><span class="sxs-lookup"><span data-stu-id="9de6c-117">invoices</span></span>       | <span data-ttu-id="9de6c-118">CDS müşteri serbest metin faturası başlıkları</span><span class="sxs-lookup"><span data-stu-id="9de6c-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="9de6c-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="9de6c-119">invoicedetails</span></span> | <span data-ttu-id="9de6c-120">CDS müşteri serbest metin faturası satırları</span><span class="sxs-lookup"><span data-stu-id="9de6c-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="9de6c-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="9de6c-121">Entity flow</span></span>

<span data-ttu-id="9de6c-122">Field Service'taki bir sözlemeden oluşturulan faturalar Common Data Service Veri tümleştirme projesi aracılığıyla Supply Chain Management ile eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9de6c-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Common Data Service Data integration project.</span></span> <span data-ttu-id="9de6c-123">Bu faturalardaki güncelleştirmeler serbest metin faturaları muhasebe durumunun **İşlemde** olması durumunda Supply Chain Management'taki serbest metin faturalarıyla eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="9de6c-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="9de6c-124">Serbest metin faturaları Supply Chain Management'da defetere nakledildikten ve muhasebe durumu **Tamamlandı** olarak güncelleştirildikten sonra Field Service'tan güncelleştirmeleri eşitleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="9de6c-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="9de6c-125">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="9de6c-125">Field Service CRM solution</span></span>

<span data-ttu-id="9de6c-126">**Sözleşme Kaynaklı Satırlar Var** alanı **Fatura** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="9de6c-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="9de6c-127">Bu alan yalnızca bir sözleşmeden oluşturulan faturaların eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9de6c-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="9de6c-128">Fatura bir sözleşemeden kaynaklanan en az bir satır içeriyorsa değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="9de6c-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="9de6c-129">**Sözleşme Kaynağı Var** alanı **Fatura Satırı** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="9de6c-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="9de6c-130">Bu alan yalnızca bir sözleşmeden oluşturulan fatura satırlarının eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9de6c-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="9de6c-131">Fatura satırının kaynağı bir sözleşmeyse değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="9de6c-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="9de6c-132">**Fatura tarihi** Supply Chain Management'ta zorunlu bir alandır.</span><span class="sxs-lookup"><span data-stu-id="9de6c-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="9de6c-133">Bu nedenle, eşitlemeden önce Field Service'ta alanın bir değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9de6c-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="9de6c-134">Bu gereksinimi karşılamak için aşağıdaki mantık eklenir:</span><span class="sxs-lookup"><span data-stu-id="9de6c-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="9de6c-135">**Fatura Tarihi** alanı **Fatura** varlığında boşsa (diğer bir deyişle, değer yoksa), bu alan bir sözleşmeden kaynaklanan bir fatura satırının eklendiği geçerli tarih olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9de6c-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="9de6c-136">Kullanıcı, **Fatura Tarihi** alanını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="9de6c-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="9de6c-137">Ancak, kullanıcı bir sözleşemeden kaynaklanan fatura kaydetmeye çalıştığında, faturada **Fatura Tarihi** alanının boş olması durumunda bir iş süreci hatası alır.</span><span class="sxs-lookup"><span data-stu-id="9de6c-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9de6c-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="9de6c-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="9de6c-139">Supply Chain Management'ta</span><span class="sxs-lookup"><span data-stu-id="9de6c-139">In Supply Chain Management</span></span>

<span data-ttu-id="9de6c-140">Field Service'ta sözleşme faturalarından oluşturulan Supply Chain Management'taki serbest metin faturalarını ayırmak amacıyla tümleştirmek için bir fatura kaynağı ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9de6c-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="9de6c-141">Bir faturanın kaynağı **Sözleşme faturası tümleştirmesi** türünde olduğunda, **Harici fatura numarası** alanı **Satış faturası** başlığında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="9de6c-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="9de6c-142">Fatura başlığında görünmesinin yanı sıra **Harici fatura numarası** bilgileri Filed Service'taki sözleşme faturalarından oluşturulan faturaların Supply Chain Management'tan Field Service'a fatura eşitleme sırasında filtrelenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9de6c-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="9de6c-143">**Alacak hesapları** \> **Kurulum** \> **Fatura kaynağı kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="9de6c-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="9de6c-144">**Yeni**'yi seçerek yeni bir fatura kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9de6c-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="9de6c-145">**Fatura kaynağı** alanına, fatura kaynağı için **FS** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="9de6c-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="9de6c-146">**Açıklama** alanında, **Field Service Sözleşme Faturası** gibi bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="9de6c-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="9de6c-147">**Kaynak türü ataması** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9de6c-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="9de6c-148">**Fatura kaynağı türü** alanını **Sözleşme faturası tümleştirmesi** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9de6c-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="9de6c-149">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9de6c-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="9de6c-150">Veri Tümleştirme projesinde</span><span class="sxs-lookup"><span data-stu-id="9de6c-150">In the Data Integration project</span></span>

<span data-ttu-id="9de6c-151">Görev: **Fatura satırları**</span><span class="sxs-lookup"><span data-stu-id="9de6c-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="9de6c-152">Supply Chain Management **Ana Hesap Görünen Değeri** alanı için varsayılan değerin istenen değerle eşleşmek üzere güncelleştirilmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="9de6c-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="9de6c-153">Varsayılan şablon değeri **401100**'dur.</span><span class="sxs-lookup"><span data-stu-id="9de6c-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9de6c-154">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="9de6c-154">Template mapping in Data integration</span></span>

<span data-ttu-id="9de6c-155">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="9de6c-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="9de6c-156">Sözleşme faturaları (Field Service'tan Supply Chain Management'a): Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="9de6c-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="9de6c-157">[![Veri tümleştirmede şablon eşleme](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="9de6c-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="9de6c-158">Sözleşme faturaları (Field Service'tan Supply Chain Management'a): Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="9de6c-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="9de6c-159">[![Veri tümleştirmede şablon eşleme](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="9de6c-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>

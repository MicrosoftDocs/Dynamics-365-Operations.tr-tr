---
title: Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme
description: Sözleşme faturalarını Dynamics 365 Field Service üzerinden Dynamics 365 Supply Chain Management içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f1790366cebf317472bc1ef9a5ecd2a19fe755d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980843"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="0dd45-103">Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme</span><span class="sxs-lookup"><span data-stu-id="0dd45-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0dd45-104">Sözleşme faturalarını Dynamics 365 Field Service üzerinden Dynamics 365 Supply Chain Management içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="0dd45-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0dd45-105">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="0dd45-105">Templates and tasks</span></span>

<span data-ttu-id="0dd45-106">Aşağıdaki şablon ve temel görevler Field Service'taki sözleşme faturaları ile Supply Chain Management'taki serbest metin faturaları eşitlemesi çalıştırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0dd45-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="0dd45-107">**Veri tümleştirmesindeki şablonun adı**</span><span class="sxs-lookup"><span data-stu-id="0dd45-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="0dd45-108">Sözleşme faturaları (Field Service'tan Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="0dd45-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="0dd45-109">**Veri tümleştirme projesindeki görevlerin adları**</span><span class="sxs-lookup"><span data-stu-id="0dd45-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="0dd45-110">Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="0dd45-110">Invoice headers</span></span>
- <span data-ttu-id="0dd45-111">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="0dd45-111">Invoice lines</span></span>

<span data-ttu-id="0dd45-112">Aşağıdaki eşitleme faturası faturalarının eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="0dd45-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="0dd45-113">Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="0dd45-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="0dd45-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="0dd45-114">Entity set</span></span>

| <span data-ttu-id="0dd45-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="0dd45-115">Field Service</span></span>  | <span data-ttu-id="0dd45-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0dd45-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="0dd45-117">faturalar</span><span class="sxs-lookup"><span data-stu-id="0dd45-117">invoices</span></span>       | <span data-ttu-id="0dd45-118">Dataverse müşteri serbest metin faturası üst bilgileri</span><span class="sxs-lookup"><span data-stu-id="0dd45-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="0dd45-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="0dd45-119">invoicedetails</span></span> | <span data-ttu-id="0dd45-120">Dataverse müşteri serbest metin faturası satırları</span><span class="sxs-lookup"><span data-stu-id="0dd45-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="0dd45-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="0dd45-121">Entity flow</span></span>

<span data-ttu-id="0dd45-122">Field Service'taki bir sözlemeden oluşturulan faturalar Microsoft Dataverse Veri tümleştirme projesi aracılığıyla Supply Chain Management ile eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="0dd45-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="0dd45-123">Bu faturalardaki güncelleştirmeler serbest metin faturaları muhasebe durumunun **İşlemde** olması durumunda Supply Chain Management'taki serbest metin faturalarıyla eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="0dd45-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="0dd45-124">Serbest metin faturaları Supply Chain Management'da defetere nakledildikten ve muhasebe durumu **Tamamlandı** olarak güncelleştirildikten sonra Field Service'tan güncelleştirmeleri eşitleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="0dd45-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="0dd45-125">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="0dd45-125">Field Service CRM solution</span></span>

<span data-ttu-id="0dd45-126">**Sözleşme Kaynaklı Satırlar Var** sütunu **Fatura** tablosuna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="0dd45-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="0dd45-127">Bu sütun, yalnızca bir sözleşmeden oluşturulan faturaların eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0dd45-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="0dd45-128">Fatura bir sözleşemeden kaynaklanan en az bir satır içeriyorsa değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="0dd45-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="0dd45-129">**Sözleşme Kaynağı Var** sütunu **Fatura Satırı** tablosuna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="0dd45-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="0dd45-130">Bu sütun, yalnızca bir sözleşmeden oluşturulan fatura satırlarının eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0dd45-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="0dd45-131">Fatura satırının kaynağı bir sözleşmeyse değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="0dd45-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="0dd45-132">**Fatura tarihi** Supply Chain Management'ta zorunlu bir alandır.</span><span class="sxs-lookup"><span data-stu-id="0dd45-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="0dd45-133">Bu nedenle, eşitlemeden önce Field Service'ta sütunun bir değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0dd45-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="0dd45-134">Bu gereksinimi karşılamak için aşağıdaki mantık eklenir:</span><span class="sxs-lookup"><span data-stu-id="0dd45-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="0dd45-135">**Fatura Tarihi** sütunu **Fatura** tablosunda boşsa (diğer bir ifadeyle, değer yoksa), bu sütun bir sözleşmeden kaynaklanan bir fatura satırının eklendiği geçerli tarih olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="0dd45-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="0dd45-136">Kullanıcı, **Fatura Tarihi** sütununu değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="0dd45-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="0dd45-137">Ancak, kullanıcı bir sözleşemeden gelen bir fatura kaydetmeye çalıştığında, faturada **Fatura Tarihi** sütununun boş olması durumunda bir iş süreci hatası alır.</span><span class="sxs-lookup"><span data-stu-id="0dd45-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="0dd45-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="0dd45-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="0dd45-139">Supply Chain Management'ta</span><span class="sxs-lookup"><span data-stu-id="0dd45-139">In Supply Chain Management</span></span>

<span data-ttu-id="0dd45-140">Field Service'ta sözleşme faturalarından oluşturulan Supply Chain Management'taki serbest metin faturalarını ayırmak amacıyla tümleştirmek için bir fatura kaynağı ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0dd45-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="0dd45-141">Bir faturanın kaynağı **Sözleşme faturası tümleştirmesi** türünde olduğunda, **Harici fatura numarası** alanı **Satış faturası** başlığında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0dd45-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="0dd45-142">Fatura başlığında görünmesinin yanı sıra **Harici fatura numarası** bilgileri Filed Service'taki sözleşme faturalarından oluşturulan faturaların Supply Chain Management'tan Field Service'a fatura eşitleme sırasında filtrelenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0dd45-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="0dd45-143">**Alacak hesapları** \> **Kurulum** \> **Fatura kaynağı kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="0dd45-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="0dd45-144">**Yeni**'yi seçerek yeni bir fatura kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0dd45-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="0dd45-145">**Fatura kaynağı** alanına, fatura kaynağı için **FS** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="0dd45-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="0dd45-146">**Açıklama** alanında, **Field Service Sözleşme Faturası** gibi bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="0dd45-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="0dd45-147">**Kaynak türü ataması** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0dd45-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="0dd45-148">**Fatura kaynağı türü** alanını **Sözleşme faturası tümleştirmesi** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0dd45-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="0dd45-149">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0dd45-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="0dd45-150">Veri Tümleştirme projesinde</span><span class="sxs-lookup"><span data-stu-id="0dd45-150">In the Data Integration project</span></span>

<span data-ttu-id="0dd45-151">Görev: **Fatura satırları**</span><span class="sxs-lookup"><span data-stu-id="0dd45-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="0dd45-152">Supply Chain Management **Ana Hesap Görünen Değeri** alanı için varsayılan değerin istenen değerle eşleşmek üzere güncelleştirilmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="0dd45-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="0dd45-153">Varsayılan şablon değeri **401100**'dur.</span><span class="sxs-lookup"><span data-stu-id="0dd45-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0dd45-154">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="0dd45-154">Template mapping in Data integration</span></span>

<span data-ttu-id="0dd45-155">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="0dd45-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="0dd45-156">Sözleşme faturaları (Field Service'tan Supply Chain Management'a): Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="0dd45-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="0dd45-157">[![Veri tümleştirmede şablon eşleme](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="0dd45-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="0dd45-158">Sözleşme faturaları (Field Service'tan Supply Chain Management'a): Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="0dd45-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="0dd45-159">[![Veri tümleştirmede şablon eşleme](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="0dd45-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>

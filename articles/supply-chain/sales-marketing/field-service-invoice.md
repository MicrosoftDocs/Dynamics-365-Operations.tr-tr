---
title: Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme
description: Sözleşme faturalarını Dynamics 365 Field Service üzerinden Dynamics 365 Supply Chain Management içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 21a77a0289055285f47323803a484c012e662e3a
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102746"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="1900c-103">Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme</span><span class="sxs-lookup"><span data-stu-id="1900c-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1900c-104">Sözleşme faturalarını Dynamics 365 Field Service üzerinden Dynamics 365 Supply Chain Management içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="1900c-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1900c-105">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="1900c-105">Templates and tasks</span></span>

<span data-ttu-id="1900c-106">Aşağıdaki şablon ve temel görevler Field Service'taki sözleşme faturaları ile Supply Chain Management'taki serbest metin faturaları eşitlemesi çalıştırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1900c-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="1900c-107">**Veri tümleştirmesindeki şablonun adı**</span><span class="sxs-lookup"><span data-stu-id="1900c-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="1900c-108">Sözleşme faturaları (Field Service'tan Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="1900c-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="1900c-109">**Veri tümleştirme projesindeki görevlerin adları**</span><span class="sxs-lookup"><span data-stu-id="1900c-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="1900c-110">Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="1900c-110">Invoice headers</span></span>
- <span data-ttu-id="1900c-111">Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="1900c-111">Invoice lines</span></span>

<span data-ttu-id="1900c-112">Aşağıdaki eşitleme faturası faturalarının eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="1900c-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="1900c-113">Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="1900c-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="1900c-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="1900c-114">Entity set</span></span>

| <span data-ttu-id="1900c-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="1900c-115">Field Service</span></span>  | <span data-ttu-id="1900c-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1900c-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="1900c-117">faturalar</span><span class="sxs-lookup"><span data-stu-id="1900c-117">invoices</span></span>       | <span data-ttu-id="1900c-118">Dataverse müşteri serbest metin faturası üst bilgileri</span><span class="sxs-lookup"><span data-stu-id="1900c-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="1900c-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="1900c-119">invoicedetails</span></span> | <span data-ttu-id="1900c-120">Dataverse müşteri serbest metin faturası satırları</span><span class="sxs-lookup"><span data-stu-id="1900c-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="1900c-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="1900c-121">Entity flow</span></span>

<span data-ttu-id="1900c-122">Field Service'taki bir sözlemeden oluşturulan faturalar Microsoft Dataverse Veri tümleştirme projesi aracılığıyla Supply Chain Management ile eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="1900c-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="1900c-123">Bu faturalardaki güncelleştirmeler serbest metin faturaları muhasebe durumunun **İşlemde** olması durumunda Supply Chain Management'taki serbest metin faturalarıyla eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="1900c-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="1900c-124">Serbest metin faturaları Supply Chain Management'da defetere nakledildikten ve muhasebe durumu **Tamamlandı** olarak güncelleştirildikten sonra Field Service'tan güncelleştirmeleri eşitleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="1900c-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="1900c-125">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="1900c-125">Field Service CRM solution</span></span>

<span data-ttu-id="1900c-126">**Sözleşme Kaynaklı Satırlar Var** sütunu **Fatura** tablosuna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="1900c-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="1900c-127">Bu sütun, yalnızca bir sözleşmeden oluşturulan faturaların eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1900c-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="1900c-128">Fatura bir sözleşemeden kaynaklanan en az bir satır içeriyorsa değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="1900c-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="1900c-129">**Sözleşme Kaynağı Var** sütunu **Fatura Satırı** tablosuna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="1900c-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="1900c-130">Bu sütun, yalnızca bir sözleşmeden oluşturulan fatura satırlarının eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1900c-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="1900c-131">Fatura satırının kaynağı bir sözleşmeyse değer **doğru** olur.</span><span class="sxs-lookup"><span data-stu-id="1900c-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="1900c-132">**Fatura tarihi** Supply Chain Management'ta zorunlu bir alandır.</span><span class="sxs-lookup"><span data-stu-id="1900c-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="1900c-133">Bu nedenle, eşitlemeden önce Field Service'ta sütunun bir değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1900c-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="1900c-134">Bu gereksinimi karşılamak için aşağıdaki mantık eklenir:</span><span class="sxs-lookup"><span data-stu-id="1900c-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="1900c-135">**Fatura Tarihi** sütunu **Fatura** tablosunda boşsa (diğer bir ifadeyle, değer yoksa), bu sütun bir sözleşmeden kaynaklanan bir fatura satırının eklendiği geçerli tarih olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1900c-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="1900c-136">Kullanıcı, **Fatura Tarihi** sütununu değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1900c-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="1900c-137">Ancak, kullanıcı bir sözleşemeden gelen bir fatura kaydetmeye çalıştığında, faturada **Fatura Tarihi** sütununun boş olması durumunda bir iş süreci hatası alır.</span><span class="sxs-lookup"><span data-stu-id="1900c-137">However, when the user tries to save an invoice that originates from an agreement, they receive a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1900c-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="1900c-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="1900c-139">Supply Chain Management'ta</span><span class="sxs-lookup"><span data-stu-id="1900c-139">In Supply Chain Management</span></span>

<span data-ttu-id="1900c-140">Field Service'ta sözleşme faturalarından oluşturulan Supply Chain Management'taki serbest metin faturalarını ayırmak amacıyla tümleştirmek için bir fatura kaynağı ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1900c-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="1900c-141">Bir faturanın kaynağı **Sözleşme faturası tümleştirmesi** türünde olduğunda, **Harici fatura numarası** alanı **Satış faturası** başlığında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1900c-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="1900c-142">Fatura başlığında görünmesinin yanı sıra **Harici fatura numarası** bilgileri Filed Service'taki sözleşme faturalarından oluşturulan faturaların Supply Chain Management'tan Field Service'a fatura eşitleme sırasında filtrelenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1900c-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="1900c-143">**Alacak hesapları** \> **Kurulum** \> **Fatura kaynağı kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1900c-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="1900c-144">**Yeni**'yi seçerek yeni bir fatura kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1900c-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="1900c-145">**Fatura kaynağı** alanına, fatura kaynağı için **FS** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1900c-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="1900c-146">**Açıklama** alanında, **Field Service Sözleşme Faturası** gibi bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1900c-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="1900c-147">**Kaynak türü ataması** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1900c-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="1900c-148">**Fatura kaynağı türü** alanını **Sözleşme faturası tümleştirmesi** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1900c-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="1900c-149">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1900c-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="1900c-150">Veri Tümleştirme projesinde</span><span class="sxs-lookup"><span data-stu-id="1900c-150">In the Data Integration project</span></span>

<span data-ttu-id="1900c-151">Görev: **Fatura satırları**</span><span class="sxs-lookup"><span data-stu-id="1900c-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="1900c-152">Supply Chain Management **Ana Hesap Görünen Değeri** alanı için varsayılan değerin istenen değerle eşleşmek üzere güncelleştirilmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="1900c-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="1900c-153">Varsayılan şablon değeri **401100**'dur.</span><span class="sxs-lookup"><span data-stu-id="1900c-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1900c-154">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="1900c-154">Template mapping in Data integration</span></span>

<span data-ttu-id="1900c-155">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="1900c-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="1900c-156">Sözleşme faturaları (Field Service'tan Supply Chain Management'a): Fatura başlıkları</span><span class="sxs-lookup"><span data-stu-id="1900c-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="1900c-157">[![Fatura üstbilgileri için veri tümleştirmesinde şablon eşleme](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="1900c-157">[![Template mapping in Data integration for invoice headers](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="1900c-158">Sözleşme faturaları (Field Service'tan Supply Chain Management'a): Fatura satırları</span><span class="sxs-lookup"><span data-stu-id="1900c-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="1900c-159">[![Fatura satırları için veri tümleştirmesinde şablon eşleme](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="1900c-159">[![Template mapping in Data integration for invoice lines](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
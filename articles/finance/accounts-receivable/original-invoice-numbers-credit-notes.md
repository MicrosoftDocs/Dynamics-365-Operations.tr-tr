---
title: Alacak dekontlarındaki orijinal faturalara başvurular
description: Bu konu, ilgili alacak dekontlarında orijinal fatura numaralarının nasıl ayarlanacağını ve yazdırılacağını açıklamaktadır.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 04a4fc96cb7de60052b17e36c33ad5d5be322be4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207363"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="f8ff6-103">Alacak dekontlarındaki orijinal faturalara başvurular</span><span class="sxs-lookup"><span data-stu-id="f8ff6-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f8ff6-104">Bazı ülke/bölgelerde, yazdırılan alacak dekontlarının orijinal faturalara referanslar içermesi yasal bir gereksinim vardır.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="f8ff6-105">Bu konu, ilgili alacak dekontlarında orijinal fatura numaralarının nasıl ayarlanacağını ve yazdırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f8ff6-106">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="f8ff6-106">Prerequisites</span></span>

- <span data-ttu-id="f8ff6-107">**Özellik yönetimi** çalışma alanında, **Satış ve proje faturası raporları için alacak faturalama düzeni**'ni açın.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="f8ff6-108">Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8ff6-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="f8ff6-109">Gerekli belgelerin yazdırılabilir biçimleri Yazdırma yönetimi'nde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="f8ff6-110">Bu konuda açıklanan işlevsellik aşağıdaki belgeler için geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="f8ff6-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="f8ff6-111">**Alacak hesapları**</span><span class="sxs-lookup"><span data-stu-id="f8ff6-111">**Accounts receivable**</span></span>

- <span data-ttu-id="f8ff6-112">Serbest metinli alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="f8ff6-112">Free text credit note</span></span>
- <span data-ttu-id="f8ff6-113">Müşteri alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="f8ff6-113">Customer credit note</span></span>

<span data-ttu-id="f8ff6-114">**Proje yönetimi ve muhasebe**</span><span class="sxs-lookup"><span data-stu-id="f8ff6-114">**Project management and accounting**</span></span>

- <span data-ttu-id="f8ff6-115">Proje alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="f8ff6-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="f8ff6-116">Alacak hesapları parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f8ff6-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="f8ff6-117">Orijinal faturalara yapılan referansların ilgili alacak dekontlarına yazdırılıp yazdırılmadığını kontrol eden parametreyi ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="f8ff6-118">**Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="f8ff6-119">**Güncelleştirmeler** sekmesinde, **Fatura** hızlı sekmesinde, **Alacak faturalama düzenini satış ve proje fatura raporlarına uygula** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Alacak hesapları parametrelerini yapılandırma](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="f8ff6-121">Orijinal faturalara referansları tanımlama</span><span class="sxs-lookup"><span data-stu-id="f8ff6-121">Define references to original invoices</span></span>

<span data-ttu-id="f8ff6-122">Belge türüne göre orijinal faturalara referansları tanımlamak için aşağıdaki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="f8ff6-123">Serbest metinli alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="f8ff6-123">Free text credit note</span></span>

1. <span data-ttu-id="f8ff6-124">**Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="f8ff6-125">Yeni bir alacak dekontu oluşturun veya var olan bir alacak dekontunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="f8ff6-126">Faturayı açın.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-126">Open the invoice.</span></span>
4. <span data-ttu-id="f8ff6-127">Eylem Bölmesi'nde, **Fatura** sekmesindeki **İşlevler** grubunda **Alacak faturalaması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="f8ff6-128">Orijinal faturaya olan referansı girin ve düzeltme nedenini seçin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Serbest metin faturası için referans tanımlama](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="f8ff6-130">Müşteri alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="f8ff6-130">Customer credit note</span></span>

1. <span data-ttu-id="f8ff6-131">**Alacak hesapları** \> **Siparişler** \> **Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="f8ff6-132">Düzeltilmesi gereken faturalanmış satış siparişini seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="f8ff6-133">Eylem Bölmesi'nde, **Satış** sekmesindeki **Alacak dekontu** grubunda **Alacak dekontu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="f8ff6-134">Düzeltme nedenini girin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-134">Enter the reason for the correction.</span></span> <span data-ttu-id="f8ff6-135">Orijinal faturaya olan referans otomatik olarak kurulur.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-135">The reference to the original invoice is automatically established.</span></span>

![Satış siparişi için referans tanımlama](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="f8ff6-137">Proje alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="f8ff6-137">Project credit note</span></span>

1. <span data-ttu-id="f8ff6-138">**Proje yönetimi ve muhasebe** \> **Proje faturaları** \> **Proje faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="f8ff6-139">Düzeltilmesi gereken proje faturasını seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="f8ff6-140">Eylem Bölmesi'nde, **Proje faturası** sekmesindeki **İşlevler** grubunda **Alacak dekontu için seçin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="f8ff6-141">**Alacak faturalaması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="f8ff6-142">Düzeltme nedenini girin.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-142">Enter the reason for the correction.</span></span> <span data-ttu-id="f8ff6-143">Orijinal faturaya olan referans otomatik olarak kurulur.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-143">The reference to the original invoice is automatically established.</span></span>

![Proje faturası için referans tanımlama](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="f8ff6-145">Alacak dekontlarını yazdırma</span><span class="sxs-lookup"><span data-stu-id="f8ff6-145">Printing credit notes</span></span>

<span data-ttu-id="f8ff6-146">Serbest metin, müşteri ve proje alacak dekontlarını yazdırdığınızda, orijinal faturaya referans ve düzeltme sebebini içerecektir.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Yazdırılmış alacak dekontu](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="f8ff6-148">Orijinal faturalara yapılan başvuruların yazdırılacağını varsayarak belgelerin yazdırılabilir biçimlerinin doğru yapılandırılmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f8ff6-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
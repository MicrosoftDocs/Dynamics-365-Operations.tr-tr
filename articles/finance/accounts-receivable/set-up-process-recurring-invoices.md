---
title: Yinelenen faturalar oluşturma ve işleme
description: Bu makalede, yinelenen faturaların nasıl ayarlanıp işleneceği açıklanmaktadır. Müşterilere düzenli olarak aynı tutar için fatura kesmeniz gerekiyorsa, yinelenen faturalar kullanabilirsiniz.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b1d36262c35210e183e92c10f69e8511280443b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228089"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="c3c3a-104">Yinelenen faturalar oluşturma ve işleme</span><span class="sxs-lookup"><span data-stu-id="c3c3a-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3c3a-105">Bu makalede, yinelenen faturaların nasıl ayarlanıp işleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="c3c3a-106">Müşterilere düzenli olarak aynı tutar için fatura kesmeniz gerekiyorsa, yinelenen faturalar kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="c3c3a-107">Bir yinelenen serbest metin faturası şablonu oluşturun</span><span class="sxs-lookup"><span data-stu-id="c3c3a-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="c3c3a-108">Müşterilere düzenli olarak tekrarlanan aynı hizmetler için fatura düzenlemek için, faturaların oluşturulması için yeniden oluşturulabilen bir serbest metin faturası şablonu tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="c3c3a-109">Bu şablon şu bilgiler içerir:</span><span class="sxs-lookup"><span data-stu-id="c3c3a-109">This template contains the following information:</span></span>

-   <span data-ttu-id="c3c3a-110">Vergi grupları, ödeme süreleri ve ödeme yöntemi gibi başlık bilgileri</span><span class="sxs-lookup"><span data-stu-id="c3c3a-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="c3c3a-111">Hizmet açıklaması, gelir hesapları, birim fiyatı ve fatura tutarı gibi satırı bilgileri</span><span class="sxs-lookup"><span data-stu-id="c3c3a-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="c3c3a-112">Sevkiyat veya işleme giderleri</span><span class="sxs-lookup"><span data-stu-id="c3c3a-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="c3c3a-113">Maliyet merkezleri ve iş birimleri gibi mali boyut bilgilerinin yanı sıra hesap dağıtımları</span><span class="sxs-lookup"><span data-stu-id="c3c3a-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="c3c3a-114">Pratikte, tüm bir fatura oluşturur ve bunu şablon olarak kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="c3c3a-115">**Yinelenen faturalar** sayfasını kullanarak şablonlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="c3c3a-116">Bir müşteriye bir serbest metin fatura şablonu atayın ve yineleme bilgilerini girin</span><span class="sxs-lookup"><span data-stu-id="c3c3a-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="c3c3a-117">Şablon oluşturulduktan sonra faturalamak istediğiniz müşteriler için şablon atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="c3c3a-118">Ayrıca, faturanın ne zaman ve ne sıklıkla kullanılacağını da belirtmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="c3c3a-119">**Müşteriler** sayfasındaki **Fatura** sekmesindeki şablonları atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="c3c3a-120">Şablonu listeye ekleyin ve aşağıdaki bilgileri güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="c3c3a-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="c3c3a-121">Yinelenen faturalama için başlangıç tarihi ve isteğe bağlı olarak bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="c3c3a-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="c3c3a-122">Yineleme faturasının sıklığı (öreğin her gün veya ayda bir)</span><span class="sxs-lookup"><span data-stu-id="c3c3a-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="c3c3a-123">Maksimum faturalama tutarı (bu bilgiler gerekiyorsa)</span><span class="sxs-lookup"><span data-stu-id="c3c3a-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="c3c3a-124">Bir müşteri, farklı sıklıklara sahip, birden fazla şablona sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="c3c3a-125">Yinelenen faturalar oluşturma</span><span class="sxs-lookup"><span data-stu-id="c3c3a-125">Generate the recurring invoices</span></span>
<span data-ttu-id="c3c3a-126">**Yinelenen faturalar** sayfasında, yinelenen fatura şablonlarının işlenmesi için bir görev mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="c3c3a-127">Fatura tarihini ve faturaların oluşturulacağı şablonu belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="c3c3a-128">Faturalar oluşturulur ve işlenen her bir fatura grubu için tek bir yineleme kimlik numarası atanır.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="c3c3a-129">Yinelenen serbest metin faturalarını nakletme</span><span class="sxs-lookup"><span data-stu-id="c3c3a-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="c3c3a-130">Yinelenen faturalar oluşturulduktan sonra fatura yineleme kimlikleri **Yinelenen faturalar** sayfasındaki bir nakil görevinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="c3c3a-131">Bağlantıyı tıklayarak bir yineleme kimliği için faturaların tümünü görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="c3c3a-132">Yineleme kimliği için faturaları gözden geçirerek faturaları ayrı ayrı silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="c3c3a-133">Müşterinin yineleme ayarları o şablon için sıfırlanır ve böylece daha sonra yeniden oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="c3c3a-134">Bir yineleme kimliği için faturaların biri, birden fazlası veya tümü nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="c3c3a-135">İş akışları etkinleştirilirse, faturaları nakletmeden önce mutlaka **Gönder** düğmesini tıklamalısınız.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="c3c3a-136">Yinelenen serbest metin faturalarını yazdırma</span><span class="sxs-lookup"><span data-stu-id="c3c3a-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="c3c3a-137">Yinelenen faturalar nakledildikten sonra serbest metin faturası listesi sayfasından faturaları yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="c3c3a-138">Seçili faturaları yazdırabilirsiniz veya yazdırmak üzere bir seri fatura seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3c3a-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
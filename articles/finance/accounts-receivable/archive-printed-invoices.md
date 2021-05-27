---
title: Yazılı müşteri faturalarını karma numaralarla arşivle
description: Bu konu, yazdırılmış müşteri faturalarını karma numaralarla kaydetmek için arşivlemenin nasıl etkinleştirileceğini açıklar.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018990"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="aa180-103">Yazılı müşteri faturalarını karma numaralarla arşivle</span><span class="sxs-lookup"><span data-stu-id="aa180-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="aa180-104">Bazı ülkelerde, Hesaplanmış karma numaraların sistemde bazı belgelerin çıktılarıyla birlikte kaydedilmesi için yasal bir gereksinim vardır.</span><span class="sxs-lookup"><span data-stu-id="aa180-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="aa180-105">Karma numaralar, yetkililere rapor verirken ve denetimler sırasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="aa180-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="aa180-106">Bu konu, yazdırılmış müşteri faturalarını karma numaralarla kaydetmek için arşivlemenin nasıl yapılandırılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="aa180-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aa180-107">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="aa180-107">Prerequisites</span></span>

- <span data-ttu-id="aa180-108">**Özellik Yönetimi** çalışma alanında, **yazdırılmış müşteri faturalarını karma numaralarla arşivle** özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="aa180-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="aa180-109">Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="aa180-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="aa180-110">Gerekli belgelerin yazdırılabilir biçimleri **Yazdırma yönetimi**'nde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="aa180-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="aa180-111">Bu işlev aşağıdaki belgeler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="aa180-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="aa180-112">**Alacak hesapları**</span><span class="sxs-lookup"><span data-stu-id="aa180-112">**Accounts receivable**</span></span>
- <span data-ttu-id="aa180-113">Müşteri faturası</span><span class="sxs-lookup"><span data-stu-id="aa180-113">Customer invoice</span></span>
- <span data-ttu-id="aa180-114">Müşteri alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="aa180-114">Customer credit note</span></span>
- <span data-ttu-id="aa180-115">Dekont / Serbest metin faturası</span><span class="sxs-lookup"><span data-stu-id="aa180-115">Free text invoice</span></span>
- <span data-ttu-id="aa180-116">Serbest metinli alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="aa180-116">Free text credit note</span></span>

<span data-ttu-id="aa180-117">**Proje yönetimi ve muhasebe**</span><span class="sxs-lookup"><span data-stu-id="aa180-117">**Project management and accounting**</span></span>
- <span data-ttu-id="aa180-118">Proje faturası</span><span class="sxs-lookup"><span data-stu-id="aa180-118">Project invoice</span></span>
- <span data-ttu-id="aa180-119">Proje alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="aa180-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="aa180-120">Müşteri asıl verisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="aa180-120">Configure customer master data</span></span>
<span data-ttu-id="aa180-121">Müşteri verilerini yapılandırmak ve yazdırılan faturaları otomatik olarak ek olarak kaydetme özelliğini açmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="aa180-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="aa180-122">**Alacak hesapları** > **Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="aa180-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="aa180-123">Müşteri seçin ve **Fatura ve teslimat** hızlı sekmesinde, **E-FATURA** bölümünde **E-Fatura eki** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aa180-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="aa180-124">Faturaları yazdır</span><span class="sxs-lookup"><span data-stu-id="aa180-124">Print invoices</span></span>
<span data-ttu-id="aa180-125">Önceki yordamda yapılandırılan, müşteriye ait serbest metin, müşteri, proje faturası veya alacak dekontunu deftere nakledebilir ve yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa180-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="aa180-126">Yazdırılan fatura için **ekler** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="aa180-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="aa180-127">**Ek** hızlı sekmesinde, **Ek ayrıntılar** alan grubunda, **belge karması numarası** alanında, yazdırılan fatura için hesaplanan kaydedilmiş karma numarayı bulun.</span><span class="sxs-lookup"><span data-stu-id="aa180-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Ek karma numarası](media/attach-hash-num.jpg)


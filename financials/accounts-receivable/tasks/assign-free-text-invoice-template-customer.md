--- 
title: "Müşteriye serbest metin fatura şablonu atama"
description: "Bu görevde, müşteriye serbest metin faturası şablonunun nasıl atanacağı gösterilmektedir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3bcb59c6edd04877dc2a052002be513205ae840a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="7af1c-103">Müşteriye serbest metin fatura şablonu atama</span><span class="sxs-lookup"><span data-stu-id="7af1c-103">Assign a free text invoice template to a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7af1c-104">Bu görevde, müşteriye serbest metin faturası şablonunun nasıl atanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7af1c-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="7af1c-105">USMF demo şirketinin kullanıldığı bu görev, alacak hesapları faturalarının yönetiminden ve işlenmesinden sorumlu kullanıcılara yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="7af1c-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="7af1c-106">Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="7af1c-107">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7af1c-108">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7af1c-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="7af1c-109">Yinelenen faturalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7af1c-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="7af1c-110">Müşterilere serbest metin faturası şablonları atamak ve faturaların müşterilere ne sıklıkta gönderileceğini belirlemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="7af1c-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="7af1c-111">Müşteriye yeni şablon atamak için Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7af1c-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="7af1c-112">Müşteriye atamak istediğiniz serbest metin faturası şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="7af1c-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7af1c-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7af1c-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7af1c-115">İlk faturanın oluşturulacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="7af1c-116">Bir yineleme bitiş tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="7af1c-117">Şunlardan birini seçin: Bitiş tarihi yok – Faturalar sonsuz olarak oluşturulur ve şablon müşteri hesabından kaldırılana kadar geçerli kalır.</span><span class="sxs-lookup"><span data-stu-id="7af1c-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="7af1c-118">Faturalama bitiş tarihi – Bu seçeneği belirtin ve faturanın oluşturulabileceği son tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="7af1c-119">Fatura oluşturmayı sona erdirecek maksimum toplam tutar.</span><span class="sxs-lookup"><span data-stu-id="7af1c-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="7af1c-120">Seçili şablon kullanarak erişilebilen maksimum toplam tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="7af1c-121">Örneğin 1000,00 girer ve her biri 100,00 tutarında aylık faturalar oluşturursanız, onuncu fatura oluşturulduktan sonra fatura oluşturma süreci sona erer.</span><span class="sxs-lookup"><span data-stu-id="7af1c-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="7af1c-122">Serbest metin faturası şablonundan veya müşteri hesabından alınan varsayılan değerleri kullanarak yinelenen faturalar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7af1c-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="7af1c-123">Faturaları oluştururken dil, deftere nakil profili, satış vergisi grubu, madde satış vergisi grubu, liste kodu, teslimat ülkesi/bölgesi, ödeme koşulları, para birimi, ödeme koşulları, ödeme yöntemi, ödeme belirtimi, ödeme planı, nakit iskontosu, mali boyutlar ve havale makbuzu için varsayılan değerleri belirlemek üzere serbest metin faturası şablonunu veya müşteri hesabını kullanın.</span><span class="sxs-lookup"><span data-stu-id="7af1c-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="7af1c-124">Yineleme şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="7af1c-125">Günlük – Bu seçeneği belirtin ve Dönem alanına gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="7af1c-126">Örneğin 15 girerseniz, bu müşteri için 15 günde bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7af1c-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="7af1c-127">Haftalık – Bu seçeneği belirtin Dönem alanına hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="7af1c-128">Örneğin 2 girerseniz, bu müşteri için 2 haftada bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7af1c-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="7af1c-129">Aylık – Bu seçeneği belirtin ve Dönem alanına ay sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="7af1c-130">Örneğin 6 girerseniz, bu müşteri için her altı ayda bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7af1c-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="7af1c-131">Yıllık – Bu seçeneği belirtin ve Dönem alanına yıl sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="7af1c-132">Örneğin 2 girerseniz, bu müşteri için her iki yılda bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7af1c-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="7af1c-133">Dönem alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7af1c-133">In the Per field, enter a number.</span></span>



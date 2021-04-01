---
title: Müşteriye serbest metin faturası şablonu atama
description: Bu görevde, müşteriye serbest metin faturası şablonunun nasıl atanacağı gösterilmektedir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1f87c731a603dbb3def0ebc2d2ebe54f9706053
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254137"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="09a71-103">Müşteriye serbest metin faturası şablonu atama</span><span class="sxs-lookup"><span data-stu-id="09a71-103">Assign a free text invoice template to a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09a71-104">Bu görevde, müşteriye serbest metin faturası şablonunun nasıl atanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="09a71-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="09a71-105">USMF demo şirketinin kullanıldığı bu görev, alacak hesapları faturalarının yönetiminden ve işlenmesinden sorumlu kullanıcılara yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="09a71-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="09a71-106">**Gezinti bölmesinde** **Modüller > Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="09a71-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="09a71-107">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="09a71-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="09a71-108">**Eylem Bölmesinde** **Fatura** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09a71-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="09a71-109">**Yinelenen faturalar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09a71-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="09a71-110">Müşterilere serbest metin faturası şablonları atamak ve faturaların müşterilere ne sıklıkta gönderileceğini belirlemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="09a71-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="09a71-111">Müşteriye yeni şablon atamak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09a71-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="09a71-112">**Şablon** alanında müşteriye atamak istediğiniz serbest metin faturası şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="09a71-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="09a71-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="09a71-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="09a71-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09a71-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="09a71-115">**Faturalama başlangıç tarihi** alanına, ilk faturanın oluşturulacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="09a71-116">**Yinelenme sonu** bölümüne, yinelenen bir bitiş tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="09a71-117">Şunlardan birini seçin: Bitiş tarihi yok – Faturalar sonsuz olarak oluşturulur ve şablon müşteri hesabından kaldırılana kadar geçerli kalır.</span><span class="sxs-lookup"><span data-stu-id="09a71-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="09a71-118">Faturalama bitiş tarihi – Bu seçeneği belirtin ve faturanın oluşturulabileceği son tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="09a71-119">**Maksimum toplam tutar** alanına, fatura oluşturma işleminin durdurulacağı maksimum toplam tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-119">In the **Maximum cumulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="09a71-120">Seçili şablon kullanarak erişilebilen maksimum toplam tutarı girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="09a71-121">Örneğin 1000,00 girer ve her biri 100,00 tutarında aylık faturalar oluşturursanız, onuncu fatura oluşturulduktan sonra fatura oluşturma süreci sona erer.</span><span class="sxs-lookup"><span data-stu-id="09a71-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="09a71-122">**Alınan varsayılan değerleri kullanarak yinelenen faturalar oluştur** bölümünde serbest metin faturası şablonunu veya müşteri hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="09a71-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="09a71-123">Faturaları oluştururken dil, deftere nakil profili, satış vergisi grubu, madde satış vergisi grubu, liste kodu, teslimat ülkesi/bölgesi, ödeme koşulları, para birimi, ödeme koşulları, ödeme yöntemi, ödeme belirtimi, ödeme planı, nakit iskontosu, mali boyutlar ve havale makbuzu için varsayılan değerleri belirlemek üzere serbest metin faturası şablonunu veya müşteri hesabını kullanın.</span><span class="sxs-lookup"><span data-stu-id="09a71-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="09a71-124">**Yineleme modeli** alanında yinelenme modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="09a71-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="09a71-125">Günlük – Bu seçeneği belirtin ve Dönem alanına gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="09a71-126">Örneğin 15 girerseniz, bu müşteri için 15 günde bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="09a71-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="09a71-127">Haftalık – Bu seçeneği belirtin Dönem alanına hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="09a71-128">Örneğin 2 girerseniz, bu müşteri için 2 haftada bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="09a71-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="09a71-129">Aylık – Bu seçeneği belirtin ve Dönem alanına ay sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="09a71-130">Örneğin 6 girerseniz, bu müşteri için her altı ayda bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="09a71-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="09a71-131">Yıllık – Bu seçeneği belirtin ve Dönem alanına yıl sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="09a71-132">Örneğin 2 girerseniz, bu müşteri için her iki yılda bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="09a71-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="09a71-133">**Dönem** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="09a71-133">In the **Per** field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Satıcı ödeme koşullarını tanımlama
description: Bu konu, satıcı faturaları için ödeme koşullarının nasıl ayarlanacağını açıklar.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6a37272694609be14b566dae3c6cf561d4c6d2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227244"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="d0355-103">Satıcı ödeme koşullarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="d0355-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0355-104">Bu konu, satıcı faturaları için ödeme koşullarının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d0355-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="d0355-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d0355-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d0355-106">**Gezinti bölmesi > Modüller > Ödeme tutarı > Ödeme kurulumu > Ödeme şartları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d0355-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="d0355-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d0355-107">Select **New**.</span></span> <span data-ttu-id="d0355-108">Ödeme şartları sayfası, vade tarihinin nasıl hesaplanacağını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d0355-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="d0355-109">Sayfa, nakit iskontosu tarihinin nasıl hesaplanacağını tanımlamak için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="d0355-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="d0355-110">**Ödeme şartları** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d0355-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="d0355-111">**Tanım alanına** bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d0355-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="d0355-112">**Günler** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d0355-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="d0355-113">Buraya girilen sayı; vade tarihine veya Ödeme yöntemi sayfasında tanımlanan dönem sonuna ekleme yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d0355-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="d0355-114">Örneğin, **Net**'i seçerseniz sayı vade tarihine eklenir.</span><span class="sxs-lookup"><span data-stu-id="d0355-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="d0355-115">**Geçerli ay**'ı seçerseniz sayı, geçerli ayın son gününe eklenerek vade tarihi hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d0355-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="d0355-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0355-116">Select **Save**.</span></span>
7. <span data-ttu-id="d0355-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d0355-117">Close the page.</span></span>
8. <span data-ttu-id="d0355-118">**Borç hesapları > Ödeme kurulumu > Nakit iskontoları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d0355-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="d0355-119">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d0355-119">Select **New**.</span></span>
10. <span data-ttu-id="d0355-120">**Nakit iskontosu** alanına bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="d0355-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="d0355-121">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d0355-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="d0355-122">Satıcı katmanlı bir iskonto teklif ederse, geçerli nakit iskontosunun süresi dolduktan sonraki nakit iskontosunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d0355-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="d0355-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d0355-123">Close the page.</span></span>
14. <span data-ttu-id="d0355-124">**Günler** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d0355-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="d0355-125">**Gün** alanına girilen değer, **Net/Geçerli** alanındaki seçime bağlı olarak, Nakit iskontosu tarihini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d0355-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="d0355-126">**Net** seçildiyse nakit iskontosu tarihini belirlemek için fatura tarihine bu değer eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="d0355-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="d0355-127">**Geçerli ay** seçildiyse nakit iskontosu tarihini belirlemek için geçerli ayın sonuna bu değer eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="d0355-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="d0355-128">**İskonto** alanına nakit iskontosunun yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="d0355-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="d0355-129">Müşteri faturaları için nakit iskontosunun nakledileceği ana hesabı girin ve sonra nakit iskontosunun satıcı faturaları için nakledileceği ana hesabı girin.</span><span class="sxs-lookup"><span data-stu-id="d0355-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="d0355-130">**İskonto mahsup hesapları** ayarı **Satıcı iskontosu için ana hesabı kullan** ayarlanırsa Ana hesap kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d0355-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="d0355-131">Seçenek **Fatura satırlarındaki hesaplar** olarak ayarlanırsa nakit iskontosu, fatura satırlarındaki kıymet/gider hesaplarına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="d0355-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="d0355-132">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0355-132">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
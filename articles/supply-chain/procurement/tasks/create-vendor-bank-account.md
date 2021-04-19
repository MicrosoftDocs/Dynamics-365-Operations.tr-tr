---
title: Satıcı banka hesabı oluşturma
description: Bu prosedür, bir satıcının banka hesabının nasıl oluşturulacağını gösterir.
author: kamaybac
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fcf15d798d2ca8e1d36556fbe2c9603f12d2b03
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812026"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="eeb63-103">Satıcı banka hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="eeb63-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eeb63-104">Bu prosedür, bir satıcının banka hesabının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eeb63-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="eeb63-105">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eeb63-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="eeb63-106">**Gezinti Bölmesi > Modüller > Tedarik ve kaynak atama > Satıcılar > Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="eeb63-107">Banka hesabını oluşturmak istediğiniz satıcıyı seçin ve sonra **Satıcı hesap kodundaki** alanındaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="eeb63-108">**Eylem Bölmesi**'nde, **Satıcı**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-108">On the **Action Pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="eeb63-109">**Banka hesapları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="eeb63-110">**Eylem Bölmesi**'nde **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-110">On the **Action Pane**, click **New**.</span></span>
6. <span data-ttu-id="eeb63-111">**Banka hesabı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="eeb63-112">Bu kimlik satıcı kaydı üzerinden banka hesabını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eeb63-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="eeb63-113">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="eeb63-114">**Banka grupları** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="eeb63-115">**Rota numarası türü** alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="eeb63-116">Bu uluslararası ödemeler için kullanılan rota numarası türüdür.</span><span class="sxs-lookup"><span data-stu-id="eeb63-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="eeb63-117">**Banka hesabı numarası** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="eeb63-118">**SWIFT kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="eeb63-119">**IBAN** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="eeb63-120">IBAN numarası doğru biçimde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="eeb63-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="eeb63-121">Örneğin, DE89370400440532013000'ı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eeb63-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="eeb63-122">Etkin tarihe ulaşılmışsa banka hesabının durumu Etkin'dir ve Bitiş tarihi geçmemiştir.</span><span class="sxs-lookup"><span data-stu-id="eeb63-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="eeb63-123">Ayrıca, Etkin tarih ve Bitiş tarihi alanları boşsa da etkindir.</span><span class="sxs-lookup"><span data-stu-id="eeb63-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="eeb63-124">Etkin tarih ve Bitiş tarihi alanlarının her ikisindeki tarihler gelecekteyse, elektronik ödemeler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="eeb63-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="eeb63-125">Diğer ödeme tipleri kullanılabilir ve banka hesabı etkindir.</span><span class="sxs-lookup"><span data-stu-id="eeb63-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="eeb63-126">**Kurulum** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="eeb63-127">**Metin kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="eeb63-128">Bu alan, alıcının banka ekstresinde görünecek bir kod belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb63-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="eeb63-129">**Bankaya ileti** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="eeb63-130">**Döviz kuru referansı** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="eeb63-131">Bu gelecek veya sabit dönemli döviz kuru için referans numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="eeb63-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="eeb63-132">**Para birimi** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="eeb63-133">Bu bölümde açık provizyonlar düzenlenirken durum özeti verilir (beklemede veya onaylanmış).</span><span class="sxs-lookup"><span data-stu-id="eeb63-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="eeb63-134">**Adres** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="eeb63-135">**Açık provizyonlar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="eeb63-136">**İletişim bilgileri** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="eeb63-137">**Telefon** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="eeb63-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-138">Close the page.</span></span>
23. <span data-ttu-id="eeb63-139">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-139">Click **Edit**.</span></span>
24. <span data-ttu-id="eeb63-140">**Ödeme** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="eeb63-141">**Banka hesabı** alanında, yeni oluşturduğunuz hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="eeb63-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="eeb63-142">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eeb63-142">Click **Save**.</span></span> <span data-ttu-id="eeb63-143">Belirtilmişse adres banka grubundan devralınabilir veya buradan ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eeb63-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
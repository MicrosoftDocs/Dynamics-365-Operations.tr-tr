---
title: Teminat mektupları için banka hizmetlerini ve banka deftere nakil profillerini ayarlama
description: Bu görev, garanti mektubu işlemek için gereken banka tesisi ve deftere nakil profilini oluşturur.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b72a412aaaf1c70b4414d00e99b923380f7dd86
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225309"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="69d31-103">Teminat mektupları için banka hizmetlerini ve banka deftere nakil profillerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="69d31-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69d31-104">Bu görev, garanti mektubu işlemek için gereken banka tesisi ve deftere nakil profilini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69d31-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="69d31-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="69d31-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="69d31-106">Genel muhasebe defteri parametresi</span><span class="sxs-lookup"><span data-stu-id="69d31-106">General ledger parameter</span></span>
1. <span data-ttu-id="69d31-107">Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.</span><span class="sxs-lookup"><span data-stu-id="69d31-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="69d31-108">Banka belgesi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="69d31-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="69d31-109">Teminat mektubunu etkinleştirme seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="69d31-110">Dönüştürme günlüğü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="69d31-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="69d31-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="69d31-113">Numara serileri sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69d31-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="69d31-114">Teminat mektubu numarası ve teminat mektubu hareket referansı için sayı sıra numarası kodunu tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="69d31-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-115">Click Save.</span></span>
9. <span data-ttu-id="69d31-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69d31-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="69d31-117">Banka hizmeti yarat</span><span class="sxs-lookup"><span data-stu-id="69d31-117">Create Bank facility</span></span>
1. <span data-ttu-id="69d31-118">Nakit ve Banka yönetimi > Kurulum > Banka tesisleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="69d31-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="69d31-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-119">Click New.</span></span>
3. <span data-ttu-id="69d31-120">Tesis grubu alanına, teminat mektubu hareketi için banka tesisi grup adını girin.</span><span class="sxs-lookup"><span data-stu-id="69d31-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="69d31-121">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="69d31-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="69d31-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-122">Click Save.</span></span>
6. <span data-ttu-id="69d31-123">Tesis türleri sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69d31-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="69d31-124">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-124">Click New.</span></span>
8. <span data-ttu-id="69d31-125">Tesis türü alanında, banka tesisi anlaşmasıyla ilişkili banka tesisi türünün adını girin.</span><span class="sxs-lookup"><span data-stu-id="69d31-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="69d31-126">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="69d31-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="69d31-127">Tesis grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="69d31-128">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="69d31-129">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="69d31-130">Tesis niteliği alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="69d31-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-131">Click Save.</span></span>
15. <span data-ttu-id="69d31-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69d31-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="69d31-133">Banka nakil profili</span><span class="sxs-lookup"><span data-stu-id="69d31-133">Bank posting profile</span></span>
1. <span data-ttu-id="69d31-134">Nakit ve Banka yönetimi > Kurulum > Banka belgesi nakletme profili seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="69d31-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="69d31-135">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-135">Click New.</span></span>
3. <span data-ttu-id="69d31-136">Hesap/Grup numarası alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69d31-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="69d31-137">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="69d31-138">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69d31-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="69d31-139">Hesabı kapatma alanında, hesap kapatma için ana hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="69d31-140">Gider hesabı alanında masraf hareketleri hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="69d31-141">Marj hesabı alanında, marj hareketi hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="69d31-142">Tasfiye hesabı alanında, teminat mektubu hareketi için tasfiye hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="69d31-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="69d31-143">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69d31-143">Click Save.</span></span>
11. <span data-ttu-id="69d31-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="69d31-144">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
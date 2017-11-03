--- 
title: "Kredi mektubu için banka hizmetlerini ve banka deftere nakil profillerini ayarlama"
description: "Bu yordam, akreditif mektubunu işlemek için gerekli olan banka tesisi ve nakletme profilini oluşturmayı gösterir."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 43422627f8529768ab9377c04568da531d6565c6
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="08d13-103">Kredi mektubu için banka hizmetlerini ve banka deftere nakil profillerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="08d13-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08d13-104">Bu yordam, akreditif mektubunu işlemek için gerekli olan banka tesisi ve nakletme profilini oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="08d13-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="08d13-105">Bu görevler, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="08d13-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="08d13-106">Genel muhasebe defteri parametresi</span><span class="sxs-lookup"><span data-stu-id="08d13-106">General ledger parameter</span></span>
1. <span data-ttu-id="08d13-107">Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.</span><span class="sxs-lookup"><span data-stu-id="08d13-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="08d13-108">Banka belgesi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="08d13-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="08d13-109">Akreditif mektubunu içeri alma seçeneğini etkinleştir'i seçin.</span><span class="sxs-lookup"><span data-stu-id="08d13-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="08d13-110">Akreditif mektubunu dışarıya verme seçeneğini etkinleştir'i seçin.</span><span class="sxs-lookup"><span data-stu-id="08d13-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="08d13-111">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-111">Click Save.</span></span>
6. <span data-ttu-id="08d13-112">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="08d13-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="08d13-113">Banka hizmeti yarat</span><span class="sxs-lookup"><span data-stu-id="08d13-113">Create Bank facility</span></span>
1. <span data-ttu-id="08d13-114">Nakit ve Banka yönetimi > Kurulum > Banka tesisleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="08d13-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="08d13-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-115">Click New.</span></span>
3. <span data-ttu-id="08d13-116">Tesis grubu alanında, banka tesisi grup adını girin.</span><span class="sxs-lookup"><span data-stu-id="08d13-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="08d13-117">Tanım alanında, banka tesisi grup tanımını girin.</span><span class="sxs-lookup"><span data-stu-id="08d13-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="08d13-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-118">Click Save.</span></span>
6. <span data-ttu-id="08d13-119">Tesis türleri sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08d13-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="08d13-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-120">Click New.</span></span>
8. <span data-ttu-id="08d13-121">Tesis türü alanına benzersiz bir kod yazın.</span><span class="sxs-lookup"><span data-stu-id="08d13-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="08d13-122">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="08d13-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="08d13-123">Tesis grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="08d13-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="08d13-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="08d13-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="08d13-126">Tesis niteliği alanında banka tesisinin niteliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="08d13-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="08d13-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-127">Click Save.</span></span>
15. <span data-ttu-id="08d13-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="08d13-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="08d13-129">Banka nakil profili</span><span class="sxs-lookup"><span data-stu-id="08d13-129">Bank posting profile</span></span>
1. <span data-ttu-id="08d13-130">Nakit ve Banka yönetimi > Kurulum > Banka belgesi nakletme profili seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="08d13-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="08d13-131">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-131">Click New.</span></span>
3. <span data-ttu-id="08d13-132">Hesap/Grup numarası alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08d13-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="08d13-133">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="08d13-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="08d13-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="08d13-135">Hesap kesme için ana hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="08d13-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="08d13-136">Nakit akışı tahminini hesaplarken bu hesap kullanılır.</span><span class="sxs-lookup"><span data-stu-id="08d13-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="08d13-137">Gider hesabı alanında masraf hareketleri hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="08d13-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="08d13-138">Marj hesabı alanında marj hareketleri hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="08d13-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="08d13-139">Bu hesaba açılış marjı nakledilirken alacak, ödeme nakledilirken ise borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="08d13-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="08d13-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08d13-140">Click Save.</span></span>


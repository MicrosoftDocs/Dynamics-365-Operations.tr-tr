--- 
title: " Kredi kartı işlemlerini yapılandırma"
description: "Bu yordam, ödeme sağlayıcılarının listesini görüntüleme ve alacak hesapları için bir ödeme hesabı yapılandırmayla ilgili açıklama sağlar."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8e7bfbf6b51aca9cf8a7f800ac7db22c0330d00
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="f30f9-103"> Kredi kartı işlemlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f30f9-103">Configure credit card processing</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f30f9-104">Bu yordam, ödeme sağlayıcılarının listesini görüntüleme ve alacak hesapları için bir ödeme hesabı yapılandırmayla ilgili açıklama sağlar.</span><span class="sxs-lookup"><span data-stu-id="f30f9-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="f30f9-105">Bu yordam demo veride USRT şirketini kullanır ve Yöneticiler ile BT Uzmanları için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f30f9-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="f30f9-106">Ödeme sağlayıcıların listesini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="f30f9-106">View a list of payment providers</span></span>
1. <span data-ttu-id="f30f9-107">Accounts receivable > Payments setup > Payment services (Alacak hesapları > Ödeme kurulumu > Ödeme hizmetleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="f30f9-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="f30f9-108">Kullanılabilir sağlayıcıları görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="f30f9-109">Ödeme hesabını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f30f9-109">Configure payment account</span></span>
1. <span data-ttu-id="f30f9-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-110">Click New.</span></span>
2. <span data-ttu-id="f30f9-111">Ödeme hizmeti alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="f30f9-112">Ödeme bağlayıcısı alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f30f9-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="f30f9-113">Ödeme hizmeti hesap bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="f30f9-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="f30f9-114">Ortam: alanına 'PROD' yazın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="f30f9-115">Kredi kartı türleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-115">Click Credit card types.</span></span>
7. <span data-ttu-id="f30f9-116">Ödeme günlüğü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f30f9-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f30f9-118">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-118">Click Add.</span></span>
10. <span data-ttu-id="f30f9-119">Para birimi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="f30f9-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f30f9-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f30f9-121">Ödeme günlüğü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f30f9-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f30f9-123">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-123">Click Add.</span></span>
15. <span data-ttu-id="f30f9-124">Para birimi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="f30f9-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f30f9-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f30f9-126">Bu adımları gerekli olan kart türleri için istediğiniz kadar tekrarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f30f9-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="f30f9-127">Ödeme günlüğü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="f30f9-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="f30f9-129">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-129">Click Add.</span></span>
20. <span data-ttu-id="f30f9-130">Para birimi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="f30f9-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-131">Click Save.</span></span>
22. <span data-ttu-id="f30f9-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-132">Close the page.</span></span>
23. <span data-ttu-id="f30f9-133">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-133">Click Validate.</span></span>
24. <span data-ttu-id="f30f9-134">Yeni kredi kartları için varsayılan işlemci onay kutusuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="f30f9-135">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f30f9-135">Click Save.</span></span>



--- 
title: " Perakende mağazasına yönelik bir ekstre oluşturma, hesaplama ve deftere nakletme"
description: "Bu yordam bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımlarını açıklar."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 33ebb28196baa9ae944dbd124274b05cb587fea4
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="80cd8-103"> Perakende mağazasına yönelik bir ekstre oluşturma, hesaplama ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="80cd8-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="80cd8-104">Bu yordam bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="80cd8-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="80cd8-105">Aynı görevler için yapılandırılabilecek toplu işler de vardır.</span><span class="sxs-lookup"><span data-stu-id="80cd8-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="80cd8-106">Toplu işleri yapılandırma ve çalıştırmayla ilgili adımlar diğer konularda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="80cd8-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="80cd8-107">Bu yordamı tamamlamak için POS'ta tamamlanan ve ardından Dynamics AX uygulamasına çekilen hareketleriniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="80cd8-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="80cd8-108">Bu kayıt USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="80cd8-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="80cd8-109">Bu yordam, Microsoft Dynamics AX'e başvuru içerebilir.</span><span class="sxs-lookup"><span data-stu-id="80cd8-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="80cd8-110">Dynamics AX'in artık Microsoft Dynamics 365 for Operations olarak adlandırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="80cd8-111">Tüm çalışma alanları > ..</span><span class="sxs-lookup"><span data-stu-id="80cd8-111">Go to All workspaces > ..</span></span> <span data-ttu-id="80cd8-112">> Perakende mağazası mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="80cd8-112">> Retail store financials.</span></span>
2. <span data-ttu-id="80cd8-113">Yeni ekstre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-113">Click New statement.</span></span>
3. <span data-ttu-id="80cd8-114">Mağaza numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="80cd8-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="80cd8-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-116">Click OK.</span></span>
    * <span data-ttu-id="80cd8-117">Kurulum grubunda, ekstreye hangi hareketlerin dahil edileceğini ve bunların ekstre satırlarında nasıl gruplandırılacağını denetleyen ayarlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="80cd8-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="80cd8-118">Kurulum grubunu açarak bu ayarları değiştirebilir veya varsayılanları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="80cd8-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="80cd8-119">Ekstre yöntemi alanı ekstre satırlarının nasıl gruplandırılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80cd8-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="80cd8-120">Ekstreyi yalnızca belirli bir personel üyesi ya da kayıt için hesaplamak istiyorsanız bir personel üyesi veya kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="80cd8-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="80cd8-121">Kapanış yöntemi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="80cd8-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="80cd8-122">Ekstreyi hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="80cd8-123">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-123">Click Yes.</span></span>
    * <span data-ttu-id="80cd8-124">Ekstreyi hesaplandıktan sonra, kullanılan her ödeme ve ekstre yöntemi için toplam tutarları içeren satırlar oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="80cd8-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="80cd8-125">Girilmesi veya güncelleştirilmesi gerekiyorsa her satıra sayılmış bir tutar girin.</span><span class="sxs-lookup"><span data-stu-id="80cd8-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="80cd8-126">Sayılan alanı POS'ta yapılan kasa sayımlarından alınan tutarlarla doldurulur.</span><span class="sxs-lookup"><span data-stu-id="80cd8-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="80cd8-127">Ekstreyi deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-127">Click Post statement.</span></span>
10. <span data-ttu-id="80cd8-128">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-128">Click Close.</span></span>
11. <span data-ttu-id="80cd8-129">Perakende ve ticaret > Kanallar > Perakende mağaza finansmanları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="80cd8-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="80cd8-130">Deftere nakledilen ekstreler sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80cd8-130">Click the Posted statements tab.</span></span>



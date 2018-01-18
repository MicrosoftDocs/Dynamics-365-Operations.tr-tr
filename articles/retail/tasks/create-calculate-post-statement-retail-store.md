--- 
title: " Perakende mağazasına yönelik bir ekstre oluşturma, hesaplama ve deftere nakletme"
description: "Bu yordam bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımlarını açıklar."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
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
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: d29f89b1ee65523e59aafd7d43465b1e4c3b8a36
ms.contentlocale: tr-tr
ms.lasthandoff: 01/18/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="a4130-103"> Perakende mağazasına yönelik bir ekstre oluşturma, hesaplama ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="a4130-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a4130-104">Bu yordam bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="a4130-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="a4130-105">Aynı görevler için yapılandırılabilecek toplu işler de vardır.</span><span class="sxs-lookup"><span data-stu-id="a4130-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="a4130-106">Toplu işleri yapılandırma ve çalıştırmayla ilgili adımlar diğer konularda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="a4130-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="a4130-107">Bu yordamı tamamlamak için POS'ta tamamlanan ve ardından Dynamics AX uygulamasına çekilen hareketleriniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a4130-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="a4130-108">Bu kayıt USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a4130-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="a4130-109">Bu yordam, Microsoft Dynamics AX'e başvuru içerebilir.</span><span class="sxs-lookup"><span data-stu-id="a4130-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="a4130-110">Dynamics AX'in artık Microsoft Dynamics 365 for Operations olarak adlandırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="a4130-111">Tüm çalışma alanları > ..</span><span class="sxs-lookup"><span data-stu-id="a4130-111">Go to All workspaces > ..</span></span> <span data-ttu-id="a4130-112">> Perakende mağazası mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a4130-112">> Retail store financials.</span></span>
2. <span data-ttu-id="a4130-113">Yeni ekstre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-113">Click New statement.</span></span>
3. <span data-ttu-id="a4130-114">Mağaza numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a4130-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a4130-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-116">Click OK.</span></span>
    * <span data-ttu-id="a4130-117">Kurulum grubunda, ekstreye hangi hareketlerin dahil edileceğini ve bunların ekstre satırlarında nasıl gruplandırılacağını denetleyen ayarlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="a4130-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="a4130-118">Kurulum grubunu açarak bu ayarları değiştirebilir veya varsayılanları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4130-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="a4130-119">Ekstre yöntemi alanı ekstre satırlarının nasıl gruplandırılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4130-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="a4130-120">Ekstreyi yalnızca belirli bir personel üyesi ya da kayıt için hesaplamak istiyorsanız bir personel üyesi veya kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="a4130-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="a4130-121">Kapanış yöntemi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="a4130-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="a4130-122">Ekstreyi hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="a4130-123">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4130-123">Click Yes.</span></span>
    * <span data-ttu-id="a4130-124">Ekstreyi hesaplandıktan sonra, kullanılan her ödeme ve ekstre yöntemi için toplam tutarları içeren satırlar oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a4130-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="a4130-125">Girilmesi veya güncelleştirilmesi gerekiyorsa her satıra sayılmış bir tutar girin.</span><span class="sxs-lookup"><span data-stu-id="a4130-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="a4130-126">Sayılan alanı POS'ta yapılan kasa sayımlarından alınan tutarlarla doldurulur.</span><span class="sxs-lookup"><span data-stu-id="a4130-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="a4130-127">Ekstreyi deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-127">Click Post statement.</span></span>
10. <span data-ttu-id="a4130-128">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-128">Click Close.</span></span>
11. <span data-ttu-id="a4130-129">Perakende ve ticaret > Kanallar > Perakende mağaza finansmanları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a4130-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="a4130-130">Deftere nakledilen ekstreler sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4130-130">Click the Posted statements tab.</span></span>



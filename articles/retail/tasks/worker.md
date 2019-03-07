---
title: " Çalışanı yapılandırma"
description: Bu yordam bir perakende çalışanını POS'ta satışlar üzerinden komisyon için uygun bir satış temsilcisi olarak yapılandırmayı gösterir.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 797640b487884fc487582addea274007e4ba7a7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "362545"
---
# <a name="configure-a-worker"></a><span data-ttu-id="4ce24-103"> Çalışanı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4ce24-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4ce24-104">Bu yordam bir perakende çalışanını POS'ta satışlar üzerinden komisyon için uygun bir satış temsilcisi olarak yapılandırmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ce24-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="4ce24-105">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4ce24-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="4ce24-106">Çalışan için komisyon satış grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="4ce24-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="4ce24-107">Satış ve pazarlama > Komisyonlar > Satış grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4ce24-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="4ce24-108">Çalışanlar bir veya daha fazla satış grubuna atanabilir.</span><span class="sxs-lookup"><span data-stu-id="4ce24-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="4ce24-109">POS'ta, mağazanın adres defterinden çalışanları içeren herhangi bir satış grubunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ce24-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="4ce24-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-110">Click New.</span></span>
3. <span data-ttu-id="4ce24-111">Grup alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4ce24-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="4ce24-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4ce24-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-113">Click Save.</span></span>
6. <span data-ttu-id="4ce24-114">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="4ce24-115">Satış temsilcisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-115">Click Sales rep.</span></span>
    * <span data-ttu-id="4ce24-116">Satış grubu birden fazla çalışan içerebilir.</span><span class="sxs-lookup"><span data-stu-id="4ce24-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="4ce24-117">Komisyonlar, komisyon hissesini nasıl tanımladığınıza bağlı olarak çalışanlar arasında bölünebilir.</span><span class="sxs-lookup"><span data-stu-id="4ce24-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="4ce24-118">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="4ce24-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="4ce24-119">Komisyon hissesi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4ce24-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="4ce24-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-120">Click Save.</span></span>
11. <span data-ttu-id="4ce24-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-121">Close the page.</span></span>
12. <span data-ttu-id="4ce24-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="4ce24-123">Çalışanlar varsayılan satış grubunu atama</span><span class="sxs-lookup"><span data-stu-id="4ce24-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="4ce24-124">Retail and commerce > Employees > Workers (Perakende ve ticaret > Personel > Çalışanlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="4ce24-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="4ce24-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4ce24-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4ce24-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4ce24-127">Perakende sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="4ce24-128">Çalışan varsayılan bir satış grubuna atanabilir.</span><span class="sxs-lookup"><span data-stu-id="4ce24-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="4ce24-129">Mağazanın işlevsellik profilinde seçenek etkinleştirilmişse varsayılan satış grubu POS'ta satış satırlarına otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="4ce24-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="4ce24-130">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-130">Click Edit.</span></span>
6. <span data-ttu-id="4ce24-131">Varsayılan grup alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="4ce24-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="4ce24-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ce24-132">Click Save.</span></span>


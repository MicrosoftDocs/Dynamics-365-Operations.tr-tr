--- 
title: " Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma"
description: "Bu yordam, boyut değerleriyle bir perakende kanalı mali boyutu oluşturma konusunu ve perakende mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3782d5d2a43b6b22a6f5b25c806e9d4bba5999a5
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="1c8ab-103"> Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1c8ab-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1c8ab-104">Bu yordam, boyut değerleriyle bir perakende kanalı mali boyutu oluşturma konusunu ve perakende mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="1c8ab-105">Konu, boyut kümeleri ve hesap yapıları oluşturmak gibi diğer ilgili adımları içermez.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="1c8ab-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="1c8ab-107">General ledger > Chart of accounts > Dimensions > Financial dimensions (Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="1c8ab-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-108">Click New.</span></span>
3. <span data-ttu-id="1c8ab-109">Şuradan alınan değerleri kullan alanında 'Perakende kanalları'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="1c8ab-110">Boyut adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="1c8ab-111">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-111">Click Activate.</span></span>
6. <span data-ttu-id="1c8ab-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-112">Click Close.</span></span>
7. <span data-ttu-id="1c8ab-113">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-113">Click Activate.</span></span>
8. <span data-ttu-id="1c8ab-114">Boyut değerlerini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-114">Click Dimension values.</span></span>
9. <span data-ttu-id="1c8ab-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-115">Close the page.</span></span>
10. <span data-ttu-id="1c8ab-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-116">Click Save.</span></span>
11. <span data-ttu-id="1c8ab-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-117">Close the page.</span></span>
12. <span data-ttu-id="1c8ab-118">Retail and commerce > Channels > Retail stores > All retail stores (Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="1c8ab-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1c8ab-120">Finansal boyutlar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="1c8ab-121">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-121">Click Edit.</span></span>
16. <span data-ttu-id="1c8ab-122">Retailchannel alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="1c8ab-123">Listede, güncelleştirilecek mağazaya ilişkin boyut değerini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="1c8ab-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="1c8ab-125">CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="1c8ab-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="1c8ab-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="1c8ab-128">Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="1c8ab-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="1c8ab-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="1c8ab-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c8ab-131">Click Save.</span></span>



--- 
title: "Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma"
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: cf32d17a36fd699141ce697d23e20b2eb5cbfa54
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="f2dc7-103">Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f2dc7-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f2dc7-104">Bu yordam, boyut değerleriyle bir perakende kanalı mali boyutu oluşturma konusunu ve perakende mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="f2dc7-105">Konu, boyut kümeleri ve hesap yapıları oluşturmak gibi diğer ilgili adımları içermez.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="f2dc7-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f2dc7-107">General ledger > Chart of accounts > Dimensions > Financial dimensions (Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="f2dc7-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-108">Click New.</span></span>
3. <span data-ttu-id="f2dc7-109">Şuradan alınan değerleri kullan alanında 'Perakende kanalları'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="f2dc7-110">Boyut adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="f2dc7-111">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-111">Click Activate.</span></span>
6. <span data-ttu-id="f2dc7-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-112">Click Close.</span></span>
7. <span data-ttu-id="f2dc7-113">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-113">Click Activate.</span></span>
8. <span data-ttu-id="f2dc7-114">Boyut değerlerini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-114">Click Dimension values.</span></span>
9. <span data-ttu-id="f2dc7-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-115">Close the page.</span></span>
10. <span data-ttu-id="f2dc7-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-116">Click Save.</span></span>
11. <span data-ttu-id="f2dc7-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-117">Close the page.</span></span>
12. <span data-ttu-id="f2dc7-118">Retail and commerce > Channels > Retail stores > All retail stores (Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="f2dc7-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f2dc7-120">Finansal boyutlar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="f2dc7-121">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-121">Click Edit.</span></span>
16. <span data-ttu-id="f2dc7-122">Retailchannel alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="f2dc7-123">Listede, güncelleştirilecek mağazaya ilişkin boyut değerini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="f2dc7-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="f2dc7-125">CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="f2dc7-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="f2dc7-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="f2dc7-128">Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="f2dc7-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="f2dc7-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="f2dc7-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f2dc7-131">Click Save.</span></span>



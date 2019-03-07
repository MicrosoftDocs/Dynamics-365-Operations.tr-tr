---
title: Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma
description: Bu yordam, boyut değerleriyle bir perakende kanalı mali boyutu oluşturma konusunu ve perakende mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf32d17a36fd699141ce697d23e20b2eb5cbfa54
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "354541"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="54e2a-103">Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="54e2a-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="54e2a-104">Bu yordam, boyut değerleriyle bir perakende kanalı mali boyutu oluşturma konusunu ve perakende mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="54e2a-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="54e2a-105">Konu, boyut kümeleri ve hesap yapıları oluşturmak gibi diğer ilgili adımları içermez.</span><span class="sxs-lookup"><span data-stu-id="54e2a-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="54e2a-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="54e2a-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="54e2a-107">General ledger > Chart of accounts > Dimensions > Financial dimensions (Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="54e2a-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="54e2a-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-108">Click New.</span></span>
3. <span data-ttu-id="54e2a-109">Şuradan alınan değerleri kullan alanında 'Perakende kanalları'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="54e2a-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="54e2a-110">Boyut adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="54e2a-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="54e2a-111">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-111">Click Activate.</span></span>
6. <span data-ttu-id="54e2a-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-112">Click Close.</span></span>
7. <span data-ttu-id="54e2a-113">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-113">Click Activate.</span></span>
8. <span data-ttu-id="54e2a-114">Boyut değerlerini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-114">Click Dimension values.</span></span>
9. <span data-ttu-id="54e2a-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-115">Close the page.</span></span>
10. <span data-ttu-id="54e2a-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-116">Click Save.</span></span>
11. <span data-ttu-id="54e2a-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-117">Close the page.</span></span>
12. <span data-ttu-id="54e2a-118">Retail and commerce > Channels > Retail stores > All retail stores (Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="54e2a-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="54e2a-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="54e2a-120">Finansal boyutlar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="54e2a-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="54e2a-121">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-121">Click Edit.</span></span>
16. <span data-ttu-id="54e2a-122">Retailchannel alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="54e2a-123">Listede, güncelleştirilecek mağazaya ilişkin boyut değerini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="54e2a-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="54e2a-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="54e2a-125">CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="54e2a-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="54e2a-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="54e2a-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="54e2a-128">Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="54e2a-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="54e2a-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="54e2a-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="54e2a-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54e2a-131">Click Save.</span></span>


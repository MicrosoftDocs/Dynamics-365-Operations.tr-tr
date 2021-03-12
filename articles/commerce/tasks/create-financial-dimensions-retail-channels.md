---
title: Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma
description: Bu yordam, boyut değerleriyle bir Commerce kanalı mali boyutu oluşturma konusunu ve mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86fc9c9a400bee1280b32f10b1e8f55e581e1984
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964757"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="3034b-103">Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3034b-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3034b-104">Bu yordam, boyut değerleriyle bir Commerce kanalı mali boyutu oluşturma konusunu ve mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="3034b-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="3034b-105">Konu, boyut kümeleri ve hesap yapıları oluşturmak gibi diğer ilgili adımları içermez.</span><span class="sxs-lookup"><span data-stu-id="3034b-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="3034b-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3034b-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3034b-107">General ledger > Chart of accounts > Dimensions > Financial dimensions (Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="3034b-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="3034b-108">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3034b-108">Click New.</span></span>
3. <span data-ttu-id="3034b-109">Şuradan alınan değerleri kullan alanında "Commerce kanalları"nı seçin.</span><span class="sxs-lookup"><span data-stu-id="3034b-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="3034b-110">Boyut adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3034b-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="3034b-111">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3034b-111">Click Activate.</span></span>
6. <span data-ttu-id="3034b-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-112">Click Close.</span></span>
7. <span data-ttu-id="3034b-113">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3034b-113">Click Activate.</span></span>
8. <span data-ttu-id="3034b-114">Boyut değerlerini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3034b-114">Click Dimension values.</span></span>
9. <span data-ttu-id="3034b-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3034b-115">Close the page.</span></span>
10. <span data-ttu-id="3034b-116">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3034b-116">Click Save.</span></span>
11. <span data-ttu-id="3034b-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3034b-117">Close the page.</span></span>
12. <span data-ttu-id="3034b-118">Perakende ve Ticaret > Kanallar > Mağazalar > Tüm mağazalar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3034b-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="3034b-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3034b-120">Finansal boyutlar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="3034b-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="3034b-121">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-121">Click Edit.</span></span>
16. <span data-ttu-id="3034b-122">Commerce kanalı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="3034b-123">Listede, güncelleştirilecek mağazaya ilişkin boyut değerini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3034b-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="3034b-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="3034b-125">CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="3034b-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3034b-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="3034b-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="3034b-128">Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="3034b-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3034b-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="3034b-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="3034b-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3034b-131">Click Save.</span></span>


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
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea36732023092f714b3a783d98b512c0fea7dade
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141419"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="1c822-103">Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1c822-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c822-104">Bu yordam, boyut değerleriyle bir Commerce kanalı mali boyutu oluşturma konusunu ve mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="1c822-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="1c822-105">Konu, boyut kümeleri ve hesap yapıları oluşturmak gibi diğer ilgili adımları içermez.</span><span class="sxs-lookup"><span data-stu-id="1c822-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="1c822-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1c822-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="1c822-107">General ledger > Chart of accounts > Dimensions > Financial dimensions (Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1c822-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="1c822-108">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c822-108">Click New.</span></span>
3. <span data-ttu-id="1c822-109">Şuradan alınan değerleri kullan alanında "Commerce kanalları"nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1c822-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="1c822-110">Boyut adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1c822-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="1c822-111">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c822-111">Click Activate.</span></span>
6. <span data-ttu-id="1c822-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-112">Click Close.</span></span>
7. <span data-ttu-id="1c822-113">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c822-113">Click Activate.</span></span>
8. <span data-ttu-id="1c822-114">Boyut değerlerini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c822-114">Click Dimension values.</span></span>
9. <span data-ttu-id="1c822-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c822-115">Close the page.</span></span>
10. <span data-ttu-id="1c822-116">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c822-116">Click Save.</span></span>
11. <span data-ttu-id="1c822-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c822-117">Close the page.</span></span>
12. <span data-ttu-id="1c822-118">Perakende ve Ticaret > Kanallar > Mağazalar > Tüm mağazalar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1c822-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="1c822-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1c822-120">Finansal boyutlar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="1c822-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="1c822-121">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-121">Click Edit.</span></span>
16. <span data-ttu-id="1c822-122">Commerce kanalı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="1c822-123">Listede, güncelleştirilecek mağazaya ilişkin boyut değerini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1c822-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="1c822-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="1c822-125">CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="1c822-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1c822-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="1c822-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="1c822-128">Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="1c822-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1c822-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="1c822-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="1c822-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c822-131">Click Save.</span></span>


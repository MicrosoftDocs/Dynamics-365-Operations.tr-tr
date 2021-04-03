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
ms.openlocfilehash: 5250e93757560f4a0f76897e3dd1374d14ff5e60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264272"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="8726e-103">Perakende kanalları için mali boyutlar oluşturma ve mağazalardaki boyut değerlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8726e-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8726e-104">Bu yordam, boyut değerleriyle bir Commerce kanalı mali boyutu oluşturma konusunu ve mağazalarda mali boyut değerleri yapılandırma adımlarını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="8726e-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="8726e-105">Konu, boyut kümeleri ve hesap yapıları oluşturmak gibi diğer ilgili adımları içermez.</span><span class="sxs-lookup"><span data-stu-id="8726e-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="8726e-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8726e-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8726e-107">General ledger > Chart of accounts > Dimensions > Financial dimensions (Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="8726e-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="8726e-108">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8726e-108">Click New.</span></span>
3. <span data-ttu-id="8726e-109">Şuradan alınan değerleri kullan alanında "Commerce kanalları"nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8726e-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="8726e-110">Boyut adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8726e-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="8726e-111">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8726e-111">Click Activate.</span></span>
6. <span data-ttu-id="8726e-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-112">Click Close.</span></span>
7. <span data-ttu-id="8726e-113">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8726e-113">Click Activate.</span></span>
8. <span data-ttu-id="8726e-114">Boyut değerlerini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8726e-114">Click Dimension values.</span></span>
9. <span data-ttu-id="8726e-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8726e-115">Close the page.</span></span>
10. <span data-ttu-id="8726e-116">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8726e-116">Click Save.</span></span>
11. <span data-ttu-id="8726e-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8726e-117">Close the page.</span></span>
12. <span data-ttu-id="8726e-118">Perakende ve Ticaret > Kanallar > Mağazalar > Tüm mağazalar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8726e-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="8726e-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8726e-120">Finansal boyutlar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="8726e-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="8726e-121">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-121">Click Edit.</span></span>
16. <span data-ttu-id="8726e-122">Commerce kanalı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="8726e-123">Listede, güncelleştirilecek mağazaya ilişkin boyut değerini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8726e-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="8726e-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="8726e-125">CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="8726e-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8726e-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="8726e-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="8726e-128">Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="8726e-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8726e-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="8726e-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="8726e-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8726e-131">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
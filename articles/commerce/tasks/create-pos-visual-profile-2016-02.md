---
title: Satış noktası (POS) görsel profilleri oluşturma
description: Bu yordam yeni bir noktası (POS) görsel profili oluşturma konusunda açıklama sağlar.
author: jashanno
manager: AnnBe
ms.date: 12/05/2015
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
ms.openlocfilehash: d2fda8857a3ff8ac52bb48e7c032ffae0441ce60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221269"
---
# <a name="create-point-of-sale-pos-visual-profiles"></a><span data-ttu-id="77120-103">Satış noktası (POS) görsel profilleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="77120-103">Create point of sale (POS) visual profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77120-104">Bu yordam yeni bir noktası (POS) görsel profili oluşturma konusunda açıklama sağlar.</span><span class="sxs-lookup"><span data-stu-id="77120-104">This procedure walks through creating a new point of sale (POS) visual profile.</span></span> <span data-ttu-id="77120-105">Görsel profil, POS kayıtlarının görünümünü belirleyen temel bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="77120-105">A visual profile contains basic information that determines the appearance of POS registers.</span></span> <span data-ttu-id="77120-106">Birden fazla görsel profiliniz oluşturabilir ve belirli kayıtlarda çalışacak belirli profiller atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77120-106">You can create several visual profiles and assign specific profiles to run on specific registers.</span></span> <span data-ttu-id="77120-107">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="77120-107">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="77120-108">Retail and Commerce > Kanal kurulumu > POS kurulumu > POS profilleri > Görsel profiller'e gidin.</span><span class="sxs-lookup"><span data-stu-id="77120-108">Go to Retail and Commerce > Channel setup > POS setup > POS profiles > Visual profiles.</span></span>
2. <span data-ttu-id="77120-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-109">Click New.</span></span>
3. <span data-ttu-id="77120-110">Profil numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="77120-110">In the Profile number field, type a value.</span></span>
4. <span data-ttu-id="77120-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="77120-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="77120-112">Uygulama türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-112">In the Application type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="77120-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="77120-114">Tema alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-114">In the Theme field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="77120-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="77120-116">Vurgu rengi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-116">In the Accent color field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="77120-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="77120-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="77120-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="77120-119">Oturum açma arka planı bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="77120-119">Toggle the expansion of the Login background section.</span></span>
13. <span data-ttu-id="77120-120">Yatay görüntü kodu alanında bir görüntü kimliği seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="77120-120">In the Landscape image ID field, select or enter an image ID.</span></span>
14. <span data-ttu-id="77120-121">Dikey görüntü kodu alanında bir görüntü kimliği seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="77120-121">In the Portrait image ID field, select or enter an image ID.</span></span>
15. <span data-ttu-id="77120-122">Arka plan bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="77120-122">Toggle the expansion of the Background section.</span></span>
16. <span data-ttu-id="77120-123">Görüntü kodu için RequestPopup</span><span class="sxs-lookup"><span data-stu-id="77120-123">RequestPopup the Image ID.</span></span>
17. <span data-ttu-id="77120-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="77120-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="77120-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
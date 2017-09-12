--- 
title: "Elektronik raporlama (ER) için sayım ve toplama biçimi oluşturma"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: cac3748182ba27735264acc947403d7b857f1b6e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="c55bd-103">Elektronik raporlama (ER) için sayım ve toplama biçimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c55bd-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c55bd-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="c55bd-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="c55bd-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c55bd-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c55bd-106">Bu adımları tamamlamak için, öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c55bd-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="c55bd-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="c55bd-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="c55bd-108">Microsoft tarafından sağlanan yapılandırma listesine erişim alma</span><span class="sxs-lookup"><span data-stu-id="c55bd-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="c55bd-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="c55bd-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c55bd-110">"Litware, Inc." emin olun</span><span class="sxs-lookup"><span data-stu-id="c55bd-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="c55bd-111">sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="c55bd-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="c55bd-112">"Litware, Inc." seçin.</span><span class="sxs-lookup"><span data-stu-id="c55bd-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="c55bd-113">sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="c55bd-113">provider.</span></span>
3. <span data-ttu-id="c55bd-114">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-114">Click Repositories.</span></span>
    * <span data-ttu-id="c55bd-115">"Operasyon kaynakları" türünün bir havuzu zaten varsa geçerli alt görevin kalan adımlarını atlayın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="c55bd-116">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="c55bd-117">Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="c55bd-118">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-118">Click Create repository.</span></span>
7. <span data-ttu-id="c55bd-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="c55bd-120">Microsoft tarafından sağlanan Intrastat yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="c55bd-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="c55bd-121">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-121">Click Open.</span></span>
2. <span data-ttu-id="c55bd-122">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c55bd-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="c55bd-123">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-123">Click Import.</span></span>
    * <span data-ttu-id="c55bd-124">Seçili yapılandırmanın 1.1 sürümü için İthalat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="c55bd-125">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-125">Click Yes.</span></span>
5. <span data-ttu-id="c55bd-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-126">Close the page.</span></span>
6. <span data-ttu-id="c55bd-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-127">Close the page.</span></span>
7. <span data-ttu-id="c55bd-128">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c55bd-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="c55bd-129">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c55bd-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="c55bd-130">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c55bd-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



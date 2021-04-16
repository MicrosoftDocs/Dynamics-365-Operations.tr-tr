---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 1 - Biçim oluşturma)
description: Bu konuda, önceden oluşturulmuş metin çıktısının verilerine dayalı olarak sayma ve toplama işlemi yapmak üzere Elektronik raporlama biçiminin nasıl yapılandırılacağı açıklanmaktadır. (1. Bölüm)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f1db144b2bfafa72abeaa92c6b21de717e4acbf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749057"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="0c09a-104">ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 1 - Biçim oluşturma)</span><span class="sxs-lookup"><span data-stu-id="0c09a-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c09a-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="0c09a-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="0c09a-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="0c09a-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="0c09a-107">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0c09a-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="0c09a-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="0c09a-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="0c09a-109">Microsoft tarafından sağlanan yapılandırma listesine erişim alma</span><span class="sxs-lookup"><span data-stu-id="0c09a-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="0c09a-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="0c09a-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0c09a-111">"Litware, Inc." emin olun</span><span class="sxs-lookup"><span data-stu-id="0c09a-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="0c09a-112">sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="0c09a-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="0c09a-113">"Litware, Inc." seçin.</span><span class="sxs-lookup"><span data-stu-id="0c09a-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="0c09a-114">sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="0c09a-114">provider.</span></span>
3. <span data-ttu-id="0c09a-115">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-115">Click Repositories.</span></span>
    * <span data-ttu-id="0c09a-116">"Operasyon kaynakları" türünün bir havuzu zaten varsa geçerli alt görevin kalan adımlarını atlayın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="0c09a-117">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="0c09a-118">Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="0c09a-119">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-119">Click Create repository.</span></span>
7. <span data-ttu-id="0c09a-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="0c09a-121">Microsoft tarafından sağlanan Intrastat yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="0c09a-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="0c09a-122">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-122">Click Open.</span></span>
2. <span data-ttu-id="0c09a-123">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0c09a-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="0c09a-124">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-124">Click Import.</span></span>
    * <span data-ttu-id="0c09a-125">Seçili yapılandırmanın 1.1 sürümü için İthalat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="0c09a-126">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-126">Click Yes.</span></span>
5. <span data-ttu-id="0c09a-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-127">Close the page.</span></span>
6. <span data-ttu-id="0c09a-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-128">Close the page.</span></span>
7. <span data-ttu-id="0c09a-129">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c09a-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="0c09a-130">Ağaçta, "Intrastat modeli" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="0c09a-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="0c09a-131">Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0c09a-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
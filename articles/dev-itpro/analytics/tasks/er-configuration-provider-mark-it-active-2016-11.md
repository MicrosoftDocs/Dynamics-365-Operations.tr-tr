--- 
title: "Elektronik raporlama (ER) için bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme"
description: "Aşağıdaki adımlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="1e087-103">Elektronik raporlama (ER) için bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="1e087-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e087-104">Aşağıdaki adımlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="1e087-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="1e087-105">Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır.</span><span class="sxs-lookup"><span data-stu-id="1e087-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="1e087-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1e087-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="1e087-107">Sağlayıcı oluşturun</span><span class="sxs-lookup"><span data-stu-id="1e087-107">Create a provider</span></span>
1. <span data-ttu-id="1e087-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="1e087-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1e087-109">Yapılandırma sağlayıcılar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e087-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="1e087-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e087-110">Click New.</span></span>
    * <span data-ttu-id="1e087-111">Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="1e087-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="1e087-112">Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (http://www.litware.com) için bir kayıt zaten varsa bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="1e087-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="1e087-113">Ad alanına "Litware, Inc." yazın.</span><span class="sxs-lookup"><span data-stu-id="1e087-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="1e087-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="1e087-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="1e087-115">İnternet adresi alanına "http://www.litware.com" yazın.</span><span class="sxs-lookup"><span data-stu-id="1e087-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="1e087-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="1e087-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="1e087-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e087-117">Click Save.</span></span>
7. <span data-ttu-id="1e087-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1e087-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="1e087-119">Etkin bir sağlayıcı olarak seçin</span><span class="sxs-lookup"><span data-stu-id="1e087-119">Select as an active provider</span></span>
1. <span data-ttu-id="1e087-120">Litware, Inc. sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="1e087-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="1e087-121">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e087-121">Click Set active.</span></span>



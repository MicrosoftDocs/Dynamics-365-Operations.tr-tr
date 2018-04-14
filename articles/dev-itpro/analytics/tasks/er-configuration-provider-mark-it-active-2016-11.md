--- 
title: "Elektronik raporlama (ER) için bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme"
description: "Aşağıdaki adımlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9ed6f62318cd6806de1b4c9d6aa314c5f0a25500
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="8ea08-103">Elektronik raporlama (ER) için bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="8ea08-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ea08-104">Aşağıdaki adımlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="8ea08-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="8ea08-105">Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır.</span><span class="sxs-lookup"><span data-stu-id="8ea08-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="8ea08-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="8ea08-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="8ea08-107">Sağlayıcı oluşturun</span><span class="sxs-lookup"><span data-stu-id="8ea08-107">Create a provider</span></span>
1. <span data-ttu-id="8ea08-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="8ea08-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8ea08-109">Yapılandırma sağlayıcılar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ea08-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="8ea08-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ea08-110">Click New.</span></span>
    * <span data-ttu-id="8ea08-111">Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="8ea08-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="8ea08-112">Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (`http://www.litware.com`) için bir kayıt zaten varsa bu yordamı atlayın.</span><span class="sxs-lookup"><span data-stu-id="8ea08-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="8ea08-113">Ad alanına "Litware, Inc." yazın.</span><span class="sxs-lookup"><span data-stu-id="8ea08-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="8ea08-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="8ea08-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="8ea08-115">İnternet adresi alanına `http://www.litware.com` yazın.</span><span class="sxs-lookup"><span data-stu-id="8ea08-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="8ea08-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ea08-116">Click Save.</span></span>
7. <span data-ttu-id="8ea08-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8ea08-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="8ea08-118">Etkin bir sağlayıcı olarak seçin</span><span class="sxs-lookup"><span data-stu-id="8ea08-118">Select as an active provider</span></span>
1. <span data-ttu-id="8ea08-119">Litware, Inc. sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="8ea08-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="8ea08-120">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ea08-120">Click Set active.</span></span>



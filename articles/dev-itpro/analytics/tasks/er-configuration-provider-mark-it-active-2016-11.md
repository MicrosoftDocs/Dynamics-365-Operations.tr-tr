--- 
title: "Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="e5c40-103">Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="e5c40-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5c40-104">Aşağıdaki adımlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="e5c40-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="e5c40-105">Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır.</span><span class="sxs-lookup"><span data-stu-id="e5c40-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="e5c40-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e5c40-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="e5c40-107">Sağlayıcı oluşturun</span><span class="sxs-lookup"><span data-stu-id="e5c40-107">Create a provider</span></span>
1. <span data-ttu-id="e5c40-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="e5c40-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e5c40-109">Yapılandırma sağlayıcılar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5c40-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="e5c40-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5c40-110">Click New.</span></span>
    * <span data-ttu-id="e5c40-111">Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="e5c40-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="e5c40-112">Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (`http://www.litware.com`) için bir kayıt zaten varsa bu yordamı atlayın.</span><span class="sxs-lookup"><span data-stu-id="e5c40-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="e5c40-113">Ad alanına "Litware, Inc." yazın.</span><span class="sxs-lookup"><span data-stu-id="e5c40-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="e5c40-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e5c40-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="e5c40-115">İnternet adresi alanına `http://www.litware.com` yazın.</span><span class="sxs-lookup"><span data-stu-id="e5c40-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="e5c40-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5c40-116">Click Save.</span></span>
7. <span data-ttu-id="e5c40-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e5c40-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="e5c40-118">Etkin bir sağlayıcı olarak seçin</span><span class="sxs-lookup"><span data-stu-id="e5c40-118">Select as an active provider</span></span>
1. <span data-ttu-id="e5c40-119">Litware, Inc. sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e5c40-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="e5c40-120">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5c40-120">Click Set active.</span></span>



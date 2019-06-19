---
title: Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme
description: Aşağıdaki adımlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4b1cd7a02cdf4c650af50199f4425eb53cef0a8
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595407"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="2ceaf-103">Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="2ceaf-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ceaf-104">Aşağıdaki adımlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="2ceaf-105">Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="2ceaf-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="2ceaf-107">Sağlayıcı oluşturun</span><span class="sxs-lookup"><span data-stu-id="2ceaf-107">Create a provider</span></span>
1. <span data-ttu-id="2ceaf-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2ceaf-109">Yapılandırma sağlayıcılar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="2ceaf-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-110">Click New.</span></span>
    * <span data-ttu-id="2ceaf-111">Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="2ceaf-112">Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (https://www.litware.com) için bir kayıt zaten varsa bu yordamı atlayın.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="2ceaf-113">Ad alanına "Litware, Inc." yazın.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="2ceaf-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="2ceaf-115">İnternet adresi alanına 'https://www.litware.com' yazın.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-115">In the Internet address field, type 'https://www.litware.com'.</span></span>
    * https://www.litware.com  
6. <span data-ttu-id="2ceaf-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-116">Click Save.</span></span>
7. <span data-ttu-id="2ceaf-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="2ceaf-118">Etkin bir sağlayıcı olarak seçin</span><span class="sxs-lookup"><span data-stu-id="2ceaf-118">Select as an active provider</span></span>
1. <span data-ttu-id="2ceaf-119">Litware, Inc. sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="2ceaf-120">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ceaf-120">Click Set active.</span></span>


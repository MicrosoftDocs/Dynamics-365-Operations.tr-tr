---
title: Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme
description: Bu konu Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Dynamics 365 for Finance and Operations'taki Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0dfbcf70493a43320e17d4d2734fe6343d43eaf3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850339"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="52828-103">Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="52828-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52828-104">Bu konu Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Dynamics 365 for Finance and Operations'taki Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="52828-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER) in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="52828-105">Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır.</span><span class="sxs-lookup"><span data-stu-id="52828-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="52828-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="52828-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="52828-107">Sağlayıcı oluşturun</span><span class="sxs-lookup"><span data-stu-id="52828-107">Create a provider</span></span>
1. <span data-ttu-id="52828-108">Sol üst köşedeki **gezinti bölmesi**'ne gidin ve **Kuruluş yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="52828-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="52828-109">Sırasıyla **Çalışma alanları > Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="52828-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="52828-110">**İlgili bağlantılar > Yapılandırma sağlayıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="52828-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="52828-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52828-111">Select **New**.</span></span>
    - <span data-ttu-id="52828-112">Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="52828-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="52828-113">Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (https://www.litware.com) için bir kayıt zaten varsa bu yordamı atlayın.</span><span class="sxs-lookup"><span data-stu-id="52828-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="52828-114">İsim alanına `Litware, Inc.`. yazın.</span><span class="sxs-lookup"><span data-stu-id="52828-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="52828-115">İnternet adresi alanına "`https://www.litware.com`" yazın.</span><span class="sxs-lookup"><span data-stu-id="52828-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="52828-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="52828-116">Select **Save**.</span></span>
8. <span data-ttu-id="52828-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="52828-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="52828-118">Etkin bir sağlayıcı olarak seçin</span><span class="sxs-lookup"><span data-stu-id="52828-118">Select as an active provider</span></span>
1. <span data-ttu-id="52828-119">Litware, Inc. sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="52828-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="52828-120">**Etkin olarak ayarla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="52828-120">Select **Set active**.</span></span>


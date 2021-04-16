---
title: Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme
description: Bu konuda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının bir yapılandırma sağlayıcısını nasıl oluşturabileceği açıklanmaktadır.
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27e1275199d098fffb56db61ed6bfd2fc3cdb790
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755142"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="5033f-103">Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="5033f-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5033f-104">Bu konu Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="5033f-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="5033f-105">Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır.</span><span class="sxs-lookup"><span data-stu-id="5033f-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="5033f-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="5033f-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="5033f-107">Sağlayıcı oluşturun</span><span class="sxs-lookup"><span data-stu-id="5033f-107">Create a provider</span></span>
1. <span data-ttu-id="5033f-108">Sol üst köşedeki **gezinti bölmesi**'ne gidin ve **Kuruluş yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5033f-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="5033f-109">Sırasıyla **Çalışma alanları > Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="5033f-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="5033f-110">**İlgili bağlantılar > Yapılandırma sağlayıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="5033f-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="5033f-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5033f-111">Select **New**.</span></span>
    - <span data-ttu-id="5033f-112">Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="5033f-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="5033f-113">Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (https://www.litware.com) için bir kayıt zaten varsa bu yordamı atlayın.</span><span class="sxs-lookup"><span data-stu-id="5033f-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="5033f-114">İsim alanına `Litware, Inc.`. yazın.</span><span class="sxs-lookup"><span data-stu-id="5033f-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="5033f-115">İnternet adresi alanına "`https://www.litware.com`" yazın.</span><span class="sxs-lookup"><span data-stu-id="5033f-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="5033f-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5033f-116">Select **Save**.</span></span>
8. <span data-ttu-id="5033f-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5033f-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="5033f-118">Etkin bir sağlayıcı olarak seçin</span><span class="sxs-lookup"><span data-stu-id="5033f-118">Select as an active provider</span></span>
1. <span data-ttu-id="5033f-119">Litware, Inc. sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="5033f-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="5033f-120">**Etkin olarak ayarla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5033f-120">Select **Set active**.</span></span>

![Elektronik raporlama çalışma alanı sayfası](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
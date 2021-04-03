---
title: Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme
description: Bu konuda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının bir yapılandırma sağlayıcısını nasıl oluşturabileceği açıklanmaktadır.
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 11ff1d531b0467cf75ec98b092fe6010f4fa95c0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569799"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="3baf9-103">Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="3baf9-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3baf9-104">Bu konu Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolüne atanan bir kullanıcının, Elektronik Raporlama (ER) için bir yapılandırma tedarikçisini nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="3baf9-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="3baf9-105">Her bir ER yapılandırması, yapılandırmanın yazarı olarak tedarikçiye başvuracaktır.</span><span class="sxs-lookup"><span data-stu-id="3baf9-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="3baf9-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma tedarikçisi oluşturacaksınız. Bu adımlar, ER yapılandırma tedarikçileri tüm şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3baf9-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="3baf9-107">Sağlayıcı oluşturun</span><span class="sxs-lookup"><span data-stu-id="3baf9-107">Create a provider</span></span>
1. <span data-ttu-id="3baf9-108">Sol üst köşedeki **gezinti bölmesi**'ne gidin ve **Kuruluş yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3baf9-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="3baf9-109">Sırasıyla **Çalışma alanları > Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="3baf9-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="3baf9-110">**İlgili bağlantılar > Yapılandırma sağlayıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3baf9-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="3baf9-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3baf9-111">Select **New**.</span></span>
    - <span data-ttu-id="3baf9-112">Sağlayıcı kaydı benzersiz bir ada ve URL'ye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="3baf9-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="3baf9-113">Bu sayfanın içeriğini gözden geçirin ve Litware, Inc. (https://www.litware.com) için bir kayıt zaten varsa bu yordamı atlayın.</span><span class="sxs-lookup"><span data-stu-id="3baf9-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="3baf9-114">İsim alanına `Litware, Inc.`. yazın.</span><span class="sxs-lookup"><span data-stu-id="3baf9-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="3baf9-115">İnternet adresi alanına "`https://www.litware.com`" yazın.</span><span class="sxs-lookup"><span data-stu-id="3baf9-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="3baf9-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3baf9-116">Select **Save**.</span></span>
8. <span data-ttu-id="3baf9-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3baf9-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="3baf9-118">Etkin bir sağlayıcı olarak seçin</span><span class="sxs-lookup"><span data-stu-id="3baf9-118">Select as an active provider</span></span>
1. <span data-ttu-id="3baf9-119">Litware, Inc. sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="3baf9-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="3baf9-120">**Etkin olarak ayarla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3baf9-120">Select **Set active**.</span></span>

![Elektronik raporlama çalışma alanı sayfası](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
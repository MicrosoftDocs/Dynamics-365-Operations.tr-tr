---
title: Regulatory Configuration Service (RCS) - RCS ortamını silme
description: Bu konu, Regulatory Configuration Service (RCS) sistem yöneticisinin bir RCS ortamını ve ilgili verileri nasıl silebileceğini açıklamaktadır.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295830"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="f06c9-103">Regulatory Configuration Service (RCS) - RCS ortamını silme</span><span class="sxs-lookup"><span data-stu-id="f06c9-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f06c9-104">Bu konu, Regulatory Configuration Service (RCS) sistem yöneticisinin bir RCS ortamını ve ilgili verileri nasıl silebileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f06c9-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="f06c9-105">Bu konudaki yordamı tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:</span><span class="sxs-lookup"><span data-stu-id="f06c9-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="f06c9-106">RCS ortamı için size **Sistem yöneticisi** rolü atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f06c9-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="f06c9-107">**Sistem Yöneticisi** rolüne **RCSDeleteEnvironmentDuty** rolü atanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f06c9-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="f06c9-108">RCS ortamını silme</span><span class="sxs-lookup"><span data-stu-id="f06c9-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="f06c9-109">RCS'yi açın ve **Elektronik raporlama** çalışma alanı kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f06c9-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="f06c9-110">**İlgili bağlantılar** bölümünde, **RCS ortamını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f06c9-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![İlgili bağlantılar bölümünde RCS ortamı bağlantısını silme](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="f06c9-112">Görüntülenen iletişim kutusunda, ortam silme kapsamı hakkındaki iletileri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="f06c9-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![RCS ortamını sil iletişim kutusundaki iletiler](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="f06c9-114">RCS ortamının silinmesi geri alınamaz.</span><span class="sxs-lookup"><span data-stu-id="f06c9-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="f06c9-115">İşlem, seçilen RCS ortamını ve Genel depoda depolanan özellikler ve yapılandırmalar dahil ilgili tüm verileri siler.</span><span class="sxs-lookup"><span data-stu-id="f06c9-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="f06c9-116">Diğer kuruluşlarla paylaşılan özellikler ve yapılandırmalar, bağımlılıkları yoksa paylaşımdan kaldırılır ve silinir.</span><span class="sxs-lookup"><span data-stu-id="f06c9-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="f06c9-117">Bağımlılıkları olan özellikler ve yapılandırmalar devam ettirilmiyor olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="f06c9-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="f06c9-118">Sağlanan alanda, silmek istediğinizi onaylamak için RCS ortamının genel benzersiz tanımlayıcısını (GUID) girin.</span><span class="sxs-lookup"><span data-stu-id="f06c9-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="f06c9-119">Ortamın GUID'i silme iletisine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="f06c9-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="f06c9-120">**Ortamı sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f06c9-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="f06c9-121">RCS ortamınız ve ilgili tüm veriler artık silindi.</span><span class="sxs-lookup"><span data-stu-id="f06c9-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f06c9-122">Bir RCS ortamını sildikten sonra, verileri kurtarmanın bir yolu yoktur.</span><span class="sxs-lookup"><span data-stu-id="f06c9-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="f06c9-123">Kullanılabilir herhangi bir RCS bölgesinde yeni bir RCS ortamı oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="f06c9-123">A new RCS environment can be created in any available RCS region.</span></span>

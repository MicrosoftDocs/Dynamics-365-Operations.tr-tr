---
title: Görev kayıtları için güvenlik tanılaması
description: Bu konu, bir görev kaydı temel alınarak güvenlik izni gereksinimlerinin nasıl analiz edileceği ve yönetileceği hakkında bilgi sağlar.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 99f9da527e818892eb3f46aceca3cc4588b99e81
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570993"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="1ec51-103">Görev kayıtları için güvenlik tanılaması</span><span class="sxs-lookup"><span data-stu-id="1ec51-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="1ec51-104">Başlamadan önce</span><span class="sxs-lookup"><span data-stu-id="1ec51-104">Before you begin</span></span>

<span data-ttu-id="1ec51-105">Bu konu, bir görev kaydı temel alınarak güvenlik izni gereksinimlerinin nasıl analiz edileceği ve yönetileceği hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1ec51-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="1ec51-106">Bu konudaki adımları gerçekleştirmeden önce, analiz etmek istediğiniz iş süreci için bir görev kaydınız olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ec51-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="1ec51-107">Bir iş süreci kaydetmek için [Görev kaydedici kaynakları](../../user-interface/task-recorder.md)'na bakın.</span><span class="sxs-lookup"><span data-stu-id="1ec51-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="1ec51-108">Görev kaydı için güvenliği yönetme</span><span class="sxs-lookup"><span data-stu-id="1ec51-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="1ec51-109">**Sistem yönetimi** > **Güvenlik** > **Görev kaydı için güvenlik tanılamaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1ec51-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="1ec51-110">Görev kaydını konumundan açın.</span><span class="sxs-lookup"><span data-stu-id="1ec51-110">Open the task recording from its location.</span></span> <span data-ttu-id="1ec51-111">**Bu bilgisayardan aç**'ı veya **Lifecycle Services'tan aç**'ı seçin ve sonra **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ec51-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="1ec51-112">Bu süreç için gerekli güvenlik nesnelerini listeleyen **Güvenlik menüsü öğe ayrıntıları** sayfasını açar.</span><span class="sxs-lookup"><span data-stu-id="1ec51-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="1ec51-113">**Eylem** ve **Çıkış** menü öğeleri listeye dahil edilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="1ec51-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="1ec51-114">**Kullanıcı kimliği** alanında bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ec51-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="1ec51-115">Kullanıcının bazı menü öğeleri için izni yoksa, **Eksik izinler** alanı **Evet** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1ec51-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Güvenlik menü öğesi ayrıntıları sayfası](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="1ec51-117">Eksik izni veren roller, görevler ve ayrıcalıklar gibi güvenlik nesnelerinin listesini görmek için **Referans ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ec51-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="1ec51-118">Listeden bir güvenlik nesnesi seçin:</span><span class="sxs-lookup"><span data-stu-id="1ec51-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="1ec51-119">**Rol** seçiliyse, **Kullanıcıya rol ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ec51-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="1ec51-120">Bu, **Kullanıcıları rollere ata** sayfasını açar.</span><span class="sxs-lookup"><span data-stu-id="1ec51-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="1ec51-121">Daha fazla bilgi için bkz. [Kullanıcıları güvenlik rollerine ata](assign-users-security-roles.md) sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="1ec51-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="1ec51-122">**Görev** seçilmişse, **Role görev ekle**'yi seçin, görevin ekleneceği rolleri ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ec51-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="1ec51-123">**Ayrıcalık** seçilmişse, **Görevlere ayrıcalık**'yi seçin, görevin ekleneceği rolleri ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ec51-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
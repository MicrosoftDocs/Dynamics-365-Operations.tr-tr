---
title: Kiralama onayı iş akışlarını ayarlama
description: Bu konu, yeni bir kiralama oluşturulduğunda çalışacak bir onay iş akışının nasıl ayarlanacağını açıklar.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0e7280bbf60901266c81a0c89395c5183f991425
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881674"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="bbefb-103">Kiralama onayı iş akışlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="bbefb-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbefb-104">Bu konu, yeni bir kiralama oluşturulduğunda çalışacak bir onay iş akışının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="bbefb-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="bbefb-105">İş akışının nasıl kullanılacağı hakkında bilgi için bkz. [Kiralama onayı iş akışlarını kullanma](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="bbefb-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="bbefb-106">**Varlık kiralama \> Kurulum \> Kiralama iş akışı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="bbefb-107">**Kiralama iş akışı** sayfasında **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="bbefb-108">Görüntülenen iletişim kutusunda, **İş akışı türünde** **Kiralama iş akışı** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="bbefb-109">Uygulama açıldı.</span><span class="sxs-lookup"><span data-stu-id="bbefb-109">The application is opened.</span></span> <span data-ttu-id="bbefb-110">Çalıştıktan sonra iş akışı uygulamasına yönlendirilmek için Azure Active Directory'de (Azure AD) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="bbefb-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="bbefb-111">**Kiralama iş akışı onayı** öğesini iş akışının üzerine sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="bbefb-112">**Başlangıç**'tan **Kiralama iş akışı onayı**'na bir düğüm bağlayın.</span><span class="sxs-lookup"><span data-stu-id="bbefb-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="bbefb-113">Ardından **Kiralama iş akışı onayı**'nı **Bitiş**'e bağlayın.</span><span class="sxs-lookup"><span data-stu-id="bbefb-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="bbefb-114">**Kiralama iş akışı onayı**'na çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bbefb-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="bbefb-115">**Özellikler**'i seçin ve **Temel ayarlar** bölümünde iş akışı için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="bbefb-116">Bu sayfada, iş akışı için daha fazla parametre ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbefb-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="bbefb-117">**Otomatik eylemleri** etkinleştirdiyseniz , sistem otomatik olarak belirli bir eylemi alacaktır.</span><span class="sxs-lookup"><span data-stu-id="bbefb-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="bbefb-118">**Bildirimler** sekmesinde etkinleştirildiyse bildirim gönderilebilir. **Gelişmiş ayarlar** sekmesinde nihai onaylacıyı belirtebilir, süre sınırı ayarlayabilir ve tamamlanması gereken belirli eylemler atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbefb-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="bbefb-119">İş akışı parametrelerini ayarlamayı bitirdiğinizde **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="bbefb-120">**Adım 1**'i seçin ve ardından **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="bbefb-121">**Temel ayarlar** bölümünde adım için bir ad girin, onay için bir konu satırı oluşturun ve onay için yönergeler belirtin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="bbefb-122">**Atama** sayfasında, atama türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="bbefb-123">Onaya belirli kullanıcılar atamak için **Kullanıcı**'yı seçin, kiralamaları onaylayan kullanıcıları seçin ve ardından **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="bbefb-124">İş akışını oluşturmak için **Kaydet ve kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="bbefb-125">Ardından, istendiğinde **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="bbefb-126">**İş akışı oluştur** sayfasında **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="bbefb-127">Yeni iş akışını seçin ve ardından **Sürümler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="bbefb-128">İş akışının etkin olmasını sağlamak için **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="bbefb-129">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bbefb-129">Select **Close**.</span></span> <span data-ttu-id="bbefb-130">Yeni etkin sürüm görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bbefb-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

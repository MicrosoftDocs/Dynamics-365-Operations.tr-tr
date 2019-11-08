---
title: Bakım bütçeleri oluşturma
description: Bu konuda Varlık Yönetimi'nde bakım bütçesi oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 99f76c684150f154404cbb241daacb7a8d05f7f9
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571772"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="da700-103">Bakım bütçeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="da700-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="da700-104">Bakım bütçeleri, önleyici bakım için beklenen maliyetlere genel bir bakış sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="da700-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="da700-105">Bütçe satırları, bütçe dönemi içinde beklenen başlangıç tarihinin bulunduğu bakım zamanlaması satırları temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="da700-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="da700-106">Bakım bütçeleri, Varlık Yönetimi'nde kullanılan maliyet türlerini temel alır: **Önleyici**, **Düzeltici**ve **Yatırım**.</span><span class="sxs-lookup"><span data-stu-id="da700-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="da700-107">Yatırım bakımı için bütçe maliyetleri, bütçe dönemindeki değiştirme tarihinin ve ilgili değişiklik değerinin bulunduğu etkin varlıklar için dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="da700-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="da700-108">Geçmiş düzeltme tarihi bütçe hesaplamasına dahilse düzeltici bakım için bütçe maliyetleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="da700-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="da700-109">Bu durumda önceki bir döneme ait düzeltici maliyetler, bakım bütçesini hesapladığınız aynı gelecek dönem için hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="da700-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="da700-110">Bakım bütçesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="da700-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="da700-111">**Varlık yönetimi** \> **Sorgular** \> **Bakım bütçesi** \> **Bütçe**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="da700-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="da700-112">**Bütçe oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="da700-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="da700-113">**Bakım bütçesi** alanına bir bütçe kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="da700-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="da700-114">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="da700-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="da700-115">**Dönem** hızlı sekmesinde, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına bütçe döneminin başlangıç ve bitiş tarihlerini girin.</span><span class="sxs-lookup"><span data-stu-id="da700-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="da700-116">Önceki bir dönemde fiili maliyetler temel alınarak hesaplanan düzeltici bütçe maliyetlerini dahil etmek için **Düzeltici başlangıç tarihi** alanına, bu maliyetlerin dahil edileceği dönemin başlangıç tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="da700-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="da700-117">Bütçede gereken ayrıntı düzeyine bağlı olarak beş **Gruplama ölçütü** hızlı sekmesinde ilgili seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="da700-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="da700-118">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="da700-118">Select **OK**.</span></span>
8. <span data-ttu-id="da700-119">**Bütçe satırları**'nı seçerek **Bakım bütçesi satırları** sayfasını açın, burada dönem için oluşturulan tüm bütçe satırlarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da700-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="da700-120">Bütçeyi onaylamak için **Bakım bütçeleri** sayfasından bütçeyi ve ardından **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="da700-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="da700-121">Ardından **Bütçeyi onayla** iletişim kutusunda, **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="da700-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="da700-122">Adınız **Bakım bütçeleri** sayfasındaki **Onaylayan** alanına girilir.</span><span class="sxs-lookup"><span data-stu-id="da700-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="da700-123">Bakım bütçesini onayladıktan sonra önce onayı kaldırmadığınız sürece **Bakım bütçesi satırları** sayfasındaki ilgili satırları yeniden hesaplayamaz veya ayarlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="da700-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="da700-124">Bakım bütçesinin onayını kaldırmak için **Bakım bütçeleri** sayfasından bütçeyi ve ardından **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="da700-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="da700-125">Ardından **Bütçeyi onayla** iletişim kutusunda, **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="da700-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![Bakım Bütçeleri](media/01-maintenance-budgets.png)

<span data-ttu-id="da700-127">Ayrıca mevcut bütçeyi kopyalayarak yeni bir bakım bütçesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da700-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="da700-128">**Bakım bütçeleri** sayfasında, kopyalanacak bütçeyi ve ardından **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="da700-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="da700-129">Bu yaklaşım, örneğin bir aylık bir bütçe oluşturduğunuzda ve bunu diğer aylara kopyalamak istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="da700-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="da700-130">Bakım bütçesi yalnızca bakım zamanlaması satırlarını temel alan bütçe maliyetlerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="da700-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="da700-131">Aynı dönemdeki fiili maliyetleri **Varlık maliyeti denetimi** sayfasında hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da700-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 

---
title: POS'ta görev yönetimi
description: Bu konu, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasındaki görev yönetimini açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036798"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="5c9ea-103">POS'ta görev yönetimi</span><span class="sxs-lookup"><span data-stu-id="5c9ea-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c9ea-104">Bu konu, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasındaki görev yönetimini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="5c9ea-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="5c9ea-105">Overview</span></span>

<span data-ttu-id="5c9ea-106">Dynamics 365 Commerce POS uygulaması, Mağaza yöneticilerinin ve çalışanların görevleri yönetmesine ve görev durumunu güncelleştirmesine izin veren görev yönetimi özelliklerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="5c9ea-107">Mağaza çalışanları, POS giriş sayfasındaki **Görevler** döşemesini seçerek veya görev bildirimlerini seçerek, görevlere erişebilir.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="5c9ea-108">Varsayılan olarak, mağaza çalışanları kendilerine atanan görevleri görüntüleyebileceğiniz **Görevlerim** sekmesine alınır.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="5c9ea-109">Ancak, bu kullanıcılar, **süresi geçen görevlere**, **açık görevlere** ve **görev listeleri** sekmelerine kolayca geçebilir.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="5c9ea-110">Mağaza yöneticileri için görev operasyonları</span><span class="sxs-lookup"><span data-stu-id="5c9ea-110">Task operations for store managers</span></span>

<span data-ttu-id="5c9ea-111">Mağaza yöneticileri, Komut çubuğundaki düğmeleri kullanarak POS uygulamasında aşağıdaki görev işlemlerini gerçekleştirebilir:</span><span class="sxs-lookup"><span data-stu-id="5c9ea-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="5c9ea-112">**Ata** – Seçili görevleri bir mağaza çalışanına atayın.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="5c9ea-113">**Görev durumu** – Seçili görevlerin durumunu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="5c9ea-114">**Filtre** – Varsayılan olarak yalnızca etkin görevler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="5c9ea-115">Ancak, filtreler uygulanarak tüm görevler, tamamlanmış veya iptal edilmiş görevler de görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="5c9ea-116">**Yeni görev** – Varolan bir görev listesi altında bir görev oluşturun veya tek amaçlı bir görev oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="5c9ea-117">Mağaza çalışanları, Komut çubuğundaki düğmeleri kullanarak POS uygulamasında aşağıdaki görev işlemlerini gerçekleştirebilir:</span><span class="sxs-lookup"><span data-stu-id="5c9ea-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="5c9ea-118">**Görev durumu** – Seçili görevlerin durumunu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="5c9ea-119">**Filtre** – Varsayılan olarak yalnızca etkin görevler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="5c9ea-120">Ancak, filtreler uygulanarak çalışanlar tüm görevler, tamamlanmış veya iptal edilmiş görevleri de görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="5c9ea-121">Aşağıdaki şekil, Commerce POS uygulamasındaki **görevlerim** sekmesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c9ea-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Commerce POS uygulamasındaki görevlerim sekmesi](media/POS-task-management.png)

<span data-ttu-id="5c9ea-123">Aşağıdaki çizimde **Görev listeleri** sekmesi gösterilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5c9ea-123">The following illustration shows the **Task lists** tab.</span></span>

![Commerce POS uygulamasındaki görev listeleri sekmesi](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="5c9ea-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5c9ea-125">Additional resources</span></span>

[<span data-ttu-id="5c9ea-126">Görev yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5c9ea-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="5c9ea-127">Görev yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5c9ea-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="5c9ea-128">Görev listeleri oluşturma ve görev ekleme</span><span class="sxs-lookup"><span data-stu-id="5c9ea-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="5c9ea-129">Mağazalara veya personele görev listeleri atama</span><span class="sxs-lookup"><span data-stu-id="5c9ea-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

---
title: İndirim yönetimi anlaşması iş akışları
description: Bu konu, bir Indirim yönetimi anlaşma iş akışının anlaşmaları onaylamak ve etkinleştirmek için nasıl ayarlanacağını açıklamaktadır.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 8436842b4f07ba000649075198bdef43ad508f8f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270969"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="9a050-103">İndirim yönetimi anlaşması iş akışları</span><span class="sxs-lookup"><span data-stu-id="9a050-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a050-104">İndirim anlaşmalarını onaylamak için, İndirim yönetimi, diğer Finance and Operations uygulamalarıyla aynı iş akışı platformunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="9a050-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="9a050-105">İki iş işlemi her iş akışı ile ilişkilendirilmiştir:</span><span class="sxs-lookup"><span data-stu-id="9a050-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="9a050-106">İş akışının bir öğesi anlaşmayı onaylar.</span><span class="sxs-lookup"><span data-stu-id="9a050-106">One element of the workflow approves the deal.</span></span>
- <span data-ttu-id="9a050-107">İş akışının bir öğesi, Kullanıcı veya iş akışı işleminin hareketleri onaylaması için, anlaşmayı etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="9a050-107">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>

<span data-ttu-id="9a050-108">İndirim anlaşması kullanabilmeniz için, bunun **indirim Yönetimi** modülünde etkin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9a050-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="9a050-109">Bir anlaşmayı etkinleştirmek için önce bir *indirim yönetimi anlaşma iş akışı* oluşturmalı ve konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="9a050-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="9a050-110">Kullanıcılar fırsatları el ile onaylayamaz.</span><span class="sxs-lookup"><span data-stu-id="9a050-110">Users can't manually approve deals.</span></span> <span data-ttu-id="9a050-111">İş akışının her zaman kullanılması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9a050-111">The workflow must always be used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="9a050-112">İndirim yönetimi anlaşması iş akışlarını oluşturma ve yönetme</span><span class="sxs-lookup"><span data-stu-id="9a050-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="9a050-113">İndirim yönetimi anlaşması iş akışlarıyla çalışmak için, **indirim Yönetimi \>kurulum \> indirim yönetimi iş akışlarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="9a050-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="9a050-114">Burada, iş akışlarını gerektiği gibi görüntüleyebilir, oluşturabilir ve güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a050-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="9a050-115">Aynı anda yalnızca bu türdeki bir iş akışı etkin olabilir.</span><span class="sxs-lookup"><span data-stu-id="9a050-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="9a050-116">İş akışları hakkında daha fazla bilgi için, **indirim yönetimi iş akışları** sayfası ile nasıl çalışılacağı ve iş akışlarının nasıl oluşturulacağını öğrenmek için [iş akışı sistemine genel bakışa](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ve ilgili konularına bakın.</span><span class="sxs-lookup"><span data-stu-id="9a050-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="9a050-117">Anlaşmayı etkinleştirmek için iş akışı kullanma</span><span class="sxs-lookup"><span data-stu-id="9a050-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="9a050-118">Bir iş akışı üzerinden bir anlaşmayı etkinleştirmek için, anlaşmayı açın (örneğin, **tüm indirim yönetimi anlaşmaları** sayfasında).</span><span class="sxs-lookup"><span data-stu-id="9a050-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="9a050-119">Ardından Eylem bölmesinden **İş akışı \> Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9a050-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="9a050-120">Yeni anlaşma iş akışı ile işlendikten ve onaylandıktan sonra, etkin ve kullanıma hazır olur.</span><span class="sxs-lookup"><span data-stu-id="9a050-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="9a050-121">Bir anlaşma etkinleştirildikten sonra, kurulumunun büyük bölümünü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a050-121">After a deal has been activated, you can't change most of its setup.</span></span> <span data-ttu-id="9a050-122">Etkin bir anlaşmayı değiştirmeniz gerekiyorsa, önce bunu devre dışı bırakın ve sonra yeni bir anlaşma oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9a050-122">If you must change an active deal, first inactivate it, and then create a new deal.</span></span> <span data-ttu-id="9a050-123">Yeni anlaşma eski anlaşmayı benziyorsa, eski anlaşmayı kopyalayarak bunu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a050-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

<span data-ttu-id="9a050-124">Bir anlaşma etkinleştirildikten sonra aşağıdaki ayarları değiştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9a050-124">You can change the following settings for a deal after it has been activated:</span></span>

- <span data-ttu-id="9a050-125">Mutabakat ölçütü</span><span class="sxs-lookup"><span data-stu-id="9a050-125">Reconcile by</span></span>
- <span data-ttu-id="9a050-126">Kümülatif garanti</span><span class="sxs-lookup"><span data-stu-id="9a050-126">Cumulative guarantee</span></span>
- <span data-ttu-id="9a050-127">Deftere nakil profili</span><span class="sxs-lookup"><span data-stu-id="9a050-127">Posting profile</span></span>
- <span data-ttu-id="9a050-128">Garanti için nakil profili</span><span class="sxs-lookup"><span data-stu-id="9a050-128">Posting profile for guarantee</span></span>
- <span data-ttu-id="9a050-129">Belge notları</span><span class="sxs-lookup"><span data-stu-id="9a050-129">Document notes</span></span>
- <span data-ttu-id="9a050-130">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="9a050-130">Currency</span></span>
- <span data-ttu-id="9a050-131">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="9a050-131">From date</span></span>
- <span data-ttu-id="9a050-132">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="9a050-132">To date</span></span>

<span data-ttu-id="9a050-133">Ayrıca, indirim satırları kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="9a050-133">In addition, rebate lines can be removed.</span></span>

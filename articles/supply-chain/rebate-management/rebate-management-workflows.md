---
title: İndirim yönetimi anlaşması iş akışları
description: Bu konu, bir Indirim yönetimi anlaşma iş akışının anlaşmaları onaylamak ve etkinleştirmek için nasıl ayarlanacağını açıklamaktadır.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 37b8022633e61c4d98d6f5d129bcf494a9ed92e0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831734"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="f41ab-103">İndirim yönetimi anlaşması iş akışları</span><span class="sxs-lookup"><span data-stu-id="f41ab-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f41ab-104">İndirim anlaşmalarını onaylamak için, İndirim yönetimi, diğer Finance and Operations uygulamalarıyla aynı iş akışı platformunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="f41ab-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="f41ab-105">İki iş işlemi her iş akışı ile ilişkilendirilmiştir:</span><span class="sxs-lookup"><span data-stu-id="f41ab-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="f41ab-106">İş akışının bir öğesi, Kullanıcı veya iş akışı işleminin hareketleri onaylaması için, anlaşmayı etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="f41ab-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="f41ab-107">İş akışının bir öğesi anlaşmayı onaylar.</span><span class="sxs-lookup"><span data-stu-id="f41ab-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="f41ab-108">İndirim anlaşması kullanabilmeniz için, bunun **indirim Yönetimi** modülünde etkin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f41ab-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="f41ab-109">Bir anlaşmayı etkinleştirmek için önce bir *indirim yönetimi anlaşma iş akışı* oluşturmalı ve konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f41ab-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="f41ab-110">İndirim yönetimi için iş akışı etkinleştirildikten sonra, kullanıcılar anlaşmaları el ile onaylayamaz.</span><span class="sxs-lookup"><span data-stu-id="f41ab-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="f41ab-111">İş akışının her zaman kullanılması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f41ab-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="f41ab-112">İndirim yönetimi anlaşması iş akışlarını oluşturma ve yönetme</span><span class="sxs-lookup"><span data-stu-id="f41ab-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="f41ab-113">İndirim yönetimi anlaşması iş akışlarıyla çalışmak için, **indirim Yönetimi \>kurulum \> indirim yönetimi iş akışlarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="f41ab-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="f41ab-114">Burada, iş akışlarını gerektiği gibi görüntüleyebilir, oluşturabilir ve güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f41ab-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="f41ab-115">Aynı anda yalnızca bu türdeki bir iş akışı etkin olabilir.</span><span class="sxs-lookup"><span data-stu-id="f41ab-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="f41ab-116">İş akışları hakkında daha fazla bilgi için, **indirim yönetimi iş akışları** sayfası ile nasıl çalışılacağı ve iş akışlarının nasıl oluşturulacağını öğrenmek için [iş akışı sistemine genel bakışa](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ve ilgili konularına bakın.</span><span class="sxs-lookup"><span data-stu-id="f41ab-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="f41ab-117">Anlaşmayı etkinleştirmek için iş akışı kullanma</span><span class="sxs-lookup"><span data-stu-id="f41ab-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="f41ab-118">Bir iş akışı üzerinden bir anlaşmayı etkinleştirmek için, anlaşmayı açın (örneğin, **tüm indirim yönetimi anlaşmaları** sayfasında).</span><span class="sxs-lookup"><span data-stu-id="f41ab-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="f41ab-119">Ardından Eylem bölmesinden **İş akışı \> Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f41ab-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="f41ab-120">Yeni anlaşma iş akışı ile işlendikten ve onaylandıktan sonra, etkin ve kullanıma hazır olur.</span><span class="sxs-lookup"><span data-stu-id="f41ab-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="f41ab-121">Bir anlaşma etkinleştirildikten sonra, kurulumunu değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f41ab-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="f41ab-122">Etkin bir anlaşmayı değiştirmeniz gerekiyorsa, bunu devre dışı bırakın ve sonra yeni bir anlaşma oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f41ab-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="f41ab-123">Yeni anlaşma eski anlaşmayı benziyorsa, eski anlaşmayı kopyalayarak bunu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f41ab-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>

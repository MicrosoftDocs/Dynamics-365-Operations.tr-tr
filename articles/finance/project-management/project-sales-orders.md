---
title: Zaman ve malzeme projeleri için Proje satış siparişleri
description: Bu konu, projeye dayalı satış siparişlerinin zaman ve malzeme projeleri için nasıl oluşturulacağını açıklar.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: d19ee9de70cd14c78a997b7a87c10b53ab3917b0
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249105"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="d961e-103">Zaman ve malzeme projeleri için Proje satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="d961e-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d961e-104">Bu konu, bir proje için satış siparişlerinin nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d961e-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="d961e-105">Satış siparişleri yalnızca **zaman ve malzeme** türünde projeler için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="d961e-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="d961e-106">Proje sözleşmesinde birden fazla finansman kaynağı içeren bir satış ve zaman projesi varsa, **Birden fazla finansman kaynağına sahip projeler için satış siparişlerine izin ver** parametresini **Proje yönetimi ve muhasebe parametreleri** sayfasında etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d961e-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="d961e-107">Birden fazla finansman kaynağına sahip proje satış siparişleri desteği, uygulama sürümü 10.0.2 ve sonrası ile başlar.</span><span class="sxs-lookup"><span data-stu-id="d961e-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="d961e-108">Birden fazla finansman kaynağına sahip proje satış siparişleri için desteği etkinleştirme parametresi, Nisan 2020 sürüm dalgasında kaldırılacaktır, bundan sonra bu özellik her zaman etkin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d961e-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="d961e-109">Proje tabanlı satış siparişlerini iki şekilde oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d961e-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="d961e-110">Projenin kendisine gidin.</span><span class="sxs-lookup"><span data-stu-id="d961e-110">Go to the project itself.</span></span> <span data-ttu-id="d961e-111">Eylem Bölmesinde, **Yönet >Madde görevleri > Satış siparişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d961e-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="d961e-112">Proje bilgisi, projedeki satış siparişine varsayılan olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d961e-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="d961e-113">Proje sözleşmesi, birden fazla finansman kaynağına sahipse, satış siparişi için fonlama kaynağını seçmeniz gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="d961e-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="d961e-114">Proje için yalnızca bir finansman kaynağı varsa, müşteri otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d961e-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="d961e-115">**Tüm satış siparişleri** liste sayfasına gidin ve yeni bir satış siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d961e-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="d961e-116">Satış siparişi için projeyi seçmeniz gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="d961e-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="d961e-117">Proje seçildikten sonra, müşteri finansman kaynağından ayarlanacaktır veya proje sözleşmesi birden fazla finansman kaynağına sahipse, finansman kaynağını seçmeniz gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="d961e-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>


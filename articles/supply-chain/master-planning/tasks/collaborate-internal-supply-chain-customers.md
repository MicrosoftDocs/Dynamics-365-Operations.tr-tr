---
title: İç tedarik zinciri müşterileriyle iş birliği
description: Bu yordam, şirketlerarası satıcı tarafından karşılanacak tüm planlı siparişlerin nasıl görüntüleneceğini gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84c42e550d51e40b7f777c3da67ed765519ddfd0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979292"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="e22cd-103">İç tedarik zinciri müşterileriyle iş birliği</span><span class="sxs-lookup"><span data-stu-id="e22cd-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e22cd-104">Bu yordam, şirketlerarası satıcı tarafından karşılanacak tüm planlı siparişlerin nasıl görüntüleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e22cd-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="e22cd-105">Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.</span><span class="sxs-lookup"><span data-stu-id="e22cd-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="e22cd-106">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e22cd-106">Click Master planning.</span></span>
2. <span data-ttu-id="e22cd-107">Plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e22cd-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="e22cd-108">Plan alanında, plan 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e22cd-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="e22cd-109">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e22cd-109">Click Run.</span></span>
4. <span data-ttu-id="e22cd-110">İş parçacığı sayısı alanına bir rakam girin.</span><span class="sxs-lookup"><span data-stu-id="e22cd-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="e22cd-111">Bu, master planlama için kullanılacak paralel iş parçacıklarının sayısını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="e22cd-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="e22cd-112">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e22cd-112">Click OK.</span></span>
    * <span data-ttu-id="e22cd-113">Bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="e22cd-113">This may take a while.</span></span>  
6. <span data-ttu-id="e22cd-114">Planlanan şirketlerarası talep'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e22cd-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="e22cd-115">Giden planlı şirketlerarası talep'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e22cd-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="e22cd-116">Bu sayfa, bir iç tedarik zinciri sayıcısı tarafından yerine getirilecek tüm planlı talebe genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="e22cd-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="e22cd-117">Yukarı doğru talep ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e22cd-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="e22cd-118">Bu bölümde, talebin nasıl karşılanacağıyla ilgili ayrıntıları görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e22cd-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="e22cd-119">Burada ek bilgiler görmeden önce tedarik şirketinde master planlamanın çalıştırılmasını beklemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e22cd-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  


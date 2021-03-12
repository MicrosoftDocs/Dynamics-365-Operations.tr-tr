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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f39f487ea29bf923c82c08aff56ff5350da0810e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987241"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="bf3e8-103">İç tedarik zinciri müşterileriyle iş birliği</span><span class="sxs-lookup"><span data-stu-id="bf3e8-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf3e8-104">Bu yordam, şirketlerarası satıcı tarafından karşılanacak tüm planlı siparişlerin nasıl görüntüleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="bf3e8-105">Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="bf3e8-106">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-106">Click Master planning.</span></span>
2. <span data-ttu-id="bf3e8-107">Plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="bf3e8-108">Plan alanında, plan 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="bf3e8-109">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-109">Click Run.</span></span>
4. <span data-ttu-id="bf3e8-110">İş parçacığı sayısı alanına bir rakam girin.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="bf3e8-111">Bu, master planlama için kullanılacak paralel iş parçacıklarının sayısını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="bf3e8-112">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-112">Click OK.</span></span>
    * <span data-ttu-id="bf3e8-113">Bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-113">This may take a while.</span></span>  
6. <span data-ttu-id="bf3e8-114">Planlanan şirketlerarası talep'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="bf3e8-115">Giden planlı şirketlerarası talep'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="bf3e8-116">Bu sayfa, bir iç tedarik zinciri sayıcısı tarafından yerine getirilecek tüm planlı talebe genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="bf3e8-117">Yukarı doğru talep ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="bf3e8-118">Bu bölümde, talebin nasıl karşılanacağıyla ilgili ayrıntıları görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="bf3e8-119">Burada ek bilgiler görmeden önce tedarik şirketinde master planlamanın çalıştırılmasını beklemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="bf3e8-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  


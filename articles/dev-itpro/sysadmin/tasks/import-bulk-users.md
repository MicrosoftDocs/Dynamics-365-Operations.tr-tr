---
title: Kullanıcıları topluca içe aktarma
description: Bu yordam, sistem yöneticisi tarafından çok sayıda kullanıcıyı Azure Active Directory'den almak için kullanılabilir.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 339cc1d3bcdc1dc93b796c385d2165f45f8f7ecf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "338740"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="182a4-103">Kullanıcıları topluca içe aktarma</span><span class="sxs-lookup"><span data-stu-id="182a4-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="182a4-104">Bu yordam, sistem yöneticisi tarafından çok sayıda kullanıcıyı Azure Active Directory'den almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="182a4-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="182a4-105">Toplu iş olarak çalıştır</span><span class="sxs-lookup"><span data-stu-id="182a4-105">Run as a batch job</span></span>
1. <span data-ttu-id="182a4-106">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="182a4-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="182a4-107">Toplu içe aktarma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="182a4-107">Click Batch import.</span></span>
3. <span data-ttu-id="182a4-108">Arka planda çalıştır bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="182a4-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="182a4-109">Toplu işleme alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="182a4-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="182a4-110">Görev açıklaması alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="182a4-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="182a4-111">Toplu iş grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="182a4-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="182a4-112">Bu isteğe bağlı bir adımdır.</span><span class="sxs-lookup"><span data-stu-id="182a4-112">This is an optional step.</span></span>  
7. <span data-ttu-id="182a4-113">Özel alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="182a4-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="182a4-114">Bu isteğe bağlı bir adımdır.</span><span class="sxs-lookup"><span data-stu-id="182a4-114">This is an optional step.</span></span>  
8. <span data-ttu-id="182a4-115">Kritik İş alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="182a4-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="182a4-116">Bu isteğe bağlı bir adımdır.</span><span class="sxs-lookup"><span data-stu-id="182a4-116">This is an optional step.</span></span>  
9. <span data-ttu-id="182a4-117">İzleme kategorisi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="182a4-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="182a4-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="182a4-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="182a4-119">Bir korumalı alan ortamında çalıştırın</span><span class="sxs-lookup"><span data-stu-id="182a4-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="182a4-120">Toplu içe aktarma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="182a4-120">Click Batch import.</span></span>
2. <span data-ttu-id="182a4-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="182a4-121">Click OK.</span></span>


---
title: Power Apps Yönetim merkezinde ortam oluşturulamıyor
description: Bu oknu, bir yönetici Microsoft Power Apps Yönetim merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420915"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="9e646-103">Power Apps Yönetim merkezinde ortam oluşturulamıyor</span><span class="sxs-lookup"><span data-stu-id="9e646-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="9e646-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="9e646-104">**Issue**</span></span>

- <span data-ttu-id="9e646-105">Kiracı/ortam yöneticisi, Microsoft Power Apps Yönetici merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9e646-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="9e646-106">Kullanıcılara ortam oluşturma adımını gerçekleştirme hakkı tanıyan bir ortam, bu adımı gerçekleştirmekte olan kullanıcıya doğrudan atanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="9e646-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="9e646-107">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="9e646-107">**Solution**</span></span>

<span data-ttu-id="9e646-108">Kiracı yöneticisinin, geçerli bir Power Apps P2 lisansını doğrudan ortam oluşturma adımını gerçekleştirecek kullanıcıya atamış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9e646-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="9e646-109">Bu hakkı tanıyan Microsoft Dynamics servis planları buradadır.</span><span class="sxs-lookup"><span data-stu-id="9e646-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="9e646-110">Tüm ürün stok tutma birimi (SKU)</span><span class="sxs-lookup"><span data-stu-id="9e646-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="9e646-111">Power Apps P2 servis planı</span><span class="sxs-lookup"><span data-stu-id="9e646-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="9e646-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="9e646-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="9e646-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9e646-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="9e646-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="9e646-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="9e646-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9e646-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="9e646-116">Çeşitli Microsoft Office SKU'larının da bu hakkı, tek başına Power Apps Plan 2 SKU'larıyla birlikte tanıdığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="9e646-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="9e646-117">Buradaki önemli nokta bu SKU'lardan birinin mevcut olması zorunluluğudur.</span><span class="sxs-lookup"><span data-stu-id="9e646-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="9e646-118">[https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) gidin.</span><span class="sxs-lookup"><span data-stu-id="9e646-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="9e646-119">[İnsan Kaynakları sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) içindeki talimatları izleyerek ortamlar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e646-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

---
title: PowerApps Yönetici merkezinde bir ortam oluşturulamıyor
description: Bu oknu, bir yönetici Microsoft PowerApps Yönetim merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519267"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="5d12d-103">PowerApps Yönetici merkezinde ortam oluşturulamıyor</span><span class="sxs-lookup"><span data-stu-id="5d12d-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d12d-104">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="5d12d-104">**Issue**</span></span>

- <span data-ttu-id="5d12d-105">Kiracı/ortam yöneticisi, Microsoft PowerApps Yönetici merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5d12d-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="5d12d-106">Kullanıcılara ortam oluşturma adımını gerçekleştirme hakkı tanıyan bir ortam, bu adımı gerçekleştirmekte olan kullanıcıya doğrudan atanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="5d12d-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="5d12d-107">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="5d12d-107">**Solution**</span></span>

<span data-ttu-id="5d12d-108">Kiracı yöneticisinin, geçerli bir PowerApps P2 lisansını doğrudan ortam oluşturma adımını gerçekleştirecek kullanıcıya atamış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5d12d-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="5d12d-109">Bu hakkı tanıyan Microsoft Dynamics servis planları buradadır.</span><span class="sxs-lookup"><span data-stu-id="5d12d-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="5d12d-110">Tüm ürün stok tutma birimi (SKU)</span><span class="sxs-lookup"><span data-stu-id="5d12d-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="5d12d-111">PowerApps P2 servis planı</span><span class="sxs-lookup"><span data-stu-id="5d12d-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="5d12d-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="5d12d-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="5d12d-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5d12d-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="5d12d-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="5d12d-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="5d12d-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5d12d-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="5d12d-116">Çeşitli Microsoft Office SKU'larının da bu hakkı, tek PowerApps Plan 2 SKU'larıyla birlikte tanıdığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5d12d-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="5d12d-117">Buradaki önemli nokta bu SKU'lardan birinin mevcut olması zorunluluğudur.</span><span class="sxs-lookup"><span data-stu-id="5d12d-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="5d12d-118">[https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) gidin.</span><span class="sxs-lookup"><span data-stu-id="5d12d-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="5d12d-119">[Talent sağlama](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) içindeki talimatları izleyerek ortamlar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5d12d-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

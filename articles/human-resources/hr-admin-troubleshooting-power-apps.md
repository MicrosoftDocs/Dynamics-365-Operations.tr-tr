---
title: Power Apps Yönetim merkezinde ortam oluşturulamıyor
description: Bu oknu, bir yönetici Microsoft Power Apps Yönetim merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053359"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="6640b-103">Power Apps Yönetim merkezinde ortam oluşturulamıyor</span><span class="sxs-lookup"><span data-stu-id="6640b-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6640b-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="6640b-104">**Issue**</span></span>

- <span data-ttu-id="6640b-105">Kiracı/ortam yöneticisi, Microsoft Power Apps Yönetici merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6640b-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="6640b-106">Kullanıcının, ortam oluşturma hakkı veren bir lisansı yok.</span><span class="sxs-lookup"><span data-stu-id="6640b-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="6640b-107">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="6640b-107">**Solution**</span></span>

<span data-ttu-id="6640b-108">Kiracı yöneticisinin, ortamı oluşturan kullanıcıya geçerli bir Power Apps P2 lisansı atadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="6640b-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="6640b-109">Aşağıdaki Microsoft Dynamics hizmet planları ortam oluşturma izni sağlar:</span><span class="sxs-lookup"><span data-stu-id="6640b-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="6640b-110">Tüm ürün stok tutma birimi (SKU)</span><span class="sxs-lookup"><span data-stu-id="6640b-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="6640b-111">Power Apps P2 servis planı</span><span class="sxs-lookup"><span data-stu-id="6640b-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="6640b-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="6640b-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="6640b-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6640b-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="6640b-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="6640b-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="6640b-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6640b-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="6640b-116">Çeşitli Microsoft Office SKU'larının da bu hakkı, tek başına Power Apps Plan 2 SKU'larıyla birlikte tanıdığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="6640b-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="6640b-117">Buradaki önemli nokta bu SKU'lardan birinin mevcut olması zorunluluğudur.</span><span class="sxs-lookup"><span data-stu-id="6640b-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="6640b-118">[https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) gidin.</span><span class="sxs-lookup"><span data-stu-id="6640b-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="6640b-119">[İnsan Kaynakları sağlama](/dynamics365/unified-operations/talent/provisioning-talent) içindeki talimatları izleyerek ortamlar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6640b-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
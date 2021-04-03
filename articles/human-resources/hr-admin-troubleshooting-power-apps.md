---
title: Power Apps Yönetim merkezinde ortam oluşturulamıyor
description: Bu oknu, bir yönetici Microsoft Power Apps Yönetim merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: ec63148364022fe5b8c40d855856eec232af3e48
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463972"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="adbdc-103">Power Apps Yönetim merkezinde ortam oluşturulamıyor</span><span class="sxs-lookup"><span data-stu-id="adbdc-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="adbdc-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="adbdc-104">**Issue**</span></span>

- <span data-ttu-id="adbdc-105">Kiracı/ortam yöneticisi, Microsoft Power Apps Yönetici merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="adbdc-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="adbdc-106">Kullanıcının, ortam oluşturma hakkı veren bir lisansı yok.</span><span class="sxs-lookup"><span data-stu-id="adbdc-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="adbdc-107">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="adbdc-107">**Solution**</span></span>

<span data-ttu-id="adbdc-108">Kiracı yöneticisinin, ortamı oluşturan kullanıcıya geçerli bir Power Apps P2 lisansı atadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="adbdc-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="adbdc-109">Aşağıdaki Microsoft Dynamics hizmet planları ortam oluşturma izni sağlar:</span><span class="sxs-lookup"><span data-stu-id="adbdc-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="adbdc-110">Tüm ürün stok tutma birimi (SKU)</span><span class="sxs-lookup"><span data-stu-id="adbdc-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="adbdc-111">Power Apps P2 servis planı</span><span class="sxs-lookup"><span data-stu-id="adbdc-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="adbdc-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="adbdc-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="adbdc-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="adbdc-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="adbdc-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="adbdc-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="adbdc-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="adbdc-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="adbdc-116">Çeşitli Microsoft Office SKU'larının da bu hakkı, tek başına Power Apps Plan 2 SKU'larıyla birlikte tanıdığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="adbdc-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="adbdc-117">Buradaki önemli nokta bu SKU'lardan birinin mevcut olması zorunluluğudur.</span><span class="sxs-lookup"><span data-stu-id="adbdc-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="adbdc-118">[https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) gidin.</span><span class="sxs-lookup"><span data-stu-id="adbdc-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="adbdc-119">[İnsan Kaynakları sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) içindeki talimatları izleyerek ortamlar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="adbdc-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
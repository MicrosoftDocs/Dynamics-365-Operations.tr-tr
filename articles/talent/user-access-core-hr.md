---
title: Kullanıcı Core HR'a erişebiliyor ancak Onboard'a veya Attract'a erişemiyor
description: Bu konu, kullanıcının Microsoft Dynamics 365 Talent - Core HR'a erişebildiği ancak Attract'a veya Onboard'a erişemediği sorunu ortadan kaldırmayı açıklamaktadır.
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
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009318"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="73c9a-103">Kullanıcı Core HR'a erişebiliyor ancak Onboard'a veya Attract'a erişemiyor</span><span class="sxs-lookup"><span data-stu-id="73c9a-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="73c9a-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="73c9a-104">**Environment details**</span></span>

- <span data-ttu-id="73c9a-105">Microsoft Dynamics Lifecycle Services (LCS) dağıtımı kullanıcı A tarafından yapıldı.</span><span class="sxs-lookup"><span data-stu-id="73c9a-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="73c9a-106">Kullanıcı A, kullanıcı B'yi Microsoft Dynamics 365 Talent: Core HR'a bir kullanıcı olarak ekledi.</span><span class="sxs-lookup"><span data-stu-id="73c9a-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="73c9a-107">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="73c9a-107">**Issue**</span></span>

<span data-ttu-id="73c9a-108">Kullanıcı B, Core HR'a erişebilmektedir ancak Talent: Attract veya Talent: Onboard uygulamasına erişememektedir.</span><span class="sxs-lookup"><span data-stu-id="73c9a-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="73c9a-109">Kullanıcı **Deneyim uygulamalarına** gitmeyi denediğinde, deneme ortamına aktarılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="73c9a-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="73c9a-110">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="73c9a-110">**Solution**</span></span>

<span data-ttu-id="73c9a-111">Kullanıcı B, kullanıcı A'nın sağlama işlemi sırasında oluşturduğu Microsoft PowerApps ortamını görüntülemek için haklar atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="73c9a-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="73c9a-112">Bilgi için, "Ortama erişim hakkı tanımak" bölümüne bkz. [Talent Sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="73c9a-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="73c9a-113">**Uzun vadeli çözüm**</span><span class="sxs-lookup"><span data-stu-id="73c9a-113">**Long-term solution**</span></span>

<span data-ttu-id="73c9a-114">Microsoft, Onboard ve Attract'a uygun hakları bir kullanıcı Core HR'a eklendiğinde otomatik olarak eklemeyi planlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="73c9a-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>

---
title: "Kullanıcılar Core HR'a erişebilir ancak Onboard ve Attract uygulamasına erişemez"
description: "Bu konu, kullanıcının Microsoft Dynamics 365 for Talent Core HR'a erişebildiği ancak Attract veya Onboard'a erişemediği sorunu ortadan kaldırmayı anlatır."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="4687b-103">Kullanıcılar Core HR'a erişebilir ancak Onboard ve Attract uygulamasına erişemez</span><span class="sxs-lookup"><span data-stu-id="4687b-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4687b-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="4687b-104">**Environment details**</span></span>

- <span data-ttu-id="4687b-105">Microsoft Dynamics Lifecycle Services (LCS) dağıtımı kullanıcı A tarafından yapıldı.</span><span class="sxs-lookup"><span data-stu-id="4687b-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="4687b-106">Kullanıcı A, kullanıcı B'yi Microsoft Dynamics 365 for Talent Core HR'a bir kullanıcı olarak ekledi.</span><span class="sxs-lookup"><span data-stu-id="4687b-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="4687b-107">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="4687b-107">**Issue**</span></span>

<span data-ttu-id="4687b-108">Kullanıcı B, Core HR'a erişebilmektedir ancak Talent: Attract veya Talent: Onboard uygulamasına erişememektedir.</span><span class="sxs-lookup"><span data-stu-id="4687b-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="4687b-109">Kullanıcı **Deneyim uygulamalarına** gitmeyi denediğinde, deneme ortamına aktarılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4687b-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="4687b-110">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="4687b-110">**Solution**</span></span>

<span data-ttu-id="4687b-111">Kullanıcı B, kullanıcı A'nın sağlama işlemi sırasında oluşturduğu Microsoft PowerApps ortamını görüntülemek için haklar atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4687b-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="4687b-112">Bilgi için, "Ortama erişim hakkı tanımak" bölümüne bkz. [Talent Sağlama](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="4687b-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="4687b-113">**Uzun vadeli çözüm**</span><span class="sxs-lookup"><span data-stu-id="4687b-113">**Long-term solution**</span></span>

<span data-ttu-id="4687b-114">Microsoft, Onboard ve Attract'a uygun hakları bir kullanıcı Core HR'a eklendiğinde otomatik olarak eklemeyi planlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4687b-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>


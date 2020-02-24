---
title: Kullanıcı Human Resources'a erişebiliyor ancak Onboard veya Attract'a erişemiyor
description: Bu konu, kullanıcının Microsoft Dynamics 365 Talent - İnsan Kaynaklarına erişebildiği ancak Attract'e veya Onboard'a erişemediği sorunu ortadan kaldırmayı açıklamaktadır.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006322"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="a8b0d-103">Kullanıcı Human Resources'a erişebiliyor ancak Onboard veya Attract'a erişemiyor</span><span class="sxs-lookup"><span data-stu-id="a8b0d-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8b0d-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="a8b0d-104">**Environment details**</span></span>

- <span data-ttu-id="a8b0d-105">Microsoft Dynamics Lifecycle Services (LCS) dağıtımı kullanıcı A tarafından yapıldı.</span><span class="sxs-lookup"><span data-stu-id="a8b0d-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="a8b0d-106">Kullanıcı A, kullanıcı B'yi Microsoft Dynamics 365 Human Resources'a bir kullanıcı olarak ekledi.</span><span class="sxs-lookup"><span data-stu-id="a8b0d-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a8b0d-107">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="a8b0d-107">**Issue**</span></span>

<span data-ttu-id="a8b0d-108">Kullanıcı B, İnsan Kaynakları'na erişebilmektedir ancak Talent: Attract veya Talent: Onboard uygulamasına erişememektedir.</span><span class="sxs-lookup"><span data-stu-id="a8b0d-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="a8b0d-109">Kullanıcı **Deneyim uygulamalarına** gitmeyi denediğinde, deneme ortamına aktarılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a8b0d-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="a8b0d-110">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="a8b0d-110">**Solution**</span></span>

<span data-ttu-id="a8b0d-111">Kullanıcı B, kullanıcı A'nın sağlama işlemi sırasında oluşturduğu Microsoft Power Apps ortamını görüntülemek için haklar atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a8b0d-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="a8b0d-112">Bilgi için, "Ortama erişim hakkı tanımak" bölümüne bkz. [Talent Sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="a8b0d-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="a8b0d-113">**Uzun vadeli çözüm**</span><span class="sxs-lookup"><span data-stu-id="a8b0d-113">**Long-term solution**</span></span>

<span data-ttu-id="a8b0d-114">Microsoft, Onboard ve Attract'e uygun hakları bir kullanıcı İnsan Kaynakları'na eklendiğinde otomatik olarak eklemeyi planlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="a8b0d-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>

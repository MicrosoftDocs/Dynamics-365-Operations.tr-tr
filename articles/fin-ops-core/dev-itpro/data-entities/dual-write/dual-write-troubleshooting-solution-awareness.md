---
title: Çözüm farkındalığıyla ilgili sorunları giderme
description: Bu konu, çözüm farkındalığıyla ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 79b2920b80ce4a8b419c2a146e15babc061cf64d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683586"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="2736e-103">Çözüm farkındalığıyla ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="2736e-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="2736e-104">Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="2736e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="2736e-105">Bu konu, çözüm farkındalığıyla ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="2736e-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2736e-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="2736e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="2736e-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2736e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="2736e-108">Çift-yazma sayfasında hata</span><span class="sxs-lookup"><span data-stu-id="2736e-108">Error on the Dual-write page</span></span>

<span data-ttu-id="2736e-109">**Çift-yazılır** sayfada aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="2736e-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="2736e-110">*namemapping='Logical' bulunan, adı 'msdyn\_dualwriteentitymap' olan varlık MetadataCache içinde bulunamadı.*</span><span class="sxs-lookup"><span data-stu-id="2736e-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="2736e-111">Bu sorunu gidermek için, Çift-Write Core çözümünün Dataverse'te yüklü olduğundan emin olun .</span><span class="sxs-lookup"><span data-stu-id="2736e-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="2736e-112">Çift-yazılır çekirdek çözümü, çözüm tanıma için bir önkoşuldur.</span><span class="sxs-lookup"><span data-stu-id="2736e-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>

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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172633"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="e76f3-103">Çözüm farkındalığıyla ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="e76f3-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e76f3-104">Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="e76f3-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="e76f3-105">Bu konu, çözüm farkındalığıyla ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="e76f3-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e76f3-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e76f3-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="e76f3-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e76f3-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="e76f3-108">Çift-yazma sayfasında hata</span><span class="sxs-lookup"><span data-stu-id="e76f3-108">Error on the Dual-write page</span></span>

<span data-ttu-id="e76f3-109">**Çift-yazılır** sayfada aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e76f3-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="e76f3-110">*namemapping='Logical' bulunan, adı 'msdyn\_dualwriteentitymap' olan varlık MetadataCache içinde bulunamadı.*</span><span class="sxs-lookup"><span data-stu-id="e76f3-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="e76f3-111">Bu sorunu gidermek için, Çift-Write Core çözümünün Common Data Service'te yüklü olduğundan emin olun .</span><span class="sxs-lookup"><span data-stu-id="e76f3-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="e76f3-112">Çift-yazılır çekirdek çözümü, çözüm tanıma için bir önkoşuldur.</span><span class="sxs-lookup"><span data-stu-id="e76f3-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>

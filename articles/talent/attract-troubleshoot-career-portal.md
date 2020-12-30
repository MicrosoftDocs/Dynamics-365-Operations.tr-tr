---
title: Attract kullanıcıları kariyer portalından iş başvurusunda bulunamıyor
description: Bu konu, kullanıcıların kariyer portalı 'ndan iş için uygulayabileceği bir sorunun nasıl giderileceğini açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462794"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="e2bcf-103">Attract kullanıcıları kariyer portalından iş başvurusunda bulunamıyor</span><span class="sxs-lookup"><span data-stu-id="e2bcf-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="e2bcf-104">Çıkış</span><span class="sxs-lookup"><span data-stu-id="e2bcf-104">Issue</span></span>

<span data-ttu-id="e2bcf-105">Attract kullanıcıları kariyer portalından iş başvurusunda bulunamıyor.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="e2bcf-106">Dynamics 365 Talent: Attract'De oluşturulan bir iş için uygulamaya çalıştıklarında , tarayıcı sayfayı devamlı olarak yükler ve eylemi tamammaz.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="e2bcf-107">Nedeni</span><span class="sxs-lookup"><span data-stu-id="e2bcf-107">Cause</span></span>

<span data-ttu-id="e2bcf-108">Bu sorun, Talent Relationship Ekibinin Talent kullanıcı rolü yoksa oluşur.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="e2bcf-109">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="e2bcf-109">Resolution</span></span>

<span data-ttu-id="e2bcf-110">Talent Relationship Ekibine Talent kullanıcı atayın.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="e2bcf-111">[Power Platform Yönetim Merkezi'nde](https://admin.powerplatform.microsoft.com) aşağıdaki yönetici kimlik bilgileriyle oturum açın:</span><span class="sxs-lookup"><span data-stu-id="e2bcf-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="e2bcf-112">Dynamics 365 Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="e2bcf-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="e2bcf-113">Genel Yönetim</span><span class="sxs-lookup"><span data-stu-id="e2bcf-113">Global admin</span></span>
   - <span data-ttu-id="e2bcf-114">Power Platform yöneticisi</span><span class="sxs-lookup"><span data-stu-id="e2bcf-114">Power Platform admin</span></span>

2. <span data-ttu-id="e2bcf-115">Gezinti bölmesinde, **ortamlar** 'ı seçin ve sonra taödünç verilen ilişki ekibine, Talent kullanıcı rolünün atanacağı ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Ortam Seç](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="e2bcf-117">**Ortamlar** bölmesinde, **ortam URL**'sini seçin ve ortamın yönetim portalında oturum açın (örneğin, https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="e2bcf-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="e2bcf-118">**Ayarlar**'ı seçin, **sistem**'i seçin ve sonra **güvenlik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Güvenliğe git](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="e2bcf-120">**Takımları** seçin .</span><span class="sxs-lookup"><span data-stu-id="e2bcf-120">Select **Teams**.</span></span>

   ![Takımları seçin](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="e2bcf-122">Arama kutusunda **Talent Relationship ekibini** arayın ve sonra arama sonuçlarından takımı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="e2bcf-123">Şeritten **ROLLERİ YÖNET** seçin.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="e2bcf-124">**Takım Rollerini Yönet** iletişim kutusunda, kullanılabilir roller listesinden **Talent kullanıcısı**' yı seçin ve sonra rolü uygulamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Rolü Uygula](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="e2bcf-126">Değişikliklerinizi test edin:</span><span class="sxs-lookup"><span data-stu-id="e2bcf-126">Test your changes:</span></span>

   1. <span data-ttu-id="e2bcf-127">Yeni bir tarayıcı penceresinden kariyer portalı 'nda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="e2bcf-128">Kariyer portalından iş için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="e2bcf-128">Apply for the job from the career portal.</span></span> 
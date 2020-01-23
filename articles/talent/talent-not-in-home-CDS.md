---
title: Talent Microsoft Dynamics 365 uygulamaları (Common Data Service 1.0) arasında görünmüyor
description: Bu konu, bir müşteri Microsoft Dynamics 365 uygulamaları arasında Microsoft Dynamics 365 Talent'ı görmüyorsa ne yapılacağı açıklar.
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
ms.openlocfilehash: a44d2e43752960d3026fa7ac92c7b261aee05448
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897039"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="8f9a4-103">Talent Microsoft Dynamics 365 uygulamaları (Common Data Service 1.0) arasında görünmüyor</span><span class="sxs-lookup"><span data-stu-id="8f9a4-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

<span data-ttu-id="8f9a4-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="8f9a4-104">**Issue**</span></span>

<span data-ttu-id="8f9a4-105">Müşteri, Microsoft Dynamics 365 Talent uygulamasını Microsoft Dynamics 365 uygulamaları arasında göremez.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="8f9a4-106">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="8f9a4-106">**Resolution**</span></span>

<span data-ttu-id="8f9a4-107">Kullanıcı, Microsoft Power Apps içinde Ortam Oluşturucu rolüne eklenmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="8f9a4-108">[Power Apps Yönetim portalını](https://preview.admin.powerapps.com/) Power Apps Plan 2 lisansına sahip yönetici kullanıcı açmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="8f9a4-109">**Ortamlar**'ı seçin ve Talent için doğru ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="8f9a4-110">**Güvenlik** sekmesinde, **Ortam rolleri** sekmesinde **Ortam Oluşturucu**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Ortam rolleri sekmesi](media/environment-roles.png)

4. <span data-ttu-id="8f9a4-112">**Kullanıcılar** sekmesinde, kullanıcıyı kuruluşunuza ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Kullanıcılar sekmesi](media/environment-maker.png)

5. <span data-ttu-id="8f9a4-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-114">Select **Save**.</span></span>
6. <span data-ttu-id="8f9a4-115">Kullanıcının şimdi [Microsoft Dynamics 365'e oturum açması gerekir](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="8f9a4-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="8f9a4-116">Kullanıcı uygulamalarını güncelleştirmek için **Eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-116">Select **Sync** to update the user apps.</span></span>

    ![Eşitleme düğmesi](media/get-more.png)

    <span data-ttu-id="8f9a4-118">Eşitleme tamamlandıktan sonra, Talent ana sayfada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8f9a4-118">After synchronization is completed, Talent will appear on the home page.</span></span>

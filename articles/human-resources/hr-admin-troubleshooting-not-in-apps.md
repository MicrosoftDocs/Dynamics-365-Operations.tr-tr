---
title: İnsan Kaynakları Microsoft Dynamics 365 uygulamalarında görünmez
description: Bu konu, bir müşteri Microsoft Dynamics 365 uygulamaları arasında Microsoft Dynamics 365 Human Resources'ı görmüyorsa ne yapılacağı açıklar.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010936"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="ec7e0-103">İnsan Kaynakları Microsoft Dynamics 365 uygulamalarında görünmez</span><span class="sxs-lookup"><span data-stu-id="ec7e0-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="ec7e0-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="ec7e0-104">**Issue**</span></span>

<span data-ttu-id="ec7e0-105">Müşteri, Dynamics 365 Human Resources'ı Microsoft Dynamics 365 uygulamaları arasında görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="ec7e0-106">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="ec7e0-106">**Resolution**</span></span>

<span data-ttu-id="ec7e0-107">Kullanıcı, Microsoft Power Apps içinde Ortam Oluşturucu rolüne eklenmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="ec7e0-108">[Power Apps Yönetim portalını](https://preview.admin.powerapps.com/) Power Apps Plan 2 lisansına sahip yönetici kullanıcı açmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="ec7e0-109">**Ortamlar**'ı seçin ve İnsan Kaynakları için doğru ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="ec7e0-110">**Güvenlik** sekmesinde, **Ortam rolleri** sekmesinde **Ortam Oluşturucu**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Ortam rolleri sekmesi](media/environment-roles.png)

4. <span data-ttu-id="ec7e0-112">**Kullanıcılar** sekmesinde, kullanıcıyı kuruluşunuza ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Kullanıcılar sekmesi](media/environment-maker.png)

5. <span data-ttu-id="ec7e0-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-114">Select **Save**.</span></span>

6. <span data-ttu-id="ec7e0-115">Kullanıcının şimdi [Microsoft Dynamics 365'e oturum açması gerekir](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="ec7e0-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="ec7e0-116">Kullanıcı uygulamalarını güncelleştirmek için **Eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-116">Select **Sync** to update the user apps.</span></span>

    ![Eşitleme düğmesi](media/get-more.png)

    <span data-ttu-id="ec7e0-118">Eşitleme tamamlandıktan sonra, İnsan Kaynakları ana sayfada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ec7e0-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>

---
title: İnsan Kaynakları Microsoft Dynamics 365 uygulamalarında görünmez
description: Bu konu, bir müşteri Microsoft Dynamics 365 uygulamaları arasında Microsoft Dynamics 365 Human Resources'ı görmüyorsa ne yapılacağı açıklar.
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
ms.openlocfilehash: 17a454cd32a08db105a13577c32368ad819bed1c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053388"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="757ec-103">İnsan Kaynakları Microsoft Dynamics 365 uygulamalarında görünmez</span><span class="sxs-lookup"><span data-stu-id="757ec-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="757ec-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="757ec-104">**Issue**</span></span>

<span data-ttu-id="757ec-105">Müşteri, Dynamics 365 Human Resources'ı Microsoft Dynamics 365 uygulamaları arasında görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="757ec-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="757ec-106">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="757ec-106">**Resolution**</span></span>

<span data-ttu-id="757ec-107">Kullanıcı, Microsoft Power Apps içinde Ortam Oluşturucu rolüne eklenmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="757ec-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="757ec-108">[Power Apps Yönetim portalını](https://preview.admin.powerapps.com/) Power Apps Plan 2 lisansına sahip yönetici kullanıcı açmalıdır.</span><span class="sxs-lookup"><span data-stu-id="757ec-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="757ec-109">**Ortamlar**'ı seçin ve İnsan Kaynakları için doğru ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="757ec-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="757ec-110">**Güvenlik** sekmesinde, **Ortam rolleri** sekmesinde **Ortam Oluşturucu**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="757ec-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Ortam rolleri sekmesi](media/environment-roles.png)

4. <span data-ttu-id="757ec-112">**Kullanıcılar** sekmesinde, kullanıcıyı kuruluşunuza ekleyin.</span><span class="sxs-lookup"><span data-stu-id="757ec-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Kullanıcılar sekmesi](media/environment-maker.png)

5. <span data-ttu-id="757ec-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="757ec-114">Select **Save**.</span></span>

6. <span data-ttu-id="757ec-115">Kullanıcının şimdi [Microsoft Dynamics 365'e oturum açması gerekir](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="757ec-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="757ec-116">Kullanıcı uygulamalarını güncelleştirmek için **Eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="757ec-116">Select **Sync** to update the user apps.</span></span>

    ![Eşitleme düğmesi](media/get-more.png)

    <span data-ttu-id="757ec-118">Eşitleme tamamlandıktan sonra, İnsan Kaynakları ana sayfada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="757ec-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
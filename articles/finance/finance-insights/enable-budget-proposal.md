---
title: Bütçe tekliflerini etkinleştirme (önizleme)
description: Bu konuda, Mali İçgörüler'de Bütçe teklifi özelliğinin nasıl açılacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222546"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="72924-103">Bütçe tekliflerini etkinleştirme (önizleme)</span><span class="sxs-lookup"><span data-stu-id="72924-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="72924-104">Bu konuda, Mali İçgörüler'de Bütçe teklifi özelliğinin nasıl açılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="72924-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="72924-105">Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="72924-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="72924-106">Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="72924-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="72924-107">(Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="72924-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="72924-108">Sürüm 10.0.20 veya sonrasını kullanıyorsanız veya bir Service Fabric dağıtımı kullanıyorsanız bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="72924-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="72924-109">Mali içgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="72924-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="72924-110">Özelliği **Özellik yönetimi** çalışma alanında görmüyorsanız veya özelliği açmaya çalışırken sorun yaşıyorsanız <fiap@microsoft.com> adresiyle iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="72924-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="72924-111">**Özellik yönetimi** çalışma alanını açın ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="72924-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="72924-112">**Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="72924-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="72924-113">**Bütçe teklifi**'ni arayın ve bu özelliği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="72924-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="72924-114">**Bütçeleme \> Kurulum \> Temel Bütçeleme \> Bütçe teklifi (önizleme)** bölümüne gidin ve **Özelliği etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="72924-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Bütçe tekliflerini etkinleştirme (önizleme)
description: Bu konuda, Mali İçgörüler'de Bütçe teklifi özelliğinin nasıl açılacağı açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 3a2060d082ed55e3b6fac506898916942ccc9db7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208497"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="3b57b-103">Bütçe tekliflerini etkinleştirme (önizleme)</span><span class="sxs-lookup"><span data-stu-id="3b57b-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3b57b-104">Bu konuda, Mali İçgörüler'de Bütçe teklifi özelliğinin nasıl açılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="3b57b-105">Ortamın birincil Azure SQL kurulumuna bağlanmak için Microsoft Dynamics Lifecycle Services (LCS) portalındaki ortam sayfasında yer alan bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="3b57b-106">Korumalı alan ortamına sınırlı dağıtımları açmak için aşağıdaki Transact-SQL (T-SQL) komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3b57b-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="3b57b-107">(Uygulama Nesne Sunucusu \[AOS\] hizmetine uzaktan bağlanmadan önce IP adresinize erişimi açmanız gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="3b57b-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="3b57b-108">Microsoft Dynamics 365 Finance dağıtımınız Service Fabric dağıtımıysa bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b57b-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="3b57b-109">Mali İçgörüler ekibi, bu sınırlı dağıtımı sizin için açmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3b57b-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="3b57b-110">Özelliği, **Özellik yönetimi** çalışma alanında göremiyorsanız veya açmaya çalıştığınızda sorunlarla karşılaşıyorsanız [Mali İçgörüler Uygulaması Önizleme ekibine](mailto:fiap@microsoft.com) e-posta gönderin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="3b57b-111">**Özellik yönetimi** çalışma alanını açın ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="3b57b-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="3b57b-112">**Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="3b57b-113">**Bütçe teklifi**'ni arayın ve bu özelliği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="3b57b-114">**Bütçeleme \> Kurulum \> Temel Bütçeleme \> Bütçe teklifi (önizleme)** bölümüne gidin ve **Özelliği etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3b57b-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="3b57b-115">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="3b57b-115">Privacy notice</span></span>
<span data-ttu-id="3b57b-116">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="3b57b-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
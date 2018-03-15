--- 
title: " Perakende ekstreleri için parametre yapılandırmaları"
description: "Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende parametrelerine ilişkin yapılandırmaları gösterir."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 0c93633e92221264cc6a67c74d62edaa59bdbd2f
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="6a80b-103"> Perakende ekstreleri için parametre yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="6a80b-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6a80b-104">Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende parametrelerine ilişkin yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a80b-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="6a80b-105">Bu yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6a80b-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="6a80b-106">Perakende ve ticaret > Genel merkez kurulumu  > Parametreler > Perakende parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="6a80b-107">Deftere nakil sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6a80b-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="6a80b-108">Özellikle periyodik iskonto tutarlarını deftere nakletmek istiyorsanız "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="6a80b-109">Varsayılan hesapları kullanmak için "Standart", her periyodik iskonto için hangi hesabın kullanılacağını belirlemek istiyorsanız "Periyodik" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="6a80b-110">Mümkün olduğunda stok satırlarının toplanması için "Özet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="6a80b-111">Ekstre deftere nakil işleminin bir parçası olarak Faturaların ve Ödemelerin otomatik kapatılmasını istiyorsanız "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="6a80b-112">Kasaya para nakli hareketlerinin toplanması gerekiyorsa "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="6a80b-113">Bankaya para nakli hareketlerinin toplanması gerekiyorsa "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="6a80b-114">Ekstre deftere nakil işleminde toplamı açmak için "Evet" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="6a80b-115">Siparişleri ekstreler deftere nakledilirken oluşturmak ve işlemek için "Evet" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="6a80b-116">Her toplu iş görevinde işlenecek maksimum sipariş sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="6a80b-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="6a80b-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6a80b-117">Click Save.</span></span>



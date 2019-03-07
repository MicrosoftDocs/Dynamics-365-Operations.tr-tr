---
title: " Perakende ekstreleri için parametre yapılandırmaları"
description: Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende parametrelerine ilişkin yapılandırmaları gösterir.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "352632"
---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="84765-103"> Perakende ekstreleri için parametre yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="84765-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="84765-104">Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende parametrelerine ilişkin yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="84765-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="84765-105">Bu yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="84765-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="84765-106">Perakende ve ticaret > Genel merkez kurulumu  > Parametreler > Perakende parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="84765-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="84765-107">Deftere nakil sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84765-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="84765-108">Özellikle periyodik iskonto tutarlarını deftere nakletmek istiyorsanız "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="84765-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="84765-109">Varsayılan hesapları kullanmak için "Standart", her periyodik iskonto için hangi hesabın kullanılacağını belirlemek istiyorsanız "Periyodik" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="84765-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="84765-110">Mümkün olduğunda stok satırlarının toplanması için "Özet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="84765-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="84765-111">Ekstre deftere nakil işleminin bir parçası olarak Faturaların ve Ödemelerin otomatik kapatılmasını istiyorsanız "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="84765-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="84765-112">Kasaya para nakli hareketlerinin toplanması gerekiyorsa "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="84765-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="84765-113">Bankaya para nakli hareketlerinin toplanması gerekiyorsa "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="84765-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="84765-114">Ekstre deftere nakil işleminde toplamı açmak için "Evet" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="84765-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="84765-115">Siparişleri ekstreler deftere nakledilirken oluşturmak ve işlemek için "Evet" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="84765-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="84765-116">Her toplu iş görevinde işlenecek maksimum sipariş sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="84765-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="84765-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84765-117">Click Save.</span></span>


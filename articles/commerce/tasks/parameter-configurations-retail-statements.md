---
title: Perakende ekstrelerini etkileyen parametrelerini yapılandırma
description: Bu konu, ekstrelerinin oluşturulması ve nakledilmesini etkileyen Commerce parametrelerine ilişkin yapılandırmaları gösterir.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 7892a216d836ebcc297a5b7eb87bc996dd9b91bf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140860"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="b373a-103">Perakende ekstrelerini etkileyen parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b373a-103">Configure parameters that affect retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b373a-104">Bu konu, ekstrelerinin oluşturulması ve nakledilmesini etkileyen Commerce parametrelerine ilişkin yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="b373a-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="b373a-105">Bu yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b373a-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="b373a-106">Gezinme panelinde **Modüller > Perakende ve Ticaret > Genel merkez ayarı   > Parametreler > Ticaret parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b373a-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="b373a-107">**Deftere nakletme** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="b373a-108">Özellikle periyodik iskonto tutarlarını deftere nakletmek istiyorsanız **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="b373a-109">Varsayılan hesapları kullanmak için **Standart**i her periyodik iskonto için hangi hesabın kullanılacağını belirlemek istiyorsanız **Periyodik** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="b373a-110">Mümkün olduğunda stok satırlarının toplanması için **Özet**i seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="b373a-111">Ekstre deftere nakil işleminin bir parçası olarak Faturaların ve Ödemelerin otomatik kapatılmasını istiyorsanız **Evet**i seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="b373a-112">Kasaya para nakli hareketlerinin toplanması gerekiyorsa **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="b373a-113">Bankaya para nakli hareketlerinin toplanması gerekiyorsa **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="b373a-114">Ekstre deftere nakil işleminde toplamı açmak için **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="b373a-115">Siparişleri ekstreler deftere nakledilirken oluşturmak ve işlemek için **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="b373a-116">Her toplu iş görevinde işlenecek maksimum sipariş sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="b373a-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="b373a-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b373a-117">Select **Save**.</span></span>


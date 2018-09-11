--- 
title: "Ürün yapılandırma modeline hesaplama ekleme"
description: "Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: bdd596e93301bceb9261d531264dc42299ca36c6
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="a3e4e-103">Ürün yapılandırma modeline hesaplama ekleme</span><span class="sxs-lookup"><span data-stu-id="a3e4e-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3e4e-104">Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3e4e-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="a3e4e-105">Beyaz hoparlörler için hoparlör yüksekliğini 10 ve diğer dolaplar için 15 olarak ayarlamak için "If" işlecini kullanarak bir mantıksal ifadeyi nasıl oluşturabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3e4e-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="a3e4e-106">Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a3e4e-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="a3e4e-107">Hesaplama ekleme</span><span class="sxs-lookup"><span data-stu-id="a3e4e-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="a3e4e-108">Hesaplama ifadesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3e4e-108">Create calculation expression</span></span>
1. <span data-ttu-id="a3e4e-109">İfadeyi düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a3e4e-109">Click Edit expression.</span></span>
2. <span data-ttu-id="a3e4e-110">ConstraintBody alanında, 'If[CabinetFinish=="White", 10, 15]' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="a3e4e-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="a3e4e-111">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a3e4e-111">Click Validate.</span></span>
4. <span data-ttu-id="a3e4e-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a3e4e-112">Click Close.</span></span>
5. <span data-ttu-id="a3e4e-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a3e4e-113">Click OK.</span></span>



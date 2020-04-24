---
title: Ürün yapılandırma modeline hesaplama ekleme
description: Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32bc2ac5815c2739147664f1e1df2528178db51e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213412"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="c0ebf-103">Ürün yapılandırma modeline hesaplama ekleme</span><span class="sxs-lookup"><span data-stu-id="c0ebf-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0ebf-104">Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0ebf-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="c0ebf-105">Beyaz hoparlörler için hoparlör yüksekliğini 10 ve diğer dolaplar için 15 olarak ayarlamak için "If" işlecini kullanarak bir mantıksal ifadeyi nasıl oluşturabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0ebf-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="c0ebf-106">Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c0ebf-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="c0ebf-107">Hesaplama ekleme</span><span class="sxs-lookup"><span data-stu-id="c0ebf-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="c0ebf-108">Hesaplama ifadesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c0ebf-108">Create calculation expression</span></span>
1. <span data-ttu-id="c0ebf-109">İfadeyi düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c0ebf-109">Click Edit expression.</span></span>
2. <span data-ttu-id="c0ebf-110">ConstraintBody alanında, 'If[CabinetFinish=="White", 10, 15]' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="c0ebf-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="c0ebf-111">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0ebf-111">Click Validate.</span></span>
4. <span data-ttu-id="c0ebf-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0ebf-112">Click Close.</span></span>
5. <span data-ttu-id="c0ebf-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0ebf-113">Click OK.</span></span>


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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e23d33c6911310cca6aac0df4589e909568a86a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258083"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="ef170-103">Ürün yapılandırma modeline hesaplama ekleme</span><span class="sxs-lookup"><span data-stu-id="ef170-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef170-104">Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir hesaplama ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef170-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="ef170-105">Beyaz hoparlörler için hoparlör yüksekliğini 10 ve diğer dolaplar için 15 olarak ayarlamak için "If" işlecini kullanarak bir mantıksal ifadeyi nasıl oluşturabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef170-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="ef170-106">Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ef170-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="ef170-107">Hesaplama ekleme</span><span class="sxs-lookup"><span data-stu-id="ef170-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="ef170-108">Hesaplama ifadesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ef170-108">Create calculation expression</span></span>
1. <span data-ttu-id="ef170-109">İfadeyi düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ef170-109">Click Edit expression.</span></span>
2. <span data-ttu-id="ef170-110">ConstraintBody alanında, 'If[CabinetFinish=="White", 10, 15]' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="ef170-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="ef170-111">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef170-111">Click Validate.</span></span>
4. <span data-ttu-id="ef170-112">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef170-112">Click Close.</span></span>
5. <span data-ttu-id="ef170-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef170-113">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Ürün yapılandırma modeline bir ifade kısıtlaması ekleme
description: Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 411e20bd8631b70df981c5785f502693d5ba3705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987141"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="43f39-103">Ürün yapılandırma modeline bir ifade kısıtlaması ekleme</span><span class="sxs-lookup"><span data-stu-id="43f39-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43f39-104">Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="43f39-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="43f39-105">Kullanıcı ön ızgarayı metal olarak seçtiyse bir hoparlöre köşe koruması uygulanması gerektiğini nasıl zorunlu kılacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="43f39-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="43f39-106">Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.</span><span class="sxs-lookup"><span data-stu-id="43f39-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="43f39-107">Bir ifade kısıtlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="43f39-107">Create an expression constraint</span></span>
1. <span data-ttu-id="43f39-108">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43f39-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="43f39-109">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43f39-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="43f39-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="43f39-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="43f39-111">Bu örnek, son teknoloji hoparlör modeli kullanır.</span><span class="sxs-lookup"><span data-stu-id="43f39-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="43f39-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43f39-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="43f39-113">Sınırlamalar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="43f39-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="43f39-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="43f39-114">Click Add.</span></span>
7. <span data-ttu-id="43f39-115">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43f39-115">Click Create.</span></span>
8. <span data-ttu-id="43f39-116">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="43f39-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="43f39-117">İfade girin</span><span class="sxs-lookup"><span data-stu-id="43f39-117">Enter expression</span></span>
1. <span data-ttu-id="43f39-118">İfadeyi düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="43f39-118">Click Edit expression.</span></span>
    * <span data-ttu-id="43f39-119">Bu aşamada görev kaydında kullanıcı arabiriminin kilidini açarsanız, kısıtlama ifadesi oluşturmak için IntelliSense'i ve simgeler listesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43f39-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="43f39-120">ConstraintBody alanında, 'Implies[FrontGrill=="Metal", CornerProtection] ' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="43f39-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="43f39-121">Bu ifade mantığı şu anlamdadır: Ön ızgara metalse, köşe koruma seçeneği seçili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="43f39-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="43f39-122">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43f39-122">Click Validate.</span></span>
    * <span data-ttu-id="43f39-123">Doğrulama işlevi, kısıtlama ifadesini gözden geçirir ve sözdizimi hatalarını denetler.</span><span class="sxs-lookup"><span data-stu-id="43f39-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="43f39-124">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43f39-124">Click Close.</span></span>
5. <span data-ttu-id="43f39-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43f39-125">Click OK.</span></span>


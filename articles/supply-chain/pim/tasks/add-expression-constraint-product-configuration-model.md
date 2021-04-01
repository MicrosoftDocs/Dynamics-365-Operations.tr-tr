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
ms.openlocfilehash: 81026d8622d3f03b3b87747800f4845cda823569
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256171"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="7a6b2-103">Ürün yapılandırma modeline bir ifade kısıtlaması ekleme</span><span class="sxs-lookup"><span data-stu-id="7a6b2-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a6b2-104">Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="7a6b2-105">Kullanıcı ön ızgarayı metal olarak seçtiyse bir hoparlöre köşe koruması uygulanması gerektiğini nasıl zorunlu kılacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="7a6b2-106">Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="7a6b2-107">Bir ifade kısıtlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a6b2-107">Create an expression constraint</span></span>
1. <span data-ttu-id="7a6b2-108">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="7a6b2-109">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="7a6b2-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7a6b2-111">Bu örnek, son teknoloji hoparlör modeli kullanır.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="7a6b2-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7a6b2-113">Sınırlamalar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="7a6b2-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-114">Click Add.</span></span>
7. <span data-ttu-id="7a6b2-115">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-115">Click Create.</span></span>
8. <span data-ttu-id="7a6b2-116">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="7a6b2-117">İfade girin</span><span class="sxs-lookup"><span data-stu-id="7a6b2-117">Enter expression</span></span>
1. <span data-ttu-id="7a6b2-118">İfadeyi düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-118">Click Edit expression.</span></span>
    * <span data-ttu-id="7a6b2-119">Bu aşamada görev kaydında kullanıcı arabiriminin kilidini açarsanız, kısıtlama ifadesi oluşturmak için IntelliSense'i ve simgeler listesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="7a6b2-120">ConstraintBody alanında, 'Implies[FrontGrill=="Metal", CornerProtection] ' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="7a6b2-121">Bu ifade mantığı şu anlamdadır: Ön ızgara metalse, köşe koruma seçeneği seçili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="7a6b2-122">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-122">Click Validate.</span></span>
    * <span data-ttu-id="7a6b2-123">Doğrulama işlevi, kısıtlama ifadesini gözden geçirir ve sözdizimi hatalarını denetler.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="7a6b2-124">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-124">Click Close.</span></span>
5. <span data-ttu-id="7a6b2-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a6b2-125">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
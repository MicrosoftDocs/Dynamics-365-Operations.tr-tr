---
title: Ürün yapılandırma modeline bir ifade kısıtlaması ekleme
description: Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920893"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="98337-103">Ürün yapılandırma modeline bir ifade kısıtlaması ekleme</span><span class="sxs-lookup"><span data-stu-id="98337-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98337-104">Bu yordam, bir ürün yapılandırma modeli için nasıl yeni bir kısıtlama ifadesi ekleyebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="98337-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="98337-105">Kullanıcı ön ızgarayı metal olarak seçtiyse bir hoparlöre köşe koruması uygulanması gerektiğini nasıl zorunlu kılacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="98337-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="98337-106">Yordam, USMF demo şirketindeki Son teknoloji hoparlör bileşenini kullanır.</span><span class="sxs-lookup"><span data-stu-id="98337-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="98337-107">Bir ifade kısıtlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="98337-107">Create an expression constraint</span></span>

1. <span data-ttu-id="98337-108">**Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="98337-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="98337-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="98337-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="98337-110">Bu örnek, son teknoloji hoparlör modeli kullanır.</span><span class="sxs-lookup"><span data-stu-id="98337-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="98337-111">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="98337-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="98337-112">**Sınırlamalar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="98337-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="98337-113">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="98337-113">Select **Add**.</span></span>
7. <span data-ttu-id="98337-114">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="98337-114">Select **Create**.</span></span>
8. <span data-ttu-id="98337-115">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="98337-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="98337-116">İfade girin</span><span class="sxs-lookup"><span data-stu-id="98337-116">Enter expression</span></span>

1. <span data-ttu-id="98337-117">**İfadeyi Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="98337-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="98337-118">Bu aşamada görev kaydında kullanıcı arabiriminin kilidini açarsanız, kısıtlama ifadesi oluşturmak için IntelliSense'i ve simgeler listesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98337-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="98337-119">**ConstraintBody** alanında, 'Implies[FrontGrill=="Metal", CornerProtection] ' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="98337-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="98337-120">Bu ifade mantığı şu anlamdadır: Ön ızgara metalse, köşe koruma seçeneği seçili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="98337-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="98337-121">**Doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="98337-121">Select **Validate**.</span></span>
    * <span data-ttu-id="98337-122">Doğrulama işlevi, kısıtlama ifadesini gözden geçirir ve sözdizimi hatalarını denetler.</span><span class="sxs-lookup"><span data-stu-id="98337-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="98337-123">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="98337-123">Select **Close**.</span></span>
5. <span data-ttu-id="98337-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="98337-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
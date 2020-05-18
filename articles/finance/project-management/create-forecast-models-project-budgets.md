---
title: Proje bütçeleri için tahmin modelleri oluşturma
description: Bu konu, kalan bütçeler için bir tahmin modelinin nasıl oluşturulacağını açıklamaktadır.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321791"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="4fc1c-103">Proje bütçeleri için tahmin modelleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="4fc1c-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fc1c-104">Bu konu, kalan bütçeler için bir tahmin modelinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="4fc1c-105">Bütçe denetimine tabi olan bir proje, iki tür bütçe kullanır: orijinal ve kalan.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="4fc1c-106">Bir proje bütçesi oluşturduğunuzda, **Tahmin modelleri** sayfasında oluşturulan orijinal ve kalan bütçe tahmin modellerini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="4fc1c-107">Belirtilen modellere dayalı proje bütçeleri, proje bütçesini kaydettiğinizde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="4fc1c-108">Bütçe denetimi için kullanılan bir tahmin modelinde alt model bulunamaz veya alt model olarak kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="4fc1c-109">**Proje yönetimi ve muhasebe** > **Kurulum** > **Tahminler**  > **Tahmin modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="4fc1c-110">Yeni bir tahmin modeli oluşturmak için **Yeni**'yi seçin ve yeni model için bir model kimlik numarası ve adı girin.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="4fc1c-111">Tahmin modeli için tahmin satırlarında herhangi bir değişiklik yapılmasını önlemek için **Durduruldu** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="4fc1c-112">Modelin ilişkili olduğu tahmin satırlarının genel muhasebede nakit akışı tahminleri oluşturması gerekiyorsa **Nakit akışı tahminlerine dahil et**'i **Evet** olarak işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="4fc1c-113">Proje tarihini fatura tarihi olarak kullanmak için, **Tahmini Fatura tarihi**'ni **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="4fc1c-114">**Bütçe türü** alanında, aşağıdaki model türlerinden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="4fc1c-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="4fc1c-115">**Orijinal bütçe**: İlk bütçe oluşturulduğunda ve onaylandığında kabul edilen orijinal bütçe tutarlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="4fc1c-116">**Kalan bütçe**: Projenin ömrü boyunca kalan bütçe tutarlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="4fc1c-117">Bu tahmin modelindeki bakiyeler gerçek hareketler tarafından azaltılır ve bütçe revizyonları tarafından artırılır veya azaltılır.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="4fc1c-118">**İleri taşı**: Projeyle ilgili İleri taşıma bütçe tutarlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="4fc1c-119">İleri taşıma, kullanılmayan bütçe tutarlarını bir mali yıldan diğerine aktarmak için çalıştırılabilecek, isteğe bağlı bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="4fc1c-120">Aşağıdaki seçenekleri gerektiği gibi ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4fc1c-120">Set the following options as required:</span></span>

   - <span data-ttu-id="4fc1c-121">Proje tarihini fatura tarihi olarak kullanmak için **Tahmini fatura tarihi**'ni etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="4fc1c-122">**Süren iş ile tahmin**'i süren işe dayalı tahmin için etkinleştirin ve sonra süren iş türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="4fc1c-123">Varsayılan **Bütçe türü**'nü **Hiçbiri** olarak ayarlayabilir veya yeni bir tür girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="4fc1c-124">Bütçe türü bir kaydı değiştirdikten sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="4fc1c-125">Varsayılan bütçe türünü değiştirirseniz, diğer tüm seçenekler güncelleştirmeler için kullanılamaz hale gelir ve bu tahmin modelini yeniden kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4fc1c-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 


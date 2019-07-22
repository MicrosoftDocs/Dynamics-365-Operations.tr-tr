---
title: ER model ve biçimlerinin veri bağlamalarında göreli yol kullanma
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6582cca9b912868f88de2770a17cbb6e67328660
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726564"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="56807-103">ER model ve biçimlerinin veri bağlamalarında göreli yol kullanma</span><span class="sxs-lookup"><span data-stu-id="56807-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="56807-104">Elektronik raporlama (ER) aracı, kullanıcıların elektronik biçim yapılarını tanımlamasına ve sonra da içerdiği veri ve Dynamics 365 for Finance and Operations'daki algoritmaları kullanarak bu yapıların nasıl doldurulması gerektiğini açıklayabilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="56807-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="56807-105">Daha fazla bilgi için bkz: [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="56807-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="56807-106">Finance and Operations verilerini almak ve bunu elektronik bir belge oluşturmak için kullanmak üzere veri akışını belirtmek için aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="56807-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="56807-107">Yapılandırılmış veri kaynaklarını tasarlanan etki alanına özgü veri modeli öğelerine bağlayın.</span><span class="sxs-lookup"><span data-stu-id="56807-107">Bind configured data sources to elements of the designed domain-specific data model.</span></span> <span data-ttu-id="56807-108">Model yapısı ve seçili veri kaynakları karmaşık hiyerarşik bir yapının parçası olabilir.</span><span class="sxs-lookup"><span data-stu-id="56807-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="56807-109">Bu nedenle, son bağlamalar çok büyük olabilir ve farklı türlerde birçok öğe (örneğin, ilişkiler, tablolar ve yöntemler) içerebilir.</span><span class="sxs-lookup"><span data-stu-id="56807-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="56807-110">Özellikle sahip olmayanlar için bağlamalar daha az okunabilir, incelenebilir ve anlaşılması çok karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="56807-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="56807-111">Veri modelinden oluşturulan biçim çıktısına hangi verilerin doldurulduğunu tanımlamak için bileşenleri biçimlendir ile veri modeli öğelerini bağlayın.</span><span class="sxs-lookup"><span data-stu-id="56807-111">Bind data model elements with format components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="56807-112">ER eşleme tasarımcılarının kullanılabilirliğini iyileştirmek için göreli yol özelliği serbest bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="56807-112">To improve usability of ER mapping designers, the relative path feature has been released.</span></span> <span data-ttu-id="56807-113">Varsayılan olarakER tasarım deneyiminin etkinleştirildiği Finance and Operations'ın her yeni örneği için göreli yol gösterimi seçeneği açıktır (Microsoft Dynamics 365 for Finance and operations, Microsoft Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="56807-113">By default, the relative path representation option is turned on for any new instance of Finance and Operations where ER design experience is enabled (Microsoft Dynamics 365 for Finance and operations, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="56807-114">Kullanıcıların bu ER bağlamalarıyla çalışırken tam yolu kullanmaya devam edebilmesi için göreli yol parametresi uyguladık.</span><span class="sxs-lookup"><span data-stu-id="56807-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="56807-115">[![Kullanıcı parametreleri](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="56807-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="56807-116">Göreli yol kullanım parametresi açıldığında, tek bir @ karakteri geçerli model öğesinin bağlamasında üst öğeye ilişkin yolu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="56807-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="56807-117">Tüm bağlama yolu daha kısalır bu da tüm eşlemeyi daha belirgin ve daha kolay anlaşılır yapar.</span><span class="sxs-lookup"><span data-stu-id="56807-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="56807-118">Çoğu durumda, ER tasarımcısında veri modeli tüm bağlamalarını görüntülemek için ek kaydırma gerekmez.</span><span class="sxs-lookup"><span data-stu-id="56807-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="56807-119">[![Model eşleme tasarımcısı](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="56807-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="56807-120">Yeni bir ER ifadesi tasarlamaya başladığınızda, üst öğenin bir alanına bağlamayı tanımlamak için yalnızca bir karakter girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="56807-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="56807-121">[![Formül tasarımcısı](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="56807-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="56807-122">Üst model öğesinin veri kaynağını mutlak yol kullanımı ile değiştirmeye karar verirken, bu model öğesinin yanı sıra iç içe geçmiş öğelerin de yeni bir veri kaynağına el ile yeniden bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="56807-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="56807-123">Göreli yol kullanımı açık olduğunda ve üst öğeye bağlanacak yeni bir veri kaynağı seçtiğinizde, bu üst öğenin tüm iç içe öğelerini tek bir tıklama ile otomatik olarak yeniden bağlamak için bir seçenek sunulur.</span><span class="sxs-lookup"><span data-stu-id="56807-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="56807-124">[![Geçerli şema iletisini değiştir](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="56807-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="56807-125">İç içe yerleştirilmiş öğelerin yeniden bağlamasının onaylarsanız yeni ana öğe, varolan üst öğeyi içeren her iç içe öğenin yoluna yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="56807-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="56807-126">Bu özellik, ER çerçevesinin geriye dönük uyumluluğunu koparmaz.</span><span class="sxs-lookup"><span data-stu-id="56807-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="56807-127">Daha önce tasarlamış olan tüm ER yapılandırmaları bu yeni özellik ile çalışacak; bunlara yükseltme veya dönüştürme gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="56807-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="56807-128">Model eşleştirmelerinde iç içe öğelerin bağlamalarının toplu değişikliği ile tanıtılan tüm değişiklikler bir yapılandırma farkı değişimlerinde doğru kaydedilir (değişiklikleri izleme).</span><span class="sxs-lookup"><span data-stu-id="56807-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="56807-129">Bu, müşterilerin, bu yeni özellik kullanılarak değiştirilmiş olan model eşleştirmelerinin tüm yeni temel sürümlerini yeniden temellendirmelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="56807-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>

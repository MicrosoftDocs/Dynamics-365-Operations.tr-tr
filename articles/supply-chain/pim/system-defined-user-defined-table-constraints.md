---
title: "Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları"
description: "Bu makalede, kullanıcı tanımlı ve sistem tanımlı olmak üzere, bir ürün yapılandırma modelindeki bileşenler için iki tablo sınırlandırma türü açıklanmaktadır. Tablo sınırlandırmaları, her bir satırın bir pozitif öznitelik değeri setine karşılık geldiği, izin verilen öznitelik kombinasyonlarının matrislerini temsil eder."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: b59452496f0ad47f1fe2ff034895a082a205dda9
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2017

---

# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="f5ada-104">Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları</span><span class="sxs-lookup"><span data-stu-id="f5ada-104">System-defined and user-defined table constraints</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f5ada-105">Bu makalede, kullanıcı tanımlı ve sistem tanımlı olmak üzere, bir ürün yapılandırma modelindeki bileşenler için iki tablo sınırlandırma türü açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f5ada-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="f5ada-106">Tablo sınırlandırmaları, her bir satırın bir pozitif öznitelik değeri setine karşılık geldiği, izin verilen öznitelik kombinasyonlarının matrislerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f5ada-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="f5ada-107">Tablo kısıtlamaları, ürün yapılandırma modelindeki bileşenler için izin verilen özniteliklerin birleşimlerinin matrislerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f5ada-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="f5ada-108">Tablodaki her satır bir dizi olası öznitelik değerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f5ada-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="f5ada-109">Ürün yapılandırma modelindeki kısıtlamaları iki türde bildirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f5ada-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="f5ada-110">**İfade kısıtlaması** – Ürün yapılandırması sırasında yalnızca uyumlu değerlerin seçilebileceğini güvence altına almak için öznitelikler arasındaki ilişkileri tanımlayan bir ifade oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f5ada-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="f5ada-111">**Tablo kısıtlaması** – Belirtilen öznitelikler kümesi için izin verilen tüm kombinasyonları tanımlayan bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f5ada-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="f5ada-112">İki türde tablo kısıtlaması vardır: Kullanıcı tanımlı tablo kısıtlamaları ve sistem tanımlı tablo kısıtlamaları.</span><span class="sxs-lookup"><span data-stu-id="f5ada-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="f5ada-113">Bu makalede, ürün yapılandırma modelinde bileşenler için kullanıcı tanımlı ve sistem tanımlı tablo kısıtlamaları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f5ada-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="f5ada-114">Kullanıcı tanımlı tablo kısıtlamaları</span><span class="sxs-lookup"><span data-stu-id="f5ada-114">User-defined table constraints</span></span>
<span data-ttu-id="f5ada-115">Kullanıcı tanımlı bir tablo kısıtlaması öznitelik türleri tarafından tanımlanan öznitelik değerlerinin bir dizi kombinasyonunu tanımlamak için kullanılan bir matris türüdür.</span><span class="sxs-lookup"><span data-stu-id="f5ada-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="f5ada-116">Örneğin, hoparlör üretiyorsanız kullanıcı tanımlı tablo kısıtlamasında kabin rengi ve ızgara rengi için sütunlar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5ada-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="f5ada-117">Kabin renginin öznitelik türünde dört; ızgara renginin öznitelik türünde üç değer vardır.</span><span class="sxs-lookup"><span data-stu-id="f5ada-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="f5ada-118">Bu nedenle, kısıtlamalar kullanılmazsa 4 × 3 = 12 olası kombinasyon oluşur.</span><span class="sxs-lookup"><span data-stu-id="f5ada-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="f5ada-119">Ancak, bu örnekte aşağıdaki tabloda gösterildiği şekilde yalnızca altı kombinasyona izin verilir.</span><span class="sxs-lookup"><span data-stu-id="f5ada-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="f5ada-120">Bu bilgiler **Tablo kısıtlamasını düzenle** sayfasında **İzin verilen kombinasyonlar** sekmesinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f5ada-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="f5ada-121">Kabin rengi</span><span class="sxs-lookup"><span data-stu-id="f5ada-121">Cabinet finish</span></span> | <span data-ttu-id="f5ada-122">Izgara rengi</span><span class="sxs-lookup"><span data-stu-id="f5ada-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="f5ada-123">Siyah</span><span class="sxs-lookup"><span data-stu-id="f5ada-123">Black</span></span>          | <span data-ttu-id="f5ada-124">Siyah</span><span class="sxs-lookup"><span data-stu-id="f5ada-124">Black</span></span>       |
| <span data-ttu-id="f5ada-125">Siyah</span><span class="sxs-lookup"><span data-stu-id="f5ada-125">Black</span></span>          | <span data-ttu-id="f5ada-126">Metal</span><span class="sxs-lookup"><span data-stu-id="f5ada-126">Metal</span></span>       |
| <span data-ttu-id="f5ada-127">Meşe</span><span class="sxs-lookup"><span data-stu-id="f5ada-127">Oak</span></span>            | <span data-ttu-id="f5ada-128">Siyah</span><span class="sxs-lookup"><span data-stu-id="f5ada-128">Black</span></span>       |
| <span data-ttu-id="f5ada-129">Pelesenk</span><span class="sxs-lookup"><span data-stu-id="f5ada-129">Rosewood</span></span>       | <span data-ttu-id="f5ada-130">Beyaz</span><span class="sxs-lookup"><span data-stu-id="f5ada-130">White</span></span>       |
| <span data-ttu-id="f5ada-131">Beyaz</span><span class="sxs-lookup"><span data-stu-id="f5ada-131">White</span></span>          | <span data-ttu-id="f5ada-132">Siyah</span><span class="sxs-lookup"><span data-stu-id="f5ada-132">Black</span></span>       |
| <span data-ttu-id="f5ada-133">Beyaz</span><span class="sxs-lookup"><span data-stu-id="f5ada-133">White</span></span>          | <span data-ttu-id="f5ada-134">Beyaz</span><span class="sxs-lookup"><span data-stu-id="f5ada-134">White</span></span>       |

<span data-ttu-id="f5ada-135">Kullanıcı tanımlı tablo kısıtlamaları ifade kısıtlamasıyla aynı şekilde işleyen statik tablo girişiyle tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f5ada-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="f5ada-136">Kullanıcı tanımlı bir tablo kısıtlaması kullandığınızda tabloları oluşturmanın, anlamanın ve sağlamanın genellikle uzun ifade kısıtlamalarından daha kolay olması bir avantaj sağlar.</span><span class="sxs-lookup"><span data-stu-id="f5ada-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="f5ada-137">Sistem tanımlı tablo kısıtlamaları</span><span class="sxs-lookup"><span data-stu-id="f5ada-137">System-defined table constraints</span></span>
<span data-ttu-id="f5ada-138">Sistem tanımlı bir tablo kısıtlaması, bir tablodaki öznitelik türü ile alan arasındaki dinamik eşlemeyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f5ada-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="f5ada-139">Sistem tanımlı bir tablo kısıtlaması bir ürün yapılandırma modeline dahil edildiğinde, öznitelik türü değerlerinin yerine tablodaki verileri güvence altına alan eşleme gösterilir.</span><span class="sxs-lookup"><span data-stu-id="f5ada-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="f5ada-140">Tablo içeriği değiştirilebileceğinden (örneğin, diğer modüller tarafından) sonuçta dinamik bir kısıtlama ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="f5ada-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="f5ada-141">Sistem tanımlı bir tablo kısıtlaması oluşturduğunuzda, bir tablo seçer, isteğe bağlı olarak kullanmak istediğiniz sorguyu tanımlar ve ardından seçilen tablodaki alanlarla öznitelik türlerini ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5ada-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="f5ada-142">Alanların türleri öznitelik türlerinin türleriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="f5ada-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="f5ada-143">Bir ürün yapılandırma modeline bir tablo kısıtlaması getirilebilmesi için, tablo kısıtlamasının model bileşenlerinden birindeki kısıtlamaya dahil edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f5ada-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="f5ada-144">Yeni kısıtlama oluşturmak için prosedür, tablo kısıtlaması türünün seçilmesi ve ardından kullanılacak tablo kısıtlaması tanımının seçilmesidir.</span><span class="sxs-lookup"><span data-stu-id="f5ada-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="f5ada-145">Son olarak, tablo kısıtlamasındaki tüm alanlar ürün yapılandırma modelindeki özniteliklerle eşlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="f5ada-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="see-also"></a><span data-ttu-id="f5ada-146">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="f5ada-146">See also</span></span>
--------

[<span data-ttu-id="f5ada-147">Ürün konfigürasyon modellerinde kilit konseptler</span><span class="sxs-lookup"><span data-stu-id="f5ada-147">Key concepts in product configuration models</span></span>](product-configuration-models.md)





---
title: "Ürün kategorisi yönetimi"
description: "Bu konu alım satım yöneticilerinin, Perakende ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasındaki ilişkileri yönetmek için Perakende ürün kategorilerini nasıl kullanacağını açıklar."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: tr-tr
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="03f13-103">Gelişmiş ürün ve kategori yönetimi</span><span class="sxs-lookup"><span data-stu-id="03f13-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="03f13-104">Bu konu,Dynamics 365 for Retail'de Perakende ürün kategorilerini ve ürünlerini yönetmenin gelişmiş bir yolunu açıklar.</span><span class="sxs-lookup"><span data-stu-id="03f13-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="03f13-105">Bu geliştirmeler alım satım yöneticilerinin Perakende ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasındaki ürün özelliklerinin genel yapısını görüntülemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="03f13-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="03f13-106">Perakende ürün kategorilerini yönetme hakkında daha fazla bilgi için **Kategori ve ürün yönetimi** çalışma alanından **Perakende ürün hiyerarşisi**'ne gidin ve **Perakende ürün kategorisi** sayfasının gelişmiş yapısını not edin.</span><span class="sxs-lookup"><span data-stu-id="03f13-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Kategori ve ürün yönetimi çalışma alanı](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="03f13-108">Önceki sürümlerde, ürün özellikleri uygulanabilirliklerinin kapsamına dayalı olarak **Temel ürün özellikleri** ve **Perakende ürün özelliklerine** ayrılmıştı.</span><span class="sxs-lookup"><span data-stu-id="03f13-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="03f13-109">**Perakende ürün özellikleri**'nin uygulanabilirlik kapsamı *genel*di; bu, belirli bir **Perakende ürün özelliği** için tüm tüzel kişilikler arasında aynı değerin paylaşıldığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="03f13-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="03f13-110">**Temel ürün özellikleri** *tüzel kişiliğe* özeldir.</span><span class="sxs-lookup"><span data-stu-id="03f13-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="03f13-111">Başka bir deyişle, belirli bir **Temel ürün özelliği** için değer, tekil iş gereksinimlerine dayanarak tüzel kişilikler arasında fark gösterebiliyordu.</span><span class="sxs-lookup"><span data-stu-id="03f13-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="03f13-112">Gelişmiş Perakende ürün kategorisi yapısında, ürün özellikleri, serbest bırakılan ürün ayrıntıları form yapısını yansıtmak amacıyla bir grup içerisindeki uygulanabilirlikleri temel alınarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="03f13-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Alanları uygulanabilirlik kapsamlarına göre gruplandırma](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="03f13-114">Tüm tüzel kişilikler arasında tüzel varlığa özel şirketleri yönetmek ve bunları özel bir tüzel kişilik için yönetmek arasında geçiş yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03f13-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="03f13-115">Bunu yapmak için, **Tüm tüzel kişilikleri görüntüle/düzenle** veya **Belirli bir tüzel kişiliği görüntüle/düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="03f13-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Tek ve tüm tüzel kişilikler arasında geçiş yapma](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Tek ve tüm tüzel kişilikler arasında geçiş yapma](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="03f13-118">Önceki sürümlerle karşılaştırıldığında, yeni Perakende ürün kategorisi yapısında bir alım satım yöneticisi tek kategori düzeyindeki ek bir ürün özellikleri kümesi için varsayılan değerler de tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="03f13-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="03f13-119">Ürün oluşturma sırasında, bu varsayılan ürün özellik değerleri, Perakende ürün hiyerarşisindeki ayrı bir kategori ile olan ilişkisi temel alınarak bir ürün tarafından devralınabilir.</span><span class="sxs-lookup"><span data-stu-id="03f13-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="03f13-120">Her bir ürün için devralınan bu ürün özellikleri, tekil işletme gereksinimlerini karşılamak üzere değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="03f13-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="03f13-121">Perakende ürün kategorisi formundan ürünleri güncelleştirmek için özellikleri seçin</span><span class="sxs-lookup"><span data-stu-id="03f13-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="03f13-122">Hangi güncelleştirilmiş ürün özelliklerinin ilişkili ürünlere gönderileceğini seçmek amacıyla ürün özellikleri için geliştirilmiş bu yeni yapıyı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03f13-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Güncelleştirilmiş ürünlerin yeni gelişmiş görünümü](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="03f13-124">Satış yöneticileri, her bir ürün için devralınan bu ürün özelliklerini, tekil işletme gereksinimlerini karşılamak üzere değiştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="03f13-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>



---
title: Perakende ürün kategorilerini ve ürünleri yönetme
description: Bu konu alım satım yöneticilerinin, Perakende ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasındaki ilişkileri yönetmek için Perakende ürün kategorilerini nasıl kullanacağını açıklar.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 27870fe6172479b891b885d9e84ca10b250e3399
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019525"
---
# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="d5036-103">Perakende ürün kategorilerini ve ürünlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="d5036-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="d5036-104">Bu konu, Dynamics 365 Retail'de ürün kategorilerini ve ürünlerini yönetmenin gelişmiş bir yolunu açıklar.</span><span class="sxs-lookup"><span data-stu-id="d5036-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Retail.</span></span> <span data-ttu-id="d5036-105">Geliştirmeler alım satım yöneticilerinin ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasında paylaşılan ürün özelliklerinin yapısını görüntülemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d5036-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="d5036-106">Ürün kategorilerinin nasıl yönetileceği hakkında daha fazla bilgi için **Kategori ve ürün Yönetimi** çalışma alanında **Perakende ürün hiyerarşisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d5036-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="d5036-107">Görüntülenen **Perakende ürün hiyerarşisi** sayfasının gelişmiş yapısını not edin.</span><span class="sxs-lookup"><span data-stu-id="d5036-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="d5036-108">Retail'in önceki sürümlerde, ürün özellikleri uygulanabilirliklerinin kapsamına dayalı olarak *temel ürün özellikleri* ve *Perakende ürün özelliklerine* ayrılmıştı.</span><span class="sxs-lookup"><span data-stu-id="d5036-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="d5036-109">Perakende ürün özellikleri kendi uygulanabilirlik kapsamı içinde *genel*'dir.</span><span class="sxs-lookup"><span data-stu-id="d5036-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="d5036-110">Başka bir deyişle, belirli bir ürün özelliği için, aynı değer farklı tüzel kişilikler arasında paylaşılıyor.</span><span class="sxs-lookup"><span data-stu-id="d5036-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="d5036-111">Aksine, temel ürün özellikleri *tüzel kişiliğe özeldir*.</span><span class="sxs-lookup"><span data-stu-id="d5036-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="d5036-112">Başka bir deyişle, belirli bir temel ürün özelliği için değer, tekil iş gereksinimlerine bağlı olarak tüzel kişilikler arasında fark gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="d5036-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="d5036-113">Gelişmiş ürün kategorisi yapısında, ürün özellikleri, serbest bırakılan ürün ayrıntıları form yapısını yansıtmak amacıyla bir grup içerisindeki uygulanabilirlikleri temel alınarak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="d5036-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Özelliklerin uygulanabilirlik kapsamlarına göre gruplandırılan alanlar](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="d5036-115">Tüm tüzel kişilikler arasında tüzel varlığa özel şirketleri yönetmek ve bunları özel bir tüzel kişilik için yönetmek arasında geçiş yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5036-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="d5036-116">Tüzel kişiliklerdeki özellikleri yönetmek için **Tüm tüzel kişilikleri görüntüle** (veya **Tüm tüzel kişilikleri düzenle**) öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d5036-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Tüm tüzel kişilikleri görüntüle/düzenle](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="d5036-118">Belirli bir tüzel kişilik özelliklerini yönetmek için **Belirli bir tüzel kişiliği görüntüle** (veya **Belirli bir tüzel kişiliği düzenle**) öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d5036-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Belirli bir tüzel kişiliği görüntüle/düzenle](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="d5036-120">Buna ek olarak, geliştirilmiş Perakende ürün kategorisi yapısında bir alım satım yöneticisi tek kategori düzeyindeki ek bir ürün özellikleri kümesi için varsayılan değerler de tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="d5036-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="d5036-121">Böylece, ürünler oluşturulduğunda, ürün özellikleri için ürün hiyerarşisindeki tek bir kategori ile bu özelliklerin ilişkisi temel alınarak varsayılan değerleri devralırlar.</span><span class="sxs-lookup"><span data-stu-id="d5036-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="d5036-122">Her bir ürün için devralınan bu ürün özellikleri, tekil işletme gereksinimlerini karşılamak üzere değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="d5036-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="d5036-123">Perakende ürün hiyerarşisi sayfasında ürünleri güncelleştirmek için özellikleri seçme</span><span class="sxs-lookup"><span data-stu-id="d5036-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="d5036-124">Hangi güncelleştirilmiş ürün özelliklerinin ilişkili ürünlere gönderileceğini seçmek amacıyla ürün özellikleri için geliştirilmiş yeni yapıyı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5036-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="d5036-125">Eylem Bölmesindeki **Perakende ürün hiyerarşisi** sayfasında **Kategori**'yi seçin ve ardından **Ürünleri güncelleştir**'i seçerek **Ürünleri güncelleştir** iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="d5036-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Ürünleri güncelleştir iletişim kutusu](media/NewUpdateProductsEnhancedView.PNG)

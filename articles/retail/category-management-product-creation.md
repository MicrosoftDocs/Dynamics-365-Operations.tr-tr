---
title: "Ürün kategorisi yönetimi ve oluşturulması"
description: "Bu konu, Perakende ürün kategorileri için yönetim deneyimine yapılan geliştirmeleri açıklar. Bu geliştirmeler alım satım yöneticilerinin Perakende ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasında bir ilişkiye sahip olmalarını imkan verir."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.search.scope: Core, Retail
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: e269f6c3815cea55b69b7eb6a9a65bf7c9e15378
ms.contentlocale: tr-tr
ms.lasthandoff: 01/18/2018

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="35079-104">Ürün kategorisi yönetimi ve oluşturulması</span><span class="sxs-lookup"><span data-stu-id="35079-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="35079-105">Perakende ürün kategorileri için yönetim deneyiminde yapılmış geliştirmeler alım satım yöneticilerinin Perakende ürün hiyerarşileri ve serbest bırakılan ürün ayrıntıları arasında bir ilişkiye sahip olmalarına olanak verir.</span><span class="sxs-lookup"><span data-stu-id="35079-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="35079-106">Bu geliştirmeleri görüntülemek için **Kategori ve ürün yönetimi**  çalışma alanında **Perakende ürün kategorisi yeni yapısı** sayfasını açmak için **Perakende ürün hiyerarşisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="35079-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="35079-107">Önceki sürümlerde, ürün özellikleri temel ürün özellikleri ve Perakende ürün özelliklerine ayrılmıştı; uygulanabilirliklerinin kapsamına dayanarak.</span><span class="sxs-lookup"><span data-stu-id="35079-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="35079-108">Perakende ürün *genel* özelliklerdi.</span><span class="sxs-lookup"><span data-stu-id="35079-108">Retail product properties were *global*.</span></span> <span data-ttu-id="35079-109">Başka bir deyişle, belirli bir ürün özelliği için, aynı değer farklı tüzel kişilikler arasında paylaşılıyor.</span><span class="sxs-lookup"><span data-stu-id="35079-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="35079-110">Temel ürün özellikleri *tüzel kişiliğe özel* idi.</span><span class="sxs-lookup"><span data-stu-id="35079-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="35079-111">Başka bir deyişle, bir ürün özelliği, tekil iş gereksinimlerine dayanarak tüzel kişilikler arasında fark gösterebiliyordu.</span><span class="sxs-lookup"><span data-stu-id="35079-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="35079-112">Bu geliştirmelerle, Perakende ürün kategorisi içindeki bir ürün özelliği için alanları ayırmaya devam ediyoruz, bir grup içerisindeki uygulanabilirliklerine dayanarak; serbest bırakılan ürün ayrıntıları form yapısını yansıtmak için.</span><span class="sxs-lookup"><span data-stu-id="35079-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="35079-113">Tüm tüzel kişilikler arasında tüzel varlığa özel şirketleri yönetmek ve bunları özel bir tüzel kişilik için yönetmek arasında geçiş yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="35079-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="35079-114">**Tüm tüzel kişilikleri görüntüle/düzenle** veya **Belirli bir tüzel kişiliği görüntüle/düzenle**'yi ihtiyaç duyduğunuz şekilde seçin.</span><span class="sxs-lookup"><span data-stu-id="35079-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="35079-115">Satış yöneticileri ayrıca tekil kategori düzeyinde ürün özellikleri için ek varsayılan değerler de tanımlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="35079-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="35079-116">Bu özellik değerleri ürün başına, ürün oluşturulması sırasında bir kategori ile ilişkilendirmelerine dayanarak devralınır.</span><span class="sxs-lookup"><span data-stu-id="35079-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="35079-117">Perakende ürün kategorisi formundan ürünleri güncelleştirmek için özellikleri seçin</span><span class="sxs-lookup"><span data-stu-id="35079-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="35079-118">Hangi güncelleştirilen ürün özelliklerinin ilişkilendirilmiş ürünlere gönderileceğini seçmek için mantıksal gruplama özelliklerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="35079-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="35079-119">Satış yöneticileri, her bir ürün için devralınan bu ürün özelliklerini, tekil işletme gereksinimlerini karşılamak üzere değiştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="35079-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


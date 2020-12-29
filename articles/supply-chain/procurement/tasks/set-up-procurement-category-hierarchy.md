---
title: Tedarik kategorisi hiyerarşisini ayarlama
description: Bu yordam, tedarik kategori hiyerarşisi içinde yeni düğümler oluşturmayı ve satın alma işleminde kullanılacak bir tedarik kategorisi yapılandırmayı gösterir.
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e45c80718c73ad785643c2a5fc0e712b291104d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439592"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="ad7ee-103">Tedarik kategorisi hiyerarşisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="ad7ee-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad7ee-104">Bu yordam, tedarik kategori hiyerarşisi içinde yeni düğümler oluşturmayı ve satın alma işleminde kullanılacak bir tedarik kategorisi yapılandırmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="ad7ee-105">Bu görevler genellikle Satınalma yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="ad7ee-106">Bu yordama başlamadan önce tedarik türünde bir kategori hiyerarşisi mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="ad7ee-107">Eğer bir demo verisi şirketi kullanıyorsanız, bu prosedürü USMF şirketinde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="ad7ee-108">Yeni bir tedarik kategorisi ekleyin</span><span class="sxs-lookup"><span data-stu-id="ad7ee-108">Add a new procurement category</span></span>
1. <span data-ttu-id="ad7ee-109">**Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Konsinye > Tedarik kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="ad7ee-110">Eylem Bölmesi'nde **Kategori hiyerarşisini düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="ad7ee-111">Geçerli tedarik kategori hiyerarşisi sayfanın sol tarafında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="ad7ee-112">Hiyerarşide değişiklik yapmak üzeresiniz.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="ad7ee-113">Eylem Bölmesi'nde **Yeni kategori düğümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="ad7ee-114">Sistem varsayılan olarak üst düğümü seçer.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-114">The system selects the top node by default.</span></span> <span data-ttu-id="ad7ee-115">Bu yordamı bir görev kılavuzu olarak çalıştırıyorsanız, Kilidi Aç düğmesine tıklayıp, yeni düğümü içine eklemek için başka bir üst düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="ad7ee-116">Bunu yaptıktan sonra, görev kılavuzunu kilitleyin ve sonrasında Yeni kategori düğümü'nü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="ad7ee-117">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ad7ee-118">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="ad7ee-119">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="ad7ee-120">Kolay ad isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-120">The friendly name is optional.</span></span> <span data-ttu-id="ad7ee-121">Bu kategori aramalarında, kategori adı ile birlikte görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="ad7ee-122">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="ad7ee-123">Yeni tedarik kategorinize ürünler ekleyin</span><span class="sxs-lookup"><span data-stu-id="ad7ee-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="ad7ee-124">**Tedarik ve kaynak atama > Konsinye > Tedarik kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="ad7ee-125">Yeni eklediğiniz düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-125">Select the node you just added.</span></span> <span data-ttu-id="ad7ee-126">Bu yordamı bir görev kılavuz olarak çalıştırıyorsanız, düğümü seçmek için görev kılavuzunun kilidini açmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="ad7ee-127">**Ürünler** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="ad7ee-128">Tedarik kategorisiyle ürünleri ilişkilendirmek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="ad7ee-129">Tedarik kategorisine eklemek istediğiniz ürünleri seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="ad7ee-130">Ürünleri **Seçili** tabloya eklemek için oku seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="ad7ee-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad7ee-131">Select **OK**.</span></span>

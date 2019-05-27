---
title: Tedarik kategorisi hiyerarşisini ayarlama
description: Bu yordam, tedarik kategori hiyerarşisi içinde yeni düğümler oluşturmayı ve satın alma işleminde kullanılacak bir tedarik kategorisi yapılandırmayı gösterir.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569903"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="78474-103">Tedarik kategorisi hiyerarşisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="78474-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78474-104">Bu yordam, tedarik kategori hiyerarşisi içinde yeni düğümler oluşturmayı ve satın alma işleminde kullanılacak bir tedarik kategorisi yapılandırmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="78474-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="78474-105">Bu görevler genellikle Satınalma yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="78474-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="78474-106">Bu yordama başlamadan önce tedarik türünde bir kategori hiyerarşisi mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="78474-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="78474-107">Eğer bir demo verisi şirketi kullanıyorsanız, bu prosedürü USMF şirketinde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="78474-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="78474-108">Yeni bir tedarik kategorisi ekleyin</span><span class="sxs-lookup"><span data-stu-id="78474-108">Add a new procurement category</span></span>
1. <span data-ttu-id="78474-109">Tedarik ve kaynak > Tedarik kategorileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="78474-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="78474-110">Kategori hiyerarşisi düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78474-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="78474-111">Geçerli tedarik kategori hiyerarşisi sayfanın sol tarafında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="78474-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="78474-112">Hiyerarşide değişiklik yapmak üzeresiniz.</span><span class="sxs-lookup"><span data-stu-id="78474-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="78474-113">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78474-113">Click New category node.</span></span>
    * <span data-ttu-id="78474-114">Sistem varsayılan olarak üst düğümü seçer.</span><span class="sxs-lookup"><span data-stu-id="78474-114">The system selects the top node by default.</span></span> <span data-ttu-id="78474-115">Bu yordamı bir görev kılavuzu olarak çalıştırıyorsanız, Kilidi Aç düğmesine tıklayıp, yeni düğümü içine eklemek için başka bir üst düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="78474-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="78474-116">Bunu yaptıktan sonra, görev kılavuzunu kilitleyin ve sonrasında Yeni kategori düğümü'nü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="78474-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="78474-117">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="78474-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="78474-118">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="78474-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="78474-119">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="78474-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="78474-120">Kolay ad isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="78474-120">The friendly name is optional.</span></span> <span data-ttu-id="78474-121">Bu kategori aramalarında, kategori adı ile birlikte görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="78474-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="78474-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78474-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="78474-123">Yeni tedarik kategorinize ürünler ekleyin</span><span class="sxs-lookup"><span data-stu-id="78474-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="78474-124">Tedarik ve kaynak > Tedarik kategorileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="78474-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="78474-125">Yeni eklediğiniz düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="78474-125">Select the node you just added.</span></span> <span data-ttu-id="78474-126">Bu yordamı bir görev kılavuz olarak çalıştırıyorsanız, düğümü seçmek için görev kılavuzunun kilidini açmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="78474-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="78474-127">Ürünler bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="78474-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="78474-128">Tedarik kategorisiyle ürün ilişkilendirmek için Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="78474-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="78474-129">Tedarik kategorisine eklemek istediğiniz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="78474-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="78474-130">Ürünü seçmek için oku tıklatın.</span><span class="sxs-lookup"><span data-stu-id="78474-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="78474-131">Tedarik kategorisine eklemek istediğiniz başka bir ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="78474-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="78474-132">Ürünü seçmek için oku tıklatın.</span><span class="sxs-lookup"><span data-stu-id="78474-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="78474-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78474-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="78474-134">Tercih edilen ve onaylanan satıcılar ekleyin</span><span class="sxs-lookup"><span data-stu-id="78474-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="78474-135">Satıcılar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="78474-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="78474-136">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="78474-136">Click Add.</span></span>
    * <span data-ttu-id="78474-137">Bir satıcıyı bir tedarik kategorisine ekleyebilir ve satıcının kategori için tercih edilen mi yoksa sadece onaylanan mı olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="78474-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="78474-138">Bir kategoriden bir satıcıyı sildiğinizde, satıcıyla ait bu kategorideki geçmiş hareketler silinmez.</span><span class="sxs-lookup"><span data-stu-id="78474-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="78474-139">Tedarik kategorisine eklemek istediğiniz satıcıyı bulun.</span><span class="sxs-lookup"><span data-stu-id="78474-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="78474-140">Satıcıyı seçmek için oku tıklatın.</span><span class="sxs-lookup"><span data-stu-id="78474-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="78474-141">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="78474-141">Click OK.</span></span>
6. <span data-ttu-id="78474-142">Değiştirmek istediğiniz satıcı satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="78474-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="78474-143">Satıcı durumu alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="78474-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="78474-144">Kategori ilke kuralındaki tedarikçi seçimi ayarı, tercih edilen mi, onaylanmış olan mı, yoksa tüm satıcıların mı satınalma talepleri üzerinde kullanılabilir olduğunu yönetir.</span><span class="sxs-lookup"><span data-stu-id="78474-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="78474-145">Kategoriye ilave bilgiler ekleyin</span><span class="sxs-lookup"><span data-stu-id="78474-145">Add additional information to the category</span></span>
1. <span data-ttu-id="78474-146">Tedarikçi değerlendirme ölçüt grupları bölümünün genişlemesini değiştir.</span><span class="sxs-lookup"><span data-stu-id="78474-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="78474-147">Bu sekme, tedarik kategorisindeki satıcıların hangi ölçütlere göre değerlendirileceğini tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="78474-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="78474-148">Bunu yapmak için Ekle'yi tıklayıp sonra istediğiniz ölçütü içeren bir tedarikçi Değerlendirme grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="78474-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="78474-149">Soru formları bölümünün genişlemesini değiştir.</span><span class="sxs-lookup"><span data-stu-id="78474-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="78474-150">Bu sekme, faaliyet türünü "Talep" olarak seçtiğiniz sürece, taleplerde yer alacak bir soru formu eklemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="78474-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="78474-151">Buna göre, talepte bulunan kişinin, belirli bir ürün veya tedarik kategorisindeki ürünler için talep göndermeden önce bir soru formu doldurması gerekir.</span><span class="sxs-lookup"><span data-stu-id="78474-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="78474-152">Madde satış vergisi grupları bölümünün genişlemesini değiştir.</span><span class="sxs-lookup"><span data-stu-id="78474-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="78474-153">Madde Satış vergisi grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="78474-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="78474-154">Satış vergisi grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="78474-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="78474-155">Kategori sayfası bölümünün genişlemesini değiştir.</span><span class="sxs-lookup"><span data-stu-id="78474-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="78474-156">Kategori sayfaları kategori hiyerarşisi sayfasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="78474-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="78474-157">Bunlar tedarik kategorisi hakkında, örneğin bir kategorideki ürünlerin türü, kategorideki ürünlerin fotoğrafları, kategoride bulunan indirimler gibi duyuruların bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="78474-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="78474-158">Kategori sayfasındaki bilgiler, satınalma talepleri üzerinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="78474-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="78474-159">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="78474-159">Close the page.</span></span>


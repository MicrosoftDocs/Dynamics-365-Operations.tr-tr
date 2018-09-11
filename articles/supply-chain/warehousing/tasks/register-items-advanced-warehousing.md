--- 
title: "Gelişmiş ambar işlemleri etkinleştirilmiş madde için madde varış günlüğü kullanarak maddeleri kaydetme"
description: "Bu yordam, gelişmiş ambar yönetimi işlemlerini kullanırken ürünlerin ürün varış günlüğü kullanılarak nasıl kaydedileceğini gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 751e73be385606bc706b2e14ea83c1b56c96402c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="40277-103">Gelişmiş ambar işlemleri etkinleştirilmiş madde için madde varış günlüğü kullanarak maddeleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="40277-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40277-104">Bu yordam, gelişmiş ambar yönetimi işlemlerini kullanırken ürünlerin ürün varış günlüğü kullanılarak nasıl kaydedileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="40277-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="40277-105">Bu genellikle bir teslim alma memuru tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="40277-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="40277-106">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="40277-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="40277-107">Bu kılavuzu başlatmadan önce, elinizde açık bir satınalma sipariş satırı içeren onaylı bir satınalma siparişi bulunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="40277-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="40277-108">Satırdaki madde stokta olmalı, ürün çeşitleri kullanmamalı ve izleme boyutları olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="40277-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="40277-109">Ayrıca, ürünün ambar yönetimi işlemi etkin bir depolama boyut grubuyla ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="40277-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="40277-110">Kullanılan ambar, ambar yönetimi işlemleri için etkinleştirilmelidir ve alım işlemi için kullanılan yerleşimin plakası kontrol edilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="40277-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="40277-111">USMF kullanıyorsanız, SAS oluşturmak için şirket hesabı 1001, ambar 51 ve ürün M9200 değerlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="40277-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="40277-112">Oluşturduğunuz satınalma siparişinin numarasınının yanı sıra, satınalma siparişi satırı için kullandığınız ürün numarası ve tesisi de not edin .</span><span class="sxs-lookup"><span data-stu-id="40277-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="40277-113">Bir ürün varış günlüğü başlığı oluşturma</span><span class="sxs-lookup"><span data-stu-id="40277-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="40277-114">Ürün varışı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="40277-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="40277-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-115">Click New.</span></span>
3. <span data-ttu-id="40277-116">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="40277-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="40277-117">USMF kullanıyorsanız, WHS yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="40277-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="40277-118">Başka veriler kullanıyorsanız, adını seçtiğiniz günlükte iki özelliğin olması gerekir: Malzeme çekme yerleşimini denetle ayarı Hayır, Karantina yönetimi ayarı Hayır olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="40277-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="40277-119">Numara alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="40277-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="40277-120">Tesis alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="40277-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="40277-121">Satınalma siparişi satırı için kullanılacak tesisi seçin.</span><span class="sxs-lookup"><span data-stu-id="40277-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="40277-122">Bu, günlükteki tüm satırlar için varsayılan olan bir varsayılan değer işlevi görür.</span><span class="sxs-lookup"><span data-stu-id="40277-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="40277-123">USMF'de ambar 51'i kullandıysanız, tesis 5'i seçin.</span><span class="sxs-lookup"><span data-stu-id="40277-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="40277-124">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="40277-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="40277-125">Seçmiş olduğunuz tesis için geçerli bir ambar seçin.</span><span class="sxs-lookup"><span data-stu-id="40277-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="40277-126">Bu, günlükteki tüm satırlar için varsayılan olan bir varsayılan değer işlevi görür.</span><span class="sxs-lookup"><span data-stu-id="40277-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="40277-127">USMF'te örnek değerler kullanıyorsanız, 51'i seçin.</span><span class="sxs-lookup"><span data-stu-id="40277-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="40277-128">Yerleşim alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="40277-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="40277-129">Seçmiş olduğunuz ambar için geçerli bir yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="40277-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="40277-130">Yerleşim, plakanın kontrol edildiği bir yerleşim profiliyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="40277-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="40277-131">Bu, günlükteki tüm satırlar için varsayılan olan bir varsayılan değer işlevi görür.</span><span class="sxs-lookup"><span data-stu-id="40277-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="40277-132">USMF'te örnek değerler kullanıyorsanız, Bulk-008'i seçin.</span><span class="sxs-lookup"><span data-stu-id="40277-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="40277-133">Plaka alanında aşağı açılan oku sağ tıklatın ve sonra Ayrıntıları göster'i seçin.</span><span class="sxs-lookup"><span data-stu-id="40277-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="40277-134">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-134">Click New.</span></span>
10. <span data-ttu-id="40277-135">Plaka alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="40277-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="40277-136">Değerini not edin.</span><span class="sxs-lookup"><span data-stu-id="40277-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="40277-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-137">Click Save.</span></span>
12. <span data-ttu-id="40277-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="40277-138">Close the page.</span></span>
13. <span data-ttu-id="40277-139">Plaka alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="40277-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="40277-140">Yeni oluşturduğunuz plakanın değerini girin.</span><span class="sxs-lookup"><span data-stu-id="40277-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="40277-141">Bu, günlükteki tüm satırlar için varsayılan olan bir varsayılan değer işlevi görür.</span><span class="sxs-lookup"><span data-stu-id="40277-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="40277-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="40277-143">Bir satır ekleyin</span><span class="sxs-lookup"><span data-stu-id="40277-143">Add a line</span></span>
1. <span data-ttu-id="40277-144">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-144">Click Add line.</span></span>
2. <span data-ttu-id="40277-145">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="40277-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="40277-146">Satınalma siparişi satırında kullandığınız ürün numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="40277-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="40277-147">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="40277-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="40277-148">Kaydetmek istediğiniz miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="40277-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="40277-149">Tarih alanı, bu ürünün eldeki miktarın stokta kaydedileceği tarihi belirler.</span><span class="sxs-lookup"><span data-stu-id="40277-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="40277-150">Lot kodu sağlanan bilgilerden hareketle benzersiz şekilde tanımlanabiliyorsa, sistem tarafından doldurulur.</span><span class="sxs-lookup"><span data-stu-id="40277-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="40277-151">Aksi halde, bunu el ile eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="40277-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="40277-152">Bu, bu kaydı belirli bir kaynak belge satırına bağlayan zorunlu bir alandır.</span><span class="sxs-lookup"><span data-stu-id="40277-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="40277-153">Kaydı tamamlama</span><span class="sxs-lookup"><span data-stu-id="40277-153">Complete the registration</span></span>
1. <span data-ttu-id="40277-154">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-154">Click Validate.</span></span>
    * <span data-ttu-id="40277-155">Bu günlüğün deftere nakile hazır olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="40277-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="40277-156">Doğrulama başarısız olursa, günlüğü deftere nakledebilmek için hataları düzeltmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="40277-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="40277-157">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-157">Click OK.</span></span>
    * <span data-ttu-id="40277-158">Tamam düğmesini tıklattıktan sonra iletiyi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="40277-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="40277-159">Günlükte sorun olmadığını belirten bir ileti görünmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="40277-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="40277-160">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-160">Click Post.</span></span>
4. <span data-ttu-id="40277-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="40277-161">Click OK.</span></span>
    * <span data-ttu-id="40277-162">Tamam düğmesine tıkladıktan sonra ileti çubuğunu kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="40277-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="40277-163">İşlemin tamamlandığını belirten bir ileti görünmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="40277-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="40277-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="40277-164">Close the page.</span></span>



---
title: "Yönetim ön koşullarını ayarlama"
description: "Uygunsuzluk yönetimi işlemlerini etkinleştirmek için bu yordamı kullanın."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a33a5c9feec99737804949f29befa03bf56eea24
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-prerequisites-for-management"></a><span data-ttu-id="6f3d5-103">Yönetim ön koşullarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6f3d5-103">Set up prerequisites for management</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f3d5-104">Uygunsuzluk yönetimi işlemlerini etkinleştirmek için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="6f3d5-105">Uyumsuzluk, açıklayıcı bilgilerin sorunun kaynağını ve tipini içerdiği bir kalite sorunu olan bir yordamı veya maddeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="6f3d5-106">Bu yordam, USMF demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="6f3d5-107">Bu yordam genellikle kalite yöneticisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="6f3d5-108">Şirket içindeki kalite yönetimi işlemlerini etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="6f3d5-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="6f3d5-109">Stokyönetimi > Kurulum > Stok ve ambar yönetim parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="6f3d5-110">Kalite yönetimi sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="6f3d5-111">Kalite yönetimi kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="6f3d5-112">Şirket için kalite yönetimi işlemlerini etkinleştirmek için bu parametreyi seçin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="6f3d5-113">Saatlik ücret alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="6f3d5-114">Yerel para biriminde saatlik ücret girmek için Saatlik ücret alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="6f3d5-115">Saatlik ücret, uygunsuzlukla ilgili operasyonlar için maliyetleri hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="6f3d5-116">Saatlik ücret ve hesaplanan maliyetler bir uyumsuzluk için referans bilgileri sağlar ve diğer işlevlerle etkileşime girmez.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="6f3d5-117">Rapor kurulumu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-117">Click Report setup.</span></span>
    * <span data-ttu-id="6f3d5-118">Bu sayfa, farklı türde kalite yönetimi raporlarında kullanılacak kalite raporu not türlerini tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-118">This page allows you to define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="6f3d5-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-119">Close the page.</span></span>
7. <span data-ttu-id="6f3d5-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="6f3d5-121">Kullanıcıyı uygunsuzluk işleme için etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="6f3d5-122">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="6f3d5-123">Bir uygunsuzluk onayını işlemek için uygunsuzlukları onaylayan veya reddeden kullanıcının atanmış kullanıcılar sayfasında bir "Ad" değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="6f3d5-124">Kullanıcının belge notları kullanabilmesi için belge işleme seçeneğinin kullanıcı ayarlarında etkinleştirilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="6f3d5-125">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6f3d5-126">Örneğin, 'Ricardo' değerini girerek filtreleme yapın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="6f3d5-127">Onaylama veya reddetme işlemlerini yapacak kullanıcıyı bulmak için uygunsuzluk kayıtlarında filtre kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="6f3d5-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6f3d5-129">Bir uygunsuzluk onayını işlemek için uygunsuzlukları onaylayan veya reddeden kullanıcının, Kullanıcılar sayfasında atanmış bir "Ad" değeri olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="6f3d5-130">Kullanıcı seçenekleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-130">Click User options.</span></span>
5. <span data-ttu-id="6f3d5-131">Tercihler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="6f3d5-132">Belge işlemeyi etkinleştir alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="6f3d5-133">Kullanıcının belge notları kullanabilmesi için belge işleme seçeneğinin kullanıcı ayarlarında etkinleştirilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="6f3d5-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-134">Close the page.</span></span>
8. <span data-ttu-id="6f3d5-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-135">Close the page.</span></span>
9. <span data-ttu-id="6f3d5-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="6f3d5-137">Uygunsuzluk işleme için tanı türlerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="6f3d5-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="6f3d5-138">Stok yönetimi > Kurulum > Kalite yönetimi > Tanı türleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="6f3d5-139">Tanılama işlemleri için bir sınıflandırma tanımlamak için Tanılama türleri sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="6f3d5-140">Bir düzeltme, onaylanan bir uyumsuzluk için yapılması gereken tanı eyleminin tipini, bunu gerçekleştirecek kişiyi ve istenen ve planlanan tamamlama tarihini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="6f3d5-141">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-141">Click New.</span></span>
3. <span data-ttu-id="6f3d5-142">Tanı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="6f3d5-143">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6f3d5-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="6f3d5-145">Uygunsuzluk işleme için kalite giderlerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="6f3d5-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="6f3d5-146">Stok yönetimi > Kurulum > Kalite yönetimi > Kalite giderleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="6f3d5-147">Kalite giderleri sayfasını, uygunsuzluklar ile ilgili işlemlerinde kullanılacak giderlerin sınıflandırılmasını tanımlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="6f3d5-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-148">Click New.</span></span>
3. <span data-ttu-id="6f3d5-149">Masraf kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="6f3d5-150">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6f3d5-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="6f3d5-152">Uygunsuzluk işleme için operasyonları tanımlayın</span><span class="sxs-lookup"><span data-stu-id="6f3d5-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="6f3d5-153">Stok yönetimi > Kurulum > Kalite yönetimi > Operasyonlar öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="6f3d5-154">Onaylanan bir uygunsuzluk için gerçekleştirilebilecek işin sınıflandırmasını tanımlamak için Operasyonlar sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="6f3d5-155">Uyumsuzluğa ilgili bir operasyonu ilişkilendirdiğinizde, operasyonu gerçekleştirmek için gereken ilgili malzemeler, emek saatleri ve tahmini maliyetlerle ilgili ayrıntılı bilgiler tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="6f3d5-156">Bu bilgiler, operasyonu gerçekleştirmek için gereken tahmini maliyetin hesaplanmasında bir temel sağlar.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="6f3d5-157">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-157">Click New.</span></span>
3. <span data-ttu-id="6f3d5-158">Operasyon alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="6f3d5-159">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6f3d5-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="6f3d5-161">Uygunsuzluk işleme için problem türlerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="6f3d5-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="6f3d5-162">Stok yönetimi > Kurulum > Kalite yönetimi > Problem türleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="6f3d5-163">Çeşitli uygunsuzluk türlerinde karşılaşılan kalite sorunlarıyla ilgili bir sınıflandırma tanımlamak için Sorun türleri sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="6f3d5-164">Uygunsuzluk türlerine; Dahili, Müşteri, Satıcı, Hizmet talebi, Üretim ve Eş ürün üretimi gibi türler dahildir.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="6f3d5-165">Tek bir sorun türü birden çok uygunsuzluk türüyle ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="6f3d5-166">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-166">Click New.</span></span>
3. <span data-ttu-id="6f3d5-167">Problem türü alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="6f3d5-168">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6f3d5-169">Uyumsuzluk tipleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="6f3d5-170">Bir sorun türünün bir veya birden fazla uygunsuzluk türünde kullanmak üzere yetkilendirmek için Uygunsuzluk türleri sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="6f3d5-171">Örneğin, bir kusur koduyla ilgili bir sorun tipi tüm uyumsuzluk tipleri için geçerli olurken, müşteri şikayetleri hakkındaki bir sorun tipi yalnızca müşteri ve servis isteği uyumsuzluk tipleri için geçerli olabilir.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="6f3d5-172">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-172">Click New.</span></span>
7. <span data-ttu-id="6f3d5-173">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="6f3d5-174">Uygunsuzluk türü alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="6f3d5-175">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-175">Close the page.</span></span>
10. <span data-ttu-id="6f3d5-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="6f3d5-177">Uygunsuzluk işleme için karantina bölgelerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="6f3d5-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="6f3d5-178">Stok yönetimi > Kurulum > Kalite yönetimi > Karantina bölgeleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="6f3d5-179">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-179">Click New.</span></span>
3. <span data-ttu-id="6f3d5-180">Karantina bölgesi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="6f3d5-181">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6f3d5-182">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f3d5-182">Close the page.</span></span>


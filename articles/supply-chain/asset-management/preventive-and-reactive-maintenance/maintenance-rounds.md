---
title: Bakım sıraları
description: Bu konuda Varlık Yönetimi'ndeki bakım sıraları açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4c9a2fee7d43142f8bb17f4e819c9949a2a20c41
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570042"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="e254d-103">Bakım sıraları</span><span class="sxs-lookup"><span data-stu-id="e254d-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e254d-104">**Varlık Yönetimi**'nde düzenli aralıklarla benzer bir görevi gerçekleştirmeniz gereken çeşitli varlıklar için bakım sıraları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="e254d-105">Örneğin aynı aralıklarda çeşitli makinelerde gerçekleştirilmesi gereken yağlama işleri veya güvenlik incelemesi işleri.</span><span class="sxs-lookup"><span data-stu-id="e254d-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="e254d-106">İlk adım, aynı bakım işi formuna gereksinim duyan varlıklar dahil olmak üzere bir bakım sırası oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="e254d-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="e254d-107">Ardından, bakım sıralarını zamanlarsınız.</span><span class="sxs-lookup"><span data-stu-id="e254d-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="e254d-108">Bakım sıralarını zamanlamayı tamamladığınızda sırayla ilgili tüm iş kayıtlarını **Tüm bakım zamanlaması** ve **Bakım zamanlaması satırları aç** seçeneklerinde görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="e254d-109">Ayrıca sıraya dayalı iş emri oluştururken bakım sıraları, işlem yapılacak yerleşime yüklü varlıklarda tamamlanmak üzere işlem yapılacak yerleşimlerde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e254d-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="e254d-110">İşlem yapılacak yerleşimlerde bakım sıralarını ayarlama hakkında daha fazla bilgi için [İşlem yapılacak yerleşimler oluşturma](../functional-locations/create-functional-locations.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="e254d-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="e254d-111">Bakım sırası ayarlama</span><span class="sxs-lookup"><span data-stu-id="e254d-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="e254d-112">**Varlık yönetimi** > **Kurulum** > **Önleyici bakım** > **Bakım sıraları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e254d-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="e254d-113">Yeni bir bakım sırası oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e254d-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="e254d-114">**Bakım sırası** alanına bir kod girin ve **Ad** alanına bakım sırası için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="e254d-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="e254d-115">**Başlangıç tarihi** alanında sıra için bir başlangıç tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="e254d-116">**Günler içinde bitirin** ve **Saatler içinde bitirin** alanlarına gün veya saat cinsinden beklenen bitiş tarihini ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="e254d-117">Beklenen bitiş tarihi, bakım zamanlaması satırları oluşturulduğunda hesaplanan başlangıç tarihine göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e254d-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="e254d-118">Örneğin ilgili işin başlangıç tarihinden itibaren bir hafta içinde tamamlanması gerektiğini belirtecek şekilde **Günler içinde bitir** alanına "7" ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="e254d-119">İş emirlerinin bu bakım sırasından oluşturulan bakım zamanlaması satırlarında otomatik olarak oluşturulması gerekiyorsa **Otomatik oluştur** geçiş düğmesinde "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="e254d-120">**İş emri türü** alanında, bu bakım sırasından oluşturulan iş emirlerinde kullanılacak iş emri türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="e254d-121">**Hizmet düzeyi** alanında, bu bakım sırasından oluşturulan iş emirlerinde kullanılacak iş emri hizmet düzeyini seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="e254d-122">**Varlık satırları** hızlı sekmesinde, bakım sırasına varlık eklemek için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e254d-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="e254d-123">Satır numarası, bakım sırasında varlıkların sırasını belirtecek şekilde **Satır numarası** alanına otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="e254d-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="e254d-124">**Varlık** alanında varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="e254d-125">**Bakım işi türü** alanında varlık için bakım işi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="e254d-126">Gerekirse, bakım işi türüyle ilgili **Bakım işi türü çeşidi**'ni ve **Ticaret**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="e254d-127">**Dönem türü** alanında yinelenmeyi (gün, hafta vb.) seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="e254d-128">**Dönem sıklığı** alanına bakım sırasının yinelenme sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="e254d-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="e254d-129">Örnek: **Dönem türü** alanında "Gün" seçeneğini belirlediyseniz ve bu alana "7" değerini girerseniz yeni bakım sırası satırları, önleyici bakım zamanlaması sırasında haftada bir kez oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e254d-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="e254d-130">**Başlangıç tarihi** alanında bakım sırasına dahil edilecek varlık için bir başlangıç tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="e254d-131">Bu tarih, bakım sırasında ayarlanan başlangıç tarihinden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e254d-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="e254d-132">Bakım sırasına daha fazla varlık eklemek için 9-16. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="e254d-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="e254d-133">**İşlem yapılacak yerleşim satırları** hızlı sekmesinde, bakım sırasına işlem yapılacak yerleşim eklemek için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e254d-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="e254d-134">Yukarıdaki ilgili alanların açıklamasına bakın.</span><span class="sxs-lookup"><span data-stu-id="e254d-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="e254d-135">Aynı alanlar, varlık satırı oluştururken de kullanılabilir ancak gerekirse işlem yapılacak yerleşim için **Üretici** ve **Model**'i de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="e254d-136">Bir satırda yalnızca işlem yapılacak yerleşimi seçerseniz ancak **Varlık türü**, **Üretici**, **Model**, **Bakım işi türü**, **Bakım işi türü çeşidi** ve **Ticaret** öğelerinde seçim yapmazsanız bakım zamanlaması sırasında bu işlem yapılacak yerleşimle ilgili tüm varlıklar bakım sırasına eklenir.</span><span class="sxs-lookup"><span data-stu-id="e254d-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="e254d-137">**Havuzlar** hızlı sekmesinde, bakım sırasına dahil edilecek bir iş emri havuzu seçmek için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e254d-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="e254d-138">Çeşitli iş emri havuzları tek bir bakım sırasına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e254d-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="e254d-139">Ayarınızı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="e254d-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="e254d-140">**Başlık** hızlı sekmesindeki **Ayrıntılar** grubunda bulunan **Varlıklar** ve**Satırlar** alanları, seçilen bakım sırasıyla ilgili varlıkların ve satırların toplam sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e254d-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="e254d-141">Aşağıdaki çizimde üç varlığı içeren bir bakım sırası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e254d-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![Şekil 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="e254d-143">Bakım sıralarını zamanla</span><span class="sxs-lookup"><span data-stu-id="e254d-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="e254d-144">Bakım sırasını ayarladığınızda bakım sırasıyla ilgili tüm işleri zamanlamak için bir iş zamanlaması çalıştırırsınız.</span><span class="sxs-lookup"><span data-stu-id="e254d-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="e254d-145">**Varlık yönetimi** > **Dönemsel** > **Önleyici bakım** > **Bakım sıraları zamanla** veya **Varlık yönetimi** > **Ortak** > **Bakım zamanlaması** > **Tüm bakım zamanlaması** veya **Bakım zamanlaması satırları aç** veya **Bakım zamanlaması havuzları aç**'a tıklayın > listeden bakım zamanlaması satırı seçin > **Bakım sıraları** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e254d-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="e254d-146">**Dönem** alanında, işi zamanlamak için kullanılacak dönem türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="e254d-147">**Dönem sıklığı** alanına, zamanlanan işe dahil edilecek dönem sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="e254d-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="e254d-148">Zamanlama başlangıcı geçerli tarihtir.</span><span class="sxs-lookup"><span data-stu-id="e254d-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="e254d-149">İş emrinin bakım sırasına göre otomatik olarak oluşturulması gerekiyorsa **Otomatik oluştur** geçiş düğmesinde "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="e254d-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="e254d-150">Bu geçiş düğmesi "Evet" olarak ayarlanırsa ve **Otomatik oluştur** geçiş düğmesi de **Bakım sıraları** formundaki bakım sırasında "Evet" olarak ayarlanırsa iş emirleri, bakım sırası satırları temel alınarak oluşturulur ve "Oluşturulan iş emri" durumuna sahip bakım zamanlaması satırları da oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e254d-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="e254d-151">Yalnızca **Otomatik oluştur** geçiş düğmelerinden biri "Evet" olarak ayarlanırsa bu açılır menüde veya **Bakım sıraları**'nda, yalnızca "Oluşturuldu" durumuna sahip bakım zamanlaması satırları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e254d-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="e254d-152">Bu durumda, iş emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="e254d-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="e254d-153">Gerekirse, işi zamanlamak için belirli sıralar veya başka bir başlangıç tarihi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="e254d-154">**Filtre**'ye tıklayın ve dahil edilecek sıraları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e254d-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="e254d-155">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e254d-155">Click **OK**.</span></span>

7. <span data-ttu-id="e254d-156">Artık bakım sıraları işlerini **Varlık yönetimi** > **Ortak** > **Bakım zamanlaması** > **Tüm bakım zamanlaması** veya **Bakım zamanlaması satırları aç** seçeneklerinde görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="e254d-157">Zamanlanan sıralar, bir iş emri havuzuna bağlanırsa bakım zamanlaması satırlarını **Bakım zamanlaması havuzları aç** seçeneğinde de görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="e254d-158">Bir sıradan oluşturulan bakım zamanlaması satırları "Bakım sıraları" referans türüne sahiptir.</span><span class="sxs-lookup"><span data-stu-id="e254d-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="e254d-159">Aşağıdaki iki çizimde **Bakım sıralarını zamanla** iletişim kutusundaki bir zamanlama işi ve söz konusu zamanlama işine göre **Tüm bakım zamanlamaları**'nda oluşturulan bakım zamanlaması satırları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e254d-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![Şekil 2](media/14-preventive-maintenance.png)

![Şekil 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="e254d-162">İş emirleri satıcı garantisi ile kapsanan varlıklarda el ile oluşturulduğunda kullanıcının garantiden haberdar olmasını sağlamak için bir iletişim kutusu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e254d-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="e254d-163">İş emrinin oluşturulması daha sonra iptal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="e254d-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="e254d-164">Otomatik olarak oluşturulan iş emirleri için garanti ilişkisi denetimi atlanır.</span><span class="sxs-lookup"><span data-stu-id="e254d-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="e254d-165">Sıraları düzenli aralıklarla zamanlamak için **Arka planda çalıştır** hızlı sekmesinde bir toplu iş ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e254d-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="e254d-166">Sıra birkaç iş emri havuzuna dahil edilirse (bkz. [İş emri havuzları](../work-orders/work-order-pools.md)) bir kayıt her bir havuz için **Bakım zamanlaması havuzları aç** seçeneğinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e254d-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="e254d-167">Bu işlem, iş emri havuzlarının filtre seçeneklerini en iyi duruma getirmek için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e254d-167">This is done to optimize the filtering options for work order pools.</span></span>


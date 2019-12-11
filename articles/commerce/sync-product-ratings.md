---
title: Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme
description: Bu konu, Microsoft Dynamics 365 Retail ürün derecelendirmelerinin nasıl eşitleneceğini açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698177"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a><span data-ttu-id="adb31-103">Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="adb31-103">Sync product ratings in Dynamics 365 Retail</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="adb31-104">Bu konu, Microsoft Dynamics 365 Retail ürün derecelendirmelerinin nasıl eşitleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="adb31-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="adb31-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="adb31-105">Overview</span></span>

<span data-ttu-id="adb31-106">Bir satış noktasında (POS) ve çağrı merkezlerindeki gibi, çok yönlü kanallar içindeki ürün derecelendirmelerini kullanmak için, derecelendirmeler ve İncelemeler hizmetindeki ürün derecelendirmeleri perakende kanal veritabanına alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="adb31-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Retail channel database.</span></span> <span data-ttu-id="adb31-107">Çok yönlü kanallarda ürün derecelendirmeleri sunulduklarında, müşterilerin satış ilişkileri ile etkileşimleri sırasında dolaylı olarak müşterilere yardımcı olabilirler.</span><span class="sxs-lookup"><span data-stu-id="adb31-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="adb31-108">Bu konuda şu görevler açıklanmıştır:</span><span class="sxs-lookup"><span data-stu-id="adb31-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="adb31-109">Ürün derecelendirmelerini içe aktarmak için bir perakende toplu işi konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="adb31-109">Configure a Retail batch job to import product ratings.</span></span>
1. <span data-ttu-id="adb31-110">Ürün değerlendirme eşitlemesiyle ilgili toplu işin başarılı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="adb31-111">Ürün derecelendirmelerini POS'ta kullanılabilir yapın.</span><span class="sxs-lookup"><span data-stu-id="adb31-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a><span data-ttu-id="adb31-112">Ürün derecelendirmelerini içe aktarmak için bir perakende toplu işi konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="adb31-112">Configure a Retail batch job to import product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="adb31-113">Başlamadan önce, perakende sürüm 10.0.6 veya sonraki sürümünün yüklü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="adb31-113">Before you start, make sure that version 10.0.6 or later of Retail is installed.</span></span>

### <a name="initialize-the-retail-scheduler"></a><span data-ttu-id="adb31-114">Retail Planlayıcısını Başlat</span><span class="sxs-lookup"><span data-stu-id="adb31-114">Initialize the retail scheduler</span></span>

<span data-ttu-id="adb31-115">Perakende planlayıcısı başlatmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="adb31-115">To initialize the retail scheduler, follow these steps.</span></span>

1. <span data-ttu-id="adb31-116">**Perakende \> Yönetim Merkezi ayarı \> Perakende Planlayıcısı \> Perakende Planlayıcısını Başlat**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="adb31-116">Go to **Retail \> Headquarters setup \> Retail scheduler \> Initialize retail scheduler**.</span></span> <span data-ttu-id="adb31-117">Alternatif olarak "Perakende Planlayıcısı Başlat"ı arayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-117">Alternatively, search for "Initialize retail scheduler."</span></span>
1. <span data-ttu-id="adb31-118">**Perakende Planlayıcısı Başlat** iletişim kutusunda, **varolan konfigürasyonu Sil** seçeneğinin **Hayır** olarak ayarlandığından emin olun ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-118">In the **Initialize retail scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="adb31-119">RetailProductRating alt işini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="adb31-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="adb31-120">**RetailProductRating** alt işinin var olduğunu doğrulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="adb31-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="adb31-121">**Perakende \> Yönetim Merkezi ayarı \> Perakende Planlayıcısı \> Planlayıcı alt işleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="adb31-121">Go to **Retail \> Headquarters setup \> Retail scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="adb31-122">Alternatif olarak, "Planlayıcı alt işleri"ni aratın.</span><span class="sxs-lookup"><span data-stu-id="adb31-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="adb31-123">Alt iş listesinde, **RetailProductRating** alt işini bulun veya arayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="adb31-124">Aşağıdaki çizimde Retail'de alt iş örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="adb31-124">The following illustration shows an example of the subjob details in Retail.</span></span>

![RetailProductRating alt işi ayrıntıları](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="adb31-126">**RetailProductRating** alt işi bulamazsanız, Perakende Planlayıcısını çalıştırmadan önce **ürün derecelendirmelerini Eşitle** işini ve **1040 CDX** işini zaten çalıştırılmış olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="adb31-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the retail scheduler.</span></span> <span data-ttu-id="adb31-127">Bu durumda, **tam veri eşitleme** işini çalıştırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="adb31-127">In this case, follow these steps to run the **Full data sync** job.</span></span>
>
> 1. <span data-ttu-id="adb31-128">**Perakende \> Yönetim Merkezi ayarı \> Perakende Planlayıcısı \> Kanal veritabanı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="adb31-128">Go to **Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span> <span data-ttu-id="adb31-129">Alternatif olarak, "kanal veritabanı" için arama yapın.</span><span class="sxs-lookup"><span data-stu-id="adb31-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="adb31-130">Eşitlenecek kanal veritabanını seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="adb31-131">Eylem bölmesinde **tam veri eşitleme**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="adb31-131">On the Action Pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="adb31-132">**Dağıtım zamanlaması seç** açılan iletişim kutusunda **1040 ürünleri** seçin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="adb31-133">**RetailProductRating** alt işin oluşturulduğunu doğrulamak için önceki yordamın adımlarını yineleyin.</span><span class="sxs-lookup"><span data-stu-id="adb31-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="adb31-134">Ürün derecelendirmelerini içeri aktar</span><span class="sxs-lookup"><span data-stu-id="adb31-134">Import product ratings</span></span>

<span data-ttu-id="adb31-135">Derecelendirmeler ve İncelemeler hizmetinden ürün derecelendirmelerini perakende olarak içe aktarmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="adb31-135">To import product ratings into Retail from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="adb31-136">**Perakende \> Yönetim Merkezi ayarı \> Perakende Planlayıcısı \> Ürün derecelendirme işini eşitle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="adb31-136">Go to **Retail \> Headquarters setup \> Retail scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="adb31-137">Alternatif olarak, "ürün derecelendirme işini Eşitle" yi aratın.</span><span class="sxs-lookup"><span data-stu-id="adb31-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="adb31-138">**Ürün derecelendirmelerini al** iletişim kutusunda, **arka planda çalıştır** hızlı sekmesinde **tekrarlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="adb31-139">**Tekrarı tanımla** iletişim kutusunda bir yinelenme düzeni ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="adb31-140">(Önerilen değer iki saattir.) Bir saatten az olan bir tekrarı planlanmayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="adb31-141">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-141">Select **OK**.</span></span>
1. <span data-ttu-id="adb31-142">**Toplu işleme** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="adb31-143">Bu ayar, günlükleri denetlemenize ve toplu işin durumunu doğrulayabileceğinizi garantilemeye yarar.</span><span class="sxs-lookup"><span data-stu-id="adb31-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="adb31-144">Toplu işi planlamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="adb31-145">Aşağıdaki çizimde Retail'de toplu iş yapılandırması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="adb31-145">The following illustration shows an example of batch job configuration in Retail.</span></span>

![Ürün derecelendirmeleri eşitleme toplu işleminin konfigürasyonu](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="adb31-147">Ürün değerlendirme eşitlemesiyle ilgili toplu işin başarılı olduğunu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="adb31-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="adb31-148">**Ürün derecelendirmeleri eşitleme** toplu işleminin başarılı olduğunu doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="adb31-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="adb31-149">**Perakende \> sistem yöneticisi \> sorgular \> toplu işler**'e gidin veya yalnızca perakende stok tutma birimi (SKU) kullanıyorsanız **perakende \> Sorgular ve raporlar \> toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="adb31-149">Go to **Retail \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Retail-only stock keeping unit (SKU), **Retail \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="adb31-150">Alternatif olarak, "toplu işler"i arayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="adb31-151">Toplu işin ayrıntılarını görüntülemek için, toplu iş listesinde, **iş açıklaması** sütununda "Ürün derecelendirmelerini al" içeren bir açıklama arayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="adb31-152">Planlanan başlangıç tarihi/saati ve yinelenme metni gibi toplu iş ayrıntılarını görüntülemek için iş kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="adb31-153">Aşağıdaki şekil toplu iş, iki saatlik aralıklarla çalışacak şekilde zamanlandığında, toplu iş ayrıntılarının perakende olarak bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="adb31-153">The following illustration shows an example of the batch job details in Retail when the batch job is scheduled to run at two-hour intervals.</span></span>

![Ürün derecelendirmesi eşitleme işinin ayrıntıları](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="adb31-155">Ürün derecelendirmelerini POS'ta kullanılabilir yapın</span><span class="sxs-lookup"><span data-stu-id="adb31-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="adb31-156">Dynamics 365 Commerce'deki derecelendirmeler ve İncelemeler çözümü bir çok yönlü kanal çözümüdür.</span><span class="sxs-lookup"><span data-stu-id="adb31-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="adb31-157">Ancak, ürün derecelendirmeleri POS'ta varsayılan olarak gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="adb31-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="adb31-158">Mağazalardaki müşterilere yardım etmek için, satış görevlileri tarafından yardım edilmekte olduğunda derecelendirmelere ve incelemelere bakın.</span><span class="sxs-lookup"><span data-stu-id="adb31-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="adb31-159">POS'ta ürün derecelendirmelerini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="adb31-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="adb31-160">**Perakende \> Perakende ayarı \> Parametreler \> Perakende parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="adb31-160">Go to **Retail \> Retail setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="adb31-161">Alternatif olarak, "Perakende parametreleri"ni arayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-161">Alternatively, search for "Retail parameters."</span></span>
1. <span data-ttu-id="adb31-162">**Konfigürasyon** parametreleri sekmesinde, **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="adb31-163">**RatingsAndReviews.EnableProductRatingsForRetailStores**gibi bir ad girin ve değeri **doğru** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="adb31-164">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-164">Select **Save**.</span></span>
1. <span data-ttu-id="adb31-165">**Perakende \> Perakende BT \> Dağıtım planı öğesine** gidin.</span><span class="sxs-lookup"><span data-stu-id="adb31-165">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span> <span data-ttu-id="adb31-166">Alternatif olarak, "dağıtım zamanlaması" için arama yapın.</span><span class="sxs-lookup"><span data-stu-id="adb31-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="adb31-167">İş listesinde, **1110** (**Global konfigürasyon**) öğesini seçin ve **şimdi Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="adb31-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="adb31-168">İş başarıyla çalıştırıldıktan sonra, ürün derecelendirmelerinin POS'ta şimdi gösterildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="adb31-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="adb31-169">Aşağıdaki çizimde, POS'ta ürün derecelendirmelerinin açılacağı perakende parametrelerinin konfigürasyonunda bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="adb31-169">The following illustration shows an example of the configuration of the Retail parameters to turn on product ratings at the POS.</span></span>

![POS'ta ürün değerlendirmeleriyle ilgili perakende parametrelerinin konfigürasyonu](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="adb31-171">Aşağıdaki çizim, POS'ta ürün derecelendirmeleri örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="adb31-171">The following illustration shows an example of product ratings at the POS.</span></span>

![POS'ta ürün derecelendirmeleri](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="adb31-173">Aşağıdaki çizim, çağrı merkezi kanallarında ürün derecelendirmeleri örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="adb31-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Çağrı merkezi kanalında ürün derecelendirmeleri](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="adb31-175">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="adb31-175">Additional resources</span></span>

[<span data-ttu-id="adb31-176">Derecelendirme ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="adb31-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="adb31-177">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="adb31-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="adb31-178">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="adb31-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="adb31-179">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="adb31-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

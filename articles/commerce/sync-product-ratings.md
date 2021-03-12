---
title: Dynamics 365 Commerce'de ürün derecelendirmelerini eşitleme
description: Bu konu, Microsoft Dynamics 365 Commerce ürün derecelendirmelerinin nasıl eşitleneceğini açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7318d53535a93352425f811ec90572e65aeb696
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006297"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="93193-103">Dynamics 365 Commerce'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="93193-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93193-104">Bu konu, Microsoft Dynamics 365 Commerce ürün derecelendirmelerinin nasıl eşitleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="93193-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="93193-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="93193-105">Overview</span></span>

<span data-ttu-id="93193-106">Bir satış noktasında (POS) ve çağrı merkezlerindeki gibi, çok yönlü kanallar içindeki ürün derecelendirmelerini kullanmak için, derecelendirmeler ve İncelemeler hizmetindeki ürün derecelendirmeleri Commerce kanal veritabanına alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="93193-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="93193-107">Çok yönlü kanallarda ürün derecelendirmeleri sunulduklarında, müşterilerin satış ilişkileri ile etkileşimleri sırasında dolaylı olarak müşterilere yardımcı olabilirler.</span><span class="sxs-lookup"><span data-stu-id="93193-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="93193-108">Bu konuda şu görevler açıklanmıştır:</span><span class="sxs-lookup"><span data-stu-id="93193-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="93193-109">Ürün derecelendirmelerini **derecelendirmeler ve İncelemeler hizmetinden** eşitlemek için **ürün derecelendirmeleri eşitleme işini** bir toplu iş olarak konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="93193-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="93193-110">Ürün değerlendirme eşitlemesiyle ilgili toplu işin başarılı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="93193-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="93193-111">Ürün derecelendirmelerini POS'ta kullanılabilir yapın.</span><span class="sxs-lookup"><span data-stu-id="93193-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="93193-112">Ürün derecelendirmelerini eşitlemek için bir toplu işi konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="93193-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93193-113">Başlamadan önce, Dynamics 365 Commerce sürüm 10.0.6 veya sonraki sürümünün yüklü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="93193-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="93193-114">Commerce Planlayıcısını Başlat</span><span class="sxs-lookup"><span data-stu-id="93193-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="93193-115">Tiaret planlayıcısı başlatmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="93193-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="93193-116">**Retail ve Commerce \> Genel merkez ayarı \> Commerce planlayıcısı \> Commerce planlayıcısını başlat**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="93193-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="93193-117">Alternatif olarak "Ticaret Planlayıcısı Başlat"ı arayın.</span><span class="sxs-lookup"><span data-stu-id="93193-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="93193-118">**Ticaret Planlayıcısı Başlat** iletişim kutusunda, **varolan konfigürasyonu Sil** seçeneğinin **Hayır** olarak ayarlandığından emin olun ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="93193-119">RetailProductRating alt işini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="93193-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="93193-120">**RetailProductRating** alt işinin var olduğunu doğrulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="93193-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="93193-121">**Retail ve Commerce \> Genel merkez ayarı \> Commerce planlayıcısı \> Planlayıcı alt işleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="93193-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="93193-122">Alternatif olarak, "Planlayıcı alt işleri"ni aratın.</span><span class="sxs-lookup"><span data-stu-id="93193-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="93193-123">Alt iş listesinde, **RetailProductRating** alt işini bulun veya arayın.</span><span class="sxs-lookup"><span data-stu-id="93193-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="93193-124">Aşağıdaki çizimde Commerce'de alt iş örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="93193-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![RetailProductRating alt işi ayrıntıları](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="93193-126">**RetailProductRating** alt işi bulamazsanız, Commerce Planlayıcısını çalıştırmadan önce **ürün derecelendirmelerini Eşitle** işini ve **1040 CDX** işini zaten çalıştırılmış olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93193-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="93193-127">Bu durumda, **tam veri eşitleme** işini çalıştırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="93193-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="93193-128">**Retail ve Commerce \> Genel merkez ayarı \> Commerce planlayıcısı \> Kanal veritabanı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="93193-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="93193-129">Alternatif olarak, "kanal veritabanı" için arama yapın.</span><span class="sxs-lookup"><span data-stu-id="93193-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="93193-130">Eşitlenecek kanal veritabanını seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="93193-131">Eylem bölmesinde **tam veri eşitleme**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93193-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="93193-132">**Dağıtım zamanlaması seç** açılan iletişim kutusunda **1040 ürünleri** seçin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="93193-133">**RetailProductRating** alt işin oluşturulduğunu doğrulamak için önceki yordamın adımlarını yineleyin.</span><span class="sxs-lookup"><span data-stu-id="93193-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="93193-134">Ürün derecelendirmelerini içeri aktar</span><span class="sxs-lookup"><span data-stu-id="93193-134">Import product ratings</span></span>

<span data-ttu-id="93193-135">Derecelendirmeler ve İncelemeler hizmetinden ürün derecelendirmelerini Commerce olarak içe aktarmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="93193-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="93193-136">**Retail ve Commerce \> Yönetim Merkezi ayarı \> Commerce Planlayıcısı \> Ürün derecelendirme işini eşitle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="93193-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="93193-137">Alternatif olarak, "ürün derecelendirme işini Eşitle" yi aratın.</span><span class="sxs-lookup"><span data-stu-id="93193-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="93193-138">**Ürün derecelendirmelerini al** iletişim kutusunda, **arka planda çalıştır** hızlı sekmesinde **tekrarlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="93193-139">**Tekrarı tanımla** iletişim kutusunda bir yinelenme düzeni ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="93193-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="93193-140">(Önerilen değer iki saattir.) Bir saatten az olan bir tekrarı planlanmayın.</span><span class="sxs-lookup"><span data-stu-id="93193-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="93193-141">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-141">Select **OK**.</span></span>
1. <span data-ttu-id="93193-142">**Toplu işleme** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="93193-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="93193-143">Bu ayar, günlükleri denetlemenize ve toplu işin durumunu doğrulayabileceğinizi garantilemeye yarar.</span><span class="sxs-lookup"><span data-stu-id="93193-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="93193-144">Toplu işi planlamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="93193-145">Aşağıdaki çizimde Commerce'de toplu iş yapılandırması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="93193-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Ürün derecelendirmeleri eşitleme toplu işleminin konfigürasyonu](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="93193-147">Ürün değerlendirme eşitlemesiyle ilgili toplu işin başarılı olduğunu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="93193-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="93193-148">**Ürün derecelendirmeleri eşitleme** toplu işleminin başarılı olduğunu doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="93193-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="93193-149">**Retail ve Commerce \> sistem yöneticisi \> sorgular \> toplu işler**'e gidin veya yalnızca Commerce stok tutma birimi (SKU) kullanıyorsanız **Retail ve Commerce \> Sorgular ve raporlar \> toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="93193-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="93193-150">Alternatif olarak, "toplu işler"i arayın.</span><span class="sxs-lookup"><span data-stu-id="93193-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="93193-151">Toplu işin ayrıntılarını görüntülemek için, toplu iş listesinde, **iş açıklaması** sütununda "Ürün derecelendirmelerini al" içeren bir açıklama arayın.</span><span class="sxs-lookup"><span data-stu-id="93193-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="93193-152">Planlanan başlangıç tarihi/saati ve yinelenme metni gibi toplu iş ayrıntılarını görüntülemek için iş kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="93193-153">Aşağıdaki şekil toplu iş, iki saatlik aralıklarla çalışacak şekilde zamanlandığında, toplu iş ayrıntılarının Commerce olarak bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="93193-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Ürün derecelendirmesi eşitleme işinin ayrıntıları](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="93193-155">Ürün derecelendirmelerini POS'ta kullanılabilir yapın</span><span class="sxs-lookup"><span data-stu-id="93193-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="93193-156">Dynamics 365 Commerce'deki derecelendirmeler ve İncelemeler çözümü bir çok yönlü kanal çözümüdür.</span><span class="sxs-lookup"><span data-stu-id="93193-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="93193-157">Ancak, ürün derecelendirmeleri POS'ta varsayılan olarak gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="93193-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="93193-158">Mağazalardaki müşterilere yardım etmek için, satış görevlileri tarafından yardım edilmekte olduğunda derecelendirmelere ve incelemelere bakın.</span><span class="sxs-lookup"><span data-stu-id="93193-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="93193-159">POS'ta ürün derecelendirmelerini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="93193-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="93193-160">**Retail ve Commerce \> Commerce ayarı \> Parametreler \> Commerce parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="93193-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="93193-161">Alternatif olarak, "Commerce parametreleri"ni arayın.</span><span class="sxs-lookup"><span data-stu-id="93193-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="93193-162">**Konfigürasyon** parametreleri sekmesinde, **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="93193-163">**RatingsAndReviews.EnableProductRatingsForRetailStores** gibi bir ad girin ve değeri **doğru** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="93193-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="93193-164">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-164">Select **Save**.</span></span>
1. <span data-ttu-id="93193-165">**Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="93193-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="93193-166">Alternatif olarak, "dağıtım zamanlaması" için arama yapın.</span><span class="sxs-lookup"><span data-stu-id="93193-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="93193-167">İş listesinde, **1110** (**Global konfigürasyon**) öğesini seçin ve **şimdi Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="93193-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="93193-168">İş başarıyla çalıştırıldıktan sonra, ürün derecelendirmelerinin POS'ta şimdi gösterildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="93193-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="93193-169">Aşağıdaki çizimde, POS'ta ürün derecelendirmelerinin açılacağı Commerce parametrelerinin konfigürasyonunda bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="93193-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![POS'ta ürün değerlendirmeleriyle ilgili Commerce parametrelerinin konfigürasyonu](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="93193-171">Aşağıdaki çizim, POS'ta ürün derecelendirmeleri örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="93193-171">The following illustration shows an example of product ratings at the POS.</span></span>

![POS'ta ürün derecelendirmeleri](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="93193-173">Aşağıdaki çizim, çağrı merkezi kanallarında ürün derecelendirmeleri örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="93193-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Çağrı merkezi kanalında ürün derecelendirmeleri](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="93193-175">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="93193-175">Additional resources</span></span>

[<span data-ttu-id="93193-176">Derecelendirme ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="93193-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="93193-177">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="93193-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="93193-178">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="93193-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="93193-179">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="93193-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

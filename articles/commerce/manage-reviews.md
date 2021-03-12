---
title: Derecelendirme ve incelemeleri yönetme
description: Bu konu, Microsoft Dynamics 365 Commerce site oluşturucuda derecelendirmelerin ve incelemelerin nasıl yönetileceğini açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
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
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a70d0526fb2443605a6b11df3ee281d4dd12f1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982578"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="6f94f-103">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="6f94f-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6f94f-104">Bu konu, Microsoft Dynamics 365 Commerce site oluşturucuda derecelendirmelerin ve incelemelerin nasıl yönetileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="6f94f-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="6f94f-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="6f94f-105">Overview</span></span>

<span data-ttu-id="6f94f-106">Dynamics 365 Commerce, kötü sözcükleri düzenleyerek metni otomatik olarak gözden geçirmek için Microsoft Azure öğretici hizmeti kullanır.</span><span class="sxs-lookup"><span data-stu-id="6f94f-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="6f94f-107">Ayrıca, Moderatörler  Dynamics 365 Commerce site oluşturucuyu kullanarak aşağıdaki el ile görevleri uygulayabilir:</span><span class="sxs-lookup"><span data-stu-id="6f94f-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="6f94f-108">Bunlara yanıt verip veya onları kaldırarak yapılan gözden geçirmeler.</span><span class="sxs-lookup"><span data-stu-id="6f94f-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="6f94f-109">Müşterinin isteği üzerindeki müşteri incelemelerini Silin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="6f94f-110">Toplu içe aktarma derecelendirmeleri ve tüm ürünlerle ilgili verileri bir Microsoft Power BI şablonu olarak inceler; böylece derecelendirmelere ve incelemelere ilişkin eğilimler analiz edilebilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="6f94f-111">İncelemeyi oku</span><span class="sxs-lookup"><span data-stu-id="6f94f-111">Read a review</span></span> 

<span data-ttu-id="6f94f-112">Commerce site oluşturucuda bir inceleme okumak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f94f-113">**Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="6f94f-114">Ürün kimliği, ürün adı veya metin İnceleme tarafından gösterilen incelemelere filtre uygulamak için sayfanın sağ üst tarafındaki arama alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="6f94f-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="6f94f-115">Ek filtreler, gözden geçirmeleri dönem, derecelendirme, kanal veya ilgi durumu (kapalı, yanıtlanan veya rapor edilen) ile sınırlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="6f94f-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Düzenleme giriş sayfası](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="6f94f-117">İncelemeyi yanıtlama</span><span class="sxs-lookup"><span data-stu-id="6f94f-117">Respond to a review</span></span> 

<span data-ttu-id="6f94f-118">Bazı durumlarda, bir ürünü satın alan müşteriler memnuniyet veya memnuniyetini veya ürünün nasıl kullanıldığını anlamamaktadır.</span><span class="sxs-lookup"><span data-stu-id="6f94f-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="6f94f-119">Bir moderatör olarak, bir gözden geçirme yanıtı postalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f94f-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="6f94f-120">Bu yanıt, sitede gözden geçirme ile birlikte görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="6f94f-121">Commerce site oluşturucuda bir incelemeyi yanıtlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f94f-122">**Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="6f94f-123">Yanıt gerektiren incelemeyi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="6f94f-124">Sağdaki özellikler bölmesinde, **Yanıt Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="6f94f-125">Yanıt metnini ve Yanıtlayıcı için gösterilmesi gereken adı girin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="6f94f-126">Varsayılan Yanıtlayıcı adı **moderatör**'dür.</span><span class="sxs-lookup"><span data-stu-id="6f94f-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="6f94f-127">Tamamladıktan sonra **Yanıt gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-127">When you've finished, select **Post response**.</span></span>

![İncelemeyi yanıtlama](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="6f94f-129">Bir inceleme atın</span><span class="sxs-lookup"><span data-stu-id="6f94f-129">Take down a review</span></span> 

<span data-ttu-id="6f94f-130">Bazen, moderatörlerde müşteri incelemelerini ele almak için bir iş doğrulaması vardır.</span><span class="sxs-lookup"><span data-stu-id="6f94f-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="6f94f-131">Commerce site oluşturucuda bir inceleme almak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f94f-132">**Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="6f94f-133">Alınması gereken incelemeyi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="6f94f-134">Sağdaki Özellikler bölmesinde **İnceleme Kaydet** altından bir kaydetme nedeni seçin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="6f94f-135">Müşterinin isteği üzerindeki müşteri incelemelerini Silin</span><span class="sxs-lookup"><span data-stu-id="6f94f-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="6f94f-136">Bazen müşteriler derecelendirmelerinin ve veri incelemelerinin bir e-ticaret Web sitesinden kalıcı olarak silinmesini ister.</span><span class="sxs-lookup"><span data-stu-id="6f94f-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="6f94f-137">Müşteriden kaldırma isteği alan bir yönetici, gözden geçirme silme özelliğini kullanarak müşterinin verilerini kaldırabilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="6f94f-138">Müşterinin verilerini bulmak ve silmek için, aracının, müşterinin oturum açmak ve gözden geçirmeleri sağlaması için kullandığı e-posta adresini gerekli kılar.</span><span class="sxs-lookup"><span data-stu-id="6f94f-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="6f94f-139">Commerce site oluşturucuda müşteri verilerini bulmak ve silmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f94f-140">**Ev \> Gözden geçirmeler \> Sil**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="6f94f-141">**E- posta adresine göre kullanıcıları ara** kutusuna müşterinin e-posta adresini girin ve **Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="6f94f-142">Müşterinin herhangi bir gözden geçirme faaliyeti varsa (örneğin, gönderimleri gözden geçirin, başka bir müşterinin incelemelerinin yardım veya başka bir müşterinin inceliğindeki Yorumlar hakkında oy varsa), sonuçlar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="6f94f-143">Her madde için **Sil** düğmesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="6f94f-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="6f94f-144">Silinmesi gereken her bir madde için **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="6f94f-145">Onaylamanız istendiğinde **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Müşteri verilerini silme](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="6f94f-147">Verilerin sistemden tümüyle kaldırılması yedi gün kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="6f94f-148">Moderatörler müşterileri bu gecikmeyle bilgilendirmelidir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="6f94f-149">Müşteriler kendi hesap ayarlarında adlarını değiştirdiyseniz, arama sonuçlarında birden çok öğe görünebilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="6f94f-150">Bu durumda, müşterinin verilerini tamamen silmek için, aracının her madde için **Sil**'i seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="6f94f-151">Derecelendirme ve inceleme verileri karşıdan yükleyin</span><span class="sxs-lookup"><span data-stu-id="6f94f-151">Download ratings and reviews data</span></span>

<span data-ttu-id="6f94f-152">Commerce site oluşturucu moderatörlerin, eğilimleri çözümleyebilmeleri için toplu olarak derecelendirmelere ve verileri gözden geçirmelerine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6f94f-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="6f94f-153">Temel ölçümleri içeren bir Power BI şablon kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="6f94f-154">Moderatörler Bu şablonu, Toplu içe aktarılan verileri bağlamak ve bir panoyu görüntülemek için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="6f94f-155">Özel bir pano oluşturmak zorunda kalmaları gerekmez.</span><span class="sxs-lookup"><span data-stu-id="6f94f-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="6f94f-156">Moderatörler, belirli ihtiyaçları karşılamak üzere Power BI şablonu da özelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="6f94f-157">Commerce site oluşturucuda dereceledirmeler ve incelemeler verilerini indirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f94f-158">**Ev \> Gözden geçirmeler \> Raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="6f94f-159">Derecelendirmeleri ve inceleme verilerini virgülle ayrılmış değerler (CSV) biçiminde toplu olarak indirmek için **İnceleme verileri indir** i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="6f94f-160">Derecelendirmelere ve incelemeler trendine bak</span><span class="sxs-lookup"><span data-stu-id="6f94f-160">View ratings and reviews trends</span></span>

<span data-ttu-id="6f94f-161">Moderatörler, Power BI şablonu bir panodaki eğilimleri görüntüleyebilmeleri için indirebilir.</span><span class="sxs-lookup"><span data-stu-id="6f94f-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="6f94f-162">Commerce site oluşturucuda dereceledirmeler ve incelemeler eğilimlerini görmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6f94f-163">**Ev \> Gözden geçirmeler \> Raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="6f94f-164">Şablonu indirmek için **PowerBI şablonu** seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-164">Select **PowerBI template** to download the template.</span></span>

    ![Power BI şablonunu indirme](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="6f94f-166">Power BI uygulamayı kullanarak karşıdan yüklenen şablonu açın.</span><span class="sxs-lookup"><span data-stu-id="6f94f-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="6f94f-167">Görüntülenen **Web içeriğine erişim** iletişim kutusunu kapatın ve sonra da görüntülenen "Yenile" hata iletisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f94f-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="6f94f-168">**Giriş** sayfasına gidin, **Düzenle sorgular**'ı seçin ve sonra **veri kaynağı ayarlarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="6f94f-169">**Veri kaynağı ayarları** iletişim kutusunda **kaynağı değiştir** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="6f94f-170">**URL** alanına önceki yordama indirdiğiniz İnceleme verilerinin yolunu girin (örneğin, **c:\\incelemeler\\İncelemelerVerileri.csv**).</span><span class="sxs-lookup"><span data-stu-id="6f94f-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Virgülle ayrılmış değerler iletişim kutusundaki URL alanı](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="6f94f-172">**Tamam** seçin ve daha sonra **Değişiklikleri uygulay**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="6f94f-173">Değişikliklerinizi veri kaynağına uygulamak için iki dakika arasında bir süre sürer.</span><span class="sxs-lookup"><span data-stu-id="6f94f-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="6f94f-174">Derecelendirmeleri ve İnceleme eğilimlerini görüntülemek için **eğilim sayfası** seçin.</span><span class="sxs-lookup"><span data-stu-id="6f94f-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Derecelendirmelere ve incelemeler trendleri](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="6f94f-176">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6f94f-176">Additional resources</span></span>

[<span data-ttu-id="6f94f-177">Derecelendirme ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="6f94f-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="6f94f-178">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="6f94f-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="6f94f-179">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6f94f-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="6f94f-180">Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="6f94f-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)

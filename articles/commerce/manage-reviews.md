---
title: Derecelendirme ve incelemeleri yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce derecelendirmeleri ve incelemeler denetleme aracı kullanılarak derecelendirmelerin ve incelemelerinin nasıl yönetileceği açıklanmaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698038"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="16c57-103">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="16c57-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="16c57-104">Bu konuda, Microsoft Dynamics 365 Commerce derecelendirmeleri ve incelemeler denetleme aracı kullanılarak derecelendirmelerin ve incelemelerinin nasıl yönetileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="16c57-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="16c57-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="16c57-105">Overview</span></span>

<span data-ttu-id="16c57-106">Dynamics 365 Commerce, kötü sözcükleri düzenleyerek metni otomatik olarak gözden geçirmek için Microsoft Azure öğretici hizmeti kullanır.</span><span class="sxs-lookup"><span data-stu-id="16c57-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="16c57-107">Ayrıca, moderörler, aşağıdaki el ile görevlerde derecelendirmeler ve gözden geçirme denetleme aracını kullanabilirler:</span><span class="sxs-lookup"><span data-stu-id="16c57-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="16c57-108">Bunlara yanıt verip veya onları kaldırarak yapılan gözden geçirmeler.</span><span class="sxs-lookup"><span data-stu-id="16c57-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="16c57-109">Müşterinin isteği üzerindeki müşteri incelemelerini Silin.</span><span class="sxs-lookup"><span data-stu-id="16c57-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="16c57-110">Toplu içe aktarma derecelendirmeleri ve tüm ürünlerle ilgili verileri bir Microsoft Power BI şablonu olarak inceler; böylece derecelendirmelere ve incelemelere ilişkin eğilimler analiz edilebilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="16c57-111">İncelemeyi oku</span><span class="sxs-lookup"><span data-stu-id="16c57-111">Read a review</span></span> 

1. <span data-ttu-id="16c57-112">**Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="16c57-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="16c57-113">Ürün kimliği, ürün adı veya metin İnceleme tarafından gösterilen incelemelere filtre uygulamak için sayfanın sağ üst tarafındaki arama alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="16c57-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="16c57-114">Ek filtreler, gözden geçirmeleri dönem, derecelendirme, kanal veya ilgi durumu (kapalı, yanıtlanan veya rapor edilen) ile sınırlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="16c57-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Düzenleme giriş sayfası](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="16c57-116">İncelemeyi yanıtlama</span><span class="sxs-lookup"><span data-stu-id="16c57-116">Respond to a review</span></span> 

<span data-ttu-id="16c57-117">Bazı durumlarda, bir ürünü satın alan müşteriler memnuniyet veya memnuniyetini veya ürünün nasıl kullanıldığını anlamamaktadır.</span><span class="sxs-lookup"><span data-stu-id="16c57-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="16c57-118">Bir moderatör olarak, bir gözden geçirme yanıtı postalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16c57-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="16c57-119">Bu yanıt, sitede gözden geçirme ile birlikte görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="16c57-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="16c57-120">Bir incelemeyi yanıtlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="16c57-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="16c57-121">**Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="16c57-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="16c57-122">Yanıt gerektiren incelemeyi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="16c57-123">Sağdaki özellikler bölmesinde, **Yanıt Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="16c57-124">Yanıt metnini ve Yanıtlayıcı için gösterilmesi gereken adı girin.</span><span class="sxs-lookup"><span data-stu-id="16c57-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="16c57-125">Varsayılan Yanıtlayıcı adı **moderatör**'dür.</span><span class="sxs-lookup"><span data-stu-id="16c57-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="16c57-126">Tamamladıktan sonra **Yanıt gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-126">When you've finished, select **Post response**.</span></span>

![İncelemeyi yanıtlama](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="16c57-128">Bir inceleme atın</span><span class="sxs-lookup"><span data-stu-id="16c57-128">Take down a review</span></span> 

<span data-ttu-id="16c57-129">Bazen, moderatörlerde müşteri incelemelerini ele almak için bir iş doğrulaması vardır.</span><span class="sxs-lookup"><span data-stu-id="16c57-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="16c57-130">Bir incelemeyi göndermek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="16c57-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="16c57-131">**Ev \> Gözden geçirmeler \> Düzenlemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="16c57-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="16c57-132">Alınması gereken incelemeyi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="16c57-133">Sağdaki Özellikler bölmesinde bir alt neden seçin ve sonra **aşağı al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="16c57-134">Müşterinin isteği üzerindeki müşteri incelemelerini Silin</span><span class="sxs-lookup"><span data-stu-id="16c57-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="16c57-135">Bazen müşteriler derecelendirmelerinin ve veri incelemelerinin bir e-ticaret Web sitesinden kalıcı olarak silinmesini ister.</span><span class="sxs-lookup"><span data-stu-id="16c57-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="16c57-136">Müşteriden kaldırma isteği alan bir yönetici, gözden geçirme silme özelliğini kullanarak müşterinin verilerini kaldırabilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="16c57-137">Müşterinin verilerini bulmak ve silmek için, aracının, müşterinin oturum açmak ve gözden geçirmeleri sağlaması için kullandığı e-posta adresini gerekli kılar.</span><span class="sxs-lookup"><span data-stu-id="16c57-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="16c57-138">Müşteri verilerini bulmak ve silmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="16c57-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="16c57-139">**Ev \> Gözden geçirmeler \> Sil**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="16c57-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="16c57-140">**E- posta adresine göre kullanıcıları ara** alanına müşterinin e-posta adresini girin ve **ara** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="16c57-141">Müşterinin herhangi bir gözden geçirme faaliyeti varsa (örneğin, gönderimleri gözden geçirin, başka bir müşterinin incelemelerinin yardım veya başka bir müşterinin inceliğindeki Yorumlar hakkında oy varsa), sonuçlar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="16c57-142">Her madde için **Sil** düğmesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="16c57-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="16c57-143">Silinmesi gereken her bir madde için **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="16c57-144">Onaylamanız istendiğinde **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Müşteri verilerini silme](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="16c57-146">Verilerin sistemden tümüyle kaldırılması yedi gün kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="16c57-147">Moderatörler müşterileri bu gecikmeyle bilgilendirmelidir.</span><span class="sxs-lookup"><span data-stu-id="16c57-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="16c57-148">Müşteriler kendi hesap ayarlarında adlarını değiştirdiyseniz, arama sonuçlarında birden çok öğe görünebilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="16c57-149">Bu durumda, müşterinin verilerini tamamen silmek için, aracının her madde için **Sil**'i seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="16c57-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="16c57-150">Derecelendirme ve inceleme verileri karşıdan yükleyin</span><span class="sxs-lookup"><span data-stu-id="16c57-150">Download ratings and reviews data</span></span>

<span data-ttu-id="16c57-151">Derecelendirmeler ve inceleme denetleme aracı, moderatörlerin, eğilimleri çözümleyebilmeleri için toplu olarak derecelendirmelere ve verileri gözden geçirmelerine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="16c57-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="16c57-152">Temel ölçümleri içeren bir Power BI şablon kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="16c57-153">Moderatörler Bu şablonu, Toplu içe aktarılan verileri bağlamak ve bir panoyu görüntülemek için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="16c57-154">Özel bir pano oluşturmak zorunda kalmaları gerekmez.</span><span class="sxs-lookup"><span data-stu-id="16c57-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="16c57-155">Moderatörler, belirli ihtiyaçları karşılamak üzere Power BI şablonu da özelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="16c57-156">Derecelendirmeleri karşıdan yüklemek ve verileri gözden geçirmeleri için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="16c57-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="16c57-157">**Ev \> Gözden geçirmeler \> Raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="16c57-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="16c57-158">Derecelendirmeleri ve inceleme verilerini virgülle ayrılmış değerler (CSV) biçiminde toplu olarak indirmek için **inceleme verileri indir**i seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="16c57-159">Derecelendirmelere ve incelemeler trendine bak</span><span class="sxs-lookup"><span data-stu-id="16c57-159">View ratings and reviews trends</span></span>

<span data-ttu-id="16c57-160">Moderatörler, Power BI şablonu bir panodaki eğilimleri görüntüleyebilmeleri için indirebilir.</span><span class="sxs-lookup"><span data-stu-id="16c57-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="16c57-161">Derecelendirmeleri karşıdan göstermek ve trendleri gözden geçirmeleri için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="16c57-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="16c57-162">**Ev \> Gözden geçirmeler \> Raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="16c57-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="16c57-163">Şablonu indirmek için **PowerBI şablonu** seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-163">Select **PowerBI template** to download the template.</span></span>

    ![Power BI şablonunu indirme](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="16c57-165">Power BI uygulamayı kullanarak karşıdan yüklenen şablonu açın.</span><span class="sxs-lookup"><span data-stu-id="16c57-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="16c57-166">Görüntülenen **Web içeriğine erişim** iletişim kutusunu kapatın ve sonra da görüntülenen "Yenile" hata iletisini kapatın.</span><span class="sxs-lookup"><span data-stu-id="16c57-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="16c57-167">**Giriş** sayfasına gidin, **Düzenle sorgular**'ı seçin ve sonra **veri kaynağı ayarlarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="16c57-168">**Veri kaynağı ayarları** iletişim kutusunda **kaynağı değiştir** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="16c57-169">**URL** alanına önceki yordama indirdiğiniz İnceleme verilerinin yolunu girin (örneğin, **c:\\incelemeler\\İncelemelerVerileri.csv**).</span><span class="sxs-lookup"><span data-stu-id="16c57-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Virgülle ayrılmış değerler iletişim kutusundaki URL alanı](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="16c57-171">**Tamam** seçin ve daha sonra **Değişiklikleri uygulay**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="16c57-172">Değişikliklerinizi veri kaynağına uygulamak için iki dakika arasında bir süre sürer.</span><span class="sxs-lookup"><span data-stu-id="16c57-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="16c57-173">Derecelendirmeleri ve İnceleme eğilimlerini görüntülemek için **eğilim sayfası** seçin.</span><span class="sxs-lookup"><span data-stu-id="16c57-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Derecelendirmelere ve incelemeler trendleri](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="16c57-175">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="16c57-175">Additional resources</span></span>

[<span data-ttu-id="16c57-176">Derecelendirme ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="16c57-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="16c57-177">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="16c57-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="16c57-178">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="16c57-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="16c57-179">Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="16c57-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)

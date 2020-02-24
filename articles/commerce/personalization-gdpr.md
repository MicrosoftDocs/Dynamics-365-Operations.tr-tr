---
title: Kişiselleştirilmiş önerilerden vazgeçme
description: Bu konu, müşterilerin Microsoft Dynamics 365 Commerce'ta kişiselleştirilmiş öneriler almamasına nasıl izin verileceğini açıklamaktadır.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8e7b800218f68167901d86d61ae483680a04cfab
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025288"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="c89f6-103">Kişiselleştirilmiş önerilerden vazgeçme</span><span class="sxs-lookup"><span data-stu-id="c89f6-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c89f6-104">Bu konu, müşterilerin Microsoft Dynamics 365 Commerce'ta kişiselleştirilmiş öneriler almamasına nasıl izin verileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c89f6-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c89f6-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="c89f6-105">Overview</span></span>

<span data-ttu-id="c89f6-106">Hesap oluşturma sırasında, yeni müşteriler otomatik olarak kişiselleştirilmiş öneriler almak için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c89f6-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="c89f6-107">Ancak, Dynamics 365 Commerce perakendeciler için kullanıcıların bu önerileri almalarını ve kişisel verilerinin işlenmesini kısıtlamalarını sağlamak amacıyla çeşitli yollar sunar.</span><span class="sxs-lookup"><span data-stu-id="c89f6-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="c89f6-108">Kişiselleştirilmiş Önerileri almaya çalışan kimliği doğrulanmış kullanıcılar, kişiselleştirilmiş listeleri hemen görmeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="c89f6-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="c89f6-109">Ek olarak, kişiselleştirme için toplanan tüm kişisel veriler kişiselleştirilmiş öneri modellerinden kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c89f6-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="c89f6-110">Kişiselleştirilmiş ürün önerileri hakkında bilgi için bkz. [Kişiselleştirilmiş önerileri etkinleştir](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="c89f6-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="c89f6-111">Bir tercih çıkış deneyimi uygulamak için perakendecilere yolları</span><span class="sxs-lookup"><span data-stu-id="c89f6-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="c89f6-112">Bir tercih çıkış deneyimi uygulamak için perakendecilerin üç yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="c89f6-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="c89f6-113">Kullanıcılar adına vazgeçme</span><span class="sxs-lookup"><span data-stu-id="c89f6-113">Opting out on behalf of users</span></span>

<span data-ttu-id="c89f6-114">Commerce arka ofiste hesap yönetiminde, perakendeciler Kullanıcı adına geri alabilir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="c89f6-115">Arka ofis ana sayfasında, **tüm müşterileri** arayın.</span><span class="sxs-lookup"><span data-stu-id="c89f6-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="c89f6-116">Müşteri arayıp seçin ve sonra **perakende** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c89f6-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Perakende hızlı sekmesi](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="c89f6-118">**Gizlilik**'in altında, **kişiselleştirmeyi devre dışı bırak** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c89f6-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Gizlilik ayarları](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="c89f6-120">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c89f6-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="c89f6-121">Modül tabanlı geri çevirme deneyimi</span><span class="sxs-lookup"><span data-stu-id="c89f6-121">Module-based opt-out experience</span></span>

<span data-ttu-id="c89f6-122">Perakendeciler, kimlik doğrulaması yapılmış kullanıcıların kendi kendilerine ait kişiselleştirilmiş öneriler dışında çalışmasına izin verebilir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="c89f6-123">Bu çıkış deneyimini sağlamak için, müşteri hesap profili sayfalarına Kullanıcı geri çevirme modülünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c89f6-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="c89f6-124">Özel uzatmalar</span><span class="sxs-lookup"><span data-stu-id="c89f6-124">Custom extensions</span></span>

<span data-ttu-id="c89f6-125">Perakendeciler, kullanıcılar için geri çevirme deneyimini yönetmek amacıyla kendi uzantılarını oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="c89f6-126">Daha fazla bilgi için, bkz. [Perakende Sunucu API'lerini çağır](e-commerce-extensibility/call-retail-server-apis.md) ve [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="c89f6-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="c89f6-127">Kimliği doğrulanmış bir kullanıcı adına kişiselleştirilmiş öneri verilerinin dijital kopyasını al</span><span class="sxs-lookup"><span data-stu-id="c89f6-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="c89f6-128">Müşteriler, kişisel verilerinin dijital bir kopyasını elde etmek ve ayrıca öneriler sonuçlarının dışa aktarılan görünümünü görmek isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="c89f6-129">Bir müşteri bu bilgileri isterse, satıcının, müşteri müşteri kimliğine göre, **Sizin için seçilen** liste için tam sonuçlar için Perakende Sunucu Uygulaması Programlama Arayüzü (API) ve sorguları çağıran özelleştirilmiş bir uzantı oluşturması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="c89f6-130">Sonuçlar daha sonra, virgülle ayrılmış değerler (CSV) biçiminde dışa aktarılabilir ve müşteriyle paylaşılabilir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="c89f6-131">Aşağıdaki örnek, bir perakendecin bu görevi nasıl yerine getirebileceği gösterir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="c89f6-132">Perakende, Kullanıcı adına kişisel öneri verileri çekmek için özel bir uzantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c89f6-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="c89f6-133">Modül oluşturma, varolan modülleri kopyalama, Retail Server API'leri arama ve veri eylemleri arama hakkında bilgi için, bkz [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="c89f6-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="c89f6-134">Özel uzantı **Tavsiyeler al** çekirdek verileri eylemine bir çağrı yapar ve listenin gereksinimlerine göre gerekli bilgileri geçirir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="c89f6-135">**Sizin için seçilen** liste için yapılan çekmeler durumunda, uzantı doğru liste adını ve müşteri kodunu veri eylemine iletmelidir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="c89f6-136">Özel uzantıyı oluşturmanın bir yolu, öneri sonuçlarını döndürmek için kullanılan varolan ürün koleksiyonu modülünü klonlamaktır.</span><span class="sxs-lookup"><span data-stu-id="c89f6-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="c89f6-137">Bu varolan modülü klonlayarak, bir satıcı varolan kodu değiştirebilir ve öneri sonuçlarını bir CSV dosyasına dışa aktarır yeni bir düğme ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="c89f6-138">Daha fazla bilgi için, bkz [Başlangıç kiti modülü kopyala](e-commerce-extensibility/clone-starter-module.md) ve [Ürün koleksiyon modülü](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c89f6-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="c89f6-139">Retail Server API kitaplığının tam görünümü için, [Retail Server müşteri ve tüketici API'leri](dev-itpro/retail-server-customer-consumer-api.md) konularına bakın.</span><span class="sxs-lookup"><span data-stu-id="c89f6-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="c89f6-140">Özel uzantı oluşturulduktan sonra, satıcı, kimliği doğrulanan kullanıcının benzersiz müşteri koduna göre tüm öneri sonuçlarının CSV dosyasını dışa aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="c89f6-141">Satıcı, kimliği doğrulanmış kullanıcıyla önerilen ürünlerin tam kişiselleştirilmiş listesini içeren dışa aktarılan CSV dosyasını paylaşabilir.</span><span class="sxs-lookup"><span data-stu-id="c89f6-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c89f6-142">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c89f6-142">Additional resources</span></span>

[<span data-ttu-id="c89f6-143">Ürün önerilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c89f6-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c89f6-144">Ürün önerilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c89f6-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c89f6-145">Kişiselleştirilmiş önerileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c89f6-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="c89f6-146">Sayfalarına ürün önerileri listesi ekleme</span><span class="sxs-lookup"><span data-stu-id="c89f6-146">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="c89f6-147">POS cihazlarına öneriler paneli Ekle</span><span class="sxs-lookup"><span data-stu-id="c89f6-147">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="c89f6-148">Ürün topluluğu modülüne genel bakış</span><span class="sxs-lookup"><span data-stu-id="c89f6-148">Product collection module overview</span></span>](product-collection-module-overview.md)

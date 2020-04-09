---
title: Bağlı uygulamalar kullanarak uygulama meta verilerine erişme
description: Bu konudaki adımlarda, Regulatory configuration service (RCS) kullanıcısının, Finance and Operations'ta meta verileri kullanarak yeni bir elektronik raporlama (ER) modeli eşlemesi tasarlayabileceği açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28b8346b916729669af42ca47fe9a882e7a77bd0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142213"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="05de3-103">Bağlı uygulamalar kullanarak uygulama meta verilerine erişme</span><span class="sxs-lookup"><span data-stu-id="05de3-103">Access application metadata by using connected applications</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05de3-104">Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama rolüne sahip Regulatory Configuration Service (RCS) kullanıcısının Finance and Operations'taki meta verilerini kullanarak nasıl yeni bir Elektronik raporlama (ER) modeli eşlemesi tasarlayabildiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="05de3-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="05de3-105">RCS bağlantılı uygulama kullanılarak uygulama meta verilerine çevrimiçi olarak erişilir.</span><span class="sxs-lookup"><span data-stu-id="05de3-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="05de3-106">Örnek ER model eşlemesi, dış ticari hareketlere erişmek üzere yapılandırılacak.</span><span class="sxs-lookup"><span data-stu-id="05de3-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="05de3-107">Bu adımları tamamlamak için öncelikle RCS'de [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="05de3-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="05de3-108">Konudaki adımları tamamlamadıysanız [ER yapılandırma kullanarak uygulama meta verilerine erişim](access-application-metadata-er-configuration.md) [elektronik raporlama örnekleri sayfasına](https://go.microsoft.com/fwlink/?linkid=862266) şu ER yapılandırmalarını indirmek ve kaydetmek için gidin: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml ve sonra prosedürü tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="05de3-109">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="05de3-109">Prerequisites</span></span>
1. <span data-ttu-id="05de3-110">**Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="05de3-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="05de3-111">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="05de3-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="05de3-112">Bu yapılandırma sağlayıcısını göremiyorsanız[Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-112">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="05de3-113">Gerekli ER yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="05de3-113">Get required ER configurations</span></span>
1. <span data-ttu-id="05de3-114">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="05de3-115">[ER yapılandırması kullanarak uygulama meta verilerine erişme](access-application-metadata-er-configuration.md) prosedüründeki adımları tamamladıysanız mevcut RCS örneğinde gerekli tüm ER yapılandırmalarına (dış ticaret meta verileri, model ve harita yapılandırmaları) zaten sahipsiniz.</span><span class="sxs-lookup"><span data-stu-id="05de3-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="05de3-116">Bu alt görevdeki kalan tüm adımları atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05de3-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="05de3-117">**Değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="05de3-118">**XML dosyasından yükle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="05de3-119">**Gözat**'a tıklayın ve **Dış ticaret meta verileri.xml** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="05de3-120">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-120">Click **OK**.</span></span> 
7. <span data-ttu-id="05de3-121">**Değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="05de3-122">**XML dosyasından yükle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="05de3-123">**Gözat**'a tıklayın ve **Dış ticaret meta modeli.xml** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="05de3-124">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-124">Click **OK**.</span></span> 
11. <span data-ttu-id="05de3-125">**Değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="05de3-126">**XML dosyasından yükle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="05de3-127">**Gözat**'a tıklayın ve **Dış ticaret meta eşlemesi.xml** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="05de3-128">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="05de3-129">Bağlı bir uygulamayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="05de3-129">Register a connected application</span></span>
1. <span data-ttu-id="05de3-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-130">Close the page.</span></span> 
2. <span data-ttu-id="05de3-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-131">Close the page.</span></span> 
3. <span data-ttu-id="05de3-132">**Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="05de3-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="05de3-133">**Bağlı uygulamalar**a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="05de3-134">Yapılandırılmış uygulamanın Azure tabanlı olduğundan ve geçerli RCS kullanıcısı için erişilebilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="05de3-134">Make sure that the configured application is Azure based and accessible for the current RCS user.</span></span> <span data-ttu-id="05de3-135">Ayrıca geçerli RCS kullanıcısının seçilen uygulamaya erişimi olması ve uygulamanın meta verilerine erişim ayrıcalıkları veren bu uygulamanın bir kullanıcı olarak kayıtlı olması da gerekir.</span><span class="sxs-lookup"><span data-stu-id="05de3-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application's metadata.</span></span> 
6. <span data-ttu-id="05de3-136">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-136">Click **New**.</span></span> 
7. <span data-ttu-id="05de3-137">**Ad** alanına "MyConnectedApp" yazın.</span><span class="sxs-lookup"><span data-stu-id="05de3-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="05de3-138">**Uygulama** alanına, "https:// mycompany.operations.dynamics.com" yazın.</span><span class="sxs-lookup"><span data-stu-id="05de3-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="05de3-139">**Kiracı** alanına "mycompany.onmicrosoft.com" yazın.</span><span class="sxs-lookup"><span data-stu-id="05de3-139">In the **Tenant** field, type 'mycompany.onmicrosoft.com'.</span></span> 
10. <span data-ttu-id="05de3-140">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-140">Click **Save**.</span></span> 
11. <span data-ttu-id="05de3-141">Yapılandırılmış uygulamaya olan bağlantıyı denetlediğinizde **Uzak uygulamaya bağlan** sayfasında **Seçilen uzak uygulama bağlantısına bağlanmak için buraya tıklayın**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="05de3-142">**Bağlantıyı denetle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="05de3-143">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-143">Click **Close**.</span></span> 
14. <span data-ttu-id="05de3-144">Bağlantı doğrulaması başarılı olduğunda geçerli kılavuzda yapılandırılan uygulama için sürüm ve kiracı ayrıntıları güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="05de3-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="05de3-145">Mevcut ER model eşleme yapılandırmasını inceleyin</span><span class="sxs-lookup"><span data-stu-id="05de3-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="05de3-146">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-146">Close the page.</span></span> 
2. <span data-ttu-id="05de3-147">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="05de3-148">Ağaçta **Dış ticari modeli** genişletin.</span><span class="sxs-lookup"><span data-stu-id="05de3-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="05de3-149">Ağaçta **Dış ticari model\Dış ticari eşleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="05de3-150">**Önkoşullar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="05de3-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="05de3-151">Şu anda bu eşleme meta veri yapılandırmasına başvuruyor.</span><span class="sxs-lookup"><span data-stu-id="05de3-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="05de3-152">Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verileri sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="05de3-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="05de3-153">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="05de3-154">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="05de3-155">Ağaçta, **Dynamics 365 for Operations\Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="05de3-156">**Kök ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="05de3-157">**Tablo** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="05de3-158">Şu anda bu eşleme meta veri yapılandırmasına başvuruyor.</span><span class="sxs-lookup"><span data-stu-id="05de3-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="05de3-159">Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verileri sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="05de3-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="05de3-160">**İptal**'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="05de3-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="05de3-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-161">Close the page.</span></span> 
13. <span data-ttu-id="05de3-162">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="05de3-163">Bağlantılı uygulamayı model eşlemeye atayın</span><span class="sxs-lookup"><span data-stu-id="05de3-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="05de3-164">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="05de3-165">**Myconnectedapp** uygulamasını seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="05de3-166">Şu anda bu eşleme, seçilen bağlı uygulamanın meta verilerine başvuruda bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="05de3-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="05de3-167">Aynı eşleme aynı anda meta veri yapılandırmasına ve bağlı uygulamaya başvurduğunda, bağlı uygulamanın meta verileri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="05de3-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="05de3-168">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="05de3-169">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="05de3-170">Ağaçta, **Dynamics 365 for Operations\Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="05de3-171">**Kök ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="05de3-172">**Tablo** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="05de3-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="05de3-173">Bu eşleme için atanmış olan bağlı uygulamanın tüm meta verileri kullandığından ikiden fazla uygulama tablosu sunuldu.</span><span class="sxs-lookup"><span data-stu-id="05de3-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="05de3-174">**İptal**'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="05de3-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="05de3-175">**Doğrula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="05de3-176">Belirtilen veri kaynağı öğeleriyle, bu eşleme için atanmış bağlı uygulamanın ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladık.</span><span class="sxs-lookup"><span data-stu-id="05de3-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="05de3-177">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-177">Close the page.</span></span> 
11. <span data-ttu-id="05de3-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="05de3-178">Close the page.</span></span> 

<span data-ttu-id="05de3-179">Bu model eşlemesini farklı bir sürüm uygulamasının meta verilerini kullanarak değerlendirmeniz gerektiğinde, bağlı başka bir uygulamayı kaydedin, bu model eşlemesine atayın ve yeni meta verilere göre doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="05de3-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>

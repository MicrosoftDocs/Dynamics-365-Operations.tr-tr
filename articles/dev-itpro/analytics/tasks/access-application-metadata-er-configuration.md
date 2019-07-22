---
title: ER yapılandırma kullanarak uygulama meta verilerine erişim
description: Bu konudaki adımlarda, Regulatory Configuration Service (RCS) kullanıcısının, Finance and Operations'ta meta verileri kullanarak yeni bir elektronik raporlama (ER) modeli eşlemesi tasarlayabileceği açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
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
ms.openlocfilehash: b95b41b27cecd4c71ed7646f329cf5736a01b561
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727041"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="aad26-103">ER yapılandırma kullanarak uygulama meta verilerine erişim</span><span class="sxs-lookup"><span data-stu-id="aad26-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aad26-104">Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama rolüne sahip Regulatory Configuration Service (RCS) kullanıcısının Dynamics 365 for Finance and Operations uygulamasının meta verilerini kullanarak nasıl yeni bir Elektronik raporlama (ER) modeli eşlemesi tasarlayabildiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="aad26-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the metadata of the Dynamics 365 for Finance and Operations application.</span></span> <span data-ttu-id="aad26-105">Uygulama meta verilerine, dış ticari hareketlere erişmek için örnek bir meta veri kümesi içeren ER meta veri yapılandırması kullanılarak erişilir.</span><span class="sxs-lookup"><span data-stu-id="aad26-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="aad26-106">RCS'de bu adımları tamamlamak için ilk olarak, [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="aad26-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="aad26-107">Daha sonra Finance and Operations konsundaki adımları tamamlayın, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="aad26-107">Then, in Finance and Operations, complete the steps in the topic, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aad26-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="aad26-108">Prerequisites</span></span>
1. <span data-ttu-id="aad26-109">**Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="aad26-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="aad26-110">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="aad26-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="aad26-111">Bu yapılandırma sağlayıcısını göremiyorsanız[Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="aad26-112">Meta veri yapılandırmasını içe aktarın</span><span class="sxs-lookup"><span data-stu-id="aad26-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="aad26-113">**Meta veri yapılandırması**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="aad26-114">Dış ticaret işletmesine elektronik belge oluşturmak üzere yapılandırılmış olan Finance and Operations uygulamasından meta veriler içeren ER meta veri yapılandırmasını içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="aad26-114">Import the ER metadata configuration that contains metadata from the Finance and Operations application that is configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="aad26-115">Bu ER meta veri yapılandırması [(ER) RCS'de kullanılacak uygulama meta verileri hazırlama](prepare-application-metadata-rcs.md) adımı tamamlandığında XML dosyası olarak dışa aktarılır.</span><span class="sxs-lookup"><span data-stu-id="aad26-115">This ER metadata configuration has been exported as XML file while the steps in the [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="aad26-116">**Değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="aad26-117">**XML dosyasından yükle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="aad26-118">**Gözat**'a tıklayın ve "Dış ticaret meta verileri.xml" dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="aad26-119">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-119">Click **OK**.</span></span> 
7. <span data-ttu-id="aad26-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="aad26-121">Veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="aad26-121">Create data model configuration</span></span>
1. <span data-ttu-id="aad26-122">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="aad26-123">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="aad26-124">**Ad** alanına, "Dış ticaret modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="aad26-125">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="aad26-126">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="aad26-127">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="aad26-128">**Ad** alanına "Kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="aad26-129">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-129">Click **Add**.</span></span> 
9. <span data-ttu-id="aad26-130">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="aad26-131">**Ad** alanına "Hareket" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="aad26-132">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="aad26-133">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-133">Click **Add**.</span></span> 
13. <span data-ttu-id="aad26-134">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="aad26-135">**Ad** alanına "Emtia kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="aad26-136">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="aad26-137">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-137">Click **Add**.</span></span> 
17. <span data-ttu-id="aad26-138">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="aad26-139">**Ad** alanına "Faturalanan tutar" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="aad26-140">**Madde türü** alanında **Gerçek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="aad26-141">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-141">Click **Add**.</span></span> 
21. <span data-ttu-id="aad26-142">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="aad26-143">**Ad** alanına "Tarih" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="aad26-144">**Madde türü** alanında **Tarih**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="aad26-145">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-145">Click **Add**.</span></span> 
25. <span data-ttu-id="aad26-146">**Kök referansı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="aad26-147">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-147">Click **OK**.</span></span> 
27. <span data-ttu-id="aad26-148">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-148">Click **Save**.</span></span> 
28. <span data-ttu-id="aad26-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-149">Close the page.</span></span> 
29. <span data-ttu-id="aad26-150">**Durumu değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="aad26-151">**Tamamla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="aad26-152">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="aad26-153">Model eşleme yapılandırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="aad26-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="aad26-154">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="aad26-155">**Yeni** alanına, "Dış ticaret modeli veri modelini temel alan Model Eşleme" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="aad26-156">**Ad** alanına, "Dış ticaret eşlemesi" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="aad26-157">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="aad26-158">**Önkoşullar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="aad26-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="aad26-159">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="aad26-160">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-160">Click **New**.</span></span> 
8. <span data-ttu-id="aad26-161">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="aad26-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="aad26-162">**Önkoşul bileşen türü** alanında **Yapılandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="aad26-163">**Dış ticaret meta veri** yapılandırılması seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="aad26-164">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-164">Click **Save**.</span></span> 
12. <span data-ttu-id="aad26-165">"Dış ticaret meta verileri" yapılandırmasındaki sürüm 1' e referans ekledik.</span><span class="sxs-lookup"><span data-stu-id="aad26-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="aad26-166">Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verileri sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="aad26-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="aad26-167">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-167">Close the page.</span></span> 
14. <span data-ttu-id="aad26-168">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="aad26-169">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="aad26-170">Ağaçta, **Dynamics 365 for Operations\Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="aad26-171">**Kök ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="aad26-172">**Ad** alanına "Intrastat" yazın.</span><span class="sxs-lookup"><span data-stu-id="aad26-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="aad26-173">**Intrastat** tablosu kayıtlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="aad26-174">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="aad26-175">Şu anda kullanılmakta olan meta veri kümesine sadece 2 tablo eklendiğinden sadece 2 tablo sunuldu.</span><span class="sxs-lookup"><span data-stu-id="aad26-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="aad26-176">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="aad26-177">Ağaçta **Intrastat**'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="aad26-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="aad26-178">Ağaçta **Intrastat\AmountMST**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="aad26-179">Ağaçta **Hareket = Intrastat**'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="aad26-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="aad26-180">Ağaçta **Hareket = Intrastat\Faturalanan tutar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="aad26-181">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="aad26-182">Ağaçta **Intrastat\TransDate**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="aad26-183">Ağaçta **Hareket = Intrastat\Tarih**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="aad26-184">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="aad26-185">Ağaçta **Intrastat\>İlişkiler**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="aad26-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="aad26-186">Ağaçta **Intrastat\>İlişkiler\IntrastatCommodity**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="aad26-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="aad26-187">Ağaçta **Intrastat\>İlişkiler\IntrastatCommodity\Code**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="aad26-188">Ağaçta **Hareket = Intrastat\Emtia kodu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="aad26-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="aad26-189">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="aad26-190">**Doğrula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="aad26-191">Belirtilen veri kaynağı öğeleriyle, başvurulan ER meta veri yapılandırmasından uygulama meta verilerinin ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladık.</span><span class="sxs-lookup"><span data-stu-id="aad26-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="aad26-192">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aad26-192">Click **Save**.</span></span> 
37. <span data-ttu-id="aad26-193">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-193">Close the page.</span></span> 
38. <span data-ttu-id="aad26-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aad26-194">Close the page.</span></span> 
39. <span data-ttu-id="aad26-195">Varolan meta veri kümesini genişletmeniz gerektiğinde bunu Finance and Operations'tan yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aad26-195">When you need to extend the existing set of metadata, you can do it in Finance and Operations.</span></span> <span data-ttu-id="aad26-196">Sonra acil durumda kurtarma için meta veri yapılandırmasının yeni sürümünü Finance and Operations'tan içe aktarabilir, bunları RCS 'ye aktarabilir ve alınan meta veri yapılandırmasının yeni sürümüne başvuran yapılandırılmış model eşleme yapılandırmasının önkoşullarını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aad26-196">Then you can export the new completed version of ER metadata configuration from Finance and Operation,s import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="aad26-197">Uygulama meta verileri hakkında bilgi elde etmenin bu yolu, yerel işletme verileri (LBD) veya şirket içi olarak dağıtılmış uygulamalar için kullanılabilecek tek yoldur (dağıtım modeli Dynamics 365 for Finance and Operations için kullanılır).</span><span class="sxs-lookup"><span data-stu-id="aad26-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used for Dynamics 365 for Finance and Operations).</span></span>
        

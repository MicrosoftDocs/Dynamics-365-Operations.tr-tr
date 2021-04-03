---
title: ER yapılandırma kullanarak uygulama meta verilerine erişim
description: Bu konuda, Regulatory configuration service kullanıcısının, meta verileri kullanarak nasıl yeni bir Elektronik raporlama modeli eşlemesi tasarlayabileceği açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c50047781fdc21c9157ceb634822c6cfb5a075
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559663"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="0c642-103">ER yapılandırma kullanarak uygulama meta verilerine erişim</span><span class="sxs-lookup"><span data-stu-id="0c642-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c642-104">Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama rolüne sahip Regulatory Configuration Service (RCS) kullanıcısının uygulama meta verilerini kullanarak nasıl yeni bir Elektronik raporlama (ER) modeli eşlemesi tasarlayabildiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="0c642-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="0c642-105">Uygulama meta verilerine, dış ticari hareketlere erişmek için örnek bir meta veri kümesi içeren ER meta veri yapılandırması kullanılarak erişilir.</span><span class="sxs-lookup"><span data-stu-id="0c642-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="0c642-106">RCS'de bu adımları tamamlamak için ilk olarak, [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0c642-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="0c642-107">Daha sonra [RCS'de kullanılacak uygulama meta verileri hazırlama](prepare-application-metadata-rcs.md) konusundaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0c642-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="0c642-108">Prerequisites</span></span>
1. <span data-ttu-id="0c642-109">**Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="0c642-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="0c642-110">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="0c642-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="0c642-111">Bu yapılandırma sağlayıcısını göremiyorsanız[Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="0c642-112">Meta veri yapılandırmasını içe aktarın</span><span class="sxs-lookup"><span data-stu-id="0c642-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="0c642-113">**Meta veri yapılandırması**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="0c642-114">Dış ticaret işletmesine elektronik belge oluşturmak üzere yapılandırılmış meta veriler içeren ER meta veri yapılandırmasını içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="0c642-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="0c642-115">Bu ER meta veri yapılandırması [RCS'de kullanılacak uygulama meta verileri hazırlama](prepare-application-metadata-rcs.md) adımı tamamlandığında XML dosyası olarak dışa aktarılır.</span><span class="sxs-lookup"><span data-stu-id="0c642-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="0c642-116">**Değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="0c642-117">**XML dosyasından yükle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="0c642-118">**Gözat**'a tıklayın ve "Dış ticaret meta verileri.xml" dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="0c642-119">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-119">Click **OK**.</span></span> 
7. <span data-ttu-id="0c642-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="0c642-121">Veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="0c642-121">Create data model configuration</span></span>
1. <span data-ttu-id="0c642-122">**Raporlama konfigürasyonları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="0c642-123">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="0c642-124">**Ad** alanına, "Dış ticaret modeli" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="0c642-125">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="0c642-126">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="0c642-127">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="0c642-128">**Ad** alanına "Kök" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="0c642-129">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-129">Click **Add**.</span></span> 
9. <span data-ttu-id="0c642-130">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="0c642-131">**Ad** alanına "Hareket" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="0c642-132">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="0c642-133">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="0c642-134">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="0c642-135">**Ad** alanına "Emtia kodu" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="0c642-136">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="0c642-137">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="0c642-138">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="0c642-139">**Ad** alanına "Faturalanan tutar" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="0c642-140">**Madde türü** alanında **Gerçek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="0c642-141">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="0c642-142">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="0c642-143">**Ad** alanına "Tarih" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="0c642-144">**Madde türü** alanında **Tarih**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="0c642-145">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="0c642-146">**Kök referansı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="0c642-147">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="0c642-148">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="0c642-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-149">Close the page.</span></span> 
29.    <span data-ttu-id="0c642-150">**Durumu değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="0c642-151">**Tamamla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="0c642-152">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="0c642-153">Model eşleme yapılandırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c642-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="0c642-154">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="0c642-155">**Yeni** alanına, "Dış ticaret modeli veri modelini temel alan Model Eşleme" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="0c642-156">**Ad** alanına, "Dış ticaret eşlemesi" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="0c642-157">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="0c642-158">**Önkoşullar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0c642-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="0c642-159">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="0c642-160">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-160">Click **New**.</span></span> 
8. <span data-ttu-id="0c642-161">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0c642-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="0c642-162">**Önkoşul bileşen türü** alanında **Yapılandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="0c642-163">**Dış ticaret meta veri** yapılandırılması seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="0c642-164">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="0c642-165">"Dış ticaret meta verileri" yapılandırmasındaki sürüm 1' e referans ekledik.</span><span class="sxs-lookup"><span data-stu-id="0c642-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="0c642-166">Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verileri sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="0c642-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="0c642-167">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-167">Close the page.</span></span> 
14.    <span data-ttu-id="0c642-168">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="0c642-169">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="0c642-170">Ağaçta, **Dynamics 365 for Operations\Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="0c642-171">**Kök ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="0c642-172">**Ad** alanına "Intrastat" yazın.</span><span class="sxs-lookup"><span data-stu-id="0c642-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="0c642-173">**Intrastat** tablosu kayıtlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="0c642-174">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0c642-175">Şu anda kullanılmakta olan meta veri kümesine sadece 2 tablo eklendiğinden sadece 2 tablo sunuldu.</span><span class="sxs-lookup"><span data-stu-id="0c642-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="0c642-176">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="0c642-177">Ağaçta **Intrastat**'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="0c642-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="0c642-178">Ağaçta **Intrastat\AmountMST**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="0c642-179">Ağaçta **Hareket = Intrastat**'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="0c642-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="0c642-180">Ağaçta **Hareket = Intrastat\Faturalanan tutar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="0c642-181">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="0c642-182">Ağaçta **Intrastat\TransDate**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="0c642-183">Ağaçta **Hareket = Intrastat\Tarih**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="0c642-184">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="0c642-185">Ağaçta **Intrastat\>İlişkiler**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="0c642-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="0c642-186">Ağaçta **Intrastat\>İlişkiler\IntrastatCommodity**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="0c642-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="0c642-187">Ağaçta **Intrastat\>İlişkiler\IntrastatCommodity\Code**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="0c642-188">Ağaçta **Hareket = Intrastat\Emtia kodu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="0c642-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="0c642-189">**Bağla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="0c642-190">**Doğrula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0c642-191">Belirtilen veri kaynağı öğeleriyle, başvurulan ER meta veri yapılandırmasından uygulama meta verilerinin ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladık.</span><span class="sxs-lookup"><span data-stu-id="0c642-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="0c642-192">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0c642-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="0c642-193">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-193">Close the page.</span></span> 
38.    <span data-ttu-id="0c642-194">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0c642-194">Close the page.</span></span> 
39.    <span data-ttu-id="0c642-195">Gerektiğinde, var olan meta veri kümesini genişletebilir ve sonra da ER meta veri yapılandırmasının yeni tamamlanan sürümünü dışa aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c642-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="0c642-196">Daha sonra bu grubu RCS 'ye aktarabilir ve içe aktarılan meta veri yapılandırmasının yeni bir sürümüne başvuran yapılandırılmış model eşleme yapılandırmasının önkoşullarını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c642-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="0c642-197">Uygulama meta verileri hakkında bilgi elde etmenin bu yolu yerel olarak dağıtılmış uygulamalar için kullanılabilecek tek yoldur (yerel işletme verileri (LBD) veya şirket içi dağıtım modeli kullanıldığında).</span><span class="sxs-lookup"><span data-stu-id="0c642-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
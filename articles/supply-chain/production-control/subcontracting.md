---
title: Alt sözleşme
description: Bu konu, Dynamics 365 Supply Chain Management içinde üretimde taşeron kullanımın için bir inceleme rehberi yapmanıza olanak sağlar.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3e282e0676e53200b0993dd9cb2b52e08fe97dca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981468"
---
# <a name="subcontracting"></a><span data-ttu-id="f3565-103">Alt sözleşme</span><span class="sxs-lookup"><span data-stu-id="f3565-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3565-104">Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta üretimde alt sözleşme için bir kılavuz yapmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="f3565-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f3565-105">Bu konunun ilk bölümü veri kurulumunu açıklar.</span><span class="sxs-lookup"><span data-stu-id="f3565-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="f3565-106">İkinci bölüm, gözden geçirme adımlarını anlatır.</span><span class="sxs-lookup"><span data-stu-id="f3565-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="f3565-107">Hedef kitle</span><span class="sxs-lookup"><span data-stu-id="f3565-107">Target audience</span></span>

<span data-ttu-id="f3565-108">Bu konu, üretimde alt sözleşme oluşturmayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="f3565-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="f3565-109">Bir taşeron etkinlik akışı temel kurulumu yapmak için HQUS tüzel içinde varolan verileri kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="f3565-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="f3565-110">HQUS tüzel varlığındaki demo verisi, gözden geçirmedeki adımları desteklemek üzere önceden ayarlanmış kurulum parametrelerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="f3565-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="f3565-111">Gözden geçirme, çeşitli roller için sorunlu noktaları ve zorlukları ele alsa da, bu sistem yöneticisi tarafından tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="f3565-112">Gösteri senaryosu</span><span class="sxs-lookup"><span data-stu-id="f3565-112">Demo scenario</span></span>

<span data-ttu-id="f3565-113">HQUS tüzel varlığında, yüksek kaliteli hoparlörler üretilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f3565-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="f3565-114">Üretim işlemi sırasında, hoparlörler aşağıdaki üç işlemden geçer.</span><span class="sxs-lookup"><span data-stu-id="f3565-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="f3565-115">**Ön montaj** – hoparlörü kabini birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="f3565-116">Kabin için malzemeler, işlem başlamadan önce malzeme deposundan çekilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="f3565-117">**Kaplama** – hoparlörü kabini birleştirildikten sonra kaplanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f3565-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="f3565-118">Bu işlem bir bir satıcı (alt yüklenici) tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="f3565-119">Önceden oluşturulmuş hoparlör kabini ile birlikte iki malzeme kaplama alt yüklenici çoğuyla birlikte gelmektedir.</span><span class="sxs-lookup"><span data-stu-id="f3565-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="f3565-120">**Sonlandırma** – önceden birleştirilmiş hoparlörü kabininin alt yüklenici tarafından kaplanmasından sonra montajın tamamlanması için hoparlörü kabinini alt yüklenici tarafından HQUS tüzel varlığına döndürülür.</span><span class="sxs-lookup"><span data-stu-id="f3565-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="f3565-121">Aşağıda, tüketim malzemelerini ve üç işlemi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3565-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Ön montaj, kaplama ve bitiş işlemleri ve bunların tükettiği malzemeleri](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="f3565-123">Ayarlama</span><span class="sxs-lookup"><span data-stu-id="f3565-123">Setup</span></span>

<span data-ttu-id="f3565-124">Gözden geçirmeye başlamadan önce, verileri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f3565-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="f3565-125">Tamamlanmış ürünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="f3565-125">Set up the finished product</span></span>

<span data-ttu-id="f3565-126">Bu yordam, serbest bırakılan ürün D8100'ün "Kaplamalı Kabin" kurulumunu ele alır.</span><span class="sxs-lookup"><span data-stu-id="f3565-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="f3565-127">**Serbest bırakılan ürün ayrıntıları** sayfasını açmak için **Ürün bilgi yönetimi \>Ürünler \> Serbest bırakılan ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="f3565-128">Hızlı filtre alanına varolan serbest ürünü bulmak için **D8100** girin.</span><span class="sxs-lookup"><span data-stu-id="f3565-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Serbest bırakılan ürün ayrıntıları sayfasında serbest bırakılan ürün D8100'ü filtrelemek](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="f3565-130">Eylem Bölmesi üzerinde **Mühendis** sekmesinde, **Yol** sayfasını açmak için **Yol**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="f3565-131">**Yol** sayfası, serbest bırakılan ürün D8100 için sekiz rota sürümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3565-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="f3565-132">Sekiz rota sürümü, tesis 1 ve tesis 5 üzerinde bölünmüş dört rotayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3565-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="f3565-133">Rota 000400 kullanılan maliyetlendirme, rota 00041 kaplama operasyonun dahili bir işlemdir olması durumunda ve rota 00042 kullanılan kaplama operasyon harici bir işlemi olduğunda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f3565-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Rota sayfasında sekiz Rota sürümleri](./media/subcontract03_route-page.png)

4. <span data-ttu-id="f3565-135">Üst bölmede, **Sürümler** kılavuzunda, tesis **5** için rota versiyonunu **00042** seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="f3565-136">Alt bölmede, **Genel Bakış** sekmesinde, kılavuzda **20** (**Cbnt CtSc**) seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Tesis 5 için rota sürümü 00042 için operasyon 20 seçili](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="f3565-138">**Genel** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-138">Select the **General** tab.</span></span>

    <span data-ttu-id="f3565-139">**Rota türü** alanının **Satıcı** olarak ayarlanmış olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f3565-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="f3565-140">Bu değer operasyon 20'nin (Cbnt CtSc) bir taşeron operasyonu olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3565-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Rota türü alanı, Genel sekmesinde Satıcı olarak ayarlı](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="f3565-142">**Kaynak gereksinimleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="f3565-143">Yeterlilikler, üretim iş planlama çizelgeleme sırasında geçerli bir kaynağı bulmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f3565-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="f3565-144">Operasyon 20 için (Cbnt CtSc), kaynağın iki yeteneği olduğuna dikkat edin, **Kaplama** ve **Kaplanmış kabinler**, gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f3565-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Kaynak gereksinimleri sekmesinde Kaplama ve Kaplamalı kabinler yetenekleri](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="f3565-146">**Uygun kaynaklar**'ı **Uygun kaynakları** iletişim kutusunu açmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="f3565-147">Operasyon için kaynak gereksinimleriyle eşleşen üç kaynak bulundu.</span><span class="sxs-lookup"><span data-stu-id="f3565-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="f3565-148">Kaynaklar 8851 ve 8852'nin **Satıcı** türünde olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f3565-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Uygun kaynaklar iletişim kutusunda üç uygun kaynak](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="f3565-150">**Tamam**'ı seçin, kapatmak için **Uygun kaynaklar** iletişim kutusunu ve **Rota** sayfasına dönmek için.</span><span class="sxs-lookup"><span data-stu-id="f3565-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="f3565-151">**Serbest bırakılan ürün ayrıntıları** sayfasına dönmek için **Yol** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="f3565-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Serbest bırakılan ürün ayrıntıları sayfası](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="f3565-153">Eylem Bölmesi üzerinde **Mühendis** sekmesinde, **Ürün Reçetesi sürümleri** sayfasını açmak için **Ürün Reçetesi sürümleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="f3565-154">**Ürün reçetesi sürümleri** sayfası serbest bırakılan ürün D8100 için dört ürün reçetesi (BOM) sürümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3565-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="f3565-155">Ürün reçetesi 000040 planlama ve maliyetlendirme, şirket içinde kaplama işlemi yapılıyorsa ürün reçetesi 000041 ve kaplama işlemi taşeron tarafından yapılıyorsa 000042 ve 000043 ürün reçeteleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f3565-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="f3565-156">Öğe S8050'ni bir **servis** öğesi türü olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f3565-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="f3565-157">Bu madde, alt sözleşmeli işi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f3565-157">This item represents the subcontracted work.</span></span>

    ![Ürün reçetesi versiyonları sayfasında dört ürün reçetesi versiyonları](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="f3565-159">**Ürün reçetesi satırları** hızlı sekmesinde, **Düzenle ürün reçetesi satırı** iletişim kutusunu açmak için **Düzenle** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f3565-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="f3565-160">Serbest bırakılan ürün D8100 için bir üretim emri oluşturulduğunda ve tahmini yapıldığında, bir satınalma emri otomatik olarak öğe S8050 için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f3565-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="f3565-161">Bu satınalma siparişi üretim emrine bağlanır.</span><span class="sxs-lookup"><span data-stu-id="f3565-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="f3565-162">Otomatik olarak oluşturulacak, satınalma siparişleri için **Satır türü** alanının **Satıcı** olarak ayarlanması ve alt yüklenici için satıcı hesabının seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f3565-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="f3565-163">Bu durumda, satıcı ABD-801 hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="f3565-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="f3565-164">Ürün reçetesi satırının operasyon numarası (Bu durumda, 20) aracılığıyla kaplama işlemi bağlı olduğu dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f3565-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Ürün reçetesi iletim kutusunu düzenlemek](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="f3565-166">Ambar çalışanları için bir parola oluşturun</span><span class="sxs-lookup"><span data-stu-id="f3565-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="f3565-167">El cihazı kullanan ambar çalışanları için bir parola tanımlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="f3565-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="f3565-168">**Çalışma kullanıcıları** sayfasını açmak için **Ambar yönetimi \>Kurulum \> Çalışan** seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="f3565-169">**Kullanıcılar** hızlı sekmesinde, kullanıcı **51** için satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![İş kullanıcıları sayfası](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="f3565-171">**Parola sıfırlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="f3565-172">**Parola** ve **Parolayı onayla** alanlarına **1** girin.</span><span class="sxs-lookup"><span data-stu-id="f3565-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="f3565-173">**Parola ayarlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="f3565-174">Adım adım gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="f3565-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="f3565-175">**Senaryo ve arka plan**</span><span class="sxs-lookup"><span data-stu-id="f3565-175">**Scenario and background**</span></span>

<span data-ttu-id="f3565-176">Ürün D8100 "Kaplamalı Kabin" için 10 adetlik bir üretim emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f3565-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="f3565-177">Kabinlerin kaplaması, satıcı ABD-801 Mükemmel Kaplama Çözümleri'nde gerçekleştirilen bir alt sözleşmeli iştir.</span><span class="sxs-lookup"><span data-stu-id="f3565-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="f3565-178">Üretim emri üç işlemden oluşur.</span><span class="sxs-lookup"><span data-stu-id="f3565-178">The production order consists of three operations.</span></span> <span data-ttu-id="f3565-179">İlk işlemde kabin şirket içi operasyon olarak önceden bir araya getirilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="f3565-180">Ön montaj için hammadde ambarında çekme için serbest bırakılır.</span><span class="sxs-lookup"><span data-stu-id="f3565-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="f3565-181">Ön montaj işleminden sonra önceden oluşturulmuş kabin, Mükemmel Kaplama Çözümleri'nde kaplama çalışması için gerekli olan iki malzeme ile birlikte gönderilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="f3565-182">Kaplanmış kabin satıcıdan geri geldiğinde, tamamlanmış olarak raporlanmadan önce şirket içi son montaj işleminden geçer.</span><span class="sxs-lookup"><span data-stu-id="f3565-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="f3565-183">**Tüm üretim emirleri** sayfasını açmak için **Üretim kontrolü \> Üretim emirleri \> Tüm üretim emirlerini**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="f3565-184">Eylem bölmesinde, **Yeni üretim emri**'ni, **Üretim emri oluştur** iletişim kutusunu açmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Üretim emri iletişim kutusu oluşturma](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="f3565-186">**Öğe numarası** alanında, **D8100**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="f3565-187">Öğe numarasını seçtikten sonra, stok boyutları için alanlar belirir.</span><span class="sxs-lookup"><span data-stu-id="f3565-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="f3565-188">**Renk** alanında, **Krom** seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="f3565-189">Ürün reçetesi ve rota için etkin sürümlerin yerleştirilmesini soracak bir ileti kutusu görünür.</span><span class="sxs-lookup"><span data-stu-id="f3565-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![İleti kutusu](./media/subcontract13_message-box.png)

5. <span data-ttu-id="f3565-191">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-191">Select **Yes**.</span></span> 

    <span data-ttu-id="f3565-192">**Üretim emri oluştur** iletişim kutusunda, ürün D8100 için ürün reçetesi ve rota için etkin sürümler otomatik olarak **Ürün reçetesi numarası** ve **Rota numarası** alanlarında sırasıyla otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="f3565-193">Bu durumda, ürün reçetesi **000040** ve rota **000040** seçilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f3565-194">Ürün reçetesi ve rota için sürüm 000040 planlama ve maliyetlendirme için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f3565-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="f3565-195">**Site** alanında, **5**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="f3565-196">**Ambar** alanında **51**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="f3565-197">**Ürün reçetesi numarası** ve **Rota numarası** alanlarında, otomatik olarak **000042** olarak seçilen değeri değiştirin.</span><span class="sxs-lookup"><span data-stu-id="f3565-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3565-198">Ürün reçetesi ve rota için sürüm 000042, kabinin kaplamasını satıcı ABD-801'e alt sözleşmeli vermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f3565-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Üretim emri oluştur iletişim kutusunda ayarlanan değerler](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="f3565-200">Üretim emri oluşturmak ve **Tüm üretim emirleri** sayfasına dönmek için **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Tüm üretim emirlerini sayfasında yeni üretim emri](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="f3565-202">Eylem bölmesinde, **Üretim emri** sekmesinde, **Tahmin** iletişim kutusunu açmak için **Tahmin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Tahmin iletişim kutusu](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="f3565-204">Tahmini onaylamak ve **Tüm üretim emirleri** sayfasına dönmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3565-205">Üretim emri tahmini yaptığınızda, servis maddesi S8050 için satınalma siparişi, satıcı ABD-801 için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f3565-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="f3565-206">Eylem Bölmesi üzerinde, **Üretim emri** sekmesinde, üretim emri için Ürün Reçetesi satırlarını görüntüleyebileceğiniz **Ürün reçetesi** sayfasını açmak için **Ürün reçetesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="f3565-207">Servis maddesi S8050 için üretim emri tahmini yapıldığında oluşturulan satınalma siparişi için bir referans olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f3565-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Ürün reçetesi sayfasındaki Üretim emri Ürün reçetesi satırları](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="f3565-209">**Tüm üretim emirleri** sayfasına dönmek için **Ürün reçetesi** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="f3565-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="f3565-210">Eylem bölmesinde, **Planlama** sekmesinde, **İş planlama** iletişim kutusunu açmak için **Planlanan işler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="f3565-211">Aşağıdaki değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="f3565-211">Specify the following values:</span></span>

    - <span data-ttu-id="f3565-212">**İş planlama çizelgeleme yönü** alanında **Yarından ileriye doğru**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="f3565-213">**Sınırlı kapasite** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f3565-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![İş planlama iletişim kutusu](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="f3565-215">**Tamam**'ı seçin, kapatmak için **İş planlama** iletişim kutusunu ve **Tüm üretim emirleri** sayfasına dönmek için.</span><span class="sxs-lookup"><span data-stu-id="f3565-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="f3565-216">Eylem Bölmesinde, **Planlama** sekmesinde, **Gannt grafiği - kaynak görünümü**'nü açmak için **Gannt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="f3565-217">Gantt şeması, kaynaklar üzerinde üretim işlerinin nasıl zamanlandığına dair görsel bir bakış gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3565-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="f3565-218">Dış kaplama işleminin üç işi içerdiğine dikkat edin: bir işlem işi, bir nakliye işi ve bir kuyruk işi.</span><span class="sxs-lookup"><span data-stu-id="f3565-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gannt şeması üzerindeki Gannt şeması - Kaynak görüntüleme sayfası](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="f3565-220">**Tüm üretim emirleri** sayfasına dönmek için **Gannt şeması - Kaynak görünümü** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="f3565-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="f3565-221">Eylem bölmesinde, **Üretim emri** sekmesinde, **Serbest bırak** iletişim kutusunu açmak için **Serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Serbest bırak iletişim kutusu](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="f3565-223">**Serbest bırak** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="f3565-224">**Üretim denetimi \> Periyodik görevler \> Ambara serbest bırak \> Ürün reçetesi ve formül satırlarının otomatik serbest bırakılması**'nı, **Ürün reçetesi ve formül satırlarının otomatik serbest bırakılması** iletişim kutusunu açmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Ürün reçetesi ve formül satırlarını otomatik serbest bırakma iletişim kutusu](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="f3565-226">Ürün reçetesi ve formül satırlarının otomatik serbest bırakılması işini çalıştırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="f3565-227">Bu iş, ambardaki hammaddelerin çekilmesi işini serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="f3565-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="f3565-228">**Tüm üretim emirleri** sayfasını açmak için **Üretim kontrolü \> Üretim emirleri \> Tüm üretim emirlerini**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="f3565-229">Üzerinde çalışmakta olduğunu üretim emrini seçmek için hızlı filtreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3565-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="f3565-230">Eylem Bölmesi üzerinde **Ambar** sekmesinde, **İş** sayfasını açmak için **İş ayrıntıları**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="f3565-231">Sayfanın, hammadde seçmek için iki iş gösterdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f3565-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="f3565-232">İlk iş, malzemeler M8100 ve M8101 için.</span><span class="sxs-lookup"><span data-stu-id="f3565-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="f3565-233">Bu malzemeler, operasyon 10 tarafından tüketilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="f3565-234">İkinci iş, malzemeler M8202 ve M8250 için.</span><span class="sxs-lookup"><span data-stu-id="f3565-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="f3565-235">Bu malzemeler, alt sözleşmeli bir operasyon olan operasyon 20 tarafından tüketilir.</span><span class="sxs-lookup"><span data-stu-id="f3565-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![İş sayfasında hammadde seçimi için iki iş kümesi](./media/subcontract22_work-page.png)

26. <span data-ttu-id="f3565-237">Operasyon 10 için ambar işini işlemek için ambar uygulamasını başlatın.</span><span class="sxs-lookup"><span data-stu-id="f3565-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="f3565-238">**Tüm üretim emirleri** sayfasını açmak için **Üretim kontrolü \> Üretim emirleri \> Tüm üretim emirlerini**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="f3565-239">Üzerinde çalışmakta olduğunu üretim emrini seçmek için hızlı filtreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3565-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="f3565-240">Eylem bölmesinde, **Üretim emri** sekmesinde, **Başlat** iletişim kutusunu açmak için **Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="f3565-241">**Genel** sekmesinde, aşağıdaki değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="f3565-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="f3565-242">**Operasyon Numarası**'da</span><span class="sxs-lookup"><span data-stu-id="f3565-242">In the **From Oper. No.**</span></span> <span data-ttu-id="f3565-243">alan, seçin **10**.</span><span class="sxs-lookup"><span data-stu-id="f3565-243">field, select **10**.</span></span>
    - <span data-ttu-id="f3565-244">**Operasyon Numarası'na** içerisinde</span><span class="sxs-lookup"><span data-stu-id="f3565-244">In the **To Oper. No.**</span></span> <span data-ttu-id="f3565-245">alan, seçin **10**.</span><span class="sxs-lookup"><span data-stu-id="f3565-245">field, select **10**.</span></span>

    ![Genel sekmesinde ayarlanan değerler](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="f3565-247">**Tamam**'ı seçin, kapatmak için **Başlat** iletişim kutusunu ve **Tüm üretim emirleri** sayfasına dönmek için.</span><span class="sxs-lookup"><span data-stu-id="f3565-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="f3565-248">Üretim emrinin durumunun şimdi **Başlatıldı** olduğunu göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="f3565-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="f3565-249">Operasyon 10 için malzemeler, malzeme çekme listesi günlüğüne otomatik nakledilmesi tarafından tüketilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f3565-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="f3565-250">Operasyon 10 için zaman tüketimi, bir rota kartı günlüğünün otomatik nakli ile hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="f3565-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="f3565-251">Operasyon 20 için ambar işini işlemek için ambar uygulamasını başlatın.</span><span class="sxs-lookup"><span data-stu-id="f3565-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="f3565-252">Eylem bölmesinde, **Üretim emri** sekmesinde, **Başlat** iletişim kutusunu açmak için **Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="f3565-253">**Genel** sekmesinde, aşağıdaki değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="f3565-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="f3565-254">**Operasyon Numarası**'da</span><span class="sxs-lookup"><span data-stu-id="f3565-254">In the **From Oper. No.**</span></span> <span data-ttu-id="f3565-255">alan, seçin **20**.</span><span class="sxs-lookup"><span data-stu-id="f3565-255">field, select **20**.</span></span>
    - <span data-ttu-id="f3565-256">**Operasyon Numarası'na** içerisinde</span><span class="sxs-lookup"><span data-stu-id="f3565-256">In the **To Oper. No.**</span></span> <span data-ttu-id="f3565-257">alan, seçin **20**.</span><span class="sxs-lookup"><span data-stu-id="f3565-257">field, select **20**.</span></span>
    - <span data-ttu-id="f3565-258">**Miktar** alanına **10** yazın.</span><span class="sxs-lookup"><span data-stu-id="f3565-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="f3565-259">**Malzeme çekme listesi** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f3565-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Genel sekmesinde ayarlanan değerler](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="f3565-261">**Tamam**'ı seçin, kapatmak için **Başlat** iletişim kutusunu ve **Tüm üretim emirleri** sayfasına dönmek için.</span><span class="sxs-lookup"><span data-stu-id="f3565-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="f3565-262">Bir malzeme çekme listesi, Kaplama operasyonunda kullanılan malzemeler ve servis maddesi için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="f3565-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="f3565-263">Servis maddesi, alt taşeron verilen operasyonun maliyetini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f3565-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="f3565-264">Eylem Bölmesinde, **Görüntüle** sekmesinde, **Malzeme çekme listesi**'ni açmak için **Malzeme çekme listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="f3565-265">Deftere nakledilmemiş olan malzeme çekme listesini seçin, daha sonra günlük satırlarını görmek için günlük numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Malzeme çekme listesi sayfasındaki günlük satırları](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="f3565-267">Eylem bölmesinde **Yazdır** \> **Malzeme çekme listesi**'ni seçin ve **Malzeme çekme listesi raporu** iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="f3565-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="f3565-268">**Teslimat notu düzenini kullanın** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f3565-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Malzeme çekme listesi raporu iletişim kutusu](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="f3565-270">**Tamam**'ı seçerek bir **Malzeme çekme listesi** raporu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f3565-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="f3565-271">Bu durumda bir satıcı teslimat notu üretim malzeme çekme listesi günlüğünden yazdırılır.</span><span class="sxs-lookup"><span data-stu-id="f3565-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="f3565-272">Teslimat notu, Kaplama operasonunu gerçekleştirecek satıcıya gönderilecek malzemeleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3565-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Malzeme çekme listesi raporu](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="f3565-274">**Malzeme çekme listesi** sayfasına dönmek için **Malzeme çekme listesi**'ni kapatın.</span><span class="sxs-lookup"><span data-stu-id="f3565-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="f3565-275">Eylem Bölmesinde, **Günlüğü deftere naklet** iletişim kutusunu açmak için **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Günlüğü deftere naklet iletişim kutusu](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="f3565-277">**Günlüğü deftere naklet** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="f3565-278">Satınalma siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="f3565-278">Open the purchase order.</span></span>

    ![Satınalma siparişi sayfası](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="f3565-280">Eylem Bölmesinde, **Satınal** sekmesinde, **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="f3565-281">**Günlüğü deftere naklet** iletişim kutusunu açmak için **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3565-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="f3565-282">**Tamam**'ı seçin, kapatmak için **Günlüğü deftere naklet** iletişim kutusunu ve **Satınalma siparişi** sayfasına dönmek için.</span><span class="sxs-lookup"><span data-stu-id="f3565-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="f3565-283">Birim fiyatı **33**'ten **40**'a değiştirin.</span><span class="sxs-lookup"><span data-stu-id="f3565-283">Change the unit price from **33** to **40**.</span></span>

    ![Satınalma siparişi sayfasındaki birim fiyatı değiştirildi](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="f3565-285">Satınalma siparişini yeniden doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="f3565-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="f3565-286">Ürün girişi.</span><span class="sxs-lookup"><span data-stu-id="f3565-286">Product receipt.</span></span>

    ![Ürün girişi naklediliyor iletişim kutusu](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="f3565-288">Satınalma faturası.</span><span class="sxs-lookup"><span data-stu-id="f3565-288">Purchase invoice.</span></span>
52. <span data-ttu-id="f3565-289">Eşleştirme durumunu güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="f3565-289">Update the match status.</span></span>

    ![Satıcı fatura sayfası](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="f3565-291">Tamamlandı bildirimi.</span><span class="sxs-lookup"><span data-stu-id="f3565-291">Report as finished.</span></span>

    ![Tamamlanan iletişim kutusu olarak raporlayın](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="f3565-293">Bitiş.</span><span class="sxs-lookup"><span data-stu-id="f3565-293">End.</span></span>

    ![Bitiş iletişim kutusu](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="f3565-295">Maliyet karşılaştırması.</span><span class="sxs-lookup"><span data-stu-id="f3565-295">Cost comparison.</span></span>

    ![Maliyet karşılaştırması grafikleri](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="f3565-297">Kurulumda veri eksik.</span><span class="sxs-lookup"><span data-stu-id="f3565-297">Missing setup in data.</span></span>

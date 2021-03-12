---
title: Kanala göre otomatik masrafları etkinleştirme ve yapılandırma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta otomatik masrafların kanala göre nasıl etkinleştirileceğini ve yapılandırılacağını açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d37b2b785dd29850dcd02d0905e5872445384990
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993740"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="5c284-103">Kanala göre otomatik masrafları etkinleştirme ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5c284-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="5c284-104">Bu konu, Microsoft Dynamics 365 Commerce'ta otomatik masrafların (oto masraflar) kanala göre nasıl etkinleştirileceğini ve yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5c284-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c284-105">Özet</span><span class="sxs-lookup"><span data-stu-id="5c284-105">Overview</span></span>

<span data-ttu-id="5c284-106">Belirli bir eyaletteki tüm veya bazı mağazalarda satılan bir ürün grubuna geri dönüşüm ücretleri veya başka ücretlerin uygulanması gereken senaryolarınız olabilir (örneğin, California).</span><span class="sxs-lookup"><span data-stu-id="5c284-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="5c284-107">Commerce'taki **Kanala göre otomatik masrafları filtrelemeyi etkinleştirme** özelliği, kanala göre otomatik masrafları belirtmenize olanak sağlar (örneğin, belirli bir fiziksel mağaza kanalı).</span><span class="sxs-lookup"><span data-stu-id="5c284-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="5c284-108">Bu özellik Dynamics 365 Commerce 10.0.10 sürümü ve sonrasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="5c284-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="5c284-109">Otomatik masrafları kanal bazında etkinleştirmek ve yapılandırmak için aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5c284-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="5c284-110">**Kanal bazında otomatik masrafları filtrelemeyi etkinleştir** özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="5c284-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="5c284-111">Kuruluş hiyerarşisi amacını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5c284-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="5c284-112">Kanala göre otomatik masrafları tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="5c284-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="5c284-113">**Kanala göre otomatik masrafları filtrelemeyi etkinleştirme** özelliği yalnızca gelişmiş otomatik masraflar özelliği açıksa çalışır.</span><span class="sxs-lookup"><span data-stu-id="5c284-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="5c284-114">Gelişmiş otomatik masrafları özelliğini etkinleştirme hakkında bilgi için bkz. [Çok yönlü kanal gelişmiş otomatik masrafları](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="5c284-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="5c284-115">Kanala göre otomatik masrafları filtrelemeyi etkinleştir özelliğini açın</span><span class="sxs-lookup"><span data-stu-id="5c284-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="5c284-116">Otomatik masrafları Commerce'ta kanala göre etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c284-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5c284-117">**Sistem Yönetimi \> Çalışma alanları \> Özellik yönetimi** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="5c284-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="5c284-118">**Etkin değil** sekmesinde **Özellik adı** listesinde, **Kanala göre otomatik masraf filtrelemeyi etkinleştir**'i bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="5c284-119">Sağ alt köşede, **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="5c284-120">Özellik etkinleştirildikten sonra, **Tümü** sekmesindeki listede görünür.</span><span class="sxs-lookup"><span data-stu-id="5c284-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="5c284-121">**Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5c284-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5c284-122">Sol bölmede **1110** (**Global yapılandırma**) işini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="5c284-123">Eylem Bölmesinde, yapılandırma değişikliklerini yaymak için **Şimdi çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="5c284-124">Daha önce kullandıktan sonra **Kanala göre otomatik masraf filtrelemeyi etkinleştir** özelliğini kapatırsanız, **Otomatik masraflar** altındaki **Perakende kanalı ilişkisi** artık görünmez ve varolan tüm yapılandırmalarla ilgili değişiklikleri kaybedersiniz.</span><span class="sxs-lookup"><span data-stu-id="5c284-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="5c284-125">**Perakende kanalı ilişkisi** yapılandırmalarının kaldırılması otomatik masraf kurallarının yinelenmesine neden olacaksa, özelliği kapatma girişimi başarısız olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5c284-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="5c284-126">Özelliği kapatmadan önce tüm otomatik masraf kurallarını gözden geçirmeyi ve gerekli değişiklikleri yapmayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5c284-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="5c284-127">Kuruluş hiyerarşisi amacını yapılandırın</span><span class="sxs-lookup"><span data-stu-id="5c284-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="5c284-128">Kanala göre otomatik masraflar için hiyerarşiyi yönetmek **Perakende otomatik masraf** adlı yeni bir kuruluş hiyerarşisi amacı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5c284-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="5c284-129">Commerce'ta bir kuruluş hiyerarşisi amacına varsayılan bir hiyerarşi atamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c284-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="5c284-130">**Kuruluş yönetimi \> Kuruluşlar \> Kuruluş hiyerarşisi amaçları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5c284-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="5c284-131">Sol bölmede, **Perakende otomatik masraf**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="5c284-132">**Atanan hiyerarşiler** altında **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="5c284-133">**Kuruluş hiyerarşileri** iletişim kutusunda bir kuruluş hiyerarşisi seçin (örneğin, **Bölgeye göre Perakende Mağazalar**) ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="5c284-134">**Atanan hiyerarşiler** altında **Varsayılan olarak ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="5c284-135">**Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5c284-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5c284-136">Sol bölmede **1040** (**Ürünler**) işini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="5c284-137">Eylem Bölmesinde **Şimdi çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="5c284-138">**1070** **(Kanal yapılandırması**) ve **1110** (**Genel yapılandırma**) işlerini çalıştırmak için önceki iki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c284-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Perakende otomatik masraf kuruluşu hiyerarşi amacı yapılandırması](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="5c284-140">Kanala göre otomatik masrafları tanımlama</span><span class="sxs-lookup"><span data-stu-id="5c284-140">Define auto charges by channel</span></span>

<span data-ttu-id="5c284-141">**Kanala göre otomatik masraf filtrelemeyi etkinleştir** özelliğini etkinleştirip **Perakende otomatik masraf** kuruluş hiyerarşisi amacını yapılandırdıktan sonra, kanala göre otomatik masraflar, sipariş başlığı düzeyinde veya sipariş satırı düzeyinde tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5c284-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="5c284-142">Otomatik masrafları Commerce'ta kanala göre tanımlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c284-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5c284-143">Sırasıyla **Alacak hesapları \> masraflar kurulumu \> Otomatik masraflar** seçimlerini yapın.</span><span class="sxs-lookup"><span data-stu-id="5c284-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="5c284-144">Sol bölmede, iş gereksinimlerinize bağlı olarak **Düzey** alanında **Başlık** ya da **Satır** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5c284-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="5c284-145">**Perakende kanal kodu** alanında, uygun kanal kodunu seçin (örneğin, **Tablo** veya **Grup**).</span><span class="sxs-lookup"><span data-stu-id="5c284-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="5c284-146">Varsayılan ayar olan **Tümü** kullanılırsa, masraf kuralları tüm kanallara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="5c284-147">**Grup** öğesini seçerseniz, **Retail ve Commerce \> Kanal kurulumu \> Masraflar \> Perakende kanal masraf grupları**'nda bir perakende kanal masraf grubunun oluşturulduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5c284-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="5c284-148">**Tablo** seçeneğini belirlersniz **Perakende kanal ilişkisi** alanında özel bir kanal (örneğin **San Francisco**) seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c284-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="5c284-149">**Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5c284-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="5c284-150">Sol bölmede **1040** (**Ürünler**) işini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="5c284-151">Eylem Bölmesinde **Şimdi çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c284-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="5c284-152">**1070** **(Kanal yapılandırması**) ve **1110** (**Genel yapılandırma**) işlerini çalıştırmak için önceki iki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c284-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Kanala göre tanımlanan otomatik masraflar](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="5c284-154">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="5c284-154">Example scenario</span></span>

<span data-ttu-id="5c284-155">Aşağıdaki örnekte, bir ürünü, ürün San Franscisco'daki bir fiziksel mağaza kanalı aracılığıyla satıldığında geri dönüşüm masrafları ücretlendirilecek şekilde, yapılandırmak için gerekli olan adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5c284-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="5c284-156">Bu örnek ayrıca otomatik masrafların Commerce satış noktası (POS) uygulamasında nasıl göründüğünü de gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c284-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="5c284-157">Kuruluş, aşağıdaki çizimde gösterildiği gibi, **GERİ DÖNÜŞÜM** olarak adlandırılan bir masraf kodu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="5c284-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![GERİ DÖNÜŞÜM masraf kodu](media/Auto-charges-charge-code.png)

<span data-ttu-id="5c284-159">Satır düzeyinde otomatik masraf oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5c284-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="5c284-160">Aşağıdaki yapılandırmaya sahiptir:</span><span class="sxs-lookup"><span data-stu-id="5c284-160">It has the following configuration:</span></span>

- <span data-ttu-id="5c284-161">**Hesap kodu** alanı **Tümü** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="5c284-162">**Madde kodu** alanı **Tablo** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="5c284-163">**Madde ilişkisi** alanı ürün kodu **91001** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="5c284-164">**Teslimat modu kodu** alanı **Tümü** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="5c284-165">**Perakende kanalı kodu** alanı **Tablo** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="5c284-166">**Perakende kanalı ilişki** alanı **San Francisco**  mağazası olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="5c284-167">Otomatik masraf satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5c284-167">An auto charges line is created.</span></span> <span data-ttu-id="5c284-168">Aşağıdaki yapılandırmaya sahiptir:</span><span class="sxs-lookup"><span data-stu-id="5c284-168">It has the following configuration:</span></span>

- <span data-ttu-id="5c284-169">**Para birimi** alanı **USD** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="5c284-170">**Masraf kodu** alanı **GERİ DÖNÜŞÜM** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="5c284-171">**Kategori** alanı **Sabit** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="5c284-172">**Masraf** alanı **6,25 $** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c284-172">The **Charges** field is set to **$6.25**.</span></span>

![Satır düzeyi otomatik masraf ve otomatik masraflar satırı yapılandırması](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="5c284-174">POS uygulamasında **San Francisco** mağaza kanalında bir satış siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5c284-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="5c284-175">**Masraflar** satırı, **6,25 $** tutarındaki geri dönüşüm ücretini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c284-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="5c284-176">POS uygulamasında **Hareket seçenekleri \> Masraflar \> Masrafları yönet**'i seçerek geri dönüşüm masrafına ait masraf kodunu ve açıklamayı görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c284-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![POS uygulamasındaki geri dönüşüm ücreti](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="5c284-178">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5c284-178">Additional resources</span></span>

[<span data-ttu-id="5c284-179">Çok yönlü kanal gelişmiş otomatik masrafları</span><span class="sxs-lookup"><span data-stu-id="5c284-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="5c284-180">Başlık masraflarını eşleşen satış satırlarına eşit dağıtma</span><span class="sxs-lookup"><span data-stu-id="5c284-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)

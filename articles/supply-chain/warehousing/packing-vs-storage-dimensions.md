---
title: Paketleme ve depolama için farklı boyutlar ayarlama
description: Bu konuda, belirtilen her boyutun kullanıldığı işlemin (paketleme, depolama veya iç içe paketleme) nasıl belirtileceğini gösterir.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: aa5cbf807e809238489c539d3ad8c0bc34421774
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501306"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="1a975-103">Paketleme ve depolama için farklı boyutlar ayarlama</span><span class="sxs-lookup"><span data-stu-id="1a975-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1a975-104">Bazı maddeler, birçok farklı işlemin her biri için fiziksel boyutları farklı izlemeniz gerekebilecek şekilde paketlenebilir veya depolanır.</span><span class="sxs-lookup"><span data-stu-id="1a975-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="1a975-105">*Ürün paketleme boyutları* özelliği, her ürün için bir veya daha fazla boyut türü ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1a975-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="1a975-106">Her boyut türü, bir dizi fiziksel ölçü (ağırlık, genişlik, derinlik ve yükseklik) sağlar ve bu fiziksel ölçüm değerlerinin geçerli olduğu işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a975-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="1a975-107">Bu özellik etkinleştirildiğinde, sisteminiz aşağıdaki boyut türlerini desteklecektir:</span><span class="sxs-lookup"><span data-stu-id="1a975-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="1a975-108">*Depolama*: Depolama boyutları, her maddeden çeşitli ambar yerleşimlerinde kaç tane depolanabileceğini belirlemek için yerleşim hacimleriyle birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a975-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="1a975-109">*Paketleme*: Paketleme boyutları konteyner kullanımı ve el ile paketleme işlemi sırasında çeşitli konteyner türlerine her bir maddeden kaç tane sığacağını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a975-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="1a975-110">*İç içe paketleme*: İç içe paketleme boyutları, paketleme işleminin birden fazla düzey içerdiği durumlarda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a975-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="1a975-111">*Depolama* boyutları, *Ürün paketleme boyutları* özelliği etkinleştirilmediğinde bile desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1a975-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="1a975-112">Bunları, Supply Chain Management'ta **Fiziksel boyut** sayfasını kullanarak ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="1a975-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="1a975-113">Bu boyutlar, paketleme ve iç içe paketleme boyutlarının belirtilmediği tüm işlemler tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a975-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="1a975-114">*Paketleme* ve *iç içe paketleme* boyutları, *Ürün paketleme boyutları* özelliğini etkinleştirdiğinizden eklenen **Fiziksel ürün boyutları** sayfasını kullanarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1a975-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="1a975-115">Bu konu, bu özelliğin nasıl kullanılacağını açıklayan bir senaryo içermektedir.</span><span class="sxs-lookup"><span data-stu-id="1a975-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="1a975-116">Ürün paketleme boyutları özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1a975-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="1a975-117">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a975-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1a975-118">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1a975-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1a975-119">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="1a975-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1a975-120">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="1a975-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1a975-121">**Özellik adı:** *Ürün paketleme boyutları*</span><span class="sxs-lookup"><span data-stu-id="1a975-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1a975-122">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="1a975-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="1a975-123">Senaryoyu ayarlama</span><span class="sxs-lookup"><span data-stu-id="1a975-123">Set up the scenario</span></span>

<span data-ttu-id="1a975-124">Örnek senaryoyu çalıştırabilmeniz için, sisteminizi bu bölümde anlatıldığı şekilde hazırlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a975-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="1a975-125">Tanıtım verilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1a975-125">Enable demo data</span></span>

<span data-ttu-id="1a975-126">Burada belirtilen tanıtım kayıtlarını ve değerlerini kullanarak bu senaryo üzerinde çalışmak için standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a975-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="1a975-127">Ek olarak, başlamadan önce *USMF* tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a975-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="1a975-128">Ürüne yeni fiziksel boyut ekleme</span><span class="sxs-lookup"><span data-stu-id="1a975-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="1a975-129">Aşağıdakileri yaparak, bir ürün için yeni bir fiziksel boyut ekleyin:</span><span class="sxs-lookup"><span data-stu-id="1a975-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="1a975-130">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1a975-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1a975-131">**Madde numarası** *A0001* olan bir ürün seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="1a975-132">Eylem Bölmesinde, **Stok yönet** sekmesini açın ve **Ambar** grubundan **Fiziksel ürün boyutları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="1a975-133">**Fiziksel ürün boyutları** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="1a975-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="1a975-134">Izgaraya aşağıdaki ayarlara sahip yeni bir boyut eklemek için Eylem Bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="1a975-135">**Fiziksel boyut türü** - *Paketleme*</span><span class="sxs-lookup"><span data-stu-id="1a975-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="1a975-136">**Fiziksel birim** - *adet*</span><span class="sxs-lookup"><span data-stu-id="1a975-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="1a975-137">**Ağırlık** - *4*</span><span class="sxs-lookup"><span data-stu-id="1a975-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="1a975-138">**Ağırlık birimi** - *kg*</span><span class="sxs-lookup"><span data-stu-id="1a975-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="1a975-139">**Derinlik** - *3*</span><span class="sxs-lookup"><span data-stu-id="1a975-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="1a975-140">**Yükseklik** - *4*</span><span class="sxs-lookup"><span data-stu-id="1a975-140">**Height** - *4*</span></span>
    - <span data-ttu-id="1a975-141">**Genişlik** - *3*</span><span class="sxs-lookup"><span data-stu-id="1a975-141">**Width** - *3*</span></span>
    - <span data-ttu-id="1a975-142">**Uzunluk** - *cm*</span><span class="sxs-lookup"><span data-stu-id="1a975-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="1a975-143">**Hacim birimi** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="1a975-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="1a975-144">**Hacim** alanı; **Derinlik**, **Yükseklik** ve **Genişlik** ayarlarınıza göre otomatik olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="1a975-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="1a975-145">Yeni konteyner türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a975-145">Create a new container type</span></span>

<span data-ttu-id="1a975-146">**Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner türleri**'ne gidin ve aşağıdaki ayarlarla yeni bir kayıt oluşturun:</span><span class="sxs-lookup"><span data-stu-id="1a975-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="1a975-147">**Konteyner türü kodu** - *Kısa Kutu*</span><span class="sxs-lookup"><span data-stu-id="1a975-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="1a975-148">**Açıklama** - *Kısa Kutu*</span><span class="sxs-lookup"><span data-stu-id="1a975-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="1a975-149">**Maksimum net ağırlık** - *50*</span><span class="sxs-lookup"><span data-stu-id="1a975-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="1a975-150">**Hacim** - *144*</span><span class="sxs-lookup"><span data-stu-id="1a975-150">**Volume** - *144*</span></span>
- <span data-ttu-id="1a975-151">**Uzunluk** - *6*</span><span class="sxs-lookup"><span data-stu-id="1a975-151">**Length** - *6*</span></span>
- <span data-ttu-id="1a975-152">**Genişlik** - *6*</span><span class="sxs-lookup"><span data-stu-id="1a975-152">**Width** - *6*</span></span>
- <span data-ttu-id="1a975-153">**Yükseklik** - *4*</span><span class="sxs-lookup"><span data-stu-id="1a975-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="1a975-154">Konteyner grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a975-154">Create a container group</span></span>

<span data-ttu-id="1a975-155">**Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner grupları**'na gidin ve aşağıdaki ayarlarla yeni bir kayıt oluşturun:</span><span class="sxs-lookup"><span data-stu-id="1a975-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="1a975-156">**Konteyner grubu kodu** - *Kısa Kutu*</span><span class="sxs-lookup"><span data-stu-id="1a975-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="1a975-157">**Açıklama** - *Kısa Kutu*</span><span class="sxs-lookup"><span data-stu-id="1a975-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="1a975-158">**Ayrıntılar** bölümüne yeni bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1a975-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="1a975-159">**Konteyner türü**'nü *Kısa Kutu* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1a975-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="1a975-160">Bir konteyner yapılandırma şablonu</span><span class="sxs-lookup"><span data-stu-id="1a975-160">Set up a container build template</span></span>

<span data-ttu-id="1a975-161">**Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner yapı şablonları**'na gidin ve **Kutular**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="1a975-162">**Konteyner grubu kodu**'nu *Kısa Kutu* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="1a975-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="1a975-163">Senaryoyu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="1a975-163">Run the scenario</span></span>

<span data-ttu-id="1a975-164">Sisteminizi önceki bölümde anlatıldığı gibi hazırladıktan sonra, senaryoyu sonraki bölümde anlatıldığı gibi çalıştırmaya hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="1a975-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="1a975-165">Satış siparişi oluşturma ve sevkiyat oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a975-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="1a975-166">Bu işlemde, yüksekliği 3'ten az olan madde *paketleme* boyutlarına göre bir sevkiyat oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="1a975-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="1a975-167">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1a975-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1a975-168">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1a975-169">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="1a975-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1a975-170">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="1a975-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="1a975-171">**Ambar:** *63*</span><span class="sxs-lookup"><span data-stu-id="1a975-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="1a975-172">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="1a975-173">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="1a975-173">The new sales order is opened.</span></span> <span data-ttu-id="1a975-174">**Satış siparişi satırları** hızlı sekmesi 'ndeki kılavuza yeni, boş bir satır dahil etmelidir.</span><span class="sxs-lookup"><span data-stu-id="1a975-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1a975-175">Bu satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="1a975-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="1a975-176">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1a975-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1a975-177">**Miktar:** *5*</span><span class="sxs-lookup"><span data-stu-id="1a975-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="1a975-178">**Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="1a975-179">**Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="1a975-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1a975-180">Close the page.</span></span>
1. <span data-ttu-id="1a975-181">Eylem bölmesindeki **Ambar** sekmesini açın ve **Ambara serbest bırak**'ı seçerek ambar için iş oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1a975-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="1a975-182">**Satış siparişi satırları** hızlı sekmesinde **Ambar \> Sevkiyat ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="1a975-183">Eylem Bölmesinde, **Taşıma** sekmesini açın ve **Konteynerleri görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="1a975-184">Maddenin, iki *Kısa Kutu* konteyneriyle konteynerlere yerleştirildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="1a975-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="1a975-185">Maddeyi depoya yerleştirme</span><span class="sxs-lookup"><span data-stu-id="1a975-185">Place an item into storage</span></span>

1. <span data-ttu-id="1a975-186">Mobil cihazı açın, ambar 63'te oturum açın ve **Stok \> Ayarla**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="1a975-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="1a975-187">**Loc** = *SHORT-01* ifadesini girin.</span><span class="sxs-lookup"><span data-stu-id="1a975-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="1a975-188">**Madde** = *A0001* ve **Miktar** = *1 adet* olacak şekilde yeni bir lisans plakası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1a975-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="1a975-189">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a975-189">Select **OK**.</span></span> <span data-ttu-id="1a975-190">"Madde A0001 yerleşimin belirtilen boyutlarına sığmadığından SHORT-01 yerleşimi başarısız oldu." hatasını alırsınız.</span><span class="sxs-lookup"><span data-stu-id="1a975-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="1a975-191">Bunun nedeni, ürünün *Depolama* türü boyutlarının yerleşim profilinde belirtilen boyutlardan daha büyük olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="1a975-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
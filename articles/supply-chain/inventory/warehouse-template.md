---
title: "Ambar yapılandırma şablonu kullanarak bir ambarı ayarlama"
description: "Bu konu ambar yapılandırma şablonu kullanarak bir ambarın nasıl ayarlanacağını açıklamaktadır."
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0b54e7f6f4b0dfb994d271aaeb547e27bf03e294
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="e7cea-103">Ambar yapılandırma şablonu kullanarak bir ambarı ayarlama</span><span class="sxs-lookup"><span data-stu-id="e7cea-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7cea-104">Bu konu ambar yapılandırma şablonu kullanarak bir ambarın nasıl ayarlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e7cea-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="e7cea-105">Kullanabileceğiniz çeşitli önceden tanımlanmış yapılandırma şablonları bulunur.</span><span class="sxs-lookup"><span data-stu-id="e7cea-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="e7cea-106">Bu şablonların nasıl kullanılacağı hakkında bilgi için bkz. [Yapılandırma veri şablonları](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="e7cea-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="e7cea-107">Yapılandırma şablonlarının yardımcı olabileceği senaryolar</span><span class="sxs-lookup"><span data-stu-id="e7cea-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="e7cea-108">Yapılandırma şablonları bir çok senaryoda yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="e7cea-109">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="e7cea-109">Here are some examples:</span></span>

- <span data-ttu-id="e7cea-110">Test ortamında bir yapılandırma ayarını tamamlayıp test ettiniz ve şimdi ayarı üretim ortamına kopyalamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="e7cea-111">Ambar ayarını çeşitli tüzel kişiliklere yaymak veya aynı tüzel kişilikte yeni bir ambar oluşturmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="e7cea-112">Ambar işlevi için hızlı bir şekilde bir demo hazırlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="e7cea-113">Mevcut maddelerin ve depoların Stok yönetimi yerine Ambar yönetimindeki işlevi kullanmasını istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="e7cea-114">Bu konu bu senaryoların ilkine odaklanır.</span><span class="sxs-lookup"><span data-stu-id="e7cea-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="e7cea-115">Bir yapılandırma ayarını test ortamından üretim ortamına kopyalamak için bir yapılandırma şablonunu nasıl kullanabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="e7cea-116">Bir yapılandırma ayarını test ortamından üretim ortamına kopyalama</span><span class="sxs-lookup"><span data-stu-id="e7cea-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="e7cea-117">Bu senaryoda, ambar yapılandırma ayarı ve bazı hareket süreçleri zaten test ortamında bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e7cea-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="e7cea-118">Şimdi ambar yapılandırma ayarını test ortamından üretim ortamına kopyalamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="e7cea-119">Bir yapılandırma ayarını kopyalarken diğer ilgili ayar verilerini de eklemeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="e7cea-120">Örneğin, ayarı test ortamından kopyalayarak ürünler ayarlamak istediğinizi varsayalım.</span><span class="sxs-lookup"><span data-stu-id="e7cea-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="e7cea-121">Bununla birlikte, ürün oluşturulmadan önce ürün için sabit çekme konumu ayarlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="e7cea-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="e7cea-122">Tek tek yapılandırma şablonları bu tür bir bağımlılığı desteklememesine karşın, bunu destekleyen varsayılan veri şablonları bulunur.</span><span class="sxs-lookup"><span data-stu-id="e7cea-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="e7cea-123">Bu varsayılan veri şablonlarını yapılandırma sürecine kolaylıkla dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="e7cea-124">Varsayılan ambar şablonunu dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="e7cea-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="e7cea-125">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="e7cea-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7cea-126">Bu çalışma alanını ilk kez kullanıyorsanız, devam etmeden önce tüm veri varlıklarını yüklemeniz gerekir</span><span class="sxs-lookup"><span data-stu-id="e7cea-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="e7cea-127">**Şablonlar** kutusunu seçin ve varsayılan şablonları yüklemek için **Varsayılan şablonları yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e7cea-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7cea-128">**Varsayılan şablonları yükle** yalnızca **Gelişmiş** görünümde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="e7cea-129">**Çerçeve parametreleri**'ni ve daha sonra **Varsayılanları görüntüle** alanında **Gelişmiş görünümü** seçin.</span><span class="sxs-lookup"><span data-stu-id="e7cea-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="e7cea-130">Varsayılan şablonlar yüklendikten sonra, iş gereksinimlerinizi karşılayacak şekilde bunları değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7cea-131">Varsayılan şablonları yüklemek ve şablonları içe aktarmak için sistem yöneticisi erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e7cea-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="e7cea-132">Bu gereksinim tüm varlıkların şablona doğru şekilde yüklenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e7cea-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="e7cea-133">Şirkete özel verileri dışa aktarmak istediğiniz tüzel kişilikte olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e7cea-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="e7cea-134">Çalışma alanında **Dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7cea-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="e7cea-135">Yeni bir dışa aktarma projesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7cea-135">Create a new export project.</span></span>
7. <span data-ttu-id="e7cea-136">**+ Şablon ekle**'yi seçin ve **400 - WMS** varsayılan ambar şablonunu bulun.</span><span class="sxs-lookup"><span data-stu-id="e7cea-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="e7cea-137">Bu şablon ambar yapılandırması için veri varlıkları ekler.</span><span class="sxs-lookup"><span data-stu-id="e7cea-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7cea-138">Dışa aktardığınız verilerin filtrelenmesi gerekirse (örneğin, yalnızca belirli bir ambarla ilgili verileri dışa aktarma istiyorsanız), her veri varlığını değerlendirmeniz ve sorgu aracılığıyla filtre eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="e7cea-139">Alternatif olarak, tüm verileri dışa aktarabilir ve ardından hedef dosyalarda istenmeyen kayıtları silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="e7cea-140">**Dışa Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7cea-140">Select **Export**.</span></span> <span data-ttu-id="e7cea-141">Projedeki tüm veri varlıklarıyla ilişkili veriler dışa aktarılır.</span><span class="sxs-lookup"><span data-stu-id="e7cea-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="e7cea-142">Veri paketi için bir zip dosyası indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="e7cea-143">Bu dosya tüm verileri seçilen biçimde (örneğin, Excel biçiminde) içerir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="e7cea-144">Belirtildiği gibi veri paketi dosyalarındaki bazı kayıtların bunları üretim ortamına aktarmadan önce güncelleştirilmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="e7cea-145">Bir kaydı güncelleştirirseniz, dosya adını değiştirmediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="e7cea-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="e7cea-146">Bir ambar yapılandırması ayarını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="e7cea-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="e7cea-147">Hedef ortamda, ambar verilerini içe aktarmak istediğiniz şirkette olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e7cea-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7cea-148">İçe aktarma işlemini yapmadan önce tüm veri bağımlılıklarını tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="e7cea-149">Örneğin, **Ambar yönetimi** şablonu **Ambar değerlendirme kodları** adında bir veri varlığı içerir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="e7cea-150">Bu varlık, **Değerlendirme kodları** ayar sayfasıyla ilişkili verileri içerir (**Ambar yönetimi** > **Kurulum** > **Mobil cihaz** > **Değerlendirme kodları**).</span><span class="sxs-lookup"><span data-stu-id="e7cea-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="e7cea-151">Mevcut bir ayar satış siparişleri için iade sürecini zaten işliyorsa, **İade değerlendirme kodu** alanında bir değer bulunur.</span><span class="sxs-lookup"><span data-stu-id="e7cea-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="e7cea-152">Bu alandaki değerlendirme kodu **Satış ve pazarlama** şablonunun bir parçası olan **Değerlendirme kodu** veri varlığıyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="e7cea-153">**Değerlendirme kodu** veri varlığındaki veriler **Ambar değerlendirme kodları** alanındaki verilerden önce içe aktarılmazsa, içe aktarma işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="e7cea-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="e7cea-154">**Veri yönetimi** çalışma alanında **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7cea-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="e7cea-155">Yeni bir içe aktarma projesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7cea-155">Create a new import project.</span></span>
4. <span data-ttu-id="e7cea-156">**+ Dosya ekle**'yi seçin ve veri paketi zip dosyasını yükleyin.</span><span class="sxs-lookup"><span data-stu-id="e7cea-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="e7cea-157">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7cea-157">Select **Import**.</span></span> <span data-ttu-id="e7cea-158">**Gelişmiş** görünümde, içe aktarma sırasında oluşabilecek sorunların genel bir görünümünü almak için **Filtre** seçeneğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="e7cea-159">**Yürütmeyi görüntüle** günlüğü içe aktarılan her veri varlığıyla ilgili ayrıntılı bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7cea-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="e7cea-160">Hedef verilere hızlıca gitmek için aşamalandırma verisi görünümünü kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="e7cea-161">Bu şekilde, uygulamadaki ilgili sayfalarda içe aktarılan verilen nasıl göründüğünü görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7cea-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="e7cea-162">Varsayılan veri şablonlarını kullandığınızda, her veri varlığı için içe aktarma sırası önceden tanımlanan şekilde çalışarak tüm bağımlı verilerin önce içe aktarılmasını sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e7cea-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="e7cea-163">Özel veri varlıkları projesinin bir parçasıysa, doğru sıranın tanımlandığından emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e7cea-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="e7cea-164">Daha fazla bilgi için bkz. [Yapılandırma veri şablonları](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="e7cea-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

<span data-ttu-id="e7cea-165">Ambarın yapılandırmasını bir şirketten yeni bir şirkete aynı örnek içinde kopyalamak için ambar şablonu kullanma hakkında daha fazla bilgi edinmek için YouTube'daki bu 3 dakikalık videoyu izleyin.</span><span class="sxs-lookup"><span data-stu-id="e7cea-165">To learn more about how to use warehouse template to copy the configuration of a warehouse from one company to a new company within the same instance, see this 3-minute video on YouTube.</span></span>

> [!Video https://www.youtube.com/embed/K2WIfFlqJYs]


## <a name="related-topic"></a><span data-ttu-id="e7cea-166">İlgili konu</span><span class="sxs-lookup"><span data-stu-id="e7cea-166">Related topic</span></span>

[<span data-ttu-id="e7cea-167">Konfigürasyon verisi şablonları</span><span class="sxs-lookup"><span data-stu-id="e7cea-167">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)


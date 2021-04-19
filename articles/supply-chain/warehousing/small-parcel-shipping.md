---
title: Küçük paket sevkiyatı
description: Bu konuda, küçük paket sevkiyatı (SPS) özelliğiyle ilgili bilgiler verilir. Bu özellik, paketlenmiş konteyner hakkındaki ayrıntıların taşıyıcıya gönderilmesi ve ardından söz konusu taşıyıcıdan gönderim etiketi, sevkiyat ücreti ve izleme numarası almak için Microsoft Dynamics 365 Supply Chain Management'ı etkinleştirmeyi sağlar.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3969ee6b46f38fe2650881fb0183c60aadce6c8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831182"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="36545-104">Küçük paket sevkiyatı</span><span class="sxs-lookup"><span data-stu-id="36545-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36545-105">Küçük paket sevkiyatı (SPS) özelliği, taşıyıcı API'leri aracılığıyla iletişim için bir çerçeve sağlayarak sevkiyat taşıyıcılarıyla doğrudan etkileşim için Microsoft Dynamics 365 Supply Chain Management'ı etkinleştirmeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="36545-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="36545-106">Bu işlev, bağımsız satış siparişlerini konteyner sevkiyatı veya kamyon yükünden az (LTL) sevkiyatı kullanmak yerine ticari sevkiyat taşıyıcıları aracılığıyla gönderdiğiniz durumlar için faydalıdır.</span><span class="sxs-lookup"><span data-stu-id="36545-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="36545-107">SPS özelliği, sevkiyat taşıyıcınızla özel bir *değerlendirme altyapısı* aracılığıyla etkileşim kurar.</span><span class="sxs-lookup"><span data-stu-id="36545-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="36545-108">Kuruluşunuzun bu değerlendirme altyapısını taşıyıcınız veya taşıyıcı merkez hizmetiniz ile birlikte çalıştırarak geliştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="36545-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="36545-109">Bu değerlendirme altyapısı, paketlenmiş konteyner hakkındaki ayrıntıların taşıyıcınıza gönderilmesi ve ardından söz konusu taşıyıcıdan gönderim etiketi, sevkiyat ücreti ve izleme numarası almak için Supply Chain Management'ı etkinleştirmeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="36545-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="36545-110">Döndürülen sevkiyat ücreti, ilişkili satış siparişine sair gider olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="36545-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="36545-111">Daha sonra döndürülen gönderim etiketi, Zebra Programlama Dili (ZPL) yazıcısı kullanılarak otomatik olarak yazdırılıp sevkiyata uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="36545-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="36545-112">Taşıyıcı, ambarınızdan paketleri alırken bu gönderim etiketini tarar.</span><span class="sxs-lookup"><span data-stu-id="36545-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="36545-113">Sisteminizi SPS'yi destekleyecek şekilde hazırlama</span><span class="sxs-lookup"><span data-stu-id="36545-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="36545-114">SPS işlevini kullanmaya başlamadan önce, Özellik yönetimi'nde SPS özelliğini açmanız, değerlendirme altyapınızı eklemeniz ve bunu desteklemek için **Taşıma yönetimi** ve **Ambar yönetimi** modüllerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="36545-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="36545-115">SPS özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="36545-115">Turn on the SPS feature</span></span>

<span data-ttu-id="36545-116">SPS özelliğini kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36545-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="36545-117">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="36545-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="36545-118">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="36545-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="36545-119">**Modül:** *Taşıma yönetimi*</span><span class="sxs-lookup"><span data-stu-id="36545-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="36545-120">**Özellik adı:** *Küçük paket sevkiyatı*</span><span class="sxs-lookup"><span data-stu-id="36545-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="36545-121">Değerlendirme altyapılarını dağıtma ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="36545-122">Supply Chain Management, değerlendirme altyapısı içermez.</span><span class="sxs-lookup"><span data-stu-id="36545-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="36545-123">Gereksinim duyduğunuz değerlendirme altyapılarını edinmeniz veya oluşturmanız ve sonra bunları sisteminize eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36545-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="36545-124">Ancak Microsoft, test etmek için kullanabileceğiniz bir tanıtım değerlendirme altyapısı sunar.</span><span class="sxs-lookup"><span data-stu-id="36545-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="36545-125">Tanıtım amaçlı değerlendirme altyapısını indirme ve dağıtma</span><span class="sxs-lookup"><span data-stu-id="36545-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="36545-126">Tanıtım amaçlı değerlendirme altyapısını edinmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="36545-127">GitHub'da, [tanıtım amaçlı değerlendirme altyapısı için dinamik bağlantı kitaplığı (DLL)](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS) öğesini indirin.</span><span class="sxs-lookup"><span data-stu-id="36545-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="36545-128">Supply Chain Management sunucunuzda DLL'yi  **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** klasörüne kaydedin.</span><span class="sxs-lookup"><span data-stu-id="36545-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="36545-129">İşlevsel değerlendirme altyapıları oluşturma ve dağıtma</span><span class="sxs-lookup"><span data-stu-id="36545-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="36545-130">Üretim veya test ortamında kullanılabilmeleri için işlevsel değerlendirme altyapılarının nasıl oluşturulduğu ve dağıtılacağı hakkında bilgi için, aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="36545-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="36545-131">Yeni bir taşıma yönetimi altyapısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="36545-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="36545-132">Taşıma yönetimi altyapılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-132">Set up transportation management engines</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="36545-133">SPS değerlendirme altyapısı oluşturma hakkında daha fazla bilgi için şu blog gönderisini okuyun: [Küçük Paket Sevkiyatı: Microsoft Dynamics 365'te küçük paket sevkiyatı işlevinden yararlanma](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="36545-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="36545-134">Supply Chain Management'ta değerlendirme altyaspısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="36545-135">SPS için bir değerlendirme altyapısı oluşturup dağıttıktan sonra, bu altyapıyı ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="36545-136">**Taşıma yönetimi \> Kurulum \> Altyapılar \> Değerlendirme altyapısı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="36545-137">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="36545-138">Yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="36545-139">**Değerlendirme altyapısı**: Değerlendirme altyapısı için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="36545-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="36545-140">Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız *Tanıtım amaçlı değerlendirme altyapısı* adını girin.</span><span class="sxs-lookup"><span data-stu-id="36545-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="36545-141">**Ad**: Değerlendirme alt yapısının kısa açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="36545-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="36545-142">Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız *Tanıtım amaçlı değerlendirme altyapısı* adını girin.</span><span class="sxs-lookup"><span data-stu-id="36545-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="36545-143">**Değerlendirme metaverileri kodu**: Ücretinizi hesaplamak için kullanılacak temeli seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="36545-144">Örneğin, ücretiniz mesafe göre hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="36545-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="36545-145">Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız, bu alanı boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36545-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="36545-146">**Altyapı derlemesi**: Dağıttığınız DLL paketinin dosya adını girin.</span><span class="sxs-lookup"><span data-stu-id="36545-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="36545-147">Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız *TMSSmallParcelShippingEngine.dll* adını girin.</span><span class="sxs-lookup"><span data-stu-id="36545-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="36545-148">**Altyapı sınıfı**: Değerlendirme altyapınız için belirlenen sınıf adını girin.</span><span class="sxs-lookup"><span data-stu-id="36545-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="36545-149">Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine* adını girin.</span><span class="sxs-lookup"><span data-stu-id="36545-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="36545-150">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="36545-150">Example scenario</span></span>

<span data-ttu-id="36545-151">Bu örnek senaryo, bu konunun önceki bölümlerinde anlatılan şekilde sisteminizi hazırladıktan sonra SPS'nin nasıl ayarlanacağını ve kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36545-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="36545-152">Bu senaryoda, yukarıda sözü edilen tanıtım amaçlı değerlendirme altyapısı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="36545-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="36545-153">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="36545-153">Make demo data available</span></span>

<span data-ttu-id="36545-154">Burada belirtilen tanıtım kayıtlarını ve değerlerini kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="36545-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="36545-155">Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36545-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="36545-156">Senaryoyu ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-156">Set up the scenario</span></span>

<span data-ttu-id="36545-157">Bu örnek senaryo için bir tanıtım taşıyıcınız, taşıyıcı grubunuz, paketleme ilkeniz ve paketleme profiliniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="36545-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="36545-158">Aşağıdaki alt bölümler senaryo için gereken kayıtların nasıl hazırlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="36545-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="36545-159">Üretim senaryosunda, kurulum işlemi genellikle burada açıklanan işleme benzer.</span><span class="sxs-lookup"><span data-stu-id="36545-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="36545-160">Ancak, farklı değerler ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="36545-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="36545-161">Taşıyıcıları ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-161">Set up carriers</span></span>

<span data-ttu-id="36545-162">Taşıyıcı ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="36545-163">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Sevkiyat taşıyıcıları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="36545-164">Eylem Bölmesi'nde, bir taşıyıcı eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="36545-165">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="36545-166">**Sevkiyat taşıyıcısı:** *Tanıtım Taşıyıcısı*</span><span class="sxs-lookup"><span data-stu-id="36545-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="36545-167">**Ad:** *Tanıtım Taşıyıcısı*</span><span class="sxs-lookup"><span data-stu-id="36545-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="36545-168">**Mod:** *Kara yolu*</span><span class="sxs-lookup"><span data-stu-id="36545-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="36545-169">**Genel bakış** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="36545-170">**Sevkiyat taşıyıcısını etkinleştir**: *Evet*</span><span class="sxs-lookup"><span data-stu-id="36545-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="36545-171">**Taşıyıcı değerlendirmesini etkinleştir**: *Evet*</span><span class="sxs-lookup"><span data-stu-id="36545-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="36545-172">**Hizmetler** hızlı sekmesinde, ızgaraya hizmet eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="36545-173">Yeni hizmet için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="36545-174">**Taşıyıcı hizmeti:** *Tanıtım taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="36545-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="36545-175">**Ad:** *Tanıtım taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="36545-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="36545-176">**Taşıma yöntemi:** *Kara yolu*</span><span class="sxs-lookup"><span data-stu-id="36545-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="36545-177">Tüm diğer alanlar için gerektiği gibi rastgele değerler girin.</span><span class="sxs-lookup"><span data-stu-id="36545-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="36545-178">(Yeni sevkiyat taşıyıcısı kaydını kaydettiğinizde, yeni bir teslimat modu oluşturulur ve **Teslimat şekli** alanı otomatik olarak ayarlanır.)</span><span class="sxs-lookup"><span data-stu-id="36545-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="36545-179">Izgaraya değerlendirme profili eklemek için **Değerlendirme profilleri** hızlı sekmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="36545-180">Yeni profil için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="36545-181">**Değerlendirme profili:** *Tanıtım taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="36545-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="36545-182">**Ad:** *Tanıtım taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="36545-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="36545-183">**Değerlendirme altyapısı:** *Tanıtım değerlendirme alt yapısı*</span><span class="sxs-lookup"><span data-stu-id="36545-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="36545-184">Tüm diğer alanlar için gerektiği gibi rastgele değerler girin.</span><span class="sxs-lookup"><span data-stu-id="36545-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="36545-185">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="36545-186">Taşıyıcıların nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Sevkiyat taşıyıcılarını ayarlama](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="36545-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="36545-187">Taşıyıcı hizmeti hesaplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-187">Set up carrier service accounts</span></span>

<span data-ttu-id="36545-188">Taşıyıcı hizmeti hesabını ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="36545-189">**Taşıma yönetimi \> Kurulum \> Değerlendirme \> Taşıyıcı hizmeti hesabı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="36545-190">Eylem bölmesinde taşıyıcı hizmeti hesabı eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="36545-191">Yeni hesap için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="36545-192">**Sevkiyat Taşıyıcısı:** *Tanıtım Taşıyıcısı*</span><span class="sxs-lookup"><span data-stu-id="36545-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="36545-193">**Taşıyıcı hizmeti:** *Tanıtım taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="36545-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="36545-194">**Taşıyıcı müşteri hesap numarası:** Sevkiyat taşıyıcısı bağlantısını teyit etmek ve kimliğini doğrulamak için kullanılan taşıyıcı müşteri hesap numarası.</span><span class="sxs-lookup"><span data-stu-id="36545-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="36545-195">Taşıyıcınız, bu değeri sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="36545-195">Your carrier will provide this value.</span></span> <span data-ttu-id="36545-196">Tanıtım hizmetini kullanıyorsanız rastgele bir değer girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36545-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="36545-197">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="36545-197">**Site:** *6*</span></span>
    - <span data-ttu-id="36545-198">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="36545-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="36545-199">Genellikle, **Taşıyıcı müşteri hesap numarası** değeri bağlantının kimliğini doğrulamak için gereken tek değerdir.</span><span class="sxs-lookup"><span data-stu-id="36545-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="36545-200">Ancak, taşıyıcınız ek kimlik doğrulama parametreleri gerektiriyorsa, kuruluşunuz bu sayfayı uygun alanları gerektiği gibi ekleyecek şekilde özelleştirmelidir.</span><span class="sxs-lookup"><span data-stu-id="36545-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="36545-201">Konteyner paketleme ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-201">Set up a container packing policy</span></span>

<span data-ttu-id="36545-202">Konteyner paketleme ilkesi ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="36545-203">Daha önce bir ZPL yazıcı tanımı ayarlamadıysanız ayarlamak için Belge Yönlendirme Aracısını uygulamasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="36545-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="36545-204">Daha fazla bilgi için [Belge yazdırmaya genel bakış](../../fin-ops-core/dev-itpro/analytics/print-documents.md) ve ilgili konuları inceleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="36545-205">**Ambar Yönetimi\> Kurulum \> Konteynerler \> Konteyner paketleme ilkeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="36545-206">Eylem bölmesinde konteyner paketleme ilkesi eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="36545-207">Yeni ilkenin üst bilgisinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="36545-208">**Konteyner paketleme ilkesi:** *Tanıtım paketleme ilkesi*</span><span class="sxs-lookup"><span data-stu-id="36545-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="36545-209">**Açıklama**: İlke için açıklama girin</span><span class="sxs-lookup"><span data-stu-id="36545-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="36545-210">**Genel bakış** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="36545-211">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="36545-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="36545-212">**Son sevkiyat için varsayılan yerleşim:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="36545-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="36545-213">**Ağırlık birimi:** *KG*</span><span class="sxs-lookup"><span data-stu-id="36545-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="36545-214">**Konteyner kapatma ilkesi:** *Otomatik serbest bırakma*</span><span class="sxs-lookup"><span data-stu-id="36545-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="36545-215">**Konteyner serbest bırakma ilkesi:** *Son sevk yerleşiminde kullanılabilir hale getir*</span><span class="sxs-lookup"><span data-stu-id="36545-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="36545-216">**Konteyner bildirimi** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="36545-217">**Konteyner kapanışında otomatik bildirim:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="36545-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="36545-218">**Konteynere ilişkin bildirim gereksinimleri:** *Taşıma yönetimi*</span><span class="sxs-lookup"><span data-stu-id="36545-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="36545-219">**Konteyner içeriğini yazdır:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="36545-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="36545-220">**Taşıyıcı etiketini yazdırma** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="36545-221">**Konteyner gönderim etiketini yazdır:** *Her zaman*</span><span class="sxs-lookup"><span data-stu-id="36545-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="36545-222">**Yazıcı adı:** Gönderim etiketlerini yazdırması gereken ZPL yazıcısının adı</span><span class="sxs-lookup"><span data-stu-id="36545-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="36545-223">Paketleme profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-223">Set up a packing profile</span></span>

<span data-ttu-id="36545-224">Paketleme profili ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="36545-225">**Ambar Yönetimi \> Kurulum \> Paketleme \> Paketleme profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="36545-226">Eylem Bölmesinde, ızgaraya paketleme profili eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="36545-227">Yeni profil için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="36545-228">**Paketleme profili kodu:** *Tanıtım paketleme profili*</span><span class="sxs-lookup"><span data-stu-id="36545-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="36545-229">**Açıklama**: Profil için açıklama girin</span><span class="sxs-lookup"><span data-stu-id="36545-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="36545-230">**Konteyner paketleme ilkesi:** *Tanıtım paketleme ilkesi*</span><span class="sxs-lookup"><span data-stu-id="36545-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="36545-231">**Konteyner kimliği modu:** *Otomatik*</span><span class="sxs-lookup"><span data-stu-id="36545-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="36545-232">**Konteyner türü:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="36545-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="36545-233">SPS taşıyıcısını kullanmak için müşteri ayarlama</span><span class="sxs-lookup"><span data-stu-id="36545-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="36545-234">Oluşturduğunuz taşıyıcıyı kullanacak bir müşteri ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="36545-235">**Alacak hesapları \> müşteriler \> Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="36545-236">Izgarada, *US-027* müşterisini bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="36545-237">Eylem Bölmesi'nde, **Genel** sekmesindeki **Kurulum** grubunda **Taşıyıcı müşteri hesapları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="36545-238">**Taşıyıcı müşteri hesapları** sayfasındaki Eylem Bölmesinde **Yeni**'yi seçerek ızgaraya bir hesap ekleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="36545-239">Yeni hesap için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="36545-240">**Sevkiyat taşıyıcısı:** *Tanıtım Taşıyıcısı*</span><span class="sxs-lookup"><span data-stu-id="36545-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="36545-241">**Taşıyıcı müşteri hesap numarası:** *12345* (Bu senaryoda bu değer önemli değildir ancak sonraki bölümde başvurulacaktır.)</span><span class="sxs-lookup"><span data-stu-id="36545-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="36545-242">Örnek senaryoda ilerleyin</span><span class="sxs-lookup"><span data-stu-id="36545-242">Go through the example scenario</span></span>

<span data-ttu-id="36545-243">Önceki bölümde açıklandığı gibi tüm örnek verileri ayarladıktan sonra örnek senaryo için hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="36545-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="36545-244">Satış siparişi oluşturma ve işi işleme</span><span class="sxs-lookup"><span data-stu-id="36545-244">Create a sales order and process the work</span></span>

<span data-ttu-id="36545-245">Satış siparişi oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="36545-246">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="36545-247">Satış siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="36545-248">**Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanını *US-027* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="36545-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="36545-249">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="36545-250">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="36545-250">The new sales order is opened.</span></span> <span data-ttu-id="36545-251">**Satış siparişi başlığı** hızlı sekmesinde, **Taşıyıcı müşteri hesap numarası** alanını daha önce bu müşteri için seçtiğiniz değere (*12345*) ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="36545-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="36545-252">**Satış siparişi satırları** bölümünde bir satış satırı ekleyin ve bunun için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="36545-253">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="36545-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="36545-254">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="36545-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="36545-255">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="36545-255">**Site:** *6*</span></span>
    - <span data-ttu-id="36545-256">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="36545-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="36545-257">**Üst bilgi** görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="36545-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="36545-258">**Teslimat** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="36545-259">**Sevkiyat taşıyıcısı:** *Tanıtım Taşıyıcısı*</span><span class="sxs-lookup"><span data-stu-id="36545-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="36545-260">**Taşıyıcı hizmeti:** *Tanıtım taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="36545-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="36545-261">**Satırlar** görünümüne dönün.</span><span class="sxs-lookup"><span data-stu-id="36545-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="36545-262">Satış satırları için teslimat şeklini güncelleştirmeniz istenirse **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="36545-263">**Satış siparişi satırları** bölümünde, daha önce ayarladığınız sipariş satırını seçin ve **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="36545-264">**Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="36545-265">Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="36545-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="36545-266">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="36545-267">Maddeleri malzeme çekme yerleşiminden paketleme istasyonuna taşımak için bir iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="36545-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="36545-268">**Satış siparişi satırları** bölümünde **Ambar \> Sevkiyat ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="36545-269">**Sevkiyat ayrıntıları** sayfasında, sevkiyat kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="36545-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="36545-270">Paketleme istasyonunda sevkiyatı paketlerken buna ihtiyacınız olacak.</span><span class="sxs-lookup"><span data-stu-id="36545-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="36545-271">Satış siparişine dönmek için **Sevkiyat ayrıntıları** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="36545-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="36545-272">Satış siparişi numarasını not edin ve **Ambar yönetimi \> İş \> Tüm işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="36545-273">Sipariş için oluşturulan işi bulmak ve seçmek için satış siparişi numarasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="36545-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="36545-274">Eylem Bölmesindeki **İş** sekmesinde, **İşi tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="36545-275">**İşi tamamlama** sayfasındaki **Kullanıcı kimliği** alanında bir kullanıcı kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="36545-276">Ardından, Eylem Bölmesi'nde **İşi doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="36545-277">İş doğrulama aşamasından geçerse Eylem Bölmesinde **İşi tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="36545-278">Maddelerin sevk istasyonuna taşınmasının simülasyonu için iş tamamlandı olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="36545-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="36545-279">Sevkiyatı paketleme</span><span class="sxs-lookup"><span data-stu-id="36545-279">Pack the shipment</span></span>

<span data-ttu-id="36545-280">Sevkiyatı paketlemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36545-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="36545-281">**Ambar yönetimi \> Kurulum \> Çalışan** bölümüne gidin ve kullanıcı hesabınızın ambar yönetimi için bir çalışan hesabıyla ilişkilendirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="36545-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="36545-282">**Ambar yönetimi \> Malzeme çekme ve konteyner kullanımı \> Paket**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="36545-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="36545-283">**Sevk istasyonu seç** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="36545-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="36545-284">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="36545-284">**Site:** *6*</span></span>
    - <span data-ttu-id="36545-285">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="36545-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="36545-286">**Yerleşim:** *Paket*</span><span class="sxs-lookup"><span data-stu-id="36545-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="36545-287">**Paketleme profili kodu:** *Tanıtım paketleme profili*</span><span class="sxs-lookup"><span data-stu-id="36545-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="36545-288">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-288">Select **OK**.</span></span>
1. <span data-ttu-id="36545-289">**Paket** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="36545-289">The **Pack** page appears.</span></span> <span data-ttu-id="36545-290">Üretim senaryosunda, bir çalışan bir lisans plakası veya sevkiyat kodunu taratır.</span><span class="sxs-lookup"><span data-stu-id="36545-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="36545-291">Ancak, bu senaryo için **Tüm sevkiyatlar** sayfasını açın ve az önce oluşturduğunuz sevkiyatın sevkiyat numarasını arayın.</span><span class="sxs-lookup"><span data-stu-id="36545-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="36545-292">Daha sonra, bu değeri **Paket** sayfasındaki **Plaka veya sevkiyat** alanına girin.</span><span class="sxs-lookup"><span data-stu-id="36545-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="36545-293">Alternatif olarak, az önce not ettiğiniz sevkiyat kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="36545-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="36545-294">Eylem Bölmesinde **Yeni konteyner**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="36545-295">Yeni konteynerin ayrıntılarını gösteren iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="36545-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="36545-296">Varsayılan değerleri olduğu gibi bırakın ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="36545-297">**Paket** sayfasındaki **Madde sevki** hızlı sekmesinde yer alan **Tanımlayıcı** alanında, maddeyi paketlemek için *A0002*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="36545-298">Madde konteynere eklenir.</span><span class="sxs-lookup"><span data-stu-id="36545-298">The item is added to the container.</span></span>
1. <span data-ttu-id="36545-299">Eylem Bölmesi'nde, **Sevk edilecek konteynerler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="36545-300">Görüntülenen **Sevk edilecek konteynerler** sayfasında az önce oluşturduğunuz konteyner satırı bulunur.</span><span class="sxs-lookup"><span data-stu-id="36545-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="36545-301">Ancak, henüz taşıyıcıdan gönderim etiketini ve izleme numarasını almadığınız için bu satırdaki **Konteyner bildirim kodu** alanı şu anda boştur.</span><span class="sxs-lookup"><span data-stu-id="36545-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="36545-302">Eylem Bölmesinde **Konteyneri kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="36545-303">**Konteyneri kapat** iletişim kutusunda **Brüt ağırlık** alanını *1 kg* olarak ayarlayıp **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="36545-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="36545-304">Şimdi gönderim etiketi, seçtiğiniz ZPL yazıcısında yazdırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="36545-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="36545-305">Bu etiket, aşağıdaki örneğe benzeyecektir.</span><span class="sxs-lookup"><span data-stu-id="36545-305">It should resemble the following example.</span></span>

    <span data-ttu-id="36545-306">![Örnek gönderim etiketi](media/sps-label-example.png "Örnek gönderim etiketi")</span><span class="sxs-lookup"><span data-stu-id="36545-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="36545-307">**Konteyner bildirim kodu** ve **Toplam navlun** değerlerinin, taşıyıcıdan alındığı şekilde eklendiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="36545-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
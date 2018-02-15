---
title: "Müşteri adayından nakde"
description: "Bu konuda, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ile Microsoft Dynamics 365 for Sales arasındaki Müşteri adayından nakde çözümüne genel bakış sunulmaktadır."
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1f76359878d162e93d8f8b7c11be529c43c94455
ms.openlocfilehash: 9b150bfca362303b4ac35a38ab818229082c7330
ms.contentlocale: tr-tr
ms.lasthandoff: 02/08/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="81bb9-103">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="81bb9-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="81bb9-104">Müşteri adayından nakde çözümü, Dynamics 365 for Finance and Operations, Enterprise edition ile Dynamics 365 for Sales arasında doğrudan eşitleme yapılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="81bb9-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="81bb9-105">Veri Tümleştirme özelliğiyle birlikte kullanılan Müşteri adayından nakde şablonları Finance and Operations ile Sales arasında hesaplar, ürünler, satışlar, satış teklifleri, satış siparişleri ve satış faturaları için veri akışı sağlar.</span><span class="sxs-lookup"><span data-stu-id="81bb9-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="81bb9-106">Finance and Operations ile Sales arasında veri akışı sağlanırken, Sales'de satış ve pazarlama faaliyetlerini gerçekleştirebilir ve Finance and Operations'da stok yönetimini kullanarak sipariş karşılamaları işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81bb9-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="81bb9-107">Müşteri adayından nakde tümleştirmesi hakkında daha fazla bilgi için kısa YouTube videosunu izleyin:</span><span class="sxs-lookup"><span data-stu-id="81bb9-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="81bb9-108">Geçerli sürümde, Müşteri adayından nakde çözümü aşağıdaki türlerde doğrudan eşitleme sağlar:</span><span class="sxs-lookup"><span data-stu-id="81bb9-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="81bb9-109">Hesapları Sales içinde koruma ve onları doğrudan Sales'den Finance and Operations'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="81bb9-110">Finance and Operations'taki ürünleri koruma ve onları doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="81bb9-111">Sales'deki ilgili kişileri koruma ve onları doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="81bb9-112">Sales'deki satış tekliflerini doğrudan Finance and Operations'la eşitleme (şablon sürümü beklemede)</span><span class="sxs-lookup"><span data-stu-id="81bb9-112">Synchronize sales quotation directly from Sales to Finance and Operations (template pending release)</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="81bb9-113">Finance and Operations'taki satış siparişlerini doğrudan Sales'le eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-113">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="81bb9-114">Satış siparişlerini Sales ile Finance and Operations arasında doğrudan eşitleme (şablon sürümü beklemede)</span><span class="sxs-lookup"><span data-stu-id="81bb9-114">Synchronize sales orders directly between Sales and Finance and Operations (template pending release)</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="81bb9-115">Finance and Operations'taki satış faturasını doğrudan Sales'le eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="81bb9-116">Önceki sürümlerde, Müşteri adayından nakde çözümü doğrudan yapılamayan aşağıdaki eşitleme türlerini sağlıyordu:</span><span class="sxs-lookup"><span data-stu-id="81bb9-116">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="81bb9-117">Hesapları Sales içinde yönetin ve onları Finance and Operations ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="81bb9-117">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="81bb9-118">Sales'deki ilgili kişileri koruma ve onları Finance and Operations ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-118">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="81bb9-119">Finance and Operations'taki ürünleri koruma ve onları Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-119">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="81bb9-120">Sales'de satış teklifleri oluşturma ve onları Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-120">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="81bb9-121">Finance and Operations'ta satış siparişleri oluşturma ve onları doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-121">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="81bb9-122">Finance and Operations'ta satış faturaları oluşturma ve onları doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="81bb9-122">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="81bb9-123">Finance and Operations için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="81bb9-123">System requirements for Finance and Operations</span></span>

<span data-ttu-id="81bb9-124">Müşteri adayından nakde tümleştirmesi aşağıdaki sürümlerde desteklenir:</span><span class="sxs-lookup"><span data-stu-id="81bb9-124">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="81bb9-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (Aralık 2017)</span><span class="sxs-lookup"><span data-stu-id="81bb9-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="81bb9-126">Dynamics 365 for Finance and Operations, Enterprise edition (Aralık 2017) - Uygulama derlemesi 7.3.11971.56116 Platform Güncelleştirmesi 12 ile birlikte (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="81bb9-126">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="81bb9-127">Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017)</span><span class="sxs-lookup"><span data-stu-id="81bb9-127">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="81bb9-128">Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) - platform güncelleştirmesi 8 ile birlikte (uygulama derlemesi 7.2.11792.56024, platform derlemesi 7.0.4565.16212 ile birlikte).</span><span class="sxs-lookup"><span data-stu-id="81bb9-128">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="81bb9-129">Aşağıdaki düzeltmeler gereklidir:</span><span class="sxs-lookup"><span data-stu-id="81bb9-129">The following hotfixes are required:</span></span>

    - <span data-ttu-id="81bb9-130">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** - Bu düzeltme Veri Tümleştirme özelliğiyle Sales'den Finance and Operations'a satış siparişi eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="81bb9-130">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="81bb9-131">Başka geliştirmeler de içerir.</span><span class="sxs-lookup"><span data-stu-id="81bb9-131">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="81bb9-132">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Bu düzeltme Veri Tümleştirme özelliğiyle Finance and Operations'tan Sales'e satış siparişi satırı eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="81bb9-132">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="81bb9-133">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Bu düzeltme Veri Tümleştirme özelliğiyle Finance and Operations'tan Sales'a satış siparişi eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="81bb9-133">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="81bb9-134">Yalnızca KB4045570 düzeltmesini yüklemeniz yeterlidir çünkü yükleme diğer düzeltmelerdeki değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="81bb9-134">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="81bb9-135">Dynamics 365 for Finance and Operations sürüm 1611 (Kasım 2016)</span><span class="sxs-lookup"><span data-stu-id="81bb9-135">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="81bb9-136">Dynamics 365 for Finance and Operations sürüm 1611 (Kasım 2016), platform güncelleştirmesi 8 veya üstü ile birlikte</span><span class="sxs-lookup"><span data-stu-id="81bb9-136">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="81bb9-137">Aşağıdaki düzeltmeler gereklidir:</span><span class="sxs-lookup"><span data-stu-id="81bb9-137">The following hotfixes are required:</span></span>

    - <span data-ttu-id="81bb9-138">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Finance and Operations'dan Sales'a Veri tümleştiriciyle satış siparişi eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="81bb9-138">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="81bb9-139">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Finance and Operations'dan Sales'a Veri tümleştiriciyle satış siparişi başlığı ve satırı eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="81bb9-139">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="81bb9-140">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Veri varlıkları aracılığıyla müşteri adayından nakde tümleştirmesi için destek gereklidir.</span><span class="sxs-lookup"><span data-stu-id="81bb9-140">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="81bb9-141">Düzeltmeleri yükledikten sonra aşağıdaki toplu işi **SalesPopulateProspectToCash** formundan tetiklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="81bb9-141">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="81bb9-142">Bu form yalnızca bir kez gereksinim duyacağınızdan gizlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="81bb9-142">This form is hidden because you only need it once.</span></span> <span data-ttu-id="81bb9-143">Forma ulaşmak için ortamda oturum açın ve aşağıdaki URL'yi tarayıcı adresinize ekleyin: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span><span class="sxs-lookup"><span data-stu-id="81bb9-143">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span></span> <span data-ttu-id="81bb9-144">Form açıldığında Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="81bb9-144">When the form opens, click OK.</span></span> <span data-ttu-id="81bb9-145">Bu, **SalesLine**, **SalesQuotationLine** ve **CustInvoiceTrans** tablolarında benzersiz değerlere sahip yeni bir **LineCreationSequnceNumber** alanı oluşturur ve ürün listesi yenilenir.</span><span class="sxs-lookup"><span data-stu-id="81bb9-145">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="81bb9-146">Müşteri adayından nakde tümleştirmesinin çalışması için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="81bb9-146">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="81bb9-147">Sales için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="81bb9-147">System requirements for Sales</span></span>

<span data-ttu-id="81bb9-148">Müşteri adayından nakde çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="81bb9-148">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="81bb9-149">Dynamics 365 for Sales sürüm 1612 (8.2.1.207) (DB 8.2.1.207) çevrimiçi</span><span class="sxs-lookup"><span data-stu-id="81bb9-149">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="81bb9-150">Dynamics 365 for Sales, sürüm 1.15.0.0 (v15) için müşteri adayından nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="81bb9-150">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="81bb9-151">1.0.0.0 ve 1.0.0.1 sürümlü şablonlar Dynamics 365 for Sales, sürüm 1.14.1.0'a yönelik Müşteri adayından nakde çözümümde desteklenir</span><span class="sxs-lookup"><span data-stu-id="81bb9-151">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="81bb9-152">2.0.0.0 ve 2.1.0.0 sürümlü şablonlar Dynamics 365 for Sales, sürüm 1.15.0.0'a yönelik Müşteri adayından nakde çözümümde desteklenir</span><span class="sxs-lookup"><span data-stu-id="81bb9-152">Templates with version 2.0.0.0 and 2.1.0.0 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="81bb9-153">Sales için Aday müşteriden nakde çözümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="81bb9-153">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="81bb9-154">CustomerSource'dan [Dynamics 365 for Sales için Müşteri adayından nakde çözüm paketi zip dosyasını](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) indirin.</span><span class="sxs-lookup"><span data-stu-id="81bb9-154">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="81bb9-155">Zip dosyasının engellenmemiş olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="81bb9-155">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="81bb9-156">Aksi takdirde, çözüm paketini yüklemeye çalışırken şu hata iletisini alabilirsiniz "İçe aktarma paketi bulunamadı."</span><span class="sxs-lookup"><span data-stu-id="81bb9-156">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="81bb9-157">Zip dosyasındaki engellemeyi kaldırmak için dosyaya sağ tıklayın ve **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="81bb9-157">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="81bb9-158">**Engellemeyi Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="81bb9-158">Select **Unblock**.</span></span>
3. <span data-ttu-id="81bb9-159">Zip dosyasını açın ve **PackageDeployer.exe**'yi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="81bb9-159">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="81bb9-160">Müşteri adayından nakde çözümünü Sales kurulumunuza yükleyin:</span><span class="sxs-lookup"><span data-stu-id="81bb9-160">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="81bb9-161">Dağıtım türü olarak **Office 365** seçin.</span><span class="sxs-lookup"><span data-stu-id="81bb9-161">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="81bb9-162">**Gelişmişi göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="81bb9-162">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="81bb9-163">Hızlı yükleme için bir bölge seçin.</span><span class="sxs-lookup"><span data-stu-id="81bb9-163">For a quick installation, select a region.</span></span> <span data-ttu-id="81bb9-164">**Bilmiyorum**'u seçerseniz, sistem tüm bölgeleri arayacaktır ve yükleme daha uzun sürecektir.</span><span class="sxs-lookup"><span data-stu-id="81bb9-164">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="81bb9-165">Yükleme haklarına sahip bir yönetici kullanıcı için kullanıcı adı ve parola girin.</span><span class="sxs-lookup"><span data-stu-id="81bb9-165">Enter the user name and password of an admin user who has installation rights.</span></span>




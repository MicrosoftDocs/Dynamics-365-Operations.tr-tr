---
title: "Müşteri adayından nakde"
description: "Bu konuda, Microsoft Dynamics 365 for Finance and Operations ile Microsoft Dynamics 365 for Sales arasındaki Müşteri adayından nakde çözümüne genel bakış sunulmaktadır."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 801407183ad90f08bde928a1d3da13cba38cfc27
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="ec37b-103">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="ec37b-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec37b-104">Müşteri adayından nakde çözümü, Dynamics 365 for Finance and Operations ile Dynamics 365 for Sales arasında doğrudan eşitleme yapılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="ec37b-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="ec37b-105">Veri Tümleştirme özelliğiyle birlikte kullanılan Müşteri adayından nakde şablonları Finance and Operations ile Sales arasında hesaplar, ürünler, satışlar, satış teklifleri, satış siparişleri ve satış faturaları için veri akışı sağlar.</span><span class="sxs-lookup"><span data-stu-id="ec37b-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="ec37b-106">Finance and Operations ile Sales arasında veri akışı sağlanırken, Sales'de satış ve pazarlama faaliyetlerini gerçekleştirebilir ve Finance and Operations'da stok yönetimini kullanarak sipariş karşılamaları işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec37b-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="ec37b-107">Müşteri adayından nakde tümleştirmesi hakkında daha fazla bilgi için YouTube'daki kısa videoyu izleyin: [![](https://img.youtube.com/vi/AVV9x5x-XCg/0.jpg)](https://www.youtube.com/watch?v=AVV9x5x-XCg)</span><span class="sxs-lookup"><span data-stu-id="ec37b-107">For more information about the Prospect to cash integration, watch the short YouTube video: [![](https://img.youtube.com/vi/AVV9x5x-XCg/0.jpg)](https://www.youtube.com/watch?v=AVV9x5x-XCg)</span></span>


<span data-ttu-id="ec37b-108">Geçerli sürümde, Müşteri adayından nakde çözümü aşağıdaki türlerde doğrudan eşitleme sağlar:</span><span class="sxs-lookup"><span data-stu-id="ec37b-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="ec37b-109">Hesapları Sales içinde koruma ve onları doğrudan Sales'den Finance and Operations'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="ec37b-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="ec37b-110">Finance and Operations'taki ürünleri koruma ve onları doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="ec37b-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="ec37b-111">Sales'deki ilgili kişileri koruma ve onları doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="ec37b-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="ec37b-112">Sales'deki satış teklifini doğrudan Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="ec37b-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="ec37b-113">Satış siparişlerini Sales ile Finance and Operations arasında doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="ec37b-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="ec37b-114">Satış faturasını doğrudan Finance and Operations'tan Sales'e eşitleme</span><span class="sxs-lookup"><span data-stu-id="ec37b-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="ec37b-115">Finance and Operations için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="ec37b-115">System requirements for Finance and Operations</span></span>
<span data-ttu-id="ec37b-116">Müşteri adayından nakde tümleştirmesi aşağıdaki sürümlerde desteklenir:</span><span class="sxs-lookup"><span data-stu-id="ec37b-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="ec37b-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (Aralık 2017)</span><span class="sxs-lookup"><span data-stu-id="ec37b-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="ec37b-118">Dynamics 365 for Finance and Operations, Enterprise edition (Aralık 2017) - Uygulama derlemesi 7.3.11971.56116 Platform Güncelleştirmesi 12 ile birlikte (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="ec37b-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="ec37b-119">Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017)</span><span class="sxs-lookup"><span data-stu-id="ec37b-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="ec37b-120">Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) - platform güncelleştirmesi 8 ile birlikte (uygulama derlemesi 7.2.11792.56024, platform derlemesi 7.0.4565.16212 ile birlikte).</span><span class="sxs-lookup"><span data-stu-id="ec37b-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="ec37b-121">Aşağıdaki düzeltmeler gereklidir:</span><span class="sxs-lookup"><span data-stu-id="ec37b-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="ec37b-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** - Bu düzeltme Veri Tümleştirme özelliğiyle Sales'den Finance and Operations'a satış siparişi eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ec37b-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="ec37b-123">Başka geliştirmeler de içerir.</span><span class="sxs-lookup"><span data-stu-id="ec37b-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="ec37b-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Bu düzeltme Veri Tümleştirme özelliğiyle Finance and Operations'tan Sales'e satış siparişi satırı eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ec37b-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="ec37b-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Bu düzeltme Veri Tümleştirme özelliğiyle Finance and Operations'tan Sales'a satış siparişi eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ec37b-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec37b-126">Yalnızca KB4045570 düzeltmesini yüklemeniz yeterlidir çünkü yükleme diğer düzeltmelerdeki değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="ec37b-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="ec37b-127">Dynamics 365 for Finance and Operations sürüm 1611 (Kasım 2016)</span><span class="sxs-lookup"><span data-stu-id="ec37b-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="ec37b-128">Dynamics 365 for Finance and Operations sürüm 1611 (Kasım 2016), platform güncelleştirmesi 8 veya üstü ile birlikte</span><span class="sxs-lookup"><span data-stu-id="ec37b-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="ec37b-129">Aşağıdaki düzeltmeler gereklidir:</span><span class="sxs-lookup"><span data-stu-id="ec37b-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="ec37b-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Finance and Operations'dan Sales'a Veri tümleştiriciyle satış siparişi eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ec37b-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
  - <span data-ttu-id="ec37b-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Finance and Operations'dan Sales'a Veri tümleştiriciyle satış siparişi başlığı ve satırı eşitlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ec37b-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
  - <span data-ttu-id="ec37b-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Veri varlıkları aracılığıyla müşteri adayından nakde tümleştirmesi için destek gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ec37b-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ec37b-133">Düzeltmeleri yükledikten sonra aşağıdaki toplu işi **SalesPopulateProspectToCash** formundan tetiklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec37b-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="ec37b-134">Bu form yalnızca bir kez gereksinim duyacağınızdan gizlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="ec37b-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="ec37b-135">Forma erişmek için ortamda oturum açın ve şu ifadeyi tarayıcı adresinizdeki URL'ye ekleyin: *&mi=action:SalesPopulateProspectToCash*, örneğin `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="ec37b-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="ec37b-136">Form açıldığında Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec37b-136">When the form opens, click OK.</span></span> <span data-ttu-id="ec37b-137">Bu, **SalesLine**, **SalesQuotationLine** ve **CustInvoiceTrans** tablolarında benzersiz değerlere sahip yeni bir **LineCreationSequnceNumber** alanı oluşturur ve ürün listesi yenilenir.</span><span class="sxs-lookup"><span data-stu-id="ec37b-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="ec37b-138">Müşteri adayından nakde tümleştirmesinin çalışması için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ec37b-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="ec37b-139">Sales için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="ec37b-139">System requirements for Sales</span></span>

<span data-ttu-id="ec37b-140">Müşteri adayından nakde çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="ec37b-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="ec37b-141">Dynamics 365 for Sales sürüm 1612 (8.2.1.207) (DB 8.2.1.207) çevrimiçi veya sonraki bir sürüm.</span><span class="sxs-lookup"><span data-stu-id="ec37b-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="ec37b-142">Dynamics 365 for Sales için aday müşteriden nakde çözümü, sürüm 1.15.0.0 veya üstü.</span><span class="sxs-lookup"><span data-stu-id="ec37b-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="ec37b-143">Çözüm AppSource'tan indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ec37b-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="ec37b-144">[Download Dynamics 365, Aday Müşteriden Nakde](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="ec37b-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>


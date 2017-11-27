---
title: "Müşteri adayından nakde"
description: "Bu konu Dynamics 365 for Finance and Operations, Enterprise edition ve Dynamics 365 for Sales arasındaki Müşteri adayından nakde çözümüne bir genel bakış sağlar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: tr-tr
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="759f0-103">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="759f0-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="759f0-104">Müşteri adayından nakde çözümü [Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration)'nü Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ve Dynamics 365 for Sales örnekleri için ORtak Veri Hizmeti (CDS) aracılığıyla kullanır.</span><span class="sxs-lookup"><span data-stu-id="759f0-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="759f0-105">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="759f0-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="759f0-106">Veri Finance and Operations ve Sales arasında akarken, satış ve pazarlama etkinliklerini Sales içerisinde gerçekleştirebilir ve sipariş tamamlamayı, stok yönetimi ile Finance and Operations içerisinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="759f0-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="759f0-107">Bu çözüm aşağıdaki alanlarda tümleştirme sağlar:</span><span class="sxs-lookup"><span data-stu-id="759f0-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="759f0-108">Hesapları Sales içinde yönetin ve onları Finance and Operations ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="759f0-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="759f0-109">İlgili kişileri Sales içinde yönetin ve onları Finance and Operations ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="759f0-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="759f0-110">Ürünleri Finance and Operations içinde yönetin ve onları Sales ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="759f0-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="759f0-111">Satış tekliflerini Sales içinde oluşturun ve onları Finance and Operations ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="759f0-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="759f0-112">Finance and Operations içinde satış siparişleri oluşturun ve onları Sales ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="759f0-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="759f0-113">Finance and Operations içinde satış faturaları oluşturun ve onları Sales ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="759f0-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="759f0-114">Bu çözüm aşağıdaki alanlarda doğrudan eşitleme sağlar:</span><span class="sxs-lookup"><span data-stu-id="759f0-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="759f0-115">Hesapları Sales içinde koruma ve onları doğrudan Sales'den Finance and Operations'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="759f0-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="759f0-116">Ürünleri Finance and Operations içinde yönetme ve onları doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="759f0-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="759f0-117">Sales'teki ilgili kişileri koruma ve onları doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="759f0-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="759f0-118">Sales'deki satış teklifi başlıklarını ve satırlarını doğrudan Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="759f0-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="759f0-119">Finance and Operations içinde satış siparişleri oluşturma ve onları doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="759f0-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="759f0-120">Sales ile Finance and Operations arasında satış siparişi başlıklarını ve satırlarını doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="759f0-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="759f0-121">Sales ile Finance and Operations arasında satış siparişlerini doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="759f0-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="759f0-122">Finance and Operations içinde satış faturaları oluşturma ve onları doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="759f0-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="759f0-123">Dynamics 365 for Finance and Operations, Enterprise sürümü için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="759f0-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="759f0-124">Adam müşteriden nakde çözümünü kullanmak için şunu yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="759f0-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="759f0-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017), Platform güncelleştirmesi 8 ile (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="759f0-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="759f0-126">Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) için düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="759f0-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="759f0-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - Bu düzeltme Sales ile Finance and Operations arasında Veri Tümleştirme özelliğiyle satış siparişi eşitleme desteği ve çeşitli başka geliştirmeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="759f0-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="759f0-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Bu düzeltme satış siparişi satırları eşitlemesini Finance and Operations'tan Sales'a Veri Tümleştirme özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="759f0-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="759f0-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Bu düzeltme satış siparişi satırları eşitlemesini Finance and Operations'tan Sales'a Veri Tümleştirme özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="759f0-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="759f0-130">**Not**: Yalnızca KB4045570 yüklemeniz yeterlidir çünkü yükleme diğer KB'lerdeki değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="759f0-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="759f0-131">Dynamics 365 for Sales için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="759f0-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="759f0-132">Adam müşteriden nakde çözümünü kullanmak için şunu yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="759f0-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="759f0-133">Dynamics 365 for Sales sürüm 1612 (8.2.1.207) (DB 8.2.1.207) çevrimiçi.</span><span class="sxs-lookup"><span data-stu-id="759f0-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="759f0-134">Dynamics 365 for Sales için Aday müşteriden nakde çözümü, sürüm 1.14.0.0 (v14) veya sonrası.</span><span class="sxs-lookup"><span data-stu-id="759f0-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="759f0-135">Sales için Aday müşteriden nakde çözümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="759f0-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="759f0-136">[Dynamics 365 for Sales için Aday müşteriden nakde çözüm paketi zip dosyasını](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSource üzerinden yükleyin.</span><span class="sxs-lookup"><span data-stu-id="759f0-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="759f0-137">Çözüm paketini yüklerken "İçe aktarma paketleri bulunamadı" hata mesajını almamak için zip dosyasının engellenmemiş olduğunda emin olun.</span><span class="sxs-lookup"><span data-stu-id="759f0-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="759f0-138">Dosyanın engelini kaldırmak için aşağıdakini yapın:</span><span class="sxs-lookup"><span data-stu-id="759f0-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="759f0-139">Zip dosyasına sağ tıklatın.</span><span class="sxs-lookup"><span data-stu-id="759f0-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="759f0-140">**Özellikler**'i seçin ve sonra **Engeli kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759f0-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="759f0-141">PackageDeployer.exe'yi çıkartın ve çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="759f0-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="759f0-142">Aday müşteriden Nakde çözümünü Sales kurulumunuzda yükleyin.</span><span class="sxs-lookup"><span data-stu-id="759f0-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="759f0-143">**Office 365** dağıtım türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="759f0-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="759f0-144">**Gelişmişi göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="759f0-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="759f0-145">Hızlı yükleme için bir **Bölge** seçin.</span><span class="sxs-lookup"><span data-stu-id="759f0-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="759f0-146">**Emin değil**'i seçerseniz, sistem tüm bölgeleri arayacaktır ve yüklemesi daha uzun sürecektir.</span><span class="sxs-lookup"><span data-stu-id="759f0-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="759f0-147">Yükleme için kullanıcı haklarına sahip bir yönetici kullanıcı için **Kullanıcı adı** ve **Parola** girin.</span><span class="sxs-lookup"><span data-stu-id="759f0-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>


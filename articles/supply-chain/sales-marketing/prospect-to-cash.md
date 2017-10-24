---
title: "Müşteri adayından nakde"
description: "Bu konu Dynamics 365 for Finance and Operations, Enterprise edition ve Dynamics 365 for Sales arasındaki Müşteri adayından nakde çözümüne bir genel bakış sağlar."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="65489-103">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="65489-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="65489-104">Müşteri adayından nakde çözümü [Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration)'nü Microsoft Dynamics 365 for Finance and Operations, Enterprise edition ve Dynamics 365 for Sales örnekleri için ORtak Veri Hizmeti (CDS) aracılığıyla kullanır.</span><span class="sxs-lookup"><span data-stu-id="65489-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="65489-105">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="65489-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="65489-106">Veri Finance and Operations ve Sales arasında akarken, satış ve pazarlama etkinliklerini Sales içerisinde gerçekleştirebilir ve sipariş tamamlamayı, stok yönetimi ile Finance and Operations içerisinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65489-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="65489-107">Bu çözüm aşağıdaki alanlarda tümleştirme sağlar:</span><span class="sxs-lookup"><span data-stu-id="65489-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="65489-108">Hesapları Sales içinde yönetin ve onları Finance and Operations ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="65489-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="65489-109">İlgili kişileri Sales içinde yönetin ve onları Finance and Operations ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="65489-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="65489-110">Ürünleri Finance and Operations içinde yönetin ve onları Sales ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="65489-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="65489-111">Satış tekliflerini Sales içinde oluşturun ve onları Finance and Operations ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="65489-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="65489-112">Finance and Operations içinde satış siparişleri oluşturun ve onları Sales ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="65489-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="65489-113">Finance and Operations içinde satış faturaları oluşturun ve onları Sales ile eşitleyin</span><span class="sxs-lookup"><span data-stu-id="65489-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="65489-114">Dynamics 365 for Finance and Operations, Enterprise sürümü için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="65489-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="65489-115">Adam müşteriden nakde çözümünü kullanmak için şunu yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="65489-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="65489-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017), Platform güncelleştirmesi 8 ile (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="65489-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="65489-117">Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) için iki düzeltme.</span><span class="sxs-lookup"><span data-stu-id="65489-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="65489-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Bu düzeltme satış siparişi satırları eşitlemesini Finance and Operations'tan Sales'a Veri Tümleştirme özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="65489-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="65489-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Bu düzeltme satış siparişi satırları eşitlemesini Finance and Operations'tan Sales'a Veri Tümleştirme özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="65489-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="65489-120">**Not**: Yalnızca KB4036524 yüklemeniz yeterlidir çünkü yükleme KB4036461 değişikliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="65489-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="65489-121">Dynamics 365 for Sales için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="65489-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="65489-122">Adam müşteriden nakde çözümünü kullanmak için şunu yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="65489-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="65489-123">Dynamics 365 for Sales sürüm 1612 (8.2.1.207) (DB 8.2.1.207) çevrimiçi veya sonrası.</span><span class="sxs-lookup"><span data-stu-id="65489-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="65489-124">Dynamics 365 for Sales için Aday müşteriden nakde çözümü, sürüm 1.14.0.0 (v14) veya sonrası.</span><span class="sxs-lookup"><span data-stu-id="65489-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="65489-125">Sales için Aday müşteriden nakde çözümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="65489-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="65489-126">[Dynamics 365 for Sales için Aday müşteriden nakde çözüm paketi zip dosyasını](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSource üzerinden yükleyin.</span><span class="sxs-lookup"><span data-stu-id="65489-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="65489-127">Çözüm paketini yüklerken "İçe aktarma paketleri bulunamadı" hata mesajını almamak için zip dosyasının engellenmemiş olduğunda emin olun.</span><span class="sxs-lookup"><span data-stu-id="65489-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="65489-128">Dosyanın engelini kaldırmak için aşağıdakini yapın:</span><span class="sxs-lookup"><span data-stu-id="65489-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="65489-129">Zip dosyasına sağ tıklatın.</span><span class="sxs-lookup"><span data-stu-id="65489-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="65489-130">**Özellikler**'i seçin ve sonra **Engeli kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65489-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="65489-131">PackageDeployer.exe'yi çıkartın ve çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="65489-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="65489-132">Aday müşteriden Nakde çözümünü Sales kurulumunuzda yükleyin.</span><span class="sxs-lookup"><span data-stu-id="65489-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="65489-133">**Office 365** dağıtım türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="65489-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="65489-134">**Gelişmişi göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65489-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="65489-135">Hızlı yükleme için bir **Bölge** seçin.</span><span class="sxs-lookup"><span data-stu-id="65489-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="65489-136">**Emin değil**'i seçerseniz, sistem tüm bölgeleri arayacaktır ve yüklemesi daha uzun sürecektir.</span><span class="sxs-lookup"><span data-stu-id="65489-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="65489-137">Yükleme için kullanıcı haklarına sahip bir yönetici kullanıcı için **Kullanıcı adı** ve **Parola** girin.</span><span class="sxs-lookup"><span data-stu-id="65489-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>


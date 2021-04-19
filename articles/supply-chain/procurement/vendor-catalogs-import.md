---
title: Satıcı kataloglarını içe aktarma
description: Bu konu satıcı katalog verilerini içe aktarma işlemini açıklar.
author: kamaybac
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: dabourq
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: ee709d72098b4304cf7748cae1a328736fa16188
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825242"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="10fda-103">Satıcı kataloglarını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="10fda-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="10fda-104">Satıcı kataloglarını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="10fda-104">Vendor catalogs import</span></span>

<span data-ttu-id="10fda-105">Dynamics 365 Supply Chain Management'da, satınalma uzmanları, şirket personelinin dahili kullanım için maddeler ve hizmetler sipariş ederken kullanabileceği kataloglar oluşturabilir ve yönetebilir.</span><span class="sxs-lookup"><span data-stu-id="10fda-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="10fda-106">Tedarik kataloğu oluşturmak için personele sunmak istediğiniz maddeleri ve hizmetleri ürün katalog verilerini içe aktararak veya ürün katalog verilerini ana ürüne el ile ekleyerek ilave edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10fda-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="10fda-107">Microsoft Dynamics 365 istemcisinden bir satıcı tarafından gönderilen katalog verilerini yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10fda-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="10fda-108">Bir satıcının, bir katalog bakım isteği (CMR) biçiminde size gönderdiği ürün verileri, XML dosyası biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="10fda-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="10fda-109">CMR dosyası satıcının şirketinize sağladığı ürünlerin ayrıntılarını içermelidir.</span><span class="sxs-lookup"><span data-stu-id="10fda-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="10fda-110">Satıcı katalog verilerini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="10fda-110">Import vendor catalog data</span></span>

<span data-ttu-id="10fda-111">Satıcı katalog verilerini içe aktarmak için aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="10fda-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="10fda-112">Veri eşleme kurallarını tanımladığınız Veri yönetimi çalışma alanında bir proje ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="10fda-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="10fda-113">**Veri yönetimi**'ni ve arından **Veri projeleri için rolleri ayarlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="10fda-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="10fda-114">Tedarik kategori hiyerarşisi ayarlayın ve satıcılarınızı tedarik kategorilerine atayın.</span><span class="sxs-lookup"><span data-stu-id="10fda-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="10fda-115">Emtia kodları kullanıyorsanız, emtia kodlarını tedarik kategorilerine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="10fda-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="10fda-116">Tedarik kategori hiyerarşisi ayarlama hakkında bilgi için bkz. [Tedarik kategori hiyerarşisi ayarlama](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="10fda-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="10fda-117">Katalog içe aktarma için satıcıyı yapılandır.</span><span class="sxs-lookup"><span data-stu-id="10fda-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="10fda-118">Bir satıcı seçin ve ardından **Tedarik** > **Kurulum** > **Katalog içe aktarma için satıcıyı yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="10fda-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="10fda-119">Katalog içe aktarma için iş akışını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="10fda-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="10fda-120">CMR dosyası şablonu oluşturun ve bunu satıcınızla paylaşın.</span><span class="sxs-lookup"><span data-stu-id="10fda-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="10fda-121">Bir satıcı kataloğu oluşturmak için **Tedarik ve kaynak atama** \> **Ortak** \> **Kataloglar** \> **Satıcı katalogları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="10fda-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="10fda-122">Satıcınızdan aldığınız katalog bakımı isteği (CMR) dosyaları bu katalogda gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="10fda-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="10fda-123">CMR dosyasını yükleyin.</span><span class="sxs-lookup"><span data-stu-id="10fda-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="10fda-124">Satıcı kataloğundaki ürünleri gözden geçirin, onaylayın veya reddedin.</span><span class="sxs-lookup"><span data-stu-id="10fda-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="10fda-125">Ürünler, tedarik kategorilerine otomatik olarak eşlenir.</span><span class="sxs-lookup"><span data-stu-id="10fda-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="10fda-126">Onaylana ürünler ana ürüne eklenir ve seçilen tüzel kişiliklere serbest bırakılır.</span><span class="sxs-lookup"><span data-stu-id="10fda-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="10fda-127">Yalnızca onaylanmış ürünler tedarik kataloğuna eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="10fda-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="10fda-128">Katalog içe aktarma dosyası şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="10fda-128">Generate a catalog import file template</span></span>

<span data-ttu-id="10fda-129">Katalog içe aktarma dosyası şablonu, satıcı ürünleri için CMR dosyası oluşturmak üzere kullandığınız bir XSD dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="10fda-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="10fda-130">CMR dosyasını yeni katalog oluşturmak, mevcut bir kataloğu değiştirmek veya mevcut katalogda değişiklik yapmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10fda-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="10fda-131">**Tedarik ve kaynak atama** \> **Kataloglar** \> **Satıcı katalogları**'nı seçin ve üzerinde çalışmak istediğiniz kataloğa çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10fda-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="10fda-132">Geçerli katalog içe aktarma şablonunu (XSD dosyası) indirin.</span><span class="sxs-lookup"><span data-stu-id="10fda-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="10fda-133">**Katalog güncelleştir** sayfasında **Eylem Bölmesinde** bulunan **Kataloglar** sekmesindeki **İlgili bilgiler** grubunda **Katalog şablonu oluştur**'a tıklayın ve **Tedarik kategorisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="10fda-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="10fda-134">**Tedarik kategori** seçeneğiyle, satıcının ürünler sağlamak için yetkilendirildiği tedarik kataloglarını içeren bir katalog şablonu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10fda-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="10fda-135">**Farklı kaydet** iletişim kutusunda, katalog dosyası şablonunu kaydetmek istediğiniz konumu seçin ve dosyayı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="10fda-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="10fda-136">Daha fazla bilgi ve örnekler için bu blog gönderisine bakın: [Dynamics AX'de satıcı katalogları](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="10fda-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
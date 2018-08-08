---
title: "Field Service için Microsoft Dynamics 365 ile tümleştirme"
description: "Bu konu Field Service için Microsoft Dynamics 365 ile tümleştirmeye genel bakış sağlar."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
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
ms.openlocfilehash: 2ef7f71dc6d58108b498ed89e9175ff2ce900cda
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="03f0f-103">Field Service için Microsoft Dynamics 365 ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="03f0f-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="03f0f-104">Microsoft Dynamics 365 for Finance and Operations Finance and Operations ile Microsoft Dynamics 365 for Field Service arasında iş süreçlerinin eşitlenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="03f0f-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="03f0f-105">Tümleştirme senaryoları iş süreçlerinin eşitlenmesine olanak tanımak için genişletilebilir Veri tümleştirici şablonları ve Common Data Service (CDS) kullanılarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="03f0f-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="03f0f-106">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="03f0f-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="03f0f-107">Field Service and Finance ile Operations arasındaki tümleştirmenin birinci aşaması Field Service'taki iş emirlerinin ve sözleşmelerin Finance and Operations'da faturalandırılmasını sağlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="03f0f-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="03f0f-108">Desteklenen akış Field Service'da başlar; iş emirlerinden alınan bilgiler Finance and Operations'a satış siparişleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="03f0f-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="03f0f-109">Finance and Operations'da satış siparişleri fatura belgeleri oluşturmak üzere faturalandırılır.</span><span class="sxs-lookup"><span data-stu-id="03f0f-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="03f0f-110">Ayrıca, Field Service sözleşme faturalarındaki bilgiler Finance and Operations'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="03f0f-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="03f0f-111">Microsoft Dynamics 365 Veri tümleştirici verileri özelleştirilebilir projeleri kullanarak eşitler.</span><span class="sxs-lookup"><span data-stu-id="03f0f-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="03f0f-112">Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel gereksinimleri karşılamak üzere eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="03f0f-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="03f0f-113">Field Service ile Finance and Operations arasındaki tümleştirmenin birinci aşaması aşağıdaki öğelerin eşitlenmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="03f0f-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="03f0f-114">Finance and Operations'taki ürünler ile Field Service'da Ürün Türü bilgisi içeren ürünler</span><span class="sxs-lookup"><span data-stu-id="03f0f-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="03f0f-115">Field Service'taki iş emirleri ile Finance and Operations'taki satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="03f0f-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="03f0f-116">Field Service'taki faturalar ile Finance and Operations'taki serbest metin faturaları</span><span class="sxs-lookup"><span data-stu-id="03f0f-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="03f0f-117">Bir iş emrini Field Service ile Finance and Operations arasında nasıl eşitleyeceğinize ilişkin bir örnek görmek için YouTube'daki kısa videoyu izleyin: [Dynamics 365 for Field Service ile Finance and Operations arasında bir iş emrini eşitleme](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span><span class="sxs-lookup"><span data-stu-id="03f0f-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [Synchronize a work order between Dynamics 365 for Field Service and Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).</span></span>

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="03f0f-118">Finance and Operations için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="03f0f-118">System requirements for Finance and Operations</span></span>
<span data-ttu-id="03f0f-119">Field Service tümleştirmesi aşağıdaki sürümleri destekler:</span><span class="sxs-lookup"><span data-stu-id="03f0f-119">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="03f0f-120">Dynamics 365 for Finance and Operations sürüm 8.0 (Nisan 2018) veya üstü</span><span class="sxs-lookup"><span data-stu-id="03f0f-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="03f0f-121">Dynamics 365 for Finance and Operations sürüm 8.0 (Nisan 2018) Nisan 2018'de yayımlanmıştır ve Platform Güncelleştirmesi 15 (7.0.4841.35234) ile birlikte 8.0.30.8020 uygulama derleme numarasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="03f0f-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="03f0f-122">Field Service için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="03f0f-122">System requirements for Field Service</span></span>
<span data-ttu-id="03f0f-123">Field Service tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="03f0f-123">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="03f0f-124">Microsoft Dynamics 365 for Field Service 9.0 veya üstü</span><span class="sxs-lookup"><span data-stu-id="03f0f-124">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="03f0f-125">Dynamics 365 for Field Service sürüm 1612 (9.0.1.733) (DB 9.0.1.733) çevrimiçi veya üstü sürüm.</span><span class="sxs-lookup"><span data-stu-id="03f0f-125">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="03f0f-126">Dynamics 365, sürüm 1.15.0.1 veya üstü sürüm için Müşteri Adayından Nakde (P2C) çözümü.</span><span class="sxs-lookup"><span data-stu-id="03f0f-126">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="03f0f-127">Çözüm [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)'tan indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="03f0f-127">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="03f0f-128">Dynamics 365, sürüm 1.0.0.0 veya üstü sürüm için tümleştirme çözümü.</span><span class="sxs-lookup"><span data-stu-id="03f0f-128">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="03f0f-129">Çözüm [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration)'tan indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="03f0f-129">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>


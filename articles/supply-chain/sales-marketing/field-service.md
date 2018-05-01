---
title: "Field Service için Microsoft Dynamics 365 ile tümleştirme"
description: "Bu konu Field Service için Microsoft Dynamics 365 ile tümleştirmeye genel bakış sağlar."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: tr-tr
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="0f9f5-103">Field Service için Microsoft Dynamics 365 ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="0f9f5-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0f9f5-104">Microsoft Dynamics 365 for Finance and Operations Finance and Operations ile Microsoft Dynamics 365 for Field Service arasında iş süreçlerinin eşitlenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="0f9f5-105">Tümleştirme senaryoları iş süreçlerinin eşitlenmesine olanak tanımak için genişletilebilir Veri tümleştirici şablonları ve Common Data Service (CDS) kullanılarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="0f9f5-106">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="0f9f5-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="0f9f5-107">Field Service and Finance ile Operations arasındaki tümleştirmenin birinci aşaması Field Service'taki iş emirlerinin ve sözleşmelerin Finance and Operations'da faturalandırılmasını sağlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="0f9f5-108">Desteklenen akış Field Service'da başlar; iş emirlerinden alınan bilgiler Finance and Operations'a satış siparişleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="0f9f5-109">Finance and Operations'da satış siparişleri fatura belgeleri oluşturmak üzere faturalandırılır.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="0f9f5-110">Ayrıca, Field Service sözleşme faturalarındaki bilgiler Finance and Operations'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="0f9f5-111">Microsoft Dynamics 365 Veri tümleştirici verileri özelleştirilebilir projeleri kullanarak eşitler.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="0f9f5-112">Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel gereksinimleri karşılamak üzere eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="0f9f5-113">Field Service ile Finance and Operations arasındaki tümleştirmenin birinci aşaması aşağıdaki öğelerin eşitlenmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="0f9f5-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="0f9f5-114">Finance and Operations'taki ürünler ile Field Service'da Ürün Türü bilgisi içeren ürünler</span><span class="sxs-lookup"><span data-stu-id="0f9f5-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="0f9f5-115">Field Service'taki iş emirleri ile Finance and Operations'taki satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="0f9f5-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="0f9f5-116">Field Service'taki faturalar ile Finance and Operations'taki serbest metin faturaları</span><span class="sxs-lookup"><span data-stu-id="0f9f5-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="0f9f5-117">Finance and Operations için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="0f9f5-117">System requirements for Finance and Operations</span></span>
<span data-ttu-id="0f9f5-118">Field Service tümleştirmesi aşağıdaki sürümleri destekler:</span><span class="sxs-lookup"><span data-stu-id="0f9f5-118">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="0f9f5-119">Dynamics 365 for Finance and Operations sürüm 8.0 (Nisan 2018) veya üstü</span><span class="sxs-lookup"><span data-stu-id="0f9f5-119">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="0f9f5-120">Dynamics 365 for Finance and Operations sürüm 8.0 (Nisan 2018) Nisan 2018'de yayımlanmıştır ve Platform Güncelleştirmesi 15 (7.0.4841.35234) ile birlikte 8.0.30.8020 uygulama derleme numarasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="0f9f5-121">Field Service için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="0f9f5-121">System requirements for Field Service</span></span>
<span data-ttu-id="0f9f5-122">Field Service tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="0f9f5-122">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="0f9f5-123">Microsoft Dynamics 365 for Field Service 9.0 veya üstü</span><span class="sxs-lookup"><span data-stu-id="0f9f5-123">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="0f9f5-124">Dynamics 365 for Field Service sürüm 1612 (9.0.1.733) (DB 9.0.1.733) çevrimiçi veya üstü sürüm.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-124">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="0f9f5-125">Dynamics 365, sürüm 1.15.0.1 veya üstü sürüm için Müşteri Adayından Nakde (P2C) çözümü.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-125">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="0f9f5-126">Çözüm [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)'tan indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-126">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="0f9f5-127">Dynamics 365, sürüm 1.0.0.0 veya üstü sürüm için tümleştirme çözümü.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-127">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="0f9f5-128">Çözüm AppSource'tan indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="0f9f5-128">The solution is available for download from AppSource.</span></span> <span data-ttu-id="0f9f5-129">**(SÜRÜM BEKLEMEDE)**</span><span class="sxs-lookup"><span data-stu-id="0f9f5-129">**(PENDING RELEASE)**</span></span>

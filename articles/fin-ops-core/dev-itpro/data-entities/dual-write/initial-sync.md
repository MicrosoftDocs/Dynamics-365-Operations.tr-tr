---
title: Finance and Operations uygulamaların ve Common Data Service'in  ilk eşitlenmesi için yürütme emri
description: Bu konu, ilk verileri oluşturmak için izlemeniz gereken eşitleme sırasını belirtir.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020060"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="91fbf-103">Finance and Operations uygulamaların ve Common Data Service'in  ilk eşitlenmesi için yürütme emri</span><span class="sxs-lookup"><span data-stu-id="91fbf-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="91fbf-104">Veri tümleştirmesini kullanmadan önce, müşteriler, satıcılar ve kişiler için gereken ilk verileri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="91fbf-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="91fbf-105">Örneğin, yeni bir **Satıcı grubu** maddesi oluşturmak ve **Ödeme şartları** değerini **Net30**olarak ayarlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="91fbf-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="91fbf-106">Bu durumda, **Satıcı grubu** maddesini oluşturmaya çalışmadan önce **Net30**'un uygulama ve Common Data Service'in her ikisinde de bulunduğundan emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="91fbf-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="91fbf-107">(Gelecekte Microsoft İlk Eşitleme denilen bir çift yazma platformu işlevselliği yayımlayacak. uygulama ve Common Data Service arasında tek seferlik veri eşitlemesi ve çift yazma kurulumunun bir parçası olacak.)</span><span class="sxs-lookup"><span data-stu-id="91fbf-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="91fbf-108">Microsoft **Ödeme Şartları** (Ödeme Koşulları) dahil olmak üzere tüm referans verileri için bir çift yazma haritası yayımlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="91fbf-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="91fbf-109">Bir sistemde ilk veri zaten varsa bir kayıtta küçük bir güncelleştirme işlemi bu kayıtta çift yazmayı tetikleyebilir.</span><span class="sxs-lookup"><span data-stu-id="91fbf-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="91fbf-110">Aşağıdaki öncelik sırasını izlemeniz ve başlangıç verilerinin hem uygulamada hem de Common Data Service'te kullanılabilir olduğundan emin olmanız gerekir .</span><span class="sxs-lookup"><span data-stu-id="91fbf-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="91fbf-111">Satıcı</span><span class="sxs-lookup"><span data-stu-id="91fbf-111">Vendor</span></span>

<span data-ttu-id="91fbf-112">İşte **Satıcı** varlığı için yürütme sırası:</span><span class="sxs-lookup"><span data-stu-id="91fbf-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="91fbf-113">Satıcı grubu</span><span class="sxs-lookup"><span data-stu-id="91fbf-113">Vendor group</span></span>

    1. <span data-ttu-id="91fbf-114">Ödeme koşulları</span><span class="sxs-lookup"><span data-stu-id="91fbf-114">Terms of payment</span></span>

        1. <span data-ttu-id="91fbf-115">Ödeme günü ve satırlar</span><span class="sxs-lookup"><span data-stu-id="91fbf-115">Payment day and lines</span></span>
        2. <span data-ttu-id="91fbf-116">Ödeme planı</span><span class="sxs-lookup"><span data-stu-id="91fbf-116">Payment schedule</span></span>

2. <span data-ttu-id="91fbf-117">Satıcı ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="91fbf-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="91fbf-118">Müşteri (Kuruluş)</span><span class="sxs-lookup"><span data-stu-id="91fbf-118">Customer (Organization)</span></span>

<span data-ttu-id="91fbf-119">İşte **Müşteri** varlığı için yürütme sırası:</span><span class="sxs-lookup"><span data-stu-id="91fbf-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="91fbf-120">Müşteri grubu</span><span class="sxs-lookup"><span data-stu-id="91fbf-120">Customer group</span></span>

    1. <span data-ttu-id="91fbf-121">Ödeme koşulları</span><span class="sxs-lookup"><span data-stu-id="91fbf-121">Terms of payment</span></span>

        1. <span data-ttu-id="91fbf-122">Ödeme günü ve satırlar</span><span class="sxs-lookup"><span data-stu-id="91fbf-122">Payment day and lines</span></span>
        2. <span data-ttu-id="91fbf-123">Ödeme</span><span class="sxs-lookup"><span data-stu-id="91fbf-123">Payment</span></span> 

2. <span data-ttu-id="91fbf-124">Müşteri ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="91fbf-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="91fbf-125">İlgili Kişi (Kişi)</span><span class="sxs-lookup"><span data-stu-id="91fbf-125">Contact (Person)</span></span>

<span data-ttu-id="91fbf-126">İşte **İlgili kişi** varlığı için yürütme sırası:</span><span class="sxs-lookup"><span data-stu-id="91fbf-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="91fbf-127">Müşteri</span><span class="sxs-lookup"><span data-stu-id="91fbf-127">Customer</span></span>
2. <span data-ttu-id="91fbf-128">Satıcı</span><span class="sxs-lookup"><span data-stu-id="91fbf-128">Vendor</span></span>

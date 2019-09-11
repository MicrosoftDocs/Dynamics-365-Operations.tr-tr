---
title: Finance and Operations ve Common Data Service'ın ilk eşzamanlı yürütülmesi için yürütme emri.
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
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873140"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="61c54-103">Finance and Operations ve Common Data Service'ın ilk eşzamanlı yürütülmesi için yürütme emri.</span><span class="sxs-lookup"><span data-stu-id="61c54-103">Execution order for initial synchronization of Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="61c54-104">Veri tümleştirmesini kullanmadan önce, müşteriler, satıcılar ve kişiler için gereken ilk verileri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="61c54-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="61c54-105">Örneğin, yeni bir **Satıcı grubu** maddesi oluşturmak ve **Ödeme şartları** değerini **Net30**olarak ayarlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="61c54-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="61c54-106">Bu durumda, **Satıcı grup** maddesini oluşturmaya çalışmadan önce **Net30**'un Microsoft Dynamics 365 for Finance and Operations ve Common Data Service'in her ikisinde de bulunduğundan emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="61c54-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both Microsoft Dynamics 365 for Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="61c54-107">(Gelecekte Microsoft İlk Eşitleme denilen bir çift yazma platformu işlevselliği yayımlayacak. Finance and Operations ve Common Data Service arasında tek seferlik veri eşitlemesi ve çift yazma kurulumunun bir parçası olacak.)</span><span class="sxs-lookup"><span data-stu-id="61c54-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="61c54-108">Microsoft **Ödeme Şartları** (Ödeme Koşulları) dahil olmak üzere tüm referans verileri için bir çift yazma haritası yayımlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="61c54-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="61c54-109">Bir sistemde ilk veri zaten varsa bir kayıtta küçük bir güncelleştirme işlemi bu kayıtta çift yazmayı tetikleyebilir.</span><span class="sxs-lookup"><span data-stu-id="61c54-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="61c54-110">Aşağıdaki öncelik sırasını izlemeniz ve başlangıç verilerinin hem Finance and Operations'ta hem de Common Data Service'te kullanılabilir olduğundan emin olmanız gerekir .</span><span class="sxs-lookup"><span data-stu-id="61c54-110">You must follow the following order of precedence and make sure that the initial data is available in both Finance and Operations and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="61c54-111">Satıcı</span><span class="sxs-lookup"><span data-stu-id="61c54-111">Vendor</span></span>

<span data-ttu-id="61c54-112">İşte **Satıcı** varlığı için yürütme sırası:</span><span class="sxs-lookup"><span data-stu-id="61c54-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="61c54-113">Satıcı grubu</span><span class="sxs-lookup"><span data-stu-id="61c54-113">Vendor group</span></span>

    1. <span data-ttu-id="61c54-114">Ödeme koşulları</span><span class="sxs-lookup"><span data-stu-id="61c54-114">Terms of payment</span></span>

        1. <span data-ttu-id="61c54-115">Ödeme günü ve satırlar</span><span class="sxs-lookup"><span data-stu-id="61c54-115">Payment day and lines</span></span>
        2. <span data-ttu-id="61c54-116">Ödeme planı</span><span class="sxs-lookup"><span data-stu-id="61c54-116">Payment schedule</span></span>

2. <span data-ttu-id="61c54-117">Satıcı ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="61c54-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="61c54-118">Müşteri (Kuruluş)</span><span class="sxs-lookup"><span data-stu-id="61c54-118">Customer (Organization)</span></span>

<span data-ttu-id="61c54-119">İşte **Müşteri** varlığı için yürütme sırası:</span><span class="sxs-lookup"><span data-stu-id="61c54-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="61c54-120">Müşteri grubu</span><span class="sxs-lookup"><span data-stu-id="61c54-120">Customer group</span></span>

    1. <span data-ttu-id="61c54-121">Ödeme koşulları</span><span class="sxs-lookup"><span data-stu-id="61c54-121">Terms of payment</span></span>

        1. <span data-ttu-id="61c54-122">Ödeme günü ve satırlar</span><span class="sxs-lookup"><span data-stu-id="61c54-122">Payment day and lines</span></span>
        2. <span data-ttu-id="61c54-123">Ödeme</span><span class="sxs-lookup"><span data-stu-id="61c54-123">Payment</span></span> 

2. <span data-ttu-id="61c54-124">Müşteri ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="61c54-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="61c54-125">İlgili Kişi (Kişi)</span><span class="sxs-lookup"><span data-stu-id="61c54-125">Contact (Person)</span></span>

<span data-ttu-id="61c54-126">İşte **İlgili kişi** varlığı için yürütme sırası:</span><span class="sxs-lookup"><span data-stu-id="61c54-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="61c54-127">Müşteri</span><span class="sxs-lookup"><span data-stu-id="61c54-127">Customer</span></span>
2. <span data-ttu-id="61c54-128">Satıcı</span><span class="sxs-lookup"><span data-stu-id="61c54-128">Vendor</span></span>

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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797310"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="948cf-103">Finance and Operations ve Common Data Service'ın ilk eşzamanlı yürütülmesi için yürütme emri.</span><span class="sxs-lookup"><span data-stu-id="948cf-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="948cf-104">Veri tümleştirmesini kullanmadan önce, müşteriler, satıcılar ve kişiler için gereken ilk verileri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="948cf-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="948cf-105">Örneğin yeni bir **Satıcı grubu** öğesi oluşturmak ve **Ödeme koşulları**'nı **Net30**olarak ayarlamak istiyorsanız **Satıcı grubu** öğesini oluşturmaya çalışmadan önce **Net30**'un hem Finance and Operations'ta hem de Common Data Service'te mevcut olduğundan emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="948cf-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="948cf-106">(Gelecekte **İlk Eşitleme** denilen bir çift yazma platformu işlevselliği yayımlayacağız. Finance and Operations ve Common Data Service arasında tek seferlik veri eşitlemesi ve çift yazma kurulumunun bir parçası olacak.)</span><span class="sxs-lookup"><span data-stu-id="948cf-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="948cf-107">İpuçları: **Ödeme Şartları** (Ödeme Koşulları) dahil olmak üzere tüm referans verileri için bir çift yazma haritası yayınlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="948cf-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="948cf-108">Bir sistemde ilk veri zaten varsa bir kayıtta küçük bir güncelleştirme işlemi bu kayıtta çift yazmayı tetikleyebilir.</span><span class="sxs-lookup"><span data-stu-id="948cf-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="948cf-109">Aşağıdaki öncelik sırasını izlemeniz ve başlangıç verilerinin hem Finance and Operations'ta hem de Common Data Service'te kullanılabilir olduğundan emin olmanız gerekir .</span><span class="sxs-lookup"><span data-stu-id="948cf-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="948cf-110">Satıcı</span><span class="sxs-lookup"><span data-stu-id="948cf-110">Vendor</span></span>

<span data-ttu-id="948cf-111">Satıcı için yürütme sırası şudur:</span><span class="sxs-lookup"><span data-stu-id="948cf-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="948cf-112">Müşteri (Kuruluş)</span><span class="sxs-lookup"><span data-stu-id="948cf-112">Customer (Organization)</span></span>

<span data-ttu-id="948cf-113">Müşteri için yürütme sırası şudur:</span><span class="sxs-lookup"><span data-stu-id="948cf-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="948cf-114">İlgili Kişi (Kişi)</span><span class="sxs-lookup"><span data-stu-id="948cf-114">Contact (Person)</span></span>

<span data-ttu-id="948cf-115">İlgili kişi için yürütme sırası şudur:</span><span class="sxs-lookup"><span data-stu-id="948cf-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```

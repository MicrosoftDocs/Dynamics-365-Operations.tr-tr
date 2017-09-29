---
title: "Açık bir iş listesinde sistem gruplama"
description: "Bu konu, mobil cihazda açık iş listesine nasıl filtre uygulanacağını açıklar."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="a016e-103">Açık bir iş listesinde sistem gruplama</span><span class="sxs-lookup"><span data-stu-id="a016e-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a016e-104">Sistem gruplandırma alanını kullanarak, mobil cihaz menü öğesini düzenlemek zorunda kalmadan bir açık iş listesini filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a016e-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="a016e-105">Bu geçerli olduğunda, sistem gruplandırma, tek bir iş başlığı alanındaki bir iş listesini filtrelemek üzere çalışır.</span><span class="sxs-lookup"><span data-stu-id="a016e-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="a016e-106">Sistem gruplandırmayı satır düzeyindeki alanlarda filtreleme yapmak için kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a016e-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="a016e-107">Açık bir iş listesinde sistem gruplandırmayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="a016e-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="a016e-108">Açık bir iş listesinde sistem gruplandırmayı ayarlamak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a016e-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="a016e-109">Bir mobil cihaz menü öğesinden **Mod: Dolaylı** ve **Faaliyet Kodu: Açık iş listesini görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a016e-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="a016e-110">Aşağıdaki seçenekler kullanılabilir olur.</span><span class="sxs-lookup"><span data-stu-id="a016e-110">The following options become available.</span></span> <span data-ttu-id="a016e-111">Bu seçenekler bir açık iş listesinde sistem gruplandırması için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a016e-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="a016e-112">Seçenek</span><span class="sxs-lookup"><span data-stu-id="a016e-112">Option</span></span>        | <span data-ttu-id="a016e-113">Açıklama</span><span class="sxs-lookup"><span data-stu-id="a016e-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="a016e-114">Sistem gruplandırmaya izin ver</span><span class="sxs-lookup"><span data-stu-id="a016e-114">Allow system grouping</span></span>   | <span data-ttu-id="a016e-115">Seçili iş listesi menü öğesi için sistem gruplandırmayı etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="a016e-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="a016e-116">Sistem gruplandırma alanı</span><span class="sxs-lookup"><span data-stu-id="a016e-116">System grouping field</span></span>   | <span data-ttu-id="a016e-117">Yalnızca **Sistem işine izin ver** **Evet** olarak ayarlandığında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a016e-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="a016e-118">Çalışanlar için çekme işinin nasıl gruplanacağını belirleyen bu alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="a016e-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="a016e-119">Örneğin, **ShipmentId** alanını seçerseniz çalışan çekme işini gruplandırmak için sevkıyat kodunu tarayacaktır.</span><span class="sxs-lookup"><span data-stu-id="a016e-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="a016e-120">Böylece sevkıyat için tüm iş çalışana atanır.</span><span class="sxs-lookup"><span data-stu-id="a016e-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="a016e-121">Bu alan, sistem tarafından gruplanan mevcut işi kullanmak için bir menü öğesi oluşturmanızı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="a016e-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="a016e-122">Çalışanı neyi taraması gerektiği hakkında bilgilendirmek için **Sistem gruplandırma etiketi** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="a016e-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="a016e-123">Sistem gruplandırma etiketi</span><span class="sxs-lookup"><span data-stu-id="a016e-123">System grouping label</span></span>   | <span data-ttu-id="a016e-124">Yalnızca **Sistem işine izin ver** **Evet** olarak ayarlandığında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a016e-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="a016e-125">Çalışan için çekme işi gruplandırma sırasında neyin taranacağına ilişkin bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="a016e-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="a016e-126">Örneğin çekme işini sevkiyata göre gruplandırmak için **ShipmentId** alanını kullanıyorsanız alana Sevkiyat kodu girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a016e-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="a016e-127">Bu alan, sistem tarafından gruplanan mevcut işi kullanmak için bir menü öğesi oluşturmanızı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="a016e-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="a016e-128">**Sistem gruplandırma** alanında alanı nasıl gruplandıracağınızı da seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="a016e-128">You must also select the field to group by in the **System grouping** field.</span></span>|


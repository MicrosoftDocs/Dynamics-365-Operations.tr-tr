---
title: Servis nesnesi ilişkileri oluşturma
description: Bu konu bir servis sözleşmesi veya servis siparişi için servis nesnesi ilişkileri oluşturmayı açıklar.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05d770234beb486eb3a8181b160967c802c15e8f
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813167"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="1081b-103">Servis nesnesi ilişkileri oluşturma</span><span class="sxs-lookup"><span data-stu-id="1081b-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1081b-104">Bu konu bir servis sözleşmesi veya servis siparişi için servis nesnesi ilişkileri oluşturmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="1081b-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="1081b-105">Bir servis nesnesi ilişkisi oluşturduğunuzda, servis nesnesini servis sözleşmesi veya servis siparişiyle ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1081b-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="1081b-106">Müşteri servis nesnesi olan bir madde için servis talep ettiğinde, servis nesnesini servis nesnesi ilişkileri listesinden seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1081b-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="1081b-107">Servis sözleşmesi için servis nesnesi ilişkisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1081b-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="1081b-108">Bir servis sözleşmesi için servis nesnesi ilişkisi oluşturmak üzere aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="1081b-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="1081b-109">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1081b-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="1081b-110">**Servis sözleşmeleri** listesinde var olan bir servis sözleşmesini seçin veya yeni bir servis sözleşmesi oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1081b-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="1081b-111">**Servis sözleşmeleri** formunda, **Eylem Bölmesi**'ndeki **Servis sözleşmesi** sekmesinde, **İlişkiler** grubunda **Servis nesneleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1081b-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="1081b-112">**Servis nesneleri** formunda **Yeni**'ye tıklayın ve bu servis sözleşmesi için servis nesnesi seçin.</span><span class="sxs-lookup"><span data-stu-id="1081b-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="1081b-113">Servis sözleşmesine bir şablon ürün reçetesi (BOM) eklemek için, **İşlevler** seçeneğine tıklayın ve **Şablon ürün reçetesini ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1081b-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="1081b-114">**Şablon ürün reçetesi** formundaki **Şablon Ürün Reçetesi** alanında bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="1081b-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="1081b-115">Servis siparişi için servis nesnesi ilişkisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1081b-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="1081b-116">Bir servis siparişi için servis nesnesi ilişkisi oluşturmak üzere aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="1081b-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="1081b-117">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1081b-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="1081b-118">**Servis siparişleri** listesinden var olan bir servis siparişini seçin veya yeni bir servis siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1081b-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="1081b-119">**Servis siparişleri** formunda, **Eylem Bölmesi**'ndeki **Servis siparişi** sekmesinde, **İlişkiler** grubunda **Servis nesneleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1081b-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="1081b-120">**Servis nesneleri** formunda **Yeni**'ye tıklayın ve bu servis siparişi için servis nesnesi seçin.</span><span class="sxs-lookup"><span data-stu-id="1081b-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="1081b-121">Servis sözleşmesine bir şablon ürün reçetesi eklemek için, **İşlevler** seçeneğine tıklayın ve **Şablon ürün reçetesini ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1081b-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="1081b-122">**Şablon ürün reçetesi** formundaki **Şablon Ürün Reçetesi** alanında bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="1081b-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="1081b-123">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1081b-123">See also</span></span>

[<span data-ttu-id="1081b-124">Servis nesnelerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="1081b-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="1081b-125">Servis nesnesi ilişkileri</span><span class="sxs-lookup"><span data-stu-id="1081b-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="1081b-126">Şablon ürün reçeteleri</span><span class="sxs-lookup"><span data-stu-id="1081b-126">Template BOMs</span></span>](template-boms.md)

  



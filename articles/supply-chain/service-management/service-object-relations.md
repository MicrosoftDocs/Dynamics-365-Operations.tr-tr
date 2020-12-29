---
title: Servis nesnesi ilişkileri
description: Servis nesnesi ve servis sözleşmesi veya servis siparişi arasında servis nesnesi ilişkileri oluşturabilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b1b76dffc2751d51c2a25d831fab512b747c15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438987"
---
# <a name="service-object-relations"></a><span data-ttu-id="d709a-103">Servis nesnesi ilişkileri</span><span class="sxs-lookup"><span data-stu-id="d709a-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d709a-104">Servis nesnesi ve servis sözleşmesi veya servis siparişi arasında servis nesnesi ilişkileri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d709a-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="d709a-105">Bir ilişki oluşturduğunuzda servis nesnesini servis sözleşmesine veya servis siparişine iliştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d709a-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="d709a-106">İlişki oluşturulduktan sonra, servis nesnesini servis sözleşmesine veya servis siparişindeki herhangi bir satıra iliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d709a-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="d709a-107">Şablon Ürün Reçeteleri</span><span class="sxs-lookup"><span data-stu-id="d709a-107">Template BOMs</span></span>

<span data-ttu-id="d709a-108">Parça ilişkisi için bir şablon ürün reçetesi de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d709a-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="d709a-109">Şablon ürün reçetesi, servis uyguladığınız ürün reçetesidir.</span><span class="sxs-lookup"><span data-stu-id="d709a-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="d709a-110">Servis ziyareti sırasında servis nenesinin bileşen parçasını değiştirirseniz bu değişikliği Servis nesneleri formunu kullanarak servis ürün reçetesinde kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d709a-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="d709a-111">Örnek</span><span class="sxs-lookup"><span data-stu-id="d709a-111">Example</span></span>

<span data-ttu-id="d709a-112">Müşteri sitesinde iki asansör hizmeti için bir servis sözleşmesi oluşturuyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="d709a-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="d709a-113">Servis sözleşmesi, SAL-001 kimlik tanımlayıcı koduna sahiptir.</span><span class="sxs-lookup"><span data-stu-id="d709a-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="d709a-114">Asansörler, Servis nesneleri formunda EL-S/1000 ve EL-L/1000 nesneleri olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d709a-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="d709a-115">Servis nesnelerini (EL-S/1000 ve EL-L/1000) servis sözleşmesine iliştiriyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="d709a-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="d709a-116">Parçanın bileşen parçalarını değiştirdikçe servis kapsamındaki parça için ürün reçetesindeki değişiklikleri kaydetmek, böylece aşağıdaki tabloda açıklandığı gibi servis ürün reçetesini servis kapsamındaki parçaya iliştirmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d709a-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="d709a-117">Servis nesnesi</span><span class="sxs-lookup"><span data-stu-id="d709a-117">Service object</span></span> | <span data-ttu-id="d709a-118">İlişki – Servis sözleşmesi</span><span class="sxs-lookup"><span data-stu-id="d709a-118">Relation – Service agreement</span></span> | <span data-ttu-id="d709a-119">Servis ürün reçetesi</span><span class="sxs-lookup"><span data-stu-id="d709a-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="d709a-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-120">EL-S/1000</span></span>      | <span data-ttu-id="d709a-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="d709a-121">ID SAL-001</span></span>                   | <span data-ttu-id="d709a-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="d709a-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-123">EL-L/1000</span></span>      | <span data-ttu-id="d709a-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="d709a-124">ID SAL-001</span></span>                   | <span data-ttu-id="d709a-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="d709a-126">Bunlar sözleşme için servis nesnesi ilişkileri olduğundan, artık aşağıdaki tabloda gösterildiği gibi bu nesnelere servis sözleşmesi satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d709a-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="d709a-127">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="d709a-127">Transaction type</span></span> | <span data-ttu-id="d709a-128">Kategori</span><span class="sxs-lookup"><span data-stu-id="d709a-128">Category</span></span>           | <span data-ttu-id="d709a-129">Servis nesnesi</span><span class="sxs-lookup"><span data-stu-id="d709a-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="d709a-130">Saat</span><span class="sxs-lookup"><span data-stu-id="d709a-130">Hour</span></span>             | <span data-ttu-id="d709a-131">Denetleme</span><span class="sxs-lookup"><span data-stu-id="d709a-131">Inspection</span></span>         | <span data-ttu-id="d709a-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-132">EL-S/1000</span></span>      |
| <span data-ttu-id="d709a-133">Saat</span><span class="sxs-lookup"><span data-stu-id="d709a-133">Hour</span></span>             | <span data-ttu-id="d709a-134">Vites kutusu temizliği</span><span class="sxs-lookup"><span data-stu-id="d709a-134">Gear box cleaning</span></span>  | <span data-ttu-id="d709a-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-135">EL-S/1000</span></span>      |
| <span data-ttu-id="d709a-136">Madde</span><span class="sxs-lookup"><span data-stu-id="d709a-136">Item</span></span>             | <span data-ttu-id="d709a-137">Temizlik malzemeleri</span><span class="sxs-lookup"><span data-stu-id="d709a-137">Cleaning materials</span></span> | <span data-ttu-id="d709a-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-138">EL-S/1000</span></span>      |
| <span data-ttu-id="d709a-139">Saat</span><span class="sxs-lookup"><span data-stu-id="d709a-139">Hour</span></span>             | <span data-ttu-id="d709a-140">Denetleme</span><span class="sxs-lookup"><span data-stu-id="d709a-140">Inspection</span></span>         | <span data-ttu-id="d709a-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-141">EL-L/1000</span></span>      |
| <span data-ttu-id="d709a-142">Saat</span><span class="sxs-lookup"><span data-stu-id="d709a-142">Hour</span></span>             | <span data-ttu-id="d709a-143">Vites kutusu temizliği</span><span class="sxs-lookup"><span data-stu-id="d709a-143">Gearbox cleaning</span></span>   | <span data-ttu-id="d709a-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-144">EL-L/1000</span></span>      |
| <span data-ttu-id="d709a-145">Madde</span><span class="sxs-lookup"><span data-stu-id="d709a-145">Item</span></span>             | <span data-ttu-id="d709a-146">Temizlik malzemeleri</span><span class="sxs-lookup"><span data-stu-id="d709a-146">Cleaning materials</span></span> | <span data-ttu-id="d709a-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="d709a-147">EL-L/1000</span></span>      |

<span data-ttu-id="d709a-148">Bir servis ziyaretinde, EL-S/1000 asansörünün vitesi kutusunu temizlemeniz gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="d709a-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="d709a-149">Nesnenin bileşen parçasını değiştirmek için, geçerli servis sözleşmesinde ayarladığınız servis nesnesi ilişkisini kullanarak Ürün Reçetesi Tasarımcısı'na ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d709a-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="d709a-150">Servis kapsamındaki parça ilişkisini kullanarak Ürün Reçetesi Tasarımcısı'na erişme</span><span class="sxs-lookup"><span data-stu-id="d709a-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="d709a-151">Servis sözleşmeleri</span><span class="sxs-lookup"><span data-stu-id="d709a-151">Service agreements</span></span>
2. <span data-ttu-id="d709a-152">Servis sözleşmesi oluşturmak için servis sözleşmesine çift tıklayın veya Servis sözleşmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d709a-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="d709a-153">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d709a-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="d709a-154">Servis sözleşmesine bir şablon ürün reçetesi iliştirmek için Servis nesnelerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d709a-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="d709a-155">Şablon ürün reçetesini değiştirmek için Servis nesneleri formunda Tasarımcı'ya tıklayarak Tasarımcı'yı açın.</span><span class="sxs-lookup"><span data-stu-id="d709a-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="d709a-156">Otomatik olarak oluşturulan servis siparişleri</span><span class="sxs-lookup"><span data-stu-id="d709a-156">Automatically created service orders</span></span>

<span data-ttu-id="d709a-157">Servis sözleşmesi için otomatik olarak servis siparişleri oluşturursanız sözleşmedeki servis nesnesi ilişkileri de servis siparişlerinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d709a-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 913b3c30bf972de7cc3dde73280e4f2f2be38507
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974347"
---
# <a name="service-object-relations"></a><span data-ttu-id="826e5-103">Servis nesnesi ilişkileri</span><span class="sxs-lookup"><span data-stu-id="826e5-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="826e5-104">Servis nesnesi ve servis sözleşmesi veya servis siparişi arasında servis nesnesi ilişkileri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="826e5-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="826e5-105">Bir ilişki oluşturduğunuzda servis nesnesini servis sözleşmesine veya servis siparişine iliştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="826e5-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="826e5-106">İlişki oluşturulduktan sonra, servis nesnesini servis sözleşmesine veya servis siparişindeki herhangi bir satıra iliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="826e5-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="826e5-107">Şablon Ürün Reçeteleri</span><span class="sxs-lookup"><span data-stu-id="826e5-107">Template BOMs</span></span>

<span data-ttu-id="826e5-108">Parça ilişkisi için bir şablon ürün reçetesi de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="826e5-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="826e5-109">Şablon ürün reçetesi, servis uyguladığınız ürün reçetesidir.</span><span class="sxs-lookup"><span data-stu-id="826e5-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="826e5-110">Servis ziyareti sırasında servis nenesinin bileşen parçasını değiştirirseniz bu değişikliği Servis nesneleri formunu kullanarak servis ürün reçetesinde kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="826e5-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="826e5-111">Örnek</span><span class="sxs-lookup"><span data-stu-id="826e5-111">Example</span></span>

<span data-ttu-id="826e5-112">Müşteri sitesinde iki asansör hizmeti için bir servis sözleşmesi oluşturuyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="826e5-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="826e5-113">Servis sözleşmesi, SAL-001 kimlik tanımlayıcı koduna sahiptir.</span><span class="sxs-lookup"><span data-stu-id="826e5-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="826e5-114">Asansörler, Servis nesneleri formunda EL-S/1000 ve EL-L/1000 nesneleri olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="826e5-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="826e5-115">Servis nesnelerini (EL-S/1000 ve EL-L/1000) servis sözleşmesine iliştiriyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="826e5-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="826e5-116">Parçanın bileşen parçalarını değiştirdikçe servis kapsamındaki parça için ürün reçetesindeki değişiklikleri kaydetmek, böylece aşağıdaki tabloda açıklandığı gibi servis ürün reçetesini servis kapsamındaki parçaya iliştirmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="826e5-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="826e5-117">Servis nesnesi</span><span class="sxs-lookup"><span data-stu-id="826e5-117">Service object</span></span> | <span data-ttu-id="826e5-118">İlişki – Servis sözleşmesi</span><span class="sxs-lookup"><span data-stu-id="826e5-118">Relation – Service agreement</span></span> | <span data-ttu-id="826e5-119">Servis ürün reçetesi</span><span class="sxs-lookup"><span data-stu-id="826e5-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="826e5-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-120">EL-S/1000</span></span>      | <span data-ttu-id="826e5-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="826e5-121">ID SAL-001</span></span>                   | <span data-ttu-id="826e5-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="826e5-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-123">EL-L/1000</span></span>      | <span data-ttu-id="826e5-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="826e5-124">ID SAL-001</span></span>                   | <span data-ttu-id="826e5-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="826e5-126">Bunlar sözleşme için servis nesnesi ilişkileri olduğundan, artık aşağıdaki tabloda gösterildiği gibi bu nesnelere servis sözleşmesi satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="826e5-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="826e5-127">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="826e5-127">Transaction type</span></span> | <span data-ttu-id="826e5-128">Kategori</span><span class="sxs-lookup"><span data-stu-id="826e5-128">Category</span></span>           | <span data-ttu-id="826e5-129">Servis nesnesi</span><span class="sxs-lookup"><span data-stu-id="826e5-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="826e5-130">Saat</span><span class="sxs-lookup"><span data-stu-id="826e5-130">Hour</span></span>             | <span data-ttu-id="826e5-131">Denetleme</span><span class="sxs-lookup"><span data-stu-id="826e5-131">Inspection</span></span>         | <span data-ttu-id="826e5-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-132">EL-S/1000</span></span>      |
| <span data-ttu-id="826e5-133">Saat</span><span class="sxs-lookup"><span data-stu-id="826e5-133">Hour</span></span>             | <span data-ttu-id="826e5-134">Vites kutusu temizliği</span><span class="sxs-lookup"><span data-stu-id="826e5-134">Gear box cleaning</span></span>  | <span data-ttu-id="826e5-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-135">EL-S/1000</span></span>      |
| <span data-ttu-id="826e5-136">Madde</span><span class="sxs-lookup"><span data-stu-id="826e5-136">Item</span></span>             | <span data-ttu-id="826e5-137">Temizlik malzemeleri</span><span class="sxs-lookup"><span data-stu-id="826e5-137">Cleaning materials</span></span> | <span data-ttu-id="826e5-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-138">EL-S/1000</span></span>      |
| <span data-ttu-id="826e5-139">Saat</span><span class="sxs-lookup"><span data-stu-id="826e5-139">Hour</span></span>             | <span data-ttu-id="826e5-140">Denetleme</span><span class="sxs-lookup"><span data-stu-id="826e5-140">Inspection</span></span>         | <span data-ttu-id="826e5-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-141">EL-L/1000</span></span>      |
| <span data-ttu-id="826e5-142">Saat</span><span class="sxs-lookup"><span data-stu-id="826e5-142">Hour</span></span>             | <span data-ttu-id="826e5-143">Vites kutusu temizliği</span><span class="sxs-lookup"><span data-stu-id="826e5-143">Gearbox cleaning</span></span>   | <span data-ttu-id="826e5-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-144">EL-L/1000</span></span>      |
| <span data-ttu-id="826e5-145">Madde</span><span class="sxs-lookup"><span data-stu-id="826e5-145">Item</span></span>             | <span data-ttu-id="826e5-146">Temizlik malzemeleri</span><span class="sxs-lookup"><span data-stu-id="826e5-146">Cleaning materials</span></span> | <span data-ttu-id="826e5-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="826e5-147">EL-L/1000</span></span>      |

<span data-ttu-id="826e5-148">Bir servis ziyaretinde, EL-S/1000 asansörünün vitesi kutusunu temizlemeniz gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="826e5-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="826e5-149">Nesnenin bileşen parçasını değiştirmek için, geçerli servis sözleşmesinde ayarladığınız servis nesnesi ilişkisini kullanarak Ürün Reçetesi Tasarımcısı'na ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="826e5-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="826e5-150">Servis kapsamındaki parça ilişkisini kullanarak Ürün Reçetesi Tasarımcısı'na erişme</span><span class="sxs-lookup"><span data-stu-id="826e5-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="826e5-151">Servis sözleşmeleri</span><span class="sxs-lookup"><span data-stu-id="826e5-151">Service agreements</span></span>
2. <span data-ttu-id="826e5-152">Servis sözleşmesi oluşturmak için servis sözleşmesine çift tıklayın veya Servis sözleşmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="826e5-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="826e5-153">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="826e5-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="826e5-154">Servis sözleşmesine bir şablon ürün reçetesi iliştirmek için Servis nesnelerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="826e5-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="826e5-155">Şablon ürün reçetesini değiştirmek için Servis nesneleri formunda Tasarımcı'ya tıklayarak Tasarımcı'yı açın.</span><span class="sxs-lookup"><span data-stu-id="826e5-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="826e5-156">Otomatik olarak oluşturulan servis siparişleri</span><span class="sxs-lookup"><span data-stu-id="826e5-156">Automatically created service orders</span></span>

<span data-ttu-id="826e5-157">Servis sözleşmesi için otomatik olarak servis siparişleri oluşturursanız sözleşmedeki servis nesnesi ilişkileri de servis siparişlerinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="826e5-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


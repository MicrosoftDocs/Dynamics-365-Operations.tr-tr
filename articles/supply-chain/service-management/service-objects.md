---
title: Servis nesneleri
description: "Servis nesneleri, üzerinde servis gerçekleştirebileceğiniz müşteri kıymetleri ve ürünleridir."
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5641077de84b6702d2c5621edef74783f2f104fd
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="service-objects"></a><span data-ttu-id="a34ca-103">Servis nesneleri</span><span class="sxs-lookup"><span data-stu-id="a34ca-103">Service objects</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a34ca-104">Servis nesneleri, üzerinde servis gerçekleştirebileceğiniz müşteri kıymetleri ve ürünleridir.</span><span class="sxs-lookup"><span data-stu-id="a34ca-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="a34ca-105">Sağladığınız servis tipine bağlı olarak, parçalar maddi veya maddi olmayan parçalar olabilir:</span><span class="sxs-lookup"><span data-stu-id="a34ca-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="a34ca-106">Maddi parçalar, üzerlerinde fiziksel bir servis görevi gerçekleştirebileceğiniz, makine veya bina gibi şeylerdir.</span><span class="sxs-lookup"><span data-stu-id="a34ca-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="a34ca-107">Fiziki servis nesnesi, Serbest bırakılan ürün ayrıntıları formunda oluşturduğunuz bir stok maddesi de olabilir.</span><span class="sxs-lookup"><span data-stu-id="a34ca-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="a34ca-108">Maddeye iliştirdiğiniz stok boyut grubuna bağlı olarak servis nesnesini madde seri numarası ayrıntı düzeyine kadar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a34ca-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="a34ca-109">Bu, servis nesnesinin temsil ettiği tam maddeyi izlemeniz gerektiğinde yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="a34ca-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="a34ca-110">Ancak, fiziki servis nesnesi aynı zamanda bir şirketin doğrudan üretim veya tedarik zinciriyle ilişkili bir madde de olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="a34ca-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="a34ca-111">Örneğin, servis siparişindeki onarımlar için kullanılan bir araç seti stoka dahil edilmeyen bir servis nesnesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="a34ca-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="a34ca-112">Bu durumda, bunu bir stok maddesi olarak kaydetmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="a34ca-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="a34ca-113">Maddi olmayan nesneler, üzerlerinde servis görevleri gerçekleştirebileceğiniz, hesap kümesi veya yasal bir belge gibi fiziki olmayan öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="a34ca-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="a34ca-114">Maddi olmayan servis nesnesi örneği</span><span class="sxs-lookup"><span data-stu-id="a34ca-114">Example of an intangible service object</span></span>

<span data-ttu-id="a34ca-115">Şirket A, birkaç küçük şirketin mali kayıtlarını tutuyor.</span><span class="sxs-lookup"><span data-stu-id="a34ca-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="a34ca-116">Şirket A'nın müşterilerinden biri, yerel bir futbol takımı. Şirket A kulübün hesapları için haftalık olarak defter tutmaktan ve yıllık denetimden sorumlu.</span><span class="sxs-lookup"><span data-stu-id="a34ca-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="a34ca-117">Kulübün hesapları Servis nesneleri formunda ayarlanıyor ve servis sözleşmesinde nesne olarak belirtiliyor.</span><span class="sxs-lookup"><span data-stu-id="a34ca-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="a34ca-118">Nesne için iki servis sözleşmesi satırı bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="a34ca-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="a34ca-119">Satır 1, satıra atanan haftalık aralıklı haftalık defter tutma ve satır 2, kendisine atanan yıllık aralıklı yıllık denetimdir.</span><span class="sxs-lookup"><span data-stu-id="a34ca-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a34ca-120">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="a34ca-120">Related topics</span></span>

[<span data-ttu-id="a34ca-121">Servis nesneleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="a34ca-121">Create service objects</span></span>](create-service-objects.md)



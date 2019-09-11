---
title: Servis nesnelerine genel bakış
description: Servis nesneleri, üzerinde servis gerçekleştirebileceğiniz müşteri kıymetleri ve ürünleridir.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a25c4d71d617a0b7cacd31f708421fd9dd960ea
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865896"
---
# <a name="service-objects-overview"></a><span data-ttu-id="4b67e-103">Servis nesnelerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="4b67e-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b67e-104">Servis nesneleri, üzerinde servis gerçekleştirebileceğiniz müşteri kıymetleri ve ürünleridir.</span><span class="sxs-lookup"><span data-stu-id="4b67e-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="4b67e-105">Sağladığınız servis tipine bağlı olarak, parçalar maddi veya maddi olmayan parçalar olabilir:</span><span class="sxs-lookup"><span data-stu-id="4b67e-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="4b67e-106">Maddi parçalar, üzerlerinde fiziksel bir servis görevi gerçekleştirebileceğiniz, makine veya bina gibi şeylerdir.</span><span class="sxs-lookup"><span data-stu-id="4b67e-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="4b67e-107">Fiziki servis nesnesi, Serbest bırakılan ürün ayrıntıları formunda oluşturduğunuz bir stok maddesi de olabilir.</span><span class="sxs-lookup"><span data-stu-id="4b67e-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="4b67e-108">Maddeye iliştirdiğiniz stok boyut grubuna bağlı olarak servis nesnesini madde seri numarası ayrıntı düzeyine kadar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b67e-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="4b67e-109">Bu, servis nesnesinin temsil ettiği tam maddeyi izlemeniz gerektiğinde yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="4b67e-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="4b67e-110">Ancak, fiziki servis nesnesi aynı zamanda bir şirketin doğrudan üretim veya tedarik zinciriyle ilişkili bir madde de olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="4b67e-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="4b67e-111">Örneğin, servis siparişindeki onarımlar için kullanılan bir araç seti stoka dahil edilmeyen bir servis nesnesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="4b67e-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="4b67e-112">Bu durumda, bunu bir stok maddesi olarak kaydetmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b67e-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="4b67e-113">Maddi olmayan nesneler, üzerlerinde servis görevleri gerçekleştirebileceğiniz, hesap kümesi veya yasal bir belge gibi fiziki olmayan öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="4b67e-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="4b67e-114">Maddi olmayan servis nesnesi örneği</span><span class="sxs-lookup"><span data-stu-id="4b67e-114">Example of an intangible service object</span></span>

<span data-ttu-id="4b67e-115">Şirket A, birkaç küçük şirketin mali kayıtlarını tutuyor.</span><span class="sxs-lookup"><span data-stu-id="4b67e-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="4b67e-116">Şirket A'nın müşterilerinden biri, yerel bir futbol takımı. Şirket A kulübün hesapları için haftalık olarak defter tutmaktan ve yıllık denetimden sorumlu.</span><span class="sxs-lookup"><span data-stu-id="4b67e-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="4b67e-117">Kulübün hesapları Servis nesneleri formunda ayarlanıyor ve servis sözleşmesinde nesne olarak belirtiliyor.</span><span class="sxs-lookup"><span data-stu-id="4b67e-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="4b67e-118">Nesne için iki servis sözleşmesi satırı bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="4b67e-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="4b67e-119">Satır 1, satıra atanan haftalık aralıklı haftalık defter tutma ve satır 2, kendisine atanan yıllık aralıklı yıllık denetimdir.</span><span class="sxs-lookup"><span data-stu-id="4b67e-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b67e-120">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="4b67e-120">Related topics</span></span>

[<span data-ttu-id="4b67e-121">Servis nesneleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="4b67e-121">Create service objects</span></span>](create-service-objects.md)


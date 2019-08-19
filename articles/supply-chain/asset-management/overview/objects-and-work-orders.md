---
title: Kıymetler ve iş emirleri
description: Bu konuda Kıymet Yönetimi'ndeki kıymetler ve iş emirleri açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783652"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="22a60-103">Kıymetler ve iş emirleri</span><span class="sxs-lookup"><span data-stu-id="22a60-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="22a60-104">Bu konuda Kıymet Yönetimi'ndeki kıymetler ve iş emirleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="22a60-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="22a60-105">Kıymetler ve iş emirleri Kıymet Yönetimi'nin merkezi parçalarıdır.</span><span class="sxs-lookup"><span data-stu-id="22a60-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="22a60-106">Bir *kıymet* sürekli bakım ve hizmet gerektiren bir makine veya makine parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="22a60-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="22a60-107">Kıymetler hiyerarşik yapıda oluşturulabilir ve işlem yapılacak yerleşimle ilişkili olabilirler.</span><span class="sxs-lookup"><span data-stu-id="22a60-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="22a60-108">Bakım işleri, kıymet yapısının tüm düzeyleriyle planlanabilir.</span><span class="sxs-lookup"><span data-stu-id="22a60-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="22a60-109">Ürün bilgileri ve kıymet belirtimi gibi çeşitli veriler ve gerekli bakım planları her kıymet için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="22a60-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="22a60-110">Aşağıdaki çizimde kıymet verilerine genel bakışla kıymetlerin iş türleriyle ilişkisi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="22a60-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="22a60-111">Kırmızı metin devir ve bağımlılıkları gösteren örnekler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="22a60-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Şekil 1](media/05-overview-image.png)

<span data-ttu-id="22a60-113">Her iş emrinin önleyici bakım, düzeltici bakım veya inceleme gibi bir iş emri türü vardır.</span><span class="sxs-lookup"><span data-stu-id="22a60-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="22a60-114">İş emri bir veya daha fazla iş emri işi içerir.</span><span class="sxs-lookup"><span data-stu-id="22a60-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="22a60-115">Her iş emri işi bir kıymet ve ilgili iş türü üzerinde gerçekleştirilmesi gereken bir işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="22a60-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="22a60-116">İlgili iş türlerine 10.000 km, 50.000 km, 1 yıllık bakım ve güvenlik incelemesi örnek verilebilir.</span><span class="sxs-lookup"><span data-stu-id="22a60-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="22a60-117">Bir iş emri birden çok kıymetle ilgili olabilir.</span><span class="sxs-lookup"><span data-stu-id="22a60-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="22a60-118">Aşağıdaki çizimde bir iş emrindeki anahtar verilere genel bakış gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="22a60-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Şekil 2](media/06-overview-image.png)

<span data-ttu-id="22a60-120">Bir iş emri başka bir iş emriyle ilgili olabilir ve iş türleri bir iş emri oluşturan izleyen işleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="22a60-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="22a60-121">Genel olarak iş emirleri arasında bağımlılık yoktur.</span><span class="sxs-lookup"><span data-stu-id="22a60-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="22a60-122">Bu nedenle, iş emri yaşam döngüsü durumunu değiştirebilirler ve birbirinden bağımsız olarak zamanlanabilirler.</span><span class="sxs-lookup"><span data-stu-id="22a60-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="22a60-123">İş emirleri düzeltici, önleyici veya reaktif bakımla ilgili çeşitli şekillerde oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="22a60-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="22a60-124">Ayrıca iş emirlerini el ile de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22a60-124">You can also create work orders manually.</span></span> <span data-ttu-id="22a60-125">Aşağıdaki çizimde iş emirlerini otomatik veya el ile oluşturma işlemine genel bakış gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="22a60-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Şekil 3](media/07-overview-image.png)

<span data-ttu-id="22a60-127">Bir iş emri üzerinde bakım işi zamanlamak ve çalıştırmak istediğinizde birkaç adımın tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="22a60-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="22a60-128">Aşağıdaki çizimde bir iş emrinin işlenmesine genel bakış gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="22a60-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Şekil 4](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="22a60-130">Genel olarak, Microsoft Dynamics 365 for Finance and Operations ve **Kıymet Yönetimi** modülünde çalışırken yeni kayıt oluşturmak için **Yeni**'yi, mevcut kaydı güncelleştirmek için **Düzenle**'yi ve yeni veya düzenlenmiş verileri kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="22a60-130">In general, when you work in Microsoft Dynamics 365 for Finance and Operations and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>

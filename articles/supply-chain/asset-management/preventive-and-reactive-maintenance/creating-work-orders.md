---
title: İş emirleri oluşturma
description: Bu konuda Varlık Yönetimi'nde iş emirleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439338"
---
# <a name="creating-work-orders"></a><span data-ttu-id="8c2f5-103">İş emirleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c2f5-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8c2f5-104">Önleyici bakım işleri planladığınızda sonraki adım işler için iş emirleri oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="8c2f5-105">Bu işlem, bakım zamanlamalarının birinde gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="8c2f5-106">Bakım zamanlamasında zamanlanmış işler farklı referans türlerine sahip olabilir:</span><span class="sxs-lookup"><span data-stu-id="8c2f5-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="8c2f5-107">Referans türü</span><span class="sxs-lookup"><span data-stu-id="8c2f5-107">Reference type</span></span> | <span data-ttu-id="8c2f5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c2f5-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2f5-109">Bakım planları</span><span class="sxs-lookup"><span data-stu-id="8c2f5-109">Maintenance plans</span></span>     | <span data-ttu-id="8c2f5-110">"Süre" veya "Sayaç" bakım planı türlerini temel alan önleyici bakım işleri.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="8c2f5-111">Bakım sıraları</span><span class="sxs-lookup"><span data-stu-id="8c2f5-111">Maintenance rounds</span></span>    | <span data-ttu-id="8c2f5-112">Benzer bir bakım türü gerektiren birkaç varlığı içeren önleyici bakım işleri.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="8c2f5-113">Bakım talebi</span><span class="sxs-lookup"><span data-stu-id="8c2f5-113">Maintenance request</span></span>   | <span data-ttu-id="8c2f5-114">İş emrine dönüştürülebilecek bir varlığın el ile oluşturulan bakım veya onarım talebi.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="8c2f5-115">**Varlık yönetimi** > **Ortak** > **Tüm bakım zamanlaması** veya **Bakım zamanlaması satırları aç** veya **Bakım zamanlaması havuzları aç** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="8c2f5-116">İş emri oluşturmak istediğiniz zamanlanmış bakım işlerini seçin ve **İş emri** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="8c2f5-117">**İş emirleri oluştur** iletişim kutusunda, seçili satırlar için toplam tahmini saat sayısı **Bakım tahmini saatleri** alanında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="8c2f5-118">**Parametreler** bölümünde, kaç adet iş emri oluşturulacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="8c2f5-119">Her bir bakım zamanlaması satırı için bir iş emri veya **Şuna göre bir iş emri** bölümünde yaptığınız seçimlere göre birkaç iş emri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="8c2f5-120">Oluşturduğunuz tüm iş emirlerinde kullanılacak bir **İş emri türü** seçin.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="8c2f5-121">Aşağıdaki çizimde **İş emirleri oluştur** iletişim kutusunun bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Şekil 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="8c2f5-123">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-123">Click **OK**.</span></span> <span data-ttu-id="8c2f5-124">Bir veya daha fazla iş emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8c2f5-124">One or more work orders are created.</span></span>


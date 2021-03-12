---
title: Servis düzeyi sözleşmelerine genel bakış
description: Servis düzeyi sözleşmesinde müşteri, şirketin sorunu kayda alışından sorun giderilene kadar olan süreyi temel alan bir minimum yanıt süresini kabul eder.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f2cfa8b72e515b6237914499af626ff8262429d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974372"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="2ec4f-103">Servis düzeyi sözleşmelerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="2ec4f-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2ec4f-104">Servis düzeyi anlaşması (SDA) bir servis şirketi ve servis müşterisi arasındaki anlaşmadır.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="2ec4f-105">SLA'da müşteri, şirketin sorunu kayda alışından sorun giderilene kadar olan süreyi temel alan bir minimum yanıt süresini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="2ec4f-106">SLA, müşterilere standart servis düzeyi sunulmasını zorunlu kılar ve ayrıca bir servis şirketi için bir servis işinin ne zaman tamamlanması gerektiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="2ec4f-107">Servis müşterilerine farklı düzeylerde servis sunmak için istenilen sayıda SDA oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="2ec4f-108">Servis düzeyi anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="2ec4f-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="2ec4f-109">**Servis yönetimi** \> **Kurulum** \> **Servis sözleşmeleri** \> **Servis düzeyi sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="2ec4f-110">**Servis düzeyi sözleşmesi** alanında, yeni servis sözleşmesi için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="2ec4f-111">Servis düzeyi sözleşmesine eklenen servis çağrılarının tamamlanması için izin vermek istediğiniz süreyi yazın.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="2ec4f-112">Ardından servis düzeyi anlaşmasının belirli bir takvimi temel almasını istiyorsanız bir takvim seçin.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="2ec4f-113">Servis düzeyi anlaşmasını uygulama</span><span class="sxs-lookup"><span data-stu-id="2ec4f-113">Apply a service level agreement</span></span>

<span data-ttu-id="2ec4f-114">SDA doğrudan bir servis anlaşmasına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="2ec4f-115">El ile oluşturduğunuz ve SLA içeren bir servis anlaşmasına iliştirdiğiniz servis siparişleri bu SLA'ya göre ölçülür.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="2ec4f-116">Otomatik olarak oluşturduğunuz servis siparişleri bir SDA'ya iliştirilmez.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="2ec4f-117">Servis düzeyi anlaşmasını servis anlaşmasına uygulama</span><span class="sxs-lookup"><span data-stu-id="2ec4f-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="2ec4f-118">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="2ec4f-119">SLA uygulamak istediğiniz servis sözleşmesini seçin ve **Eylem Bölmesinde** **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="2ec4f-120">**Servis düzeyi sözleşmesi** alanında, atamak istediğiniz SLA'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="2ec4f-121">Servis düzeyi anlaşmasını servis anlaşması grubuna uygulama</span><span class="sxs-lookup"><span data-stu-id="2ec4f-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="2ec4f-122">**Servis yönetimi** \> **Kurulum** \> **Servis sözleşmeleri** \> **Servis sözleşmesi grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="2ec4f-123">**Servis düzeyi sözleşmesi** alanında, atamak istediğiniz SLA'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="2ec4f-124">Servis siparişindeki zamanı SDA'ya göre izleme</span><span class="sxs-lookup"><span data-stu-id="2ec4f-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="2ec4f-125">Bir SLA'nın atandığı bir servis sözleşmesi için yeni bir servis siparişi oluşturduğunuzda, servisin teslim edilmesi için zaman aralığı başlatılır ve sistem teslimat süresini izlemeye başlar.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="2ec4f-126">Ek olarak aşağıdaki seçenekleri ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="2ec4f-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="2ec4f-127">Servis siparişlerinde harcanan toplam zamanı kaydetmek için servis siparişindeki zaman kaydını başlatabilir ve durdurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="2ec4f-128">Servis düzeyi anlaşmasında belirlenen zaman aralığıyla uyumluluğu izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="2ec4f-129">Servis düzeyi anlaşmasının zaman aralığı aşıldığında belirlenmesi gereken neden kodlarını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ec4f-130">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="2ec4f-130">See also</span></span>

[<span data-ttu-id="2ec4f-131">Servis düzeyi anlaşmalarıyla uyumluluğu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="2ec4f-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  



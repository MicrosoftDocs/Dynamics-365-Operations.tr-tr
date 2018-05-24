---
title: "Hizmet düzeyi sözleşmeleri"
description: "Servis düzeyi sözleşmesinde müşteri, şirketin sorunu kayda alışından sorun giderilene kadar olan süreyi temel alan bir minimum yanıt süresini kabul eder."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a><span data-ttu-id="377f2-103">Hizmet düzeyi sözleşmeleri</span><span class="sxs-lookup"><span data-stu-id="377f2-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="377f2-104">Servis düzeyi anlaşması (SDA) bir servis şirketi ve servis müşterisi arasındaki anlaşmadır.</span><span class="sxs-lookup"><span data-stu-id="377f2-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="377f2-105">SLA'da müşteri, şirketin sorunu kayda alışından sorun giderilene kadar olan süreyi temel alan bir minimum yanıt süresini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="377f2-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="377f2-106">SLA, müşterilere standart servis düzeyi sunulmasını zorunlu kılar ve ayrıca bir servis şirketi için bir servis işinin ne zaman tamamlanması gerektiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="377f2-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="377f2-107">Servis müşterilerine farklı düzeylerde servis sunmak için istenilen sayıda SDA oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="377f2-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="377f2-108">Servis düzeyi anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="377f2-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="377f2-109">**Servis yönetimi** \> **Kurulum** \> **Servis sözleşmeleri** \> **Servis düzeyi sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="377f2-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="377f2-110">**Servis düzeyi sözleşmesi** alanında, yeni servis sözleşmesi için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="377f2-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="377f2-111">Servis düzeyi sözleşmesine eklenen servis çağrılarının tamamlanması için izin vermek istediğiniz süreyi yazın.</span><span class="sxs-lookup"><span data-stu-id="377f2-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="377f2-112">Ardından servis düzeyi anlaşmasının belirli bir takvimi temel almasını istiyorsanız bir takvim seçin.</span><span class="sxs-lookup"><span data-stu-id="377f2-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="377f2-113">Servis düzeyi anlaşmasını uygulama</span><span class="sxs-lookup"><span data-stu-id="377f2-113">Apply a service level agreement</span></span>

<span data-ttu-id="377f2-114">SDA doğrudan bir servis anlaşmasına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="377f2-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="377f2-115">El ile oluşturduğunuz ve SLA içeren bir servis anlaşmasına iliştirdiğiniz servis siparişleri bu SLA'ya göre ölçülür.</span><span class="sxs-lookup"><span data-stu-id="377f2-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="377f2-116">Otomatik olarak oluşturduğunuz servis siparişleri bir SDA'ya iliştirilmez.</span><span class="sxs-lookup"><span data-stu-id="377f2-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="377f2-117">Servis düzeyi anlaşmasını servis anlaşmasına uygulama</span><span class="sxs-lookup"><span data-stu-id="377f2-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="377f2-118">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="377f2-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="377f2-119">SLA uygulamak istediğiniz servis sözleşmesini seçin ve **Eylem Bölmesinde** **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="377f2-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="377f2-120">**Servis düzeyi sözleşmesi** alanında, atamak istediğiniz SLA'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="377f2-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="377f2-121">Servis düzeyi anlaşmasını servis anlaşması grubuna uygulama</span><span class="sxs-lookup"><span data-stu-id="377f2-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="377f2-122">**Servis yönetimi** \> **Kurulum** \> **Servis sözleşmeleri** \> **Servis sözleşmesi grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="377f2-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="377f2-123">**Servis düzeyi sözleşmesi** alanında, atamak istediğiniz SLA'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="377f2-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="377f2-124">Servis siparişindeki zamanı SDA'ya göre izleme</span><span class="sxs-lookup"><span data-stu-id="377f2-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="377f2-125">Bir SLA'nın atandığı bir servis sözleşmesi için yeni bir servis siparişi oluşturduğunuzda, servisin teslim edilmesi için zaman aralığı başlatılır ve sistem teslimat süresini izlemeye başlar.</span><span class="sxs-lookup"><span data-stu-id="377f2-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="377f2-126">Ek olarak aşağıdaki seçenekleri ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="377f2-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="377f2-127">Servis siparişlerinde harcanan toplam zamanı kaydetmek için servis siparişindeki zaman kaydını başlatabilir ve durdurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="377f2-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="377f2-128">Servis düzeyi anlaşmasında belirlenen zaman aralığıyla uyumluluğu izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="377f2-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="377f2-129">Servis düzeyi anlaşmasının zaman aralığı aşıldığında belirlenmesi gereken neden kodlarını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="377f2-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="377f2-130">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="377f2-130">See also</span></span>

[<span data-ttu-id="377f2-131">Servis düzeyi anlaşmalarıyla uyumluluğu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="377f2-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  




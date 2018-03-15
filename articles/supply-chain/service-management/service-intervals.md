---
title: "Servis aralıkları"
description: "Servis aralığı, servis siparişlerini oluşturduğunuzda servis sözleşmesi satırları için servis siparişi satırlarının oluşturulma sıklığını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: 4a51a3c3483e81cefdaf3d8e62a4f1f47fcd706b
ms.contentlocale: tr-tr
ms.lasthandoff: 02/20/2018

---

# <a name="service-intervals"></a><span data-ttu-id="bda06-103">Servis aralıkları</span><span class="sxs-lookup"><span data-stu-id="bda06-103">Service intervals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bda06-104">Servis sözleşmesi aralığı, servis siparişlerini otomatik olarak oluşturduğunuzda servis siparişi satırlarının oluşturulma sıklığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bda06-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="bda06-105">Servis siparişlerini otomatik olarak oluşturduğunuzda servis siparişi satırları, sözleşme satırının başlangıç tarihinden başlayarak, servis sözleşmesi satırı için belirlediğiniz aralığa göre oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bda06-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="bda06-106">**Servis sözleşmeleri** sayfasındaki servis sözleşmesi satırının **Aralık** alanı boşsa satır bir defalık bir olaydır ve bu servis siparişlerini yinelenen şekilde oluşturmak için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="bda06-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="bda06-107">Örnek</span><span class="sxs-lookup"><span data-stu-id="bda06-107">Example</span></span>

<span data-ttu-id="bda06-108">Bu örnek, bir servis aralığının bir servis siparişinde servis sözleşmesi satırlarını ve servis siparişi satırlarını nasıl etkileyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bda06-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="bda06-109">Servis sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bda06-109">Create a service agreement</span></span>

<span data-ttu-id="bda06-110">Servis sözleşmesi oluştururken ilk olarak **Servis siparişlerini birleştir** seçeneğini, **Servis sözleşmesine göre** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bda06-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="bda06-111">**Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bda06-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="bda06-112">Yeni bir servis sözleşmesi oluşturmak için **Eylem Bölmesi**'nde **Servis sözleşmesi** sekmesinde, **Yeni** grubundaki **Servis sözleşmesi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bda06-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="bda06-113">Açıklama girin, **Proje Kodu** alanında bir proje seçin ve **Başlangıç Tarihi** alanına tarih girin.</span><span class="sxs-lookup"><span data-stu-id="bda06-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="bda06-114">**Servis siparişlerini birleştir** alanında, **Servis sözleşmesine göre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bda06-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="bda06-115">Artık aşağıdaki servis sözleşmesini oluşturmuş bulunuyorsunuz:</span><span class="sxs-lookup"><span data-stu-id="bda06-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="bda06-116">Proje</span><span class="sxs-lookup"><span data-stu-id="bda06-116">Project</span></span>      | <span data-ttu-id="bda06-117">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="bda06-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bda06-118">Projeniz</span><span class="sxs-lookup"><span data-stu-id="bda06-118">Your project</span></span> | <span data-ttu-id="bda06-119">Proje için belirlediğiniz tarih.</span><span class="sxs-lookup"><span data-stu-id="bda06-119">The date you specified for the project.</span></span> <span data-ttu-id="bda06-120">Bu örnekte, güncel tarih kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bda06-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="bda06-121">Servis sözleşmesi satırı oluşturma</span><span class="sxs-lookup"><span data-stu-id="bda06-121">Create a service agreement line</span></span>

<span data-ttu-id="bda06-122">Ardından, **Saat** hareket türüne sahip bir servis sözleşmesi satırı oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="bda06-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="bda06-123">Örneğin bu bölümünü tamamlamak için **Servis aralıkları** sayfasında 10 günlük bir servis aralığı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bda06-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="bda06-124">Yeni oluşturduğunuz servis sözleşmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bda06-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="bda06-125">**Servis sözleşmeleri** sayfasının alt bölmesinde yeni bir satır oluşturmak için **Satırlar** hızlı sekmesinde **Ekle** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bda06-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="bda06-126">**Hareket türü** alanında **Saat**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bda06-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="bda06-127">**Çalışan** alanında servisi verecek çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="bda06-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="bda06-128">**Servis aralığı** alanında, 10 günlük aralığı seçin.</span><span class="sxs-lookup"><span data-stu-id="bda06-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="bda06-129">Şimdi aşağıdaki bilgileri içeren bir servis sözleşmesi satırı oluşturdunuz:</span><span class="sxs-lookup"><span data-stu-id="bda06-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="bda06-130">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="bda06-130">Transaction type</span></span> | <span data-ttu-id="bda06-131">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="bda06-131">Start date</span></span>                               | <span data-ttu-id="bda06-132">Servis aralığı</span><span class="sxs-lookup"><span data-stu-id="bda06-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="bda06-133">Saat</span><span class="sxs-lookup"><span data-stu-id="bda06-133">Hour</span></span>             | <span data-ttu-id="bda06-134">Güncel tarih.</span><span class="sxs-lookup"><span data-stu-id="bda06-134">The current date.</span></span>                        | <span data-ttu-id="bda06-135">10 günde bir</span><span class="sxs-lookup"><span data-stu-id="bda06-135">Every 10 days</span></span>    |
| <span data-ttu-id="bda06-136">Çalışan</span><span class="sxs-lookup"><span data-stu-id="bda06-136">Worker</span></span>           | <span data-ttu-id="bda06-137">Servisi gerçekleştirecek çalışan.</span><span class="sxs-lookup"><span data-stu-id="bda06-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="bda06-138">Satır için belirtilen zaman aralığı yok.</span><span class="sxs-lookup"><span data-stu-id="bda06-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="bda06-139">Planlanan servis siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="bda06-139">Create planned service orders</span></span>

<span data-ttu-id="bda06-140">Şimdi gelecek aya ait planlanan servis siparişleri ve servis siparişi satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bda06-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="bda06-141">**Servis sözleşmeleri** sayfasında, **Eylem Bölmesi**'nde, **Teslim Et** sekmesindeki **Planlanan servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bda06-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="bda06-142">**Servis siparişleri oluştur** sayfasında, **Başlangıç Tarihi** alanında güncel tarihi ve **Bitiş Tarihi** alanında güncel tarihten bir ay sonraki tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="bda06-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="bda06-143">**Saat** kaydırıcısını **Evet** konumuna getirin.</span><span class="sxs-lookup"><span data-stu-id="bda06-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="bda06-144">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bda06-144">Click **OK**.</span></span>

<span data-ttu-id="bda06-145">Servis siparişinde hiçbir gruplandırma bulunmadığından ( **Servis siparişlerini birleştir** alanındaki **Servis sözleşmesine göre** seçeneğiyle tanımlanır), servis siparişi başına bir servis siparişi satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bda06-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="bda06-146">Oluşturulan servis siparişleri</span><span class="sxs-lookup"><span data-stu-id="bda06-146">Service orders created</span></span>

<span data-ttu-id="bda06-147">Üç servis siparişi satırı, **Servis siparişleri oluştur** iletişim kutusunda belirttiğiniz zaman çerçevesinin sınırları içinde oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="bda06-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="bda06-148">Servis siparişi satırlarını **Servis sözleşmeleri** sayfasında (**Eylem Bölmesi** \> **Teslim Et** sekmesi \>**Görüntüle** düğmesi) görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bda06-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bda06-149">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="bda06-149">Related topics</span></span>

[<span data-ttu-id="bda06-150">Servis aralıkları ayarlama</span><span class="sxs-lookup"><span data-stu-id="bda06-150">Set up service intervals</span></span>](set-up-service-intervals.md)  



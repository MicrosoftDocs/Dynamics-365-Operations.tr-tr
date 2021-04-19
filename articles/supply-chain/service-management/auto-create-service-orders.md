---
title: Servis siparişlerini otomatik oluşturma
description: Servis sözleşmesinin geçerli olduğu dönem için bir servis sözleşmesini temel alan servis siparişleri oluşturabilirsiniz.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b864aee332c82bc6b6845e7f9e425cfef377033
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824642"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="6279e-103">Servis siparişlerini otomatik oluşturma</span><span class="sxs-lookup"><span data-stu-id="6279e-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6279e-104">Servis sözleşmesinin geçerli olduğu dönem için bir servis sözleşmesini temel alan servis siparişleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6279e-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="6279e-105">Bir servis sözleşmesinden oluşturduğunuz servis siparişleri servis sözleşmesine iliştirilir.</span><span class="sxs-lookup"><span data-stu-id="6279e-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="6279e-106">Servis siparişleri otomatik olarak aşağıdaki ayarlardan oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="6279e-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="6279e-107">Servis sözleşmesi satırlarında ayarlanan servis sözleşmesi aralığı.</span><span class="sxs-lookup"><span data-stu-id="6279e-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="6279e-108">Servis sözleşmesi aralığı servis siparişi satırlarının oluşturulma sıklığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6279e-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="6279e-109">Daha fazla bilgi için bkz. [Servis aralıkları](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="6279e-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="6279e-110">**Servis siparişleri oluştur** formundaki **Başlangıç tarihi** ve **Bitiş tarihi** alanlarındaki servis dönemini tanımlamak için belirttiğiniz dönem.</span><span class="sxs-lookup"><span data-stu-id="6279e-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="6279e-111">Daha fazla bilgi için bkz. [Servis siparişlerini otomatik oluşturma](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="6279e-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="6279e-112">Servis sözleşmesi başlığındaki **Servis siparişlerini birleştir** seçeneği.</span><span class="sxs-lookup"><span data-stu-id="6279e-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="6279e-113">Bu seçenek servis sözleşmesinden oluşturulan servis siparişi satırlarının servis siparişlerini personele, servis görevine, servis nesnesine veya servis sözleşmesine göre birleştirip birleştirmeyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6279e-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="6279e-114">Daha fazla bilgi için bkz. [Servis siparişlerini birleştirme](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="6279e-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="6279e-115">Servis sözleşmesi satırındaki **Zaman aralığı** seçeneği.</span><span class="sxs-lookup"><span data-stu-id="6279e-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="6279e-116">Zaman aralığı bir servis siparişinin hesaplanan tarihi ile bağlantılı olarak ne kadar uzağa taşınabileceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6279e-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="6279e-117">Daha fazla bilgi için bkz. [Zaman aralıkları](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="6279e-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="6279e-118">Bir servis siparişi için belirtilen gün <STRONG>Servis yönetimi parametreleri</STRONG> formunda seçtiğiniz takvimde açık değilse, takvim uyumsuzluğu olduğunu belirten bir iletiyle karşılaşırsınız.</span><span class="sxs-lookup"><span data-stu-id="6279e-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="6279e-119">Endişe etmeden iletiyi yok sayabilirsiniz; söz konusu gün takvimde kapalı olmasına karşın servis siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6279e-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="6279e-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6279e-120">Example 1</span></span>

<span data-ttu-id="6279e-121">Servis sözleşmesi 1 Ocak 2012'den 31 Kasım 2012'ye kadar sürer.</span><span class="sxs-lookup"><span data-stu-id="6279e-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="6279e-122">**Servis siparişleri oluştur** formunda belirttiğiniz servis dönemi 1 Kasım 2012 ile 1 Kasım 2013 arasındaysa, servis siparişleri 1 Kasım 2012'den 31 Aralık 2012'ye kadar oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6279e-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="6279e-123">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6279e-123">Example 2</span></span>

<span data-ttu-id="6279e-124">Servis sözleşmesi 1 Ocak 2012'den 31 Kasım 2012'ye kadar sürer.</span><span class="sxs-lookup"><span data-stu-id="6279e-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="6279e-125">İki servis sözleşmesi satırı servis sözleşmesine iliştirilir.</span><span class="sxs-lookup"><span data-stu-id="6279e-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="6279e-126">İlk servis sözleşmesi satırının başlangıç tarihi 2 Ocak 2012 ve bitiş tarihi 1 Mart 2012'dir.</span><span class="sxs-lookup"><span data-stu-id="6279e-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="6279e-127">İkinci servis sözleşmesi satırının başlangıç tarihi 1 Nisan 2012 ve bitiş tarihi 31 Aralık 2012'dir.</span><span class="sxs-lookup"><span data-stu-id="6279e-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="6279e-128">**Servis siparişleri oluştur** formunda 1 Ekim 2012 ile 31 Aralık 2012 arasında olan bir dönem belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6279e-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="6279e-129">Dolayısıyla, birinci sözleşme satırının başlangıç tarihi ve bitiş tarihi servis siparişi için belirttiğiniz dönemden önce olduğundan servis siparişleri yalnızca ikinci sözleşme satırı için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6279e-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
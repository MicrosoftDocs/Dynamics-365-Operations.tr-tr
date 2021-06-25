---
title: Tamamlanmamış veya eksik çalışmalar nedeniyle sevkiyatı onaylayamıyorsunuz
description: Tamamlanmamış veya eksik çalışmalar nedeniyle sevkiyatı onaylayamıyorsunuz
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123855"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="57931-103">Tamamlanmamış veya eksik çalışmalar nedeniyle sevkiyatı onaylayamıyorsunuz</span><span class="sxs-lookup"><span data-stu-id="57931-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="57931-104">Hata kodu: WAX515</span><span class="sxs-lookup"><span data-stu-id="57931-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="57931-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="57931-105">Symptoms</span></span>

<span data-ttu-id="57931-106">Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="57931-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="57931-107">%1 yükü için sevkiyat onaylanamıyor çünkü yük için tüm işler tamamlanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="57931-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="57931-108">Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="57931-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="57931-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="57931-109">Cause</span></span>

<span data-ttu-id="57931-110">Yükleme veya sevkiyat işlemi şu anda sevkiyat onayının başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="57931-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="57931-111">Sevkiyatı onaylamadan önce, yükleme için en az bir miktar çalışmanın mevcut olması ve bu çalışmanın *Kapalı* veya *İptal edilmiş* durumunda olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="57931-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="57931-112">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="57931-112">Resolution</span></span>

<span data-ttu-id="57931-113">Yükleme veya sevkiyat ile ilgili satış siparişlerini veya transfer emirlerini kontrol edin ve ilgili tüm çalışmanın tamamlandığından veya iptal edildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="57931-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="57931-114">Birkaç sayfada birden sevkiyatlar ve yüklemelerde çalışabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57931-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="57931-115">Aşağıdaki alt bölümler birkaç örnek sağlar.</span><span class="sxs-lookup"><span data-stu-id="57931-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="57931-116">Tüm yüklemeler sayfası</span><span class="sxs-lookup"><span data-stu-id="57931-116">All loads page</span></span>

1. <span data-ttu-id="57931-117">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="57931-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="57931-118">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="57931-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="57931-119">Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57931-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="57931-120">Her çalışma kodunun durumunu denetleyin.</span><span class="sxs-lookup"><span data-stu-id="57931-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="57931-121">*Kapalı* veya *İptal edildi* durumundaki çalışma kodlarını takip edin.</span><span class="sxs-lookup"><span data-stu-id="57931-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="57931-122">Her çalışma kodu *Kapalı* veya *İptal edildi* durumunda olduğunda, sevkiyatı onaylamak için yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="57931-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="57931-123">Tüm sevkiyatlar sayfası</span><span class="sxs-lookup"><span data-stu-id="57931-123">All shipments page</span></span>

1. <span data-ttu-id="57931-124">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="57931-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="57931-125">Onaylanamayan sevkiyatı seçin.</span><span class="sxs-lookup"><span data-stu-id="57931-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="57931-126">Eylem Bölmesinde **Sevkiyatlar** sekmesindeki **Çalışma** grubunda **İş ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="57931-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="57931-127">Her çalışma kodunun durumunu denetleyin.</span><span class="sxs-lookup"><span data-stu-id="57931-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="57931-128">*Kapalı* veya *İptal edildi* durumundaki çalışma kodlarını takip edin.</span><span class="sxs-lookup"><span data-stu-id="57931-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="57931-129">Her çalışma kodu *Kapalı* veya *İptal edildi* durumunda olduğunda, sevkiyatı onaylamak için yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="57931-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="57931-130">Tüm çalışmalar sayfası</span><span class="sxs-lookup"><span data-stu-id="57931-130">All work page</span></span>

1. <span data-ttu-id="57931-131">**Ambar yönetimi \> İş \> Tüm çalışmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="57931-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="57931-132">Sevkiyatın onaylanamadığı sipariş numarası ile ilgili çalışmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="57931-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="57931-133">Eylem Bölmesinde **Sevkiyat** sekmesindeki **Sevkiyat** grubunda **Sevkiyatı onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57931-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="57931-134">Her çalışma kodunun durumunu denetleyin.</span><span class="sxs-lookup"><span data-stu-id="57931-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="57931-135">*Kapalı* veya *İptal edildi* durumundaki çalışma kodlarını takip edin.</span><span class="sxs-lookup"><span data-stu-id="57931-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="57931-136">Her çalışma kodu *Kapalı* veya *İptal edildi* durumunda olduğunda, sevkiyatı onaylamak için yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="57931-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

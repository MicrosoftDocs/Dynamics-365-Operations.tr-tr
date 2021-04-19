---
title: Gelen ve giden varlıklar
description: Bu konuda Varlık Yönetimi'nde gelen ve giden varlıkları kaydetme açıklanmaktadır.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a2bac914330058400a7e4d7d355bd4a00a4522f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816808"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="57c53-103">Gelen ve giden varlıklar</span><span class="sxs-lookup"><span data-stu-id="57c53-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="57c53-104">Şirketiniz başka yerlerden veya müşterilerden alınan varlıklar üzerinde onarım işleri veya bakım işleri yapıyorsa, Varlık Yönetimi hem şirketinize giden gelen varlıkları hem de iade edilen varlıkları izleyebilir.</span><span class="sxs-lookup"><span data-stu-id="57c53-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="57c53-105">Gelen ve giden varlıkları yönetmek için gelen ve giden yaşam döngüsü durumlarını kullanmak istiyorsanız bu eylemleri desteklemek için bakım talebi yaşam döngüsü durumlarını ve yaşam döngüsü modellerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="57c53-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="57c53-106">Daha fazla bilgi için bkz. [Bakım istekleri](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="57c53-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="57c53-107">Varlık Yönetimi kurulumu, gelen ve giden varlıklarla çalışabilir olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="57c53-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="57c53-108">Varlıkları gelen olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="57c53-108">Register assets as inbound</span></span>

1. <span data-ttu-id="57c53-109">**Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Etkin bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="57c53-110">Bakım talebini seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="57c53-111">**Bakım talebi durumunu güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="57c53-112">**Gelen**'i (veya gelen varlıklar için oluşturduğunuz başka bir yaşam döngüsü durumu) seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Varlıkları gelen olarak kaydetme](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="57c53-114">Gelen varlıkları alındı olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="57c53-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="57c53-115">**Varlık yönetimi** \> **Ortak** \> **Gelen/Giden** \> **Gelen varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="57c53-116">Varlık veya bakım talebini seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="57c53-117">**Varlıkları al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="57c53-118">**Alındı** alanında tarihi ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="57c53-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="57c53-119">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-119">Then select **OK**.</span></span> <span data-ttu-id="57c53-120">Kayıt, **Gelen varlıklar** listesi sayfasından kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="57c53-120">The record is removed from the **Inbound assets** list page.</span></span>

![Gelen varlıkları alındı olarak kaydetme](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="57c53-122">Varlıkları giden olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="57c53-122">Register assets as outbound</span></span>

<span data-ttu-id="57c53-123">Bakım veya onarım işini tamamladığınızda, varlığı iade edildiği gibi kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57c53-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="57c53-124">**Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Etkin bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="57c53-125">Bakım talebini seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="57c53-126">**Bakım talebi durumunu güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="57c53-127">**Giden**'i (veya giden varlıklar için oluşturduğunuz başka bir yaşam döngüsü durumu) seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="57c53-128">Giden varlıkları teslim edildi olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="57c53-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="57c53-129">**Varlık yönetimi** \> **Ortak** \> **Gelen/Giden** \> **Giden varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="57c53-130">Varlık veya bakım talebini seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="57c53-131">Varlıkları **Teslim et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="57c53-132">**Teslim edildi** alanında tarihi ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="57c53-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="57c53-133">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57c53-133">Then select **OK**.</span></span> <span data-ttu-id="57c53-134">Kayıt, **Giden varlıklar** listesi sayfasından kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="57c53-134">The record is removed from the **Outbound assets** list page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
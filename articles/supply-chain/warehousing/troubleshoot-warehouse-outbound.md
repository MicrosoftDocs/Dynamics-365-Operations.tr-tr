---
title: Giden ambar işlemlerinde sorun giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta giden ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993990"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="79e5b-103">Giden ambar işlemlerinde sorun giderme</span><span class="sxs-lookup"><span data-stu-id="79e5b-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79e5b-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta giden ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="79e5b-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="79e5b-105">Şu hata iletisini alıyorum: "Satış siparişi serbest bırakılamadı."</span><span class="sxs-lookup"><span data-stu-id="79e5b-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e5b-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="79e5b-106">Issue description</span></span>

<span data-ttu-id="79e5b-107">Bu sorun birkaç nedenle oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="79e5b-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="79e5b-108">Örneğin, sipariş alacak yönetimi tutuluyor durumundadır ve bir satış siparişiyle ilişkili tüm satış satırları için geçerli bir posta adresi girilene kadar hiçbir sevkiyat oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="79e5b-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="79e5b-109">Alternatif olarak, siparişin ambara serbest bırakılması için önce giderilmesi gereken bir sipariş tutma işlemi vardır.</span><span class="sxs-lookup"><span data-stu-id="79e5b-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="79e5b-110">Bu tutma işlemi, siparişe özgü olabilir veya müşteri hesabı üzerinde olabilir.</span><span class="sxs-lookup"><span data-stu-id="79e5b-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e5b-111">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="79e5b-111">Issue resolution</span></span>

<span data-ttu-id="79e5b-112">Satış siparişi ve sipariş satırlarına adres ekleyin veya adresi güncelleştirin, ardından siparişi ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="79e5b-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="79e5b-113">Siparişler yalnızca geçerli teslimat adresi varsa (**Kuruluş yönetimi** modülünde ayarlanan adres biçimi kurulumu için) ambara serbest bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="79e5b-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="79e5b-114">Sipariş tutmayı araştırın ve sorunları giderin.</span><span class="sxs-lookup"><span data-stu-id="79e5b-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="79e5b-115">Ardından sipariş veya müşteriden tutma işlemini kaldırın ve siparişi ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="79e5b-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="79e5b-116">Şu iletiyi alıyorum: "%1 yükü için sevkiyat onaylandı."</span><span class="sxs-lookup"><span data-stu-id="79e5b-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="79e5b-117">Ancak hiçbir satır deftere nakledilmiyor.</span><span class="sxs-lookup"><span data-stu-id="79e5b-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e5b-118">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="79e5b-118">Issue description</span></span>

<span data-ttu-id="79e5b-119">Bir yükle ilgili sevkiyat onaylanmıştır ancak başka bir deftere nakil işlemi gerçekleşmemiştir.</span><span class="sxs-lookup"><span data-stu-id="79e5b-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="79e5b-120">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="79e5b-120">Issue resolution</span></span>

<span data-ttu-id="79e5b-121">Sevkiyat onayı deftere nakli etkilemez.</span><span class="sxs-lookup"><span data-stu-id="79e5b-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="79e5b-122">Yalnızca sevkiyat ve yük durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="79e5b-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="79e5b-123">Deftere nakletme işlemi ayrı bir işlemde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="79e5b-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="79e5b-124">Şu hata iletisini alıyorum: "Ambar yönetimi etkinleştirilmiş olduğundan, doğrudan teslimat %1 ambarı için işlenemiyor.</span><span class="sxs-lookup"><span data-stu-id="79e5b-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="79e5b-125">Lütfen ambar yönetimi için etkinleştirilmemiş olan başka bir ambar belirtin."</span><span class="sxs-lookup"><span data-stu-id="79e5b-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="79e5b-126">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="79e5b-126">Issue description</span></span>

<span data-ttu-id="79e5b-127">Ambar yönetimi (WMS) için etkinleştirilmiş bir ambardan doğrudan teslimatın satış satırına bir madde eklenir.</span><span class="sxs-lookup"><span data-stu-id="79e5b-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="79e5b-128">Satış satırı güncelleştirildiğinde bu hata iletisini alırsınız.</span><span class="sxs-lookup"><span data-stu-id="79e5b-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="79e5b-129">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="79e5b-129">Issue resolution</span></span>

<span data-ttu-id="79e5b-130">Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir.</span><span class="sxs-lookup"><span data-stu-id="79e5b-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="79e5b-131">Şu anda WMS doğrudan teslimi desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="79e5b-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="79e5b-132">Bu nedenle, doğrudan teslimi kullanmak için WMS harici bir madde ve ambar seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="79e5b-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>

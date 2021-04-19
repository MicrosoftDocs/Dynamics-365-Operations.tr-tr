---
title: Giden ambar işlemlerinde sorun giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta giden ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 919b6f433db47f24adc9a474942557a1467d1f71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828190"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="b6594-103">Giden ambar işlemlerinde sorun giderme</span><span class="sxs-lookup"><span data-stu-id="b6594-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6594-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta giden ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b6594-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="b6594-105">Şu hata iletisini alıyorum: "Satış siparişi serbest bırakılamadı."</span><span class="sxs-lookup"><span data-stu-id="b6594-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b6594-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b6594-106">Issue description</span></span>

<span data-ttu-id="b6594-107">Bu sorun birkaç nedenle oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="b6594-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="b6594-108">Örneğin, sipariş alacak yönetimi tutuluyor durumundadır ve bir satış siparişiyle ilişkili tüm satış satırları için geçerli bir posta adresi girilene kadar hiçbir sevkiyat oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="b6594-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="b6594-109">Alternatif olarak, siparişin ambara serbest bırakılması için önce giderilmesi gereken bir sipariş tutma işlemi vardır.</span><span class="sxs-lookup"><span data-stu-id="b6594-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="b6594-110">Bu tutma işlemi, siparişe özgü olabilir veya müşteri hesabı üzerinde olabilir.</span><span class="sxs-lookup"><span data-stu-id="b6594-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b6594-111">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b6594-111">Issue resolution</span></span>

<span data-ttu-id="b6594-112">Satış siparişi ve sipariş satırlarına adres ekleyin veya adresi güncelleştirin, ardından siparişi ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="b6594-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="b6594-113">Siparişler yalnızca geçerli teslimat adresi varsa (**Kuruluş yönetimi** modülünde ayarlanan adres biçimi kurulumu için) ambara serbest bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="b6594-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="b6594-114">Sipariş tutmayı araştırın ve sorunları giderin.</span><span class="sxs-lookup"><span data-stu-id="b6594-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="b6594-115">Ardından sipariş veya müşteriden tutma işlemini kaldırın ve siparişi ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="b6594-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="b6594-116">Şu iletiyi alıyorum: "%1 yükü için sevkiyat onaylandı."</span><span class="sxs-lookup"><span data-stu-id="b6594-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="b6594-117">Ancak hiçbir satır deftere nakledilmiyor.</span><span class="sxs-lookup"><span data-stu-id="b6594-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b6594-118">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b6594-118">Issue description</span></span>

<span data-ttu-id="b6594-119">Bir yükle ilgili sevkiyat onaylanmıştır ancak başka bir deftere nakil işlemi gerçekleşmemiştir.</span><span class="sxs-lookup"><span data-stu-id="b6594-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b6594-120">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b6594-120">Issue resolution</span></span>

<span data-ttu-id="b6594-121">Sevkiyat onayı deftere nakli etkilemez.</span><span class="sxs-lookup"><span data-stu-id="b6594-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="b6594-122">Yalnızca sevkiyat ve yük durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b6594-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="b6594-123">Deftere nakletme işlemi ayrı bir işlemde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b6594-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="b6594-124">Şu hata iletisini alıyorum: "Ambar yönetimi etkinleştirilmiş olduğundan, doğrudan teslimat %1 ambarı için işlenemiyor.</span><span class="sxs-lookup"><span data-stu-id="b6594-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="b6594-125">Lütfen ambar yönetimi için etkinleştirilmemiş olan başka bir ambar belirtin."</span><span class="sxs-lookup"><span data-stu-id="b6594-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b6594-126">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b6594-126">Issue description</span></span>

<span data-ttu-id="b6594-127">Ambar yönetimi (WMS) için etkinleştirilmiş bir ambardan doğrudan teslimatın satış satırına bir madde eklenir.</span><span class="sxs-lookup"><span data-stu-id="b6594-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="b6594-128">Satış satırı güncelleştirildiğinde bu hata iletisini alırsınız.</span><span class="sxs-lookup"><span data-stu-id="b6594-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="b6594-129">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b6594-129">Issue resolution</span></span>

<span data-ttu-id="b6594-130">Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir.</span><span class="sxs-lookup"><span data-stu-id="b6594-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="b6594-131">Şu anda WMS doğrudan teslimi desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="b6594-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="b6594-132">Bu nedenle, doğrudan teslimi kullanmak için WMS harici bir madde ve ambar seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="b6594-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
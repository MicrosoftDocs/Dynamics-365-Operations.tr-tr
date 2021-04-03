---
title: Genel muhasebe için varsayılan açıklamalar
description: Varsayılan açıklamalar, fiş deftere nakillerinde Açıklama alanını genel muhasebeye güncelleştirmek için kullanılabilir.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500392"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="e7e7a-103">Genel muhasebe için varsayılan açıklamalar</span><span class="sxs-lookup"><span data-stu-id="e7e7a-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e7e7a-104">Varsayılan açıklamalar, fiş deftere nakillerinde **Açıklama** alanını genel muhasebeye güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="e7e7a-105">Bu işlevsellik, Varış yeri maliyetiyle çalışacak şekilde geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="e7e7a-106">Genel muhasebe deftere nakilleri için varsayılan açıklamaları ayarlamak üzere, **Kuruluş yönetimi \> Kurulum \> Varsayılan açıklamalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="e7e7a-107">Aşağıdaki tabloda, Varış yeri maliyetini desteklemek için **Varsayılan açıklamalar** sayfasındaki **Açıklama** alanı için eklenen yeni değerler listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="e7e7a-108">Açıklama türü</span><span class="sxs-lookup"><span data-stu-id="e7e7a-108">Description type</span></span> | <span data-ttu-id="e7e7a-109">Notlar</span><span class="sxs-lookup"><span data-stu-id="e7e7a-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="e7e7a-110">İthalat maliyetlendirmesi - Maliyet tahakkuku</span><span class="sxs-lookup"><span data-stu-id="e7e7a-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="e7e7a-111">Bir satın alma siparişi faturası deftere nakledildiğinde, tahmini seyahat maliyetleri için bir maliyet tahakkuku işlenir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="e7e7a-112">Açıklamaya yolculuk numarasını eklemek için varsayılan açıklamalar belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="e7e7a-113">Sevkiyat numarası için *%4* kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="e7e7a-114">İthalat maliyetlendirmesi - Transitteki mal siparişi</span><span class="sxs-lookup"><span data-stu-id="e7e7a-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="e7e7a-115">Transitteki mal işlemesi kullanıyorsanız satın alma siparişi faturası deftere nakledilir ve mallar transitteki mallar hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="e7e7a-116">Açıklamaya transitteki mal sipariş numarasını eklemek için varsayılan açıklamalar belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="e7e7a-117">Transitteki sipariş numarası için *%4* kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="e7e7a-118">Stok – kapatma – ayarlama</span><span class="sxs-lookup"><span data-stu-id="e7e7a-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="e7e7a-119">Borç hesapları (AP) faturası, bir yolculuk maliyeti için işlendiğinde, yolculuk maliyetlerini tahmin etmek için bir stok ayarlaması işlenir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="e7e7a-120">Açıklamaya yolculuk numarasını eklemek için varsayılan açıklamalar belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="e7e7a-121">Sevkiyat numarası için *%4* kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7e7a-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="e7e7a-122">**Varsayılan açıklamalar** sayfasıyla çalışma hakkında daha fazla bilgi için, bkz. [Otomatik deftere nakil için varsayılan açıklamaları ayarlama](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="e7e7a-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>

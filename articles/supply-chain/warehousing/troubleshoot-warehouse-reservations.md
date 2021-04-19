---
title: Ambar yönetiminde rezervasyonlarla ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar rezervasyonları ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828118"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="eb151-103">Ambar yönetiminde rezervasyonlarla ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="eb151-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb151-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar rezervasyonları ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="eb151-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="eb151-105">Toplu iş ve seri numarası kayıtları ile ilgili konular için bkz. [Ambar toplu iş ve seri rezervasyon hiyerarşilerinde sorun giderme](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="eb151-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="eb151-106">Şu hata iletisini alıyorum: "Rezervasyonlara dayanan iş oluşturulduğu için rezervasyonlar silinemedi."</span><span class="sxs-lookup"><span data-stu-id="eb151-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="eb151-107">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="eb151-107">Issue description</span></span>

<span data-ttu-id="eb151-108">Satır karşılığında açık iş bulunduğundan bir satış satırındaki stok ayırmayı geri alamazsınız.</span><span class="sxs-lookup"><span data-stu-id="eb151-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="eb151-109">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="eb151-109">Issue resolution</span></span>

<span data-ttu-id="eb151-110">Maddeyi bir paketleme istasyonundan başka bir konuma (*Baydoor* gibi) getirmek için açık paketleme grubu işinin bulunup bulunmadığını araştırın.</span><span class="sxs-lookup"><span data-stu-id="eb151-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="eb151-111">Stok ayırma işlemini fiziksel olarak neyin yaptığını belirlemek için **İş oluşturma geçmişi günlüğü** ve **İş ayrıntıları** sayfalarındaki kayıtları gözden geçirin ve daha sonra ayırmayı geri almak için işi tamamlayın veya silin.</span><span class="sxs-lookup"><span data-stu-id="eb151-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="eb151-112">Şu hata iletisini alıyorum: "Stok miktarı %1, %2 maddesi için yetersiz stok hareketi nedeniyle güncelleştirilemedi..."</span><span class="sxs-lookup"><span data-stu-id="eb151-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="eb151-113">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="eb151-113">Issue description</span></span>

<span data-ttu-id="eb151-114">Bu sorun, belirtilen boyutlara sahip yeterli stok hareketi bulunmadığından, sistem bir stok miktarını güncelleştiremediği takdirde oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="eb151-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="eb151-115">Tam hata iletisinin tüm metni şöyledir:</span><span class="sxs-lookup"><span data-stu-id="eb151-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="eb151-116">%12 Lot Kimliği ve %11 başvuru kodu için boyutları Boyut=%3, Renk=%4, Ekler=%5, Tesis=%6, Ambar=%7, Konum=%8, Stok durumu=Mevcut, Plaka=%9, Parti numarası=%10 olan %2 maddesi için yeterli stok hareketi olmadığından %1 stok miktarı güncelleştirilemedi.</span><span class="sxs-lookup"><span data-stu-id="eb151-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="eb151-117">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="eb151-117">Issue resolution</span></span>

<span data-ttu-id="eb151-118">Hiçbir stok hareketinin fiziksel olarak miktar ayırmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="eb151-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="eb151-119">Örneğin, bu hareketler açık kalite emirleri, stok bloke kayıtları veya çıkış emirleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="eb151-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="eb151-120">Şu hata iletisini alıyorum: "Fiziksel eldeki miktar... stokta yalnızca 0,00 mevcut olduğundan ayrılamaz."</span><span class="sxs-lookup"><span data-stu-id="eb151-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="eb151-121">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="eb151-121">Issue description</span></span>

<span data-ttu-id="eb151-122">Bu sorun, belirtilen boyutlara sahip yeterli stok hareketi bulunmadığından, sistem bir stok miktarını güncelleştiremediği takdirde oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="eb151-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="eb151-123">Tam hata iletisinin tüm metni şöyledir:</span><span class="sxs-lookup"><span data-stu-id="eb151-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="eb151-124">Fiziksel eldeki miktar Tesis=%1, Ambar=%2, Stok durumu = Mevcut, Parti numarası=%3, Sahip=%4: Stokta yalnızca 0,00 mevcut olduğundan %5 ayrılamaz.</span><span class="sxs-lookup"><span data-stu-id="eb151-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="eb151-125">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="eb151-125">Issue resolution</span></span>

<span data-ttu-id="eb151-126">Bu sorun büyük olasılıkla açık olan bir iş nedeniyle oluşur.</span><span class="sxs-lookup"><span data-stu-id="eb151-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="eb151-127">İşi tamamlayın ya da iş oluşturma işlemi olmadan alın.</span><span class="sxs-lookup"><span data-stu-id="eb151-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="eb151-128">Hiçbir stok hareketinin fiziksel olarak miktar ayırmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="eb151-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="eb151-129">Örneğin, bu hareketler açık kalite emirleri, stok bloke kayıtları veya çıkış emirleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="eb151-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

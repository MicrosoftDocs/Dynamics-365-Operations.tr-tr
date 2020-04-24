---
title: Servis durumu ve ilerleme alanı etkileşimi
description: Servis siparişleri formunda, servis siparişi başlığındaki İlerleme alanı, tüm servis siparişinin durumunu yansıtır ve Durum tek tek servis siparişi satırlarının durumlarını rapor eder.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207336"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="16b85-103">Servis durumu ve ilerleme alanı etkileşimi</span><span class="sxs-lookup"><span data-stu-id="16b85-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="16b85-104">**Servis siparişleri** formunda, servis siparişi başlığındaki **İlerleme** alanı, tüm servis siparişinin durumunu yansıtır ve **Durum** tek tek servis siparişi satırlarının durumlarını rapor eder.</span><span class="sxs-lookup"><span data-stu-id="16b85-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16b85-105">İlerleme</span><span class="sxs-lookup"><span data-stu-id="16b85-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="16b85-106">Satır 1 Durumu</span><span class="sxs-lookup"><span data-stu-id="16b85-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="16b85-107">Satır 2 Durumu</span><span class="sxs-lookup"><span data-stu-id="16b85-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="16b85-108">Satır 3 Durumu</span><span class="sxs-lookup"><span data-stu-id="16b85-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16b85-109"><strong>İşlemde</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-110"><strong>Oluşturuldu</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-111"><strong>Oluşturuldu</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-112"><strong>Oluşturuldu</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16b85-113"><strong>İşlemde</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-114"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-115"><strong>Oluşturuldu</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-116"><strong>Oluşturuldu</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16b85-117"><strong>İşlemde</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-118"><strong>Oluşturuldu</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-119"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-120"><strong>Deftere nakledildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16b85-121"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-122"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-123"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-124"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16b85-125"><strong>Deftere nakledildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-126"><strong>Deftere nakledildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-127"><strong>Deftere nakledildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-128"><strong>Deftere nakledildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16b85-129"><strong>Deftere nakledildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-130"><strong>Deftere nakledildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-131"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="16b85-132"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="16b85-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16b85-133">Tüm satırların durumu **Oluşturuldu** ise, servis siparişinin ilerlemesi devam ediyordur; satırlardan bazısının durumu **İptal edildi** ya da **Deftere nakledildi** ise işleme devam ediyordur.</span><span class="sxs-lookup"><span data-stu-id="16b85-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="16b85-134">Servis siparişindeki tüm satırlar **Deftere nakledildi** olarak işaretlenmişse, sipariş durumunun ilerlemesi **Deftere nakledildi**'dir.</span><span class="sxs-lookup"><span data-stu-id="16b85-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="16b85-135">Bazı satırlar **Deftere nakledildi** ve bazıları **İptal edildi** ise, ilerleme hala **Deftere nakledildi** şeklindedir.</span><span class="sxs-lookup"><span data-stu-id="16b85-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  



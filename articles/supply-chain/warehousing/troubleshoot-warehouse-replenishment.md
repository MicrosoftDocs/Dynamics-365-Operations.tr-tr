---
title: Ambar stok yenileme sorunlarını giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644885"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="49e27-103">Ambar stok yenileme sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="49e27-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49e27-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="49e27-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="49e27-105">"%1 kimlikli iş, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir hata iletisi alıyorum.</span><span class="sxs-lookup"><span data-stu-id="49e27-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="49e27-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="49e27-106">Issue description</span></span>

<span data-ttu-id="49e27-107">Bağımlı stok yenileme işi nedeniyle malzeme çekme işi engellenmiştir.</span><span class="sxs-lookup"><span data-stu-id="49e27-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="49e27-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="49e27-108">Issue resolution</span></span>

<span data-ttu-id="49e27-109">Dalga talep stok yenilemesini kullandığınızda, kaynak sipariş talebini yerine getirmek için bir malzeme çekme konumunda stoğun yenilenmesi gerekiyorsa sistem hem stok yenileme işini, hem de malzeme çekme işini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49e27-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="49e27-110">Ancak, stok yenileme işi tamamlanana kadar malzeme çekme işini engeller.</span><span class="sxs-lookup"><span data-stu-id="49e27-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="49e27-111">Bu davranış kasıtlı yapılır çünkü stok yenileme işi tamamlanana kadar malzeme çekme konumunda stok yeterli olmaz.</span><span class="sxs-lookup"><span data-stu-id="49e27-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="49e27-112">Stok yenileme işini tamamlayın ve sonra malzeme çekme işini işleyin.</span><span class="sxs-lookup"><span data-stu-id="49e27-112">Complete the replenishment work, and then process the picking work.</span></span>

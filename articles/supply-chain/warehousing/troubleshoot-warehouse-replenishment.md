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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993912"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="6bf63-103">Ambar stok yenileme sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="6bf63-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bf63-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6bf63-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="6bf63-105">"%1 kimlikli iş, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir hata iletisi alıyorum.</span><span class="sxs-lookup"><span data-stu-id="6bf63-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6bf63-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6bf63-106">Issue description</span></span>

<span data-ttu-id="6bf63-107">Bağımlı stok yenileme işi nedeniyle malzeme çekme işi engellenmiştir.</span><span class="sxs-lookup"><span data-stu-id="6bf63-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6bf63-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6bf63-108">Issue resolution</span></span>

<span data-ttu-id="6bf63-109">Dalga talep stok yenilemesini kullandığınızda, kaynak sipariş talebini yerine getirmek için bir malzeme çekme konumunda stoğun yenilenmesi gerekiyorsa sistem hem stok yenileme işini, hem de malzeme çekme işini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6bf63-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="6bf63-110">Ancak, stok yenileme işi tamamlanana kadar malzeme çekme işini engeller.</span><span class="sxs-lookup"><span data-stu-id="6bf63-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="6bf63-111">Bu davranış kasıtlı yapılır çünkü stok yenileme işi tamamlanana kadar malzeme çekme konumunda stok yeterli olmaz.</span><span class="sxs-lookup"><span data-stu-id="6bf63-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="6bf63-112">Stok yenileme işini tamamlayın ve sonra malzeme çekme işini işleyin.</span><span class="sxs-lookup"><span data-stu-id="6bf63-112">Complete the replenishment work, and then process the picking work.</span></span>

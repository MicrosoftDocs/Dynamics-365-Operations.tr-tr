---
title: Ambar stok yenileme sorunlarını giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
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
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828094"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="28bef-103">Ambar stok yenileme sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="28bef-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28bef-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="28bef-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="28bef-105">"%1 kimlikli iş, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir hata iletisi alıyorum.</span><span class="sxs-lookup"><span data-stu-id="28bef-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="28bef-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="28bef-106">Issue description</span></span>

<span data-ttu-id="28bef-107">Bağımlı stok yenileme işi nedeniyle malzeme çekme işi engellenmiştir.</span><span class="sxs-lookup"><span data-stu-id="28bef-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="28bef-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="28bef-108">Issue resolution</span></span>

<span data-ttu-id="28bef-109">Dalga talep stok yenilemesini kullandığınızda, kaynak sipariş talebini yerine getirmek için bir malzeme çekme konumunda stoğun yenilenmesi gerekiyorsa sistem hem stok yenileme işini, hem de malzeme çekme işini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="28bef-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="28bef-110">Ancak, stok yenileme işi tamamlanana kadar malzeme çekme işini engeller.</span><span class="sxs-lookup"><span data-stu-id="28bef-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="28bef-111">Bu davranış kasıtlı yapılır çünkü stok yenileme işi tamamlanana kadar malzeme çekme konumunda stok yeterli olmaz.</span><span class="sxs-lookup"><span data-stu-id="28bef-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="28bef-112">Stok yenileme işini tamamlayın ve sonra malzeme çekme işini işleyin.</span><span class="sxs-lookup"><span data-stu-id="28bef-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
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
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263216"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="07675-103">Ambar stok yenileme sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="07675-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07675-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar stok yenileme ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="07675-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="07675-105">"%1 kimlikli iş, bitmemiş stok yenileme işi nedeniyle engellenemez" şeklinde bir hata iletisi alıyorum.</span><span class="sxs-lookup"><span data-stu-id="07675-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="07675-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="07675-106">Issue description</span></span>

<span data-ttu-id="07675-107">Bağımlı stok yenileme işi nedeniyle malzeme çekme işi engellenmiştir.</span><span class="sxs-lookup"><span data-stu-id="07675-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="07675-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="07675-108">Issue resolution</span></span>

<span data-ttu-id="07675-109">Dalga talep stok yenilemesini kullandığınızda, kaynak sipariş talebini yerine getirmek için bir malzeme çekme konumunda stoğun yenilenmesi gerekiyorsa sistem hem stok yenileme işini, hem de malzeme çekme işini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07675-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="07675-110">Ancak, stok yenileme işi tamamlanana kadar malzeme çekme işini engeller.</span><span class="sxs-lookup"><span data-stu-id="07675-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="07675-111">Bu davranış kasıtlı yapılır çünkü stok yenileme işi tamamlanana kadar malzeme çekme konumunda stok yeterli olmaz.</span><span class="sxs-lookup"><span data-stu-id="07675-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="07675-112">Stok yenileme işini tamamlayın ve sonra malzeme çekme işini işleyin.</span><span class="sxs-lookup"><span data-stu-id="07675-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
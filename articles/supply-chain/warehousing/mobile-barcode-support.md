---
title: Mobil barkod desteği
description: Bu konu, Ambar mobil tarama uygulamasının Android uyumlu cihazlarda nasıl ele alınacağını açıklar.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0612833391cf7690343b7180f11d49ba1ad92d24
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439263"
---
# <a name="mobile-barcode-support"></a><span data-ttu-id="1506f-103">Mobil barkod desteği</span><span class="sxs-lookup"><span data-stu-id="1506f-103">Mobile barcode support</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1506f-104">Android bir açık kaynak projesi olduğu için, ambar barkod tarayıcı üreten tüm donanım üreticileri Android işletim sistemini çalıştıran için bir cihaz oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="1506f-104">Because Android is an open source project, any manufacturer of hardware for warehouse bar code scanners can build a device to run the Android operating system.</span></span> <span data-ttu-id="1506f-105">Bir cihaz, yalnızca Android yürütme ortamı için yazılan uygulamaları yürütebilmesi durumunda Android uyumlu olur.</span><span class="sxs-lookup"><span data-stu-id="1506f-105">A device is only Android-compatible if it can run apps that are written for the Android execution environment.</span></span>
<span data-ttu-id="1506f-106">Ancak, bir donanım satıcısı kendi donanımında çalışan Android sürümü için alt katmanları değiştirebilir veya alt katmanlar oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="1506f-106">However, a hardware vendor can modify and create overlays for the Android version that runs on their hardware.</span></span> <span data-ttu-id="1506f-107">Microsoft Android için bir mobil barkod tarama uygulamasının bir üreticinin barkod tarama donanımıyla ve bu donanımda çalışan Android sürümüyle uyumlu olmasını sağlamak konusunda herhangi bir sorumluluk alamaz.</span><span class="sxs-lookup"><span data-stu-id="1506f-107">Microsoft cannot take any responsibility to ensure that a mobile bar code scanning app for Android is compatible with a manufacturer’s bar code scanning hardware and the Android version that runs on it.</span></span> 

<span data-ttu-id="1506f-108">Dynamics 365 Supply Chain Management - Ambar uygulaması, Android ile çalışan bazı cihazlar ile barkod tarama için test edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1506f-108">The Dynamics 365 Supply Chain Management - warehouse app has been tested with a selection of Android powered devices for bar code scanning.</span></span> <span data-ttu-id="1506f-109">Bu testleri yalnızca pazarda bulunan cihazlardan bazı örnekleri içerir.</span><span class="sxs-lookup"><span data-stu-id="1506f-109">These tests only cover a sample of the devices that are available on the market.</span></span>

<span data-ttu-id="1506f-110">Müşteri olarak, satın almak istediğiniz donanıma karar vermeden önce Ambar mobil uygulamasını seçilen donanımda test etmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="1506f-110">As a customer, we recommend that you test the Warehouse mobile scanning app on selected hardware before you decide on the hardware that you want to buy.</span></span>


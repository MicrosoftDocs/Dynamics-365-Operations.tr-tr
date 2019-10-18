---
title: İş kartı cihazından plaka kontrollü bir yerleşime tamamlandı olarak bildirme
description: Bu konu, yerleşimi bir plaka kontrol ediyorsa bir üretim emrindeki bitmiş ürünleri bir stoka tamamlamaya ilişkin süreci açıklamaktadır.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995154"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="3fec1-103">İş kartı cihazından plaka kontrollü bir yerleşime tamamlandı olarak bildirme</span><span class="sxs-lookup"><span data-stu-id="3fec1-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="3fec1-104">Tamamlandı bildirimi ile çağrılan süreç, bir üretim emrindeki bitmiş ürünleri stoka tamamlar.</span><span class="sxs-lookup"><span data-stu-id="3fec1-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="3fec1-105">Bitmiş ürün gelişmiş ambar süreçleri için etkinleştirilmişse, o ürün, üretim çıkış yerleşimi adı verilen bir yerleşime tamamlandı olarak bildirilir.</span><span class="sxs-lookup"><span data-stu-id="3fec1-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="3fec1-106">Üretim çıkış yerleşiminin ayarlanması hakkında bilgi için [Üretim çıkış yerleşimi](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="3fec1-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="3fec1-107">Bu görevi tamamlamak için, varolan bir plaka numarasını seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="3fec1-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="3fec1-108">Üretim çıkış yerleşimi, plaka tarafından izlenmeye ayarlanmışsa, üretim çıkış yerleşimine tamamlandı olarak bildirilirken bir plaka numarası eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="3fec1-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="3fec1-109">**Plaka** alanı, **İş kartı cihazı** sayfasındaki **İlerlemeyi bildir** komut isteminde görünür durumdadır.</span><span class="sxs-lookup"><span data-stu-id="3fec1-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="3fec1-110">Alan **İlerlemeyi bildir** komut isteminde yalnızca üretim emrinin son işlemi bildirilirken görünür.</span><span class="sxs-lookup"><span data-stu-id="3fec1-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="3fec1-111">Alan yalnızca üretim emrine ait madde ambar yönetim süreçleri için etkinleştirildiğinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3fec1-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 

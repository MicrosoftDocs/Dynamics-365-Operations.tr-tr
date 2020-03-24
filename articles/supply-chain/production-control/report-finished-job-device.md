---
title: İş kartı cihazından plaka kontrollü bir yerleşime tamamlandı olarak bildirme
description: Bu konu, yerleşimi bir plaka kontrol ediyorsa bir üretim emrindeki bitmiş ürünleri bir stoka tamamlamaya ilişkin süreci açıklamaktadır.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092580"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="2c636-103">İş kartı cihazından plaka kontrollü bir yerleşime tamamlandı olarak bildirme</span><span class="sxs-lookup"><span data-stu-id="2c636-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="2c636-104">Tamamlandı bildirimi ile çağrılan süreç, bir üretim emrindeki bitmiş ürünleri stoka tamamlar.</span><span class="sxs-lookup"><span data-stu-id="2c636-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="2c636-105">Bitmiş ürün gelişmiş ambar süreçleri için etkinleştirilmişse, o ürün, üretim çıkış yerleşimi adı verilen bir yerleşime tamamlandı olarak bildirilir.</span><span class="sxs-lookup"><span data-stu-id="2c636-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="2c636-106">Üretim çıkış yerleşiminin ayarlanması hakkında bilgi için [Üretim çıkış yerleşimi](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="2c636-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="2c636-107">Üretim çıkış konumu lisans levhası denetimli ise, tamamlandı bildirimi yapılırken bir lisans kalıbının sağlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2c636-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="2c636-108">**Plaka** alanı, **İş kartı cihazı** sayfasındaki **İlerlemeyi bildir** komut isteminde görünür durumdadır.</span><span class="sxs-lookup"><span data-stu-id="2c636-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="2c636-109">Alan yalnızca, üretim emrinin son operasyonunu raporlarken **rapor ilerleme durumu** satırında görünür ve üretim emri için madde ambar yönetim işlemleri için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2c636-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="2c636-110">Lisans levhası sağlamak için iki seçenek vardır</span><span class="sxs-lookup"><span data-stu-id="2c636-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="2c636-111">Kullanıcı, lisans levhası alanında varolan bir lisans levhasını seçer.</span><span class="sxs-lookup"><span data-stu-id="2c636-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="2c636-112">Lisans levhası otomatik olarak bir numara serisinden üretilir ve lisans levhası alanına varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2c636-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="2c636-113">Lisans kalıbının otomatik olarak oluşturulmasına izin seçeneği, **Cihazlar için iş kartını konfigüre et** sayfasında **lisans levhası oluştur** seçeneği seçilerek konfigüre edilir.</span><span class="sxs-lookup"><span data-stu-id="2c636-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>

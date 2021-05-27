---
title: Malzeme çekme listesi kaydı sırasında konum seçildiğinde hata oluşur
description: Malzeme çekme listesi kaydı sırasında konum seçildiğinde hata oluşur.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026967"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="d3a31-103">Malzeme çekme listesi kaydı sırasında konum seçildiğinde hata oluşur</span><span class="sxs-lookup"><span data-stu-id="d3a31-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="d3a31-104">KB numarası: 4613106</span><span class="sxs-lookup"><span data-stu-id="d3a31-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="d3a31-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="d3a31-105">Symptoms</span></span>

<span data-ttu-id="d3a31-106">Bu sorun, sisteminiz satış siparişlerini otomatik olarak rezerve etmek üzere yapılandırıldığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="d3a31-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="d3a31-107">Malzeme çekme listesi kayıt satırının konumunu seçmeyi denerseniz, ambar yönetimi (WMS) rezervasyon işlemlerini kullandığınızda aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="d3a31-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="d3a31-108">Miktar, yeni boyutlarla güncelleştirilemiyor</span><span class="sxs-lookup"><span data-stu-id="d3a31-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="d3a31-109">Belirtilen bir konumda yeterli eldeki stok olmadığı için bu sorun oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="d3a31-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="d3a31-110">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="d3a31-110">Resolution</span></span>

<span data-ttu-id="d3a31-111">Sistem, beklendiği şekilde davranıyordur.</span><span class="sxs-lookup"><span data-stu-id="d3a31-111">The system is behaving as designed.</span></span>

<span data-ttu-id="d3a31-112">Ambar düzeyinde rezervasyon işlemini kullandığınız senaryolarda, eldeki stok tüm stok boyutları için rezerve edilemez ve belirtilen bir konumda eldeki stokta yeterli değilse, malzeme çekme satırından el ile rezervasyon işlemini kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="d3a31-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="d3a31-113">Daha sonra, mevcut eldeki miktarların tümü için konum gibi alt rezervasyonları dağıtmak amacıyla *Lot rezerve et* işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3a31-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>

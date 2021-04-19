---
title: Zaman pencereleri
description: Servis siparişi satırlarının planlamasını en iyi duruma getirmek için zaman aralıkları kullanabilirsiniz.
author: ShylaThompson
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99a958c76e8bd31b57e3f89b2be45028c0597a58
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824306"
---
# <a name="time-windows"></a><span data-ttu-id="7cb80-103">Zaman pencereleri</span><span class="sxs-lookup"><span data-stu-id="7cb80-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cb80-104">Servis siparişi satırlarının planlamasını en iyi duruma getirmek için zaman aralıkları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cb80-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="7cb80-105">Sistemi otomatik olarak sistem siparişleri oluşturacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cb80-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="7cb80-106">Zaman aralığı tarafından belirlenen ölçütleri temel alarak olabildiğince az sayıda servis siparişine olabildiğince çok servis siparişi satırı bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cb80-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="7cb80-107">Zaman aralıkları, servis siparişi satırının hesaplanan tarih itibariyle ne kadar ilerlediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7cb80-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="7cb80-108">Hesaplanan tarih, servis siparişi satırının gerçekleştirilmesinin planlandığı tarihtir.</span><span class="sxs-lookup"><span data-stu-id="7cb80-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="7cb80-109">Tarih, aralık ayarı ve **Servis siparişleri oluşturma** sayfasında tanımladığınız servis dönemini temel alır.</span><span class="sxs-lookup"><span data-stu-id="7cb80-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="7cb80-110">Zaman aralığını aşağıdaki tablodaki değerleri kullanarak tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="7cb80-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="7cb80-111">Yöntem</span><span class="sxs-lookup"><span data-stu-id="7cb80-111">Method</span></span> | <span data-ttu-id="7cb80-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="7cb80-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb80-113">Hafta</span><span class="sxs-lookup"><span data-stu-id="7cb80-113">Week</span></span>   | <span data-ttu-id="7cb80-114">Servis siparişi satırı, ilk hesaplanan tarihle aynı hafta içindeki herhangi bir açık güne taşınabilir.</span><span class="sxs-lookup"><span data-stu-id="7cb80-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="7cb80-115">Ay</span><span class="sxs-lookup"><span data-stu-id="7cb80-115">Month</span></span>  | <span data-ttu-id="7cb80-116">Servis siparişi satırı, ilk hesaplanan tarihle aynı ay içindeki herhangi bir açık güne taşınabilir.</span><span class="sxs-lookup"><span data-stu-id="7cb80-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="7cb80-117">Örneğin, servis siparişi satırının hesaplanan tarihi 15 Şubat 2017 olsun.</span><span class="sxs-lookup"><span data-stu-id="7cb80-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="7cb80-118">Servis siparişi satırı 1 Şubat ile 28 Şubat 2017 tarihleri arasındaki herhangi bir haftaya planlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7cb80-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="7cb80-119">El ile</span><span class="sxs-lookup"><span data-stu-id="7cb80-119">Manual</span></span> | <span data-ttu-id="7cb80-120">Servis siparişi satırının ilk hesaplanan tarihten önce veya sonra taşınabileceği maksimum gün sayısını tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="7cb80-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="7cb80-121">Servis sözleşmesi satırı için zaman aralığı belirtmediyseniz servis sözleşmesinden türetilen servis siparişi satırı tam olarak ilk planlandığı tarihte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7cb80-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cb80-122">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="7cb80-122">Related topics</span></span>

[<span data-ttu-id="7cb80-123">Zaman pencereleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="7cb80-123">Create time windows</span></span>](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
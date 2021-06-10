---
title: Konteyner ağırlığını ve hacmini yüke dahil etme
description: Bu konu, yüklerdeki konteyner ağırlığı ve hacmi dahil etmek için işlevi ayarlamayı ve uygulamayı açıklar.
author: Henrikan
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9196e9c4ce1a8aa629400b8bf379e7164a797b85
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102651"
---
# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="6cd49-103">Konteyner ağırlığını ve hacmini yüke dahil etme</span><span class="sxs-lookup"><span data-stu-id="6cd49-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cd49-104">Konteyner ağırlığı ve hacmini bir yükte ekleme işlevi, bir yükte giden konteynerlerin ve maddelerin toplam ağırlığı ve hacmi hakkında net bir görünüm verir.</span><span class="sxs-lookup"><span data-stu-id="6cd49-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="6cd49-105">Bir yük, tek bir sevkiyat veya birden fazla sevkiyat içerir ve bu sevkiyatlar, tek bir satış siparişine veya birden fazla satış siparişine ait farklı öğeler içerir.</span><span class="sxs-lookup"><span data-stu-id="6cd49-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="6cd49-106">Maddeler bir konteyner içerisinde depolanır ve konteyner bir yüke yüklenir.</span><span class="sxs-lookup"><span data-stu-id="6cd49-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="6cd49-107">Bir konteyner dışındaki maddeler de yükün parçası olabilir.</span><span class="sxs-lookup"><span data-stu-id="6cd49-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="6cd49-108">Bu koşullara dayalı olarak, sistem yükteki ağırlık ve hacmin değerlerini, hem konteynerlerin hem de maddelerin yükünü ve hacmini dikkate alarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="6cd49-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="6cd49-109">Hesaplanan değerler hassas değilse, yük üzerindeki gerçek ağırlık ve hacimleri girerek bunları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6cd49-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="6cd49-110">Ağırlık ve hacim için değerler taşıma yönetimi işleminde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6cd49-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="6cd49-111">Örneğin, değerler rota oranı workbenchinde kullanılır, burada yükler için rota ve oranı belirlemeye yardımcı olurlar ve ayrıca taşıma ödemesi ve sürücü girişi için de kullanılırlar.</span><span class="sxs-lookup"><span data-stu-id="6cd49-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="6cd49-112">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="6cd49-112">Where it applies</span></span>

<span data-ttu-id="6cd49-113">Bir yükteki konteyner ağırlığını ve hacmini dahil etmek, taşıma yönetimi işlemine uygulanır; örneğin rota oranı workbench'i, taşıma ödemeleri veya sürücü girişi gibi.</span><span class="sxs-lookup"><span data-stu-id="6cd49-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="6cd49-114">Nasıl ayarlanır</span><span class="sxs-lookup"><span data-stu-id="6cd49-114">How it is set up</span></span>

<span data-ttu-id="6cd49-115">Bir yük için dikkate alınacak konteynerlerin sayısı, konteynerin ağırlığı ve hacmine ve kullanılan konteynerin yüzdesine dayanarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="6cd49-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="6cd49-116">Bir konteyner için ağırlık ve hacmi ayarlamak için **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner türleri** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6cd49-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="6cd49-117">Konteyner kullanım yüzdesini ayarlamak için **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner grupları** üzerine tıklayın ve **Konteyner kullanım yüzdesi** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6cd49-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
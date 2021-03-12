---
title: Taşıma yönetimi durumları
description: Bu konuda, bir taşıma durumunun nasıl oluşturulacağı ve o durumun bir taşıyıcı durumuna nasıl eşleneceği açıklanmaktadır.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9d3ed4b73f909b50e97c971a37c548c8c4a9e620
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006478"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="ce7c7-103">Taşıma yönetimi durumları</span><span class="sxs-lookup"><span data-stu-id="ce7c7-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce7c7-104">Sevkiyat taşıyıcılarınız tarafından sağlanan kodları yorumlamak üzere taşıma durumları için ana kodları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="ce7c7-105">Bu, durum sağlamak için sevkiyat taşıyıcıları ile tümleştirme yapmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="ce7c7-106">Taşıma ana durum kodu için sağladığınız taşıma durumu; yük, sevkiyat veya konteyner durumunu izlemenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="ce7c7-107">Bir yük, sevkiyat veya konteyner için belirli bir taşıma durumu yalnızca veri tümleştirmesi aracılığıyla güncelleştirilebilir ve kullanıcı arabirimi aracılığıyla el ile yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="ce7c7-108">Taşıma durumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ce7c7-108">Create a transportation status</span></span>

<span data-ttu-id="ce7c7-109">Taşıma durumu oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="ce7c7-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="ce7c7-110">**Taşımacılık yönetimi \> Kurulum \> Taşıma ana durumları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="ce7c7-111">Taşıma ana durumu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="ce7c7-112">**Taşıma ana durumu** alanında, taşıma durumu için benzersiz bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="ce7c7-113">**Taşıma türü** alanında, taşıma türü olarak *Sevkiyat taşıyıcısı* veya *Hub*'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="ce7c7-114">Bir ad ve taşıma durumu girin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="ce7c7-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="ce7c7-116">Taşıma durumunu bir taşıyıcı durumuna eşleme</span><span class="sxs-lookup"><span data-stu-id="ce7c7-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="ce7c7-117">Taşıma durumunu bir taşıyıcı durumuna eşlemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="ce7c7-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="ce7c7-118">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Taşıyıcı taşıma durumu** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="ce7c7-119">Sevkiyat taşıyıcısı kodunu taşıma durumu ana koduyla eşlemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="ce7c7-120">Sevkiyat taşıyıcısı ve taşıyıcı hizmeti için benzersiz kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="ce7c7-121">Seçili sevkiyat taşıyıcısı koduyla eşleştirmek istediğiniz taşıma durumu kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="ce7c7-122">Sevkiyat taşıyıcısı tarafından kullanılan harici kodu girin.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="ce7c7-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ce7c7-123">Close the page.</span></span>

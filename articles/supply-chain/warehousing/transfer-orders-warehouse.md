---
title: Transfer emirleri için ambarlar ayarlama
description: Bu konu, transfer emirleri için ambarlar nasıl ayarlayabileceğinizi açıklar.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e482567eb92b9ab891d41d82d10cbb87f9b7fb01
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017495"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="606cb-103">Transfer emirleri için ambarlar ayarlama</span><span class="sxs-lookup"><span data-stu-id="606cb-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="606cb-104">Ambarlar arası transfer emirlerini destekleyen bir hiyerarşi oluşturmak için ambar düzeylerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="606cb-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="606cb-105">Master planlama, bu kurulumu temel alarak madde gereksinimlerini tek tek ambar düzeyinde hesaplar ve bunları karşılamak üzere, atanmış bir kaynak ambardan planlı transfer emirleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="606cb-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="606cb-106">**Stok yönetimi > Kurulum > Stok dökümü > Ambarlar** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="606cb-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="606cb-107">Stok yenilemesi yapmak istediğiniz ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="606cb-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="606cb-108">**Master planlama** hızlı sekmesinde, **Yeniden doldurma** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="606cb-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="606cb-109">**Ana ambar** alanında, stok yenileme ambarı olarak atamak istediğiniz ambarı seçin.</span><span class="sxs-lookup"><span data-stu-id="606cb-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="606cb-110">Master planlama seçilen ambara ait transfer gereksinimini hesaplayıp atanmış **Ana ambar** noktasından bir planlı transfer emri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="606cb-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="606cb-111"><STRONG>Dolum</STRONG> onay kutusunu alanını silerseniz, seçili ambara <STRONG>Ana ambar</STRONG>'a göre bir ambar düzeyi atanır, ancak <STRONG>Ana ambar</STRONG> bir dolum ambarı olarak ayarlanmaz.</span><span class="sxs-lookup"><span data-stu-id="606cb-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="606cb-112">Yeni kurulumu uygulamak için sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="606cb-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="606cb-113">Yeniden dolum için ambar atamak isterseniz, önce bu ambarı bir stok boyutu olarak <STRONG>Stok boyutu grupları</STRONG> sayfasında ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="606cb-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="606cb-114">Bu sayfada <STRONG>Etkin</STRONG> alanını ve <STRONG>Boyuta göre kapsama planı</STRONG> alanını ambar için seçin.</span><span class="sxs-lookup"><span data-stu-id="606cb-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="606cb-115">Taşıma sağlama süresi ayarlama</span><span class="sxs-lookup"><span data-stu-id="606cb-115">Set up transport lead time</span></span>

<span data-ttu-id="606cb-116">**Taşıma günü** sayfasında ambarlar arasındaki taşıma sağlama sürelerini de ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="606cb-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="606cb-117">**Stok yönetimi > Kurulum > Dağıtım > Taşıma günleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="606cb-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="606cb-118">**Alım noktası** alanında, **ambar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="606cb-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="606cb-119">**Sevkiyat ambarı** , **Alım ambarı** ve **Taşıma günleri** 'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="606cb-119">Select the **Shipping warehouse** , **Receiving warehouse** , and **Transport days**.</span></span> 
4. <span data-ttu-id="606cb-120">(İsteğe bağlı) Taşıma şekline bağlı olarak taşıma süresini de **Teslimat türüne göre taşıma günleri** sekmesinde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="606cb-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>

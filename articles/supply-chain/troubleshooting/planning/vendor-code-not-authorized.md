---
title: Satıcı kodu belirli bir ürün ve tarih için yetkilendirilmemiş
description: Planlı siparişi kesinleştirmeyi veya satınalma siparişine satır eklemeyi denediğinizde, satıcı kodunun bir ürün ve tarih için yetkilendirilmemiş olduğunu belirten bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294203"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="851a9-103">Satıcı kodu belirli bir ürün ve tarih için yetkilendirilmemiş</span><span class="sxs-lookup"><span data-stu-id="851a9-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="851a9-104">Hata kodu: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="851a9-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="851a9-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="851a9-105">Symptoms</span></span>

<span data-ttu-id="851a9-106">Planlı siparişi kesinleştirmeye veya bir satınalma siparişine satır eklemeye çalıştığınızda, aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="851a9-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="851a9-107">%1 satıcı kodu %3 konumundaki %2 için yetkili değil.</span><span class="sxs-lookup"><span data-stu-id="851a9-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="851a9-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="851a9-108">Cause</span></span>

<span data-ttu-id="851a9-109">Bu hata, **Onaylanan satıcı denetimi yöntemi** alanı belirtilen ürün için *Yalnızca uyarı* veya *İzin verilmiyor* olarak ayarlandığı ve satıcı o ürünü tedarik yetkisine sahip olmadığı için oluşur.</span><span class="sxs-lookup"><span data-stu-id="851a9-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="851a9-110">Çözüm</span><span class="sxs-lookup"><span data-stu-id="851a9-110">Resolution</span></span>

<span data-ttu-id="851a9-111">Bu sorunu gidermek için, ilgili ürünün satıcı denetimini devre dışı bırakın ya da satıcıyı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="851a9-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="851a9-112">Bir ürünün satıcı denetimini devre dışı bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="851a9-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="851a9-113">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="851a9-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="851a9-114">İlgili ürünü açın.</span><span class="sxs-lookup"><span data-stu-id="851a9-114">Open the relevant product.</span></span>
1. <span data-ttu-id="851a9-115">**Satınalma** hızlı sekmesinde, **Onaylanmış satıcı denetimi yöntemi** alanını *Yalnızca uyarı* veya *İzin verilmiyor* dışında bir değere ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="851a9-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="851a9-116">Ürün için satıcıyı onaylamak üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="851a9-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="851a9-117">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="851a9-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="851a9-118">İlgili maddeyi açın.</span><span class="sxs-lookup"><span data-stu-id="851a9-118">Open the relevant item.</span></span>
1. <span data-ttu-id="851a9-119">Eylem Bölmesi'nde, **Satın al** sekmesindeki **Onaylanan satıcı** grubunda **Ayar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="851a9-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="851a9-120">**Onaylanan satıcı** liste sayfasında ızgaraya satır eklemeyin ve ardından aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="851a9-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="851a9-121">**Satıcı**: Geçerli ürün için onaylanacak satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="851a9-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="851a9-122">**Geçerlilik tarihi**: Satıcının onaylandığı ilk tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="851a9-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="851a9-123">**Sona erme tarihi**: Satıcının onaylandığı son tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="851a9-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="851a9-124">Daha fazla bilgi için bkz. [Belirli ürünler için satıcıları onaylama](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="851a9-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>

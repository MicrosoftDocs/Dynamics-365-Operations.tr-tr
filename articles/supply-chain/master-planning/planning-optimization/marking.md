---
title: Planlama İyileştirmesi ile stok işaretleme
description: Bu konuda, Planlama İyileştirmesi'ni kullandığınızda, kesinleştirilmiş siparişlerde stok işaretleme için kullanılabilir seçenekler hakkında bilgi sağlanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 236e1955dd80564e748aab1c595b017cb78e9418
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983503"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="4f948-103">Planlama İyileştirmesi ile stok işaretleme</span><span class="sxs-lookup"><span data-stu-id="4f948-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f948-104">Bu konuda, Planlama İyileştirmesi'ni kullandığınızda, kesinleştirilmiş siparişlerde stok işaretleme için kullanılabilir seçenekler hakkında bilgi sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4f948-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="4f948-105">*İşaretleme*, arz ve talebi bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4f948-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="4f948-106">Master planlamanın talebin nasıl olmasını beklediğini gösteren bir *ilişkilendirmeye* benzerdir.</span><span class="sxs-lookup"><span data-stu-id="4f948-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="4f948-107">Planlama açısından temel fark işaretlemenin ilişkilendirmeden daha kalıcı olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="4f948-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="4f948-108">İşaretleme özelliği, ilk giren ilk çıkar (FIFO) ve son giren ilk çıkar (LIFO) yaklaşımları için özel maliyetlendirme senaryolarını desteklemek üzere sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="4f948-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="4f948-109">Ancak, artık bazı maliyetlendirme dışı senaryolar için de kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4f948-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="4f948-110">Arz ve talep arasında işaretleme isteğe bağlıdır ve neredeyse kalıcıdır.</span><span class="sxs-lookup"><span data-stu-id="4f948-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="4f948-111">İşaretleme kullanıcı tarafından el ile kaldırılabileceği gibi, **İşaretlemeyi kaldır** seçeneğinin belirlendiği bir satış siparişi satırı açılımı çalıştırılarak da kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="4f948-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="4f948-112">İlişkilendirme, talebi gerekli arzla bağlamak için kapsama sırasında master planlama tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="4f948-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="4f948-113">İlişkilendirme, her planlama çalışmasının talebi kapsaması gereken arzı iyileştirmesi için güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4f948-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="4f948-114">Master planlama, ilişkilendirme bilgilerini güncelleştirdiğinde, var olan tüm işaretler korunur.</span><span class="sxs-lookup"><span data-stu-id="4f948-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="4f948-115">İlişkilendirme; ilgili işaret, eldeki rezervasyonlar ve siparişe ait rezervasyonları dahil ederek aşağıdaki sırada başlar:</span><span class="sxs-lookup"><span data-stu-id="4f948-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="4f948-116">Talep ve arz arasında işaretleme</span><span class="sxs-lookup"><span data-stu-id="4f948-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="4f948-117">Eldeki rezervasyonlar</span><span class="sxs-lookup"><span data-stu-id="4f948-117">On-hand reservations</span></span>
1. <span data-ttu-id="4f948-118">Siparişteki rezervasyonlar</span><span class="sxs-lookup"><span data-stu-id="4f948-118">On-order reservations</span></span>

<span data-ttu-id="4f948-119">Planlı bir siparişi kesinleştirirken, **Kesinleştirme** iletişim kutusu kesinleştirme sırasında oluşturulan siparişler için işaretleme seçeneklerini ayarlamak amacıyla kullanabileceğiniz bir **İşaretlemeyi güncelleştir** alanı sağlar.</span><span class="sxs-lookup"><span data-stu-id="4f948-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="4f948-120">Aşağıdaki değerlerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="4f948-120">Select one of the following values:</span></span>

- <span data-ttu-id="4f948-121">**Hayır**: Stok işaretleme uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="4f948-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="4f948-122">**Standart**: Stok işaretleme ilişkilendirmeye göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4f948-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="4f948-123">Bir karşılama siparişi (arz) karşılığında bir gereksinim siparişi (talep) işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="4f948-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="4f948-124">Bazı miktarlar, karşılama siparişinde kalırsa işaretlenmez ve başvuru bilgileri boş bırakılır.</span><span class="sxs-lookup"><span data-stu-id="4f948-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="4f948-125">Örneğin, 100 ea değerinde bir satış siparişi 150 ea değerinde bir satın alma siparişiyle ilişkilendirildirse, başvuru bilgileri yalnızca satış siparişine atanır.</span><span class="sxs-lookup"><span data-stu-id="4f948-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="4f948-126">**Genişletilmiş**: Herhangi bir miktarın karşılama siparişinde kalıp kalmadığına bakılmaksızın, hem gereksinim siparişi (talep) hem karşılama siparişi (arz) işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="4f948-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="4f948-127">Örneğin, 100 ea değerinde bir satış siparişi 150 ea değerinde bir satın alma siparişiyle ilişkilendirildirse, başvuru bilgileri hem satış siparişine hem de satın alma siparişine atanır.</span><span class="sxs-lookup"><span data-stu-id="4f948-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>

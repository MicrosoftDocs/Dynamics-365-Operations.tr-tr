---
title: Fiziksel değeri dahil et
description: Madde modeli grupları formunun Stok modeli FasTab'indeki Fiziksel değeri dahil et onay kutusu fiziksel olarak güncelleştirilmiş hareketlerin bir madde için devam eden ortalama maliyet fiyatının hesaplanmasına dahili edilip edilmeyeceğinin belirlenmesi için kullanırsınız.
author: AndersGirke
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834438f8389e295bbb992f0b8397ff45559690c3
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693009"
---
# <a name="include-physical-value"></a><span data-ttu-id="28a0f-103">Fiziksel değeri dahil et</span><span class="sxs-lookup"><span data-stu-id="28a0f-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28a0f-104">Madde modeli grupları formunun Stok modeli FasTab'indeki Fiziksel değeri dahil et onay kutusu fiziksel olarak güncelleştirilmiş hareketlerin bir madde için devam eden ortalama maliyet fiyatının hesaplanmasına dahili edilip edilmeyeceğinin belirlenmesi için kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="28a0f-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="28a0f-105">**Fiziksel değeri dahil et** onay kutusu aşağıdaki değerlere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="28a0f-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="28a0f-106">Değer</span><span class="sxs-lookup"><span data-stu-id="28a0f-106">Value</span></span>    | <span data-ttu-id="28a0f-107">Sonuç</span><span class="sxs-lookup"><span data-stu-id="28a0f-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28a0f-108">Seçildi</span><span class="sxs-lookup"><span data-stu-id="28a0f-108">Selected</span></span> | <span data-ttu-id="28a0f-109">Devam eden ortalama maliyet fiyatının hesaplanması için hem fiziksel olarak güncelleştirilen hareketler hem de mali olarak güncelleştirilen hareketler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="28a0f-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="28a0f-110">Temizlendi</span><span class="sxs-lookup"><span data-stu-id="28a0f-110">Cleared</span></span>  | <span data-ttu-id="28a0f-111">Devam eden ortalama maliyet fiyatının hesaplanması için sadece mali olarak güncelleştirilen hareketler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="28a0f-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="28a0f-112">Onay kutusu, kullandığınız stok modeline bağlı olarak bir miktar farklı etkilere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="28a0f-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="28a0f-113">FIFO (İlk giren, ilk çıkan), LIFO (Son giren, ilk çıkar) veya LIFO tarihi stok modelini kullandığınızda **Fiziksel değeri dahil et** onay kutusunu işaretlerseniz, stok kapanışı ayrıca fiziksel olarak güncelleştirilen hareketlerde de düzenlemeler yapar.</span><span class="sxs-lookup"><span data-stu-id="28a0f-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="28a0f-114">Bu stok modellerini kullandığınızda **Fiziksel değeri dahil et** onay kutusunu işaretlemezseniz, stok kapanışı yalnızca mali olarak güncelleştirilen hareketlerde kapatmalar yapar.</span><span class="sxs-lookup"><span data-stu-id="28a0f-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="28a0f-115">Ağırlıklı ortalama veya ağırlıklı ortalama tarih stok modelini kullanırken stok, **Fiziksel değeri dahil et** onay kutusunu işaretlemenizden veya işaretlememenizden bağımsız olarak yalnızca mali olarak güncelleştirilmiş hareketleri kapatır.</span><span class="sxs-lookup"><span data-stu-id="28a0f-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="28a0f-116">**Örnek 1** **Fiziksel değeri dahil et** onay kutusunu seçtiniz ve aşağıdaki satın alma emirlerini aldınız:</span><span class="sxs-lookup"><span data-stu-id="28a0f-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="28a0f-117">10,00 ABD Doları maliyet fiyatında 2 adetlik bir satınalma siparişi için sevk irsaliyesi güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="28a0f-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated.</span></span>
-   <span data-ttu-id="28a0f-118">12,00 ABD Doları maliyet fiyatında 3 adetlik bir satınalma siparişi için fatura güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="28a0f-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated.</span></span>

<span data-ttu-id="28a0f-119">Bu durumda, maliyet fiyatının hesaplanmasında hem fiziksel olarak güncelleştirilmiş hem mali olarak güncelleştirilmiş hareketler kullanıldığından, cari ortalama maliyet fiyatı 11,20 = (2x10+3x12)/(2+3) ABD Doları olur.</span><span class="sxs-lookup"><span data-stu-id="28a0f-119">In this case, the running average cost price will be USD 11.20 = (2x10+3x12)/(2+3), because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> 

<span data-ttu-id="28a0f-120">**Örnek 2** **Fiziksel değeri dahil et** onay kutusunu işaretlemezseniz ve madde kurulumundaki maliyet fiyatı 10,00 USD ise.</span><span class="sxs-lookup"><span data-stu-id="28a0f-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> 

-   <span data-ttu-id="28a0f-121">12,00 ABD Doları maliyet fiyatında 20 miktarı için sevk irsaliyesi güncelleştirilmiş bir satın alma emri alırsınız.</span><span class="sxs-lookup"><span data-stu-id="28a0f-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span>

<span data-ttu-id="28a0f-122">Bir satış siparişi nakledildiğinde, cari ortalama maliyet fiyatı fiziksel olarak nakledilmiş hareketleri içermeyeceğinden, maliyet tutarı olarak 10,00 ABD Doları nakledilir.</span><span class="sxs-lookup"><span data-stu-id="28a0f-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> 

> [!NOTE]
> <span data-ttu-id="28a0f-123">Karşılaştırma amacıyla, bu madde için **Fiziksel değeri dahil et** onay kutusunu işaretlerseniz bir satış siparişi deftere nakledildiğinde nakledilen maliyet tutarı 12,00 ABD Doları olacaktır.</span><span class="sxs-lookup"><span data-stu-id="28a0f-123">For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>

---
title: Maddenin ürün reçetesi veya formülü olamaz
description: Bir siparişi kesinleştirmeye çalıştığınızda, madde doğrulaması sırasında bir hata iletisi alırsınız. Maddenin ürün reçetesi (BOM) veya formülü olamayacağını belirtir.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294200"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="fd1b5-104">Maddenin ürün reçetesi veya formülü olamaz</span><span class="sxs-lookup"><span data-stu-id="fd1b5-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="fd1b5-105">Hata kodu: PRO2614</span><span class="sxs-lookup"><span data-stu-id="fd1b5-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="fd1b5-106">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="fd1b5-106">Symptoms</span></span>

<span data-ttu-id="fd1b5-107">Bir siparişi kesinleştirmeye çalıştığınızda, madde doğrulaması sırasında aşağıdaki hata iletisi alırsınız:</span><span class="sxs-lookup"><span data-stu-id="fd1b5-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="fd1b5-108">Madde bir ürün reçetesi veya formüle sahip olamaz</span><span class="sxs-lookup"><span data-stu-id="fd1b5-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="fd1b5-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="fd1b5-109">Resolution</span></span>

<span data-ttu-id="fd1b5-110">Ürün reçetesi (BOM) veya formülü olan maddeler *Planlama maddesi*, *BOM* veya *formül* türünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fd1b5-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="fd1b5-111">Maddenin türünü değiştirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fd1b5-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="fd1b5-112">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="fd1b5-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="fd1b5-113">İlgili ürünü açın.</span><span class="sxs-lookup"><span data-stu-id="fd1b5-113">Open the relevant product.</span></span>
1. <span data-ttu-id="fd1b5-114">**Mühendis** hızlı sekmesinde **Üretim türü** alanını *Planlama maddesi*, *BOM* veya *formül* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fd1b5-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>

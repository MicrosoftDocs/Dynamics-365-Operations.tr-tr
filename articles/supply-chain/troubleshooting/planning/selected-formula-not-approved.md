---
title: Seçili formül numarası toplu iş emri için onaylanmadı
description: Planlı bir siparişi kesinleştirmeye çalışırken, seçili formül numarasının bir toplu iş emri için onaylanmadığını bildiren bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294196"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="895cf-103">Seçili formül numarası toplu iş emri için onaylanmadı</span><span class="sxs-lookup"><span data-stu-id="895cf-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="895cf-104">Hata kodu: PRO2614</span><span class="sxs-lookup"><span data-stu-id="895cf-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="895cf-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="895cf-105">Symptoms</span></span>

<span data-ttu-id="895cf-106">Planlı siparişi kesinleştirmeye çalıştığınızda aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="895cf-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="895cf-107">Seçili formül numarası, bir toplu iş emri için onaylanmamış.</span><span class="sxs-lookup"><span data-stu-id="895cf-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="895cf-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="895cf-108">Cause</span></span>

<span data-ttu-id="895cf-109">Sistem, etkin madde için onaylanmış bir formülün kullanılabilir olduğundan emin olmak üzere kesinleştirme işlemini doğrular.</span><span class="sxs-lookup"><span data-stu-id="895cf-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="895cf-110">Formülü onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="895cf-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="895cf-111">Çözüm</span><span class="sxs-lookup"><span data-stu-id="895cf-111">Resolution</span></span>

<span data-ttu-id="895cf-112">Formülü onaylamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="895cf-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="895cf-113">**Ürün bilgi yönetimi \> Ürün reçeteleri ve formüller \> Formüller** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="895cf-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="895cf-114">İlgili formülü seçin.</span><span class="sxs-lookup"><span data-stu-id="895cf-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="895cf-115">Eylem Bölmesinde, **Formül** sekmesinde **Koru** gurubunda **Formülü onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="895cf-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="895cf-116">**Ürün reçetesini veya formülü onayla** iletişim kutusunda, bir onaylayan seçin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="895cf-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>

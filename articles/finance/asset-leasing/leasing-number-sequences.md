---
title: Numara serileri atama
description: Bu konu, kiralama kimlikleri için numara serilerinin nasıl oluşturulacağını açıklamaktadır. Ayrıca, dizin yeniden değerleme işleminde kullanılan benzersiz kimliklerin nasıl oluşturulacağı da açıklanmıştır.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0b5d622df1e5dcdf7f1322328bce7e185f8edb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819830"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="d99f3-104">Numara serileri atama</span><span class="sxs-lookup"><span data-stu-id="d99f3-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d99f3-105">Bu konu, kiralama kimlikleri için numara serilerinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d99f3-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="d99f3-106">Ayrıca, dizin yeniden değerleme işleminde kullanılan benzersiz kimliklerin nasıl oluşturulacağı da açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="d99f3-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="d99f3-107">**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d99f3-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="d99f3-108">**Numara serileri** yan sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d99f3-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="d99f3-109">Yan çubukta **Numara serileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d99f3-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="d99f3-110">**Kiralama Kimliği** referansı için bir numara serisi belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d99f3-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="d99f3-111">Bu numara serisi, her bir kiralama için benzersiz tanımlayıcı oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d99f3-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="d99f3-112">**İşlem Kimliği** referansı için bir numara serisi belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d99f3-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="d99f3-113">Bu numara serisi, her bir dizin yeniden değerleme işlemi için benzersiz tanımlayıcı oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d99f3-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="d99f3-114">**Sonlandırma Teklifi Kimliği** referansı için bir numara serisi belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d99f3-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="d99f3-115">Bu numara serisi, her bir sonlandırma teklifi için benzersiz tanımlayıcı oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d99f3-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
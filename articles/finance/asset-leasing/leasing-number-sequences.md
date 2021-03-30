---
title: Numara serileri atama
description: Bu konu, kiralama kimlikleri için numara serilerinin nasıl oluşturulacağını açıklamaktadır. Ayrıca, dizin yeniden değerleme işleminde kullanılan benzersiz kimliklerin nasıl oluşturulacağı da açıklanmıştır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 3e89fb7616aff323d5815918a37e1fccf9b7f578
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207267"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="569d2-104">Numara serileri atama</span><span class="sxs-lookup"><span data-stu-id="569d2-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="569d2-105">Bu konu, kiralama kimlikleri için numara serilerinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="569d2-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="569d2-106">Ayrıca, dizin yeniden değerleme işleminde kullanılan benzersiz kimliklerin nasıl oluşturulacağı da açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="569d2-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="569d2-107">**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="569d2-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="569d2-108">**Numara serileri** yan sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="569d2-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="569d2-109">Yan çubukta **Numara serileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="569d2-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="569d2-110">**Kiralama Kimliği** referansı için bir numara serisi belirleyin.</span><span class="sxs-lookup"><span data-stu-id="569d2-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="569d2-111">Bu numara serisi, her bir kiralama için benzersiz tanımlayıcı oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="569d2-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="569d2-112">**İşlem Kimliği** referansı için bir numara serisi belirleyin.</span><span class="sxs-lookup"><span data-stu-id="569d2-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="569d2-113">Bu numara serisi, her bir dizin yeniden değerleme işlemi için benzersiz tanımlayıcı oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="569d2-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="569d2-114">**Sonlandırma Teklifi Kimliği** referansı için bir numara serisi belirleyin.</span><span class="sxs-lookup"><span data-stu-id="569d2-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="569d2-115">Bu numara serisi, her bir sonlandırma teklifi için benzersiz tanımlayıcı oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="569d2-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
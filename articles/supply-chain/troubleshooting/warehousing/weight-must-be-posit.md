---
title: Ağırlık pozitif olmalıdır
description: Ağırlık pozitif olmalıdır
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924315"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="ceaa0-103">Ağırlık pozitif olmalıdır</span><span class="sxs-lookup"><span data-stu-id="ceaa0-103">Weight must be positive</span></span>

<span data-ttu-id="ceaa0-104">Hata kodu: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="ceaa0-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="ceaa0-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="ceaa0-105">Symptoms</span></span>

<span data-ttu-id="ceaa0-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="ceaa0-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ceaa0-107">Ağırlık pozitif olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ceaa0-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="ceaa0-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="ceaa0-108">Cause</span></span>

<span data-ttu-id="ceaa0-109">**Brüt Ağırlık** alanı *0* (sıfır) veya negatif değer olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ceaa0-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="ceaa0-110">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="ceaa0-110">Resolution</span></span>

<span data-ttu-id="ceaa0-111">Bir ağırlık belirlemem için aşağıdaki adımlardan birini izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceaa0-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="ceaa0-112">**Brüt ağırlık** alanında bir değer belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ceaa0-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="ceaa0-113">Ardından açılan listede bir birim seçin.</span><span class="sxs-lookup"><span data-stu-id="ceaa0-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="ceaa0-114">**Brüt ağırlık** değerini hesaplamak için **Sistem ağırlığını al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceaa0-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>

---
title: Serbest bırakılmış ürünler V2 varlığını kullanarak bir maddeyi içe aktaramazsınız
description: Serbest bırakılmış ürünler V2 varlığını kullanarak bir maddeyi içe aktaramazsınız.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026975"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="ac106-103">Serbest bırakılmış ürünler V2 varlığını kullanarak bir maddeyi içe aktaramazsınız</span><span class="sxs-lookup"><span data-stu-id="ac106-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="ac106-104">KB numarası: 4611825</span><span class="sxs-lookup"><span data-stu-id="ac106-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="ac106-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="ac106-105">Symptoms</span></span>

<span data-ttu-id="ac106-106">*Serbest bırakılmış ürünler V2* varlığını kullanarak bir maddeyi içe aktarmaya çalıştığınızda, aşağıdaki örneğe benzer bir hata iletisi alırsınız:</span><span class="sxs-lookup"><span data-stu-id="ac106-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="ac106-107">Maddeler - izleme boyutu gruplarında bir kayıt oluşturulamıyor (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="ac106-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="ac106-108">Madde Numarası: 2040663, Toplu iş.</span><span class="sxs-lookup"><span data-stu-id="ac106-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="ac106-109">Kayıt zaten var.</span><span class="sxs-lookup"><span data-stu-id="ac106-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="ac106-110">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="ac106-110">Resolution</span></span>

<span data-ttu-id="ac106-111">Yeni serbest bırakılan ürünleri içe aktarmak için, *Serbest bırakılan ürünler V2* varlığı yerine *Serbest bırakılmış ürün oluşturma V2* varlığını kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ac106-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>

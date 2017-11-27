---
title: "Tek fiş ve para birimi yeniden değerleme yükseltmesi"
description: "Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükler girer ve ayrıca Alacak hesapları veya Borç hesapları yabancı para birimi yeniden değerleme işlemini çalıştırır. Bu konuda, bu kuruluşlar Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken izlemeleri gereken adımlar açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e0cd0c96ad0f30d56eefdc46a0a69160d864175
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="d75f9-104">Tek fiş ve para birimi yeniden değerleme yükseltmesi</span><span class="sxs-lookup"><span data-stu-id="d75f9-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d75f9-105">Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükler girer ve ayrıca Alacak hesapları veya Borç hesapları yabancı para birimi yeniden değerleme işlemini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d75f9-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="d75f9-106">Bu konuda, bu kuruluşlar Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken izlemeleri gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d75f9-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="d75f9-107">Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d75f9-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="d75f9-108">Dynamics 365 for Operations'ı yükseltmeden önce Alacak hesapları ve Borç hesapları için yabancı para birimi yeniden değerleme işlemlerini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d75f9-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="d75f9-109">**Yöntem** alanı ayarını **Fatura tarihi** yapın.</span><span class="sxs-lookup"><span data-stu-id="d75f9-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="d75f9-110">Son yabancı para birimi yeniden değerleme işlemini tersine çeviren bir yeniden değerleme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d75f9-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="d75f9-111">Bu nedenle, açık hareketler orijinal muhasebe para birimleriyle değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d75f9-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="d75f9-112">Dynamics 365 for Operations'ı sürüm 1611'e yükseltin.</span><span class="sxs-lookup"><span data-stu-id="d75f9-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="d75f9-113">Alacak hesapları ve Borç hesapları yabancı para birimi yeniden değerleme işlemlerini yeniden çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d75f9-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="d75f9-114">Bu kez, **Yöntem** alanı ayarını **Standart** yapın.</span><span class="sxs-lookup"><span data-stu-id="d75f9-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="d75f9-115">Geçerli döviz kurları temel alınarak yeni bir yeniden değerleme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d75f9-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="d75f9-116">Bu hareket gerçekleşmemiş kazanç/kayıp ve doğru özet genel muhasebe hesabını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d75f9-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>






---
title: Tek fiş günlüklerini ve para birimi yeniden değerlemelerini yükseltme
description: Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükler girer ve ayrıca Alacak hesapları veya Borç hesapları yabancı para birimi yeniden değerleme işlemini çalıştırır. Bu konuda, bu kuruluşlar Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken izlemeleri gereken adımlar açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "328160"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="97570-104">Tek fiş günlüklerini ve para birimi yeniden değerlemelerini yükseltme</span><span class="sxs-lookup"><span data-stu-id="97570-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97570-105">Bazı kuruluşlar, birden fazla müşteri veya satıcı olan tek bir fiş içeren günlükler girer ve ayrıca Alacak hesapları veya Borç hesapları yabancı para birimi yeniden değerleme işlemini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="97570-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="97570-106">Bu konuda, bu kuruluşlar Microsoft Dynamics 365 for Operations'ı sürüm 1611'e yükseltirken izlemeleri gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="97570-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="97570-107">Microsoft Dynamics 365 for Operations sürüm 1611'e yükseltmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="97570-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="97570-108">Dynamics 365 for Operations'ı yükseltmeden önce Alacak hesapları ve Borç hesapları için yabancı para birimi yeniden değerleme işlemlerini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="97570-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="97570-109">**Yöntem** alanı ayarını **Fatura tarihi** yapın.</span><span class="sxs-lookup"><span data-stu-id="97570-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="97570-110">Son yabancı para birimi yeniden değerleme işlemini tersine çeviren bir yeniden değerleme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="97570-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="97570-111">Bu nedenle, açık hareketler orijinal muhasebe para birimleriyle değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="97570-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="97570-112">Dynamics 365 for Operations sürüm 1611'e yükseltme.</span><span class="sxs-lookup"><span data-stu-id="97570-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="97570-113">Alacak hesapları ve Borç hesapları yabancı para birimi yeniden değerleme işlemlerini yeniden çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="97570-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="97570-114">Bu kez, **Yöntem** alanı ayarını **Standart** yapın.</span><span class="sxs-lookup"><span data-stu-id="97570-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="97570-115">Geçerli döviz kurları temel alınarak yeni bir yeniden değerleme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="97570-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="97570-116">Bu hareket gerçekleşmemiş kazanç/kayıp ve doğru özet genel muhasebe hesabını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="97570-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





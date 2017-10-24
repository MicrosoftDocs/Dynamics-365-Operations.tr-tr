---
title: "Birimlerarası muhasebe için dengelenmiş günlükler"
description: "Bu makalede Genel muhasebe sayfasında bir karşı mali boyut seçildiğinde bir defterin nasıl otomatik olarak dengeleneceği açıklanmıştır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="1f8c0-103">Birimlerarası muhasebe için dengelenmiş günlükler</span><span class="sxs-lookup"><span data-stu-id="1f8c0-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1f8c0-104">Bu makalede Genel muhasebe sayfasında bir karşı mali boyut seçildiğinde bir defterin nasıl otomatik olarak dengeleneceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1f8c0-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="1f8c0-105">Muhasebe girişleri mali boyut değerleri düzeyinde dengelenmiyorsa, günlüğü dengelemek için ek hesap girişleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1f8c0-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="1f8c0-106">Bu hesap girişleri, ana hesabı belirlemek için **Otomatik hareketlere yönelik hesaplar** sayfasındaki **Birimlerarası - borç** ve **Birimlerarası - kredi** deftere nakil türlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1f8c0-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="1f8c0-107">Örneğin, Dal, genel muhasebe hesabındaki ikinci segmenttir ve dengeleme mali boyutu olarak seçilir ve aşağıdaki muhasebe girişleri oluşturulmak üzeredir.</span><span class="sxs-lookup"><span data-stu-id="1f8c0-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="1f8c0-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="1f8c0-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="1f8c0-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="1f8c0-109">100.00 DR</span></span> |
| <span data-ttu-id="1f8c0-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="1f8c0-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="1f8c0-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="1f8c0-111">100.00 DR</span></span> |
| <span data-ttu-id="1f8c0-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="1f8c0-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="1f8c0-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="1f8c0-113">200.00 CR</span></span> |

<span data-ttu-id="1f8c0-114">Bu durumda, aşağıdaki bakiyeler belirlenir:</span><span class="sxs-lookup"><span data-stu-id="1f8c0-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="1f8c0-115">Dal MSP için = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="1f8c0-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="1f8c0-116">Dal NY için = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="1f8c0-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="1f8c0-117">Bu nedenle, günlüğü mali boyut değerlerinin düzeyinde dengelemek için aşağıdaki muhasebe girişleri otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1f8c0-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="1f8c0-118">(Birimlerarası Borç) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="1f8c0-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="1f8c0-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="1f8c0-119">100.00 DR</span></span> |
| <span data-ttu-id="1f8c0-120">(Birimlerarası Alacak) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="1f8c0-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="1f8c0-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="1f8c0-121">100.00 CR</span></span> |







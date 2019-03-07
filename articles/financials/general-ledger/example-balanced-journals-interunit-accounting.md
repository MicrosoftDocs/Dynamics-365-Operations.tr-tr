---
title: Birimlerarası muhasebe için dengelenmiş günlükler
description: Bu makalede Genel muhasebe sayfasında bir karşı mali boyut seçildiğinde bir defterin nasıl otomatik olarak dengeleneceği açıklanmıştır.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b596a2332a9ada01df7b4e718a79eb624ee52fc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "326780"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="e9aa4-103">Birimlerarası muhasebe için dengelenmiş günlükler</span><span class="sxs-lookup"><span data-stu-id="e9aa4-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9aa4-104">Bu makalede Genel muhasebe sayfasında bir karşı mali boyut seçildiğinde bir defterin nasıl otomatik olarak dengeleneceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="e9aa4-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="e9aa4-105">Muhasebe girişleri mali boyut değerleri düzeyinde dengelenmiyorsa, günlüğü dengelemek için ek hesap girişleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e9aa4-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="e9aa4-106">Bu hesap girişleri, ana hesabı belirlemek için **Otomatik hareketlere yönelik hesaplar** sayfasındaki **Birimlerarası - borç** ve **Birimlerarası - kredi** deftere nakil türlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e9aa4-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="e9aa4-107">Örneğin, İş Birimi, genel muhasebe hesabındaki ikinci segmenttir ve dengeleme mali boyutu olarak seçilir ve aşağıdaki muhasebe girişleri oluşturulmak üzeredir.</span><span class="sxs-lookup"><span data-stu-id="e9aa4-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="e9aa4-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="e9aa4-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="e9aa4-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="e9aa4-109">100.00 DR</span></span> |
| <span data-ttu-id="e9aa4-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="e9aa4-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="e9aa4-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="e9aa4-111">100.00 DR</span></span> |
| <span data-ttu-id="e9aa4-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="e9aa4-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="e9aa4-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="e9aa4-113">200.00 CR</span></span> |

<span data-ttu-id="e9aa4-114">Bu durumda, aşağıdaki bakiyeler belirlenir:</span><span class="sxs-lookup"><span data-stu-id="e9aa4-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="e9aa4-115">Business Birimi MSP için = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="e9aa4-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="e9aa4-116">Business Birimi NY için = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="e9aa4-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="e9aa4-117">Bu nedenle, günlüğü mali boyut değerlerinin düzeyinde dengelemek için aşağıdaki muhasebe girişleri otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e9aa4-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="e9aa4-118">(Birimlerarası Borç) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="e9aa4-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="e9aa4-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="e9aa4-119">100.00 DR</span></span> |
| <span data-ttu-id="e9aa4-120">(Birimlerarası Alacak) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="e9aa4-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="e9aa4-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="e9aa4-121">100.00 CR</span></span> |






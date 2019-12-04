---
title: Tümleşik genel muhasebe
description: Bu konu Finance and Operations ile Common Data Service'i kullanan Customer Engagement arasında genel muhasebe verileri tümleştirmesini açıklar.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 43819e23b167663a51095546cab307e7d7c79a38
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771060"
---
## <a name="integrated-ledger"></a><span data-ttu-id="f3975-103">Tümleşik genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="f3975-103">Integrated ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3975-104">Bir iş uygulamasında, genel muhasebe verileri bir şirketin iş yapma şekliyle ilgili temel ayarı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f3975-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="f3975-105">Örneğin, genel muhasebe verileri şirketin izlediği mali yılı, işlemlerinin para birimlerini ve kullandığı hesapları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f3975-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="f3975-106">Bu konuda, bu temel mali verilerin tümleştirilmesi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f3975-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="f3975-107">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="f3975-107">Templates</span></span>

<span data-ttu-id="f3975-108">Genel muhasebe verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel mali varlık eşlemeleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="f3975-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="f3975-109">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="f3975-109">Finance and Operations apps</span></span>      | <span data-ttu-id="f3975-110">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="f3975-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="f3975-111">Para birimleri</span><span class="sxs-lookup"><span data-stu-id="f3975-111">Currencies</span></span>                       | <span data-ttu-id="f3975-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="f3975-112">transactioncurrencies</span></span>
<span data-ttu-id="f3975-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="f3975-113">FiscalCalendar</span></span>                   | <span data-ttu-id="f3975-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="f3975-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="f3975-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="f3975-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="f3975-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="f3975-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="f3975-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="f3975-117">ExchRateType</span></span>                     | <span data-ttu-id="f3975-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="f3975-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="f3975-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="f3975-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="f3975-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="f3975-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="f3975-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="f3975-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="f3975-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="f3975-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="f3975-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="f3975-123">MainAccountCategory</span></span>              | <span data-ttu-id="f3975-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="f3975-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="f3975-125">MainAccount</span><span class="sxs-lookup"><span data-stu-id="f3975-125">MainAccount</span></span>                      | <span data-ttu-id="f3975-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="f3975-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="f3975-127">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="f3975-127">Ledger</span></span>                           | <span data-ttu-id="f3975-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="f3975-128">msdyn\_ledgers</span></span>
<span data-ttu-id="f3975-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="f3975-129">ExchangeRates</span></span>                    | <span data-ttu-id="f3975-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="f3975-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="f3975-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="f3975-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="f3975-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="f3975-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="f3975-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="f3975-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="f3975-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="f3975-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="f3975-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="f3975-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="f3975-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="f3975-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="f3975-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="f3975-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="f3975-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="f3975-138">msdyn\_chartofaccounts.md</span></span>


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Currency](dual-write/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](dual-write/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](dual-write/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](dual-write/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](dual-write/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](dual-write/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](dual-write/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](dual-write/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](dual-write/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](dual-write/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](dual-write/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](dual-write/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]





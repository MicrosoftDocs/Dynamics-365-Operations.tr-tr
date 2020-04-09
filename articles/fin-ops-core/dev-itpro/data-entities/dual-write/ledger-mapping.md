---
title: Tümleşik genel muhasebe
description: Bu konu Common Data Service'i kullanan Finance and Operations ve diğer Dynamics 365 uygulamaları arasında genel muhasebe verileri tümleştirmesini açıklar.
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
ms.openlocfilehash: 6f1a1c7329f0936147fb8f7a8e0e9fea14f7dd4b
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173027"
---
# <a name="integrated-ledger"></a><span data-ttu-id="a5885-103">Tümleşik genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="a5885-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a5885-104">Bir iş uygulamasında, genel muhasebe verileri bir şirketin iş yapma şekliyle ilgili temel ayarı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a5885-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="a5885-105">Örneğin, genel muhasebe verileri şirketin izlediği mali yılı, işlemlerinin para birimlerini ve kullandığı hesapları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a5885-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="a5885-106">Bu konuda, bu temel mali verilerin tümleştirilmesi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a5885-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="a5885-107">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="a5885-107">Templates</span></span>

<span data-ttu-id="a5885-108">Genel muhasebe verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel mali varlık eşlemeleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="a5885-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="a5885-109">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="a5885-109">Finance and Operations apps</span></span>      | <span data-ttu-id="a5885-110">Dynamics 365'teki model yönetimli uygulama</span><span class="sxs-lookup"><span data-stu-id="a5885-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="a5885-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5885-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="a5885-112">Para birimleri</span><span class="sxs-lookup"><span data-stu-id="a5885-112">Currencies</span></span>                       | <span data-ttu-id="a5885-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="a5885-113">transactioncurrencies</span></span>            |
<span data-ttu-id="a5885-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="a5885-114">FiscalCalendar</span></span>                   | <span data-ttu-id="a5885-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="a5885-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="a5885-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="a5885-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="a5885-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="a5885-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="a5885-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="a5885-118">ExchRateType</span></span>                     | <span data-ttu-id="a5885-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="a5885-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="a5885-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="a5885-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="a5885-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="a5885-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="a5885-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="a5885-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="a5885-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="a5885-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="a5885-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="a5885-124">MainAccountCategory</span></span>              | <span data-ttu-id="a5885-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="a5885-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="a5885-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="a5885-126">MainAccount</span></span>                      | <span data-ttu-id="a5885-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="a5885-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="a5885-128">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="a5885-128">Ledger</span></span>                           | <span data-ttu-id="a5885-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="a5885-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="a5885-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="a5885-130">ExchangeRates</span></span>                    | <span data-ttu-id="a5885-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="a5885-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="a5885-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="a5885-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="a5885-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="a5885-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="a5885-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="a5885-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="a5885-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="a5885-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="a5885-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="a5885-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="a5885-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="a5885-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="a5885-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="a5885-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="a5885-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="a5885-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]





---
title: Tümleşik genel muhasebe
description: Bu konu Dataverse'i kullanan Finance and Operations ve diğer Dynamics 365 uygulamaları arasında genel muhasebe verileri tümleştirmesini açıklar.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5fedcbcd8db2692214ea66b2fbab9f7381e0a622
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748529"
---
# <a name="integrated-ledger"></a><span data-ttu-id="f1c85-103">Tümleşik genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="f1c85-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="f1c85-104">Bir iş uygulamasında, genel muhasebe verileri bir şirketin iş yapma şekliyle ilgili temel ayarı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f1c85-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="f1c85-105">Örneğin, genel muhasebe verileri şirketin izlediği mali yılı, işlemlerinin para birimlerini ve kullandığı hesapları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f1c85-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="f1c85-106">Bu konuda, bu temel mali verilerin tümleştirilmesi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f1c85-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="f1c85-107">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="f1c85-107">Templates</span></span>

<span data-ttu-id="f1c85-108">Genel muhasebe verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel mali tablo eşlemeleri koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="f1c85-108">Ledger data includes a collection of core financial table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="f1c85-109">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="f1c85-109">Finance and Operations apps</span></span>      | <span data-ttu-id="f1c85-110">Dynamics 365'teki model yönetimli uygulama</span><span class="sxs-lookup"><span data-stu-id="f1c85-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="f1c85-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1c85-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="f1c85-112">Para birimleri</span><span class="sxs-lookup"><span data-stu-id="f1c85-112">Currencies</span></span>                       | <span data-ttu-id="f1c85-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="f1c85-113">transactioncurrencies</span></span>            |
<span data-ttu-id="f1c85-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="f1c85-114">FiscalCalendar</span></span>                   | <span data-ttu-id="f1c85-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="f1c85-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="f1c85-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="f1c85-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="f1c85-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="f1c85-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="f1c85-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="f1c85-118">ExchRateType</span></span>                     | <span data-ttu-id="f1c85-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="f1c85-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="f1c85-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="f1c85-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="f1c85-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="f1c85-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="f1c85-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="f1c85-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="f1c85-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="f1c85-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="f1c85-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="f1c85-124">MainAccountCategory</span></span>              | <span data-ttu-id="f1c85-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="f1c85-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="f1c85-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="f1c85-126">MainAccount</span></span>                      | <span data-ttu-id="f1c85-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="f1c85-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="f1c85-128">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="f1c85-128">Ledger</span></span>                           | <span data-ttu-id="f1c85-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="f1c85-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="f1c85-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="f1c85-130">ExchangeRates</span></span>                    | <span data-ttu-id="f1c85-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="f1c85-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="f1c85-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="f1c85-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="f1c85-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="f1c85-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="f1c85-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="f1c85-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="f1c85-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="f1c85-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="f1c85-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="f1c85-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="f1c85-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="f1c85-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="f1c85-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="f1c85-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="f1c85-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="f1c85-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
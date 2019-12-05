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
## <a name="integrated-ledger"></a>Tümleşik genel muhasebe

[!include [banner](../includes/banner.md)]

Bir iş uygulamasında, genel muhasebe verileri bir şirketin iş yapma şekliyle ilgili temel ayarı tanımlar. Örneğin, genel muhasebe verileri şirketin izlediği mali yılı, işlemlerinin para birimlerini ve kullandığı hesapları tanımlar. Bu konuda, bu temel mali verilerin tümleştirilmesi açıklanmaktadır.

## <a name="templates"></a>Şablonlar

Genel muhasebe verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel mali varlık eşlemeleri topluluğudur.

Finance and Operations uygulamaları      | Diğer Dynamics 365 uygulamaları
---------------------------------|---------------------------------
Para birimleri                       | transactioncurrencies
FiscalCalendar                   | msdyn\_fiscalcalendars
FiscalCalendarYear               | msdyn\_fiscalcalendaryears
ExchRateType                     | msdyn\_exchangeratetypes
ExchangeRateCurrencyPair         | msdyn\_currencyexchangeratepairs
FiscalPeriodEntity               | msdyn\_fiscalcalendarperiods
MainAccountCategory              | msdyn\_mainaccountcategory
MainAccount                      | msdyn\_mainaccounts
Genel muhasebe                           | msdyn\_ledgers
ExchangeRates                    | msdyn\_currencyexchangerates
FinancialCalendarPeriod          | msdyn\_fiscalcalendarperiods
DimensionAttributeEntity         | msdyn\_dimensionattributes.md
DimensionIntegrationFormatEntity | msdyn\_financialdimensionformats.md
LedgerChartOfAccounts            | msdyn\_chartofaccounts.md


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





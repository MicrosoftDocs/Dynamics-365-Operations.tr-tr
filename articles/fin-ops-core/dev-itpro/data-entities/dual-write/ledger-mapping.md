---
title: Tümleşik genel muhasebe
description: Bu makalede, finans ve operasyon ile Dataverse'ü kullanan diğer Dynamics 365 uygulamaları arasında genel muhasebe verilerinin tümleştirilmesi açıklanmaktadır.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e5598295a25e31b33cd8b4d7ce3250a982ab4e87
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112255"
---
# <a name="integrated-ledger"></a>Tümleşik genel muhasebe

[!include [banner](../../includes/banner.md)]



Bir iş uygulamasında, genel muhasebe verileri bir şirketin iş yapma şekliyle ilgili temel ayarı tanımlar. Örneğin, genel muhasebe verileri şirketin izlediği mali yılı, işlemlerinin para birimlerini ve kullandığı hesapları tanımlar. Bu makalede, bu temel mali verilerin tümleştirilmesi açıklanmaktadır.

## <a name="templates"></a>Şablonlar

Genel muhasebe verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel mali tablo eşlemeleri koleksiyonudur.

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları     | Tanım
---------------------------------|----------------------------------|------------
[CDS Döviz Kurları](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Hesap planı](mapping-reference.md#121) | msdyn_chartofaccountses |
[Para birimleri](mapping-reference.md#218) | transactioncurrencies |
[Döviz kuru para birimi çifti](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Döviz kuru türü](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Mali boyut biçimi](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Mali boyutlar](mapping-reference.md#128) | msdyn_dimensionattributes |
[Mali takvim tümleştirme varlığı](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Mali takvim dönemi](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Mali takvim yılı tümleştirme varlığı](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Genel muhasebe](mapping-reference.md#148) | msdyn_ledgers |
[Ana hesap](mapping-reference.md#152) | msdyn_mainaccounts |
[Ana hesap kategorileri](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


---
title: Tümleşik genel muhasebe
description: Bu konu Dataverse'i kullanan Finance and Operations ve diğer Dynamics 365 uygulamaları arasında genel muhasebe verileri tümleştirmesini açıklar.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.openlocfilehash: 18a95725af8014845d6fb39806917de7632ad56b92b75387cd916de927127b38
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723093"
---
# <a name="integrated-ledger"></a>Tümleşik genel muhasebe

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bir iş uygulamasında, genel muhasebe verileri bir şirketin iş yapma şekliyle ilgili temel ayarı tanımlar. Örneğin, genel muhasebe verileri şirketin izlediği mali yılı, işlemlerinin para birimlerini ve kullandığı hesapları tanımlar. Bu konuda, bu temel mali verilerin tümleştirilmesi açıklanmaktadır.

## <a name="templates"></a>Şablonlar

Genel muhasebe verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel mali tablo eşlemeleri koleksiyonudur.

Finance and Operations uygulamaları | Müşteri etkileşimi uygulamaları     | Tanım
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

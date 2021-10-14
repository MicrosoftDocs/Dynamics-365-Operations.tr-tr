---
title: Şirketlerarası para birimi dönüştürmeleri
description: Bu konuda, şirketlerarası hareketler için para birimi dönüştürmeleri açıklanmaktadır
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548594"
---
# <a name="intercompany-currency-conversions"></a>Şirketlerarası para birimi dönüştürmeleri

[!include [banner](../../includes/banner.md)]

Özgün satış siparişindeki ve şirketlerarası satın alma siparişindeki para birimi kodu farklı olduğunda eşitleme etkinleştirilirse aşağıdaki alanların para birimi dönüştürülür:

- **Birim fiyat**
- **Satış masrafları** veya **Satınalmadaki masraflar**
- **İskonto**
- **Çok satırlı iskonto**

Bu alanlar daha sonra şirketlerarası satış siparişi satırı ile eşitlenir.

Ancak, şirketlerarası satın alma siparişindeki ve şirketlerarası satış siparişindeki para birimi her zaman farklı olduğundan aşağıdaki alanlar para birimi dönüştürmesi kullanılmadan etkinleştirilir:

- **Birim fiyat**
- **Satış masrafları** veya **Satınalmadaki masraflar**
- **İskonto**
- **İskonto yüzdesi**
- **Çok satırlı iskonto**
- **Çok satırlı iskonto yüzdesi**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

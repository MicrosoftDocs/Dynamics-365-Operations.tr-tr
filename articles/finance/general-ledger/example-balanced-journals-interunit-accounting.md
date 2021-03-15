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
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f189d1ed5b0917c9975587accc2275556ceb8143
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968766"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Birimlerarası muhasebe için dengelenmiş günlükler

[!include [banner](../includes/banner.md)]

Bu makalede Genel muhasebe sayfasında bir karşı mali boyut seçildiğinde bir defterin nasıl otomatik olarak dengeleneceği açıklanmıştır. 

Muhasebe girişleri mali boyut değerleri düzeyinde dengelenmiyorsa, günlüğü dengelemek için ek hesap girişleri oluşturulur. Bu hesap girişleri, ana hesabı belirlemek için **Otomatik hareketlere yönelik hesaplar** sayfasındaki **Birimlerarası - borç** ve **Birimlerarası - kredi** deftere nakil türlerini kullanır. Örneğin, İş Birimi, genel muhasebe hesabındaki ikinci segmenttir ve dengeleme mali boyutu olarak seçilir ve aşağıdaki muhasebe girişleri oluşturulmak üzeredir.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

Bu durumda, aşağıdaki bakiyeler belirlenir:

-   Business Birimi MSP için = 100,00 CR
-   Business Birimi NY için = 100,00 DR

Bu nedenle, günlüğü mali boyut değerlerinin düzeyinde dengelemek için aşağıdaki muhasebe girişleri otomatik olarak oluşturulur.

|                                   |           |
|-----------------------------------|-----------|
| (Birimlerarası Borç) – MSP – OU\_256 | 100,00 DR |
| (Birimlerarası Alacak) – NY – OU\_249 | 100,00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
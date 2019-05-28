---
title: Amortisman hesaplamaları için yuvarlanan tutar
description: Bu makalede, Defter ayarları sayfalarında bulunan Yuvarlama amortismanı alanı ele alınmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7721e46a72e0f8133ed67c597a066a97ffd61669
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549139"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Amortisman hesaplamaları için yuvarlanan tutar

[!include [banner](../includes/banner.md)]

Bu makalede, Defter ayarları sayfalarında bulunan Yuvarlama amortismanı alanı ele alınmaktadır.

Her defter için yuvarlanan amortisman tutarları ayarlanır. Yuvarlanan amortisman tutarları, gelecek amortismanı ve sabit kıymetin değerini gösteren sabit kıymet amortisman profilinde ve ayrıca amortisman tekliflerinde kullanılır. Defter için izin verilen en düşük amortisman tutarını girin. 

Ayarlanan yuvarlamadan bağımsız olarak, son amortisman dönemindeki amortisman tutarı yuvarlanmaz. Son amortisman döneminin sonunda sabit kıymet değeri mutlaka 0 (sıfır) olmalı veya hurda değeri kullanılıyorsa hurda değerine eşit olmalıdır.

### <a name="example"></a>Örnek

Amortisman, yuvarlama olmadan 2,444.44 olarak hesaplanır. Aşağıdaki tabloda da gösterildiği gibi, önerilen tutarlar yuvarlamanın nasıl ayarlandığına bağlı olarak değişir.

| Yuvarlama yöntemi | Amortisman tutarı |
|-----------------|---------------------|
| Yuvarlama 0,1    | 2.444,40            |
| Yuvarlama 1,00   | 2,444.00            |
| Yuvarlama 10,00  | 2,440.00            |
| Yuvarlama 100,00 | 2,400.00            |






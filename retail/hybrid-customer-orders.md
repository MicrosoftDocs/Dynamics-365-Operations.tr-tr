---
title: "Karma müşteri siparişleri"
description: "Karma müşteri siparişi toplanma veya daha sonra sevk edilen ürünlerin yanı sıra deposundan müşteri tarafından gerçekleştirilmesi ürünleri içeren tek bir sıradır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Karma müşteri siparişleri

Karma müşteri siparişi toplanma veya daha sonra sevk edilen ürünlerin yanı sıra deposundan müşteri tarafından gerçekleştirilmesi ürünleri içeren tek bir sıradır.

Microsoft Dynamics 365 - işlemleri için perakende, ya da tüm ürünler Yürüt seçebilir veya seçili ürünler için müşteri siparişi yerine getirmek. Ürün siparişi oluşturulduktan sonra işaretlenen satırlar yürütmek gibi otomatik olarak faturalandırılır, benzer şekilde bu siparişi oluşturulduktan sonra çekilen-up için olan sipariş için aynıdır. Borç Tutarı üzerinde karma siparişleri depozito yüzdesi çekme ekleyerek ve sevk ürün satırları satırları Yürüt tutarının tamamı ile belirlenir. Karma siparişler için sistem müşteri sipariş ve Öde ve Al modları arasında şöyle geçer:

-   Sepetinizdeki tüm ürünler ayarlanmışsa, **teslim taşıyan**, sipariş Öde ve Al hareketi olarak ele alınır.
-   Arabası satırlarında herhangi biri veya tümü olarak ayarlanmışsa, **çekme** veya **sevk teslim**, sipariş müşteri sipariş işlem olarak ele alınacaktır.

Sepeti satır seçiliyse ve **seçilen çekme**, **seçilen sevk**, veya **seçili yürütmek** ise seçiliyken, yalnızca belirli arabası satırı Bu teslim yöntemi ile ayarlanır. Bu durumda, işlem akış akışını her zaman olduğu gibi devam eder. Ancak, **seçilen çekme**, **seçilen sevk**, veya **seçili yürütmek** seçildiği, arabası olmadan çizgi sepeti satırları listeler yeni bir sayfa açar seçili. Bu ekranda aynı anda teslim yöntemini ayarlamak için birden çok satır seçebilirsiniz. Satırları seçmek için bu yöntemi kullandığınızda, satıra atanan tüm önceki teslim yöntemi geçersiz kılınır.

<a name="see-also"></a>Ayrıca bkz.
--------

[Müşteri siparişleri genel bakış](customer-orders-overview.md)



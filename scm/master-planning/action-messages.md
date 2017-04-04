---
title: "belgelenmemiş"
description: "Bir eylem mesajı, geçerli bir planlanmış veya kesinleştirilmiş siparişi değiştirmek için sistem tarafından oluşturulan bir öneridir."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 21 - 54
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f2ac69ddf485139b057dafa20e5f1a961fc32067
ms.lasthandoff: 03/29/2017


---

# <a name="undocumented"></a>belgelenmemiş

Bir eylem mesajı, geçerli bir planlanmış veya kesinleştirilmiş siparişi değiştirmek için sistem tarafından oluşturulan bir öneridir.

### <a name="introduction"></a>Giriş

Eylem iletileri değişen gereksinimlere yanıt olarak master planlama hesaplaması tarafından oluşturulur. Örneğin, talebi karşılamak üzere zaten bir satınalma siparişi oluşturduğunuz bir satış siparişindeki sevk tarihi veya miktarı değişmiş olabilir. Bu durumda, satınalma siparişini güncelleştirmek için master planlama tarafından bir veya birden çok eylem iletisi oluşturulur Tavsiye edilen değişiklikleri yapıp yapmayacağınıza karar verebilirsiniz.

Bir öğeye eklediğiniz bir karşılama grubu için eylem iletilerinin nasıl hesaplanacağını ayarlayabilirsiniz.

 <a name="selecting-action-messages"></a> Eylem iletilerini seçme
==========================

**Karşılama grupları **sayfası üzerinde, sistemin üretmesini istediğiniz eylem iletilerini ve iletilerin uygulanacağı Karşılama gruplarını veya öğelerini seçebilirsiniz. Aşağıdaki eylem iletilerini seçebilirsiniz.

| İleti             | Açıklama                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **İlerlet**         | Bu iletiyi seçerseniz, sistem siparişleri önceki bir tarihe taşımak için gerektiğinde eylem iletilerini oluşturacaktır. **İlerletme marjı** alanı içinde, ilerletme eylemi olmadan giriş ve çıkış arasında geçebilecek maksimum gün sayısını belirtebilirsiniz. |
| **Ertele**        | Bu iletiyi seçerseniz, sistem siparişleri sonraki bir tarihe taşımak için gerektiğinde eylem iletilerini oluşturacaktır. **Erteleme marjı** alanı içinde, erteleme eylemi olmadan giriş ve çıkış arasında geçebilecek maksimum gün sayısını da belirtebilirsiniz.       |
| **Azalt**        | Bu iletiyi seçerseniz, üretim emirleri, satınalma siparişleri ve diğer giriş hareketlerini fazladan stok düzeylerini engellemek için düşürülecektir.                                                                                                   |
| **Artır**        | Bu iletiyi seçerseniz, üretim emirleri, satınalma siparişleri ve diğer giriş hareketlerini stok düzeylerinde noksanlığı engellemek için artırılacaktır.                                                                                                    |
| **Türev eylemler** | Bu iletiyi seçerseniz, eylem iletileri Türetilmiş gereksinimler için örneğin, Üretim gereksinimlerini sağlamak için bileşen siparişleri için eylemler oluşturulacaktır.                                                                                                   |





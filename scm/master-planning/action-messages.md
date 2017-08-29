---
title: Eylem iletileri
description: "Bir eylem mesajı, geçerli bir planlanmış veya kesinleştirilmiş siparişi değiştirmek için sistem tarafından oluşturulan bir öneridir."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fbae19bd9699f17e7ce581415bf859cb87ebdb83
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="action-messages"></a>Eylem iletileri

[!include[banner](../includes/banner.md)]


Bir eylem mesajı, geçerli bir planlanmış veya kesinleştirilmiş siparişi değiştirmek için sistem tarafından oluşturulan bir öneridir.

## <a name="introduction"></a>Giriş

Eylem iletileri değişen gereksinimlere yanıt olarak master planlama hesaplaması tarafından oluşturulur. Örneğin, talebi karşılamak üzere zaten bir satınalma siparişi oluşturduğunuz bir satış siparişindeki sevk tarihi veya miktarı değişmiş olabilir. Bu durumda, satınalma siparişini güncelleştirmek için master planlama tarafından bir veya birden çok eylem iletisi oluşturulur Tavsiye edilen değişiklikleri yapıp yapmayacağınıza karar verebilirsiniz.

Bir öğeye eklediğiniz bir karşılama grubu için eylem iletilerinin nasıl hesaplanacağını ayarlayabilirsiniz.

## <a name="select-action-messages"></a>Eylem iletilerini seç

**Karşılama grupları** sayfası üzerinde, sistemin üretmesini istediğiniz eylem iletilerini ve iletilerin uygulanacağı Karşılama gruplarını veya öğelerini seçebilirsiniz. Aşağıdaki eylem iletilerini seçebilirsiniz.

| İleti             | Açıklama                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **İlerlet**         | Bu iletiyi seçerseniz, sistem siparişleri önceki bir tarihe taşımak için gerektiğinde eylem iletilerini oluşturacaktır. **İlerletme marjı** alanı içinde, ilerletme eylemi olmadan giriş ve çıkış arasında geçebilecek maksimum gün sayısını belirtebilirsiniz. |
| **Ertele**        | Bu iletiyi seçerseniz, sistem siparişleri sonraki bir tarihe taşımak için gerektiğinde eylem iletilerini oluşturacaktır. **Erteleme marjı** alanı içinde, erteleme eylemi olmadan giriş ve çıkış arasında geçebilecek maksimum gün sayısını da belirtebilirsiniz.       |
| **Azalt**        | Bu iletiyi seçerseniz, üretim emirleri, satınalma siparişleri ve diğer giriş hareketlerini fazladan stok düzeylerini engellemek için düşürülecektir.                                                                                                   |
| **Artır**        | Bu iletiyi seçerseniz, üretim emirleri, satınalma siparişleri ve diğer giriş hareketlerini stok düzeylerinde noksanlığı engellemek için artırılacaktır.                                                                                                    |
| **Türev eylemler** | Bu iletiyi seçerseniz, eylem iletileri Türetilmiş gereksinimler için örneğin, Üretim gereksinimlerini sağlamak için bileşen siparişleri için eylemler oluşturulacaktır.                                                                                                   |







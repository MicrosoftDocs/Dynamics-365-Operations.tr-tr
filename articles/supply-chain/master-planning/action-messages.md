---
title: Eylem iletileri
description: Bir eylem mesajı, geçerli bir planlanmış veya kesinleştirilmiş siparişi değiştirmek için sistem tarafından oluşturulan bir öneridir.
author: ChristianRytt
manager: AnnBe
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a74feeaf61e93ed2802b5f45941d7e15e947b615
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658971"
---
# <a name="action-messages"></a>Eylem iletileri

[!include [banner](../includes/banner.md)]

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






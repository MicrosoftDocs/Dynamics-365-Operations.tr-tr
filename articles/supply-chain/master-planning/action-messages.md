---
title: Eylem iletileri
description: Bir eylem mesajı, geçerli bir planlanmış veya kesinleştirilmiş siparişi değiştirmek için sistem tarafından oluşturulan bir öneridir.
author: ChristianRytt
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb208d390d3b5d2091f5b0f112532794a4d78d8adcf947291a4183c3b3fd3f9c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769575"
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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
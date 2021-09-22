---
title: Sipariş iptal edilirken rezervasyonlar kaldırılamıyor
description: Bir satış siparişini bu siparişle ilişkilendirilmiş iş iptal edilene ve ters çevrilene kadar iptal edemezsiniz. Bunun için şu üç adımı izleyin.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477859"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Sipariş iptal edilirken rezervasyonlar kaldırılamıyor

## <a name="symptoms"></a>Belirtiler

İş bir satış siparişiyle ilişkilendirilmişse ve bu siparişi iptal etmeyi denerseniz aşağıdaki hata iletisini alırsınız:

> Rezervasyonlara dayanan iş oluşturulmuş olduğundan rezervasyonlar kaldırılamıyor.

Satış siparişini iş iptal edilene ve ters çevrilene kadar iptal edemezsiniz. Bu gereksinim, satış siparişiyle ilişkilendirilmiş iş kapatılmış olsa bile geçerlidir.

## <a name="resolution"></a>Çözüm

Bu sorunu düzeltmek için şu adımları izleyin:

1. İşi iptal edin ve stoku istenen konuma geri yerleştirin. Satış siparişinin ilgili yüküne gidin ve yükleme satırında **Çekilen miktarı azalt** ya da Eylem Bölmesi'ndeki **İşi tersine çevir**'i seçin.

    İş artık *İptal edildi* durumunda olur ve yeni stok hareketi işi otomatik olarak oluşturulur stoku ters çevirme işlemi sırasında tanımlanan konuma geri yerleştirmek için işlenir.

2. Yükü silin. Sevkiyat da silinir.

3. Artık satış siparişine gidip iptal edebilirsiniz.

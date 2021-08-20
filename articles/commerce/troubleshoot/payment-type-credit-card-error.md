---
title: Satış siparişi sayfasında ödeme türü kredi kartı olmalıdır hatası
description: Bu konu, sipariş eşitlendikten sonra satış siparişi sayfasında hata iletisi gösterildiğinde size yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 03bcbedb12b95a00141d27e9a93186a7fa7dabba70147177524f604dd10ed252
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750684"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Satış siparişi sayfasında "ödeme türü kredi kartı olmalıdır" hatası

[!include [banner](../../includes/banner.md)]

Bu konu, sipariş eşitlendikten sonra satış siparişi sayfasında hata iletisi gösterildiğinde size yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Satış siparişi sayfasını bir siparişi eşitledikten sonra açtığınızda, şu hata iletisini alırsınız: "kredi kartı numarası belirtildiği için ödeme türü kredi kartı olmalıdır."

![Ödeme türü kredi kartı olmalıdır hatası.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Çözüm

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Commerce Headquarters'da ödeme türünü ayarlayın

1. **Alacak hesapları \> Ödemeler kurulumu \> Ödeme şartları**'na gidin.
1. Sol gezinti bölmesinde ödeme koşullarınızı seçin.
1. **Ödeme türü** alanında, **kredi kartı**'nın seçildiğinden emin olun.

## <a name="additional-resources"></a>Ek kaynaklar

[Çevrimiçi satışları ve ödemeleri deftere nakletme](../tasks/posting-online-sales-payments.md)

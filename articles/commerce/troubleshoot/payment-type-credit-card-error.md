---
title: Satış siparişi sayfasında ödeme türü kredi kartı olmalıdır hatası
description: Bu makale, sipariş eşitlendikten sonra satış siparişi sayfasında hata iletisi gösterildiğinde size yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 794317a84a8a0ff205ac1b6a5caa6ef1cf098ea3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905355"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Satış siparişi sayfasında "ödeme türü kredi kartı olmalıdır" hatası

[!include [banner](../../includes/banner.md)]

Bu makale, sipariş eşitlendikten sonra satış siparişi sayfasında hata iletisi gösterildiğinde size yardımcı olabilecek sorun giderme kılavuzu sağlar.

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

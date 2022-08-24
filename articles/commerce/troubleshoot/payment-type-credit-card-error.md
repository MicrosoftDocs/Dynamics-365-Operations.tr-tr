---
title: Satış siparişi sayfasında ödeme türü kredi kartı olmalıdır hatası
description: Bu makale, sipariş eşitlendikten sonra satış siparişi sayfasında hata iletisi gösterildiğinde size yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285645"
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

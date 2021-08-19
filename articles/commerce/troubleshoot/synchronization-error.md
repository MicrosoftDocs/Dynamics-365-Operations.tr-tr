---
title: Varsayılan ödeme hizmeti ile ilgili sipariş eşitleme hatası
description: Bu konu, bir çevrimiçi sipariş eşitlendiğinde oluşabilecek bir hatayı gidermeye yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 6f8e0ea7675ffc5cbada36207422b410234e33afcaec90636e90e573a90ac484
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715248"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Varsayılan ödeme hizmeti ile ilgili sipariş eşitleme hatası

[!include [banner](../../includes/banner.md)]

Bu konu, bir çevrimiçi sipariş eşitlendiğinde oluşabilecek bir hatayı gidermeye yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Çevrimiçi bir siparişi eşitlediğinizde, şu hata iletisini alırsınız: "Kredi kartı işlemlerini işlemek için varsayılan bir ödeme hizmeti olmalıdır."

![Eksik varsayılan ödeme hizmeti hatası.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Çözüm

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Commerce genel merkezinde varsayılan ödeme hizmetini onaylama veya ayarlama

Commerce genel merkezinde varsayılan ödeme hizmetini onaylamak veya ayarlamak için şu adımları izleyin.

1. **Alacak hesapları \> Ödeme kurulumu \> Ödeme hizmetleri** menüsüne gidin.
1. **Yeni kredi kartları için varsayılan işlemci** seçeneğinin bir ödeme servisi için **Evet** olarak ayarlandığından emin olun.

## <a name="additional-resources"></a>Ek kaynaklar

[Kredi kartı ayarı, onayı ve çekimi](../../finance/accounts-receivable/credit-card-authorizations.md)
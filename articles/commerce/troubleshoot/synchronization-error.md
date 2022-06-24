---
title: Varsayılan ödeme hizmeti ile ilgili sipariş eşitleme hatası
description: Bu makale, bir çevrimiçi sipariş eşitlendiğinde oluşabilecek bir hatayı gidermeye yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 49d16c39fdcee0a22d1cabe14cd9b6d124d6f04d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901688"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Varsayılan ödeme hizmeti ile ilgili sipariş eşitleme hatası

[!include [banner](../../includes/banner.md)]

Bu makale, bir çevrimiçi sipariş eşitlendiğinde oluşabilecek bir hatayı gidermeye yardımcı olabilecek sorun giderme kılavuzu sağlar.

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
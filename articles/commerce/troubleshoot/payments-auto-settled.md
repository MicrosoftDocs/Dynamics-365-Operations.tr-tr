---
title: Ödemeler, siparişler faturalanmadan veya sevk edilmeden önce otomatik olarak kapatılıyor
description: Bu konu, satış siparişinin faturalanmamış veya sevk edilmemiş olmasına rağmen, sipariş verildikten sonra bir ödemenin Adyen portalında hemen kapatılmasıyla ilgili sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018272"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Ödemeler, siparişler faturalanmadan veya sevk edilmeden önce otomatik olarak kapatılıyor

[!include [banner](../../includes/banner.md)]

Bu konu, satış siparişinin faturalanmamış veya sevk edilmemiş olmasına rağmen, sipariş verildikten sonra bir ödemenin Adyen portalında hemen kapatılmasıyla ilgili sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Bir sipariş verildikten sonra, satış siparişi faturalanmamış veya sevk edilmemiş olmasına rağmen, Adyen portalında ödeme hemen kapatılıyor.

## <a name="resolution"></a>Çözünürlük

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Adyen portalında e-ticaret ödemeleri için el ile kaydetmeyi yapılandırın

Adyen portalında e-ticaret ödemeleri için el ile kaydetmeyi yapılandırmak için aşağıdaki adımları izleyin.

1. Adyen portalında oturum açın.
1. Sağ üst köşede, e-ticaret kanalı için satıcı hesabınızı seçin.
1. Üst gezinti çubuğunda, **Hesap**'ı seçin ve ardından **Ayarlar**'ı seçin.
1. **Kaydetme gecikmesi** alanında, **el ile** seçeneğini belirleyin.

    ![Adyen portalında kaydetme gecikmesi ayarı](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Ek kaynaklar

[Adyen ödeme kaydetme](https://docs.adyen.com/point-of-sale/capturing-payments)

[Adyen için Dynamics 365 Ödeme Bağlayıcısı](../dev-itpro/adyen-connector.md)

[Dynamics 365 için Adyen Payment Connector sorunlarını giderme](https://docs.adyen.com/plugins/microsoft-dynamics)

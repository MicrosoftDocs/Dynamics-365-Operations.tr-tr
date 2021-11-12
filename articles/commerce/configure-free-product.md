---
title: Satın alınacak ürünü ücretsiz konfigüre etme
description: Bu konu, Microsoft Dynamics 365 Commerce'te ücretsiz olarak satın alınabilmesi için bir ürünü konfigüre etme yöntemini açıklamaktadır.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ad96a3dde93a48694aee418ecfbbd33dc9830d6
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713897"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Satın alınacak ürünü ücretsiz konfigüre etme

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'te ücretsiz olarak satın alınabilmesi için bir ürünü konfigüre etme yöntemini açıklamaktadır.

## <a name="configure-the-product"></a>Ürünü yapılandırma

Ürünü Dynamics 365 Commerce'te ücretsiz olarak satmak için fiyatı 0 (sıfır) olarak ayarlamalısınız. Ek olarak, ürünün **Sıfır fiyatı geçerli** ayarını konfigüre etmelisiniz.

Commerce Headquarters'da **Sıfır fiyat geçerli** ayarını konfigüre etmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Ürünler ve kategoriler \> Kategoriye göre serbest bırakılmış ürünler**'e gidin.
1. Ücretsiz olarak satmak istediğiniz ürüne gidin. 
1. Ürün sayfasının **Commerce** bölümünde, **Sıfır fiyat geçerli** seçeneğini **Evet** olarak ayarlayın.

Aşağıdaki çizimde, **Sıfır fiyat geçerli** seçeneğinin **Evet** olarak ayarlandığı bir ürün örneği gösterilmektedir.

![Sıfır fiyat geçerli seçeneğinin Evet olarak ayarlandığı bir ürün örneği.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Çevrimiçi mağazanın işlevsellik profilini konfigüre edin

Ücretsiz hareketler işlenebilmeden önce, ödeme içermeyen hareketlere izin vermek için, çevrimiçi deponuzun işlevsellik profilinin **Ödeme içermeyen ödemeye izin ver** seçeneğini konfigüre etmelisiniz. İşlevsellik profillerinin nasıl oluşturulacağı hakkında bilgi için, bkz [Çevrimiçi işlev profili oluşturma](online-functionality-profile.md).

Commerce Headquarters'da **Ödeme içermeyen ödemeye izin ver** ayarını konfigüre etmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> Çevrimiçi mağaza kurulumu** öğesine gidin.
1. Mağaza işlevsellik profilinin sayfasında, **Ödeme** altında **Ödeme içermeyen ödemeye izin ver** seçeneğini **Evet** olarak ayarlayın.

Aşağıdaki resimde, **Ödeme içermeyen ödemelere izin ver** seçeneğini **Evet** olarak ayarlandığında, çevrimiçi mağaza profili örneği gösterilmektedir.

![Ödeme içermeyen ödemelere izin ver seçeneğini Evet olarak ayarlandığında, çevrimiçi mağaza profili örneği.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Perakende satış fiyatı yönetimi](price-management.md)

[Çevrimiçi işlevsellik profili oluşturma](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

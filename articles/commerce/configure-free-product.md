---
title: Satın alınacak ürünü ücretsiz konfigüre etme
description: Bu makale, Microsoft Dynamics 365 Commerce'te ücretsiz olarak satın alınabilmesi için bir ürünü konfigüre etme yöntemini açıklamaktadır.
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
ms.openlocfilehash: 4bd7e4f7a7873e471f1aee94f15e7932e8d9eecd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890367"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Satın alınacak ürünü ücretsiz konfigüre etme

[!include [banner](includes/banner.md)]


Bu makale, Microsoft Dynamics 365 Commerce'te ücretsiz olarak satın alınabilmesi için bir ürünü konfigüre etme yöntemini açıklamaktadır.

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

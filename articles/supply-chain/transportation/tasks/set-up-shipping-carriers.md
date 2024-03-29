---
title: Sevkiyat taşıyıcılarını ayarlama
description: Bu makale, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir.
author: Weijiesa
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48586a0ddaa7cd95a81380dadffef8f276076dd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858986"
---
# <a name="set-up-shipping-carriers"></a>Sevkiyat taşıyıcılarını ayarlama

[!include [banner](../../includes/banner.md)]

Bu makale, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir. Ulaşım Koordinatörü, daha sonra, gelen veya giden bir yük için Sevkiyat taşıyıcısı atayabilir.

## <a name="create-a-new-shipping-carrier"></a>Yeni bir Sevkiyat taşıyıcısı oluşturun

1. **Gezinti bölmesi > Modüller > Taşımacılık Yönetimi > Kurulum > Taşıyıcılar > Seviyat taşıyıcıları seçeneğine gidin**.
2. Eylem Bölmesi'nde **Yeni**'yi seçin.
3. **Sevkiyat taşıyıcıları** alanına bir değer yazın.
4. **Ad** alanına bir değer yazın.
5. **Mod** alanında, açılır menüden bir seçenek belirleyin.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Sevkiyat taşıyıcısı için genel bilgileri doldurun

1. **Genel Bakış** bölümünün genişletilmiş görünümüne geçin.
2. **Sevkiyat taşıyıcısını etkinleştir** onay kutusunu işaretleyin veya temizleyin.
3. **Satıcı hesabı** alanında, açılır menüden bir seçenek belirleyin. Sevkiyat taşıyıcısının atanacağı satıcı hesabını seçin.  
4. **Taşıma ödemesi türü** alanında bir seçenek belirleyin. Taşıma ödemesi sayfasını kullanmak için **El ile**'yi seçin veya **EDI**'yi seçerek ödemeyi Elektronik Veri Değişimi (EDI) kullanarak güncelleştirin.  
5. **Taşıyıcı değerlendirmesini etkinleştir** onay kutusunu işaretleyin veya temizleyin.

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Sevkiyat taşıyıcısı için gerekli hizmetleri oluşturun

1. **Hizmetler** bölümünün genişletilmiş görünümüne geçin.
2. **Yeni**'yi seçin.
3. **Taşıyıcı hizmeti** alanına bir değer yazın.
4. **Ad** alanına bir değer yazın.
5. **Şablon kodu yükle** alanında, hizmetle ilişkilendirilecek bir yükleme şablonu seçin. Yük şablonu, ağırlık ve hacim için tüm yükte geçerli olacak maksimum ölçümleri belirler. Yük şablonu örneğin bir konteyner veya kamyonun boyutunu temsil edebilir. Yükleme şablonu kimlikleri, yük oluşturma şablonlarında da belirtilmiştir ve yükleme oluşturma stratejilerini uygulamanıza yardımcı olan [yük oluşturma çalışma ekranı](load-building-workbench.md) kullanılırken da yüklenir. Sonuç olarak, sistem belirtilen yükleme şablonu kimliklerini karşılaştırarak her yeni yükü uygun bir sevkiyat taşıyıcısı hizmetiyle eşleştirebilecektir.
6. **Taşıma yöntemi** alanında, açılır menüden bir seçenek belirleyin.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Taşıyıcı için adresi (isteğe bağlı) ayarlayın

1. **Adresler** bölümünün genişletilmiş görünümüne geçin.
2. **Yeni**'yi seçin.
3. **Ad veya açıklama** alanına bir değer yazın.
4. **Ülke / bölge** alanında, açılır menüden bir seçenek belirleyin.
5. **Bitiş posta kodu** alanında, açılır menüden bir seçenek belirleyin.
6. **Cadde** alanına bir değer yazın.
7. **Tamam**'ı seçin.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Sevkiyat taşıyıcısı için derecelendirme profilini ayarlayın

1. **Değerlendirme profilleri** bölümünün genişletilmiş görünümüne geçin.
2. **Yeni**'yi seçin.
3. **Değerlendirme profili** numarası alanına bir değer yazın.
4. **Ad** alanına bir değer yazın.
5. **Tesis** alanında, açılır menüden bir seçenek belirleyin.
6. **Ambar** alanında, açılır menüden bir seçenek belirleyin.
7. **Değerlendirme altyapısı** alanında, açılır menüden bir seçenek belirleyin. Taşıyıcı ile aranızdaki sözleşmeye uyugn olacak Değerlendirme altyapısını seçin.  
8. **Ara oran** alanında, açılır menüden bir seçenek belirleyin.
9. **Yoldaki süre altyapısı** alanında, açılır menüden bir seçenek belirleyin.
10. **Kaydet**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
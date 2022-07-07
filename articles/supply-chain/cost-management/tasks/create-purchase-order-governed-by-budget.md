---
title: Bütçeyle yönetilen bir satınalma siparişi oluşturma
description: Bu yordamı, kullanılabilir bütçeye karşı denetleyen bir satınalma siparişi oluşturmak için kullanın.
author: JennySong-SH
ms.date: 06/15/2020
ms.topic: business-process
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa9777ad3aa487dfb558879335f93f347b8ac749
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016202"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Bütçeyle yönetilen bir satınalma siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordamı, kullanılabilir bütçeye karşı denetleyen bir satınalma siparişi oluşturmak için kullanın.

## <a name="review-the-budget-control-configuration"></a>Bütçe kontrol konfigürasyonunu gözden geçirin

1. **Bütçeleme > Kurulum > Bütçe kontrolü > Bütçe kontrol yapılandırması**'na gidin.
1. **Kullanılabilir bütçe fonları** sekmesini seçin.
1. **Belgeler ve günlükler** sekmesini seçin.
1. **Bütçe kontrolü kuralları tanımla** sekmesini seçin.
1. **Bütçe grupları tanımla** sekmesini seçin.
1. Sayfayı kapatın.

## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

1. **Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri** öğesine gidin.
1. **Yeni**'yi seçin.
1. **Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.
1. **Genel** hızlı sekmesini genişletin.
1. **Muhasebe tarihi** alanında, tarihi ayarlayın.
1. İletişim kutusunu kapatmak ve yeni satın alma siparişinizi açmak için **Tamam**'ı seçin.
1. Yeni bir satır eklemek için, **Satınalma siparişi satırları** hızlı sekmesinde, araç çubuğundan **Satır ekle**'yi seçin ve sonra bir maddeyi siparişe eklemek için satırı gerektiği şekilde doldurun.
1. **Satınalma siparişi satırları** hızlı sekme araç çubuğunda, **Finansal öğeler \> Tutarları dağıt**'ı seçin.
1. **Genel muhasebe hesabı** alanında, bir hesap belirtin.
1. Sayfayı kapatın.

## <a name="perform-budget-checking"></a>Bütçe kontrolü gerçekleştir

1. Henüz bir satır eklediğiniz satınalma siparişiyle çalışmaya devam edin.
1. **Satınalma siparişi satırları** hızlı sekme araç çubuğunda, **Finansal öğeler \> Bütçe kontrolü gerçekleştir**'i seçin.
1. **Satınalma siparişi satırları** hızlı sekme araç çubuğunda, **Finansal öğeler \> Bütçe kontrol hataları veya uyarıları**'nı seçin.
1. **Bütçe kontrol hataları veya uyarıları** iletişim kutusu açılır. Kontrol sonuçlarını kontrol edin ve sonra iletişim kutusunu kapatmak için **Kapat**'ı seçin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
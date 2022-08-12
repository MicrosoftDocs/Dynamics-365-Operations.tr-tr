---
title: Store Commerce kurulum ve yükleme sorunlarını giderme
description: Bu makalede, Microsoft Dynamics 365 Commerce Store Commerce uygulamasındaki kurulum ve yükleme sorunlarının nasıl giderileceği açıklanmaktadır.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8af2c476ced05fc159a53131f8b51ad914a6c7c3
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168960"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Store Commerce kurulum ve yükleme sorunlarını giderme

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce Store Commerce uygulamasındaki kurulum ve yükleme sorunlarının nasıl giderileceği açıklanmaktadır.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Uygulamayı etkinleştiremiyorum ve bir bağlantı hata iletisi alıyorum

Geçerli Bulut Satış Noktası (CPOS) URL'sini girdikten sonra, aşağıdaki örneğe benzer bir bağlantı hata iletisi alabilirsiniz:

> Bir bağlantı hatası oluştu ve cihazınız CPOS'ye bağlanamıyor. Girilen CPOS URL'sinde bazı sorunlar olabilir.

Bu durumda, URL'de yazım hataları olup olmadığını kontrol edin veya çevrimdışı olduğundan CPOS'ye ulaşılıp ulaşılmadığını belirleyin.

Ek olarak, Cloud Scale Unit (CSU) sürümünün 10.0.25 (9.35.\*.\*) veya sonrası olduğunu doğrulayın. Store Commerce uygulamasını kullanmak için CPOS sürüm 10.0.25 veya sonrası gereklidir.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Modern POS zaten yüklü olduğu için uygulamayı yükleyemiyorum

Yükleme sırasında, aşağıdaki örnekte olduğu gibi bir hata iletisi alabilirsiniz:

> Daha önce eski yükleyici aracılığıyla bu ürünün (Modern POS) bir sürümü (9.\*.\*.\*) yüklenmiş.

Hatayı düzeltmek üzere, makinedeki tüm kullanıcılar için Modern Satış Noktası (MPOS) uygulamasını kaldırmanız ve sonra yeniden denemeniz gerekir. Aşağıdaki PowerShell komutunu çalıştırarak tüm kullanıcılar için MPOS'un kaldırılıp kaldırılmadığını doğrulayabilirsiniz.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Geçersiz bir URL veya hata durumu nedeniyle uygulamayı etkinleştiremiyorum

Girdiğiniz CPOS URL'si geçerli değilse ve değiştirmek istiyorsanız veya etkinleştirme sırasında Store Commerce uygulaması bir hata veriyorsa uygulamayı sıfırlayarak işlemi yeniden başlatabilirsiniz. Store Commerce uygulaması yalnızca geçerli bir CPOS URL'sini kaydeder.

Store Commerce uygulamasını sıfırlamak için aşağıdaki adımları izleyin.

1. Windows **Başlat** menüsünde, uygulamayı seçip basılı tutun (veya sağ tıklayın) ve **Daha Fazla\> Uygulama ayarları**'nı seçin.
2. **Sıfırla** düğmesini bulana kadar uygulama ayarları sayfasında aşağı gidin.
3. **Sıfırla**'yı seçin. Sonra, istendiğinde, uygulamayı sıfırlamak istediğinizi onaylayın.

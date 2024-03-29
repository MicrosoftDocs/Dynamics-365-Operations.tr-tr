---
title: POS'ta URL Aç
description: Bu makalede Dynamics 365 Commerce'da ürün ve müşteri arama özelliğinde yapılmış olan iyileştirmelere genel bakış sunulmaktadır.
author: ShalabhjainMSFT
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.custom: 141393
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: ad82cf1039515e58d1717453ee3fb4e3dafd84fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276440"
---
# <a name="open-url-in-pos"></a>POS'ta URL Aç

[!include [banner](includes/banner.md)]

Bu makale, Dynamics 365 Commerce satış noktası (POS) içerisinde bir URL açmak için bir düğme yapılandırmayı açıklar. Bu özellik bir kod özelleştirme gerektirmez ve geliştirici rolünde olmayan bir kişi tarafından yapılandırılabilir. 

Bu özellik, POS'ta bir düğmenin bir URL açmak için düğme kılavuzu tasarımcısı kullanılarak yapılandırılmasına olanak sağlar. Şu anda, bu aşağıdaki yapılandırmalarda desteklenmektedir:

- Yeni pencerede aç.
- POS içinde açın.
- Yerel bir uygulama açın.

## <a name="open-in-new-window"></a>Yeni pencerede aç

Bu yapılandırma, bir URL'nin yeni bir pencerede mi yoksa uygulama içinde mi açılacağını tanımlar. Bir web URL'sini uygulama içinde açmak üzere yapılandırıldığında, POS'un yan gezinti paneli ve üst çubuğu, kullanıcı etkileşimine görünür ve kullanılabilir durumdadır. Yeni bir pencerede açılmak üzere yapılandırıldığında, URL Modern POS for Windows içerisinde yeni bir uygulama penceresinde veya tüm diğer POS istemcilerinde yeni bir tarayıcı sekmesinde açılır. Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçiliyken URL'yi yapılandırmalısınız.

## <a name="open-within-pos"></a>POS içinde açın

POS içerisinde bir web URL'sini açmak şu anda yalnızca Modern POS on Windows'ta desteklenmektedir. Diğer istemciler üzerinde, bu yeterlilik geliştirme altındadır ve gelecek güncelleştirmeler için planlanmaktadır. Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçili değilken URL'yi yapılandırmalısınız.

## <a name="open-a-native-app"></a>Yerel bir uygulama açın

Bu özellik, web URL'si olmayanları da yerel uygulamada açmanıza olanak sağlar. Örneğin, MailTo, SIP, IM veya MSTEAMS gibi URL protokollerini belirtebilirsiniz, bu sayede bunlar ana cihazdaki bunlara karşılık gelen uygulamalar tarafından ele alınabilir. Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçiliyken URL'yi yapılandırmalısınız.

- Windows bilgisayarlarda Deployment Image Servicing and Management (DISM) kullanarak bilgisayarınızı ayarlıyorsanız, varsayılan protokol ilişkilendirmelerini ayarlamak için bkz [Varsayılan Uygulama İlişkilendirmelerini İçe veya Dışa Aktarma](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
- Windows bilgisayarlarınızı yönetmek için Intune gibi bir MDM kullanıyorsanız, bkz. [Policy CSP ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).
- Özel bir web sitesi kurmakta olan bir geliştiriciyseniz bkz [Bir URI için varsayılan uygulamayı çalıştırmak](/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Yerel bir uygulamayı sorunsuzca açın

Windows, iOS ve Android, uygulama protokolü ilişkilendirmelerine dayanarak uygulamaların daha pürüzsüzce açılmasına olanak sağlar. Uygulamanız bir web tarayıcısından açılmak için halihazırda yapılandırılmamışsa, bunun yapılandırılması için bir geliştiriciye ihtiyaç duyabilirsiniz.

- Windows için bkz. [Uygulama URI işleyicileri kullanarak web siteleri için uygulamaları etkinleştirmek](/windows/uwp/launch-resume/web-to-app-linking).
- iOS bkz. [Geliştiriciler için Evrensel Bağlantılar](https://developer.apple.com/ios/universal-links/).
- Android için bkz. [Android Uygulama Bağlantılarını işlemek](https://developer.android.com/training/app-links/).

| İstemci                | Yeni pencerede aç | Yerel uygulama açın | POS içinde açın | Ayrıntılı                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Modern POS on Windows | ✓\*                | ✓               | ✓              | \* Yeni Modern POS penceresinde açar |
| Bulut POS             | ✓\*                | ✓               | X              | \* Yeni tarayıcı sekmesinde açar        |
| Modern POS on iOS     | ✓\*                | ✓               | X              | \* Yeni tarayıcı sekmesinde açar        |
| Modern POS on Android | ✓\*                | ✓               | X              | \* Yeni tarayıcı sekmesinde açar        |

## <a name="before-you-begin"></a>Başlamadan önce

Başlamadan önce, nasıl yapılandırılacağını gözden geçirin [Satış noktası (POS) için ekran düzenleri](pos-screen-layouts.md).

## <a name="open-url-in-pos"></a>POS'ta URL Aç

Bir URL'nin POS içinde açılmasını yapılandırmak için aşağıdaki adımları izleyin.

1. Ana ofiste, **Perakende ve Ticaret \> Kanal Kurulumu \> POS Kurulumu \> POS \> Ekran Düzenleri**'ne gidin.
2. **Düğme Grupları \> Tasarımcı**'yı seçin.
3. Yeni bir düğme oluşturun.
4. **Düğme** nitelikleri seçin.
5. **URL Aç**'ı eylem olarak seçin.
6. Kullanmak istediğiniz URL'yi seçin.
7. URL'nin yeni pencerede açılmasını isteyip istemediğinizi yapılandırın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

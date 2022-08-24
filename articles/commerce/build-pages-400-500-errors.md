---
title: 4xx/5xx durum kodu hataları için özel yanıt sayfaları oluşturma
description: Bu makale, Microsoft Dynamics 365 Commerce'un yazma araçlarını kullanarak 4xx ve 5xx durum kodu hataları için özel yanıt sayfaları oluşturma yöntemini açıklamaktadır .
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4a3b1762cebc74c1b77f9ca60925608bc966e306
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276413"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>4xx/5xx durum kodu hataları için özel yanıt sayfaları oluşturma

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'un yazma araçlarını kullanarak 4xx ve 5xx durum kodu hataları için özel yanıt sayfaları oluşturma yöntemini açıklamaktadır .

Bir istek başarılı olmazsa, sunucu HTTP durum kodu hata yanıtları verir. 404 durum kodu yakalanarak sayfa bulunamazsa döndürülür ve sunucu hatası oluşursa 500 durum kodu yakalanır ve döndürülür. Dynamics 365 Commerce'te uygulama kullanıcıları bu durum kodu hata yanıtları için kullanıcılara gösterilen özel durum kodu hata yanıtı sayfaları oluşturabilir.

## <a name="build-a-status-code-error-response-page"></a>Durum kodu oluştur hata yanıt sayfası

Durum kodu hata yanıtı sayfası oluşturmaya başlamak için aşağıdaki adımları izleyin.

1. Tercih ettiğiniz Web tarayıcınızda Dynamics 365 Commerce oturumu açın. 
1. 4xx/5xx durum kodu hata yanıtı sayfası oluşturmak istediğiniz siteyi seçin.

### <a name="build-the-template"></a>Şablonu oluştur

Durum kodu hata yanıtı sayfası oluşturmaya başlamak için aşağıdaki adımları izleyin.

1. **Şablonlar**'a gidin.
1. Yeni sayfa şablonu oluşturmak için **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, yeni şablon için ad girin ve **Tamam**'ı seçin.
1. Durum kodu hata yanıtı sayfasında olmasını istediğiniz yapıyı temel alarak şablonu oluşturun.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin. 

### <a name="build-the-status-code-error-response-page"></a>Durum kodu oluştur hata yanıt sayfası

Durum kodu hata yanıtı sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Sayfalar**'a gidin.
1. Sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seç** iletişim kutusunda bir şablon seçin ve sonra **Sayfa adı** altında, durum kodu hata yanıt sayfası için bir ad girin. **Sayfa URL**'si alanını boş bırakın.
1. Sayfayı oluşturun.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

> [!NOTE]
> 4xx ve 5xx durum kodu hataları için ayrı durum kodu hatası yanıtı sayfaları oluşturabilirsiniz. Alternatif olarak, her iki hata kategorisi için de aynı genel durum kodu hata yanıtı sayfasını kullanabilirsiniz.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Durum kodu hatası için yeniden yönlendirme ayarlayın hata yanıtı sayfası

Durum kodu hata yanıtı sayfasına yeniden yönlendirme ayarlamak için aşağıdaki adımları izleyin.

1. **URL'ler \> Yeni \> Yeni Diğer Ad** a gidin ve daha önce oluşturduğunuz durum kodu hata yanıtı sayfasını seçin.
1. **Diğer ad** alanına, yeniden yönlendirme ayarlamakta olduğunuz durum kodu hata yanıtı sayfasına bağlı olarak **varsayılan-4xx** veya **varsayılan-5xx** değerini girin. Bu diğer adlar yayımlanmalıdır. Aksi durumda yeniden yönlendirme çalışmaz.
1. Bağlantıyı onaylamak için **Tamam**'ı seçin.

> [!NOTE]
> Her iki hata kategorisi için de tek bir durum kodu hata yanıtı sayfası kullanıyorsanız, diğer hata kategorisine ait diğer adı aynı sayfaya bağlamak için bu yordamı yineleyin.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlarla çalışma](work-with-templates.md)

[Yeni site sayfası ekleme](add-new-page.md)

[URL sayfası oluşturma](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

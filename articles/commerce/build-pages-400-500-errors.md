---
title: 4xx/5xx durum kodu hataları için özel yanıt sayfaları oluşturma
description: Bu konu, Microsoft Dynamics 365 Commerce'un yazma araçlarını kullanarak 4xx ve 5xx durum kodu hataları için özel yanıt sayfaları oluşturma yöntemini açıklamaktadır .
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697118"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>4xx/5xx durum kodu hataları için özel yanıt sayfaları oluşturma

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'un yazma araçlarını kullanarak 4xx ve 5xx durum kodu hataları için özel yanıt sayfaları oluşturma yöntemini açıklamaktadır .

## <a name="overview"></a>Genel Bakış

Bir istek başarılı olmazsa, sunucu HTTP durum kodu hata yanıtları verir. 404 durum kodu yakalanarak sayfa bulunamazsa döndürülür ve sunucu hatası oluşursa 500 durum kodu yakalanır ve döndürülür. Dynamics 365 Commerce'te uygulama kullanıcıları bu durum kodu hata yanıtları için kullanıcılara gösterilen özel durum kodu hata yanıtı sayfaları oluşturabilir.

## <a name="build-a-status-code-error-response-page"></a>Durum kodu oluştur hata yanıt sayfası

Durum kodu hata yanıtı sayfası oluşturmaya başlamak için aşağıdaki adımları izleyin.

1. Tercih ettiğiniz Web tarayıcınızda Dynamics 365 Commerce oturumu açın. 
1. 4xx/5xx durum kodu hata yanıtı sayfası oluşturmak istediğiniz siteyi seçin.

### <a name="build-the-template"></a>Şablonu oluştur

Durum kodu hata yanıtı sayfası oluşturmaya başlamak için aşağıdaki adımları izleyin.

1. **Şablonlar \> Yeni şablon**a gidin.
1. Yeni şablon adı verin.
1. Durum kodu hata yanıtı sayfasında olmasını istediğiniz yapıyı temel alarak şablonu oluşturun.
1. Şablonu giriş yapın ve yayımlayın.

### <a name="build-the-status-code-error-response-page"></a>Durum kodu oluştur hata yanıt sayfası

Durum kodu hata yanıtı sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Sayfalar \> Yeni Sayfa**ya gidin.
1. Durum kodu hata yanıtı sayfasını adlandırın, ancak **URL** alanını **ayarlamayın**.
1. Sayfayı oluşturun.
1. Sayfayı giriş yapın ve yayımlayın.

> [!NOTE]
> 4xx ve 5xx durum kodu hataları için ayrı durum kodu hatası yanıtı sayfaları oluşturabilirsiniz. Alternatif olarak, her iki hata kategorisi için de aynı genel durum kodu hata yanıtı sayfasını kullanabilirsiniz.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Durum kodu hatası için yeniden yönlendirme ayarlayın hata yanıtı sayfası

Durum kodu hata yanıtı sayfasına yeniden yönlendirme ayarlamak için aşağıdaki adımları izleyin.

1. **URL'ler \> Yeni \> Yeni Diğer Ad**a gidin ve daha önce oluşturduğunuz durum kodu hata yanıtı sayfasını seçin.
1. **Diğer ad** alanına, yeniden yönlendirme ayarlamakta olduğunuz durum kodu hata yanıtı sayfasına bağlı olarak **varsayılan-4xx** veya **varsayılan-5xx** değerini girin. Bu diğer adlar yayımlanmalıdır. Aksi durumda yeniden yönlendirme çalışmaz.
1. Bağlantıyı onaylamak için **Tamam**'ı seçin.

> [!NOTE]
> Her iki hata kategorisi için de tek bir durum kodu hata yanıtı sayfası kullanıyorsanız, diğer hata kategorisine ait diğer adı aynı sayfaya bağlamak için bu yordamı yineleyin.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlarla çalışma](work-with-templates.md)

[Yeni site sayfası ekleme](add-new-page.md)

[URL sayfası oluşturma](create-page-url.md)

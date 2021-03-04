---
title: Statik dosyaları karşıya yükleme ve sunma
description: Bu konu, Microsoft Dynamics 365 Commerce site Builder'a statik bir dosya yükleme ve bu dosyayı istemek için kullanılabilecek özel bir URL ve dosya adı oluşturma konularını açıklamaktadır.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595006"
---
# <a name="upload-and-serve-static-files"></a>Statik dosyaları karşıya yükleme ve sunma

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce site Builder'a statik bir dosya yükleme ve bu dosyayı istemek için kullanılabilecek özel bir URL ve dosya adı oluşturma konularını açıklamaktadır.

Bazı üçüncü taraf bağlayıcılar, bir dosyanın barındırılmasını ve e-ticaret sitesinden sunulmasını gerektirir. Bu bağlayıcılar, dosyanın istekler tarafından belirli bir geri arama URL'sine yol ve dosya adıyla verilmesini bekler. Bu nedenle bu konu, bir Dynamics 365 Commerce e-ticaret sitesinde Kullanıcı tarafından tanımlanabilir bir URL ve dosya adı bulunan statik bir dosyanın nasıl karşıya yükleneceğini ve hizmet verileceğini açıklamaktadır.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Statik dosya döndüren bir site URL'si oluştur

Commerce Site Builder 'da statik dosya döndüren bir site URL'si oluşturmak için aşağıdaki adımları izleyin.

1. Sitenizin ortam kitaplığına gidin ve tanımladığınız URL'ye istek tarafından sunulması gereken dosyayı karşıya yükleyin. Dosyayı zaten karşıya yüklediyseniz, bu adımı atlayabilirsiniz.
1. Sitenizin **URL**'lerine gidin.
1. **Yeni \> Yeni URL**'yi seçin.
1. **Yenı URL** iletişim kutusunda **ortam kitaplığı varlığı** seçeneğini belirleyin.
1. **URL yolu** alanına URL yolunu girin. Yola dosya adını dahil edin.
1. **Sonraki**'yi seçin. Ortam kitaplığı açılır ve **belge** türünün yüklenmiş olduğu tüm ortam varlıklarını gösterir .
1. Adım 5'te tanımladığınız URL'ye yönelik istekler için sunulması gereken dosyayı seçin.
1. **Kaydet**'i seçin.

Bu noktada, oluşturduğunuz URL Taslak durumundadır. URL'nin gösterdiği dosya, siz URL'yi yayınlana kadar döndürülmez. URL'yi yayımlamadan önce, doğru verileri döndüren doğrulamasını doğrulayabilirsiniz.

## <a name="validate-and-publish-a-url"></a>URL doğrulayın ve yayınlayın

Yayınlamadan önce URL'yi doğrulamak için aşağıdaki adımları izleyin.

1. Sitenizin **URL** 'lerine gidin ve önizlenecek URL'yi seçin.
2. Sağdaki Özellikler bölmesinde, **Düzenle** düğmesinin altında, doğru URL bağlantısını seçin. Yeni bir tarayıcı penceresi açılır ve bir 404 hatası almalısınız.
3. **?preview=inprogress** sorgu dizesini URL 'ye ekleyin (örneğin `https://yoursite.com/callback.html?preview=inprogress`) ve sayfayı yeniden yükleyin. Ortam kitaplığına yüklediğiniz dosya yanıt olarak döndürülmeli.

URL'yi doğruladıktan sonra yayımlayabilirsiniz.

1. Sitenizin **URL** 'lerine gidin ve URL'yi seçin.
2. Komut çubuğunda, **Yayınla** öğesini seçin.

## <a name="update-the-file-that-a-url-points-to"></a>URL'nin gösterdiği dosyayı Güncelleştir

URL yayımlandıktan sonra, farklı bir dosyayı işaret eden şekilde güncelleştirebilirsiniz. Alternatif olarak, sonraki bölümde açıklandığı gibi, URL'yi farklı türden bir kaynağa işaret eden bir kaynak türü gösteren şekilde güncelleştirebilirsiniz. Örneğin, URL'yi dahili bir sayfaya veya yeniden yönlendirmeye işaret edebilirsiniz.

URL'nin gösterdiği dosyayı güncelleştirmek için aşağıdaki adımları izleyin.

1. Sitenizin **URL** 'lerine gidin ve güncellenecek URL'yi seçin.
1. Sağdaki özellikler bölmesinde, **Düzenle**'yi seçin.
1. **URL ataması altında**, **Adım 2** kutusunu seçin ve ortam kitaplığından yeni bir belge seçin.
1. **Uygula**'yı seçin.

## <a name="update-the-asset-type-that-a-url-points-to"></a>URL'nin gösterdiği varlık türünü güncelleştir

Ayrıca bir URL'yi, dahili sayfa veya yeniden yönlendirme gibi farklı bir varlık türünü (kaynak) işaret eden şekilde güncelleştirebilirsiniz.

URL'nin gösterdiği varlık türünü güncelleştirmek için aşağıdaki adımları izleyin.

1. Sitenizin **URL** 'lerine gidin ve güncellenecek URL'yi seçin.
1. Sağdaki özellikler bölmesinde, **Düzenle**'yi seçin.
1. **URL ataması** altında , **1. adımda** farklı bir varlık türü seçin.
1. **Adım 2** kutusunu seçin ve sonra yeni varlığı seçin.
1. **Uygula**'yı seçin.

## <a name="change-the-url-path"></a>URL yolunu değiştir

URL oluşturulduktan sonra, yolu değiştirilemez. Bir dosyaya veya başka bir kaynak türüne hizmet veren URL yolunu değiştirmeniz gerekiyorsa, yeni bir URL oluşturmanız, varolan dosya veya diğer kaynakla eşlemeniz ve sonra eski URL'yi yayımdan kaldırmanız ve silmeniz gerekir.

URL yolu değiştirmek için, aşağıdaki adımları izleyin.

1. Yeni bir URL oluşturmak ve varolan bir dosyaya veya başka bir kaynağa eşlemek için, [Bu konunun yukarısındaki statik dosya bölümü döndüren bir site URL 'si oluştur konusundaki yönergeleri izleyin ](#create-a-site-url-that-returns-a-static-file).
1. Yeni URL'yi seçin ve komut çubuğunda **yayınla** 'yı seçin . Yeni URL yayımlandı.
1. Eski URL'yi yayımdan kaldırmak için, onu seçin ve sonra komut çubuğunda **Yayımdan Kaldır**'ı seçin. İsterseniz eski URL'yi artık silebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Dijital varlık yönetimine genel bakış](dam-overview.md)

[Resimleri karşıya yükleme](dam-upload-images.md)

[Videoları karşıya yükleme](dam-upload-video.md)

[Resimler ve videolar dışındaki dosyaları karşıya yükleme](dam-upload-files.md)

[Resimleri kırpma](dam-crop-images.md)

[Görüntü odak noktalarını özelleştirme](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
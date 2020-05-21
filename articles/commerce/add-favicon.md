---
title: Favicon ekleme
description: Bu konu, sitenize bir tercih simgesi ekleneceğini açıklamaktadır.
author: bicyclingfool
manager: annbe
ms.date: 04/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2d95e8b799c3b89418657342868e0ec7e94a86f9
ms.sourcegitcommit: ce79fb570e299a26a644e29da7ceb5a57a1374e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295092"
---
# <a name="add-a-favicon"></a>Favicon ekleme

[!include [banner](includes/banner.md)]

Bu konu, sitenize bir tercih simgesi ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bir tercih edilen simge, Web tarayıcısı sekmesinde, adres çubuğunda, gözatma geçmişinde ve diğer yerlerin yanı sıra yer imleri veya Sık Kullanılanlar'da gösterilen küçük bir grafik dosyasıdır. Markanızı temsil ettiğinden ve yeniden zorlayan ve sitenizi müşterilerinizin ziyaret ettiği diğer sitelerden ayırt etmenize yardımcı olacağından sitenize bir tercih edilen bir simge eklemeniz önerilir.

Sitenize çeşitli boyutlarda ve dosya türlerindeki birçok tercih edilebilir simge ekleyebilmenize rağmen bu konu, tek bir tercih edilen simgenin nasıl ekleneceğini göstermektedir. Ancak, aynı işlem ve yer, daha fazla tercih edilen simge eklemek için kullanılır.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Sitenizin varlık koleksiyonuna bir tercih simgesi yükleyin

Sitenizin varlık koleksiyonuna bir tercih simgesi yüklemek için aşağıdakileri takip edin.

1. Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.
1. Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.
1. Dosya Gezgini penceresinde, karşıya yüklemek istediğiniz site simgesi resim dosyasının konumuna göz atın, dosyayı ve ardından **Aç**'ı seçin.
1. **Medya Öğesini Karşıya Yükle** iletişim kutusunda gerekli başlığı ve alt metni girin.
1. Görüntüleri karşıya yükledikten hemen sonra yayımlamak isterseniz, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin.

    > [!NOTE]
    > **Yükledikten sonra medya öğelerini yayımla** onay kutusunu seçmezseniz, **Medya öğeleri** sayfasına dönmeniz ve daha sonra site simgesini el ile yayımlamanız gerekir.

1. **Tamam**'ı seçin.
1. Sağdaki özellik bölmesinde, tercih edilen simgenin ortak URL'sini kopyalayın. Bu URL'yi daha sonra kullanacaksınız.

## <a name="create-the-html-for-your-favicon"></a>Site simgeniz için HTML oluşturma

Tercih edilen simgenin HTML'ini oluşturmak için aşağıdaki HTML dizesini kullanın. **href** özniteliği için, **site\_simgeniz\_için\_genel\_URL**'yi önceden kopyaladığınız genel URL ile değiştirin.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-page-fragment-that-contains-a-metatag-for-your-favicon"></a>Site simgesi için meta etiketi içeren bir sayfa parçası oluşturma

Site simgesi için meta etiketi içeren bir sayfa parçası oluşturmak için aşağıdaki adımları seçin.

1. **Sayfa parçaları**'na gidin ve **Yeni**'yi seçin.
1. **Yeni Sayfa Parçası** iletişim kutusunda, sayfa parçasının temel aldığı modül olarak **Meta etiketleri**'ni seçin.
1. Sayfa parçası için bir ad girin ve **Tamam**'ı seçin.
1. Parça hiyerarşisi ağacında, **Varsayılan meta etiketleri** alt öğesini seçin.
1. Sağ bölmede, **Meta Etiketleri** altında **Ekle**'yi seçin ve site simgesi için daha önce oluşturduğunuz HTML dizesini girin. 
1. **Düzenlemeyi bitir**'i seçin, ardından sayfa parçasını yayımlamak için **Yayımla**'yı seçin.

## <a name="add-the-metatag-page-fragment-to-the-html-head-section-of-your-pages"></a>Meta etiket sayfası parçasını, sayfalarınızın HTML başlık bölümüne ekleyin

Meta etiket sayfası parçasını, sayfalarınızın HTML **başlık** bölümüne eklemek için şu adımları izleyin.

1. **Şablonlar**a gidin, site simgenizi eklemek istediğiniz sayfaların şablonunu açın ve **Düzenle**'yi seçin.
1. Şablon hiyerarşisi ağacında, **HTML başlığı** kapsayıcısının sağında bulunan üç nokta düğmesini (**...**) seçin ve sonra **Sayfa parçası ekle**'yi seçin.
1. **Sayfa Parçası Seç** iletişim kutusunda daha önce oluşturduğunuz meta etiketi sayfa parçasını ve sonra **Tamam**'ı seçin.
1. **Düzenlemeyi bitir**'i seçin, ardından şablonu yayımlamak için **Yayımla**'yı seçin.

> [!NOTE]
> Sitenizde birden fazla şablon kullanılıyorsa, tüm bunlara meta etiketleri sayfa parçasını eklemeniz gerekir.

Meta etiketleri sayfa parçasını eklediğiniz şablonu temel alan sayfaları önizlerken, tarayıcı sekmesinde site simgesini görmeniz gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Logo ekleme](add-logo.md)

[Site teması seçme](select-site-theme.md)

[CSS geçersiz kılma dosyalarıyla çalışma](css-override-files.md)

[Hoş geldiniz iletisi ekleme](add-welcome-message.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)


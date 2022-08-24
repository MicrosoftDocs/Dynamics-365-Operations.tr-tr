---
title: Site simgesi ekleme
description: Bu makale, sitenize bir tercih simgesi ekleneceğini açıklamaktadır.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 41d6d8f823c7364f9206fd0f7588e35b6f0a018a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270450"
---
# <a name="add-a-favicon"></a>Site simgesi ekleme

[!include [banner](includes/banner.md)]

Bu makale, sitenize bir tercih simgesi ekleneceğini açıklamaktadır.

Bir tercih edilen simge, Web tarayıcısı sekmesinde, adres çubuğunda, gözatma geçmişinde ve diğer yerlerin yanı sıra yer imleri veya Sık Kullanılanlar'da gösterilen küçük bir grafik dosyasıdır. Markanızı temsil ettiğinden ve yeniden zorlayan ve sitenizi müşterilerinizin ziyaret ettiği diğer sitelerden ayırt etmenize yardımcı olacağından sitenize bir tercih edilen bir simge eklemeniz önerilir.

Sitenize çeşitli boyutlarda ve dosya türlerindeki birçok tercih edilebilir simge ekleyebilmenize rağmen bu makale, tek bir tercih edilen simgenin nasıl ekleneceğini göstermektedir. Ancak, aynı işlem ve yer, daha fazla tercih edilen simge eklemek için kullanılır.

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

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Site simgesi için meta etiketi içeren bir parça oluşturma

Site simgesi için meta etiketi içeren bir parça oluşturmak için aşağıdaki adımları seçin.

1. **Parçalar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni parça** iletişim kutusunda, parçanın temel aldığı modül olarak **Meta etiketleri**'ni seçin.
1. Parça için bir ad girin ve **Tamam**'ı seçin.
1. Parça hiyerarşisi ağacında, **Varsayılan meta etiketleri** alt öğesini seçin.
1. Sağ bölmede, **Meta Etiketleri** altında **Ekle**'yi seçin ve site simgesi için daha önce oluşturduğunuz HTML dizesini girin. 
1. **Düzenlemeyi bitir**'i seçin, ardından parçayı yayımlamak için **Yayımla**'yı seçin.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Meta etiket parçasını, sayfalarınızın HTML başlık bölümüne ekleme

Meta etiket parçasını, sayfalarınızın HTML **başlık** bölümüne eklemek için şu adımları izleyin.

1. **Şablonlar** a gidin, site simgenizi eklemek istediğiniz sayfaların şablonunu açın ve **Düzenle**'yi seçin.
1. Şablon hiyerarşisi ağacında, **HTML başlığı** kapsayıcısının sağında bulunan üç nokta düğmesini (**...**) seçin ve sonra **Parça ekle**'yi seçin.
1. **Parçayı seç** iletişim kutusunda daha önce oluşturduğunuz meta etiketi sayfa parçasını ve sonra **Tamam**'ı seçin.
1. **Düzenlemeyi bitir**'i seçin, ardından şablonu yayımlamak için **Yayımla**'yı seçin.

> [!NOTE]
> Sitenizde birden fazla şablon kullanılıyorsa, tüm bunlara meta etiketleri parçası eklemeniz gerekir.

Meta etiketleri parçasını eklediğiniz şablonu temel alan sayfaları önizlerken, tarayıcı sekmesinde site simgesini görmeniz gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Logo ekleme](add-logo.md)

[Site teması seçme](select-site-theme.md)

[CSS geçersiz kılma dosyalarıyla çalışma](css-override-files.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

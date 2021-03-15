---
title: Gizlilik ilkesi sayfası ekle
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize gizlilik ilkesi sayfası ekleme yöntemi açıklanmıştır.
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a9e09a1d0dbd6c0dc94b5668bb29de6605e2ca9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980219"
---
# <a name="add-a-privacy-policy-page"></a>Gizlilik ilkesi sayfası ekle


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize gizlilik ilkesi sayfası ekleme yöntemi açıklanmıştır.

## <a name="overview"></a>Genel Bakış

Gizlilik uyumluluğu, site kullanıcılarını verilerinin nasıl toplanacağı ve işlendiği hakkında bilgi veren kuruluş önlemleri içerir. Böylece kullanıcılar, kişisel verilerinin nasıl işleneceğini istediklerini ve gerekli eylemleri nasıl ele alabilirler.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'te Microsoft Gizlilik Bildirimini inceleyin

Dynamics 365 Commerce yazma araçlarına oturum açarken Microsoft gizlilik bildirimi'ni gözden geçirmek için, sağ üst köşedeki **Yardım** düğmesini (**?**) seçin ve sonra **Gizlilik ve tanımlama bilgileri**'ni seçin. [Microsoft gizlilik bildirimi](https://privacy.microsoft.com/privacystatement)'ne bağlantı içeren yeni bir sekme açılır.

## <a name="build-a-privacy-policy-page-for-your-site"></a>Siteniz için bir gizlilik ilkesi sayfası oluşturun

Dynamics 365 Commerce'te, sitenizi kullanıcılarına Gizlilik ilkenizin erişim izni vermenin birkaç yolu vardır. Bu bölümde Gizlilik ilkesi sayfasının nasıl oluşturulacağı ve altbilgi parçası kullanılarak sayfaya nasıl referans bulunduğu gösterilmiştir.

Aşağıdaki kılavuz, bir ticaret sitesi için genel gizlilik ilkesi sayfasının nasıl oluşturulacağını gösteren bir örnektir. Şirketinizin yasal gereksinimlerini en iyi karşılayan Gizlilik ilkesi sayfası çözümü tasarlanırken ve uygulamadığınızdan sorumlusunuz.

Başlatmak için, yazma araçlarında, bir gizlilik ilkesi sayfası oluşturmak istediğiniz siteye gidin.

### <a name="create-a-template"></a>Şablon oluştur

> [!NOTE]
> Gizlilik ilkesi sayfası için kullanılabilecek bir şablon zaten oluşturulmuşsa, bir [gizlilik ilkesi sayfası oluştur](#build-a-privacy-policy-page) bölümüne geçin.

Bir şablon oluşturmak için şu adımları izleyin.

1. Bir sayfa şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Promosyon başlığı şablonu**'nu girin ve **Tamam**'ı seçin.
1. Şablonda, gerekli tüm sayfa yuvalarına gerekli modülleri ekleyin. Kılavuz için kırmızı Ünlem işaretlerinin üzerine gelin. (Örneğin, **HTML Başı** yuvası bir **Varsayılan Harici Komut Dosyası** modülü gerektirebilir.)
1. **Gövde** yuvasında bir **varsayılan sayfa** modülü ekleyin.
1. **Varsayılan sayfa** modülünde, **Ana** yuvasına bir **içerik zengin blok** modülü ekleyin.
1. **İçerik zengin blok** modülünde, bir **içerik zengin blok öğe** modülü ekleyin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="build-a-privacy-policy-page"></a>Gizlilik ilkesi sayfası oluştur

Gizlilik ilkesi sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seç** iletişim kutusunda gizlilik ilkesi sayfası şablonunu seçin.
1. Bir sayfa adı ve sayfa URL'si girin ve **Tamam**'ı seçin. 
1. Yeni sayfanın **ana** yuvasına bir **içerik zengin blok** modülü ekleyin.
1. **İçerik zengin blok** modülünde, bir **içerik zengin blok öğe** modülü ekleyin.
1. **İçerik zengin blok** modülü Özellikler bölmesinde **Veri Kaynağı Ekle**'yi ve sonra da **Zengin Metin İçeriği**'ni seçin.
1. Zengin metin düzenleyicisinde, Gizlilik ilkesi sayfası için içerik girin. Zengin metin Düzenleyicisini gerektiğinde tam ekran moduna genişletin.
1. İçeriği girmeyi bitirdiğinizde, Web tarayıcısında sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfa ve modül özelliklerine kalan tüm eklemeleri tamamlayın.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

Gizlilik ve ilke sayfası için URL yayınlamak için şu adımları izleyin.

1. **URL**'lere gidin ve Gizlilik ilkesi sayfasının URL'sini seçin.
1. Seçili URL'yi yayımlamak için **Yayımla**'yı seçin.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Altbilgide Gizlilik ilkesi sayfasına bağlantı oluştur

Bir parçaya Gizlilik ilkesi sayfası için bağlantı ekleyebilirsiniz. Bu şekilde, bir bağlantıyı paylaşabilir ve parçaya başvurarak birden fazla site sayfası arasında güncelleştirebilirsiniz. Bu örnek, bir altbilgi parçasına gizlilik ilkesi sayfası bağlantısının nasıl ekleneceğini gösterir.

Alt bilgi parçasına bğalantı eklemek için bu adımları izleyin.

1. **Parçalar**'a gidin ve yeni sayfa parçası oluşturmak için **Yeni**'yi seçin.
1. **Yeni parça** iletişim kutusunda, **Alt bilgi** modülünü seçin.
1. **Parça adı** altında, parça için bir ad girin ve **Tamam**'ı seçin.
1. **Altbilgi kategorisi** yuvasında bir **alt bilgi öğesi** modülü ekleyin.
1. Sağdaki özellikler bölmesinde, **Bağlantı metni**'ni seçin.
1. **Bağlantı metni** iletişim kutusunda, Gizlilik ilkesi sayfasının bağlantı metnini ve bağlantı hedefini girin ve **Tamam**'ı tıklatın.
1. Gizlilik ilkesi sayfasının URL'sini almak için, **sayfalar**'a gidin, Gizlilik ilkesi sayfasına gidin ve Özellikler bölmesinden URL'yi kopyalayın.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Parçanın önizlemesine bakın ve Gizlilik ilkesi sayfası bağlantısını sınayın.

Parça artık diğer site sayfaları için şablonda başvurulabilir. Bu parçaya bir şablonun **altbilgi** modülünde referans olduğu zaman, bağlantı başvurusu bu şablon kullanılarak oluşturulan tüm sayfalarda görünür.

## <a name="additional-resources"></a>Ek kaynaklar

[Uyumluluğa genel bakış](compliance-overview.md)

[Erişilebilirlik özellikleri ve yetenekleri](accessibility.md)

[Tanımlama bilgisi uyumluluğu](cookie-compliance.md)

[İzlenen içerik değişiklikleriyle ilişkili kullanıcı kimliklerini değiştirme](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
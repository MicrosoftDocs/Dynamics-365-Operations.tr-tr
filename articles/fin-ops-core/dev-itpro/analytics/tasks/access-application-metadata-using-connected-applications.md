---
title: Bağlı uygulamalar kullanarak uygulama meta verilerine erişme
description: Bu konudaki adımlarda, Regulatory configuration service kullanıcısının, meta verileri kullanarak nasıl yeni bir Elektronik raporlama modeli eşlemesi tasarlayabileceği açıklanmaktadır.
author: NickSelin
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88fb3a947dd15f80238baab5f315c889f47f5b3b
ms.sourcegitcommit: 273903b7b73ac726d447c50f7086e6d8b0f0f74e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087027"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Bağlı uygulamalar kullanarak uygulama meta verilerine erişme

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama rolüne sahip Regulatory Configuration Service (RCS) kullanıcısının Finance and Operations'taki meta verilerini kullanarak nasıl yeni bir Elektronik raporlama (ER) modeli eşlemesi tasarlayabildiğini açıklar. RCS bağlantılı uygulama kullanılarak uygulama meta verilerine çevrimiçi olarak erişilir. Örnek ER model eşlemesi, dış ticari hareketlere erişmek üzere yapılandırılacak. Bu adımları tamamlamak için öncelikle RCS'de [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) adımlarını tamamlamanız gerekir. Konudaki adımları tamamlamadıysanız [ER yapılandırma kullanarak uygulama meta verilerine erişim](access-application-metadata-er-configuration.md) [elektronik raporlama örnekleri](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) şu ER yapılandırmalarını indirmek ve kaydetmek için gidin: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml ve sonra prosedürü tamamlayın.

## <a name="prerequisites"></a>Önkoşullar
1. **Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin. 
2. Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız[Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın. 

## <a name="get-required-er-configurations"></a>Gerekli ER yapılandırmalarını alma
1. **Raporlama konfigürasyonları**'na tıklayın. 
2. [ER yapılandırması kullanarak uygulama meta verilerine erişme](access-application-metadata-er-configuration.md) prosedüründeki adımları tamamladıysanız mevcut RCS örneğinde gerekli tüm ER yapılandırmalarına (dış ticaret meta verileri, model ve harita yapılandırmaları) zaten sahipsiniz. Bu alt görevdeki kalan tüm adımları atlayabilirsiniz. 
3. **Değiştir**'e tıklayın. 
4. **XML dosyasından yükle**'ye tıklayın. 
5. **Gözat**'a tıklayın ve **Dış ticaret meta verileri.xml** dosyasını seçin. 
6. **Tamam**'a tıklayın. 
7. **Değiştir**'e tıklayın. 
8. **XML dosyasından yükle**'ye tıklayın. 
9. **Gözat**'a tıklayın ve **Dış ticaret meta modeli.xml** dosyasını seçin. 
10. **Tamam**'a tıklayın. 
11. **Değiştir**'e tıklayın. 
12. **XML dosyasından yükle**'ye tıklayın. 
13. **Gözat**'a tıklayın ve **Dış ticaret meta eşlemesi.xml** dosyasını seçin. 
14. **Tamam**'a tıklayın. 

## <a name="register-a-connected-application"></a>Bağlı bir uygulamayı kaydetme
1. Sayfayı kapatın. 
2. Sayfayı kapatın. 
3. **Tüm çalışma alanları** > **Elektronik raporlama**'ya gidin. 
4. **Bağlı uygulamalar** a tıklayın. 
5. Yapılandırılmış uygulamanın Azure tabanlı olduğundan ve geçerli RCS kullanıcısı için erişilebilir olduğundan emin olun. Ayrıca geçerli RCS kullanıcısının, seçilen uygulamaya erişimi olması ve uygulamanın meta verilerine erişim ayrıcalıkları veren bu uygulamanın kayıtlı bir kullanıcısı olması gerekir. 
6. **Yeni**'ye tıklayın. 
7. **Ad** alanına "MyConnectedApp" yazın. 
8. **Uygulama** alanına, "https:// mycompany.operations.dynamics.com" yazın. 
9. **Kiracı** alanına "mycompany.onmicrosoft.com" yazın. 
10. **Kaydet**'e tıklayın. 
11. Yapılandırılmış uygulamaya olan bağlantıyı denetlediğinizde **Uzak uygulamaya bağlan** sayfasında **Seçilen uzak uygulama bağlantısına bağlanmak için buraya tıklayın**'a tıklayın. 
12. **Bağlantıyı denetle**'ye tıklayın. 
13. **Kapat**'a tıklayın. 
14. Bağlantı doğrulaması başarılı olduğunda geçerli kılavuzda yapılandırılan uygulama için sürüm ve kiracı ayrıntıları güncelleştirilir. 

## <a name="review-existing-model-mapping-configuration"></a>Mevcut ER model eşleme yapılandırmasını inceleyin
1. Sayfayı kapatın. 
2. **Raporlama konfigürasyonları**'na tıklayın. 
3. Ağaçta **Dış ticari modeli** genişletin. 
4. Ağaçta **Dış ticari model\Dış ticari eşleme**'yi seçin. 
5. **Önkoşullar** bölümünü genişletin. 

    > [!NOTE]
    > Şu anda bu eşleme meta veri yapılandırmasına başvuruyor. Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verileri sunulacaktır. 

6. **Tasarımcı**'yı tıklatın. 
7. **Tasarımcı**'yı tıklatın. 
8. Ağaçta, **Dynamics 365 for Operations\Tablo kayıtları**'nı seçin. 
9. **Kök ekle**'ye tıklayın. 
10. **Tablo** alanında bir değer girin veya bir değer seçin. 

    > [!NOTE]
    > Şu anda bu eşleme meta veri yapılandırmasına başvuruyor. Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verileri sunulacaktır. 

11. **İptal**'e tıklayın 
12. Sayfayı kapatın. 
13. Sayfayı kapatın. 

## <a name="assign-connected-application-to-model-mapping"></a>Bağlantılı uygulamayı model eşlemeye atayın 
1. **Düzenle**'yi tıklatın. 
2. **Myconnectedapp** uygulamasını seçin. 

    > [!NOTE]
    > Şu anda bu eşleme, seçilen bağlı uygulamanın meta verilerine başvuruda bulunuyor. Aynı eşleme aynı anda meta veri yapılandırmasına ve bağlı uygulamaya başvurduğunda, bağlı uygulamanın meta verileri kullanılır. 

3. **Tasarımcı**'yı tıklatın. 
4. **Tasarımcı**'yı tıklatın. 
5. Ağaçta, **Dynamics 365 for Operations\Tablo kayıtları**'nı seçin. 
6. **Kök ekle**'ye tıklayın. 
7. **Tablo** alanında bir değer girin veya bir değer seçin. 

    > [!NOTE]
    > Bu eşleme için atanmış olan bağlı uygulamanın tüm meta verileri kullandığından ikiden fazla uygulama tablosu sunuldu. 

8. **İptal**'e tıklayın 
9. **Doğrula**'ya tıklayın. 

    > [!NOTE]
    > Belirtilen veri kaynağı öğeleriyle, bu eşleme için atanmış bağlı uygulamanın ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladık. 

10. Sayfayı kapatın. 
11. Sayfayı kapatın. 

Bu model eşlemesini farklı bir sürüm uygulamasının meta verilerini kullanarak değerlendirmeniz gerektiğinde, bağlı başka bir uygulamayı kaydedin, bu model eşlemesine atayın ve yeni meta verilere göre doğrulayın.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

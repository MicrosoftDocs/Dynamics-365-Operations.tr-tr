---
title: Customer Voice'u e-ticaret sitesi sayfalarıyla tümleştirme
description: Bu makale, Microsoft Dynamics 365 Customer Voice'u Dynamics 365 Commerce e-ticaret site sayfalarıyla tümleştirmeyi açıklamaktadır.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: c8c67ecf4950c92fc91c8d119e06e5e8afff0ddf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850342"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Customer Voice'u e-ticaret sitesi sayfalarıyla tümleştirme

[!include [banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Customer Voice'u Dynamics 365 Commerce e-ticaret site sayfalarıyla tümleştirmeyi açıklamaktadır.

Gerçek zamanlı müşteri geribildirimini toplamak, analiz etmek ve izlemek için [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/)'u e-ticaret sitenizle tümleştirebilirsiniz. Tümleştirmeye başlamak için bir hesap oluşturmanız ve toplamak istediğiniz geri bildirim türü için bir Customer Voice projesi şablonu seçmeniz gerekir.

## <a name="integrate-the-customer-voice-service"></a>Customer Voice hizmetini tümleştirme

Customer Voice hesabı oluşturmak için [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/)'a gidin ve istemleri izleyin.

Customer Voice hesabı oluşturup oturum açtıktan sonra, sonraki adımda toplamak istediğiniz geri bildirim türü için bir proje şablonu seçmeniz gerekir.

Bir Customer Voice projesi şablonu seçmek için, aşağıdaki adımları izleyin.

1. [Customer Voice proje şablonu sayfasına](https://customervoice.microsoft.com/Pages/ProjectPage.aspx) gidin.
1. **Kullanmaya başlayın**'ı seçin.
1. Toplamak istediğiniz geri bildirim türüne yönelik proje şablonunu seçin ve ardından **İleri**'yi seçin.
1. **Gönder** sekmesindeki **Ekleme biçimi seç** bölümünde ekleme biçimi seçin. **Ekleme kodu** alanı, Commerce site oluşturucusuna eklenmesi gereken kodu gösterir.

Bu makaledeki örneklerde, **Dönemsel müşteri anketi** proje şablonunu ve **Düğme** ekleme biçimi kullanılmıştır.

Aşağıdaki örnek çizimde, **Düğme** ekleme biçiminin seçildiği ve bu seçeneğin ekleme kodunun **Ekleme kodu** alanında görüntülendiği **Dönemsel müşteri anketi** proje şablonu sayfası gösterilmektedir. Aşağıdaki bölümlerde açıklandığı gibi, sağlanan kodu site sayfalarınıza eklemek için üç ayrı işlem gereklidir.

![Düğme seçeneğinin belirlenmiş olduğu Customer Voice Dönemsel müşteri anketi sayfası.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Harici betik URL'sini ekleme

Customer Voice anketi olması gereken tüm site sayfalarında, Customer Voice'un ekleme kodunda sağladığı harici betik URL'sini eklemeniz gerekir. Kodu birden çok site sayfasına eklemenin en iyi yolu, site oluşturucusunda harici betik URL'sini içeren bir parça oluşturmak ve bu parçayı uygun sayfa şablonlarına eklemektir. Güncelleştirilmiş bir şablonu yayımladıktan sonra, eklenen harici betik kodu etkilenen site sayfalarında aşağıdaki örneğe benzeyecektir.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Parçalar hakkında daha fazla bilgi için, bkz. [Parçalarla çalışma](work-with-fragments.md).

> [!NOTE]
> Parçaya yalnızca URL'yi eklemeniz gerekir. Harici betik modülü diğer betik kodunu ekler.

Harici betik URL'sini bir parçaya eklemek için aşağıdaki adımları izleyin.

1. Site oluşturucuda, [Harici betik modülünü](script-module.md) temel alan bir parça oluşturun.
1. Yeni parçada, **Varsayılan harici betik** alanını seçin.
1. **Varsayılan harici betik** özellikleri bölmesindeki **Betik kaynağı** alanına, aşağıdaki örnekte gösterildiği gibi harici betik URL'sini girin.

    ![Yeni parçanın Betik kaynağı alanında harici betik URL'si.](media/customer-voice-integration-2.png)

1. **Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. Parçayı yayımlamak için **Yayımla**'yı seçin.

Eklenen harici betik bloğunu içeren yeni parça şimdi uygun sayfa şablonuna eklenmeye hazırdır.

### <a name="embed-the-external-style-sheet-code"></a>Harici stil sayfası kodunu ekleme

Ardından, Customer Voice anketi olması gereken tüm site sayfalarında, Customer Voice'un ekleme kodunda sağladığı harici stil sayfası kodunu eklemeniz gerekir. Önceki bölümde olduğu gibi, harici stil sayfası kodunu birden çok site sayfasına eklemenin en iyi yolu, site oluşturucusunda stil sayfası kodunu içeren bir parça oluşturmak ve bu parçayı uygun sayfa şablonlarına eklemektir. Eklenen harici stil sayfası kodu aşağıdaki örnek koda benzer.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Harici stil sayfası kodunu bir parçaya eklemek için aşağıdaki adımları izleyin.

1. Site oluşturucuda, [Meta etiketler modülünü](metatags-module.md) temel alan bir parça oluşturun.
1. Parçada, **Varsayılan meta etiketler** alanını seçin.
1. **Varsayılan meta etiketler** özellikleri bölmesindeki **Meta etiketler** alanına, aşağıdaki örnekte gösterildiği gibi stil sayfası kodunu girin.

    ![Yeni parçanın Meta etiketler alanında harici stil sayfası kodu.](media/customer-voice-integration-3.png)

1. **Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. Parçayı yayımlamak için **Yayımla**'yı seçin.

Eklenen harici stil sayfası kodunu içeren yeni parça şimdi uygun sayfa şablonuna eklenmeye hazırdır.

### <a name="embed-the-inline-script-code"></a>Satır içi betik kodunu ekleme 

Ardından, Customer Voice anketi olması gereken tüm site sayfalarında, Customer Voice'un ekleme kodunda sağladığı satır içi betik kodunu eklemeniz gerekir. Önceki bölümlerde olduğu gibi, satır içi betik kodunu birden çok site sayfasına eklemenin en iyi yolu, site oluşturucusunda satır içi betik kodunu içeren bir parça oluşturmak ve bu parçayı uygun sayfa şablonlarına eklemektir.

Aşağıdaki satır içi betik kodu örneğinde, **SURVEY\_KEY** yer tutucudur. **SURVEY\_KEY** yer tutucusunun değeri, Customer Voice'un ekleme kodunda sağladığı asıl anket anahtarıyla eşleşmelidir. Son satır, kodların yüklenmesine yeterli süre tanımak amacıyla anket düğmesini işlemesi için kodu bir saniye sonra çağırır. Seçtiğiniz ankete bağlı olarak, şirket adı gibi başka meta veriler de eklemeniz veya güncelleştirmeniz gerekebilir.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Satır içi betik kodunu bir parçaya eklemek için aşağıdaki adımları izleyin.

1. Site oluşturucuda, [Satır içi betik modülünü](script-module.md) temel alan bir parça oluşturun.
1. Yeni parçada, **Varsayılan satır içi betik** alanını seçin.
1. **Varsayılan satır içi betik** özellikleri bölmesindeki **Satır içi betik** alanına, aşağıdaki örnekte gösterildiği gibi satır içi betik kodunu girin.

    ![Yeni parçanın Satır içi betik alanında satır içi betik kodu.](media/customer-voice-integration-4.png)

1. **Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. Parçayı yayımlamak için **Yayımla**'yı seçin.

Eklenen satır içi betik kodunu içeren yeni parça şimdi uygun sayfa şablonuna eklenmeye hazırdır.

## <a name="add-fragments-to-a-template"></a>Şablona parçalar ekleme

Customer Voice ekleme kodunu içeren parçaları oluşturmayı bitirdiğinizde, bunları kullanmak istediğiniz site sayfalarıyla ilişkilendirilmiş sayfa şablonlarına eklemeniz gerekir. Aşağıdaki örnek çizimde, üç örnek parça ürün ayrıntıları sayfası (PDP) şablonuna eklenmiştir.

![PDP şablonuna eklenen örnek parçalar.](media/customer-voice-integration-5.png)

Güncelleştirilmiş şablon yayımlandıktan sonra Customer Voice anketi, şablon tarafından denetlenen tüm sayfalarda görünür.

Şablonlar hakkında bilgi edinmek için bkz. [Şablonlarla çalışma](work-with-templates.md).

## <a name="configure-content-security-policy"></a>İçerik güvenlik ilkesini yapılandırma

Varsayılan olarak, ek yapılandırmalar yapılmadığı sürece içerik güvenlik ilkesi (CSP) başka hizmetlere çağrı yapılmasına izin vermez. Bu nedenle, güncelleştirilmiş şablonları yayımladıktan sonra anket ilgili site sayfalarında yüklenemeyebilir. CSP ile ilgili hataları görüntülemek için web tarayıcınızın geliştirici araçlarını (F12) açın ve anketi içeren bir sayfaya gidin. CSP ile ilgili hatalar konsol çıktısında gösterilir.

Site oluşturucusunda CSP'yi yapılandırarak hataları gidermek için aşağıdaki adımları izleyin.

1. **Site ayarları \> uzantılarına** gidin.
1. **İçerik güvenlik ilkesi** sekmesinde, **child-src** yönergesine `https://customervoice.microsoft.com/` adresini ekleyin.
1. **frame-src** yönergesine `https://customervoice.microsoft.com/` adresini ekleyin.
1. **img-src** yönergesine `https://mfpembedcdnmsit.azureedge.net` ve **.azureedge.net** adreslerini ekleyin.

Daha fazla bilgi için bkz. [İçerik güvenlik ilkesi](manage-csp.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Harici betik modülü](script-module.md)

[Meta etiketler modülü](metatags-module.md)

[Satır içi betik modülü](script-module.md)

[İçerik güvenlik ilkesi](manage-csp.md)

[Parçalarla çalışma](work-with-fragments.md)

[Şablonlarla çalışma](work-with-templates.md)

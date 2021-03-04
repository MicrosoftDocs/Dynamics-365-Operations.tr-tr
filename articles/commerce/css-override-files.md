---
title: CSS geçersiz kılma dosyalarıyla çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'te geçişli stil sayfalarının (CSS) nasıl geçersiz kılındığını, ne zaman ve nasıl kullanılacağını açıklamaktadır.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ec43b16b1df07400cffe597378ad4035e4d07e0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416429"
---
# <a name="work-with-css-override-files"></a>CSS geçersiz kılma dosyalarıyla çalışma


[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'te geçişli stil sayfalarının (CSS) nasıl geçersiz kılındığını, ne zaman ve nasıl kullanılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Kalıcı site stilleri genellikle sitenin teması üzerinden işlenmelidir. Temalar, sitenizin herhangi bir sayfasında modüller için temel CSS ve stil ayarlarını sağlar. Temalar, Dynamics 365 Commerce çevrimiçi yazılım geliştirme SETI (SDK) kullanılarak oluşturulur ve bunlar Web siteleriniz ile Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtılır. SDK yardımda Tema hata ayıklama özellikleri ve modül arabirim yapılandırmaları özelleştirilebilir ve ortaklaşa bulunmayan site tasarım paketleri oluşturur. Bu tasarım paketleri bir siteye dağıtıldığında, Site yazarları, site geliştirme yerine içerik oluşturma, düzenleme ve yayımlama işlemlerinde yoğunlaşabilir.

Bir temanın normal ömrü verildiğinde, SDK ve LCS dağıtım ardışık düzeninde stil değişiklikleri yapmak amacıyla geliştiricilerin bağımlılığı bazı senaryolarda potansiyel olarak ayarlanabilir. SDK yapılandırılmamışsa veya LCS dağıtımını beklemek için bir zaman kalmazsa, site prototipleri veya düzeltmeleri bir miktar görünebilir.

Bu senaryolarda, CSS dosyaları geçersiz kılma yardımcı olabilir. Commerce geliştirme araçlarında, kimliği doğrulanmış kullanıcılar bir CSS dosyayı karşıya yükleyebilir, önizleyebilir ve böylece sitenin temasını geçersiz kılmak için etkinleştirebilir. SDK veya LCS dağıtımının ek yükü gerekli değildir. CSS geçersiz kılma dosyasında belirtilen geçersiz kılmalar tek bir metin stilinde yapılan bir değişikliğe veya eksiksiz bir marka yelpazesinin geniş kapsamlı olabilir.

Dosyaları CSS geçersiz kılma işleminden önce, aşağıdaki sınırlamaları göz önünde bulundurun:

- Aynı anda CSS bir sitede yalnızca bir geçersiz kılma dosyası etkin olabilir. Bu nedenle, tüm etkin geçersiz kılmalar tek bir geçersiz kılma dosyasında bulunmalıdır.
- Geçersiz kılmaları Commerce geliştirme araçlarında önizleme yapabilseniz de, geçersiz kılmaların tanıtan hataları tanımlamaya yardımcı olan adanmış hata ayıklama özellikleri bulunmamaktadır. Başka bir deyişle, dosyaları CSS geçersiz kılma işlemini kullandığınızda, modül ve yazma doğrulaması için SDK'nın sağladığı araç takımı ile aynı olmaz.

Bununla birlikte CSS, dosyaları geçersiz kıl, bir tasarımı prototip almanın veya tam tema güncelleştirmesi geliştirip dağıtılmadan önce bir düzeltme uygulamaya yönelik olarak hızlı bir yol sağlar.

## <a name="create-a-css-override-file"></a>Bir CSS geçersiz kılma dosyası oluştur

CSS geçersiz kılma dosyası oluşturmak için herhangi bir tümleşik geliştirme ortamı (IDE), metin düzenleyicisi veya kaynak kodu düzenleyicisi kullanabilirsiniz. Normal bir yaklaşım, varolan sitenizdeki stil seçicileri, özellikleri ve değerleri tanımlamak için tarayıcınızda standart Web hata ayıklayıcıları kullanmaktır. Birçok tarayıcı değerleri değiştirmenize ve hata ayıklayıcıda önizlemenize olanak tanır. Yapmak istediğiniz değişiklikleri tanımladıktan sonra, onları kendi CSS dosyanıza kaydedebilirsiniz.

## <a name="upload-a-css-override-file"></a>CSS geçersiz kılma dosyası yükle

Bir CSS dosyasını Commerce'te sitenize yüklemek için aşağıdaki adımları izleyin.

1. Düzenleme araçlarında sitenize gidin.
1. Soldaki gezinti bölmesinde **Tasarımcı** seçin.

    > [!NOTE]
    > Kullanmakta olduğunuz Commerce geliştirme araçlarının sürümüne bağlı olarak, **tasarımcı** seçmeden önce gezinti bölmesindeki **ayarları** genişletmeniz gerekebilir.

1. Ana tasarım bölmesinin en üstünde, henüz seçilmemişse, **CSS geçersiz kıl** sekmesini seçin.
1. **Kullanılabilir CSS geçersiz kılmalar** altında, **CSS dosyasını karşıya yükle**'yi seçin. Bir Dosya Gezgini penceresi görünür.
1. Dosya Gezgininde, CSS dosyaya gözatın ve dosyayı seçin ve sonra **Aç**'ı seçin. Karşıya yüklenen CSS dosya artık **mevcut CSS geçersiz kılmalar** altında görünür.

## <a name="preview-a-css-override-file"></a>CSS geçersiz kılma dosyasını önizlemede görüntüleme

CSS geçersiz kılma dosyasını, canlı sitenizde etkin hale getirmek üzere önizlemek için, aşağıdaki adımları izleyin.

1. Sol taraftaki gezinme bölmesinde, **tasarım**'ı seçin ve sonra **CSS geçersiz kılma** sekmesinde, kullanılabilir **CSS geçersiz kılmalar** altında önizlemek istediğiniz CSS dosyayı bulun.
1. CSS dosya adının yanında **önizleme sitesi** seçeneğini belirleyin.
1. **URL Seç** iletişim kutusunda, geçersiz kılmanın uygulanmasını görmek istediğiniz sitenin URL 'sini seçin ve **Tamam** 'ı seçin.
1. Seçili URL'nin birden çok çeşidi varsa, görüntülenen **önizleme çeşitlemeleri** iletişim kutusunda istediğiniz değişkeni seçin.

Kendi stilinize karşı stilinizi doğrulayabileceğiniz yeni bir tarayıcı sekmesi veya penceresi açılır. Daha sonra, URL'yi gözden geçirip görüş bildirme amacıyla diğer kimliği doğrulanmış Commerce kullanıcılarıyla paylaşabilirsiniz.

## <a name="activate-a-css-override-file-on-your-live-site"></a>Canlı sitenizdeki CSS bir geçersiz kılma dosyasını etkinleştirme

CSS geçersiz kılma dosyasını önizledikten ve onayladıktan sonra, calı sitenizde etkinleştirebilirsiniz.

> [!NOTE]
> Aynı anda sitede yalnızca bir CSS geçersiz kılma dosyası etkin olabilir. Yeni bir geçersiz kılma dosyasını etkinleştirirseniz, önceki geçersiz kılma dosyası devre dışı demektir. Bu nedenle, tek bir CSS geçersiz kılma dosyasında gerekli tüm geçersiz kılmaların bulunduğundan emin olun.

CSS geçersiz kılma dosyasını etkinleştirmek için, aşağıdaki adımları izleyin.

1. Sol taraftaki gezinme bölmesinde, **tasarım**'ı seçin ve sonra **CSS geçersiz kılma** sekmesinde, kullanılabilir **CSS geçersiz kılmalar** altında etkinleştirmek istediğiniz CSS dosyayı bulun.
1. CSS dosya adı altında **Etkinleştir**'i seçin. Geçersiz kılma dosyası, canlı sitenizde hemen etkin hale gelir.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>Canlı sitenizdeki CSS bir geçersiz kılma dosyasını devre dışı bırakma

Sitenizdeki bir CSS geçersiz kılma dosyasını devre dışı bırakmak için aşağıdaki adımları izleyin.

1. Sol taraftaki gezinme bölmesinde, **tasarım**'ı seçin ve sonra **CSS geçersiz kılma** sekmesinde, kullanılabilir **CSS geçersiz kılmalar** altında devre dışı bırakmak istediğiniz CSS dosyayı bulun.
1. CSS dosya adı altında **Devre dışı bırak**'ı seçin. Geçersiz kılma dosyası, canlı sitenizde hemen devre dışı hale gelir.

> [!TIP]
> CSS geçersiz kılma dosyalarına ek seçeneklere erişmek için üç nokta (**...**) CSS dosya adının yanında. **Karşıdan yükleme**, **yenidenadlandırma** ve **değiştirme** seçenekleri, varolan bir CSS geçersiz kılma dosyasında hızlı değişiklikler yapmak için yararlıdır.

## <a name="additional-resources"></a>Ek kaynaklar

[Logo ekleme](add-logo.md)

[Site teması seçme](select-site-theme.md)

[Stil ön ayarlarıyla çalışma](style-presets.md)

[Favicon ekleme](add-favicon.md)

[Hoş geldiniz iletisi ekleme](add-welcome-message.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
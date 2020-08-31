---
title: Kişiselleştirilmiş ürün önerileri etkinleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce'un müşterileri için kişiselleştirilmiş ürün önerilerinin nasıl yapılacağı açıklanmaktadır.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4103096f23e5568cc2bf64f21720c7c16d3e0cd1
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664870"
---
# <a name="enable-personalized-recommendations"></a>Kişiselleştirilmiş önerileri etkinleştirme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'un müşterileri için kişiselleştirilmiş ürün önerilerinin nasıl yapılacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce uygulamasında perakendeciler, kişiselleştirilmiş ürün önerileri (kişiselleştirme olarak da bilinir) kullanabilir. Böylece, kişiselleştirilmiş öneriler müşteri deneyimine çevrimiçi ve satış noktasında (POS) dahil edilebilir. Kişiselleştirme işlevi açıldığında, sistem, bir kullanıcının satın alma ve ürün bilgilerini, kişiselleştirilmemiş ürün önerileri oluşturmak üzere ilişkilendirebilir.

## <a name="personalization-prerequisites"></a>Kişiselleştirme önkoşulları

Müşteriler için kişiselleştirilmiş ürün önerileri yapmadan önce, ürün önerilerinin yalnızca depolama alanını Azure Data Lake Store'a geçirmiş olan Commerce Users için desteklendiğini göz önünde bulundurun. Müşteriler kişiselleştirilmiş ürün önerileri alabilmek için, perakendecilerin [ürün önerileriniaçık](enable-product-recommendations.md) olmaları gerekir.

> [!NOTE]
> Ürün önerilerini etkinleştirerek, kişiselleştirmeyi de etkinleştirmeniz gerekir. Ancak, kişiselleştirmeyi kapatırsanız diğer ürün önerisi türlerini kapatmayın.

Ürün önerileri listeleri hakkında daha fazla bilgi edinmek için [Ürün önerilerine genel bakış](product-recommendations.md) başlıklı makaleye bakın.

## <a name="turn-on-personalization"></a>Kişiselleştirmeyi açın

Kişiselleştirmeyi açmak için aşağıdaki adımları izleyin.

1. **Perakende ve Ticaret \> ürün önerileri \> öneri parametrelerine** gidin.
1. Perakende paylaşılan parametreleri listesinde, **öneri listelerini** seçin.
1. **Kişiselleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.

![Kişiselleştirmeyi açma](./media/enablepersonalization.png)

> [!NOTE]
> Kişiselleştirmeyi etkinleştirdiğinizde, kişiselleştirilmiş ürün önerisi listeleri oluşturma işlemi başlatılır. Bu listelerin kullanılabilmesi ve çevrimiçi olarak ve POS'ta görülebilmesi için bir güne kadar gerekli olabilir.

## <a name="personalized-lists"></a>Kişiselleştirilmiş listeler

Öneri Servisi, varolan makine tarafından oluşturulan listelerin kişiselleştirmesine ek olarak, hem çevrimiçi hem de POS'ta ürün bulma deneyiminin kişiselleştirmesine olanak sağlar.

Kişiselleştirme etkinleştirildikten sonra, perakendeciler, tüm POS terminallerinde "sizin için özelleştirilmiş" listeler çevrimiçi veya "müşteri" için önerilen "listeleri gösterebilir. Ek olarak, perakendeciler varolan ürün öneri listelerine kişiselleştirmeye uygulayabilir ve kimliği doğrulanmış kullanıcılar için genel veri koruma düzenlemesi (GDPR) geri çevirme deneyimleri sağlayabilir. Kişiselleştirmeyi kapatırsanız bu özellikleri de devre dışı bırakırsanız.

### <a name="online-picks-for-you-lists"></a>Çevrimiçi "sizin için seçilenler" listeleri

"Sizin için seçilenler" listesi, kimliği doğrulanmış bir kullanıcıya önerilen ürünlerin kişiselleştirilmiş bir listesini gösteren yapay bir zekası-makine öğrenme (AI-ML) listesidir. Bu liste, kullanıcının çok yönlü kanal satın alma geçmişine dayalıdır. Kullanıcı başka Satın almalar da yaptığı için, kişiselleştirilmiş öneriler dinamik olarak güncelleştirilir. Bu tür bir liste ayrıca, perakendecilerin Gezinme hiyerarşileri temelinde en üstteki çekmeleri gösterebilmesi için kategori filtrelemeyi destekler.

"Sizin için seçilenler" listesi herhangi bir e-ticaret sayfasında görünebileceği için, aşağıdaki kullanıcı gereksinimlerinin karşılanması gerekir:

- Kullanıcıların oturum açmış olmaları gerekir. Anonim kullanıcılar kişiselleştirilmiş önerileri görmez.
- Kullanıcıların hesabında en az bir satın alım olması gerekir.
- Kullanıcıların kişiselleştirilmiş öneriler almak için kabul olmaları gerekiyor.

Aşağıdaki resimde, bir çevrimiçi mağaza sayfasındaki "sizin için seçilenler" listesinin bir örneği gösterilmektedir.

![Çevrimiçi "sizin için seçilenler" listeleri](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>POS'ta "müşteri için önerilenler" listeleri

Perakendeciler müşteir seçimi deneyimlerini geliştirmek için, varolan müşteri ayrıntıları sayfalarını, bağlamsal bir "müşteri için önerilenler" listesine ekleyerek kişiselleştirebilirler.

Aşağıdaki resimde, bir POS terminalindeki "Müşteri için önerilenler" listesinin bir örneği gösterilmektedir.

![POS'ta "müşteri için önerilenler" listesi](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Varolan öneri listelerine kişiselleştirmeyi Uygula

Perakendeciler, "yeni", "trend", "En çok satan", "Bunları da sevdiler" ve "Sıkça birlikte alındı" gibi varolan öneri listelerine kişiselleştirme uygulayabilir. Varolan listelere kişiselleştirme uygulandığında, oturum açmış bir kullanıcının önceden satın aldığı öğeler bu listelerden kaldırılır. Hem anonim kullanıcıların hem de kişiselleştirilmiş öneriler almakla karşılaşan kullanıcıların, varolan listelerin varsayılan sürümleri gösterilir. Bu nedenle, perakendeciler, ayrı sayfa deneyimlerini el ile korumak zorunda değildir.

Örneğin, oturum açmış bir Kullanıcı aşağıdaki çizimde yer alan "Trend - varsayılan" listesinde görünen siyah izlemeyi ve kahverengi çalışma ön yüklemeleri 'ni zaten satın aldı. Bu nedenle, Kullanıcı "Trend - kişiselleştirilmiş" listesinde gösterildiği gibi, bu ürünler yerine yeni ürünler görürler.

![Kişiselleştirme uygulanıyor](./media/applypersonalization.png)

Ticaret Sitesi Oluşturmada varolan bir öneri listesine kişiselleştirme uygulamak için, aşağıdaki adımları izleyin.

1. Ürün toplama modülünü içeren varolan bir site oluşturma sayfasını açın.
1. Soldaki gezinti bölmesinde ürün koleksiyon modülünü seçin.
1. Sağdaki gezinti bölmesinde **Ürünler**'in altında listeyi seçin.
1. **Ürün listesi konfigürasyonu seç** iletişim kutusunda, **Tür**'ün altında, liste türünü seçin.
1. **Kişiselleştirmeyi Uygula** onay kutusunu seçin ve **Tamam**'ı seçin.

    ![Bir trend listesine kişiselleştirme uygulanıyor](./media/ApplyPersonalizationToTrending.PNG)

1. Sayfa parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın. Sayfa yayımlandıktan sonra, oturum açan kullanıcılar kişiselleştirilmiş liste listeleri görür.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün önerilerine genel bakış](product-recommendations.md)

[Dynamics 365 Commerce ortamında Azure Data Lake Storage'yi etkinleştirme](enable-adls-environment.md)

[Ürün önerilerini etkinleştir](enable-product-recommendations.md)

["Benzer görünümleri araştır" önerilerini etkinleştirme](shop-similar-looks.md)

[Kişiselleştirilmiş önerilerden vazgeçme](personalization-gdpr.md)

[POS'ta ürün önerileri ekleme](product.md)

[Hareket ekranına öneriler ekleme](add-recommendations-control-pos-screen.md)

[AI-ML öneri sonuçlarını ayarlama](modify-product-recommendation-results.md)

[Seçkin önerileri el ile oluşturma](create-editorial-recommendation-lists.md)

[Demo verileriyle öneriler oluşturma](product-recommendations-demo-data.md)

[Ürün önerileri SSS](faq-recommendations.md)

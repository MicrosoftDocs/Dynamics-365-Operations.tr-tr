---
title: Modüllerle çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta modüllerin nasıl ve ne zaman kullanılacağını açıklamaktadır.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 06a26e5dfd35bf229e67ed27213210d0da726bdf
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698085"
---
# <a name="work-with-modules"></a>Modüllerle çalışma

Bu konu, Microsoft Dynamics 365 Commerce'ta modüllerin nasıl ve ne zaman kullanılacağını açıklamaktadır.

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a>Genel Bakış

Modüller, sayfa yapınızı oluşturan mantıksal yapı taşlarıdır ve çeşitli amaçlara ve kapsamlarına sahiptirler. Bazı modüller yüksek düzey konteynerlerdir ve bunların tek amacı diğer modülleri (alt modüller) tutmak ve düzenlemek içindir. Basit bir resim yerleşimi modülü gibi diğer modüller ise çok özel bir amaca sahiptir. Döngü modülü gibi diğer modüller ise bu iki kategori arasında bir yere denk düşen bir yer.

Varsayılan olarak Dynamics 365 Commerce siteniz, temel e-ticaret senaryolarını elde etmenizi sağlayan bir başlangıç kiti modül kitaplığı içerir. Bu modülleri kullanarak bir uçtan uca e-ticaret sitesi oluşturmak zorunda olmalısınız. Ancak, bu modülleri özelleştirmek veya belirli gereksinimler için yeni, özel modüller oluşturmak isteyebilirsiniz. Özel modüller oluşturmak istiyorsanız özel bir modül kitaplığı oluşturmanıza yardımcı olacak bir modül tasarımı yazılım geliştirme seti (SDK) vardır.

## <a name="container-modules-and-slots"></a>Konteyner modüller ve yuvalar

Daha önce belirtildiği gibi bazı modüller alt modülleri tutacak şekilde tasarlanmıştır. Bu modüller *konteyner* olarak bilinir ve iç içe geçmiş modül hiyerarşilerine izin verir. Konteyner modüller *yuvalar* içerir. Yuvalar, konteynerdeki alt modüllerin düzenini ve amacını işlemek için kullanılır. Aşağıda, çeşitli önemli yuvaların tanımlandığı, temel sayfa kapsayıcı modülü (herhangi bir sayfa için üst düzey modülüdür) yer alan bir örnek verilmiştir:

- Bir üstbilgi yuvası
- Bir gövde yuvası
- Bir altbilgi yuvası

Modülün geliştiricisi bu yuvaları tanımlar ve hangi alt modüllerin ve kaç alt modülün doğrudan bunun içine koyulacağını belirler. Örneğin, üstbilgi yuvası **üstbilgi modülü** türünün yalnızca bir modülünü destekleyebilir, oysa gövde yuvası herhangi bir türdeki (diğer sayfa kapsayıcı modüller dışında) sınırsız sayıda modülü destekleyebilir.

Yazma araçlarında, sayfa yazarlarının her yuvaya hangi modüllerin konulacağını ve bunların ne koyabileceği konusunda bilinmesi gerekmez. Sayfa yazarları bir yuva seçtikten sonra bu sayfaya eklenecek bir modül seçmeyi denediğinizde, bu yuva için desteklenen modül türlerinin filtrelenmiş bir görünümünü görürler.

## <a name="content-modules"></a>İçerik modülleri

İçerik modülleri, metin (ör., başlıklar, paragraflar ve bağlantılar) veya varlık başvuruları (ör., görüntüler, video ve PDF'ler) gibi içerik ve ortam öğeleri içerir. Tipik içerik modülü türlerine örnek olarak **Her**, **Özellik** ve **Ana başlık** verilebilir. Bu üç tür modüller metin veya ortam içerebilir ve sayfada herhangi bir şeyin görünmesini sağlamak için alt modüller gerekmez.

Normal, günlük sayfa ve içerik yazma faaliyetlerinin büyük çoğunluğu içerik modüllerini içerir çünkü bu modüller, üst kapsayıcı modüllerinde işlenen gerçek içeriği tanımlar. Birçok içerik modülü vardır ve bu modüller genellikle bir sayfanın iç içe modül hiyerarşisine ekleyebileceğiniz son taşlardır.

Aşağıdaki şekil, modüllerin üst kapsayıcı modül yuvalarında nasıl iç içe geçmiş olduğunu gösterir.

![İçe içe geçme modülleri](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Modül ekle veya kaldır

Aşağıdaki yordamlarda modüllerin nasıl ekleneceği ve kaldırılacağı açıklanmaktadır.

### <a name="add-a-module"></a>Modül ekle

Sayfada yuv aveya konteynere modül eklemek için bu adımları izleyin.

1. Soldaki anahat bölmesinde, alt modülün eklenebileceği bir konteyner veya yuva seçin.

    > [!NOTE]
    > Modül tasarımcısı, belirli bir modül yuvasına eklenebilecek modül türlerinin listesini tanımlar. Böylece, şablon yazarları, belirli bir şablondan oluşturulan tüm sayfalar için tutarlı arama motoru iyileştirmesi (SEO) ve geliştirme verimliliğini sağlamaya yardımcı olmak için izin verilen modül seçeneklerini geliştirebilirler.

1. Modül için üç nokta düğmesini (**...**) seçin ve sonra **Modül ekle**'yi seçin. **Modül Ekle** iletişim kutusu görünür. Yalnızca seçili konteynerde veya yuvada desteklenen modüller görünür şekilde bu iletişim kutusuna otomatik olarak filtre uygulanır. Modül listesi sayfa şablonu veya konteyner modülü tanımı tarafından belirlenir.

    > [!NOTE]
    > Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Modül Ekle** seçeneği kullanılamaz.

1. İletişim kutusunda, sayfanıza eklenecek bir modül arayıp seçin.

    > [!TIP]
    > **Özellik** ve **Hero** yeni başlayanlar için daha iyi modül türleridir.

1. Seçili modülü sayfanızdaki seçili konteynere veya yuvaya eklemek için **Tamam**'ı seçin.

### <a name="remove-a-module"></a>Modül kaldırma

Sayfada yuva veya konteynerden modül kaldırmak için bu adımları izleyin.

1. Soldaki anahat bölmesinde, kaldırılacak modülün adının yanında üç nokta düğmesini seçin ve çöp tenekesi düğmesini seçin.
1. Modülü kaldırma isteğinizi onaylamanız istendiğinde, **tamam**'ı seçin.

## <a name="configure-modules"></a>Modülleri konfigüre et

Aşağıdaki yordamlarda içerik ve konteyner modüllerin nasıl yapılandırılacağı açıklanmaktadır.

### <a name="configure-a-content-module"></a>Bir içerik modülü konfigüre edin

Sayfada bir içerik modülünü konfigüre etmek için aşağıdaki adımları izleyin.

1. Soldaki anahat bölmesinde bir içerik modülü türü seçin ( Örneğin, **özellik**, **hero** veya **başlık**).
1. Sağdaki Özellikler bölmesinde, üst bilgileri seçerek iç içe geçmiş denetimleri genişletin ve gerekli tüm denetim değerlerini ayarlayın.
1. Özellikler bölmesinde **veri yapılandırma** bölümü varsa genişletmek için bunu seçin. Aksi durumda, adım 5'e geçin.
1. **Veri Kaynağı Ekle** düğmesi varsa, bunu seçin ve eklenecek içerik öğelerini seçin.
1. Gerekli veya istenen modül denetimlerinin ayarlarını girin.
1. **Kaydet**'i seçin.

### <a name="configure-a-container-module"></a>Konteyner modülü yapılandırma

Sayfada bir konteyner modülünü konfigüre etmek için aşağıdaki adımları izleyin.

1. Sayfanızda bir konteyner modülü seçin (örneğin, bir döngü veya sıvı konteyner modülü).
1. Sağdaki Özellikler bölmesinde, üst bilgileri seçerek iç içe geçmiş denetimleri genişletin ve gerekli tüm denetim değerlerini ayarlayın.
1. Soldaki anahat bölmesinde, konteyner veya konteyner içindeki yuvalardan birinin adının yanında üç nokta düğmesini seçin ve **Modül ekle**yi seçin. Daha sonra seçili konteynere alt modüller ekleyin. Daha fazla bilgi için bu konunun önceki [modül ekleme](#add-a-module) yordamına bakın.
1. Bir üst kapsayıcıda eş öğe olarak birden fazla alt modül varsa, bunların görüntüleme sıralarını üst konteynerde değiştirebilirsiniz. Modül için üç nokta düğmesini seçin ve sonra yukarı ok ve aşağı ok düğmelerini kullanın.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Şablonlarla çalışma](work-with-templates.md)

[Önceden ayarlanmış düzenlerle çalışma](work-with-layouts.md)

[Parçalarla çalışma](work-with-fragments.md)

[Sayfaya konteyner modülü ekleme](add-container-module.md)

[Sayfaya İçerik yerleştirme modülleri ekleme](add-content-placement-modules.md)


---
title: Modüllerle çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta modüllerin nasıl ve ne zaman kullanılacağını açıklamaktadır.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 89d95814e892e3afcb6514ab0d0219f7b08b9c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000471"
---
# <a name="work-with-modules"></a>Modüllerle çalışma

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta modüllerin nasıl ve ne zaman kullanılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Modüller, sayfa yapınızı oluşturan mantıksal yapı taşlarıdır ve çeşitli amaçlara ve kapsamlarına sahiptirler. Bazı modüller yüksek düzey konteynerlerdir ve bunların tek amacı diğer modülleri (alt modüller) tutmak ve düzenlemek içindir. Basit bir resim yerleşimi modülü gibi diğer modüller ise çok özel bir amaca sahiptir. Döngü modülü gibi diğer modüller ise bu iki kategori arasında bir yere denk düşen bir yer.

Varsayılan olarak Dynamics 365 Commerce siteniz, temel e-ticaret senaryolarını elde etmenizi sağlayan bir modül kitaplığı içerir. Bu modülleri kullanarak bir uçtan uca e-ticaret sitesi oluşturmak zorunda olmalısınız. Ancak, bu modülleri özelleştirmek veya belirli gereksinimler için yeni, özel modüller oluşturmak isteyebilirsiniz. Özel modüller oluşturmak istiyorsanız özel bir modül kitaplığı oluşturmanıza yardımcı olacak bir modül tasarımı yazılım geliştirme seti (SDK) vardır.

## <a name="container-modules-and-slots"></a>Konteyner modüller ve yuvalar

Daha önce belirtildiği gibi bazı modüller alt modülleri tutacak şekilde tasarlanmıştır. Bu modüller *konteyner* olarak bilinir ve iç içe geçmiş modül hiyerarşilerine izin verir. Konteyner modüller *yuvalar* içerir. Yuvalar, konteynerdeki alt modüllerin düzenini ve amacını işlemek için kullanılır. Aşağıda, çeşitli önemli yuvaların tanımlandığı, temel sayfa kapsayıcı modülü (herhangi bir sayfa için üst düzey modülüdür) yer alan bir örnek verilmiştir:

- Bir üstbilgi yuvası
- Bir alt başlık yuvası
- Bir ana yuva
- Bir altbilgi yuvası
- Bir alt bilgi yuvası

Modülün geliştiricisi bu yuvaları tanımlar ve hangi alt modüllerin ve kaç alt modülün doğrudan bunun içine koyulacağını belirler. Örneğin, üstbilgi yuvası **üstbilgi modülü** türünün yalnızca bir modülünü destekleyebilir, oysa gövde yuvası herhangi bir türdeki (diğer sayfa kapsayıcı modüller dışında) sınırsız sayıda modülü destekleyebilir.

Yazma araçlarında, sayfa yazarlarının her yuvaya hangi modüllerin konulacağını ve bunların ne koyabileceği konusunda bilinmesi gerekmez. Sayfa yazarları bir yuva seçtikten sonra bu sayfaya eklenecek bir modül seçmeyi denediğinizde, bu yuva için desteklenen modül türlerinin filtrelenmiş bir görünümünü görürler.

## <a name="content-modules"></a>İçerik modülleri

İçerik modülleri, metin (ör., başlıklar, paragraflar ve bağlantılar) veya varlık başvuruları (ör., görüntüler, video ve PDF'ler) gibi içerik ve ortam öğeleri içerir. Tipik içerik modülü türleri arasında içerik bloku, metin bloku ve promosyon başlık modülleri bulunur. Bu üç tür modüller metin veya ortam içerebilir ve sayfada herhangi bir şeyin görünmesini sağlamak için alt modüller gerekmez.

Normal, günlük sayfa ve içerik yazma faaliyetlerinin büyük çoğunluğu içerik modüllerini içerir çünkü bu modüller, üst kapsayıcı modüllerinde işlenen gerçek içeriği tanımlar. Birçok içerik modülü vardır ve bu modüller genellikle bir sayfanın iç içe modül hiyerarşisine ekleyebileceğiniz son taşlardır.

Aşağıdaki şekil, modüllerin üst kapsayıcı modül yuvalarında nasıl iç içe geçmiş olduğunu gösterir.

![İçe içe geçme modülleri](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Modül ekle veya kaldır

Aşağıdaki yordamlarda modüllerin nasıl ekleneceği ve kaldırılacağı açıklanmaktadır.

### <a name="add-a-module"></a>Modül ekle

Sayfada yuv aveya konteynere modül eklemek için bu adımları izleyin.

1. Soldaki ana hat bölmesinde veya doğrudan ana tuvalde, alt modülün eklenebileceği bir kapsayıcı veya yuva seçin.

    > [!NOTE]
    > Modül tasarımcısı, belirli bir modül yuvasına eklenebilecek modül türlerinin listesini tanımlar. Böylece, şablon yazarları, belirli bir şablondan oluşturulan tüm sayfalar için tutarlı arama motoru iyileştirmesi (SEO) ve geliştirme verimliliğini sağlamaya yardımcı olmak için izin verilen modül seçeneklerini geliştirebilirler. Bir yuvaya modül eklerken **Modül Ekle** iletişim kutusu, yalnızca seçili kapsayıcı veya yuvada desteklenen modülleri gösterecek şekilde otomatik olarak filtrelenir. Bu izin verilen modüüller liste sisayfa şablonu veya kapsayıcı modülü tanımı tarafından belirlenir.

1. Ana hat bölmesini kullanıyorsanız, modül adının yanındaki üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin. Denetimleri doğrudan tuval içinde kullanıyorsanız, boş bir yuvada veya seçili olan modüle bitişik olan artı sembolünü (**++**) seçin ve sonra **Modül Ekle**'yi seçin.

    > [!NOTE]
    > Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Modül Ekle** seçeneği kullanılamaz.

1. **Modül Ekle** iletişim kutusunda, sayfanıza eklenecek bir modül arayıp seçin.

    > [!TIP]
    > **İçerik bloku**, yeni başlayanların çalışması için iyi bir modüldür.

1. Seçili modülü sayfanızdaki seçili konteynere veya yuvaya eklemek için **Tamam**'ı seçin.

### <a name="remove-a-module"></a>Modül kaldırma

Sayfada yuva veya konteynerden modül kaldırmak için bu adımları izleyin.

1. Soldaki ana hat bölmesinde, kaldırılacak modülün adının yanında üç nokta (**...**) düğmesini seçin ve çöp kutusu sembolünü seçin. Alternatif olarak, ana tuval içinde, seçili bir modülün araç çubuğunda çöp kutusu sembolünü seçebilirsiniz.
1. Modülü kaldırma isteğinizi onaylamanız istendiğinde, **Tamam**'ı seçin.

## <a name="move-a-module-to-a-new-position"></a>Mobülü yeni bir konuma taşıma

Bir modülü sayfanızda yeni bir konuma taşımak için aşağıdaki yöntemlerden birini kullanın.

### <a name="move-a-module-using-the-outline-pane"></a>Bir modülü ana hat bölmesini kullanarak taşıma

Bir modülü ana hat bölmesini kullanarak taşımak için aşağıdaki adımları izleyin.

1. Ana hat bölmesinde taşımak istediğiniz modülü seçin ve tutun, sonra modülü ana hatta yeni bir konuma sürükleyin. Ana hattaki ve tuvaldeki mavi çizgi modülün nereye yerleştirilebileceğini belirtir.
1. Yeni pozisyona bırakmak için modülü serbest bırakın.

### <a name="move-a-module-directly-within-the-canvas"></a>Modülü doğrudan tuval içinde taşıma

Bir modülü doğrudan tuval içinde taşımak için aşağıdaki adımları izleyin.

1. Tuvalde taşımak istediğiniz modülü seçin. 
1. Modülün araç çubuğunda yukarı veya aşağı doğru bir ok sembolü seçin ve sonra oku sayfada yeni bir konuma sürükleyin. Tuval ve ana hattaki mavi çizgi modülün nereye yerleştirilebileceğini belirtir. Bir modül yukarı veya aşağı taşınamayacağı takdirde o ok sembolü gri kalır. 
1. Yeni pozisyona bırakmak için modülü serbest bırakın.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Bir modülü üç nokta menüsünü kullanarak taşıma

Bir modülü üç nokta menüsünü kullanarak taşımak için aşağıdaki adımları izleyin.

1. Ana hattan veya tuval içinden bir modül seçin.
1. Ana hat bölmesinde modül adının yanındaki veya tuval içinde modülün araç çubuğundaki üç noktayı (**...**) seçin.
1. Modül, kapsayıcı veya yuva içinde yukarı veya aşağı taşınacaksa, **Yukarı** veya **Aşağı** seçeneklerini görürsünüz. Modülü, alt öğelerine göre yukarı veya aşağı taşımak için istenen taşıma seçeneğini belirleyin.

## <a name="configure-modules"></a>Modülleri konfigüre et

Aşağıdaki yordamlarda içerik ve konteyner modüllerin nasıl yapılandırılacağı açıklanmaktadır.

### <a name="configure-a-content-module"></a>Bir içerik modülü konfigüre edin

Sayfada bir içerik modülünü konfigüre etmek için aşağıdaki adımları izleyin.

1. Soldaki ana hat bölmesinde ağacı genişletin ve herhangi bir içerik modülünü seçin (örneğin, **İçerik bloku**). Alternatif olarak modülü ana tuvalde de seçebilirsiniz.
1. Sağdaki modül özellikleri bölmesinde istenen modül denetimlerinin özelliklerini girin.
1. Komut satırında **Kaydet**'i seçin. Bu, önizleme tuvalini de yenilenecek.

### <a name="edit-module-text-properties"></a>Modül metni özelliklerini düzenleme

Salt okunur olmayan modül metni özellikleri doğrudan tuval içinde düzenlenebilir.

Modül metni özelliklerini düzenlemek için aşağıdaki adımları izleyin.

1. Tuvaldeki metin denetimini seçin ve sonra imlecinizi metni düzenlemek istediğiniz yere getirin.
1. Metin içeriğinizi girin.
1. Diğer içeriği düzenlemeye devam etmek için metin içeriğinin dışında bir yeri seçin.

### <a name="inline-image-selection"></a>Satır içi resim seçimi

Salt okunur olmayan modül resimleri doğrudan tuvalden değiştirilebilir.

Bir içerik modülüne yönelik yeni bir resim seçmek için aşağıdaki adımları izleyin.

1. Tuval içinde, resme çift tıklayın. Bu, ortam seçici penceresini açar.
1. Kullanmak istediğiniz yeni bir resmi bulup seçin ve **Tamam'ı** seçin. Yeni resim tuval içinde işlenir.

### <a name="configure-a-container-module"></a>Konteyner modülü yapılandırma

Sayfada bir konteyner modülünü konfigüre etmek için aşağıdaki adımları izleyin.

1. Sayfanızda bir konteyner modülü seçin (örneğin, bir döngü veya sıvı konteyner modülü).
1. Sağdaki Özellikler bölmesinde, üst bilgileri seçerek iç içe geçmiş denetimleri genişletin ve gerekli tüm denetim değerlerini ayarlayın.
1. Soldaki anahat bölmesinde, konteyner veya konteyner içindeki yuvalardan birinin adının yanında üç nokta düğmesini seçin ve **Modül ekle** yi seçin. Daha sonra seçili konteynere alt modüller ekleyin. Daha fazla bilgi için bu konunun önceki [Modüllerle çalış](#add-a-module) bölümüne bakın.
1. Bir üst kapsayıcıda eş öğe olarak birden fazla alt modül varsa, bunların görüntüleme sıralarını üst konteynerde değiştirebilirsiniz. Modül için üç nokta düğmesini seçin ve sonra yukarı ok ve aşağı ok düğmelerini kullanın.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Şablonlarla çalışma](work-with-templates.md)

[Önceden ayarlanmış düzenlerle çalışma](work-with-layouts.md)

[Parçalarla çalışma](work-with-fragments.md)

[Sayfaya konteyner modülü ekleme](add-container-module.md)

[Yayımlama gruplarıyla çalışma](publish-groups.md)


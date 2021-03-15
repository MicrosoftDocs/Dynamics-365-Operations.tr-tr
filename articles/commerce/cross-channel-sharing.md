---
title: Kanallar arası paylaşımı etkinleştirme ve kullanma
description: Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucunun çapraz kanal paylaşımı özelliğinin nasıl etkinleştirileceği ve kullanılacağı açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3990365dda0a0cff7adcc1d97120293d43f6e858
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973143"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Kanallar arası paylaşımı etkinleştirme ve kullanma

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucunun çapraz kanal paylaşımı özelliğinin nasıl etkinleştirileceği ve kullanılacağı açıklanmaktadır.

## <a name="overview"></a>Genel bakış

Kanallar arası paylaşım, perakendecilere bir sitenin çoklu kanalları arasında içeriği yeniden kullanma ve paylaşma olanağı sağlar. Bu özellik, site kanallarının uyumlu bir temel dili olduğunda veya ortak olarak çok sayıda içerik öğesi olduğunda yararlıdır.

Kanallar arası paylaşım, istenen içeriğin kanala özgü sürümü bulunamadığında, kullanılabilir içerik aranabilecek bir varsayılan kanal etkinleştirilerek çalışır. Kanallar arasında paylaştırılması amaçlanan içerik varsayılan kanalda oluşturulur. Bu içerik, herhangi bir site kanalında kullanılan herhangi bir yerel ayar için yerelleştirilebilir.

## <a name="when-to-use-cross-channel-sharing"></a>Kanallar arası paylaşım ne zaman kullanılır?

Kanallar arası paylaşım, tek bir sitedeki birden fazla kanal içeriği paylaşabileceği zaman yararlıdır. Örneğin, tek bir site altında gruplandırılan birden çok markaya ve mağazaya sahip olan bir satıcı, bazı içerikleri mağazaların bir kısmı veya tümü arasında paylaşabilir. Bu paylaşılan içerik hüküm ve koşullar, ödeme koşulları, sevkiyat yöntemleri ve sık sorulan sorular (SSS) ile ilgili sayfalar içerebilir.

Kanallar arası paylaşım parçaları da destekler. Bu nedenle, kanala özgü parçaları içeren bir içerik sayfası, çapraz kanal içeriği olarak oluşturulabilir. Bu durumda, içeriğin büyük çoğunluğu kanallar arasında paylaştırılsa da, bir çapraz kanal sayfasındaki kanala özgü parçalar yalnızca ilgili mağaza kanalından istendiğinde işlenir.

Yalnızca bir kanalı olan siteler veya içerik paylaşamayan birden çok kanalı olan siteler, kanallar arası paylaşımdan yararlanamaz.

## <a name="enable-cross-channel-sharing"></a>Kanallar arası paylaşımı etkinleştirme

Kanallar arası paylaşım site düzeyinde etkinleştirilir. Bu işlem tek yönlüdür. Başka bir deyişle, kanallar arası paylaşım etkinleştirildikten sonra devre dışı bırakılamaz.

Commerce site oluşturucuda kanallar arası paylaşımı etkinleştirmek için aşağıdaki adımları izleyin.

1. **Site ayarları \> Özellikler**'e gidin.
1. **Çapraz Kanal** özelliğini **Açık** olarak ayarlayın.

    ![Commerce Site Builder'da Çapraz Kanal seçeneği açık olarak ayarlandı](./media/enabling-cross-channel-sharing.png)

Kanallar arası paylaşımı etkinleştirdikten sonra, çapraz kanal bilgileri aşağıdaki örneklemede görüldüğü gibi, **Site ayarları \> Özellikler** konumundaki **Kanallar** bölümünde görünür.

![Kanallar arası paylaşım etkinleştirildikten sonra görünür olan kanal bilgileri](./media/channels-cross-channel.png)

Ek olarak, kanallar arası paylaşımı etkinleştirdikten sonra, Commerce site oluşturucunun sağ üst tarafındaki **Kanal** alanı çapraz kanal içeriğini aşağıdaki örnekte gösterildiği şekilde yönetebileceğiniz **Çapraz Kanal Çevrimiçi Mağaza** seçeneğini içerir.

![Kanallar arası paylaşım etkinleştirildikten sonra Kanallar alanındaki Çapraz Kanal Çevrimiçi Mağaza seçeneği](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Çapraz kanal içeriği oluşturma ve kullanma

Çapraz kanal içeriğini birden çok şekilde oluşturabilir ve kullanabilirsiniz. Örneğin, çapraz kanal parçaları oluşturabilir, çapraz kanal ve kanala özgü içerik kullanan çapraz kanal sayfaları oluşturabilir ve kanala özel parça sürümleri ile çapraz kanal parçalarını geçersiz kılabilirsiniz.

### <a name="create-a-cross-channel-fragment"></a>Çapraz kanal parçası oluşturma

Commerce site oluşturucuda çapraz kanal parçası oluşturmak için aşağıdaki adımları izleyin.

1. **Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.
1. **Yeni parça** iletişim kutusunda, **Promosyon başlığı** modülünü seçin ve sonra **Parça adı** altında bir ad girin (örneğin, **Çapraz kanal başlığı**). Daha sonra **Tamam**'ı seçin.
1. **Promosyon başlığı** modülünün özellik bölmesinde, **İleti ekle**'yi seçin ve sonra **İleti**'yi seçin.
1. **İleti** iletişim kutusunda, **Metin** alanına **Çapraz kanal** girin ve **Tamam**'ı seçin. 
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

Bu çapraz kanal parçası, herhangi bir site kanalında oluşturulan çapraz kanal veya kanala özel sayfalarda kullanılabilir.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Çapraz kanal içeriğini kullanan bir çapraz kanal sayfası oluşturma

Çapraz kanal sayfaları sitenizin herhangi bir kanalında kullanılabilir. Bu nedenle, paylaşılan içerik sayfasını bir kez oluşturup sonraki güncelleştirmeleri tek bir yerde yapabilirsiniz. Örneğin, `/toc` URL'sine sahip bir çapraz kanal **Hüküm ve koşullar** sayfası bir sitenin tüm kanalları arasında paylaşılabilir. Site kanallarının temel URL'leri `www.fabrikam.com/brand1` ve `www.fabrikam.com/brand2` ise aynı çapraz kanal, paylaşılan **Hükümler ve koşullar** sayfası sırasıyla her iki site kanal URL'sinde de kullanılabilir olacaktır: `www.fabrikam.com/brand1/toc` ve `www.fabrikam.com/brand2/toc`. **Hüküm ve koşullar** sayfasının daha sonra güncelleştirilmesi gerekiyorsa, yalnızca tek, paylaşılan sayfayı güncelleştirmeniz gerekir.

Commerce site oluşturucuda çapraz kanal içeriğini kullanan bir çapraz kanal sayfası oluşturmak için aşağıdaki adımları izleyin.

1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seçin** iletişim kutusunda **Pazarlama** gibi bir şablon seçin.
1. **Sayfa Adı** alanına sayfa için ad girin (örneğin, **Çapraz kanal sayfası**).
1. **Sayfa URL**'si alanına bir sayfa URL'si girin (örneğin, **examplepage**) ve sonra **Tamam**'ı seçin.
1. Yeni sayfanın **Ana** yuvasında, üç nokta düğmesini (**...**) ve sonra **Parça ekle**'yi seçin.
1. **Parça Ekle** iletişim kutusunda, promosyon başlığı bulunan daha önce oluşturduğunuz çapraz kanal parçasını ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. "Çapraz-kanal" yazan promosyon başlığını görmelisiniz.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Çapraz kanal içeriğini kullanan bir kanala özel sayfa oluşturma

Kanala özel sayfalarda çapraz kanal içeriği kullanarak paylaşılan içerik parçasını bir kez oluşturup kanala özel sayfalarda kullanabilirsiniz. Bu "tek kaynak" hüküm ve koşullar, ödeme koşulları veya ilgili kişi bilgileri gibi paylaşılan içerikler için faydalıdır.

Commerce site oluşturucuda çapraz kanal içeriğini kullanan kanala özel sayfa oluşturmak için aşağıdaki adımları izleyin.

1. Belirli bir kanaldan (örneğin, **Fabrikam genişletilmiş çevrimiçi mağaza** gibi), **Sayfalar**'a gidin ve ardından yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon seçin** iletişim kutusunda **Pazarlama** gibi bir şablon seçin.
1. **Sayfa adı** alanına sayfa için ad girin (örneğin, **Kanala özel sayfa**).
1. **Sayfa URL**'si alanına bir sayfa URL'si girin (örneğin, **channelspecificpage**) ve sonra **Tamam**'ı seçin.
1. Yeni sayfanın **Ana** yuvasında, üç nokta düğmesini (**...**) ve sonra **Parça ekle**'yi seçin.
1. **Parça Ekle** iletişim kutusunda **Kanal** altında, **Çapraz Kanal Çevrimiçi Mağaza**'yı seçin. Daha önce oluşturduğunuz çapraz kanal parçası listede görünmelidir. Bunu seçin ve ardından **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. "Çapraz-kanal" yazan promosyon başlığını görmelisiniz.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Çapraz kanal sayfasının kanala özel sürümünü oluşturma

Kanallar arası paylaşım, çapraz kanal içeriğinin geçersiz kılınmasını destekler. Örneğin, site kanallarından biri dışındaki tümü aynı içerik parçasını paylaşır. Bu bir site kanalının farklı içeriği olması gerekir. Farklı içerik uygulamak için, çapraz kanal sayfasının kanala özel sürümünü oluşturarak, kanala özgü içerikle çapraz kanal içeriğini geçersiz kılarsınız.

Commerce site oluşturucuda çapraz kanal içeriğinin kanala özel sürümünü oluşturmak için aşağıdaki adımları izleyin.

1. Sağ üst köşedeki **Kanal** alanında, **Çapraz Kanal Çevrimiçi Mağaza**'yı seçin.
1. Daha önce oluşturduğunuz çapraz kanal sayfasını açın.
1. Sağ üst köşedeki **Kanal** alanında belirli içeriğe sahip olması gereken kanalı seçin. Sayfa düzenleyicisi yeni bir sayfa varyantı oluşturmanızı isteyen bir ileti gösterir.
1. **Sayfa varyantı oluştur** seçeneğini belirleyin.
1. Sayfa varyantının **Ana** yuvasında, üç nokta düğmesini (**...**) ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Promosyon başlığı** modülünü seçin ve **Tamam**'ı seçin.
1. **Promosyon başlığı** modülünün özellik bölmesinde, **İleti ekle**'yi seçin ve sonra **İleti**'yi seçin.
1. **İleti** iletişim kutusunda, **Metin** alanına **Kanala özel** girin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin. "Kanala-özel" yazan promosyon başlığını görmelisiniz.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

Şimdi, kanalın temel URL'sini kullanır ve bu sitedeki çapraz kanal sayfasının URL'sine giderseniz, çapraz kanal içeriği yerine kanala özel içeriği görürsünüz.

## <a name="additional-resources"></a>Ek kaynaklar

[İçerik ekleme yolları](add-manage-content.md)

[Sayfa modeli sözlüğü](page-elements-overview.md)

[Belge durumları ve yaşam döngüsü](document-states-overview.md)

[Yayımlama gruplarıyla çalışma](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
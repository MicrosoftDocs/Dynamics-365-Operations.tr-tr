---
title: Önceden ayarlanmış düzenlerle çalışma
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta önceden belirlenmiş düzenlerle nasıl çalışılacağı açıklanmaktadır.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 56ad992b6a9fd6fce09cadad70b8098acdc74ac0
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090857"
---
# <a name="work-with-preset-layouts"></a>Önceden ayarlanmış düzenlerle çalışma

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta önceden belirlenmiş düzenlerle nasıl çalışılacağı açıklanmaktadır.

Bu konudaki yordamları gerçekleştirmeden önce, [hazır ayar ve özel düzenleri](templates-layouts-overview.md#preset-and-custom-layouts) okuduğunuzdan emin olun. Genel genel bakış için, bkz. [Şablonlar ve düzenler genel bakış](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Yeni önceden ayarlanmış düzeni oluşturma

Önceden ayarlı düzen oluşturmak için iki yöntem vardır. Varolan bir özel düzeni yeni bir hazır ayar düzeni olarak kaydedebilir veya sıfırdan bir hazır ayar düzeni oluşturabilirsiniz.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Varolan özel düzenden önceden belirlenmiş düzen oluşturma

Varolan özel düzenden önceden belirlenmiş düzen oluşturmak için şu adımları izleyin.

1. Şu anda hazır ayar düzeni kullanmayan ve sitenizdeki diğer sayfalar için yeniden kullanmak istediğiniz bir modül yapısına sahip olan varolan sayfayı açın.
1. Sayfayı kullanıma almak için **Düzenle**'yi seçin.
1. **Yeni Düzen olarak kaydet**'i seçin. **Yeni düzen olarak Kaydet** iletişim kutusu görünür.
1. Önceden ayarlı düzen için bir ad ve açıklama girin. Girdiğiniz değerler, yerleşiminizde yeni sayfalar oluştururken veya bu yazarlardan diğerine geçiş yaparken diğer yazarlar tarafından gösterilir. Bu nedenle, sayfa yazarları için yararlı olacak değerleri girin.
1. **Tamam**'ı seçin.

Yeni sayfalar oluşturduğunuzda veya aynı şablon hiyerarşisindeki bir sayfa için farklı bir düzen seçtiğinizde, önceden ayarlanmış düzen artık kullanılabilir olacaktır.

> [!TIP]
> Belirli bir sayfanın önceden belirlenmiş bir yerleşime bağlı olup olmadığını hızlı şekilde görmek için, sayfalar liste görünümünde sayfayı seçin ve sağdaki Özellik bölmesinde Düzen meta verilerini inceleyin.

### <a name="create-a-new-preset-layout"></a>Yeni önceden ayarlanmış düzeni oluşturma

Sıfırdan önceden belirlenmiş düzen oluşturmak için şu adımları izleyin.

1. Soldaki gezinti bölmesinde **Düzenler** seçin.
1. **Yeni Düzen** seçin. **Yeni düzen** iletişim kutusu görünür.
1. Hazır ayar düzeniniz için kullanılacak şablonu seçin.
1. Önceden ayarlı düzen için bir ad ve açıklama girin. Girdiğiniz değerler, yerleşiminizde yeni sayfalar oluştururken veya bu yazarlardan diğerine geçiş yaparken diğer yazarlar tarafından gösterilir. Bu nedenle, sayfa yazarları için yararlı olacak değerleri girin.
1. Yeni hazır ayar düzenini oluşturmak ve düzen düzenleyicisini açmak için **Tamam**'ı seçin.
1. Düzen Düzenleyicisinde, sol taraftaki anahat ağacını ve sağdaki Özellik bölmesini kullanarak modülleri ekleyin ve konfigüre edin. (Bu işlem, şablon düzenleyicisinde bir şablon için modül ekleme ve konfigüre etme işlemine benzer.) Modüllerin yerleşimi ve tüm kilitli varsayılan ayarlar, bu önceden ayarlanmış düzeni kullanan tüm sayfalar için merkezi modül yapılandırmasına dönüşür.

## <a name="modify-a-preset-layout"></a>Önceden belirlenmiş yerleşimi değiştirme

Önceden belirlenmiş düzen değiştirmek için şu adımları izleyin.

1. Soldaki gezinti bölmesinde **Düzenler** seçin.
1. Düzen düzenleyicisinde, soldaki anahat ağacında, değiştirilecek modülü seçin. Ardından şu adımlardan birini izleyin:

    - Bir modülü üst öğenin içinde yukarı veya aşağı taşımak için üç nokta düğmesini (**...**) oluşturun ve **yukarı taşı** veya **aşağı taşı**'yı seçin.
    - Bir modülün varsayılan ayarlarını değiştirmek için, varsayılan değerleri girmek ve isteğe bağlı olarak bunları tüm aşağı akış sayfalarında kilitlemek için özellik bölmesini kullanın.
    - Konteyner modüllerine yeni modüller veya parçalar eklemek için üç nokta düğmesini seçin ve sonra **Modül ekle**'yi veya **Parça ekle**'yi seçin.
    - Bir modülü düzenden kaldırmak için, üç nokta düğmesini de seçin ve sonra **Sil**'i seçin.

## <a name="change-a-preset-layout-theme"></a>Hazır ayar düzen temasını değiştirme

Tipik bir uygulama, varsayılan temayı önceden belirlenmiş bir düzen kullanan tüm sayfalar için ayarlayacaktır.

Hazır ayar düzeninizi kullanan tüm alt sayfaların temasını ayarlamak veya değiştirmek için aşağıdaki adımları izleyin.

1. Düzen düzenleyicisinde, soldaki anahat ağacında, sayfa konteyner modülü seçin. (Bu modül genellikle ikinci düğümdür ve **varsayılan sayfa** olarak adlandırılır.)
1. Sağdaki özellik bölmesindeki **Tema** alanında bir tema seçin.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Hazır ayar düzenine kaydetme, iade etme, önizleme ve yayımlama

Hazır ayar düzeninizi kaydetmek ve iade etmek için aşağıdaki adımları izleyin.

1. Mizanpaj Düzenleyicisinin üst kısmında **Kaydet**'i seçin. Kaydedilen değişiklikler, bu akış yönündeki sayfaları iade edilene kadar etkilemez.
1. **Düzenlemeyi bitir**'i seçin. Değişiklikleriniz, aşağı akışlar için artık bulunabilir.

Değişikliklerinizin önizlemesine bakmak için, önceden ayarlanmış düzenini kullanan varolan bir sayfayı açın veya düzenden yeni bir sayfa oluşturun.

Değişiklik önceden belirlenmiş yerleşiminizde yapılan değişiklikleri önizledikten sonra, görünümü canlı sitenizde yayımlamak için aşağıdaki adımlardan birini izleyin:

1. **Düzenlere** gidin, düzeni seçin ve sonra **Yayınla**'yı seçin.
1. Düzen düzenleyicisini açmak için düzen açını ve ardından **Yayımla**'yı seçin.
1. Yayımlanmamış yerleşime başvuran bir sayfa yayımlayın. Düzen otomatik olarak yayımlanacak.

> [!WARNING]
> Önceden belirlenmiş mizanpajlara birden çok sayfa başvuruyor. Önceden belirlenmiş bir düzeni yayımladığınızda, birden çok sayfanın düzenini etkileyebilirsiniz.

## <a name="rename-a-preset-layout"></a>Önceden belirlenmiş yerleşimi yeniden adlandırma

Site oluşturucuda önceden belirlenmiş bir düzeni yeniden adlandırmak için bu adımları izleyin.

1. Sol gezinti bölmesinde **Düzenler**'i seçin.
1. Yeniden adlandırmak istediğiniz düzenin düzen adını seçin.
1. Düzeni düzenlemeye başlamak için **Düzenle**'yi seçin.
1. Düzen özellikleri bölmesinde, düzen adının yanındaki kalem simgesini seçin.
1. Düzen adını gerektiği gibi düzenleyin.
1. Ad değişikliğini onaylamak için onay işaretini seçin.
1. **Düzenlemeyi bitir**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Şablonlarla çalışma](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

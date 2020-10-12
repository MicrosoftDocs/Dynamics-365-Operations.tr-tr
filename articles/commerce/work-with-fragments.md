---
title: Parçalarla çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.
author: phinneyridge
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 671caf1feeb7ac9e7d5a166c5de12540ab9b9792
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818362"
---
# <a name="work-with-fragments"></a>Parçalarla çalışma 

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Parçalar, tüm sitenizde yeniden kullanılması gereken modül yapılandırmaları için merkezi bir yazma deneyimine olanak sağlar. Örneğin, üstbilgiler, altbilgiler ve başlıklar birçok sayfada paylaşıldıklarından, genellikle parçalar halinde yapılandırılır. Parçaları sitenizdeki diğer sayfalara eklenebilen minyatür Web sayfaları olarak düşünebilirsiniz. Parçaların kendi yaşam döngüsü vardır. Başka bir deyişle bunlar, yazma araçlarında bağımsız varlıklar olarak oluşturulur, başvurulur, güncellenir ve silinir.

Parçalar yapılandırıldıktan sonra, site yapınızda modüllerin kullanılabileceği her yerde kullanılabilirler. Parçalar sayfalarda, mizanpajlarda, şablonlarda ve diğer parçalarda başvurulabilir.

> [!NOTE]
> Parçalar, diğer parçaların içinde en fazla yedi düzeye kadar iç içe geçmiş olabilir.

Örneğin, sitemizde birçok sayfada dönemsel olay yükseltmek istiyorsanız, bir parça kullanabilirsiniz. Yeni parça oluşturma işlemindeki ilk adım, başlatmak istediğiniz modül türünü seçmektir. Bu örnekte, bir kahraman modülünden parça oluşturabilirsiniz.

> [!NOTE]
> Parçalar herhangi bir modül türünden oluşturulabilir.

Bundan sonra, hero parçacığını özel tanıtım içerikleriniz ile konfigüre edebilirsiniz. Ayrıca, bunu gereksinim duyduğunuz şekilde yerelleştirebilirsiniz. Yeni tek başına kahraman parçası daha sonra, siteniz genelinde önceden yapılandırılmış bir modül olarak tüketilebilir. Bunu şablonlara, belirli sayfalara veya kahramanı modüllerini içerebilecek diğer parçalara kolayca ekleyebilirsiniz.

Parçanın eklendiği tüm yerler, oluşturduğunuz Merkez kahraman parçasına yapılan referanslardır. Değişiklikleri parçalara yayımlarsanız, bu değişiklikler derhal site genelinde referans alınan tüm yerlere yansıtılır. Bu nedenle, parçalar bir sitede modül konfigürasyonlarını tekrar kullanmak ve merkezi olarak yönetmek için güçlü ve etkili bir yol sağlar. Bunları etkili şekilde kullanarak, size önemli ölçüde yükseltebilir ve Site içeriğiyle ilgili maliyeti azaltmaya yardımcı olabilirsiniz.

Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül konfigürasyonlarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.

![Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül konfigürasyonlarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Parça oluştur

Yeni bir parça oluşturabilir veya varolan bir modül konfigürasyonunu parça olarak kaydedebilirsiniz.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Varolan bir modül konfigürasyonunu parça olarak kaydet

Önceden yapılandırılmış bir modülü yeniden kullanılabilir parçaya dönüştürmek için aşağıdaki adımları izleyin.

1. Bir parçaya dönüştürmek istediğiniz modülü içeren sayfayı veya şablonu açın.
1. Sol taraftaki ana hat bölmesinde veya doğrudan ana tuvalden, önceden yapılandırılmış modülü seçin.
1. Ana hat bölmesinde veya tuval içinde seçili modülün araç çubuğunda modül adının yanındaki üç noktayı (**...**) seçin. 
1. **Sayfa Parçası Olarak Paylaş**'ı seçin. 
1. **Sayfa Parçası Olarak Kaydet** iletişim kutusunda, parça için bir ad girin.
1. Modül konfigürasyonunu diğer sayfalara eklenebilecek bir parça olarak kaydetmek için **Tamam**'ı seçin.

Aşağıdaki resimde bir modül yapılandırmasının bir parça olarak nasıl kaydedileceği gösterilmektedir.

![Bir modül yapılandırmasının parça olarak nasıl kaydedileceği ile ilgili bir ekran yakalama](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a>Yeni bir parça oluşturun.

Bir yeni parça oluşturmak için şu adımları izleyin.

1. Soldaki gezinti bölmesinde **Parçalar** seçin.
1. **Yeni Sayfa Parçası**'nı seçin. Kullanılabilen tüm modül türlerini gösteren bir iletişim kutusu görüntülenir. Daha önce belirtildiği gibi, parçalar herhangi bir modül türünden oluşturulabilir.
1. Parçanız için bir modül türü seçin.

Aşağıdaki resimde, yeni bir parçanın oluşturulacağı yer gösterilmiştir.

![Yeni parçanın oluşturulacağı yerin Ekran yakalaması](./media/fragment-nav-menu.png)

> [!TIP]
> Genel bir konteyner modülü türü seçerek parçanız daha sonra güncelleştirmeniz ve yapılandırmanız gerektiğinde en iyi esnekliği elde edebilirsiniz.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Sayfaya parça ekleme, kaldırma veya düzenleme

Aşağıdaki yordamlarda parçaların nasıl ekleneceği, kaldırılacağı ve düzenleneceği açıklanmaktadır.

### <a name="add-a-fragment"></a>Parça ekle

Bir sayfaya parça eklemek için bu adımları izleyin.

1. Soldaki ana hat bölmesinde veya doğrudan ana tuvalde, alt modüllerin eklenebileceği bir kapsayıcı veya yuva seçin.
1. Çevrimiçi bölmesinde kapsayıcının veya yuvanın adının yanındaki üç noktayı (**...**) seçin.  Alternatif olarak, ana tuvali kullanıyorsanız artı simgesini (**+**) seçin.  
1. **Parça Ekle**'yi seçin.

    ![Bir yuvaya veya kapsayıcıya varolan bir parçanın nasıl ekleneceği ile ilgili bir ekran yakalama](./media/add-fragment.png)
 
    > [!NOTE]
    > Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Parça Ekle** seçeneği kullanılamaz.
    
1. **Parça Ekle** iletişim kutusunda, eklenecek bir parça arayıp seçin. Listelenmiş parça listelenmezse, önce seçilen konteyner veya yuvanın desteklediği bir modül türünden bir parça oluşturmanız gerekebilir.
1. Seçili parça sayfanızdaki seçili konteynere veya yuvaya eklemek için istediğiniz parçayı seçin.

    ![Parça seçicinin kalıcı penceresindeki Ekran yakalaması](./media/fragment-picker.png)

> [!NOTE]
> Bir konteynerde veya bir yuvada izin verilen modüller, sayfa şablonu veya modüllerin kendi tanımları tarafından tanımlanır.

### <a name="remove-a-fragment"></a>Parça kaldırma

Sayfada yuva veya konteynerden parça kaldırmak için bu adımları izleyin.

1. Soldaki ana hat bölmesinde, kaldırılacak parçanın adının yanında üç nokta (**...**) düğmesini seçin ve çöp kutusu sembolünü seçin.  Alternatif olarak, parçayı tuval içinde seçebilir ve parçanın araç çubuğunda çöp kutusu sembolünü seçebilirsiniz.
1. Parçayı kaldırma isteğinizi onaylamanız istendiğinde, **tamam**'ı seçin.

> [!NOTE]
> Sayfadan bir parçayı kaldırdığınızda, yalnızca bu sayfadan gelen başvuruyu kaldırırsınız. Sitenizden parçayı **silmeyin**. Sitenizdeki parçaları silmek için, parça denetçisi Kullanıcı arabirimini (UI) kullanmanız gerekir. Bir sitedeki parçaları yalnızca herhangi bir sayfa, şablon veya başka parçalar tarafından başvurulmuyorsa silebilirsiniz.

### <a name="edit-a-fragment"></a>Parça Düzenle

Parçaları düzenlemek için, parça düzenleyici kullanıcı arabimirni kullanmalısınız. Bu kısıtlama tasarımdan kaynaklanır. Yazarların belirli bir sayfa için modülleri düzenleme işlemini, birçok sayfada paylaşılabilecek parça düzenleme işlemi ile karıştıradığından emin olmanıza yardımcı olur.

Bir parça düzenlemek için şu adımları izleyin.

1. Soldaki gezinti bölmesinde **Parçalar** seçin.
1. **Parçalar** altında düzenlenecek parçayı seçin.
1. Parçanın modül özelliklerini ve yapısını gereksinim duyduğunuz şekilde Düzenle. İşlem, düzenleme modüllerinin sayfa düzenleyici görünümde düzenlenmesi işlemine benzer.

Bir parçayı sayfada, şablonda veya üst parçada seçerek ve sağdaki Özellikler bölmesinde **parça Düzenle** 'yi seçerek düzenleyebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Şablonlarla çalışma](work-with-templates.md)

[Önceden ayarlanmış düzenlerle çalışma](work-with-layouts.md)

[Yayınlama gruplarıyla çalışma](publish-groups.md)

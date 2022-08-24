---
title: Parçalarla çalışma
description: Bu makale, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 785e6f847fd1645557060356926f2dda8da22ac1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268218"
---
# <a name="work-with-fragments"></a>Parçalarla çalışma 

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.

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

![Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül yapılandırmalarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Parça oluştur

Yeni bir parça oluşturabilir veya varolan bir modül konfigürasyonunu parça olarak kaydedebilirsiniz.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Varolan bir modül konfigürasyonunu parça olarak kaydet

Önceden yapılandırılmış bir modülü Commerce site oluşturucuda yeniden kullanılabilir parçaya dönüştürmek için aşağıdaki adımları izleyin.

1. Bir parçaya dönüştürmek istediğiniz modülü içeren sayfayı veya şablonu açın.
1. Sol taraftaki ana hat bölmesinde veya doğrudan görsel sayfa oluşturucuda, önceden yapılandırılmış modülü seçin.
1. Ana hat bölmesinde veya görsel sayfa oluşturucuda seçili modülün araç çubuğunda modül adının yanındaki üç noktayı (**...**) seçin. 
1. **Parça olarak Paylaş**'ı seçin. 
1. **Parça Olarak Kaydet** iletişim kutusunda, parça için bir ad girin.
1. Modül konfigürasyonunu diğer sayfalara eklenebilecek bir parça olarak kaydetmek için **Tamam**'ı seçin.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Yeni parça oluştur

Commerce site oluşturucuda yeni parça oluşturmak için aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Parçalar** seçin.
1. **Yeni**'yi seçin. Kullanılabilen tüm modül türlerini gösteren bir **yeni parça** iletişim kutusu görüntülenir. Daha önce belirtildiği gibi, parçalar herhangi bir modül türünden oluşturulabilir.
1. Parçanız için bir modül türü seçin.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Genel bir konteyner modülü türü seçerek parçanız daha sonra güncelleştirmeniz ve yapılandırmanız gerektiğinde en iyi esnekliği elde edebilirsiniz.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Sayfaya parça ekleme, kaldırma veya düzenleme

Aşağıdaki yordamlarda parçaların nasıl ekleneceği, kaldırılacağı ve düzenleneceği açıklanmaktadır.

### <a name="add-a-fragment"></a>Parça ekle

Commerce site oluşturucuda bir sayfaya parça eklemek için aşağıdaki adımları izleyin.

1. Soldaki ana hat bölmesinde veya doğrudan görsel sayfa oluşturucuda, alt modüllerin eklenebileceği bir kapsayıcı veya yuva seçin.
1. Kapsayıcının veya yuvanın adının yanındaki üç noktayı (**...**) seçin.  Alternatif olarak, görsel sayfa oluşturucuyu kullanıyorsanız artı simgesini (**+**) seçin.  
1. **Parça Ekle**'yi seçin.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Parça Ekle** seçeneği kullanılamaz.
    
1. **Parça Seç** iletişim kutusunda, eklenecek bir parça arayıp seçin. Listelenmiş parça listelenmezse, önce seçilen konteyner veya yuvanın desteklediği bir modül türünden bir parça oluşturmanız gerekebilir.
1. Seçili parça sayfanızdaki seçili konteynere veya yuvaya eklemek için istediğiniz parçayı seçin.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> Bir konteynerde veya bir yuvada izin verilen modüller, sayfa şablonu veya modüllerin kendi tanımları tarafından tanımlanır.

### <a name="remove-a-fragment"></a>Parça kaldırma

Commerce site oluşturucuda bir sayfadaki bir yuva veya kapsayıcıdan parça kaldırmak için aşağıdaki adımları izleyin.

1. Soldaki ana hat bölmesinde, kaldırılacak parçanın adının yanında üç nokta (**...**) düğmesini seçin ve çöp kutusu sembolünü seçin.  Alternatif olarak, parçayı görsel sayfa oluşturucu içinde seçebilir ve parçanın araç çubuğunda çöp kutusu sembolünü seçebilirsiniz.
1. Parçayı kaldırma isteğinizi onaylamanız istendiğinde, **tamam**'ı seçin.

> [!NOTE]
> Sayfadan bir parçayı kaldırdığınızda, yalnızca bu sayfadan gelen başvuruyu kaldırırsınız. Sitenizden parçayı **silmeyin**. Sitenizdeki parçaları silmek için, parça denetçisi Kullanıcı arabirimini (UI) kullanmanız gerekir. Bir sitedeki parçaları yalnızca herhangi bir sayfa, şablon veya başka parçalar tarafından başvurulmuyorsa silebilirsiniz.

### <a name="edit-a-fragment"></a>Parça Düzenle

Parçaları düzenlemek için, parça düzenleyici kullanıcı arabimirni kullanmalısınız. Bu kısıtlama tasarımdan kaynaklanır. Yazarların belirli bir sayfa için modülleri düzenleme işlemini, birçok sayfada paylaşılabilecek parça düzenleme işlemi ile karıştıradığından emin olmanıza yardımcı olur.

Commerce site oluşturucuda bir parçayı düzenlemek için aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Parçalar** seçin.
1. **Parçalar** altında düzenlenecek parçayı seçin.
1. Parçanın modül özelliklerini ve yapısını gereksinim duyduğunuz şekilde Düzenle. İşlem, düzenleme modüllerinin sayfa düzenleyici görünümde düzenlenmesi işlemine benzer.

Bir parçayı sayfada, şablonda veya üst parçada seçerek ve sağdaki Özellikler bölmesinde **parça Düzenle** 'yi seçerek düzenleyebilirsiniz.

### <a name="rename-a-fragment"></a>Parçaları yeniden adlandırma

Site oluşturucuda bir parçayı yeniden adlandırmak için şu adımları izleyin.

1. Soldaki gezinti bölmesinde, **Parçalar**'ı seçin.
1. Yeniden adlandırmak istediğiniz parçanın parça adını seçin.
1. Parçayı düzenlemeye başlamak için **Düzenle**'yi seçin. Parça zaten başka bir kişi tarafından düzenlenmişse parçayı düzenleyemeyeceğinizi unutmayın.
1. Parça özellikleri bölmesinde, parça adının yanındaki kalem simgesini seçin.
1. Parça adını gerektiği gibi düzenleyin.
1. Ad değişikliğini onaylamak için onay işaretini seçin.
1. **Düzenlemeyi bitir**'i seçin.

Daha sonra, bir parçayı oluşturulduktan sonra düzenleyerek ve ardından özellik bölmesinde parça adının yanındaki kalem simgesini seçerek yeniden adlandırabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Şablonlarla çalışma](work-with-templates.md)

[Önceden ayarlanmış düzenlerle çalışma](work-with-layouts.md)

[Yayımlama gruplarıyla çalışma](publish-groups.md)

[Sayfaları ve parçaları geri döndürmek için sürüm geçmişini görüntüleme](version-history-revert.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

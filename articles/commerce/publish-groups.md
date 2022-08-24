---
title: Yayımlama gruplarıyla çalışma
description: Bu makalede, Microsoft Dynamics 365 Commerce'ta grup yayımlama özelliği açıklanmaktadır.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 5a19d25b0b34ea3d452cacdd51ea071747ff1d90
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279018"
---
# <a name="work-with-publish-groups"></a>Yayımlama gruplarıyla çalışma

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'ta grup yayımlama özelliği açıklanmaktadır.

E-ticaret Web siteleri yıl boyunca yeni içerikle sürekli güncelleştirilir. Güncelleştirmeler sıklıkla tatiller, mevsimsel pazarlama kampanyaları veya promosyon tarafından başlatılır gibi e-ticaret olaylarının çevresinde toplu olarak yayımlanır. Bu güncelleştirmeler genellikle, Web sitesi içeriği gruplarının (örnekler, sayfalar, resimler, parçalar ve şablonlar) tek bir eylemde aynı anda hazırlanabilsin, doğrulanmalıdır ve yayımlanmaktadır.

Öğeleri, her kümenin kendi yaşam döngüsü olduğu, öğeleri birlikte yayımlayan mantıksal kümeler halinde gruplandırma yeteneği, site yazarlarına birçok avantaj sağlar. Commerce'da bu mantıksal kümeler, yayınlama grupları olarak bilinir. Bunlar, site yazarlarının, kendi yapılandırılabilir, test edilebilir ve yayımlanabilir varlıkları olarak güncelleştirme kümelerini izlemesine olanak tanır.

Yazarlar, canlı siteyi veya diğer kendi kendini içeren yayınlama gruplarını etkilemeden, aşamalı bir yayınlama grubundaki güncelleştirmelerin önizlemesini yapabilir. Böylece yazarlar, yayınlama grubundaki tüm öğeleri canlı siteye eşzamanlı olarak yayımlamak için yayınlama eylemini zamanlayabilir. Olay tabanlı site güncelleştirme kilometre taşları etrafında önemli miktarda yıllık gelir oluşturan kurumsal düzey şirketler için güncelleştirmeleri gruplandırma, önizleme ve zamanlama yeteneği çok önemlidir.

Şirketler yavaş veya geçersiz kılınan içerik dağıtımları için maliyetler alabilir. Yayınlama grupları, başlatan, zaman içinde düzenlenen, doğrulanan ve yayımlanan garantiye yardımcı olur. Bunların büyük veya küçük olup olmadığı, yayınlama grupları yazarların devam eden site güncelleştirme görevlerini düzenlemesine ve basitleştirmesine yardımcı olan değerli bir araç takımı sağlar.

## <a name="when-to-use-publish-groups"></a>Yayınlama grupları ne zaman kullanılır

Birden çok belgeyi birlikte hazırlamak ve yayınlamak gerektiğinde, yayınlama gruplarını kullanabilirsiniz. Örneğin, Web sitenizde her mevsimi bir içerik güncelleştirilebileceği takdirde, bu mevsimlik pazarlama hareketleri için yayınlama grupları oluşturabilirsiniz. "Sonbahar mevsimlik güncelleştirmesi" yayın grubu, yeni mevsimlik görüntüler, mevsimlik pazarlama iletileri bulunan parçalar, mevsimsel ürün koleksiyonları içeren sayfalar veya diğer Web sitesi güncelleştirmeleri içerebilir.

Yayınlama gruplarının avantajı, çoklu güncelleştirmeleri paralel olarak aşamalayabilmeniz olabilir. Örneğin, "sonbahar mevsimsel güncelleştirme" yayınlama grubuna ait güncelleştirmeden hemen sonra, belirli bir tatil hafta sonu için içerik güncelleştirmesi olabilir. Bu durumda, sonraki "sonbahar tatil güncelleştirmesi" yayım grubu için içeriği aşamalı olarak, "sonbahar mevsimsel güncelleştirmesi" yayın grubu içeriğini sahne alanı 'nda oluşturabilirsiniz. Her yayın grubu kendi benzersiz sayfa, resim, parçacık, şablon ve benzer kümesini içerir. Bu iki yayınlama grubunu bağımsız olarak, ancak eşzamanlı bir zaman çizelgesinde sahne edebilir, önizleyebilir ve doğrulayabilirsiniz. Böylece, her bir yayınlama grubu sitenizde belirli tarih ve saatlerde canlı duruma geçmek için zamanlanabilir.

## <a name="turn-on-the-publish-groups-feature"></a>Grup yayımlama özelliğini açın

Yayınlama grupları özelliği isteğe bağlıdır ve siteniz için kapatılmalıdır.

Commerce geliştirme araçlarında sitenizin grup yayımlama özelliğini etkinleştirmek için, aşağıdaki adımları izleyin.

1. Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.
1. **Site ayarları** altında **Özellikler** dosyasını seçin.
1. **Yayın grupları** seçeneğini **açık** olarak ayarlayın.

## <a name="create-a-publish-group"></a>Yayın grubu oluşturun

Commerce geliştirme araçlarında sitenizin yayın grup özelliğini oluşturmak için, aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Yayın Grupları**'nı seçin.
1. Komut çubuğunda **yeni** seçin.
1. **Yayınlama grubu oluştur** iletişim kutusunda, **Yayın Grup adı** altında açıklayıcı bir ad girin. Daha sonra **Tamam**'ı seçin.

## <a name="set-the-publish-group-authoring-context"></a>Yayınlama grubu yazma bağlamını ayarla

Commerce'te, varsayılan yazma içeriği canlı site bağlamındadır. Canlı site yazma bağlamı, yayınlama grubu kullanmadan web sitenize doğrudan görüntüleyebileceğiniz ve bunlar üzerinde değişiklik yapabileceğiniz varsayılan görünümdür. Bu, sitenizin yayınlanmış sürümünde en son doğrudan güncelleştirmeleri temsil eder. Sol gezinti bölmesinde, **yayınlama grupları** 'nın altındaki içerik denetimi **canlı site** adını gösteriyorsa, canlı site yazma bağlamında çalışıyorsunuz demektir. **Canlı site**, bağlam denetiminin varsayılan adıdır. Aksi durumda, bağlam denetimi bir yayınlama grubunun adını gösterir.

Bir yayınlama grubunda çalışmak için, bunun için yayınlama grubu yazma bağlamına geçmeniz gerekir. Yayınlama grubu bağlamını ayarlamak için aşağıdaki adımlardan birini izleyin.

- Sol gezinti bölmesinde, doğrudan **yayınlama grupları** altında bağlam denetimini seçin ve sonra görünen seçenekler listesinden yayınlama grubunun adını seçin. Bağlam denetimi yeniden adlandırılır ve bir yayınlama grubunun adını gösterir.
- Sol gezinti bölmesinde, **Yayın grupları**'nı seçin ve sonra **Yayın gruplar**'ı altında, yayınlama grubunun adını seçin. Bağlam denetimi yeniden adlandırılır ve bir yayınlama grubunun adını gösterir.

Yayınlama grubu yazma içeriğinizi ayarladıktan sonra, site içeriğini önizlerken ve düzenlerken o yayımlama grubu bağlamında çalışıyorsunuz demektir.

Varsayılan canlı site yazma bağlamına dönmek için içerik denetimini seçin ve sonra **Canlı site**'ı seçin.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Yayın grubuna sayfalar veya başka öğeler ekleme

Bir yayın grubu yazma bağlamını seçtikten sonra sol gezinti bölmesindeki içerik denetimi adını gösterir, içeriği varsayılan canlı site bağlamında olduğu gibi oluşturabilirsiniz. Ayrıca, varolan sayfaları veya diğer öğeleri başka yayınlama gruplarından veya canlı site bağlamından ekleyebilirsiniz.

Varolan sayfaları bir yayınlama grubuna kopyalamak için aşağıdaki adımları izleyin.

1. Kopyalamanın kaynağı olan yazma bağlamını seçin ve sonra sol gezinti bölmesinde **sayfalar**'ı seçin.
1. Bir yayınlama grubuna eklenecek sayfayı seçin.
1. Komut çubuğunda **yayınlama grubuna Kopyala**'yı seçin.
1. **Bir yayınlama grubu Seç** iletişim kutusunda sayfayı eklemek için yayınlama grubunu seçin ve **Tamam**'ı seçin.

Özelleştirilmiş ürün sayfaları, URL'ler, şablonlar, düzenler, parçalar ve ortam kitaplığı varlıkları oluşturmak ya da bu türlerin varolan öğelerini bir yayınlama grubuna eklemek için aynı temel adımları kullanabilirsiniz.

## <a name="validate-a-publish-group"></a>Yayın grubu doğrulayın

Yayın grubu içeriğindeki tüm bağımlılıkların karşılanması ve tüm doğrulamaların geçirildiğinden emin olmak için, bir yayınlama eylemini zamanlamadan önce ele geçirilmesi gereken herhangi bir sorunu tanımlamak üzere doğrulamayı çalıştırabilirsiniz.

Zamanlamadan önce yayın grubunu doğrulamak için aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Yayın Grupları**'nı seçin.
1. Doğrulanacak yayın grubu seçin.
1. Komut çubuğunda **Doğrula** seçin.

Doğrulama, yayınlama grubundaki tüm içerikte çalıştırılır. Başarılı bir yayımlama eyleminin önlenmesi ile ilgili tüm sorunlar, sağ üst tarafta görünen bir bildirim kutusunda görüntülenir.

> [!NOTE]
> Doğrulama, her zaman bir yayınlama grubu zamanlandığı zaman otomatik olarak çalıştırılır. Ancak, bir yayınlama grubunu canlı çalışmaya başlamadan önce düzeltmeniz gereken sorunları tanımlamada yardımcı olduğundan, Komut çubuğundaki **Doğrula** düğmesi kullanışlıdır.

## <a name="schedule-a-publish-group-to-go-live"></a>Yayımlama grubunun yayınlanmasını zamanlama

Bir yayınlama grubunun sitenizde etkin olacak şekilde zamanlamak için, aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Yayın Grupları**'nı seçin.
1. **Yayın Grubu** altında, zamanlanacak yayınlama grubunu seçin.
1. Komut çubuğunda **Zamanlayı düzenle** seçin. **Zamanlama düzenle** iletişim kutusu görünür.
1. Yayınlama grubunuzun etkin olması gereken tarih ve saati seçin ve **Tamam**'ı seçin.

Bir yayınlama grubunu zamanlamayı iptal etmek için, aynı adımları uygulayın, ancak **zamanlamayı düzenle** iletişim kutusunda **yayınlama grubunu zamanla**'yı seçin.

> [!NOTE]
> Çok büyük yayın gruplarının, planlanan zamanı geldiğinde bir dakika veya iki kez yayımlanması gerekebilir. Bir yayınlama eyleminin anlık olmadığından ve daha küçük yayınlama gruplarının daha hızlı yayımlanabileceğini unutmayın.

## <a name="publish-groups-faq"></a>Yayınlama grubu SSS

**Bir yayımlama grubunda kaç öğe olabilir?**

Şimdilik, her bir yayınlama grubu için 2.000 madde sınırı vardır. Çok büyük yayın gruplarının, planlanan zamanı geldiğinde yayımlanmasının birkaç dakika sürebileceğini unutmayın.

**Yazılım geliştirme terminolojisinde kod "branşlar" gibi yayınlama grupları mı?**

Evet ve hayır. Yayınlama grupları, sitenizin çatallanmış sürümleri olarak düşünülebilir. Bu şekilde, dallar gibi davranırlar. Ancak, bağımsız öğeler düzeyinde birleştirme kavramı yoktur. Son yayımlanan madde yalnızca daha önceden var olan öğeleri geçersiz kılar ve en son yayımlama eylemi önceki yayımlama eylemlerinin her zaman yerini alır.

**Aynı anda canlı çalışmak için iki yayınlama grubunu zamanlayabilir miyim?**

Hayır. Performans ve çakışma nedenleriyle, sistem, zamanlanan yayımlama gruplarını en az beş dakika ayrı olacak şekilde şaşırtmanızı zorlayacaktır.

**İndirimler ve ürün güncelleştirmeleri gibi çok yönlü arka ofis öğelerini planlamak için yayınlama grupları kullanabilir miyim?**

Şu anda, yayınlama grupları özelliği yalnızca Web sitesi içeriğini destekler. Ancak Microsoft, arka ofis alım satım senaryoları ile tümleştirmenin, çok yönlü kanal kampanyası düzenleme ve otomasyonu için yararlı olabileceğini bilmektedir.

## <a name="additional-resources"></a>Ek kaynaklar

[İçerik ekleme yolları](add-manage-content.md)

[Sayfa modeli sözlüğü](page-elements-overview.md)

[Belge durumları ve yaşam döngüsü](document-states-overview.md)

[Kanallar arası paylaşımı etkinleştirme ve kullanma](cross-channel-sharing.md)

[Modüllerle çalışma](work-with-modules.md)

[Parçalarla çalışma](work-with-fragments.md)

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Site gezintisini özelleştirme](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

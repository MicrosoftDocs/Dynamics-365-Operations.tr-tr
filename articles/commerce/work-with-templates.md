---
title: Şablonlarla çalışma
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta şablonlarla nasıl çalışılacağı açıklanmaktadır.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a3fc4259a76f6edcfaa0b8f6e08292477c6c0835
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416439"
---
# <a name="work-with-templates"></a>Şablonlarla çalışma


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta şablonlarla nasıl çalışılacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

[Şablonlar ve mizanpajlarda genel bakış](templates-layouts-overview.md) anlatıldığıgibi, Özet Akış yazarları için kullanılabilen seçenekler kümesini tanımlar. Şablonlar, birkaç nedenden dolayı kuruluşun Web yazma ekibi için yararlıdır ve iyi yapılandırılmış Şablonlar aşağıdaki hedeflerin tümü için yardımcı olabilir:

- Günlük İçerik Düzenleyici rolleri için geliştirme deneyimini basitleştirin.

    - Filtre modülü seçenekleri için belirli bir sayfa bölümü için yalnızca ilgili modüller gösterilir. (Örneğin, bir şablonun pazarlama bölümü, bu bağlamda asla kullanılmamalıdır ve gösterildiklerinde içerik yazma görevlerini karmaşıklaşmaya yetecek ilgisiz modülleri filtrelemek için yapılandırılabilir.)
    - Geliştirme verimliliğini artırmaya yardımcı olmak için varsayılan modül ayarını konfigüre edin.
    - Geliştirme verimliliğini artırmaya yardımcı olmak için varsayılan sayfa parçalarını tanımlayın. (Örneğin, şablondaki üstbilgi ve altbilgi parçaları otomatik olarak her bir aşağı akış sayfasında görünür.)

- Onaylı bir modül düzenleme ve konfigürasyon seçenekleri kümesi tanımlayarak kurumsal siteler marka üzerinde tutun.

    > [!TIP] 
    > Başarılı e-ticaret siteleri müşterilere tanıdık, yinelenebilir ve marka ile Kullanıcı deneyimi (UX) tasarım desenleri sağlar. Şablon kullanarak, siteniz arasındaki tutarlılığı denetlemenize yardımcı olursunuz.

- Yinelenebilir ve programlı olarak tanımlanmış sayfa tanımlarını ve meta verileri sağlayarak arama motoru iyileştirme (SEO) puanlarını geliştirin.

> [!NOTE]
> Şablonlar bir site içindeki tutarlılığı denetlemek üzere tasarlansa da, teorik olarak, herhangi bir tutarlılığı zorlayabilmeleri için kendilerine göre konfigüre edilebilir. Marka ve site yöneticileri, siteleri üzerindeki sayfalar için herhangi bir çeşitliğin düzeyini tanımlayabilir. Örneğin, bir şablon tamamen açık bırakılabilir, böylece içerik yazarları istedikleri sayfa tasarımını oluşturabilirler. Bu durumda, yukarıdaki listede bulunan avantajlardan hiçbiri uygulanamaz.

## <a name="modify-a-template"></a>Şablonu değiştirin

Şablonlar, Şablon Düzenleyicisi kullanılarak değiştirilir.

Şablon düzenleyicisini açmak için aşağıdaki adımlardan birini izleyin:

- Sitenizin gezinti bölmesinde, **şablonlar**'ı seçin ve sonra değiştirilecek şablonu seçin.
- Varolan bir sayfanın sayfa düzenleyicisinde, soldaki anahat ağacında en üst düğümü seçin. Ardından sağdaki özellikler bölmesinde, **Şablon düzenle** seçin.

Soldaki anahat ağacı görünümünde alt düzenler ve sayfalar için kullanılabilen modül seçenekleri ve yapıları gösterilir. Anahat ağacında bir modül seçtiğinizde, sağ tarafta bulunan Özellik bölmesinde seçilen modülün şablon özelliklerini görüntüleyebilirsiniz. Bu özelliklerden bazıları şablon düzenlemede benzersizdir. Aşağıdaki tablo bu özellikleri açıklar.

| Özellik adı | Tanım |
|---|---|
| Minimum Gerçekleşme | Bu özellik, seçili modül için minimum oluşum sayısını tanımlar. Örneğin değer **1** olarak ayarlanırsa, bir değer **0** (sıfır) olarak ayarlandığında modül isteğe bağlı olduğu halde, akış yönündeki yazarlar için gereklidir. |
| Maksimum Gerçekleşme | Bu özellik, seçili modül için maksimum oluşum sayısını tanımlar. Örneğin, değer **1** olarak ayarlanırsa modül yalnızca bir kez eklenebilir. |
| Min. Modüller (Konteynerler) | Başka modüller içeren modüller (*konteyner modülleri* için), bu özellik alt öğe olarak eklenmesi gereken en az toplam modül sayısını tanımlar. Örneğin, bir döngü modülü için, değer 1'den büyük bir sayıya ayarlanmış olabilir. |
| Maks. Modüller (Konteynerler) | Konteyner modüller için, bu özellik alt öğe olarak eklenmesi gereken en fazla toplam modül sayısını tanımlar. Örneğin, bir döngü modülü için, değer 10'dan küçük bir sayıya ayarlanmış olabilir. |
| Kilitli | Tüm çekirdek modül özelliklerinin yanında **kilitli** bir Boole denetimi görünür. Şablondaki bir modül ayarını şablon yazarının kilitlemesine olanak tanır. Kilitli olan bir modül ayarı alt düzen veya sayfalar tarafından geçersiz kılınamaz. Bu şablon kullanan tüm mizanpajlar ve sayfalar için merkezi olarak düzenlenebilir bir özellik değeri haline gelir. |

## <a name="create-a-new-template"></a>Yeni şablon oluştur

Bir yeni şablon oluşturmak için şu adımları izleyin.

1. Sitenizin gezinti bölmesinde, şablon denetim görünümünü açmak için **şablonlar**'ı seçin.
1. **Yeni Şablon** seçin.
1. Şablon oluşturma iletişim kutusunda şablon için ad ve açıklama girin. Girdiğiniz değerler, yeni sayfalar oluşturduklarında yazarlara gösterilir. Bu nedenle, sayfa yazarları için yararlı olacak meta verileri girin. Örneğin, açıklama olarak **genel pazarlama sayfaları oluşturmak için bu şablonu kullanın** girin. Bu meta veriler daha sonra düzenlenebilir.
1. Yen şablon düzenini oluşturmak ve şablon düzenleyicisini açmak için **Tamam**'ı seçin. Şablon Düzenleyicisi solda bir anahat ağacı ve sağdaki bir özellik bölmesi gösterir.
1. Anahat ağacında, düğümleri genişletin ve **HTML Başı** yuvasını seçin.
1. Bu yuvada henüz herhangi bir modül yoksa, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Varsayılan sayfa özeti**'ni seçin ve **Tamam**'ı seçin.
1. Anahat ağacında yeni modülü seçin ve Özellik bölmesinde, şablondaki tüm alt sayfalar için otomatik olarak konfigüre edilecek tüm varsayılan ayarları girin. Herhangi bir varsayılan ayar istemiyorsanız, değerleri boş bırakın.
1. Anahat ağacında **Gövde** yuvasını seçin, üç nokta düğmesini ve sonra **Modül ekle**'yi seçin.
1. Bir sayfa konteyner modülü seçin (yalnızca bir seçenek olabilir) ve sonra **Tamam**'ı seçin.

Yeni sayfa konteyner modülünün altında yeni bir yuvalar kümesi(**başlık**, **ana** vb.) göreceksiniz. Burada, bu şablondan sayfa oluştururken yazarların kullanabildiği modül seçeneklerini ekleyebilir ve konfigüre edebilirsiniz. Varsayılan olarak, bir yuvaya modül eklmezseniz, kullanılabilen tüm modül türleri o yuva için desteklenir.

Şablon artık teknik olarak geçerlidir ve yeni sayfalar oluşturmak için kaydedilebilir, teslim edilebilir ve kullanılabilir. Ancak, sonraki üç bölüm, ilk olarak konfigüre etmek isteyebileceğiniz bazı diğer varsayılan ayarları açıklar.

## <a name="add-a-header-and-a-footer"></a>Üst bilgi ve alt bilgi ekle

Sitenizde zaten bir başlık parçası varsa, bir şablona üstbilgi ve altbilgi eklemek için aşağıdaki adımları izleyin.

1. Anahat ağacında, **gövde** yuvasını ve bunun alt sayfa modülünü genişletin.
1. **Üstbilgi** yuvasını seçin.
1. **Başlık** yuvası için üç nokta düğmesini seçin ve **Parça Ekle**'yi seçin.
1. Sitenizin başlık parçasını arayıp seçin ve **Tamam**'ı seçin.

Şablonu kullanan tüm sayfalar şimdi bu başlık parçasını otomatik olarak devralacaktır.

Sitenizde henüz bir başlık parçası yoksa nasıl oluşturulacağı hakkında bilgi için [parça oluşturma](work-with-fragments.md#create-a-fragment)'ya bakın ve önceki yordamı tamamlayın.

## <a name="change-the-template-theme"></a>Şablon temasını değiştirin

Şablon kullanan tüm sayfalar için varsayılan temayı ayarlamak üzere aşağıdaki adımları izleyin.

1. Soldaki anahat ağacında **Gövde** yuvayı genişletin.
1. **Gövde** yuvasında sayfa konteyner modülünü seçin (örneğin, **Varsayılan sayfa**).
1. Sağdaki özellik bölmesinde, **Tema** alanında bir tema seçin.

Varsayılan olarak tüm yeni sayfalar artık seçili temayı kullanır. Sayfaların, düzen veya sayfa düzeyinde bu ayarı geçersiz kılmasını önlemek için **kilitli** Boolean kontrolünü **doğru** olarak ayarlayın.

## <a name="add-a-script-to-a-template"></a>Şablona komut dosyası ekleme

Şablonunuza JavaScript içeren HTML **&lt;kod&gt;** öğeleri ekleyebilirsiniz. Bu şekilde, sayfalarınızın HTML kafasını, gövdesine başlaması ve gövde bitiş bölümlerine varsayılan kod davranışları sağlayabilirsiniz.

Bir şablona komut eklemek için bu adımları izleyin.

1. Soldaki anahat ağacında, **&lt;komut dosyası&gt;** öğesini eklemek istediğiniz yuvayı seçin (ör., HTML başlığı, gövde başlangıcı veya gövde sonu).
1. Ana yuvası için üç nokta düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda bir kod modülü (örneğin, **harici komut dosyası** veya **satır içi komut dosyası**) seçin.
1. Sağdaki Özellik bölmesinde, uygun komut dosyası Özellik denetiminde (örneğin, **satır içi kod** veya **komut dosyası etiketleri**), kodunuzu girin.
1. Özellik bölmesinde, konfigüre etmek istediğiniz diğer tüm isteğe bağlı ayarları girin.

> [!TIP]
> Diğer şablonlar için herhangi bir komut dosyası modüllerinizi tekrar kullanmak istiyorsanız, onları parçalara dönüştürebilirsiniz. Bu şekilde, geliştirme sürecini daha etkili hale getirmek ve güncelleştirme işlemini merkezileştirmenizi sağlar. Bir kod modülünü bir parçaya dönüştürme hakkında bilgi için, bkz. [Mevcut modül yapılandırmasını parça olarak kaydet](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Şablona kaydetme, iade etme, önizleme ve yayımlama

Şablon kaydetmek ve iade etmek için aşağıdaki adımları izleyin.

1. Şablon Düzenleyicisinin üst kısmında **Kaydet**'i seçin. Kaydedilen değişiklikler, bu akış yönündeki sayfaları iade edilene kadar etkilemez.
1. **Düzenlemeyi bitir**'i seçin. Değişiklikleriniz, aşağı akışlar için artık bulunabilir.

Değişikliklerinizin önizlemesine bakmak için, şablon kullanan varolan bir sayfayı açın veya şablondan yeni bir sayfa oluşturun.

Değişiklik şablonda yapılan değişiklikleri önizledikten sonra, şablonu canlı sitenizde yayımlamak için aşağıdaki adımlardan birini izleyin:

* **Şablonlara** gidin, şablonu seçin ve sonra **Yayınla**'yı seçin.
* Düzen düzenleyicisini açmak için düzen açını ve ardından **Yayımla**'yı seçin.
* Yayımlanmamış şablona başvuran bir sayfa yayımlayın. Şablon otomatik olarak yayımlanır.

> [!WARNING]
> Bir şablon veya herhangi bir başka içerik yönetimi sistemi (CMS) öğesi yayımlandığında, bunlar internette bulunabilir. Belgeleri veya varlıkları ortak kullanıma hazır oluncaya kadar yayımlamayın. Kaydedilen ve iade edilmiş, ancak yayınlanmamış olan belge sürümleri yalnızca kimliği doğrulanmış sistem kullanıcıları tarafından keşfedilebilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Önceden ayarlanmış düzenlerle çalışma](work-with-layouts.md)

---
title: Dynamics 365 Commerce e-ticaret yerelleştirme kılavuzu
description: Bu makale, bir Microsoft Dynamics 365 Commerce e-ticaret sitesinin ek dillere nasıl yerelleştirileceğini ve siteyi çoklu kanalları destekleyecek şekilde konfigüre etme konusunu açıklamaktadır.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 955a85340f6d35f1e203d74920d07b5dc6ff8654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873396"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commerce e-ticaret yerelleştirme kılavuzu

[!include [banner](includes/banner.md)]

Bu makale, bir Microsoft Dynamics 365 Commerce e-ticaret sitesinin ek dillere nasıl yerelleştirileceğini ve siteyi çoklu kanalları destekleyecek şekilde nasıl yapılandırılacağını açıklar ve işlemle ilgili kavramları ve terminolojiyi kapsar.

Dynamics 365 Commerce'deki e-ticaret özellikleri, belirli ülkeler ve dillerle ilgili olabilecek çevrimiçi deneyimlere olanak verecek, ancak şablonların, sayfaların, içeriğin ve ortamların en fazla yeniden kullanılmasına olanak veren şekilde tasarlanmıştır. Ayrıca, temel bir site oluşturabilir ve daha sonra zaman içinde ek ülkeler ve diller için destek ekleyerek yeni pazarlara genişletebilirsiniz.

## <a name="definitions"></a>Tanımlar

**Yerel ayar, yerel ayar tanımlayıcısı**: Yerel ayar (yerel ayar tanımlayıcısı olarak da bilinir) bir ülke veya bölgeyle ilişkilendirilmiş dili tanımlar. Örneğin, "fr-ca" yerel ayar tanımlayıcısı, Kanada Fransızcası ile ilişkilendirilir.

**Temel dil**: Sitenizin içeriğini yerelleştirme için vermeden önce üzerinde geliştirdiğiniz dil.

**Kanal, çevrimiçi mağaza**: Bir kanal (çevrimiçi mağaza olarak da bilinir) bir çevrimiçi e-ticaret vitrini için ödeme yöntemleri, fiyat grupları, ürün hiyerarşileri, sınıflamalar ve ürünler tanımlar.

## <a name="concepts"></a>Kavramlar

### <a name="url-driven-experience"></a>URL tabanlı deneyim

Dynamics 365 Commerce e-ticaret siteleri, kanallar ve yerel ayar tanımlayıcıları üzerinden müşteriler için benzersiz pazarlarla yerelleştirilmiş deneyimler sunar. Kanallar, bir pazar için benzersiz ürünleri, kategorileri, para birimlerini ve ödeme yöntemlerini tanımlar ve yerel ayar tanımlayıcıları, müşterilerin görmesini sağlayan içeriğin dilini belirler. Bir e-ticaret sitesi, pazarlaştırılmış ve yerelleştirilmiş deneyimler arasında ayrım yapmak için URL kullanır. Bu benzersiz kanal ve bölgesel deneyimler için site URL'Leri, Site Oluşturucu'daki **Site ayarları \> Kanallar** sayfasında Dynamics 365 Commerce site oluşturucu için tanımlanmıştır.

Site oluşturucuda bir URL, bir etki alanı birleşimidir ve bir kanalın ve bir yerel ayar için giriş noktasını tanımlayan bir yoldur. Aşağıdaki örnekte, Fabrikam Inc. adlı kurgusal bir çevrimiçi mağaza. bir kanalın ve yerel ayarın dört benzersiz birleşimini tanımlar ve her birleşimi müşterilere içerik sunan benzersiz bir URL'ye eşler.

| Etki alanı                     |  Yol      | Kanal       |   Yerel ayar     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Fabrikam genişletilmiş çevrimiçi mağaza | tr-tr  |
| `https://fabrikam.com` | /es    | Fabrikam genişletilmiş çevrimiçi mağaza | es     |
| `https://fabrikam.ca`  | /      | Contoso çevrimiçi mağaza    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso çevrimiçi mağaza    | en-ca  |

#### <a name="domain"></a>Etki alanı

Etki alanları, e-ticaret sitenizi Microsoft Dynamics Lifecycle Services (LCS) ile ayarladığınızda kurulur. E-ticaret ortamınız sağlandığında, bir servis isteği açarak başka etki alanları da ekleyebilirsiniz. E-ticaret siteleriniz için etki alanları kurma hakkında daha fazla bilgi için bkz. [Dynamics 365 Commerce'te etki alanları](domains-commerce.md).

#### <a name="path"></a>Yol

- Yol, etki alanıyla birlikte, benzersiz bir kanal ve yerel ayar birleşimiyle eşlenen rasgele bir dizedir. Önceki örnekte, yol olarak kullanılan dize, yolun eşlendiği yerel ayar tanımlayıcısıyla eşleşir. Ancak, farklı bir yaklaşım kullanabilirsiniz.
- Bir kanalın ve bir yerel ayarın birleşimi bir etki alanı ve boş bir yol ("/") ile eşleştirilebilir. Önceki örnekte, `https://fabrikam.ca/` adresini ziyaret eden müşterilerimiz Kanada Fransızcasındaki Kanada pazarına yönelik ürünleri ve sınıflamalar elde edilecek.
- Ticari site oluşturucu, bir etki alanı ve yolun yinelenen birleşimlerini oluşturmanızı önler. Ancak, bir kanalın çoğaltılmış birleşimlerini ve bir yerel ayarı ile bir etki alanı ve bir yolun farklı bir birleşimini eşleyebilirsiniz.

#### <a name="channel"></a>Kanal

- Kanallar, (çevrimiçi mağaza olarak da bilinir) bir çevrimiçi e-ticaret vitrini için ödeme yöntemleri, fiyat grupları, ürün hiyerarşileri, sınıflamalar ve ürünler tanımlar.
- Kanallar, Dynamics 365 Commerce yönetim merkezlerinde tanımlanır, yapılandırılır ve yayımlanır.
- Site oluşturucu, Commerce yönetim merkezinde konfigüre edilen ve bir tesisle eşleştirilecek olan çevrimiçi mağazaları algılayabilir.

Kanallar hakkında daha fazla bilgi için bkz. [Kanallar genel bakış](channels-overview.md). Çevrimiçi kanalın nasıl ayarlanacağı hakkında daha fazla bilgi için, bkz. [Çevrimiçi kanal ayarlama](channel-setup-online.md).

#### <a name="locale"></a>Yerel ayar

- Yerel ayar, yerelleştirme için XML yerelleştirme takas dosyası biçimi (XLIFF) dosyalarını teslim ettiğinizde kullanılan gerçek tanımlayıcıdır. Yerel ayarlar, Commerce yönetim merkezlerindeki her bir kanal için tanımlanır ve yayımlanır. Site oluşturucuda dillerin ve kanalların nasıl yapılandırılacağı hakkında bilgi için, sonraki bölüme bakın.
- Aynı yerel ayarlar birden çok kanala eşlenebilir. Bu şekilde, ortak bir dil birden çok pazarda sunulabilir.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>E-ticaret siteniz için dil ve kanal yapılandırma

Kullanıma hazır olarak, tüm Dynamics 365 Commerce e-ticaret siteleri Fabrikam demo sitesiyle başlayıp başlamadığınızdan veya sıfırdan yeni bir site oluşturmanıza bakılmaksızın, tek bir çevrimiçi kanal ve tek bir dil kullanacak şekilde yapılandırılmıştır.

Bu konfigürasyonda, müşteriler ve ortaklar genellikle ülkeler ve diller arasında kullanılacak tüm kıymetleri geliştirir. Bu varlıklar arasında şablonlar, sayfalar, parçalar, içerik ve medya yer alır. Tüm site içeriği, siteniz için seçtiğiniz ilk dilde geliştirilmiştir veya Fabrikam demo sitesini kullanıyorsanız, site içeriği İngilizce olarak geliştirilir.

![Kullanıma hazır Dynamics 365 Commerce e-ticaret sitesi](media/loc-guide-1.png)

> [!NOTE]
> Fabrikam demo sitesini, ek bir dil için konfigüre edebilirsiniz böylece bu dilde içerik geliştirme yapılabilmesini sağlayabilirsiniz. Bir siteye ve kanala yeni dil ekleme hakkında bilgi almak için bu makalenin ilerleyen bölümlerindeki [Siteniz için ek dil yapılandırma](#configure-an-additional-language-for-your-site) başlıklı konuya bakın.

Ancak, Dynamics 365 Commerce e-ticaret siteleri için içerik yönetim sistemi (CMS) ve sayfa modeli, yeni pazarlara ve yerel ayarlara genişlemeye olanak sağlayacak şekilde tasarlanmıştır. Bu nedenle, tek bir e-ticaret sitesi sayesinde, birden fazla pazara ve dile yayılan çevrimiçi bir mağazanın varlıklarını yönetebilirsiniz.

![Birden çok pazara ve dile yayılan Dynamics 365 Commerce e-ticaret sitesi](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Siteniz için ek dil konfigüre etme

Bir e-ticaret sitesi için yeni bir dil konfigüre etme işlemi üç adıma sahiptir.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>Adım 1: Commerce yönetim merkezinde dili kanallarınıza (çevrimiçi mağaza) ekleyin

1. Commerce yönetim merkezinde yeni dili eklemek istediğiniz kanala gidin. Commerce yönetim merkezinde yapılandırdığınız kanallar listesini bulmak için **Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.
1. **Perakende Kanal Kodu** değerini seçerek sitenize eşlenen çevrimiçi mağazayı açın. Commerce site oluşturucuda **Kanallar** sitesi ayar sayfasını açarak ve **Kanallar** sütunundaki çevrimiçi mağazanın adına bakarak, sitenize eşlenen çevrimiçi mağazayı doğrulayabilirsiniz. 
1. **Diller** hızlı sekmesinde **Ekle**'yi seçin. **Dil** alanında, yeni diliniz için yerel ayar kodunu seçin. Sonra **Kaydet**'i seçin.
1. **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım planı**'na gidin ve **1070 Kanal yapılandırması** işini yürütün. İşin çalışması bittiğinde, 2. adıma geçin ve site oluşturucuda sitenizin bir kanalına dili ekleyin.

![Commerce yönetim merkezinde bulunan çevrimiçi mağazanın Diller Hızlı Sekmesi](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>Adım 2: Site oluşturucuda dili bir kanala ekleyin

Site oluşturucuda bir kanala dil eklemek için aşağıdaki adımları izleyin.

1. Commerce site oluşturucuda, sitenizi açın ve sonra da site ayarlarında **Kanallar** sayfasını açın.
1. Dili eklemek istediğiniz kanalın adını seçin.
1. Sağdaki bölmeden **Yerel ayar ekle**'yi seçin.
1. **Yerel ayar ekle** iletişim kutusunda, **Yerel ayar ekle** altında, Commerce yönetim merkezinde kanala daha önce eklediğiniz dilin yerel ayarını seçin.
1. Müşterilerin bu kanaldaki ve dildeki sitenizi görüntülemesini istediğiniz etki alanını ve yolu seçin.
1. Site oluşturucu sayfalarını ve parçalarını görüntülemek, oluşturmak ve güncelleştirmek için dilin varsayılan dil olmasını istiyorsanız, **Varsayılan yazma kanalı dili olarak kullan** onay kutusunu seçin. 
    > [!NOTE]
    > Bu ayar, yalnızca site oluşturucusunu etkiler. Müşterileriniz için yayınlanan site deneyimini etkilemez.
1. **Tamam**'ı seçin.
1. **kaydet ve yayınla** yı seçin.

#### <a name="step-3-localize-your-site-content"></a>Adım 3: Site içeriğinizi yerelleştirin

Commerce site oluşturucuda **Sayfalar** görünümüne döndüğünüzde, yeni dil kanalda ve üst sağ taraftaki yerel ayarlar seçicisinde kullanılabilir olur. Artık temel dilinizde sayfaların yerelleştirilmiş sürümlerini oluşturabilirsiniz.

Sayfalarınızın ve parçalarınızın içeriğini yerelleştirme işlemi bu makalenin devamında yer alan, [E-ticaret sitesi içeriğini yerelleştirme](#localize-e-commerce-site-content) bölümünde ele alınır.

### <a name="configure-a-new-channel-for-your-site"></a>Siteniz için yeni bir kanal konfigüre edin

Dynamics 365 Commerce e-ticaret siteleri, Commerce yönetim merkezinde konfigüre edilen birden çok çevrimiçi kanal arasında tanımlanan deneyimlere hizmet verebilir. Bir site, müşterileri ödeme yöntemleri, fiyat grupları, ürün hiyerarşileri, sınıflamalar ve bir dizi ürün gibi benzersiz konfigürasyonlara göre göstermek için birden çok kanal kullanır. Bir kanal genellikle bu boyutları bağımsız ülkeler ile ilişkilendirilmiş deneyimlerle ilgili gereksinimlere ve tercihlere uyacak şekilde konfigüre etmek için kullanılır. Ancak, bu yaklaşım müşterinin yaptığı bir iş karardır. Gereksinim değildir.

Bir kanal (çevrimiçi mağaza) ayarlamak ile ilgili ön koşullar ve görevler bu belgenin kapsamı dışındadır. Commerce yönetim merkezinde çevrimiçi kanalın nasıl ayarlanacağı hakkında daha fazla bilgi için, bkz. [Kanal kurulumu temelleri](channels-overview.md#channel-setup-basics). Çevrimiçi kanallara özgü adımlar ve gereksinimler hakkında bilgi için, bkz. [Çevrimiçi kanal kurulumu](channel-setup-online.md).

Site oluşturucuda bir sitenize bir kanal eklemek için aşağıdaki adımları izleyin.

1. Commerce site oluşturucusunda, **Site ayarları \> Kanallar**'a gidin. 
1. **Kanal ekle**'yi seçin.
1. **Kanal ekle** iletişim kutusunda **Kanal** altında eklemek istediğiniz kanalı seçin. 
    > [!NOTE]
    > Yalnızca sitenize eklenmemiş olan kanalları ekleyebilirsiniz.
1. Kanalın varsayılan yerel ayarını seçin. Kanala yeni diller eklerseniz, varsayılan dil bunlardan biriyle değiştirilebilir.
1. Bir kanalın ve bir dilin bu birleşimi için içerik ve deneyimlere hizmet veren URL'yi oluşturacak etki alanını ve yolu belirtin.
1. **Tamam**'ı seçin.
1. **kaydet ve yayınla** yı seçin.

## <a name="localize-e-commerce-site-content"></a>E-ticaret sitesi içeriğini yerelleştirin

### <a name="xliff-basics"></a>XLIFF temelleri

XLIFF, içerik yönetim araçları arasında yerelleştirilebilir içeriği geçirmek için sektör standardında bir dosya biçimidir. Commerce site oluşturucu, yerelleştirilebilir ve yeniden içe aktarılacak şekilde sayfa, parça ve görüntü meta veri içeriği vermek için XLIFF dosya biçimini kullanır.

Microsoft Dynamics müşterileri genellikle XLIFF dosyalarını gereksinim duydukları dillere çevirmek için [Translated.com](https://translated.com/welcome) gibi üçüncü taraf yerelleştirme satıcılarıyla çalışırlar.

### <a name="localize-assets-in-site-builder"></a>Site oluşturucuda varlıkları yerelleştirin

Aşağıdaki e-ticaret sitesi varlıkları site oluşturucuda yerelleştirilebilir:

- Sayfalar
- Parçalar
- Ortam varlıkları
- Modüller

Tüm yeni sayfalar, parçalar ve ortam varlıkları kanal ve yerel ayar seçicisinde şu anda seçili olan kanal ve dil bağlamında oluşturulur. Ek diller veya kanallar yapılandırmadığınız için bu dil genellikle "temel dilinizdir". Birden çok kanal ve dilin yapılandırıldığı sitelerde, "temel dil", site ayarlarındaki **Kanallar** sayfasında varsayılan olarak belirlediğiniz kanal ve yerel ayarlar tarafından tanımlanır.

Sayfalar, parçalar ve ortam varlıkları için içeriği yerelleştirme adımları benzerdir. Özel durumlar ve farklılıklar, izleyen bölümlerde gösterilecek. Ancak, modül içeriğini yerelleştirme adımları farklılık gösterir. Daha fazla bilgi için bu makalenin sonraki kısımlarında yer alan [Yerelleştirme modülleri](#localize-modules) bölümüne bakın.

#### <a name="step-1-export-an-xliff-file"></a>Adım 1: XLIFF dosyasını dışa aktar

Site oluşturucuda bir sayfa, parça veya görüntü için bir XLIFF dosyasını dışa aktarmak için aşağıdaki adımları izleyin.

1. Yerelleştirilebilecek temel dil içeriğini dışa aktarmak istediğiniz varlığı açın.
1. Komut çubuğunda, **Yerelleştirme \> XLIFF'i dışa aktar** öğesini seçin.
    > [!NOTE]
    > **Yerelleştirme** seçeneği yalnızca, varlık **Düzenle** durumundayken görünür.

Tarayıcınızın indirilenler klasörüne, **\<assetname\>.xlf** adlı bir XLIFF dosyası indirilir. Bu XLIFF dosyası, yerelleştirdiğiniz varlığa özeldir. Yerelleştirmek istediğiniz her varlık için bir XLIFF dosyası dışa aktaracaksınız.

#### <a name="step-2-localize-the-xliff-file"></a>Adım 2: XLIFF dosyasını yerelleştirin

Çoğu durumda, XLIFF dosyalarınızı çevirmek için bir yerelleştirme satıcısıyla çalışacaksınız. Ancak, varlıkları dahili olarak yerelleştirmeniz halinde veya yerelleştirme işlemini yalnızca test etmek istiyorsanız, bir XLIFF dosyasında aşağıdaki değişiklikleri yapmalısınız:

- /xliff/file öğesine bir hedef dil özniteliği ekleyin ve bu değeri, yerelleştireceğiniz dilin yerel ayar tanımlayıcısına ayarlayın. 
    > [!NOTE]
    > Bu yerel ayar tanımlayıcısının, site ayarlarındaki **Kanallar** sayfasından yerel ayar tanımlayıcısıyla eşleşmesi gerekir.
- Her //source öğesi için, söz konusu kaynak öğesinin içeriğinin yerelleştirmiş sürümü olduğu metin değeri için bir hedef öğe kardeşi ekleyin.

XLIFF dosyalarını yöneten şema hakkında bilgi için bkz. [XLIFF 1.2 Özellikleri](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Bir varlığı birden çok dile yerelleştirmek için, bu dillerin her biri için yerelleştirilmiş bir XLIFF dosyası oluşturmanız gerekir.

#### <a name="step-3-import-the-localized-xliff-file"></a>Adım 3: Yerelleştirilmiş XLIFF dosyasını içe aktarma

Bir varlık için XLIFF dosyasını içe aktarmak için aşağıdaki adımları izleyin.

1. Commerce site oluşturucuda, bir XLIFF dosyasını içe aktarmak istediğiniz varlığı açın.
1. Kanal ve sağ üst taraftaki yerel ayar seçicide, yerelleştirilmiş içeriği almakta olduğunuz kanalı ve dili seçin.
1. Komut çubuğunda, **Yerelleştirme \> XLIFF'i içe aktar** öğesini seçin. Ardından, seçili varlık ve dil için yerelleştirilmiş XLIFF dosyasını bulun ve seçin.

XLIFF dosyası başarıyla alındıktan sonra sayfanın, parçanın veya varlığın "değişken" öğesini oluşturulur. Bu noktadan itibaren, yerelleştirilmiş değişkende yapılan tüm değişiklikler yalnızca o varyantı etkileyecektir. Varyantın türetildiği temel kıymeti etkilemez. Benzer şekilde, temel varlıkta yapılan değişiklikler o varlığın türevini etkilemez. 

Ancak, sayfalar söz konusu olduğunda, söz konusu sayfaların bağlı olduğu şablon veya düzeni değiştirerek varyantlarda değişiklikler yapabilirsiniz. Benzer şekilde, bir parçadaki değişiklikler o değişkenle ilgili bir bağımlılığı olan tüm sayfaları etkileyecektir.

### <a name="images"></a>Görüntüler

Yalnızca bu görüntülerle ilişkilendirilmiş içerik meta verileri yerelleştirilirse, resimler bir sayfa veya modül türevi içinde oluşturulabilir. Şu anda, bir ortam varlığının aşağıdaki meta verileri yerelleştirilebilir:

- Alternatif metin
- Açıklama
- Başlık

Şu anda, bir resim veya video gibi bir dijital varlığın ikili dosyasını yerelleştiremezsiniz. Dynamics 365 Commerce ürün ekibi şu anda bu özellik üzerinde çalışıyor.

### <a name="localize-modules"></a>Modülleri yerelleştirme

Modülün kendisinde bir parça olarak oluşturulan dizeler (örneğin, döner resim modülünde "Önce" ve "İleri"), modül içeriğinden ayrı olarak yerelleştirilmiştir. Yönergeler için, bkz. [Modül yerelleştirme](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Sayfa modeli sözlüğü](page-elements-overview.md)

[Kanallar arası paylaşım](cross-channel-sharing.md)

[Modülü yerelleştirme](e-commerce-extensibility/localize-module.md)

[Modül tanımı dosyası](e-commerce-extensibility/module-definition-file.md)

[Commerce uzantı kaynaklarını ve etiket dosyalarını yerelleştirme](dev-itpro/extension-resource-localization.md)

[CultureInfoFormatter sınıfını kullanarak modülleri globalleştirme](e-commerce-extensibility/globalize-modules.md)

[Uygulama ayarları: Temalar](e-commerce-extensibility/app-settings.md#themes-section)

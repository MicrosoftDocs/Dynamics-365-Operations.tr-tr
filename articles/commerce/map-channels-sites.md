---
title: Kanalları e-ticaret siteleriyle eşleme
description: Bu makalede, diğer iş gereksinimlerinin birçoğu için çıkarım yapılabilecek, Microsoft Dynamics 365 Commerce'teki daha yaygın kanal eşleme senaryoları açıklanmaktadır.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902775"
---
# <a name="map-channels-to-e-commerce-sites"></a>Kanalları e-ticaret siteleriyle eşleme

Bu makalede, diğer iş gereksinimlerinin birçoğu için çıkarım yapılabilecek, Microsoft Dynamics 365 Commerce'teki daha yaygın kanal eşleme senaryoları açıklanmaktadır.

Dynamics 365 Commerce, müşterilere yönelik [e-ticaret sitesi](#e-commerce-sites) deneyimleri için yapılandırılmış bir ürün, fiyat ve indirim grubuna sahip olan [çevrimiçi kanalları](#channels) eşlemek için birçok iş senaryosunu destekler.

Bu makale, aşağıdaki senaryoları destekler:

- **Tek bir e-ticaret sitesi deneyimi sunan tek dilli kanal.** Örneğin, bu senaryoda ABD İngilizcesi pazarında yapılandırılmış tek bir marka sitesi bulunabilir.
- **Tek bir yerelleştirilmiş e-ticaret sitesi deneyimi sunan çok dilli kanal.** Örneğin, bu senaryoda Fransızca ve İngilizce dil desteği ile Kanada için yapılandırılmış tek bir marka sitesi bulunabilir. Bu senaryoda, farklı dilleri seçen kullanıcılar aynı site deneyimine sahip olur, ancak deneyim her kullanıcının seçili diliyle yerelleştirilir.
- **Dil başına farklı bir site deneyimi sunan çok dilli kanal.** Örneğin, bu senaryoda Fransızca ve İngilizce dil desteği ile Kanada için yapılandırılmış tek bir marka sitesi bulunabilir. Bu senaryoda, her dil için benzersiz bir site deneyimi vardır.
- **Tek bir yerelleştirilmiş site deneyimi sunan birden çok kanal (tek dil ve/veya çoklu dil).** Örneğin, bu senaryoda Avustralya ve Yeni Zelanda için yapılandırılmış tek bir marka sitesi bulunabilir. Bu senaryoda, her iki ülke de İngilizce dilinde aynı site deneyimini paylaşır, ancak her ülke farklı ürünler, para birimleri, fiyatlar, indirimler ve sevkiyat şekilleriyle yapılandırılır.
- **Kanal başına farklı bir site deneyimi sunan birden çok kanal (tek dil ve/veya çoklu dil).** Örneğin, bu senaryoda birden çok dilde Avustralya, Kanada ve Almanya için yapılandırılmış tek bir marka sitesi bulunabilir. Bu senaryoda, her ülke için farklı ürünler, para birimleri, fiyatlar, indirimler ve sevkiyat şekilleriyle yapılandırılan benzersiz bir site deneyimi sunulur.

## <a name="channels"></a>Kanallar

Bir kanal (çevrimiçi mağaza veya çevrimiçi kanal olarak da bilinir), e-ticaret müşterileriniz tarafından kullanılabilecek ürünler, fiyatlandırma, iskontolar, diller, ödeme yöntemleri, teslimat şekilleri, karşılama merkezleri ve çevrimiçi deneyimin diğer yönlerini eşlemek için kullanılan bir çevrimiçi e-ticaret mağazasını temsil eder. Kanallar, Commerce Headquarters'da oluşturulur ve yönetilir ve tek bir [tüzel kişilikle](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities) eşleştirilir. Tüzel kişilik genellikle kanal için vergi raporlaması gerektiren tek bir ülkeye dayanır ve yalnızca tek bir para birimiyle yapılandırılabilir.

Kanallar hakkında daha fazla bilgi için bkz. [Kanala genel bakış](channels-overview.md). Çevrimiçi kanalın nasıl oluşturulacağı hakkında daha fazla bilgi için bkz. [Çevrimiçi kanal ayarlama](channel-setup-online.md).

Commerce Headquarters'dan alınan aşağıdaki örnek, tanıtım verileri seçeneği işaretliyse Dynamics 365 Commerce ile dağıtılan varsayılan çevrimiçi kanalları gösterir.

![Commerce Headquarters'daki varsayılan tanıtım verileri kanalları.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>E-ticaret siteleri

Bir e-ticaret sitesi, müşterilerin göz atmak ve alışveriş yapmak için kullandığı bir site sayfaları kümesini içerir. E-ticaret siteleri Commerce site oluşturucuda yönetilir.

Site oluşturucuda site oluşturma ve yönetme hakkında daha fazla bilgi için bkz. [E-ticaret sitesine genel bakış](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Yaygın kanal eşleme senaryoları

Dynamics 365 Commerce çok çeşitli kanal eşleme senaryolarını destekler. Aşağıdaki kanal eşleme senaryoları olası tüm kanal eşleme senaryolarının yalnızca bir alt kümesidir. Bunlar, sahip olduğunuz benzersiz iş senaryolarını planlamanıza yardımcı olacak bir kılavuz olarak hazırlanmıştır. Dynamics 365 Commerce demo verileriyle birlikte gelen Adventure Works adlı hayali bir spor malzemeleri mağazası her bir senaryo için örnek olarak kullanılmıştır.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Tek bir e-ticaret sitesi deneyimi sunan tek dilli kanal

En temel senaryoda tek bir kanal tek bir pazarda satış yaparken tek bir dil sunar. Bu senaryo için bir örnek, yalnızca ABD İngilizcesi pazarı için ayarlanmış Adventure Works çevrimiçi mağazasıdır.

Aşağıdaki örnek çizimde, Commerce headquarters'da bir kanal yapılandırması gösterilmektedir. Bu yapılandırmada, çevrimiçi kanal yalnızca tek bir dili (**en-US**), tek bir para birimini (**USD**) ve vergi raporlamasında kullanılan tek bir işletme tüzel kişiliğini (**usrt**) destekler.

![Commerce Headquarters'da vurgulanan Adventure Works çevrimiçi mağazasının tüzel kişilik, para birimi ve dil değerleri.](media/channel-mapping-3.png)

Tek bir çevrimiçi kanal, site oluşturucuda tek bir e-ticaret sitesiyle eşleştirilebilir. Yeni bir sitenin nasıl oluşturulacağı ve bir kanala nasıl eşleneceğini öğrenmek için bu makalenin [Site oluşturucuda bir kanalı bir siteye eşleme](#map-a-channel-to-a-site-in-site-builder) bölümüne bakın.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Tek bir yerelleştirilmiş e-ticaret sitesi deneyimi sunan çok dilli kanal

Bu senaryoda, tek bir kanal birden fazla dili destekler. Bu nedenle, ürün adları, açıklamalar ve öznitelikler Commerce Headquarters'da yerelleştirilebilir. Tam bir yerelleştirilmiş site deneyimi sağlamak için sitedeki pazarlama içeriği Commerce site oluşturucuda da yerelleştirilebilir.

Bu senaryonun sınırlaması, tek bir kanalın yalnızca bir para birimi, bir tüzel kişilik ve bir ürün ve fiyat kümesiyle yapılandırılabilir olmasıdır. Bu yapılandırma, tek bir para birimine ve birden çok dile (örneğin Kanada, İngilizce ve Fransızca dillerine sahiptir), tek bir tüzel kişiliğe ve tek bir ürün ve fiyat kümesine sahip ülkeler için en iyi çalışır.

Bir kanaldaki her dil kendi etki alanı adıyla yapılandırılabilir. Örneğin, `www.adventure-works.ca` etki alanı Kanada İngilizcesi sürümü için yapılandırılabilir ve `www.adventure-works-fr.ca` etki alanı Kanada Fransızcası sürümü için yapılandırılabilir. Alternatif olarak, bir kanaldaki farklı diller tek bir etki alanında yapılandırılabileceği gibi, her dil için farklı bir yol da kullanılabilir. Örneğin, `www.adventure-works.ca` etki alanı Kanada İngilizcesi sürümü için yapılandırılabilir ve ardından `www.adventure-works.ca/fr` yolu Kanada Fransızcası sürümü için yapılandırılabilir. [Coğrafi algılama](geo-detection-redirection.md), kullanıcının konumuna göre kullanıcıyı doğru siteye yeniden yönlendirmek üzere de etkinleştirilebilir.

Müşterilerin diller arasında el ile geçiş yapmasının nasıl sağlanacağı hakkında bilgi için bu makalenin [Site seçici modülünü ekleme ve yapılandırma](#add-and-configure-the-site-picker-module) bölümüne bakın. Yerelleştirilmiş sayfaların ve parçaların özelleştirilmesi hakkında bilgi için [Birden çok kanal ve dil içeren site içeriğini yönetme](#manage-site-content-that-has-multiple-channels-and-languages) bölümüne bakın.

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Dil başına farklı bir site deneyimi sunan çok dilli kanal

Tek bir kanalın birden fazla dili desteklediği bir senaryoyu tercih edebilirsiniz, ancak her dil için tamamen farklı bir site deneyimi oluşturulur. Bu senaryoyu uygulamak için önerilen yöntem, tek bir sitede [sayfa varyantları](#implement-page-variants-for-each-language) kullanmaktır.

Diğer bir yöntem de, site oluşturucudaki her dil için yeni bir e-ticaret sitesi oluşturmak ve sonra her siteyi tek bir çevrimiçi kanal ve dille eşlemektir. Sonuç, her biri bir dil için olmak üzere birden çok e-ticaret sitesine eşlenen tek bir çevrimiçi kanal olacaktır. Bu çok siteli yöntem, site oluşturucuda yönetilecek birden fazla site olacağından ek yönetim kaynakları gerektirir.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Tek bir yerelleştirilmiş site deneyimi sunan birden çok kanal (tek dil ve/veya çoklu dil)

Markalı bir site, tek bir sitedeki her kanal için farklı bir para birimini, ürün kümesini ve fiyat kümesini desteklemek üzere her bölge için birden çok çevrimiçi kanal gerektirebilir. Örneğin, Adventure Works sitesinde, birden çok dile sahip Kanada pazarı için bir çevrimiçi kanal, bir dile sahip ABD pazarı için bir kanal ve bir dile sahip Alman pazarı için bir kanal bulunabilir. Bu senaryoda, her çevrimiçi kanal bölgeye özel tüzel kişilik için yapılandırılır ve diğer kanalların sahip olduğu ürün kümelerini, bu ürünlerin bir alt kümesini veya farklı bir ürün kümesini içerebilir. Her kanalın bölgesel para birimi, vergiler, indirimler ve sevkiyat şekillerinde kendi fiyatları da olacaktır.

Bu senaryoda, her piyasa kendi etki alanı adlarıyla yapılandırılabilir. Örneğin, `www.adventure-works.com` etki alanı ABD piyasası için yapılandırılabilir ve `www.adventure-works.de` etki alanı Alman piyasası için yapılandırılabilir. Alternatif olarak, her pazar farklı bir yol kullanacak şekilde yapılandırılabilir. Örneğin, `www.adventure-works.com` etki alanı ABD piyasası için yapılandırılabilir ve sonra `www.adventure-works.com/de` yolu Alman piyasası için kullanılabilir. [Coğrafi algılama](geo-detection-redirection.md), kullanıcıların konumuna göre kullanıcıları doğru siteye yeniden yönlendirmek üzere de etkinleştirilebilir.

Ayrıca sitenizin, kullanıcıların el ile belirli bir pazara geçmelerini sağlayan bir açılan liste sağlamasını da isteyebilirsiniz. Daha fazla bilgi için, bu makalenin [Site seçici modülü ekleme ve yapılandırma](#add-and-configure-the-site-picker-module) bölümüne bakın.

Birden çok kanalı tek bir sitede yapılandırma hakkında bilgi için [Bir e-ticaret sitesinde birden çok kanalı yapılandırma](#configure-multiple-channels-on-an-e-commerce-site) bölümüne bakın.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Kanal başına farklı bir site deneyimi sunan birden çok kanal (tek dil ve/veya çoklu dil)

Farklı bölgelerdeki tek bir marka için birden çok kanala sahip olmak isteyebilirsiniz ve her bir bölgenin farklı bir site deneyimine sahip olmasını isteyebilirsiniz. Bu senaryoyu uygulamak için iki yöntem vardır:

- [Sayfa varyantlarını](#implement-page-variants-for-each-language) kullanın.
- Site oluşturucudaki her çevrimiçi kanal için farklı bir site yapılandırın ve sonra her siteyi farklı bir çevrimiçi kanala ve dile eşleyin. Bu yöntem, site oluşturucuda yönetilecek birden fazla site olacağından ek yönetim kaynakları gerektirir.

## <a name="cross-channel-sharing"></a>Kanallar arası paylaşım

Kanallar arası paylaşım, tek bir sitedeki birden fazla kanal içeriği paylaşabileceği zaman yararlıdır. Örneğin, tek bir site altında gruplandırılan birden çok markaya ve mağazaya sahip olan bir satıcı, bazı içerikleri mağazaların bir kısmı veya tümü arasında paylaşabilir. Paylaşılan içerik hüküm ve koşullar, ödeme koşulları, sevkiyat yöntemleri ve sık sorulan sorular (SSS) ile ilgili sayfalar içerebilir. Daha fazla bilgi için bkz. [Kanallar arası paylaşımı etkinleştirme ve kullanma](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Site oluşturucuda bir kanalı bir siteye eşleme

Farklı çevrimiçi kanallar kullanmak üzere site oluşturmak ve yapılandırmak için birden çok yöntem vardır.

### <a name="create-a-new-site"></a>Yeni bir site oluşturma

Site oluşturucuda yeni bir site oluşturmak için **Siteler** listesi sayfasına gidip **Yeni site**'yi seçebilirsiniz. Daha sonra, görüntülenen **Yeni site** iletişim kutusunda, aşağıdaki örnek çizimde gösterildiği gibi, sitenin varsayılan çevrimiçi kanalını ve dilini seçebilirsiniz.

![Site oluşturucuda yeni bir kanal oluşturma.](media/channel-mapping-4.png)

Bu şekilde oluşturduğunuz site boş kalır ve herhangi bir site sayfası (örneğin, bir giriş sayfası, kategori sayfaları ve ürün sayfaları) içermez.

Daha fazla bilgi için, bkz [e-ticaret sitesi oluşturma](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Site kopyalama işlemini kullanarak yeni bir site oluşturma

Önceki bölümde açıklandığı gibi, yepyeni ve boş bir site oluşturmak yerine, Commerce modül kitaplığı içinde sağlanan Fabrikam veya Adventure Works sitesi gibi başlangıç sitelerinden birinin kopyasıyla başlamak daha iyi bir uygulamadır.

Varolan bir siteyi kopyalamak için, site oluşturucuda **Siteler** listesi sayfasına gidin ve **Siteyi kopyala**'yı seçin. Sonra da, **Siteyi kopyala** iletişim kutusunda kaynak siteyi seçebilir ve hedef sitenin adını belirtebilirsiniz.

Bu aşamada, sitenin varsayılan çevrimiçi kanalını ve dilini henüz seçemezsiniz. Ancak bu özellikleri, site kopyalama işlemi tamamlandıktan sonra yapılandırabilirsiniz. Site oluşturucuda **Siteler** listesi sayfasında siteyi ilk kez seçtiğinizde, varsayılan kanalı ve dili seçebileceğiniz bir **Sitenizi ayarlayın** iletişim kutusu belirir.

Site kopyalama işlemi hakkında daha fazla bilgi için bkz. [E-ticaret sitesini kopyalama](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Varolan bir site kanalını yönetme

Bir site bir kanal ile yapılandırıldıktan sonra, aşağıdaki örnek çizimde gösterildiği gibi, site oluşturucunun **Site Oluşturucu \> Kanallar** bölümünde seçilen siteden kanalı yönetebilir ve güncelleştirebilirsiniz.

![Site oluşturucuda kanal eşlemesini yönetme.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Tek bir kiracıda birden çok siteyi destekleme

Birçok markalı site tek bir kiracıda birlikte çalışabilir. Aşağıdaki örnek gösterimde, her biri farklı tek bir çevrimiçi kanalla eşlenen üç farklı markalı site (Adventure Works, Adventure Works Business ve Fabrikam) gösterilmektedir.

![Site oluşturucuda site listesi.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Birden çok siteye ait yollarla tek bir etki alanı adı yapılandırma

Tek bir etki alanı adı birden çok site için kullanılabilir ve daha sonra yollar siteleri veya dilleri ayırmak için kullanılabilir. Örneğin, `www.mycompany.com` etki alanı iki farklı e-ticaret sitesi için yapılandırılmıştır: Fabrikam için bir tane ve Adventure Works için bir tane. Bu durumda, boş yol olarak da bilinen varsayılan yol (`www.mycompany.com`), Fabrikam sitesi için kullanılabilir ve Adventure Works sitesi için başka bir yol (örneğin, `www.mycompany.com/adventureworks`) kullanılabilir. Diğer bir seçenek de Fabrikam sitesinin varsayılan yolu yerine özel bir yol (örneğin `www.mycompany.com/fabrikam`) kullanmaktır.

Alternatif olarak, her site için farklı bir etki alanı adı kullanılabilir (örneğin, `www.adventure-works.com` ve `www.fabrikam.com`). Böylece, yollar farklı diller veya bölgeler (örneğin Kanada Fransızcası için `www.adventure-works.com/fr-ca`) için kullanılabilir.

## <a name="configure-multiple-languages-on-a-site"></a>Sitede birden çok dil yapılandırma

Diller site oluşturucunun **Site ayarları \> Kanallar** bölümünde e-ticaret sitesi için yapılandırılabilir. Aşağıdaki örnekte, her dil yolun yerel ayarı kullanılarak yapılandırılmıştır; böylece her dilin benzersiz bir URL'si olur.

![Sitede yapılandırılan birden çok dil.](media/channel-mapping-10.png)

Yeni bir kanal dili eklemek için, **Site ayarları \> Kanallar**'a gidin ve kanal bağlantısını seçin. Sağda görüntülenen bölmede, eklemek istediğiniz kanalı ve yerel ayarı seçmek için **Yerel ayar ekle**'yi seçin. Sonra seçili kanal için kullanılacak yolu belirtin.

### <a name="add-and-configure-the-site-picker-module"></a>Site seçici modülünü ekleme ve yapılandırma

Birden çok dil ve veya kanal içeren bir siteyi yapılandırdıktan sonra, kullanıcıların dil veya ülke özelliklerini el ile seçmesini sağlamak için site sayfası üst bilgisine bir dil seçici eklemek isteyebilirsiniz. Modül kitaplığı [üst bilgi modülü](author-header-module.md), kullanıcıların [site seçici modülünü](site-selector.md) kullanarak dil seçmesini sağlamak için yerleşik desteğe sahiptir. Site seçicisi modülü, üst bilgi parçasındaki üst bilgi modülüne eklenebilir.

Site seçici modülü ekleme ve yapılandırma hakkında daha fazla bilgi için bkz. [Site seçici modülü](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Her dil için sayfa varyantlarını uygulama

Bu senaryoda, yalnızca bir kanal vardır, ancak birden çok dil vardır. Sayfa varyantı oluşturarak, bir sayfanın görünümünü seçilen dile göre değiştirebilirsiniz. Daha sonra, bu varyanta yerelleştirilmiş içeriği ekleyebilirsiniz.

Site oluşturucuda açık bir sayfanız varsa ve geçerli kanalı ve dili gösteren sağ üst taraftaki bağlantıyı seçerseniz, aşağıdaki örnek çizimde gösterildiği gibi bir kanal ve dil seçici görünür. Geçerli dilin sayfasını geçersiz kılmak istiyorsanız, başka bir yerel ayar seçin ve sonra **Değiştir**'i seçin. [Birden çok kanal ve dil içeren bir siteyi yönetiyorsanız](#manage-site-content-that has-multiple-channels-and-languages) kanalı da değiştirebilirsiniz.

![Site oluşturucuda bir sayfanın dilini değiştirme.](media/channel-mapping-14.png)

Seçili sayfa veya parçanın varyantı henüz oluşturulmadıysa, aşağıdaki örnek çizimde gösterildiği gibi bir uyarı mesajı alırsınız. Bu durumda, ileti metninde **Sayfa varyantı oluştur** bağlantısını seçin. Görüntülenen iletişim kutusu, varolan bir varyantın kopyasını başlatmanıza veya bir şablondan yeni sayfa oluşturmanıza olanak veren seçenekler sağlar.

![Site oluşturucuda bir sayfa varyantı oluşturmak için sorma](media/channel-mapping-16.png)

Varyant oluşturmazsanız, orijinal sayfa işlenir ve modül dizeleri için uygun dili ve Commerce Headquarters'dan alınan ürün bilgilerini gösterir. Ancak, sayfa başlığı veya diğer pazarlama içeriği gibi metinler doğrudan varsayılan sayfa modüllerinde belirtildiyse, o metnin dizeleri özgün dilde kalır.

Her bir sayfa ve parçayı el ile oluşturmak yerine her sayfayı ve parçayı, daha sonra yerelleştirme için gönderilebilecek bir XML Yerelleştirme Takas Dosyası Biçimi (XLIFF) dosyasına aktarabilirsiniz. Her XLIFF yerelleştirildikten sonra, yerelleştirilmiş bir sayfa varyantı olarak içe aktarılabilir. Bir XLIFF dosyasını site oluşturucuda bir sayfadan veya parçadan dışa aktarmak veya bir XLIFF dosyasını bir sayfaya veya parçaya içe aktarmak için komut çubuğunda **Yerelleştirme**'yi seçin. Daha sonra aşağıdaki örnek çizimde gösterildiği gibi, **XLIFF'i Dışa Aktar** veya **XLIFF'i İçe Aktar**'ı seçin.

![Bir sayfa veya parçayı XLIFF formatında içe veya dışa aktarma.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Birden çok kanal ve dil içeren site içeriğini yönetme

Birden çok kanal ve/veya dil içeren bir site, her bir kanal ve dil kombinasyonu için her bir sayfa ve parçanın benzersiz bir varyantını depolar. Bu davranış, sayfa varyantlarının yerelleştirilmiş veriler içermesini sağlar, ancak belirli bir varyant için bir sayfanın görünümünü değiştirme esnekliği de sağlar.

Sayfa varyantlarıyla nasıl çalışılacağı hakkında bilgi için bu makalenin [Her bir dil için sayfa varyantlarını uygulama](#implement-page-variants-for-each-language) bölümüne bakın.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Bir e-ticaret sitesinde birden çok kanal yapılandırma

Site oluşturucuda **Site ayarları \> Kanallar**'a gidip **Kanal ekle**'yi seçerek bir e-ticaret sitesine kanal ekleyebilirsiniz. Ardından, görüntülenen **Kanal ekle** iletişim kutusunda çevrimiçi kanalı ve varsayılan yerel ayarı seçebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Kanallara genel bakış](channels-overview.md)

[Çevrimiçi kanal ayarlama](channel-setup-online.md)

[Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Coğrafi konum algılama ve yeniden yönlendirme özelliğini ayarlama](geo-detection-redirection.md)

[Kanallar arası paylaşımı etkinleştirme ve kullanma](cross-channel-sharing.md)

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[E-ticaret sitesini kopyalama](copy-ecommerce-site.md)

[Site seçicisi modülü](site-selector.md)

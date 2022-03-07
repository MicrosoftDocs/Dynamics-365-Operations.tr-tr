---
title: Taraf ve genel adres defteri
description: Bu konu, Çift yazmanın taraf ve genel adres defteri işlevlerini açıklamaktadır.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: e7bec58f8094a1448017822e7d8840368cc482b8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750800"
---
# <a name="party-and-global-address-book"></a>Taraf ve genel adres defteri

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Taraf ve genel adres defteri, Finance and Operations uygulamalarındaki kavramlardır. Taraf, bir kişi veya kuruluş olabilir. **Tarafın** Ad, dil, kişi ve adres gibi özelliklerini genel olarak depolamak ve yönetmek için kolaylık sunar. Bir özellik değeri bir yerde değiştiğinde, **tarafın** bulunduğu tüm yerlere yansıtılır.

## <a name="party"></a>Taraf

*Taraf*, işle ilgisi bulunan bir kişi veya kuruluştur. Kişi veya kuruluş, taraf kavramını kullanarak bir işletmede birden fazla role (çalışan, müşteri, satıcı veya ilgili kişi) sahip olabilir. Rol, bağlama ve amaca bağlıdır. Burada, Contoso ve Fabrikam adlı iki hayali şirketten birkaç örneğe yer verilmektedir.

+ **Çalışan**: Bir personel. Örneğin, Contoso personeli.
+ **Satıcı** Bir tedarikçi kuruluş veya bir işletmeye mal veya servis sağlayan tek bir sahip anlamına gelir. Örneğin, Fabrikam Contoso'ya malzeme satıyorsa Fabrikam satıcı rolündedir.
+ **İlgili kişi**: İletişime geçilecek kişi. Örneğin, Contoso Fabrikam'dan malzeme satın alıyorsa contoso'daki bir personel Fabrikam'daki ilgili kişiyle bağlantı kurar.
+ **Müşteri**: Müşteri bir şirketten bir şey satın alan kişi veya şirkettir. Örneğin, Contoso Fabrikam'dan malzeme satın alıyorsa Contoso bir Fabrikam müşterisidir.

Taraf modeli, özellikle bir taraf birden fazla rol oynadığında kuruluşlar ve kişiler arasındaki orta seviye ve karmaşık ilişkileri temsil etmek için kullanılır. Burada bazı genel örnekler verilmiştir:

+ Bir taraf hem müşteri hem de satıcı olabilir. Örneğin, Kuzey Amerika'da, Fabrikam Contoso'ya elektrik kabloları satar ve contoso'dan montajlı hoparlörler satın alır. Avrupa'da, Fabrikam Contoso'ya parça satar ancak Contoso'dan herhangi bir şey satın almaz.
+ Bir taraf hem personel hem de müşteri olabilir. Örneğin, bir Contoso çalışanı Contoso'dan kişisel kullanım için elektronik aygıtlar satın alır.
+ Bir kişi ile bir kuruluş arasında çoğa çok ilişkisi olabilir. Örneğin, Fabrikam, hizmet uzmanları sağlar ve bir yerleşim koordinatörü çalıştırır. Koordinatör, Fabrikam müşterilerinin birkaçından gelen iş istekleriyle uygun hizmet uzmanlarını eşleştirir. Contoso, müşteri hesaplarından biridir. Contoso'ya bir uzman gerektiğinde, Contoso, koordinatörle iletişim kurar ve koordinatör bu isteği yerine getirir. Koordinatör, tüm müşterilerin istekleriyle ilgilenerek çoğa çok ilişkisi oluşturur.

Aşağıdaki resimde taraf için veri modeli gösterilmektedir:

![Taraf için veri modeli](media/party-gab-image1.png)

> [!Tip]
> Yeni bir hesap kaydı oluşturmaya çalıştığınızda, kaydı ada göre aramak için "taraf" alanını kullanın. Kaydı bulursanız, yalnızca kaydı seçmeniz gerekir. Sistem, taraftan gelen tüm verileri otomatik olarak doldurur. Gerekli tüm alanları el ile girmeniz gerekmez. Bu davranış, kullanıma hazır bir şekilde gönderilen firma, ilgili kişi ve satıcı formlarında bulunabilir.

Finance and Operations uygulamalarındaki tüm taraf rolleri Çift yazma tarafından desteklenmez. Taraf rollerinin tam listesi için bkz. [Genel adres defterine genel bakış](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Genel adres defteri

Genel adres defteri, bir işte yer alan kuruluşların ve kişilerin posta ve elektronik adresler dizinidir.

Genel adres defteri gerektiği kadar posta adresi ve elektronik adres depolar ve işler. Örneğin, Fabrikam'ın 50 konumda benzin istasyonları olduğunu varsayalım. Her yerin farklı bir posta adresi, e-posta adresi ve telefon numarası vardır. Tüm iş harcamaları Ana benzin istasyonuna faturalandıralınır, ancak Satın almalar doğrudan satın almayı talep eden belirli benzin istasyonuna sevk edilir. Genel adres defteri, ana benzin istasyonunu faturalama adresi, her bir benzin istasyonunu da Fabrikam için sevkiyat adresi olarak kaydeder. Adresler bir kez depolanabilir ve teklifler ve siparişler için gerektiğinde alınır.

Bir kişi veya bir kuruluş iş bağlamına dayalı olarak birden fazla rol yürütebilir. Bunu yaparken, posta adresleri ve elektronik adresleri aynı olabilir. Bu durumda, bir roldeki adres değişikliği diğer rolde görünmelidir veya tam tersi de geçerlidir. Genel adres defteri, adresleri genel olarak depolar ve işler.

![Genel Adres Defteri için veri modeli](media/party-gab-image2.png)

## <a name="contacts"></a>İlgili kişiler

Müşteri etkileşimi uygulamalarında *ilgili kişi* bir kişidir. Ancak, **ilgili kişi** tablosu bir kişiyi, bir portal kullanıcısını, bir B2C müşterisini veya bir satıcıyı temsil edecek şekilde aşırı yüklenmiştir. Bu gösterim örtülüdür ve ilgili işlemleri araştırmadan farkı anlayamazsınız. **İlgili kişi** tablosu, **hesap** tablosuyla 1:1 ilişkisi olacak şekilde sınırlanmıştır. Taraf ve genel adres defteri modelinin bir parçası olarak çift yazma sınıflandırma için açık özellikler sunar ve Çift yazma **ilgili kişi** ve kuruluş (firma varlığı veya satıcı varlığı) arasında N:N ilişkilere izin verir.

İki tür **İlgili kişi** satırı vardır:

+ Şeritli ilgili kişi: **Şirket** alanında zorunlu değer bulunan ilgili kişi satırı.
+ Şeritsiz ilgili kişi: **Şirket** alanı boş olan ilgili kişi satırı.

**İlgili kişi** tablosu şu tür satırları depolayabilir:

Row türü | Tanım
---|---
Müşteri olan, örneğin, satış yapılabilir ilgili kişi veya B2C müşterisi olan kişi. | **Şirket** alanının boş olmadığı ve **Müşteri mi?** alanı **Evet** olarak ayarlanan şeritli bir ilgili kişi kaydı.
Satıcı olan bir kişi, örneğin, satıcı gibi tek sahip. | **Şirket** alanının boş olmadığı ve **Satıcı mı?** alanı **Evet** olarak ayarlanan şeritli bir ilgili kişi kaydı.
Hem müşteri hem de satıcı olan bir kişi. | **Şirket** alanının boş olmadığı ve **Müşteri mi?** alanı **Evet** olarak ayarlanan ve **Satıcı mı?** alanı **Evet** olarak ayarlanan şeritli bir ilgili kişi kaydı. Bir kişi, bir ürün için üretici, başka bir ürün için tüketici olabilir. Her iki Finance and Operations uygulaması ve çift yazma bu ilişkiyi destekler.
Bir kuruluşun ilgili kişisi olan, ancak müşteri veya satıcı olmayan kişi. | **Şirket** alanının boş olduğu ve **Müşteri mi?** alanı **Hayır** olarak ayarlanan ve **Satıcı mı?** alanı **Hayır** olarak ayarlanan şeritsiz bir ilgili kişi kaydı.

## <a name="contact-for-party"></a>Taraf için ilgili kişi

**Taraf için ilgili kişi** **Hesaplar** satırları ve **İlgili kişi** satırları arasındaki N:N ilişkilerini depolar ve işler. Şeritli **ilgili kişi** satırlarını şeritsiz satırlardan filtreleyebilir ve yalnızca şeritsiz **ilgili kişi** satırlarını bir **Hesap** veya **satıcı** satırlarıyla ilişkilendirebilir.

Örneğin, Natasha Jones ve Miguel Reyes, bölgelerindeki çiftliklere hizmet sunan veterinerlerdir. Natasha Seattle bölgesinde ve Miguel Kent bölgesinde hizmet sunar. Customer Engagement uygulamasında, çiftlikler müşteri olarak, veterinerler ise ilgili kişiler olarak temsil edilir. Natasha için tek bir **ilgili kişi** kaydı, Natasha'nın birlikte çalıştığı tüm çiftlikler ile ilişkilidir. Benzer şekilde, Miguel için tek bir **ilgili kişi** kaydı, Miguel'in birlikte çalıştığı tüm çiftlikler ile ilişkilidir.

Bu ilişkiler, **taraf için ilgili kişi** tablosunda depolanır. Kullanıma hazır formlarda bilgileri bulabilirsiniz:

+ **Hesap** formundayken **İlişkili ilgili kişiler** adında bir sekme bulunur. Bir veya daha fazla ilgili kişiyi **hesap** satırıyla ilişkilendirmek için bu sekmeyi kullanın. Bu formda, bir kuruluş için ilgili kişi atıyorsunuz. İlgili kişileri atadıktan sonra, söz konusu hesap için birincil ilgili kişi olarak birini seçebilirsiniz. **Hızlı Oluştur** formunu kullanarak yalnızca bir ilgili kişi seçebilirsiniz. **Satıcı** formunu kullanırken ve kayıt türü **Kuruluş** olduğunda davranış aynıdır.
+ **İlgili Kişi** formundayken ve satır müşteri veya satıcı ya da her ikisi (şeritli ilgili kişi) olduğunda, **ilişkili ilgili kişiler** adında bir sekme vardır. Bir veya daha fazla ilgili kişiyi ilişkilendirmek için bu sekmeyi kullanın. Bu formda, B2C müşterisi veya satıcı için ilgili kişi atıyorsunuz. İlgili kişileri atadıktan sonra, birincil ilgili kişi olarak birini seçebilirsiniz. **Hızlı Oluştur** formunu kullanarak yalnızca bir ilgili kişi seçebilirsiniz.
+ **İlgili Kişi** formundayken ve satır ilgili kişi (şeritsiz ilgili kişi) olduğunda, **ilişkili ilgili kuruluşlar** adında bir sekme vardır. Bir veya daha fazla müşteri ya da satıcıyı ilişkilendirmek için bu sekmeyi kullanın. Bu formda, bir müşteri veya satıcıyı temel ilgili kişiye atıyorsunuz. Müşteri veya satıcı, bir kuruluş, bir kişi veya her ikisi olabilir. Belirli bir anda dört alandan yalnızca bir değer seçebilirsiniz.

    ![İlişkili kuruluşlar sekmesi](media/party-gab-image3.png)

    + **Taraf Kimliği**'ni seçerseniz, temel ilgili kişi seçilen tarafın tüm rollerine atanır.
    + **İlişkili ilgili kişi**'yi seçerseniz kişi türünde olan şeritli ilgili kişiyi seçersiniz.
    + **İlişkili hesap** veya **satıcı**'yı seçerseniz bir kuruluş seçersiniz.

    Seçiminiz ne olursa olsun, ilişkilendirme taraf düzeyinde oluşturulur ve tarafın tüm rollerine uygulanır ve "taraf için ilgili kişi" varlığı içinde depolanır.

> [!Note]
> Customer engagement uygulamasında **taraf için ilgili kişi** tablosunun görünen adı **müşteri/satıcı için ilgili kişi**'dir.

**Müşteri**'nin **Hayır** ve **satıcı**'nın **Hayır** olduğu bir **İlgili kişi** satırı açtığınızda **ilişkili kuruluşlar** sekmesini göreceksiniz. Bir veya daha fazla müşteri ya da satıcı kuruluşunu ilgili kişiyle ilişkilendirmek için bu sekmeyi kullanın.

**Müşteri**'nin **Evet** ve **satıcı**'nın **Evet** olduğu bir **İlgili kişi** satırı açtığınızda **ilişkili ilgili kişiler** sekmesini göreceksiniz. Bir veya daha fazla ilgili kişiyi ilişkilendirmek için bu sekmeyi kullanın.

## <a name="postal-address"></a>Posta adresi

**Hesap**, **ilgili kişi** ve **satıcı** formlarında **adresler** adlı yeni bir sekme sunuldu. **Adresler**, bu görüntüde gösterildiği gibi, N adreslerini kılavuz kullanarak destekler:

![Posta adresi için kılavuz](media/party-gab-image4.png)

+ **Posta adresi rolleri** sütunu adresin amacını listeler.
+ **Birincil** sütununda birincil adres listelenir.
+ **Adres numarası** sütunu, adres sırasını listeler.
+ **+ Yeni Adres** düğmesi yeni adres oluşturmanıza olanak tanır. İstediğiniz sayıda adres oluşturabilirsiniz.

**Hesap** formunun **Özet** sekmesindeki **Adres 1** ve **Adres 2** alanları sırasıyla **teslim** ve **fatura** adreslerine karşılık gelir.

![Posta adresi için Özet sekmesi](media/party-gab-image5.png)

**İlgili kişi** formunun **Özet** sekmesindeki **Adres1**, **Adres 2** ve **Adres 3** alanları sırasıyla **İşletme**, **Teslim** ve **fatura** adreslerine karşılık gelir.

## <a name="electronic-address"></a>Elektronik adres

**Hesap**, **ilgili kişi** ve **satıcı** formlarında **Elektronik adresler** adlı yeni bir sekme sunuldu. **Adresler**, bu görüntüde gösterildiği gibi, N adreslerini kılavuz kullanarak destekler:

![Elektronik adresler için kılavuz](media/party-gab-image6.png)

+ **Tür** sütununda adresin türü listelenir.
+ **Birincil** sütununda birincil adres listelenir.
+ **Amaç** sütunu elektronik adresin amacını listeler.
+ **+ Yeni Elektronik Adres** yeni adres oluşturmanıza olanak tanır. İstediğiniz sayıda adres oluşturabilirsiniz.

Elektronik adresler yalnızca bu kılavuzda kullanılabilir. Gelecekteki sürümlerde, tüm elektronik ve posta adresi alanları, **Özet** ve **Ayrıntılar** sekmelerinde olduğu gibi diğer sekmelerden de kaldırılacaktır.

## <a name="setup-instructions"></a>Ayar yönergeleri

Mevcut bir ikili yazma müşterisiyseniz, aşağıdaki ayarlama yönergeleri gereklidir. Aksi takdirde, bu bölümü atlayabilirsiniz.

1. Artık gerekli olmadıklarından aşağıdaki eşlemeleri durdurun. Bunun yerine, İlgili Kişiler v2 (msdyn_contactforparties) eşlemesini çalıştırın.

    + CDS İlgili Kişileri V2 ve İlgili Kişiler (müşteri ilgili kişilerini gösterir)
    + CDS İlgili Kişileri V2 ve İlgili Kişiler (satıcı ilgili kişilerini gösterir)

2. Aşağıdaki varlık eşlemeleri taraf işlevselliği için güncelleştirilir ve bu nedenle en son sürümün bu eşlemelere uygulanması gereklidir.

Eşleme | Bu sürüme Güncelleştir | Değişiklikler
---|---|---
Müşteriler V3 (hesaplar) | 1.0.0.5 |Taraf numarası ve taraflarla ilgili ad, kişisel ayrıntılar, posta adresi alanları, elektronik ilgili kişi adresi alanları gibi alanlar kaldırıldı.
Müşteri V3 (ilgili kişiler) | 1.0.0.5 | Taraf numarası ve taraflarla ilgili ad, kişisel ayrıntılar, posta adresi alanları, elektronik ilgili kişi adresi alanları gibi alanlar kaldırıldı.
Satıcılar V2 (msdyn_vendors) | 1.0.0.6 | Taraf numarası ve taraflarla ilgili ad, kişisel ayrıntılar, posta adresi alanları, elektronik ilgili kişi adresi alanları gibi alanlar kaldırıldı.
CDS satış teklifi başlıkları (teklifler) | 1.0.0.6 | İlgili kişi, Contactforparty referansı ile değiştirildi.
Satış faturası başlıkları V2 (faturalar) | 1.0.0.4 | İlgili kişi, Contactforparty referansı ile değiştirildi.
CDS satış siparişi başlıkları (salesorders) | 1.0.0.5 | İlgili kişi, Contactforparty referansı ile değiştirildi.
Kişiler v2 (msdyn_contactforparties) | 1.0.0.2 | Bu yeni bir eşlemedir. Taraf çözümünün önceki bir sürümüne sahipseniz, bu eşlemeyi belirtilen şekilde en son sürüme güncelleştirdiğinizden emin olun.
CDS Taraf posta adresi konumları (msdyn_partypostaladdresses) | 1.0.0.1  | Bu, önceki taraf önizleme sürümünün parçası olarak eklenen yeni bir eşlemedir.
CDS posta adresi geçmişi v2 (msdyn_postaladdresses) | | Bu, önceki taraf önizleme sürümünün parçası olarak eklenen yeni bir eşlemedir.
CDS Taraf posta adresi konumları (msdyn_postaladdresscollections) | | Bu, önceki taraf önizleme sürümünün parçası olarak eklenen yeni bir eşlemedir.
Taraf İlgili Kişileri v3 (msdyn_partyelectronicaddresses) | | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.

## <a name="templates"></a>Şablonlar

Tablo eşlemeleri koleksiyonu, aşağıdaki tabloda gösterildiği gibi taraf ve genel adres defteri etkileşimi için birlikte çalışır.

Finance and Operations Uygulaması | Müşteri etkileşimi uygulaması     | Tanım
----------------------------|-----------------------------|------------
[İlgili kişi unvanları](mapping-reference.md#223) | msdyn_salescontactpersontitles |
[Müşteriler V3](mapping-reference.md#101) | hesaplar |
[Müşteriler V3](mapping-reference.md#116) | ilgili kişiler |
[CDS Tarafları](mapping-reference.md#220) | msdyn_parties |
[CDS Taraf posta adresi yerleşimleri](mapping-reference.md#233) | msdyn_partypostaladdresses |
[CDS posta adresi geçmişi V2](mapping-reference.md#235) | msdyn_postaladdresses |
[CDS posta adresi yerleşimleri](mapping-reference.md#234) | msdyn_postaladdresscollections |
[CDS satış teklifi başlığı](mapping-reference.md#215) | teklifler |
[CDS satış siparişi başlıkları](mapping-reference.md#217) | salesorders |
[Kapanış sözleri](mapping-reference.md#222) | msdyn_complimentaryclosings |
[İlgili Kişiler V2](mapping-reference.md#221) | msdyn_contactforparties |
[Karar verici roller](mapping-reference.md#224) | msdyn_decisionmakingroles |
[İstihdam iş görevleri](mapping-reference.md#225) | msdyn_employmentjobfunctions |
[Bağlılık programı düzeyleri](mapping-reference.md#226) | msdyn_loyaltylevels |
[Taraf ilgili kişileri V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses |
[Kişisel karakter türleri](mapping-reference.md#227) | msdyn_personalcharactertypes |
[Satış faturası başlıkları V2](mapping-reference.md#118) | faturalar |
[Selamlamalar](mapping-reference.md#228) | msdyn_salutations |
[Satıcılar V2](mapping-reference.md#202) | msdyn_vendors |

Daha fazla bilgi için, bkz. [Çift yazma eşleme başvurusu](mapping-reference.md).

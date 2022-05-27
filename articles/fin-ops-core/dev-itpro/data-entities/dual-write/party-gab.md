---
title: Taraf ve genel adres defteri
description: Bu konu, Çift yazmanın taraf ve genel adres defteri işlevlerini açıklamaktadır.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 1e2dcfa69308f6691e787a1ff1893f9080dcaef1
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717460"
---
# <a name="party-and-global-address-book"></a>Taraf ve genel adres defteri

[!include [banner](../../includes/banner.md)]



Finans ve Operasyon uygulamalarında, *Taraf* ve *global adres defteri* kavramları kullanılır. Taraf, bir kişi veya kuruluş olabilir. Tarafın ad, dil, kişi ve adres gibi özelliklerini genel olarak depolamak ve yönetmek için kolaylık sunar. Ardından, bir özellik değeri bir yerde değiştiğinde, bu değişim tarafın bulunduğu tüm yerlere yansıtılır.

## <a name="party"></a>Taraf

Taraf, bir işle ilgisi bulunan bir kişi veya kuruluştur. Kişi veya kuruluş, taraf kavramını kullanarak bir işletmede birden fazla role (örneğin çalışan, müşteri, satıcı veya ilgili kişi) sahip olabilir. Rol, bağlama ve amaca bağlıdır. Burada, Contoso ve Fabrikam adlı iki hayali şirketten birkaç rol örneğine yer verilmektedir:

+ **Çalışan** – Bir personel. Örnek olarak bir Contoso personelini verebiliriz.
+ **Satıcı** – Bir tedarikçi kuruluş veya bir işletmeye mal veya servis sağlayan tek bir sahip anlamına gelir. Örneğin, Fabrikam Contoso'ya malzeme satıyorsa Fabrikam, Contoso'nun bir satıcısıdır.
+ **İlgili kişi** – İletişime geçilecek kişi. Örneğin, Contoso Fabrikam'dan malzeme satın alıyorsa Contoso'daki bir personel Fabrikam'daki ilgili kişiyle bağlantı kurar.
+ **Müşteri** – Bir şirketten bir şey satın alan kişi veya şirkettir. Örneğin, Contoso Fabrikam'dan malzeme satın alıyorsa o zaman Contoso bir Fabrikam müşterisidir.

Taraf modeli, özellikle bir taraf birden fazla rol oynadığında kuruluşlar ve kişiler arasındaki orta seviye ve karmaşık ilişkileri temsil etmek için kullanılır. Burada bazı genel örnekler verilmiştir:

+ Bir taraf hem müşteri hem de satıcı olabilir. Örneğin, Kuzey Amerika'da, Fabrikam Contoso'ya elektrik kabloları satar ve Contoso'dan montajlı hoparlörler satın alır. Avrupa'da, Fabrikam Contoso'ya parça satar ancak Contoso'dan herhangi bir şey satın almaz.
+ Bir taraf hem personel hem de müşteri olabilir. Örneğin, bir Contoso çalışanı Contoso'dan kişisel kullanım için elektronik aygıtlar satın alır.
+ Bir kişi ile bir kuruluş arasında çoğa çok (N:N) ilişkisi olabilir. Örneğin, Fabrikam, hizmet uzmanları sağlar ve bir yerleşim koordinatörü çalıştırır. Yerleşim koordinatörü, Fabrikam müşterilerinin birkaçından gelen iş istekleriyle uygun hizmet uzmanlarını eşleştirir. Contoso, Fabrikam'ın müşterilerinden biridir. Contoso'ya bir hizmet uzmanı gerektiğinde, Contoso yerleşim koordinatörüyle iletişim kurar ve koordinatör bu isteği yerine getirir. Yerleşim koordinatörü tüm müşterilerle ilgili istekleri işlediği için bir N:N ilişkisi söz konusudur.

Aşağıdaki görselde taraf için veri modeli gösterilmektedir:

![Taraf için veri modeli.](media/party-gab-image1.png)

> [!TIP]
> Yeni bir firma kaydı oluşturmaya çalıştığınızda, kaydı ada göre aramak için **Taraf** alanını kullanın. Bu şekilde, kaydı bulursanız yalnızca seçmeniz gerekir. Sistem, taraftan gelen tüm verileri otomatik olarak doldurur. Gerekli tüm alanları el ile ayarlamanız gerekmez. Bu davranış, kullanıma hazır bir şekilde gönderilen **Firma**, **İlgili Kişi** ve **Satıcı** sayfalarında bulunabilir.

Çift yazma, finans ve operasyon uygulamalarının tüm taraf rollerini desteklemez. Taraf rollerinin tam listesi için bkz. [Genel adres defterine genel bakış](../../../fin-ops/organization-administration/overview-global-address-book.md).

### <a name="global-address-book"></a>Genel adres defteri

Genel adres defteri, bir işte yer alan kuruluşların ve kişilerin posta ve elektronik adresler dizinidir.

Genel adres defteri gerektiği kadar posta adresi ve elektronik adres depolar ve işler. Örneğin, Fabrikam'ın 50 konumda benzin istasyonları olduğunu varsayalım. Her yerin farklı bir posta adresi, e-posta adresi ve telefon numarası vardır. Tüm iş harcamaları Ana benzin istasyonuna faturalandırılır, ancak doğrudan satın almayı talep eden belirli benzin istasyonuna sevk edilir. Genel adres defteri, ana benzin istasyonunu faturalama adresi, her bir benzin istasyonunu da Fabrikam için sevkiyat adresi olarak kaydeder. Adresler bir kez depolanabilir ve teklifler ve siparişler için gerektiğinde alınır.

İş bağlamına bağlı olarak, bir kişi veya organizasyon birden fazla rol üstlenebilir ve tüm roller için aynı posta adresi ve elektronik adres kullanılabilir. Bu durumda, bir roldeki adres değişikliği diğer rollerde de görünmelidir. Genel adres defteri, adresleri genel olarak depolar ve işler.

Aşağıdaki resimde genel adres defteri için veri modeli gösterilmektedir.

![Genel adres defteri için veri modeli.](media/party-gab-image2.png)

## <a name="contact"></a>İletişim

Müşteri etkileşimi uygulamalarında ilgili kişi bir kişidir. Ancak, **İlgili kişi** tablosu bir kişiyi, bir portal kullanıcısını, bir işletmeden müşteriye (B2C) müşterisini veya bir satıcıyı temsil edecek şekilde aşırı yüklenmiştir. Bu gösterim örtülüdür ve ilgili işlemleri araştırmadan farkı anlayamazsınız. **İlgili kişi** tablosu, **Firma** tablosuyla bire bir (1:1) ilişkisi olacak şekilde sınırlanmıştır. Taraf ve genel adres defteri modelinin bir parçası olarak çift yazma sınıflandırma için açık özellikler sunar ve Çift yazma ilgili kişi ve kuruluş (**Firma** varlığı veya **Satıcı** varlığı) arasında N:N ilişkilere izin verir.

İki tür **İlgili kişi** satırı vardır:

+ **Şeritli ilgili kişi** – **Şirket** alanında zorunlu değer bulunan **İlgili kişi** satırı.
+ **Şeritsiz ilgili kişi** – **Şirket** alanı boş olan **İlgili kişi** satırı.

**İlgili kişi** tablosu aşağıdaki tür satırları depolayabilir.

| Row türü | Tanım |
|----------|-------------|
| Müşteri olan (örneğin, satış yapılabilir ilgili kişi veya B2C müşterisi) kişi. | **Şirket** alanının boş olmadığı ve **Müşteri mi?** alanı **Evet** olarak ayarlanan şeritli bir ilgili kişi kaydı. |
| Satıcı olan bir kişi (örneğin, bir satıcı gibi bir tek sahip). | **Şirket** alanının boş olmadığı ve **Satıcı mı?** alanı **Evet** olarak ayarlanan şeritli bir ilgili kişi kaydı. |
| Hem müşteri hem de satıcı olan bir kişi | **Şirket** alanının boş olmadığı ve **Müşteri mi?** alanı **Evet** olarak ayarlanan ve **Satıcı mı?** alanı **Evet** olarak ayarlanan şeritli bir ilgili kişi kaydı. Bir kişi, bir ürün için üretici, başka bir ürün için tüketici olabilir. Hem finans ve operasyon uygulamaları hem de çift yazma bu ilişkiyi destekler. |
| Bir kuruluşun ilgili kişisi olan, ancak müşteri veya satıcı olmayan kişi | **Şirket** alanının boş olduğu ve **Müşteri mi?** alanı **Hayır** olarak ayarlanan ve **Satıcı mı?** alanı **Hayır** olarak ayarlanan şeritsiz bir ilgili kişi kaydı. |

## <a name="contact-for-party-table"></a>Taraf için ilgili kişi tablosu

**Taraf için ilgili kişi** tablosu, **Firma** satırları ve **İlgili kişi** satırları arasındaki N:N ilişkilerini depolar ve işler. Şeritli **ilgili kişi** satırlarını şeritsiz satırlardan filtreleyebilir ve yalnızca şeritsiz **ilgili kişi** satırlarını bir **Firma** veya **Satıcı** satırlarıyla ilişkilendirebilir.

Örneğin, Natasha Jones ve Miguel Reyes, bölgelerindeki çiftliklere hizmet sunan veterinerlerdir. Natasha, Seattle bölgesinde ve Miguel, Kent bölgesinde hizmet sunar. Customer Engagement uygulamasında, çiftlikler müşteri olarak, veterinerler ise ilgili kişiler olarak temsil edilir. Natasha için tek bir **ilgili kişi** kaydı, Natasha'nın birlikte çalıştığı tüm çiftlikler ile ilişkilidir. Benzer şekilde, Miguel için tek bir **İlgili kişi** kaydı, Miguel'in birlikte çalıştığı tüm çiftlikler ile ilişkilidir.

Bu ilişkiler, **taraf için ilgili kişi** tablosunda depolanır. Kullanıma hazır bir şekilde gönderilen **Firma**, **İlgili Kişi** ve **Satıcı** sayfalarıyla ilgili bilgilere şuradan erişebilirsiniz:

+ **Firma** sayfasında, bir veya daha fazla ilgili kişiyi **Firma** satırıyla ilişkilendirmek için **İlişkili İlgili Kişiler** sekmesini kullanabilirsiniz. Bu yöntemle bir kuruluş için ilgili kişi atarsınız. Ardından hesabın birincil ilgili kişisi olarak bir ilgili kişi seçebilirsiniz. **Hızlı oluştur** sayfasını kullanırsanız, yalnızca bir ilgili kişi seçebilirsiniz. **Satıcı** sayfasını kullanırken ve kayıt türü **Kuruluş** olduğunda davranış aynıdır.
+ **İlgili kişi** sayfasında; satır, müşteri, satıcı veya her ikisi (şeritli ilgili kişi) olduğunda, bir veya daha fazla ilgili kişi ilişkilendirmek için **İlişkili ilgili kişiler** sekmesini kullanabilirsiniz. Bu yöntemle B2C müşterisi veya satıcı için ilgili kişiler atarsınız. Ardından birincil ilgili kişisi olarak bir ilgili kişi seçebilirsiniz. **Hızlı oluştur** sayfasını kullanırsanız, yalnızca bir ilgili kişi seçebilirsiniz.
+ **İlgili kişi** sayfasında; satır, ilgili kişi (şeritsiz ilgili kişi) olduğunda, bir veya daha fazla müşteri veya satıcı ilişkilendirmek için **İlişkili Kuruluşlar** sekmesini kullanabilirsiniz. Bu yöntemle bir müşteri veya satıcıları temel ilgili kişiye atarsınız. Müşteri veya satıcı, bir kuruluş, bir kişi veya her ikisi olabilir. Belirli bir anda dört alandan yalnızca bir değer seçebilirsiniz:

    + **Taraf Kimliği** alanında bir değer seçerseniz, temel ilgili kişi seçilen tarafın tüm rollerine atanır.
    + **İlişkili ilgili kişi** alanında bir değer seçerseniz, **Kişi** türünde olan şeritli ilgili kişiyi seçersiniz.
    + **İlişkili Firma** veya **İlişkili satıcı** alanında bir değer seçerseniz, bir kuruluş seçersiniz.

    ![İlgili Kişi sayfasındaki İlişkili Kuruluşlar sekmesi.](media/party-gab-image3.png)

    Seçiminiz ne olursa olsun, ilişkilendirme taraf düzeyinde oluşturulur ve tarafın tüm rollerine uygulanır ve **Taraf için ilgili kişi** varlığı içinde depolanır.

> [!NOTE]
> Customer Engagement uygulamalarında **Taraf için ilgili kişi** tablosunun görünen adı **Müşteri/Satıcı için ilgili kişi**'dir.

Hem **Müşteri mi?** alanı hem de **Satıcı mı?** alanlarının **Hayır** olarak ayarlandığı bir **İlgili kişi** satırı açtığınızda, **İlişkili Kuruluşlar** sekmesi görüntülenir. Bir veya daha fazla müşteri ya da satıcı kuruluşu ilgili kişiyle ilişkilendirmek için bu sekmeyi kullanın.

**Müşteri mi?** alanı veya **Satıcı mı?** alanlarının birinin **Evet** olarak ayarlandığı bir **İlgili kişi** satırı açtığınızda, **İlişkili İlgili Kişiler** sekmesi görüntülenir. Bir veya daha fazla ilgili kişiyi ilişkilendirmek için bu sekmeyi kullanın.

## <a name="postal-addresses"></a>Posta adresleri

**Firma**, **İlgili Kişi** ve **Satıcı** formlarında yeni bir **Adresler** sekmesi sunuldu. Bu sekme, aşağıdaki görselde gösterildiği gibi, bir ızgara kullanılarak birden fazla posta adresini destekler.

![Posta adresleri için ızgara.](media/party-gab-image4.png)

Izgara aşağıdaki sütunları içerir:

+ **Posta Adresi Rolleri** – Posta adresinin amacı.
+ **Birincil** – Adresin birincil adres olup olmadığını gösteren değer.
+ **Adres Numarası** – Adres sırası.

İstediğiniz sayıda posta adresi oluşturmak için ızgaranın üzerindeki **Yeni Adres** düğmesini kullanabilirsiniz.

**Firma** sayfasının **Özet** sekmesindeki **Adres 1** ve **Adres 2** alanları sırasıyla **teslim** ve **fatura** adreslerine karşılık gelir.

![Posta adresleri için özet sekmesi.](media/party-gab-image5.png)

**İlgili kişi** sayfasının **Özet** sekmesindeki **Adres1**, **Adres 2** ve **Adres 3** alanları sırasıyla **İşletme**, **Teslim** ve **fatura** adreslerine karşılık gelir.

## <a name="electronic-addresses"></a>Elektronik adresler

**Firma**, **İlgili Kişi** ve **Satıcı** formlarında yeni bir **Elektronik Adresler** sekmesi sunuldu. Bu sekme, aşağıdaki görselde gösterildiği gibi, bir ızgara kullanılarak birden fazla elektronik adresi destekler.

![Elektronik adresler için ızgara.](media/party-gab-image6.png)

Izgara aşağıdaki sütunları içerir:

+ **Tür** – Elektronik adres türü.
+ **Birincil** Adresin birincil adres olup olmadığını gösteren değer.
+ **Amaç** – Elektronik adresin amacı.

İstediğiniz sayıda adresi oluşturmak için ızgaranın üzerindeki **Yeni Elektronik Adres** düğmesini kullanabilirsiniz.

Müşteri adayı uygunluk işlemi sırasında hem iş telefonu numarası hem de cep telefonu numarası sağlayabilirsiniz. **IsMobile=No** ise iş telefonu numarası birincil telefon numarası; **IsMobile=Yes** ise cep telefonu numarası ikincil telefon numarası olarak kabul edilir.

> [!TIP]
> Posta adreslerini ve elektronik adresleri yönetmek için **Hesap** ve **İlgili Kişi** formlarındaki **Adresler** ve **Elektronik Adresler** sekmelerini kullanın. Bu, adres verilerinin finans ve operasyon uygulamalarıyla eşitlenmesini sağlar.

## <a name="setup"></a>Ayar

1. Customer Engagement uygulama ortamınızı açın.

2. [Ayrılmış Dual-write Application Orchestration paketinde](separated-solutions.md) açıklandığı gibi, tüm önkoşul çözümlerini yükleyin.

3. [Çift Yazma Taraf ve Genel Adres Defteri Çözümleri](https://aka.ms/dual-write-gab)'ni yükleyin.

4. Finans ve Operasyon uygylamasını açın. Veri Yönetimi modülüne gidin ve Çift yazma sekmesini seçin. Çift yazma yönetim sayfası açılır.

5. [Çözüm Uygula](link-your-environment.md) işlevini kullanarak 2. adımda yüklenen çözümlerin her ikisini de uygulayın.

6. Artık gerekli olmadıklarından aşağıdaki eşlemeleri durdurun. Bunun yerine, `Contacts V2 (msdyn_contactforparties)` eşlemesini çalıştırın.

    + CDS İlgili Kişileri V2 ve İlgili Kişiler (müşteri ilgili kişilerini gösterir)
    + CDS İlgili Kişileri V2 ve İlgili Kişiler (satıcı ilgili kişilerini gösterir)

7. Aşağıdaki varlık eşlemeleri taraf işlevselliği için güncelleştirilir ve bu nedenle en son sürümün bu eşlemelere uygulanması gereklidir.

    Eşleme | Bu sürüme Güncelleştir | Değişiklikler
    ---|---|---
    `CDS Parties (msdyn_parties)`| 1.0.0.2 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Contacts V2 (msdyn_contactforparties)`| 1.0.0.6 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Customers V3 (accounts)` | 1.0.0.5 |`PartyNumber` ve taraflarla ilgili ad, kişisel ayrıntılar, posta adresi alanları ve elektronik ilgili kişi adresi alanları gibi alanlar kaldırıldı.
    `Customer V3 (contacts)` | 1.0.0.5 | `PartyNumber` ve taraflarla ilgili ad, kişisel ayrıntılar, posta adresi alanları ve elektronik ilgili kişi adresi alanları gibi alanlar kaldırıldı.
    `Vendors V2 (msdyn_vendors)` | 1.0.0.6 | `PartyNumber` ve taraflarla ilgili ad, kişisel ayrıntılar, posta adresi alanları ve elektronik ilgili kişi adresi alanları gibi alanlar kaldırıldı.
    `CDS Sales quotation headers (quotes)` | 1.0.0.7 | İlgili kişi, `ContactforParty` referansı ile değiştirildi.
    `Sales invoice headers V2 (invoices)` | 1.0.0.4 | İlgili kişi, `ContactforParty` referansı ile değiştirildi.
    `CDS Sales order headers (salesorders)` | 1.0.0.5 | İlgili kişi, `ContactforParty` referansı ile değiştirildi.
    `CDS Party postal address locations (msdyn_partypostaladdresses)` | 1.0.0.1  | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `CDS postal address history V2 (msdyn_postaladdresses)` | 1.0.0.2 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `CDS postal address locations (msdyn_postaladdresscollections)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Party Contacts V3 (msdyn_partyelectronicaddresses)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Complimentary Closings (msdyn_compliemntaryclosings)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Decision making roles (msdyn_decisionmakingroles)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Loyalty levels (msdyn_loyaltylevels)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Contact person titles (msdyn_salescontactpersontitles)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Personal character types (msdyn_personalcharactertypes)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Salutations (msdyn_salutations)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `Employment job functions (msdyn_employmentjobfunctions)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.
    `CDS Address roles (msdyn_addressroles)` | 1.0.0.0 | Bu sürümünün parçası olarak eklenen yeni bir eşlemedir.

8. Yukarıdaki eşlemeleri çalıştırmadan önce, aşağıdaki adımlarda açıklandığı şekilde tümleştirme anahtarlarını el ile güncelleştirmeniz gerekir. Sonra **Kaydet**'i seçin.

    | Eşleme | Anahtarlar |
    |-----|------|
    | Hesap |  accountnumber [Firma Numarası]<br>msdyn_company.cdm_companycode [Şirket (Şirket Kodu)] |
    | Başvur | msdyn_contactpersonid [Firma Numarası/İlgili Kişi Kimliği]<br>msdyn_company.cdm_companycode [Şirket (Şirket Kodu)] |
    | Müşteri/Satıcı için İlgili Kişi | msdyn_contactforpartynumber [Taraf Numarası için İlgili Kişi]<br>msdyn_associatedcompanyid.cdm_companycode [İlişkili Şirket (Şirket Kodu)] |
    | Satıcı | msdyn_vendoraccountnumber [Satıcı Firma Numarası]<br>msdyn_company.cdm_companycode [Şirket (Şirket Kodu)]|

9. Dataverse'de, yinelenen saptama kurallarının karakter sınırları 450 ile 700 karakter olarak artırıldı. Bu sınır, yinelenen saptama kurallarına bir veya daha fazla anahtar eklemenize olanak tanır. Aşağıdaki alanları ayarlayarak **Firmalar** tablosunun yinelenen saptama kuralını genişletin.

    | Alan | Değer |
    |-------|-------|
    | Kuruluş adı | Aynı firma adına sahip firmalar. |
    | Tanım | Firma Adı özniteliğinde aynı değere sahip olan firma kayıtlarını saptar. |
    | Temel Kayıt Türü | Hesap |
    | Eşleşen Kayıt Türü | Hesap |
    | Firma Adı (alan) | Tam Eşleşme |
    | Şirket (alan) | Tam Eşleşme |
    | İlişki Türü (alan) | Tam Eşleşme |
    | Taraf kodu (alan) | Tam Eşleşme |
    | Seçim (alan) | (boş) |

    ![Hesaplar için tekrarlanan kural.](media/duplicate-rule-1.PNG)

10. Aşağıdaki alanları ayarlayarak **İlgili Kişiler** tablosunun yinelenen saptama kuralını genişletin.

    | Alan | Değer |
    |-------|-------|
    | Kuruluş adı | Adı ve soyadı aynı olan ilgili kişiler. |
    | Tanım | Ad ve soyad alanlarında aynı değerlere sahip ilgili kişi kayıtlarını saptar. |
    | Temel Kayıt Türü | Başvur |
    | Eşleşen Kayıt Türü | Başvur |
    | Ad (alan) | Tam Eşleşme |
    | Soyad (alan) | Tam Eşleşme |
    | Şirket (alan) | Tam Eşleşme |
    | Taraf kodu (alan) | Tam Eşleşme |
    | Seçim (alan) | (boş) |

    ![İlgili kişiler için tekrarlanan kural.](media/duplicate-rule-2.PNG)

11. Varolan bir çift yazma kullanıcısıysanız, [Taraf ve genel adres defteri modeline yükseltme](upgrade-party-gab.md) bölümündeki talimatları izleyin ve verilerinizi yükseltin. **Bu adımı tamamlamadan 12. adıma geçmeyin.** Yeni bir ikili yazma kullanıcısı kullanıyorsanız, 12. adıma devam edin.

12. Varolan bir ikili yazma kullanıcısı iseniz, adım 11' i tamamlayın ve sonra da haritaları aşağıdaki sırada çalıştırın. Yeni bir ikili yazma müşterisiyseniz, doğrudan devam edebilirsiniz. Şu ifadeleri içeren bir mesaj görürseniz "Proje doğrulama başarısız oldu. Hedef alan eksik... " eşlemeyi açın ve **Tabloları Yenile**'yi seçin ve ardından eşlemeyi çalıştırın.

    Finans ve operasyon uygulaması | Müşteri etkileşimi uygulaması  
    ----------------------------|------------------------
    [CDS Tarafları](mapping-reference.md#220) | msdyn_parties
    [CDS posta adresi yerleşimleri](mapping-reference.md#234) | msdyn_postaladdresscollections
    [CDS posta adresi geçmişi V2](mapping-reference.md#235) | msdyn_postaladdresses
    [CDS Taraf posta adresi yerleşimleri](mapping-reference.md#233) | msdyn_partypostaladdresses
    [Taraf ilgili kişileri V3](mapping-reference.md#236) | msdyn_partyelectronicaddresses
    [Müşteriler V3](mapping-reference.md#101) | hesaplar
    [Müşteriler V3](mapping-reference.md#116) | ilgili kişiler
    [Satıcılar V2](mapping-reference.md#202) | msdyn_vendors
    [İlgili kişi unvanları](mapping-reference.md#223) | msdyn_salescontactpersontitles
    [Kapanış sözleri](mapping-reference.md#222) | msdyn_complimentaryclosings
    [Selamlamalar](mapping-reference.md#228) | msdyn_salutations
    [Karar verici roller](mapping-reference.md#224) | msdyn_decisionmakingroles
    [İstihdam iş görevleri](mapping-reference.md#225) | msdyn_employmentjobfunctions
    [Bağlılık programı düzeyleri](mapping-reference.md#226) | msdyn_loyaltylevels
    [Kişisel karakter türleri](mapping-reference.md#227) | msdyn_personalcharactertypes
    [İlgili Kişiler V2](mapping-reference.md#221) | msdyn_contactforparties
    [CDS satış teklifi başlığı](mapping-reference.md#215) | teklifler
    [CDS satış siparişi başlıkları](mapping-reference.md#217) | salesorders
    [Satış faturası başlıkları V2](mapping-reference.md#118) | faturalar
    [CDS Adresi rolleri](mapping-reference.md#301) | msdyn_addressroles

> [!NOTE]
> `CDS Contacts V2 (contacts)` eşlemesi, 1. adımda durdurduğunuz eşlemedir. Başka eşlemeler çalıştırmayı denediğinizde, bu 2 eşleme bağlılar listesinde görüntülenebilir. Bu eşlemeleri çalıştırmayın.
>
> Taraf ve genel adres defteri çözümü yüklüyse, `Microsoft.Dynamics.SCMExtended.Plugins.Plugins.LeadPrimaryContactPostCreate: QualifyLead of lead` adlı eklentiyi devre dışı bırakmanız gerekir. Taraf ve genel adres defteri çözümünü kaldırdıysanız eklentiyi yeniden etkinleştirmeniz gerekir.
>
> **Firma**, **İlgili kişi** ve **Satıcı** tablolarına dahil edilen `msdyn_*partynumber` alanı (tek satırlık metin alanı) bundan sonra kullanılmamalıdır. Etiket adında açıklık adına **(Kullanım dışı)** ön eki bulunmaktadır. Bunun yerine, **msdyn_partyid** alanını kullanın. Alan, **msdyn_party** tablosunda arama yapar.
>
> Tablo Adı | Eski alan | Yeni alan
> --------|-------|--------
> Hesap | `msdyn_partynumber` | `msdyn_partyid`
> Başvur | `msdyn_partynumber` | `msdyn_partyid`
> msdyn_vendor | `msdyn_vendorpartynumber` | `msdyn_partyid`

## <a name="templates"></a>Şablonlar

Tablo eşlemeleri koleksiyonu, aşağıdaki tabloda gösterildiği gibi taraf ve genel adres defteri etkileşimi için birlikte çalışır.

| Finans ve operasyon uygulaması | Müşteri etkileşimi uygulaması | Açıklama |
|----------------------------|-------------------------|-------------|
| [İlgili kişi unvanları](mapping-reference.md#223) | msdyn\_salescontactpersontitles |
| [Müşteriler V3](mapping-reference.md#101) | hesaplar |
| [Müşteriler V3](mapping-reference.md#116) | ilgili kişiler |
| [CDS Tarafları](mapping-reference.md#220) | msdyn\_parties |
| [CDS Taraf posta adresi yerleşimleri](mapping-reference.md#233) | msdyn\_partypostaladdresses |
| [CDS posta adresi geçmişi V2](mapping-reference.md#235) | msdyn\_postaladdresses |
| [CDS posta adresi yerleşimleri](mapping-reference.md#234) | msdyn\_postaladdresscollections |
| [CDS satış teklifi başlığı](mapping-reference.md#215) | teklifler |
| [CDS satış siparişi başlıkları](mapping-reference.md#217) | salesorders |
| [Kapanış sözleri](mapping-reference.md#222) | msdyn\_complimentaryclosings |
| [İlgili Kişiler V2](mapping-reference.md#221) | msdyn\_contactforparties |
| [Karar verici roller](mapping-reference.md#224) | msdyn\_decisionmakingroles |
| [İstihdam iş görevleri](mapping-reference.md#225) | msdyn\_employmentjobfunctions |
| [Bağlılık programı düzeyleri](mapping-reference.md#226) | msdyn\_loyaltylevels |
| [Taraf ilgili kişileri V3](mapping-reference.md#236) | msdyn\_partyelectronicaddresses |
| [Kişisel karakter türleri](mapping-reference.md#227) | msdyn\_personalcharactertypes |
| [Satış faturası başlıkları V2](mapping-reference.md#118) | faturalar |
| [Selamlamalar](mapping-reference.md#228) | msdyn\_salutations |
| [Satıcılar V2](mapping-reference.md#202) | msdyn\_vendors |
| [CDS Adresi rolleri](mapping-reference.md#301) |msdyn\_addressroles|

Daha fazla bilgi için, bkz. [Çift yazma eşleme başvurusu](mapping-reference.md).

## <a name="address-roles-as-a-multi-select-drop-down-list"></a>Çoklu seçim açılan listesi olarak adres rolleri
Posta adresi veya elektronik adres birden çok amaca hizmet edebilir. Örneğin, bir posta adresi hem faturalama adresi hem de teslimat adresi olarak hizmet verebilir. Bu gibi durumlarda, bir kullanıcı aşağıdaki çizimde gösterildiği gibi, açılan listeden hem **Fatura** hem de **Teslimat**'ı seçebilir. 

![Amaç/Rol açılan listesi.](media/purpose.png)

## <a name="known-issues-and-limitations"></a>Bilinen sorunlar ve sınırlamalar

+ Finans ve operasyon uygulamalarında, adresle birlikte bir müşteri oluşturup kaydettiğinizde, adres **Adres** tablosuyla eşitlenmeyebilir. Bu, çift yazma platformunun sıralama sorunundan kaynaklanır. Geçici çözüm olarak, önce müşteriyi oluşturun ve kaydedin. Sonra adresi ekleyin.
+ Finans ve operasyon uygulamalarında, bir müşteri kaydının birincil adresi olduğunda ve bu müşteri için yeni bir ilgili kişi oluşturduğunuzda, ilgili kişi kaydı ilişkili müşteri kaydından bir birincil adres devralır. Bu, satıcı ilgili kişisi için de gerçekleşir. Dataverse şu anda bu davranışı desteklemiyor. Çift yazma etkinleştirilirse, finans ve operasyon uygulamasından birincil adresle devralınan müşteri ilgili kişileri, adresiyle birlikte Dataverse'e eşitlenir.
+ Finans ve operasyon uygulamalarında, **İlgili Kişi Ekle** formundan bir kişi kaydı oluşturabilirsiniz. **İlgili kişiyi görüntüle** formundan yeni bir ilgili kişi oluşturmaya çalıştığınızda eylem başarısız olur. Bu, bilinen bir sorundur.

    ![İlgili Kişi Ekle ile ilgili bilinen sorun.](media/party-gab-contact-issue.png)

+ **İlk eşitleme**, **ContactForParty** üzerindeki **Kullanılabilirlik Başlangıç Tarihi** ve **Kullanılabilirlik Bitiş Tarihi** zaman alanlarını desteklemez çünkü DIXF değeri tamsayı yerine bir dizeye dönüştürür. Dönüştürme, `Cannot convert the literal '<say 08:00:00>' to the expected type edm.int32` hatasını tetikler.
+ Dataverse geçerlilik tarihini desteklemediği için çift yazma özelliğiyle bir finans ve operasyon uygulaması kullanarak ileri tarihli bir posta adresi giremezsiniz. Bir Finans ve operasyon uygulaması kullanarak geleceğe yönelik bir posta adresi girerseniz bu adres Dataverse'e tam olarak eşitlenir ve adresi kullanıcı arabiriminde hemen görürsünüz. Bu kayıtta yapılan güncelleştirmeler, güncel olmadığı ve geleceğe yönelik olduğu için finans ve operasyon uygulamasında bir hataya neden olur.

---
title: "Kayıt kodları"
description: "Bu konu, ayarlama ve kayıt kimlikleri kullanma hakkında bilgi sağlar."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Kayıt kodları

Bu konu, ayarlama ve kayıt kimlikleri kullanma hakkında bilgi sağlar.

Birçok ülke ve bölgelerin farklı düzenlemeler ve kayıt kayıt numaraları veya kimlikleri için gereksinimleri vardır. Bu konu, Avrupa farklı ülkelerde/bölgelerde taraflar için gerekli ayarları ve desteklenen kayıt türlerini işleme genel bakış sağlar. Tüm ülkeler/bölgeler kayıt numaraları farklı durum ofisleri tarafından sağlanan ilgili çeşitli ülkeye özgü işlevleri desteklemek için kendi gereksinimleri vardır. Sosyal Güvenlik numarası (SSK), vergi kimlik numarası (TIN) ve Avrupa KDV kimlik AB KDV kayıt numaraları örnekleri içerir. Bu özellik, hesap ülkeye özgü gereksinimleri bazı Avrupa ülkelerinde alarak tüm bölgelerde tüm ülkeler için birleşik bir çerçeve sağlar. Aşağıdaki bölümlerde genel ayarlama ve kayıt kimlikleri için kullanılan bilgi akışını açıklar.

## <a name="registration-type-creation"></a>Kayıt türü oluşturma
Kayıt Kimliği girmek için önce her taraf tabi olduğu kayıt numaraları farklı türleri için kayıt türlerini ayarlamanız gerekir. Git **kuruluş yönetim**&gt;**genel adres defteri**&gt;**kayıt türleri**&gt;**kayıt türleri** sayfa oluşturmak ve satıcılar, müşteriler, çalışanlar ve farklı ülkelerde/bölgelerde yasal varlıklar için kayıt türlerini yönetmek için.

|Alan                 |Açıklama      |
|------------------------------|----------------------------|                                                                           
| Dosya Adı                | Kayıt tipinin adı. |                                                                           
| Açıklama         | Kayıt tipi açıklaması. |
| Ülke/bölge      | Ülkenin/bölgenin benzersiz tanıtıcısı.|
| Vergi dairesi       | Kayıt türüyle ilişkili vergi dairesi.|
| Sınırlama:       | Vergi kayıt türü için uygulanan sınırlama türü: hiçbiri, kişi, kuruluş.|
| Biçim              | Kayıt türü için doğrulama biçimi.|
| Güncelleştirilebilir      | Kayıt türü için kayıt numarası girildiği doğrulandıktan sonra güncelleştirilebilir tanımlar.|
| Benzersiz              | Kayıt türü için kayıt numarası benzersizdir tanımlar. |
| Ülke/bölge için birincil | Bir taraf ile ilişkili olan ya da daha fazla adresleri özellikle ülke ve kayıt kimliği bu adresleri için geçerli bir adres ülke için birincil olarak atamanız gerekir. Sadece bir kimliği birincil olarak kaydedebilirsiniz. Yalnızca birincil adresi ülke için kayıt numarasının girilmesi durumunda tanımlar. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Kayıt tipi kayıt kategoriye atama
Kaydı kategorisi özellikle ülke vergi, Gümrük ve diğer amaçlar için kullanımı için onaylanan ülke kayıt tanımlayıcısıdır. Bu kategorideki farklı raporlarda belirli kayıt kimliği (denetleme basamaklarını vb. dahil) ve ekleme kayıt kimlik doğrulama kuralları tanımlar. Sayfayı kullanın **kuruluş yönetim**&gt;**genel adres defteri**&gt;**kayıt türleri**&gt;**kayıt kategorileri** kayıt türünü belirli bir ülke için desteklenen kayıt kategori atamak için.

| Alan            | Açıklama|
|-----------------------|----------------|
| Kayıt türü     | Kayıt ülke özellikle yazın.|
| Sınırlama:         | Kısıtlama türü vergi kayıt türü için geçerlidir: yok, kişi, kuruluş.|
| Kayıt kategorisi | Benzersiz kayıt tanımlayıcı ülkede kullanımı için onaylanmış. Tam liste kategoriler içinde desteklenen AX7.1 olan aşağıda. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Genel adres defteri kayıtları için kayıt kimliklerini girin
Müşteriler, satıcılar, kişiler, iş ilişkileri ve tüzel kişilikler için birleştirilmiş adres bilgilerini Microsoft Dynamics 365 işlemleri için Genel Adres Defteri'nde (GAB) içerir. Daha fazla bilgi için [genel adres defteri genel bakış](/dynamics365/operations/organization-administration/overview-global-address-book). Genel Adres Defteri içinde depolanan parti kayıtları, bir veya birden çok adres kaydı içerebilir. Bu adresler, fatura adresini veya sevkiyat gibi farklı amaçlar için kullanılır. Adres bilgileri müşteriler, satıcılar, çalışanları ve tüzel kişilikler için kayıt kodları ayarlayabilirsiniz. Parti (tüzel kişilik, satıcı, müşteri, çalışan) kayıt Numarasını girin ve ardından istediğiniz kayıt Bul **kayıt kimliklerini** ilgili taraf, tüzel kişilik, satıcı, müşteri, açmak için alt formlar üzerindeki **adreslerini yönetmek** sayfa. Üzerinde **Vergi kaydı** sekmesini tıklatın, **Ekle**ve ardından kayıt kimliği hakkında bilgi girin.

|Alan                |Açıklama                                                |
|---------------------|-----------------------------------------------------------|
| Kayıt türü   | Kayıt türü seçili ülke/bölge.     |
| Giriş kayıt numarası | Parti kayıt kimliği.                                |
| Açıklama         | Kayıt numarasının tanımı.               |
| Bölüm             | Kayıt numarası hakkında ek bilgi. |
| Veren kurum      | Kayıt numarası verilen yetki.        |
| Verildiği tarih         | Kayıt numarası için verilen tarih.              |
| Yürürlüğe giriş           | Kayıt numarası yürürlük tarihi.           |
| Bitiş          | Kayıt numarası için sona erme tarihi.          |

> [!NOTE]
> Vergi muafiyet numarası tüzel kişilik, satıcı, müşteri kaydından seçilebilir kimlikleri KDV kimliği için ilgili ve parti için girilen.

## <a name="search-for-records-by-registration-id"></a>Kayıt kayıt kimliği Ara
Parti kayıt kayıt kimliği temel alarak arama Partisi, tüzel kişilik, satıcı, müşteri ve çalışan ilişkili formlarda kullanılabilir. ' I **kayıt kimliği Ara** açmak için **kayıt kimliği arama ölçütü** sayfa. Arama ölçütlerini belirtin ve tıklatın **bulmak**. Sistem Genel Adres Defteri'ni ve ilişkili taraf kayıt türlerini seçili kayıtları görüntüler.

## <a name="supported-registration-categories"></a>Desteklenen kayıt kategorileri
Aşağıdaki tabloda işlemleri için Dynamics 365 desteklenen kayıt türlerini listeler. Microsoft Dynamics AX 2012 alanları kayıt kimlikleri için kullanıyorsanız, bu tablo bu alanlar da işlemleri kayıt kategorileri için Dynamics 365 eşleştirir.

| İşlem kaydı kategorisi için Dynamics 365         |Ülke/Bölge  | Dynamics AX 2012 terim/alan|
|---------------------------------------------------------------|---------------------|---------------------------------|
| VAT Kodu                                                        | Tüm ülkeler, Avrupa Birliği (AB)|  Vergi muafiyet numarası (Legislative türü AX2012 R3 vergisi kodu)|
| Kurum kodu (COID)                                          | Belçika Çek Cumhuriyeti Estonya Macaristan Letonya Litvanya Polonya İsviçre | Kuruluş numarası (EnterpriseNumber) kayıt numarası (RegNum\_W) sicil numarası (RegNum\_W) sicil numarası (RegNum\_W) sicil numarası (RegNum\_W) kuruluş kodu (EnterpriseCode) kayıt numarası (RegNum\_W) kullanıcı kimliği (UID AX2012 R3 içinde Legislative türü) |
| Şube kodu                                                     | Belçika            | Şube numarası (BranchNumber)|
| Spisová značka (kayıt numarası, Ajansı, bölüm verme) | Çek Cumhuriyeti     | Sayı (CommercialRegisterInsetNumber) Kept iç metin ticari ticari kayıt (CommercialRegisterSection) (CommercialRegister) bölümünü kaydetmek|
| Gümrük müşteri kodu                                           | Finlandiya | Gümrük müşteri numarası (CustomsCustomerNumber\_FI)|
| INN                                                           | Rusya Federasyonu| INN (Legislative türü AX2012 R3 olarak INN)|
| RRC                                                           | Rusya Federasyonu| RRC (Legislative türü AX2012 R3 içinde RRC)|
| OKDP                                                          | Rusya Federasyonu| OKDP (Legislative türü OKDP AX2012 R3 içinde)|
| OKPO                                                          | Rusya Federasyonu| OKPO (Legislative türü OKPO AX2012 R3 içinde)|
| RCOAD                                                         | Rusya Federasyonu| RCOAD (Legislative türü RCOAD AX2012 R3 içinde)|
| OGRN                                                          | Rusya Federasyonu| OGRN (Legislative türü OGRN AX2012 R3 içinde) |
| SNILS                                                         | Rusya Federasyonu| SNILS (Legislative türü SNILS AX2012 R3 içinde)|
| CIFTS                                                         | Rusya Federasyonu| CIFTS (Legislative türü CIFTS AX2012 R3 içinde)|

İşleme, gerekli Önkoşullar da dahil olmak üzere, kayıt kimlikleri hakkında daha fazla bilgi için aşağıdaki görev kayıtları KDV kimlik ömrü Hizmetleri (LCS) bakın:

-   KDV Kodu ayarlama
-   Satıcının KDV kimliği kayıt
-    KDV Kimliği kullanılarak taraf arama




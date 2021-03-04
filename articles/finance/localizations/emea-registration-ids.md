---
title: Kayıt kodları
description: Bu konu, kayıt kimliklerini ayarlama kullanma hakkında bilgi sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a0b978228e26ec70457a4bcb1c064070953909b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448964"
---
# <a name="registration-ids"></a>Kayıt kodları

[!include [banner](../includes/banner.md)]

Bu konu, kayıt kimliklerini ayarlama kullanma hakkında bilgi sağlar.

Birçok ülke ve bölgenin farklı düzenlemeleri ve kayıt numaralarını veya kimliklerini kaydetmek için gereksinimleri vardır. Bu konu, farklı Avrupa ülkeleri/bölgeleri için gerekli ayarların ve desteklenen kayıt türlerinin genel bir bakışını sağlamaktadır. Farklı devlet dairelerinden sağlanan kayıt numaralarıyla ilgili ülkeye özgü işlevsellikleri desteklemek için tüm ülkelerin/bölgelerin kendilerine ait gereksinimleri vardır. Örnekler arasında Sosyal Güvenlik numarası (SSK), vergi kimlik numarası (TIN) ve Avrupa KDV kimlik AB KDV kayıt numaraları bulunmaktadır. Bu özellik, bazı Avrupa ülkelerinin gereksinimlerini göz önünde bulundurarak, bir bölgedeki tüm ülkeleri birleştiren bir çerçeve sağlar. Aşağıdaki bölümler kayıt kimliklerini ayarlamak ve işlemek için genel akış hakkında bilgi sağlar.

## <a name="registration-type-creation"></a>Kayıt türü oluşturma
Kayıt kimlikleri girebilmeden önce, her tarafın tabi olduğu kayıt numaraları için kayıt türleri ayarlamak zorundasınız. Farklı ülkeler/bölgelerdeki satıcılar, müşteriler, çalışanlar ve tüzel kişilikler için kayıt türleri oluşturmak ve yönetmek için **Kuruluş yönetimi** &gt; **Genel adres defteri** &gt; **Kayıt türleri** &gt; **Kayıt türleri**  sayfasına gidin.

|Alan                 |Açıklama      |
|------------------------------|----------------------------|                                                                           
| Dosya Adı                | Kayıt türünün adı. |                                                                           
| Açıklama         | Kayıt türünün açıklaması. |
| Ülke/bölge      | Ülke/bölgenin benzersiz tanımlayıcı.|
| Vergi dairesi       | Kayıt türüyle ilişkili vergi dairesi.|
| Sınırlama:       | Vergi kayıt türüne uygulanan sınırlama türü: Hiçbiri, Kişi, Kuruluş.|
| Biçim              | Kayıt için doğrulama biçimi.|
| Güncelleştirilebilir      | Kayıt türü için kayıt numarasının girildikten sonra güncelleştirilebileceğini tanımlar.|
| Benzersiz              | Kayıt türü için kayıt numarasının benzersiz olup olmadığını tanımlar. |
| Ülke/bölge için birincil | Bir taraf belirli bir ülkede bir ya da birden fazla kayıt numarası ile ilişkilendirildiyse, kayıt numarası bu adreslerin tümü için geçerli olacaktır, bu yüzden de bir adresi ülke için birincil olarak atamanız gerekir. Yalnızca bir kimliği birincil olarak kaydedebilirsiniz. Kayıt numarasının yalnızca birincil ülke adresi için girilip girilemeyeceğini tanımlar. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Bir kayıt kategorisine bir kayıt türü atama
Kayıt kategorisi ülke/bölge kayıt tanımlayıcısıdır, belirli bir ülke/bölge için vergi, gümrük ve diğer amaçlar için onaylanmıştır. Belirli bir kayıt kimliğinin kategori belirleyici doğrulama kuralları (denetleme basamakları vb. dahil) ve farklı raporlardaki ekleme kayıt kimliği. **Kuruluş yönetimi** &gt; **Genel adres defteri** &gt; **Kayıt türleri** &gt; **Kayıt kategorileri** sayfasını kullanarak belirli bir ülkenin kayıt türünü desteklenen kayıt kategorisine ekleyin.

| Alan            | Açıklama|
|-----------------------|----------------|
| Kayıt türü     | Belirli ülke/bölgedeki kayıt türü.|
| Sınırlama:         | Vergi kayıt türüne uygulanan sınırlama türü: Hiçbiri, Kişi, Kuruluş.|
| Kayıt kategorisi | Ülkede kullanılan benzersiz kayıt kimlik tanımlayıcısı. Desteklenen kategorilerin tam listesi bu konunun ilerleyen kısımlarında gösterilmektedir. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Genel adres defteri kayıtları için kayıt kimlikleri girin

Genel adres defteri (GAB) müşteriler, satıcılar, bağlantılar, iş ilişkileri ve tüzel varlıklar için birleştirilmiş adres bilgilerini içerir. Daha fazla bilgi için [Genel adres defterine genel bakış](../../fin-and-ops/organization-administration/overview-global-address-book.md). Genel adres defterinde depolanan taraf kayıtları, bir veya birden fazla adres kaydı içerebilir. Bu adresler farklı amaçlar için kullanılabilir; örneğin faturalama veya teslimat. Müşteriler, satıcılar, çalışanlar ve tüzel varlıklar için adres bilgileri için kayıt kimlikleri ayarlayabilirsiniz. Kayıt kimliğini girmek istediğiniz taraf (tüzel varlık, satıcı, müşteri, çalışan) kaydını bulun ve daha sonra **Kayıt kimlikleri** forumuna taraf, tüzel varlık, satıcı, müşteri, satıcı ile ilgili **Adresleri yönet** sayfasında tıklayın. **Vergi kaydı** sekmesinde, **Ekle** üzerine tıklayın ve kayıt kimliği hakkında aşağıdaki bilgiyi girin.


|Alan                |Açıklama                                                |
|---------------------|-----------------------------------------------------------|
| Kayıt türü   | Seçili ülke/bölgedeki kayıt türü.     |
| Giriş kayıt numarası | Taraf kayıt kimliği.                                |
| Açıklama         | Kayıt numarasının açıklaması.               |
| Bölüm             | Kayıt numarası hakkında ek bilgi. |
| Veren kurum      | Kayıt numarasını veren daire.        |
| Verildiği tarih         | Kayıt numarasının verilme tarihi.              |
| Yürürlüğe giriş           | Kayıt numarasının geçerlilik tarihi.           |
| Bitiş          | Kayıt numarası için bitiş tarihi.          |

> [!NOTE]
> Tüzel kişiliğin, satıcının, müşterinin vergi muafiyet numarası, taraf için girilen vergi numarasıyla ilgili kayıt kimliklerinden seçilebilir.

## <a name="search-for-records-by-registration-id"></a>Kayıt kimliklerine göre kayıt ara
Kayıt kimliklerine dayalı taraf kaydı arama taraf, tüzel kişilik, satıcı, müşteriler ve çalışan için formlarda arama yapın. **Kayıt kimlik arama kriteri sayfasını açmak için** **Kayıt kimlik aramasına** tıklayın. Kriteri belirtin ve **Bul** üzerine tıklayın. Sistem seçili kayıtları, ilişkili türdeki taraf kayıtlarını genel adres defterinden görüntüler.

## <a name="supported-registration-categories"></a>Desteklenen kayıt kategorileri
Aşağıdaki tabloda, desteklenen kayıt türleri listelenmiştir. Kayıt kimlikleri için Microsoft Dynamics AX 2012 alanlarına aşinaysanız, bu tablo bu alanları da Dynamics 365 Finance kayıt kategorilerine eşleştirir.

| Finance Kayıt kategorisi         |Ülke/Bölge  | Dynamics AX 2012 terim/alan|
|---------------------------------------------------------------|---------------------|---------------------------------|
| VAT Kodu                                                        | Tüm Avrupa Birliği (AB) ülkeleri|  Vergi muafiyeti numarası (yasal Vergi Kimliği Türü AX 2012 R3'te)|
| Kurum kodu (COID)                                          | Belçika Çek Cumhuriyeti Estonya Macaristan Letonya Litvanya Polonya İsviçre | Kuruluş numarası (EnterpriseNumber) Kayıt numarası (RegNum\_W) Kayıt numarası (RegNum\_W) Kayıt numarası (RegNum\_W) Kayıt numarası (RegNum\_W) Kuruluş kodu (EnterpriseCode) Kayıt numarası (RegNum\_W) UID (AX 2012 R3 yasal UID tipi) |
| Şube kodu                                                     | Belçika            | Şube numarası (BranchNumber)|
| Spisová značka (Kayıt numarası, veren ajans, bölüm) | Çek Cumhuriyeti     | Sayı (CommercialRegisterInsetNumber) Ticari kayıtta tutulur (CommercialRegisterSection) (CommercialRegister) ticari kaydın bölümü|
| Gümrük müşteri kodu                                           | Finlandiya | Gümrük müşteri numarası (CustomsCustomerNumber\_FI)|
| INN                                                           | Rusya Federasyonu| INN (Yasal INN türü AX 2012 R3)|
| RRC                                                           | Rusya Federasyonu| RRC (Yasal RRC türü AX 2012 R3)|
| OKDP                                                          | Rusya Federasyonu| OKDP (Yasal OKDP türü AX 2012 R3)|
| OKPO                                                          | Rusya Federasyonu| OKPO (Yasal OKPO türü AX 2012 R3)|
| RCOAD                                                         | Rusya Federasyonu| RCOAD (Yasal türü RCOAD AX 2012 R3 içinde)|
| OGRN                                                          | Rusya Federasyonu| OGRN (Yasal OGRN türü AX 2012 R3) |
| SNILS                                                         | Rusya Federasyonu| SNILS (Yasal türü SNILS AX 2012 R3 içinde)|
| CIFTS                                                         | Rusya Federasyonu| CIFTS (Yasal türü CIFTS AX 2012 R3 içinde)|
| Pasaport                                                      | İspanya             | Pasaport|
| Resmi kimlik belgesi                              | İspanya             | Resmi kimlik belgesi|
| İkametgah belgesi                                         | İspanya             | İkametgah belgesi|
| Diğer kimlik belgesi                                 | İspanya             | Diğer kimlik belgesi|
| Censused değil                                                  | İspanya             | AX 2012 R3'te yoktur|


Gerekli ön koşullar dahil kayıt kimlikleri işleme için, Lifecycle Services (LCS) içinde KDV kimliği için aşağıdaki görev kayıtlarına bakın:

-   KDV Kodu ayarlama
-   Satıcının KDV kimlik kaydı
-    KDV Kimliği kullanılarak taraf arama






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "Kayıt kodları"
description: "Bu konu, kayıt kimliklerini ayarlama kullanma hakkında bilgi sağlar."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fc4a56eceb75673b7a044bd8392f8d0cc675e869
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="registration-ids"></a>Kayıt kodları

[!include[banner](../includes/banner.md)]


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
| Kayıt kategorisi | Ülkede kullanılan benzersiz kayıt kimlik tanımlayıcısı. AX7.1'de desteklenen kategorilerin tüm listesi aşağıdadır: |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Genel adres defteri kayıtları için kayıt kimlikleri girin
Microsoft Dynamics 365 for Operations içindeki Genel adres defteri (GAB), müşteriler, satıcılar, bağlantılar, iş ilişkileri ve tüzel varlıklar için birleştirilmiş adres bilgilerini içerir. Daha fazla bilgi için [Genel adres defterine genel bakış](/dynamics365/operations/organization-administration/overview-global-address-book). Genel adres defterinde depolanan taraf kayıtları, bir veya birden fazla adres kaydı içerebilir. Bu adresler farklı amaçlar için kullanılabilir; örneğin faturalama veya teslimat. Müşteriler, satıcılar, çalışanlar ve tüzel varlıklar için adres bilgileri için kayıt kimlikleri ayarlayabilirsiniz. Kayıt kimliğini girmek istediğiniz taraf (tüzel varlık, satıcı, müşteri, çalışan) kaydını bulun ve daha sonra **Kayıt kimlikleri** forumuna taraf, tüzel varlık, satıcı, müşteri, satıcı ile ilgili **Adresleri yönet** sayfasında tıklayın. **Vergi kaydı** sekmesinde, **Ekle** üzerine tıklayın ve kayıt kimliği hakkında aşağıdaki bilgiyi girin.

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
Aşağıdaki tablo, Dynamics 365 for Operations içerisindeki desteklenen kayıtları listeler. Kayıt kimlikleri için Microsoft Dynamics AX 2012 alanlarına aşinaysanız, bu tablo bu alanları da Dynamics 365 for Operations kayıt kategorilerine eşleştirir.

| Dynamics 365 for Operations Kayıt kategorileri         |Ülke/Bölge  | Dynamics AX 2012 terim/alan|
|---------------------------------------------------------------|---------------------|---------------------------------|
| VAT Kodu                                                        | Tüm Avrupa Birliği (AB) ülkeleri|  Vergi muafiyeti numarası (yasal Vergi Kimliği Türü AX2012 R3'te)|
| Kurum kodu (COID)                                          | Belçika Çek Cumhuriyeti Estonya Macaristan Letonya Litvanya Polonya İsviçre | Kuruluş numarası (EnterpriseNumber) Kayıt numarası (RegNum\_W) Kayıt numarası (RegNum\_W) Kayıt numarası (RegNum\_W) Kayıt numarası (RegNum\_W) Kuruluş kodu (EnterpriseCode) Kayıt numarası (RegNum\_W) UID (AX2012 R3 yasal UID tipi) |
| Şube kodu                                                     | Belçika            | Şube numarası (BranchNumber)|
| Spisová značka (Kayıt numarası, veren ajans, bölüm) | Çek Cumhuriyeti     | Sayı (CommercialRegisterInsetNumber) Ticari kayıtta tutulur (CommercialRegisterSection) (CommercialRegister) ticari kaydın bölümü|
| Gümrük müşteri kodu                                           | Finlandiya | Gümrük müşteri numarası (CustomsCustomerNumber\_FI)|
| INN                                                           | Rusya Federasyonu| INN (Yasal INN türü AX2012 R3)|
| RRC                                                           | Rusya Federasyonu| RRC (AX2012 R3 içindeki yasal türü RRC)|
| OKDP                                                          | Rusya Federasyonu| OKDP (Yasal OKDP türü AX2012 R3)|
| OKPO                                                          | Rusya Federasyonu| OKPO (Yasal OKPO türü AX2012 R3)|
| RCOAD                                                         | Rusya Federasyonu| RCOAD (Yasal türü RCOAD AX2012 R3 içinde)|
| OGRN                                                          | Rusya Federasyonu| OGRN (Yasal OGRN türü AX2012 R3) |
| SNILS                                                         | Rusya Federasyonu| SNILS (Yasal türü SNILS AX2012 R3 içinde)|
| CIFTS                                                         | Rusya Federasyonu| CIFTS (Yasal türü CIFTS AX2012 R3 içinde)|

Gerekli ön koşullar dahil kayıt kimlikleri işleme için, Lifecycle Services (LCS) içinde KDV kimliği için aşağıdaki görev kayıtlarına bakın:

-   KDV Kodu ayarlama
-   Satıcının KDV kimlik kaydı
-    KDV Kimliği kullanılarak taraf arama






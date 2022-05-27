---
title: Satıcıları işe alma
description: Bu konu yeni satıcıları işe alma sürecini açıklar. Bu işlem sırasında çeşitli roller için gerekli olan eylemleri açıklar.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, SysUserRequestListPage, VendRequestListPage, VendRequestCompanyProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 396b3c4622c612fa082796080aa230a0d693ce4f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671014"
---
# <a name="onboard-vendors"></a>Satıcıları işe alma

[!include [banner](../includes/banner.md)]

---

Microsoft Dynamics 365 Supply Chain Management'ta satıcıyı temsil eden bir kişiden alınan bilgiler temel alınarak yeni satıcılar işe alınabilir ve satıcı olarak kaydedilebilir.

Bu işlem aşağıdaki adımlardan oluşur ve sistemde çeşitli rollerin eylem gerçekleştirmesini gerektirir.

1. **Veri yönetimi OData** – Varlığı içe aktarma - İlk talep satıcı adayı kayıt talebidir. Genellikle, bu istek müşteri tarafından barındırılan ve anonim erişime izin veren bir web sitesi gibi bir kaynaktan gelir. Satıcılar satıcı adı, doğrulama, kuruluş numarası ve ilgili kişinin adı ve e-posta adresi gibi temel bilgileri sağlayarak kaydolabilir. Talepler Veri yönetimi arabirimi aracılığıyla içe aktarılır.
2. **Aday satıcı kaydı talebi liste sayfası** - Aday satıcı kaydı talebinde sağlanan bilgileri temel alarak bir tedarik uzmanı satıcının işe alınıp alınmayacağına karar verir. Tedarik uzmanı **Aday satıcı kaydı talepleri** liste sayfasında gelen talebi görür.
3. **Kullanıcı sağlama iş akışı** - Bir tedarik uzmanı gelen talepteki verileri doğrulayıp işe alma işlemine devam etmeye karar verdiğinde kullanıcı talebi iş akışı yeni kullanıcı sağlar ve ilgili kişiyi doğrulanmış bir Microsoft Dynamics 365 kullanıcı olarak kabul etmek üzere bir davet e-postası gönderir.
4. **Satıcı kayıt sihirbazı** - Satıcının ilgili kişisi yeni kullanıcı hesabını kullanarak oturum açar. Adres, işletme bilgileri, tedarik kategorileri ve soru formu yanıtları gibi bilgileri sağlamak üzere satıcı kaydı sihirbazını tamamlar.
5. **Onay iş akışı** - Kayıt bilgilerini içeren bir satıcı talebi oluşturulur. Bu satıcı talebi bir iş akışına gönderilir ve inceleme ve onay için yönlendirilir.
6. **Satıcı ana verileri oluşturma ve kullanıcı rolü değişikliği** - Satıcı talebi onaylandıktan sonra satıcı kaydı oluşturulur. Satıcı ilgili kişisinin kullanıcı hesabına satıcı işbirliği için izin sağlanır veya devre dışı bırakılır.

Aşağıdaki tablo işleme dahil olan adımları ve rolleri gösterir.

| Rol ve "işlem"       | Veri yönetimi OData – Varlık içe aktarma | Aday satıcı kaydı talebi liste sayfası | Kullanıcı sağlama iş akışı | Satıcı kaydı sihirbazı | Onay iş akışı | Satıcı ana verileri oluşturma ve kullanıcı rolü değişikliği |
|--------------------------|---|---|---|---|---|---|
| Sistem                   | Yeni bir satıcı için talep içe aktarılır. | | | | | Satıcı teklifi kabul edildikten sonra satıcı kaydı oluşturulur. |
| Tedarik uzmanı | | İşe alma işlemini başlatın. | | | Satıcı talebini inceleyin ve kabul edin veya reddedin. | |
| Yönetici            | | | Supply Chain Management ve Microsoft Azure. için bir kullanıcı oluşturun. | | | |
| Satıcı ilgili kişisi    | | | İlgili kişiye e-posta gönderin. | Satıcı bilgilerini kaydedin. | | |

Satıcı işe alım sürecinin kısa bir tanıtımı için YouTube'daki şu kısa videoyu izleyin: [Finance and Operations'ta yeni bir satıcı nasıl işe alınır?](https://www.youtube.com/watch?v=0KUc3AGaTKk).

## <a name="importing-the-prospective-vendor-registration-request"></a>Aday satıcı kaydı talebini içe aktarma

Aday satıcı kaydı talebi Supply Chain Management'taki bir varlıktır. Sistemi verileri bu varlık aracılığıyla içeri aktarmak üzere ayarlayabilirsiniz. 

Aşağıdaki tablo bu varlığın içerdiği ve içe aktarılabilecek bilgileri gösterir.

| Alan                        | Tanım |
|------------------------------|-------------|
| Satıcı adı                  | Satıcının adı. |
| İş gerekçesi       | Satıcı talebinin nedeni veya nedenleri. |
| Organizasyon numarası          | Resmi olarak bilinen bir kayıt numarası. |
| İş kolu             | Satıcının faaliyet gösterdiği iş kolu. |
| İlgili kişinin adı  | Satıcı bilgilerini kaydetmek üzere davet edilecek kişinin adı. |
| İlgili kişinin ikinci adı | Satıcı bilgilerini kaydetmek üzere davet edilecek kişinin ikinci adı. |
| İlgili kişinin soyadı.   | Satıcı bilgilerini kaydetmek üzere davet edilecek kişinin soyadı. |
| İlgili kişinin e-posta adresi       | Supply Chain Management'ta yeni bir kullanıcı oluşturmak için kullanılacak ve kiracının Azure Active Directory (Azure AD) hesabına kaydedilecek e-posta adresi. |
| Gönderilme tarihi               | Talebin harici sistemde oluşturulduğu tarih. |
| Tüzel kişilik                 | Satıcının bir satıcı olmayı talep ettiği tüzel kişilik. Bu değer Supply Chain Management'ta kaydedilmiş bir tüzel kişilik kodu olmalıdır. İçe aktarma işlemiyle herhangi bir değer alınmazsa, Tedarik ve kaynak atama parametrelerinden bir değer uygulanır. |
| Satıcı türü                  | Satıcı bir kuruluş veya kişi olabilir. Satıcı türü satıcının son olarak nasıl oluşturulacağını belirler. |

Aday satıcı kayıt talebi içe aktarıldıktan sonra **Aday satıcı kaydı talebi** liste sayfasında görünür. Bu liste sayfasından tedarik uzmanı bir kullanıcıyı davet edebilir. Kullanıcı sağlama için kullanıcı talebi iş akışına gönderilir.

## <a name="submitting-a-prospective-vendor-user-request"></a>Aday satıcı kullanıcısı talebini gönderme

Aday satıcı kullanıcısı talebinin amacı ilk isteği gönderen kişiye provizyon sağlamaktır; böylece söz konusu aday müşteri kaydı talebinde sağlanan e-posta adresini kullanarak Supply Chain Management'ta oturum açabilir.

Aday satıcı kullanıcısı talebi kullanıcı talebi iş akışı tarafından işlenir. Bu iş akışı Azure AD B2B işbirliği aracılığıyla iletişim kurar. Supply Chain Management'ta uygun güvenlik ayarlarına sahip bir kullanıcı oluşturur.

Ayarlanan yeni kullanıcılar aşağıdaki güvenlik rollerine sahiptir:

- Sistem harici kullanıcısı
- Satıcı adayı (harici)

Yeni kullanıcı, kullanıcı talebi iş akışı tarafından oluşturulan bir e-posta alır. Bu e-posta kullanıcıyı sistemde oturum açmaya davet eder.

E-posta yapılandırma ve genel olarak iş akışı hakkında bilgi için [Satıcı işbirliği ayarlama ve sürdürme](set-up-maintain-vendor-collaboration.md) konusundaki kullanıcı talebi iş akışının açıklamasına bakın.

## <a name="vendor-registration"></a>Satıcı kaydı

Supply Chain Management'ta oturum açan aday satıcı kullanıcısı, satıcı bilgilerini girebileceği satıcı sihirbazının ilk sayfasını görür.

Sihirbaz satıcı talebi yapılandırmasını gösterir. Satıcının iş yaptığı ülke veya bölge sihirbazda hangi bilgilerin isteneceğini ve hangi bilgilerin zorunlu olduğunu belirler.

Satıcı talebi yapılandırma hakkında daha fazla bilgi için bkz. [Satıcı işbirliği ayarlama ve sürdürme](set-up-maintain-vendor-collaboration.md). Aşağıdaki tabloda sihirbazın sayfalarına genel bakış ve her sayfanın amacı verilmektedir.

| Sayfa                       | Tanım |
|----------------------------|-------------|
| Ülke/bölge             | Ülke veya bölge kalan sihirbaz sayfalarına uygulanacak satıcı talebi yapılandırmasını belirler. Ayrıca **Vergi durumu** aramasındaki değerleri de belirler. |
| Hüküm ve koşullar       | Bu sayfa satıcı talebi yapılandırmasına bağlı olarak kullanılabilir. Kullanılabilir durumdaysa, kullanıcının devam etmek için hüküm ve koşulları kabul etmesi gerekir. |
| Satıcı bilgileri         | Bu sayfa, orijinal aday satıcı kayıt talebinden otomatik olarak girilen satıcı adını içerir. Ayrıca kuruluş numarası, satıcının telefon numarası, faks numarası, e-posta adresi ve satıcının çeşitli amaçlarla kullanılan adreslerini içerir. |
| İlgili kişi bilgileri | Bu sayfa, orijinal aday satıcı kayıt talebinden otomatik olarak girilen ilgili kişi adını içerir. Ayrıca ilgili kişisinin telefon numarasını, e-posta adresini ve ilgili kişinin çeşitli amaçlarla kullanılan adreslerini içerir. |
| İş bilgileri       | Bu sayfa vergi tescil numaralarını (çeşitli ülkeler veya bölgeler için) ve çalışanların sayısını içerir. Ayrıca işletmenin azınlıklara ait olup olmadığını da belirtir. |
| Tedarik kategorileri     | Bu sayfa satıcının onay için talep ettiği tedarik kategorilerini içerir. Kullanıcı tedarik kategorisi hiyerarşisinden kategorileri seçebilir. Hiyerarşide gösterilen düzey sayısını **Tedarik ve kaynak atama** &gt; **Kurulum** altındaki **Tedarik ve kaynak atama parametleri** &gt; **Satıcı işbirliği**'nden yapılandırabilirsiniz. |
| Soru formları             | Sihirbaz satıcı için bir soru formu kümesi içerebilir. Sihirbazda görünen soru formları satıcı talebinde veya tedarik kategorisine göre yapılandırılır. Soru formları tedarik kategorisine göre yapılandırılırsa, satıcının onay için istediği tedarik kategorileri soru formunun sihirbazda görüntülenip görüntülenmeyeceğini belirler. **Tedarik kategorileri** sayfasında, ilgili kategori altından bir soru formu ekleyebilir ve faaliyet türünü **Satıcı işe alma** olarak ayarlayabilirsiniz. |

Aday satıcı kullanıcısı satıcı kaydı sihirbazını tamamladığında, satıcı talebi oluşturulur.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Bir satıcı talebini el ile veya otomatik olarak gönderme

Bir satıcı talebi taslak olarak oluşturulabilir ve el ile bir iş akışına gönderilebilir. Alternatif olarak, satıcı talebi satıcı kaydı sihirbazı tamamlandığında bir iş akışına otomatik olarak gönderilebilir. Örneğin bir tedarik uzmanının talebin iş akışına gönderilmeden önce bir onay sürecine yönlendirilmesinin gerekli olup olmadığını değerlendirmek istemesi durumunda bir talep el ile gönderilebilir.

- **Tedarik ve kaynak atama parametreleri** &gt; **Satıcı işbirliği**'ni ve ardından **Aday satıcı kaydını iş akışına otomatik gönder**'i seçerek, satıcı talebini satıcı kaydı sihirbazı tamamlandığında iş akışına otomatik olarak gönderilmek üzere yapılandırabilirsiniz.

## <a name="vendor-requests"></a>Satıcı talepleri

Satıcı talepleri **Satıcı işbirliği kullanıcı talepleri** sayfasında bulunur.

Bir satıcı talebi aday satıcı kullanıcısının satıcı kayıt sihirbazında girdiği bilgileri içerir.

Talep satıcı bilgilerini incelemenize ve satıcının Supply Chain Management'ta kayıtlı bir satıcı olması gerekip gerekmediğine karar vermenize olanak tanır.

Satıcı talebi bir iş akışına gönderilmeli ve ilgili gözden geçirenlere ve onaylayanlara yönlendirilmelidir. İş akışlarını ayarlama hakkındaki teme bilgiler için bkz. [Tedarik ve kaynak atama iş akışları](procurement-sourcing-workflows.md).

Aşağıdaki tabloda satıcı taleplerinin sahip olabileceği durumlar gösterilmektedir.

| Durum                     | Tanım |
|----------------------------|-------------|
| Taslak                      | Satıcı talebi henüz gönderilmedi. |
| Talep gönderildi          | Satıcı talebi gönderildi ve iş akışındaki ilk adım işleniyor. |
| Bekleyen inceleme             | Bir iş akışı görevinde birden çok gözden geçiren varsa, bir gözden geçiren satıcı talebini gözden geçirme görevini kabul edip gözden geçirmeyi tamamlayabilir. Yalnızca bir gözden geçiren varsa, bu katılımcı gözden geçirmeyi iş akışı eyleminde **Tamamlandı**'yı seçerek tamamlayabilir. İş maddesini önceden kabul etmesi gerekmez. |
| Talep onay bekliyor   | Satıcı talebi onay için katılımcılara yönlendirilmiştir ve ek bilgi talep etme seçeneği bulunur. Ek bilgi talebi iş maddesinin yeniden gönderene yönlendirilmesine neden olur. Satıcı talebi bu durumdayken de onaylanabilir veya reddedilebilir. |
| Başvuru değişikliği talebi | Ek bilgiler onaylayan tarafından talep edilir ve satıcı talebi satıcı talebini gönderen kişiye yönlendirilir. Gönderen gerekli bilgileri ekleyip satıcı talebini yeniden gönderebilir. Satıcı talebi yeniden gönderilirse, durum tekrar **Talep onay bekliyor** durumuna döner. |
| Talep onaylandı           | Bu durum son durumdur. |
| Talep reddedildi           | Bu durum son durumdur. |

## <a name="approving-a-vendor-request"></a>Satıcı talebini onaylama

Bir satıcı talebi onaylandığında bir satıcı hesabı oluşturulur ve durum hem başlangıçtaki aday satıcı kayıt talebinde hem de satıcı talebinde **Onaylandı** olarak görüntülenir.

Satıcı talebini onaylamadan önce **Yeni satıcı** sayfasında **Genel** hızlı sekmesinde, bir satıcı grubu seçmek için **Satıcı grubu**'nu seçin.

Aday satıcı kullanıcısının Supply Chain Management'a satıcıyı temsil eden satıcı işbirliği kullanıcısı olarak erişmesi gerekirse satıcı işbirliği erişimi iznini **Evet** olarak ayarlayın. Aday satıcının kayıt olmak için kullandığı kullanıcı hesabını devre dışı bırakmak için bu izni **Hayır** olarak ayarlayın.

Satıcı işbirliğine erişim izni **Evet** olarak ayarlanırsa, satıcı talebi onaylandığında, kullanıcının rollerini kullanıcı **Dış roller**'de **Satıcı** türü için tanımlanan rollere sahip olacak şekilde değiştirmek için bir talep gönderilir. Bu izin **Hayır** olarak ayarlanırsa, satıcı talebi onaylandığında, kullanıcıyı devre dışı bırakmak için bir talep gönderilir. Bu durumda, kullanıcı talebini devre dışı bırakmak üzere bir iş akışı ayarlanması gerekir.

Satıcı talebi onaylandığında bir satıcı hesabı oluşturulması için, satıcı taleplerinden satıcılar oluşturma numara serisinin **Otomatik** olarak ayarlanması gerekir.

Satıcı işbirliği kullanıcısının erişim izinlerine genel bakış için bkz. [Satıcı işbirliği ayarlama ve sürdürme](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Satıcı talebini reddetme

Bir satıcı talebi reddedilirse, satıcı talebinde bir reddetme nedeni seçilmesi gerekir.

Bir satıcı talebi reddedildiğinde, satıcıyı devre dışı bırakmak için bir talep gönderilir. Bu durumda, kullanıcı talebini devre dışı bırakmak üzere bir iş akışı ayarlanması gerekir. Daha fazla bilgi için bkz. [Satıcı işbirliğini ayarlama ve sürdürme](set-up-maintain-vendor-collaboration.md).

Bir satıcı talebi reddedildiğinde durum hem başlangıçtaki aday satıcı kayıt talebinde hem de satıcı talebinde **Reddedildi** olarak görüntülenir.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Çeşitli durumlardaki bir aday satıcı kaydı talebini silme

Aday satıcı kayıt talebinin çeşitli durumları talebin ilerlemesi hakkında genel bir bilgi sağlar.

Aday satıcı kaydı talebindeki **Sil** eylemini kullanarak oluşturulan kayıt zincirini temizleyebilir ve kaldırabilir ve kullanıcı hesabını devre dışı bırakabilirsiniz. **Sil** eyleminin sonucu, aday satıcı kaydı talebinin durumuna göre aşağıdaki tabloda gösterildiği şekilde farklılık gösterir.


|          Durum          |                                                                                     Durum açıklaması                                                                                      |                                                                                                                                                            Sil eyleminin sonucu                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Yeni            |                                                                         Talep üzerinde herhangi bir eylem gerçekleştirilmemiştir.                                                                          |                                                                                                                                              Aday satıcı kaydı talebi silinir.                                                                                                                                               |
|      Kullanıcı istedi      | <strong>Kullanıcıyı davet et</strong>'i seçtiğinizde, durum <strong>Talep edilen kullanıcı</strong> olarak değişir ve aday kullanıcı talebi oluşturulup kullanıcı talebi iş akışına gönderilir. |                                                                                                          Kullanıcı talebi iş akışı sonlandırılmadığından, bu duruma sahip olan bir aday satıcı kaydı talebini silemezsiniz.                                                                                                          |
|       Kullanıcı davet edildi       |                                                               Kullanıcı talebi iş akışı onaylanır ve kullanıcı oluşturulur.                                                               |                                                                                                                      Kullanıcıyı devre dışı bırakma talebi oluşturulur ve aday satıcı kaydı talebi silinir.                                                                                                                      |
| Kayıt devam ediyor |                                                         Yeni kullanıcı oturum açtı ve satıcı kaydı sihirbazını başlattı.                                                          |                                                                                     Kullanıcıyı devre dışı bırakmak üzere bir talep oluşturulur ve aday satıcı kaydı talebi ve satıcı kaydı sihirbazına girilen veriler silinir.                                                                                      |
|  Satıcı talebi oluşturuldu  |                                                                     Satıcı kaydı sihirbazı tamamlandı.                                                                      | Kullanıcıyı devre dışı bırakmak üzere bir talep oluşturulur ve aday satıcı kaydı talebi, satıcı kaydı sihirbazına girilen veriler ve satıcı talebi silinir.<blockquote>[!NOTE]<br>Satıcı talebi iş akışında gözden geçirme aşamasındayken <strong>Sil</strong> eylemini kullanamazsınız.</blockquote> |
|         Onaylandı         |                                                                               Satıcı talebi onaylanır.                                                                               |                                                                                                   Aday satıcı kaydı talebi, satıcı kaydı sihirbazına girilen veriler ve satıcı talebi silinir.                                                                                                    |
|         Reddedildi         |                                                                               Satıcı talebi reddedilir.                                                                               |                                                                                                   Aday satıcı kaydı talebi, satıcı kaydı sihirbazına girilen veriler ve satıcı talebi silinir.                                                                                                    |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
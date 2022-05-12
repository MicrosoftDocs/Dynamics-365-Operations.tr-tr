---
title: B2B e-ticaret web sitelerindeki iş ortağı kullanıcılarını yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce işletmeler arası (B2B) e-ticaret web sitelerinde ve Commerce Headquarters'ta iş ortağı kullanıcılarını ekleme, silme ve düzenleme işlemleri açıklanmaktadır.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c2fb4846a8457296a2ce758198ade5f4b0df8124
ms.sourcegitcommit: 96e2fb26efd2cd07bbf97518b5c115e17b77a0a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2022
ms.locfileid: "8616869"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>B2B e-ticaret web sitelerindeki iş ortağı kullanıcılarını yönetme

[!include [banner](../../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce işletmeler arası (B2B) e-ticaret web sitelerinde ve Commerce Headquarters'ta iş ortağı kullanıcılarını ekleme, silme ve düzenleme işlemleri açıklanmaktadır.

> [!NOTE]
> - [Müşteri hiyerarşilerini kullanarak B2B iş ortaklarını yönetme](partners-customer-hierarchies.md) konusu bu belge için bir ön koşuldur.
> - **Kuruluş yönetimi \> Belge yönetimi \> Belge türleri**'nde **Belge türleri** formunu açarak Commerce genel merkezde belge türleri varlığını başlattığınızdan emin olun.

B2B e-ticaret web siteleri kuruluşların iş ortakları olarak kaydolmasını gerektirir. Bir kuruluş, bir B2B e-ticaret web sitesine kayıt ayrıntılarını gönderdikten sonra, kayıt isteği bir uygunluk işleminden geçer. Kuruluş başarıyla uygun bulunursa bir iş ortağı olarak eklenir.

Bir kuruluş iş ortağı olarak eklendikten sonra, iş ortağı olma isteğini başlatan kuruluş kullanıcısı yönetici kullanıcı olarak tanımlanır ve B2B e-ticaret web sitesinin ek yetkili kullanıcılarını ekleme ayrıcalığı verilir. Bu yetkili kullanıcılar daha sonra işletme iş ortakları adına sipariş verebilir.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Yeni bir iş ortağı için yönetici kullanıcıyı ayarlama

Potansiyel iş ortakları, B2B sitesindeki bir bağlantı aracılığıyla bir ekleme isteği göndererek B2B e-ticaret web sitesine ekleme işlemini başlatabilir. Daha sonra, ekleme ve kaydolma için gerekli ayrıntıları sağlamak amacıyla özelleştirilebilir formu kullanabilirler. İstek gönderildikten sonra bir gönderim onay sayfası görüntülenir. Gönderim onaylanırsa isteğin onun adına gönderilidği şirket iş ortağı olur ve istekte bulunan kişi (yani ekleme isteğini başlatan kullanıcı) iş ortağı için yönetici kullanıcı olur.

Commerce Headquarters'da iş ortağı isteğini onaylamak için şu adımları izleyin.

1. **Perakende ve Ticaret IT \> Dağıtım planı**'na gidin.
1. Tüm iş ortağı ekleme isteklerini Commerce Headquarters'a çekmek için **P-0001** işini çalıştırın.
1. **P-0001** işi başarıyla çalıştırıldıktan sonra, **Perakende ve Ticaret BT \> Müşteri**'ye gidin ve **Müşterileri ve kanal isteklerini eşitle** işini çalıştırın. Bu iş başarıyla çalıştırıldıktan sonra, ekleme istekleri Commerce Headquarters'da **B2B aday müşterisi** türünde aday müşteri kayıtları olarak oluşturulur. 
1. **Müşteriler \> Tüm aday müşteriler**'e gidin ve aday müşteri ayrıntıları sayfasını açmak için yeni iş ortağının aday müşteri kaydını seçin.
1. Ekleme isteğini onaylamak için **Genel** sekmesinde, **Dönüştür \> Onayla/Reddet**'i seçin. Bir onay iletisi görüntülendiğinde, işleme devam etmek istediğinizi onaylayın ve isteği onaylayın. Onay, aday müşteri kaydının **Durum** alanını **Onaylandı** olarak değiştirir. Daha sonra, kuruluşlarının iş ortağı olarak onaylandığını doğrulamak için istekte bulunan kişinin e-posta adresine bir e-posta gönderilir. Talep eden kişinin iş ortağı için bir yönetici olarak eklendiği bir müşteri hiyerarşisi de oluşturulur.

    > [!NOTE]
    > Şu an için, onay e-postası hemen onay sırasında gönderilir. Ancak, gelecekteki Commerce işlevi yöneticinin e-postaları el ile tetiklemesini sağlayacaktır.

1. **Retail ve Commerce BT \> Dağıtım zamanlaması**'na gidin ve yeni müşteri ve müşteri hiyerarşisi kayıtlarını kanal veritabanına göndermek için **1010 (Müşteriler)** işini çalıştırın.

> [!NOTE]
> Yeni müşteri kayıtlarının kanal veritabanına gönderildiğinden emin olmak için, müşteriyle ilişkilendirilmiş adres defterlerinden en az birinin, çevrimiçi mağazayla ilişkilendirilmiş müşteri adres defterine eklenmesi gerekir. Bu işlemi çevrimiçi mağazanın varsayılan müşterisindeki adres defterini yapılandırarak otomatikleştirebilirsiniz böylece sistem adres defteri değerini her yeni müşteriye kopyalar.

Müşteri hiyerarşisi kayıtları kanal veritabanıyla eşitlendikten sonra, istekte bulunan kişi, ekleme isteğini gönderdiğinde sağladığı e-posta adresini kullanarak B2B e-ticaret web sitesinde oturum açabilir. Kullanıcılar, hesaplarının parolasını tanımlamak için kayıt akışını kullanabilir. Azure Active Directory (Azure AD) B2C kimlik sağlayıcısı kaydının Aday müşteri onayında oluşturulan B2B müşteri kaydıyla bağlantılı hale getirilmesini sağlama hakkında daha fazla bilgi için bkz. [Otomatik bağlamayı etkinleştirme](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>B2B adaylarınız onaylandıklarında veya reddedildiğinde bildirilir

Bir B2B aday müşteri ekleme isteğini onayladığınızda veya reddettiğinizde, aday müşteriye otomatik olarak bir e-posta bildirimi gönderilebilir.

Commerce Headquarters'da **B2B aday müşterisi onaylandı** veya **B2B aday müşterisi reddedildi** bildirimi türü olayları için e-posta bildirimleri ayarlamak üzere aşağıdaki adımları izleyin.

1. **B2B aday müşterisi onaylandı** veya **B2B aday müşterisi reddedildi** bildirim türü tetiklendiğinde aday müşterilere gönderilecek e-postalar için e-posta şablonları oluşturun. Bu bildirim türlerinin desteklediği yer tutucular hakkında bilgi için bkz. [Bildirim türleri](../email-templates-transactions.md#notification-types). E-posta şablonları oluşturma hakkında bilgi için bkz. [E-posta şablonu oluşturma](../email-templates-transactions.md#create-an-email-template).
1. E-posta bildirim profilinize **B2B aday müşterisi onaylandı** ve **B2B aday müşterisi reddedildi** bildirim türlerini ekleyin ve bunları oluşturduğunuz e-posta şablonlarıyla eşleyin. E-posta bildirim profilleri hakkında daha fazla bilgi için, bkz. [E-posta bildirim profili kurulumu](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Ek iş ortağı kullanıcıları ekleme

İş ortağı yönetici kullanıcısı, gerektiğinde B2B e-ticaret web sitesine ek iş ortağı kullanıcıları ekleyebilir.

B2B e-ticaret web sitesine ek iş ortağı kullanıcıları eklemek için şu adımları izleyin.

1. B2B e-ticaret web sitesinde yönetici olarak oturum açın.
1. **Hesabım \> Kuruluş kullanıcıları \> Ayrıntıları görüntüle**'ye gidin ve **Kullanıcı ekle**'yi seçin.
1. Gerekli bilgileri girin ve ardından **Kaydet**'i seçin. Yeni kullanıcı durumu **Beklemede** olarak ayarlanır.

**P-0001** ve **Müşterileri ve kanal isteklerini eşitle**  işleri çalıştırıldıktan sonra, Commerce Headquarters'da yeni kullanıcı için **Kişi** türünde müşteri kaydı oluşturulur. Bu müşteri kaydı, ilgili iş ortağının müşteri hiyerarşisi kaydıyla da ilişkilidir. Ayrıca, yeni kullanıcının e-posta adresine, iş ortağı kuruluşunun kullanıcısı olarak eklendiklerini ve artık B2B e-ticaret web sitesinde oturum açabileceklerini bildiren bir e-posta gönderilir.

Sonra, yeni iş ortağı kullanıcısını kanal veritabanıyla eşitlemek için **1010 (Müşteriler)** işini çalıştırın.

Müşteri kaydı eşitlendikten sonra, B2B e-ticaret web sitesinde kullanıcının durumu **Etkin** olarak ayarlanır ve yeni kullanıcı, e-posta adresini kullanarak B2B e-ticaret web sitesinde oturum açabilir. Kullanıcılar, hesaplarının parolasını tanımlamak için kayıt akışını kullanabilir. Azure AD B2C kimlik sağlayıcısı kaydının Commerce headquarters'da oluşturulan B2B müşteri kaydıyla bağlantılı hale getirilmesini sağlama hakkında daha fazla bilgi için bkz. [Otomatik bağlamayı etkinleştirme](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>İş ortağı kullanıcı ayrıntılarını düzenleme

İş ortağı kullanıcılarının ayrıntılarını düzenlemek için şu adımları izleyin.

1. B2B e-ticaret web sitesinde yönetici olarak oturum açın.
1. **Hesabım \> Kuruluş kullanıcıları \> Ayrıntıları görüntüle**'ye gidin, **Düzenle** düğmesini (kalem simgesi) seçin, gerekli değişiklikleri yapın ve **Kaydet**'i seçin. Değişiklikler yalnızca **P-0001**, **Müşterileri ve kanal isteklerini eşitle** ve **1010 (Müşteriler)** işleri çalıştırıldıktan sonra geçerli olur.

## <a name="remove-a-business-partner-user"></a>Bir iş ortağı kullanıcısını kaldırma

Gerektiğinde, bir yönetici bir iş ortağı kuruluşunun mevcut kullanıcılarını B2B e-ticaret web sitesine erişebilen kullanıcılar listesinden kaldırabilir.
İş ortağı kullanıcısını kaldırmak için şu adımları izleyin.
- B2B e-ticaret web sitesinde yönetici olarak oturum açın.
- **Hesabım > Kuruluş kullanıcıları \> Ayrıntıları görüntüle**'ye gidin ve **Kaldır** düğmesini ("X" simgesi) seçin. Bir onay iletisi görüntülendiğinde, kullanıcıyı kaldırmak istediğinizi onaylayın. Değişiklik yalnızca **P-0001**, **Müşterileri ve kanal isteklerini eşitle** ve **1010 (Müşteriler)** işleri çalıştırıldıktan sonra geçerli olur.

> [!NOTE]
> Bir kullanıcıyı B2B e-ticaret web sitesine erişebilen kullanıcılar listesinden kaldırdığınızda, ilgili müşteri kaydı iş ortağının müşteri hiyerarşisi kaydından kaldırılır. Ancak, müşteri kaydının kendisi, Commerce Headquarters'dan silinmez.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Mevcut müşterileri B2B e-ticaret web sitesinde iş ortakları olarak ekleme

Yöneticiler doğrudan Commerce Headquarters'da iş ortakları ve kullanıcılar ekleyebilir. Bu özellik, mevcut iş ortaklarınızı B2B e-ticaret web sitesinde eklemek için yararlıdır.

Commerce Headquarters'da iş ortaklarını ve kullanıcıları eklemek için şu adımları izleyin.

1. **Kuruluş** türünde müşteri kaydı oluşturun veya seçin ve iş ortağı olarak ekleyin.
1. İş oratğı için yönetici veya iş ortağı olarak eklemek üzere **Kişi** türünde bir müşteri oluşturun veya seçin. Birincil e-posta adreslerinin müşterilerle ilişkilendirildiğinden emin olun. Bu e-posta adresleri web sitesinde oturum açmak için kullanılır. 

    > [!NOTE]
    > Sistem, web sitesinde oturum açabilmeleri gereken kullanıcılar için benzersiz bir müşteri kaydı bulabilmelidir. Sistem, tüzel kişilikte aynı birincil e-posta adresine sahip birden fazla müşteri bulursa kullanıcı web sitesinde oturum açamaz.

1. Müşteri hiyerarşi kimliği oluşturun.
1. **Ad** alanına, bir ad girin.
1. **Kuruluş** alanına iş ortağı kuruluşu müşterisini girin.
1. **Hiyerarşi** hızlı sekmesinde **Ekle**'yi seçin.
1. **Ad** alanında **Kişi** türünde bir müşteri seçin.
1. Yönetici olarak belirlenmesi gereken müşteri için **Yönetici** rolünü seçin.
1. Hiyerarşiye ek müşteriler eklemek için bu işlemi yineleyin.

## <a name="additional-information"></a>Ek bilgiler

- Bu konuda belirtilen tüm işler, bir zamanlamada toplu iş biçiminde çalışacak şekilde yapılandırılabilir. Beklenti, iş ortaklarının toplu işleri gerektiği gibi yapılandırmasıdır.
- Şu anda, yönetici kullanıcı olarak yalnızca bir kullanıcı/müşteri kaydı atanabilir ve bu rol yalnızca Commerce Headquarters'da değiştirilebilir. İş ortaklarının B2B e-ticaret web sitelerinden birden fazla yönetici belirlemesine veya yönetici değiştirmesine izin veren self servis özellikler için destek sunulmaz.
- Kullanıcılar için harcama limitleri tanımlanabilse de, sipariş giriş işlemi sırasında harcama limitlerinin zorunlu kılınması henüz uygulanmamıştır.
- Bir kullanıcının B2B e-ticaret web sitesindeki deneyimi için tüm iş mantığı ve doğrulama, Commerce Headquarters'da kullanıcıyla eşlenen müşteri kaydının yapılandırmasını temel alır.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B e-ticaret sitesi ayarlama](set-up-b2b-site.md)

[Müşteri hiyerarşileri kullanarak B2B iş ortaklarını yönetme](partners-customer-hierarchies.md)

[B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma](payment-method.md)

[B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama](quantity-limits.md)

[Numara serilerine genel bakış](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

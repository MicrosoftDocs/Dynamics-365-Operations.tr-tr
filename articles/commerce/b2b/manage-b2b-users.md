---
title: B2B e-ticaret web sitelerindeki iş ortağı kullanıcılarını yönetme
description: Bu konuda, yöneticilerin işletmeden işletmeye (B2B) e-ticaret web sitelerinde iş ortağı kullanıcıları ekleme, düzenleme ve silme yöntemleri açıklanmaktadır.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c1bd8d9cb494cef78fa7c14f6c391821d48749a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799865"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>B2B e-ticaret web sitelerindeki iş ortağı kullanıcılarını yönetme

[!include [banner](../../includes/banner.md)]

Bu konuda, yöneticilerin işletmeden işletmeye (B2B) e-ticaret web sitelerinde iş ortağı kullanıcıları ekleme, düzenleme ve silme yöntemleri açıklanmaktadır.

B2B e-ticaret web siteleri kuruluşların iş ortakları olarak kaydolmasını gerektirir. Bir kuruluş, bir B2B e-ticaret web sitesine kayıt ayrıntılarını gönderdikten sonra, bir uygunluk işleminden geçer. Kuruluş başarıyla uygun bulunursa bir iş ortağı olarak eklenir.

Bir kuruluş iş ortağı olarak eklendikten sonra, iş ortağı olma isteğini başlatan kuruluş kullanıcısı yönetici kullanıcı olarak tanımlanır ve B2B e-ticaret web sitesinin ek yetkili kullanıcılarını ekleme ayrıcalığı verilir. Bu yetkili kullanıcılar daha sonra işletme iş ortakları adına sipariş verebilir.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>Commerce Headquarters'da B2B e-ticaret yetenekleri özelliğini açma

Commerce Headquarters'da B2B e-ticaret yetenekleri özelliği, kuruluşların iş ortaklarını eklemesine ve yönetici kullanıcıları tanımlamasına olanak tanır. Bu özellik yöneticilerin iş ortağı kullanıcıları ve ekipleri oluşturmasına ve yönetmesine ve onlara belirli roller atamasına da olanak tanır. Son olarak, iş ortağı kullanıcılarının sipariş şablonları oluşturmasına ve ürünleri yeniden sipariş etmek için mevcut siparişleri kullanmasına olanak tanır.

Commerce Headquarters'da B2B e-ticaret yetenekleri özelliğini açmak için şu adımları izleyin.

1. **Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. **Tümü** sekmesinde, **Perakende ve ticaret** terimini kullanarak **Modül** alanına filtre uygulayın.
1. **B2B e-ticaret özelliklerinin kullanımını etkinleştir** adlı özelliği bulup seçin ve ardından **Şimdi etkinleştir**'i seçin.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Numara serisi oluşturma ve Commerce paylaşılan parametrelerine ekleme

Numara serileri, ana veri kayıtları ve tanımlayıcı gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır. Numara serileri hakkında daha fazla bilgi için bkz. [Numara serilerine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Bir numara serisi oluşturmak ve bunu Commerce Headquarters'da Commerce paylaşılan parametrelerine eklemek için şu adımları izleyin.

1. **Perakende ve Ticaret \> Headquarters kurulumu \> Numara serileri \> Numara serileri**'ne gidin ve bir numara serisi oluşturun.
1. **Perakende ve Ticaret \> Headquarters kurulumu \> Parametreler \> Commerce paylaşılan parametreleri**'ne gidin ve yeni numara serisini **Müşteri hiyerarşi kimliği** başvurusuna ekleyin.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Yeni bir iş ortağı için yönetici kullanıcıyı ayarlama

Potansiyel iş ortakları, sitedeki bir bağlantı aracılığıyla bir ekleme isteği göndererek B2B e-ticaret web sitesine ekleme işlemini başlatabilir. Potansiyel bir iş ortağı kullanıcısı bağlantıyı seçtikten sonra, ekleme ve kaydolma için gereken ayrıntıları sağlayabilir. İstek gönderildikten sonra bir gönderim onay sayfası görüntülenir. Gönderim onaylanırsa istek sahibi (yani, ekleme isteğini başlatan kullanıcı) iş ortağı yöneticisi kullanıcı olur.

Commerce Headquarters'da bir iş ortağı yöneticisi kullanıcısını onaylamak ve ayarlamak için şu adımları izleyin.

1. **Perakende ve Ticaret IT \> Dağıtım planı**'na gidin.
1. Tüm iş ortağı ekleme isteklerini Commerce Headquarters'a çekmek için **P-0001** işini çalıştırın.
1. **P-0001** işi başarıyla çalıştırıldıktan sonra, **Perakende ve Ticaret BT \> Müşteri**'ye gidin ve **Zaman uyumsuz moddan müşterileri ve iş ortaklarını eşitle** işini çalıştırın. Bu iş başarıyla çalıştırıldıktan sonra, ekleme istekleri Commerce Headquarters'da potansiyel müşteri kayıtları olarak oluşturulur. Bu kayıtların **Tür Kimliği** alanı **B2B müşteri adayı** olarak ayarlanır.
1. **Müşteriler \> Tüm potansiyel müşteriler**'e gidin ve potansiyel müşteriler sayfasını açın.
1. Aday müşteri ayrıntıları sayfasını açmak için yeni iş ortağının aday müşteri kaydını seçin.
1. Ekleme isteğini onaylamak veya reddetmek için **Genel** sekmesinde, **Dönüştür \> Onayla/Reddet**'i seçin. Bir onay iletisi görüntülendiğinde, işleme devam etmek istediğinizi onaylayın ve isteği onaylayın. Daha sonra, kuruluşlarının iş ortağı olarak onaylandığını doğrulamak için istekte bulunan kişinin e-posta adresine bir e-posta gönderilir.

    İsteği onayladıktan sonra, aday müşteri kaydının **Durum** alanı **Onaylandı** olarak ayarlanır. Ayrıca, sistemde iki yeni müşteri kaydı oluşturulur: iş ortağı kuruluşu için **Tür Kuruluş** müşteri kaydı ve istekte bulunan kişi için bir **Tür Kişi** müşteri kaydı. İş ortağı için bir müşteri hiyerarşi kaydı da oluşturulur. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. **Perakende ve Ticaret IT \> Dağıtım planı**'na gidin ve yeni oluşturulan müşteri ve müşteri hiyerarşisi kayıtlarını kanal veritabanına göndermek için **1010** (**Müşteriler**) işini çalıştırın.

İstek onaylandıktan ve müşteri ile müşteri hiyerarşisi kayıtları kanal veritabanıyla eşitlendikten sonra, istekte bulunan kişi, isteği gönderdiğinde sağladığı e-posta adresini kullanarak B2B e-ticaret web sitesinde oturum açabilir. Kullanıcılar, hesaplarının parolasını tanımlamak için kayıt akışını kullanabilir.

## <a name="onboard-additional-business-partner-users"></a>Ek iş ortağı kullanıcıları ekleme

İş ortağı yönetici kullanıcısı, gerektiğinde B2B e-ticaret web sitesine ek iş ortağı kullanıcıları ekleyebilir.

B2B e-ticaret web sitesine ek iş ortağı kullanıcıları eklemek için şu adımları izleyin.

1. B2B e-ticaret web sitesinde yönetici olarak oturum açın.
1. **Hesabım \> Kuruluş kullanıcıları \> Ayrıntıları görüntüle**'ye gidin ve **Kullanıcı ekle**'yi seçin.
1. Gerekli bilgileri girin ve ardından **Kaydet**'i seçin. Yeni kullanıcı durumu **Beklemede** olarak ayarlanır.

    **P-0001** ve **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle**  işleri çalıştırıldıktan sonra, Commerce Headquarters'da yeni kullanıcı için **Tür Kişi** müşteri kaydı oluşturulur. Bu müşteri kaydı, ilgili iş ortağının müşteri hiyerarşisi kaydıyla da ilişkilidir. Ayrıca, yeni kullanıcının e-posta adresine, iş ortağı kuruluşunun kullanıcısı olarak eklendiklerini ve artık B2B e-ticaret web sitesinde oturum açabileceklerini bildiren bir e-posta gönderilir.

1. Yeni iş ortağı kullanıcısını kanal veritabanıyla eşitlemek için **1010** (**Müşteriler**) işini çalıştırın.

Müşteri kaydı eşitlendikten sonra, B2B e-ticaret web sitesinde kullanıcının durumu **Etkin** olarak ayarlanır ve yeni kullanıcı, e-posta adresini kullanarak B2B e-ticaret web sitesinde oturum açabilir. Kullanıcılar, hesaplarının parolasını tanımlamak için kayıt akışını kullanabilir.

## <a name="edit-business-partner-user-details"></a>İş ortağı kullanıcı ayrıntılarını düzenleme

İş ortağı kullanıcılarının ayrıntılarını düzenlemek için şu adımları izleyin.

1. B2B e-ticaret web sitesinde yönetici olarak oturum açın.
1. **Hesabım \> Kuruluş kullanıcıları \> Ayrıntıları görüntüle**'ye gidin, **Düzenle** düğmesini (kalem simgesi) seçin, gerekli değişiklikleri yapın ve **Kaydet**'i seçin. Değişiklikler yalnızca **P-0001**, **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** ve **1010** (**Müşteriler**) işleri çalıştırıldıktan sonra geçerli olur.

## <a name="remove-a-business-partner-user"></a>Bir iş ortağı kullanıcısını kaldırma

Gerektiğinde, bir yönetici bir iş ortağı kuruluşunun mevcut kullanıcılarını B2B e-ticaret web sitesine erişebilen kullanıcılar listesinden kaldırabilir.

İş ortağı kullanıcısını kaldırmak için şu adımları izleyin.

1. B2B e-ticaret web sitesinde yönetici olarak oturum açın.
1. **Hesabım \> Kuruluş kullanıcıları \> Ayrıntıları görüntüle**'ye gidin ve **Kaldır** düğmesini ("X" simgesi) seçin. Bir onay iletisi görüntülendiğinde, kullanıcıyı kaldırmak istediğinizi onaylayın. Değişiklikler yalnızca **P-0001**, **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** ve **1010** (**Müşteriler**) işleri çalıştırıldıktan sonra geçerli olur.

> [!NOTE]
> Bir kullanıcıyı B2B e-ticaret web sitesine erişebilen kullanıcılar listesinden kaldırdığınızda, ilgili müşteri kaydı iş ortağının müşteri hiyerarşisi kaydından kaldırılır. Ancak, müşteri kaydının kendisi, Commerce Headquarters'dan silinmez.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Commerce Headquarters'a iş ortağı ve kullanıcılar ekleme

Yöneticiler doğrudan Commerce Headquarters'da iş ortakları ve kullanıcılar ekleyebilir.

Commerce Headquarters'da iş ortaklarını ve kullanıcıları eklemek için şu adımları izleyin.

1. İş ortağı kuruluşu için **Tür Kuruluş** müşteri kaydı oluşturun.
1. İş ortağı kullanıcıları için **Tür Kişi** müşteri kayıtları oluşturun. Her müşteri için birincil e-posta adresinin belirtildiğinden emin olun.
1. İş ortağı kuruluşunun yönetici kullanıcısı olarak atanması gereken her **Tür Kişi** müşteri kaydı için **Perakende** hızlı sekmesinde **B2B yöneticisi** seçeneğini **Evet** olarak ayarlayın.
1. Müşteri hiyerarşi kimliği oluşturun. **Ad** alanına, bir ad girin.
1. **Kuruluş** alanına iş ortağı kuruluşu müşterisini girin.
1. **Ekle**'yi seçin ve sonra **Ad** alanından bir müşteri seçin.
1. Hiyerarşiye ek müşteriler eklemek için bu işlemi yineleyin.

## <a name="additional-information"></a>Ek bilgiler

- Bu konuda belirtilen tüm işler, bir zamanlamada toplu iş biçiminde çalışacak şekilde yapılandırılabilir. Beklenti, iş ortaklarının toplu işleri gerektiği gibi yapılandırmasıdır.
- Şu anda, yönetici kullanıcı olarak yalnızca bir kullanıcı/müşteri kaydı atanabilir ve bu rol yalnızca Commerce Headquarters'da değiştirilebilir. İş ortaklarının B2B e-ticaret web sitelerinden birden fazla yönetici belirlemesine veya yönetici değiştirmesine izin veren self servis özellikler için destek sunulmaz.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Kullanıcılar için harcama limitleri tanımlanabilse de, sipariş giriş işlemi sırasında harcama limitlerinin zorunlu kılınması henüz uygulanmamıştır.
- Bir kullanıcının B2B e-ticaret web sitesindeki deneyimi için tüm iş mantığı ve doğrulama, Commerce Headquarters'da kullanıcıyla eşlenen müşteri kaydının yapılandırmasını temel alır.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B e-ticaret sitesi ayarlama](set-up-b2b-site.md)

[B2B kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma](org-model.md)

[B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma](payment-method.md)

[B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama](quantity-limits.md)

[Numara serilerine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
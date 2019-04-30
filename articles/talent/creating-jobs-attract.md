---
title: Attract'ta iş oluşturun, onaylayın ve yayınlayın
description: Bu konu, Attract'taki bir işin öğelerini açıklar. Bu aynı zamanda bir iş oluşturmayı açıklar.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1e76572c1a843fe7abd515333d5b7cb03b91eb11
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/12/2019
ms.locfileid: "969361"
---
# <a name="create-approve-and-post-jobs-in-attract"></a>Attract'ta iş oluşturun, onaylayın ve yayınlayın

[!include [banner](includes/banner.md)]

Bu konu Microsoft Dynamics 365 for Talent: Attract içindeki bir maddeyi açıklar. Bu aynı zamanda bir iş oluşturmayı açıklar.

## <a name="job-creation"></a>İş oluşturma

Yöneticiler, işe alanlar ve işe alma müdürleri işler oluşturabilir. Bir iş oluşturduğunuzda, işlem sırasında rolünüzü seçmeniz istenir: işe alma yöneticisi veya işveren. Bir rol seçtikten sonra işlem şablonu seçmeniz istenir. **Atla**'yı seçerseniz varsayılan şablon kullanılır. İşlem şablonları hakkında daha fazla bilgi için bkz. [Attract'ta işlem şablonu oluştur](./process-templates-attract.md).

Attract'taki bir işin iş ayrıntıları, işe alma ekibi, bir işe alma işlemi, iş yayınlama ve analitiği vardır.

## <a name="job-details"></a>İş ayrıntıları

**İş ayrıntıları** sekmesi, iş sorumlulukları ve öznitelikleri hakkında ayrıntılı bilgi içerir. İş unvanı, iş açıklaması ve iş yeri alanları gerekli alanlardır. Diğer alanlar, isteğe bağlıdır.

Varsayılan olarak **Boş pozisyon sayısı** **1** olarak ayarlanır. Ancak, değerde değişiklik yapabilirsiniz. Ne zaman iş için bir teklif hazırlanırsa **Mevcut boş pozisyon sayısı** alanının değeri azaltılır.

Konum yönetimi Yönetim Merkezinde etkinleştirilirse **Pozisyonları güncelleştir** araması kullanılabilir. Bu arama Common Data Service'teki JobPosition varlığını okur ve iş için seçilebilecek pozisyonların bir listesini verir. Seçtiğiniz pozisyon sayısı açık pozisyon sayısını aşarsa, bir uyarı alırsınız. Pozisyon birden çok iş üzerinde kullanılırsa da uyarı alırsınız.

> [!NOTE]
> Pozisyon yönetimi, Kapsamlı işe alma eklentisinde kullanılabilir.

İşe alma sürecinin Teklif eylemindeki ayarlara bağlı olarak pozisyon sayısı, bir teklifte iki kez kullanılabilir. Daha fazla bilgi için bkz. [İşe alma süreci](./activities-attract.md).

Attract'ta varsayılan **Beceriler** kümesi bulunur. Bu beceriler yazarken öneri olarak görünür. Yeni yetenek metin alanına girip Enter' basarak daha fazla yetenek ekleyebilirsiniz.

Attract'ta varsayılan **İş fonksiyonları** kümesi bulunur. Yeni iş fonksiyonu alanına girip Enter tuşuna basın, en çok üç iş fonksiyonu ekleyebilirsiniz.

Attract'ta varsayılan **Şirket sektörü** kümesi bulunur. Yeni şirket sektörü alanına girip Enter tuşuna basın, en çok üç şirket sektörü ekleyebilirsiniz.

## <a name="hiring-team"></a>İşe alım takımı

**İşe alım ekibi** sekmesi, işe dahil edilecek kişilerin listesini içerir. Kullanıcılar işe alma ekibine eklendiğinde, işe alma ekibinde role atanmalıdır. Rol, kullanıcıların aldıkları bildirimleri ve erişimi olduğu verileri belirler. Seçilebilecek roller **İş veren**, **İşe Alma Yöneticisi**, **Temsilci**, ve **Görüşmeyi Yapan**dır. Rol izinleri hakkında daha fazla bilgi için "Rol yönetimi" belgesine bakın. İşe alanlar ve işe alma müdürleri kendi adlarına çalışması için bir veya birden çok temsilci atayabilir. Temsilciler hakkında daha fazla bilgi için bkz: [Attract'te güvenlik ve rol yönetimi](./security-attract.md).

İşe alma ekibi, iş etkinleştirildikten sonra güncelleştirilebilir.

## <a name="process"></a>İşlem

İşe alma süreci hakkında varsayılan bilgiler, iş oluştururken seçtiğiniz işlem şablonunu temel alır. O anda belirli bir şablon seçilmezse, varsayılan şablon kullanılır. İşe alma işlemi tanımladığınızda Aday müşteri, Başvuru ve Teklif aşamaları dışında çeşitli aşamalar ekleyebilir veya kaldırabilirsiniz. Ancak aday müşteri aşaması kaldırılamaz, devre dışı bırakılabilir. Her aşamada, bir veya birkaç faaliyet ekleyebilir veya kaldırabilirsiniz.

İşe alma işlemine eklenebilen faaliyetler hakkında daha fazla bilgi için bkz. [Attract işe alma süreci faaliyetleri ](./activities-attract.md).

> [!NOTE]
> İşe alma süreci, iş etkinleştirildikten sonra güncelleştirilemez.

## <a name="postings"></a>Deftere nakil işlemleri

Bir iş etkinleştirildikten sonra yayınlanabilir. Yalnızca iş verenler ve yöneticiler, işleri yayınlayabilir. İş, Talent Careers (bir Microsoft Dynamics 365 for Talent kariyer sitesi) veya LinkedIn'de yayınlanabilir. Attract ekibi, iş kurulu toplayıcılarıyla ortaklık için devamlı çalışmaktadır. Zaman içinde bu listeyi genişler. Bir iş yalnızca dahili olarak yayınlanırsa, adayların işi görüntülemeleri ve başvurmaları için bir AAD hesabına sahip olmaları gerekir. İş, herkese açık olarak listelenmişse, adaylar tüm kimlik doğrulama seçenekleriyle işleri görüntüleyebilir ve başvurabilirler. 

İş yayınları hakkında daha fazla bilgi için [Attract'taki kariyer sitesi işlevi](career-site.md).

> [!NOTE]
> İş yayınlama işlevi yalnızca işe Attract için Kapsamlı İşe Alım Eklentisiyle kullanılabilir.

### <a name="posting-jobs-to-linkedin"></a>LinkedIn'e iş ilanı vermek 

Bir işi Attract'ten LinkedIn'e göndermeden önce yöneticinin LinkedIn Şirket Kimlik Kodunu ve LinkedIn Şirket adını **Yönetici ayarlarında** eklemesi gerekir. LinkedIn Şirket Kimlik Kodu, Attract'ten verdiğiniz iş ilanlarının doğru şirket sayfasına eşleştirildiğinden emin olunması için önemlidir.

LinkedIn Şirket Kimlik Kodu, şirketinizi LinkedIn içinde benzersiz şekilde tanımlayan bir dizi sayıdır. LinkedIn şirket kimlik kodunuzu bulmak hakkında daha fazla bilgi için lütfen [LinkedIn sitesini](https://aka.ms/findID) ziyaret edin.

LinkedIn şirketinizi güncelleştirmek için **Yönetim merkezi**'ni, **Ayarlar** menüsünden seçin (çark simgesi),  **LinkedIn Tümleştirmesi** sekmesini seçin. **LinkedIn'e Bağlan** sekmesi altında, LinkedIn Şirket Adınızı ve Şirket Kimlik Kodunuzu girin ve ayarları kaydedin.

> [!NOTE]
> LinkedIn'e iş ilanı verirken dikkate alınacak dört önemli şey vardır.
> 1. LinkedIn'de ilan verilen işler "Sınırlı Listeleme" işleri olarak yayınlanır. Sınırlı listeleme işleri, LinkedIn sayfasının tamamında öne çıkarılamaz. LinkedIn'e Attract'tan yayınlanan sınırlı yayınlanmış işleri öne çıkarmak istiyorsanız, "İş Kaydırma" etkinleştirmek için LinkedIn ile birlikte çalışmalısınız. Daha fazla ayrıntı için aşağıdaki bağlantılara bakın ve LinkedIn destek ile iletişime geçin.
>
>    [Sınırlı Listelemeler - İş Kaydırma için Premium İş Alanları](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping)
>
>    [İş kaydırma hakkında SSS](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions)
>
> 1. İşleri LinkedIn'e ilan verirken, Attract, Microsoft 365 Organizasyonu adını işe karşı iletir. LinkedIn, işleri LinkedIn tarafına dayalı bir şirkete bağlantılar, iletilen kuruluş adına dayalı olarak. İşiniz LinkedIn'de yanlış şirkete karşı ilan verildiyse, Microsoft 365 Organizasyon adınızın, LinkedIn'deki şirket adıyla örtüştüğünden emin olun.  
>
>    [Adresi Bağlantıyı ve daha fazlasını değiştirmek](https://docs.microsoft.com/en-us/office365/admin/manage/change-address-contact-and-more)
>
>    Bu adımdan sonra sorun yaşarsanız, LinkedIn desteği ile iletişime geçin. 
> 
> 1. LinkedIn'e verilen iş ilanları LinkedIn sitesinde yayınlanır. LinkedIn'e iş ilanı vermek için test ortamı yoktur. 
>
> 1. Geçerli LinkedIn toplu iş işleme işlemi nedeniyle LinkedIn'e ilan verilen işlerin LinkedIn içerisindeki adaylara görünür hale gelmesi 24 saate kadar sürebilir.


## <a name="activate"></a>Etkinleştir

Bir iş etkinleştirildikten sonra yayınlanabilir, adaylar ve başvuranlar eklenebilir. Bir işe aday ekleme seçeneği, işe alma sürecindeki Aday eyleminde ayarlanır.

> [!NOTE]
> İşe alma süreci, iş etkinleştirildikten sonra güncelleştirilemez.

## <a name="prospects-and-applicants"></a>Adaylar ve başvuranlar

Bir işe aday ekleme seçeneği, işe alma sürecindeki [Aday eyleminde](./activities-attract.md#prospect-activity) ayarlanır. Bu seçenek, iş etkinleştirmeden önce ayarlanmalıdır. Bir iş etkinleştirildikten sonra, adaylar ve başvuranlar eklenebilir.

## <a name="approvals"></a>Onaylar

Attract işleri, onay için gönderilebilir. Tüm işler onay gerektirmez. Gereksinim şablon düzeyinde ayarlanır. Varsayılan olarak, onaylar şablonda kapatılır. Onayları belirlemek için, bir işlem şablonuna gidin ve **Onay** alanını Varsayılan olarak ayarlayın. Daha sonra iş oluştururken bu şablonu seçin.

Bir iş kaydedildikten sonra onay için gönderilebilir. Onayları kullanan belge durumları aşağıdaki tabloda listelenmiştir.

| Durum   | İl                                                               |
|----------|---------------------------------------------------------------------|
| Taslak    | İş kaydedildi, ancak bir iş akışına gönderilmedi. |
| Bekleyen  | İş, onaylayıcılara gönderildi.                            |
| Onaylandı | İş onaylandı, ancak etkinleştirilmedi.            |
| Reddedildi | İş reddedildi ve etkinleştirilemez.               |
| Etkin   | İş onaylanmış ve etkinleştirilmiş.                            |

İş listesinde iş durumları üzerinde filtre uygulayabilirsiniz.

Onaylar, şirket içindeki bir kullanıcıya doğrudan Microsoft Azure Active Directory (Azure AD) ile gönderilebilir. Onaylar, paralel şekilde onaylayanlar olarak listelenen tüm kişilere gönderilir. Tüm onaylayıcıların ilerlemeden önce işi onaylaması gerekir. Tek bir onaylayıcı işi reddederse, iş **Reddedildi** durumu görüntüler. Bir iş onaylandıktan sonra etkinleştirilebilir.

Bir kullanıcı işi onayladıktan sonra ancak etkinleştirilmeden önce düzenlerse, iş durumu **Taslak** olarak geri çevrilir ve işin yeniden onaya gönderilmesi gerekir. Bir onaylanan iş etkinleştirildikten sonra bunu düzenleyemezsiniz.

Onaylayanlar olarak listelenen kişiler, Attract ve bir epostayla onaylamak için bir öğe olduğunu bildiren bir bildirim alır.  E-posta içinde, onaylayıcılar işi açmak, ayrıntıları görüntülemek ve onaylamak veya reddetmek için bağlantıya tıklayabilirler. İşin durumu **Onaylandı** veya **Reddedildi** olarak ayarlandıktan sonra, yayınlayan Attract içinde bildirim alır ve bir e-posta da alırlar. Ayrıca, onaylayıcılar onay talebine 24 saat içinde yanıt vermedilerse bir anımsatma e-postası alırlar.

> [!NOTE]
> Onay e-postaları için özel e-posta şablonları oluşturabilirsiniz. Daha fazla bilgi için bkz. [E-posta şablonları oluşturmak ve yönetmek](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>İş oluşturma

Bir iş oluşturmak için şu adımları izleyin.

1. **İşler**e gidin.
2. **Yeni**'yi seçin.
3. **İş unvanı** alanına iş unvanı girin. **Rol** alanına rolünüzü girin.
4. **Şablon** alanında bir şablon seçin. Alternatif olarak **Atla**yı seçebilirsiniz. **Atla** öğesini seçerseniz varsayılan şablon olarak işaretlenen şablon kullanılır.

    Belge onay işlemine gitmesi gerekiyorsa **Onay işlemi** alanının **Varsayılan** olarak ayarlandığı bir şablon seçin.

5. **Ayrıntılar** sekmesinde işin ayrıntılarını girin. **Unvan**, **İş açıklaması** ve **Konum** alanları gerekli alanlardır.
6. **Kaydet**'i seçin.
7. **İşe alım ekibi** sekmesinde, bir işe alma yöneticisi, işe alan veya görüşmeyi yapan ekleyin.
8. **Kaydet**'i seçin.
9. **Süreç** sekmesinde, gereken aşamaları ekleyin veya kaldırın:

    - Aşama eklemek için **+ Yeni aşama**yı seçin.
    - Aşama kaldırmak için kaldırılacak aşama üzerine imleci getirin ve görünen çöp kutusu düğmesini seçin.

        > [!NOTE]
        > Aday, Başvuru ve Teklif aşamaları kaldırılamaz.

10. Gereken eylemleri ekleyip kaldırın:

    - Aktivite eklemek için sağdaki listeden uygun aşamaya sürükleyin. Alternatif olarak, faaliyete çift tıklatın ve eklemek için aşamayı seçin.
    - Faaliyeti kaldırmak için, aktiviteyi genişletin ve faaliyet üst bilgisindeki çöp kutusu düğmesini seçin.

11. **Kaydet**'i seçin.
12. Onay işlemi kullanmayı seçtiyseniz, aşağıdaki adımları izleyin:

    1. **+ Onaylayan ekle**'yi seçin ve Azure AD hesabı olan bir kullanıcı girin. Birden çok onaylayan ekleyebilirsiniz.
    2. **Onaylayanlara gönder**'i seçin.

    İşin **İş durumu** alanı **Bekleyen** olarak ayarlanır. **İş durumu** alanı değeri **Onaylandı** olarak değiştiğinde, iş etkin hale getirilebilir.

13. İşi etkinleştirmek için **Etkinleştir** öğesini seçin.
14. İşi yayınlamak için **Gönderiler**'e gidin, Talen Careers sitesi veya LinkedIn'in altındaki **Hemen Yayınla**'yı seçin.

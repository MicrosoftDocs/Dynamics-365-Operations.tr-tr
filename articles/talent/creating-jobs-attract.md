---
title: Attract'te iş oluşturma
description: Bu konu, Attract'teki bir işin öğelerini açıklar. Bu aynı zamanda bir iş oluşturmayı açıklar.
author: hasrivas
manager: AnnBe
ms.date: 07/18/2019
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
ms.openlocfilehash: 95bc75596f6f014b58160022f41ae86a825c5afc
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527278"
---
# <a name="create-a-job-in-attract"></a>Attract'te iş oluşturma

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu Microsoft Dynamics 365 Talent: Attract'teki iş öğelerini açıklar. Bu aynı zamanda bir iş oluşturmayı açıklar.

## <a name="job-creation"></a>İş oluşturma

Yöneticiler, işe alanlar ve işe alma müdürleri işler oluşturabilir. Bir iş oluşturduğunuzda, işlem sırasında rolünüzü seçmeniz istenir: işe alma yöneticisi veya işveren. Bir rol seçtikten sonra işlem şablonu seçmeniz istenir. **Atla**'yı seçerseniz varsayılan şablon kullanılır. İşlem şablonları hakkında daha fazla bilgi için bkz. [Attract'te işlem şablonu oluştur](./process-templates-attract.md).

Attract'teki bir işin iş ayrıntıları, işe alma ekibi, bir işe alma işlemi, iş yayınlama ve analitiği vardır.

## <a name="job-details"></a>İş ayrıntıları

**İş ayrıntıları** sekmesi, iş sorumlulukları ve öznitelikleri hakkında ayrıntılı bilgi içerir. İş unvanı, iş açıklaması ve iş yeri alanları gerekli alanlardır. Diğer alanlar, isteğe bağlıdır.

Varsayılan olarak **Boş pozisyon sayısı** **1** olarak ayarlanır. Ancak, değerde değişiklik yapabilirsiniz. Ne zaman iş için bir teklif hazırlanırsa **Mevcut boş pozisyon sayısı** alanının değeri azaltılır.

Konum yönetimi Yönetim Merkezinde etkinleştirilirse **Pozisyonları güncelleştir** araması kullanılabilir. Bu arama Common Data Service'teki JobPosition varlığını okur ve iş için seçilebilecek pozisyonların bir listesini verir. Seçtiğiniz pozisyon sayısı açık pozisyon sayısını aşarsa, bir uyarı alırsınız. Pozisyon birden çok iş üzerinde kullanılırsa da uyarı alırsınız.

> [!NOTE]
> Pozisyon yönetimi, Kapsamlı işe alma eklentisinde kullanılabilir.

İşe alma sürecinin Teklif eylemindeki ayarlara bağlı olarak pozisyon sayısı, bir teklifte iki kez kullanılabilir. Daha fazla bilgi için bkz. [İşe alım süreçlerindeki faaliyetler](./activities-attract.md).

Attract'te varsayılan **Beceriler** kümesi bulunur. Bu beceriler yazarken öneri olarak görünür. Yeni yetenek metin alanına girip Enter' basarak daha fazla yetenek ekleyebilirsiniz.

Attract'te varsayılan **İş fonksiyonları** kümesi bulunur. Yeni iş fonksiyonu alanına girip Enter tuşuna basın, en çok üç iş fonksiyonu ekleyebilirsiniz.

Attract'te varsayılan **Şirket sektörü** kümesi bulunur. Yeni şirket sektörü alanına girip Enter tuşuna basın, en çok üç şirket sektörü ekleyebilirsiniz.

## <a name="hiring-team"></a>İşe alım takımı

**İşe alım ekibi** sekmesi, işe dahil edilecek kişilerin listesini içerir. Kullanıcılar işe alma ekibine eklendiğinde, işe alma ekibinde role atanmalıdır. Rol, kullanıcıların aldıkları bildirimleri ve erişimi olduğu verileri belirler. Seçilebilecek roller **İş veren**, **İşe Alma Yöneticisi**, **Temsilci**, ve **Görüşmeyi Yapan** dır. Rol izinleri hakkında daha fazla bilgi için "Rol yönetimi" belgesine bakın. İşe alanlar ve işe alma müdürleri kendi adlarına çalışması için bir veya birden çok temsilci atayabilir. Temsilciler hakkında daha fazla bilgi için bkz: [Attract'te güvenlik ve rol yönetimi](./security-attract.md).

İşe alma ekibi, iş etkinleştirildikten sonra güncelleştirilebilir.

## <a name="process"></a>İşlem

İşe alma süreci hakkında varsayılan bilgiler, iş oluştururken seçtiğiniz işlem şablonunu temel alır. O anda belirli bir şablon seçilmezse, varsayılan şablon kullanılır. İşe alma işlemi tanımladığınızda Aday müşteri, Başvuru ve Teklif aşamaları dışında çeşitli aşamalar ekleyebilir veya kaldırabilirsiniz. Ancak aday müşteri aşaması kaldırılamaz, devre dışı bırakılabilir. Her aşamada, bir veya birkaç faaliyet ekleyebilir veya kaldırabilirsiniz.

İşe alma sürecine eklenebilen faaliyetler hakkında daha fazla bilgi için bkz. [İşe alım süreçlerindeki faaliyetler](./activities-attract.md).

> [!NOTE]
> İşe alma süreci, iş etkinleştirildikten sonra güncelleştirilemez.

## <a name="postings"></a>Deftere nakil işlemleri

Bir iş etkinleştirildikten sonra yayınlanabilir. Yalnızca iş verenler ve yöneticiler, işleri yayınlayabilir. İş, Talent Careers (bir Dynamics 365 Talent kariyer sitesi) veya LinkedIn'de yayınlanabilir. Attract ekibi, iş kurulu toplayıcılarıyla ortaklık için devamlı çalışmaktadır. Zaman içinde bu listeyi genişler. Bir iş yalnızca dahili olarak yayınlanırsa, adayların işi görüntülemeleri ve başvurmaları için bir AAD hesabına sahip olmaları gerekir. İş, herkese açık olarak listelenmişse, adaylar tüm kimlik doğrulama seçenekleriyle işleri görüntüleyebilir ve başvurabilirler. 

İş başvuruları hakkında daha fazla bilgi için bkz. [Microsoft Dynamics 365 Talent - Attract'te kariyer sitenizi ayarlama](career-site.md).

> [!NOTE]
> İş yayınlama işlevi yalnızca işe Attract için Kapsamlı İşe Alım Eklentisiyle kullanılabilir.

## <a name="activate"></a>Etkinleştir

Bir iş etkinleştirildikten sonra yayınlanabilir, adaylar ve başvuranlar eklenebilir. Bir işe aday ekleme seçeneği, işe alma sürecindeki Aday eyleminde ayarlanır.

> [!NOTE]
> İşe alma süreci, iş etkinleştirildikten sonra güncelleştirilemez.

## <a name="prospects-and-applicants"></a>Adaylar ve başvuranlar

Bir işe aday ekleme seçeneği, işe alma sürecindeki [İşe alım süreçlerindeki faaliyetler](./activities-attract.md#prospect-activity) içinde ayarlanır. Bu seçenek, iş etkinleştirmeden önce ayarlanmalıdır. Bir iş etkinleştirildikten sonra, adaylar ve başvuranlar eklenebilir.

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
> Onay e-postaları için özel e-posta şablonları oluşturabilirsiniz. Daha fazla bilgi için bkz. [E-posta şablonları oluşturmak ve yönetmek](https://docs.microsoft.com/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>İş oluşturma

Bir iş oluşturmak için şu adımları izleyin.

1. **İşler** e gidin.
2. **Yeni**'yi seçin.
3. **İş unvanı** alanına iş unvanı girin. **Rol** alanına rolünüzü girin.
4. **Şablon** alanında bir şablon seçin. Alternatif olarak **Atla** yı seçebilirsiniz. **Atla** öğesini seçerseniz varsayılan şablon olarak işaretlenen şablon kullanılır.

    Belge onay işlemine gitmesi gerekiyorsa **Onay işlemi** alanının **Varsayılan** olarak ayarlandığı bir şablon seçin.

5. **Ayrıntılar** sekmesinde işin ayrıntılarını girin. **Unvan**, **İş açıklaması** ve **Konum** alanları gerekli alanlardır.
6. **Kaydet**'i seçin.
7. **İşe alım ekibi** sekmesinde, bir işe alma yöneticisi, işe alan veya görüşmeyi yapan ekleyin.
8. **Kaydet**'i seçin.
9. **Süreç** sekmesinde, gereken aşamaları ekleyin veya kaldırın:

    - Aşama eklemek için **+ Yeni aşama** yı seçin.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
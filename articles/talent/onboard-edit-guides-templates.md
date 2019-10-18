---
title: Dynamics 365 Talent - Onboard'da işe alım ve alıştırma kılavuz ve şablonlarını düzenleme
description: Bu konuda Microsoft Dynamics 365 Talent - Onboard'da işe alım ve alıştırma kılavuz ve şablonuna etkinliklerin ve diğer bilgilerin nasıl ekleneceği açıklanmaktadır.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7803c7cd2c58b8544d2c8dd711c295d6882f9fca
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010810"
---
# <a name="edit-onboarding-guides-and-templates"></a>İşe alım kılavuzları ve şablonları düzenleme

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Onboard'da işe alım ve alıştırma kılavuzu veya şablonu oluşturduktan sonra giriş, etkinlik, ilgili kişi ve kaynak eklemeniz gerekir. Onboard, işe alım kılavuzlarınıza aşağıdakiler dahil olmak üzere zengin içerik eklemenizi sağlar:

- YouTube videoları
- Microsoft Sway sunuları
- Microsoft PowerApps uygulamaları
- Microsoft Stream videoları
- Microsoft Forms formları
- Web içeriği içeren iframe'ler

## <a name="edit-introductions-or-activities-imported-from-a-template"></a>Bir şablondan içe aktarılan tanıtımları veya faaliyetleri düzenle

Bir şablondan işe alım kılavuzu oluşturursanız veya bir şablondaki faaliyetleri bir başkasına içe aktardığınızda, içe aktarılan faaliyetlerde bir **Kilit** düğmesi görürsünüz. Bunlara *yönetilen faaliyetler* denir.

[![Yönetilen faaliyetler](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)

Yönetilen bir aktiviteyi seçtiğinizde, faaliyetin en üstünde kaynak şablonu görebilirsiniz.

[![Yönetilen etkinlik kaynağı](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)

Bir şablonda aktivite düzenlerseniz, Onboard, tüm şablonlara ve bu şablonu temel alan gönderilmemiş kılavuzlara değişiklikleri sağlar. Düzenlediğiniz şablonu temel alan gönderilmemiş bir kılavuz seçer ve kılavuzdaki **etkinlikler** sekmesini seçerseniz, kılavuzun değiştiğine ilişkin bir bildirim görürsünüz. Bildirimi kapatmak için **Tamam**'ı seçin. 

[![Değişiklik Bildirimi](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)

Güncellenmiş etkinliklerin yanında siyah bir nokta göreceksiniz.

[![Değiştirilen faaliyet](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)

Faaliyetin sağ bölümüne atanan, son tarih veya başka bilgiler eklemek dışında, yönetilen faaliyetleri özgün şablon dışında düzenleyemezsiniz.

Yönetilen bir aktiviteyi düzenlemek istiyorsanız veya bir etkinliğin geldiği şablondan gelen güncelleştirmeleri almasını istemiyorsanız, o faaliyetin **Kilit** düğmesini seçin. **Kilit** düğmesi kaybolur. Faaliyet artık özgün şablon tarafından yönetilmeyecek ve artık bu şablondan güncelleştirme almayacak. Bir etkinlikte yaptığınız güncelleştirmeler özgün şablonu etkilemez.

Bir kılavuzdan gelen bir aktiviteyi siler ve bu kılavuzun şablonundaki değişiklikleri gönder seçeneğini tıklattığınızda, etkinlik rehberde silinmiş olarak kalır.

> [!NOTE]
> İlgili kişiler ve kaynaklar şablonlar tarafından yönetilmiyor. Ayrıca, bölümler yönetilmez, bu nedenle bir şablona bölüm eklerseniz veya düzenlerseniz, değişiklikler bu şablonu kullanan tüm kılavuzlara veya şablonlara itilecektir.
> 
> Bir şablona yeni aktiviteler eklerseniz, yeni aktiviteler o şablonu temel alan kılavuzlara ve şablonlara itilir ve yeni aktiviteler en üstte görüntülenir.

## <a name="import-activities-from-another-template"></a>Başka bir şablondan faaliyetleri içe aktar

Bir veya daha fazla şablonu bir kılavuza veya şablona içe aktarabilirsiniz.

1. Düzenlemek istediğiniz kılavuzu veya şablonu seçin.

2. **Faaliyetler** sekmesini seçin.

3. Sağdaki bölümde **içe aktar** sekmesini seçin.

   [![Faaliyetleri içe aktar](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)

4. Görevleri tarayıcınızda yeni bir sekmede önizlemek için, herhangi bir şablonda **yeni sekme ile aç** düğmesini seçin.

   [![Faaliyetleri içe aktar](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)

5. İstenen şablonu sürükleyip kılavuz şablonunda etkinliklerin görünmesini istediğiniz yere sürükleyin ve bırakın. Kılavuzunuz veya şablonunuzu düzenlemeye devam edin.

İçe aktarılan faaliyetler, bu aktivitelerin içe aktardığınız şablon tarafından yönetildiğini gösteren bir **Kilit** düğmesi içerir. İçe aktardığınız şablonda değişiklik yaptığınızda, bu aktiviteler bunları içe aktardığınız şablonda güncelleştirilir. Ancak değişiklikler, içe aktardığınız şablondan oluşturulan herhangi bir kılavuza otomatik olarak itilecektir.

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a>Değişiklikleri şablondan diğer şablonlara veya kılavuzlara gönderme

Başka şablon veya kılavuzlarda kullanılan etkinlikleri içeren bir şablonu düzenlerseniz, bunların diğer şablonlarda veya kılavuzlarda görünmesini istiyorsanız, değişiklikleri gönderin.

Şablonunuzun aktivitelerinin başka şablonlarda veya kılavuzlarda kullanıldığından emin değilseniz, bu etkinliklerin nerede göründüğünü görüntülemek için **Kullanılacak yer** sekmesinde kullanılır.

   [![Faaliyetlerin kullanıldığı kılavuzları ve şablonları görüntüle](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)

Değişikliklerinizi göndermek için:

1. **Kaydet** düğmesini seçerek değişikliklerinizi kaydedin. Bunu yapmazsanız, sonraki adımda yaptığınız değişiklikleri kaydetmeniz istenecektir.

2. **Bu değişiklikleri gönder**'i seçin.

   
## <a name="add-or-edit-an-introduction"></a>Giriş ekleme veya düzenleme

1. **Giriş** sekmesinde, kılavuzunuz ve bir açılış mesajı için bir başlık girin. Örnek metni kullanmak için **Bu iletiyi kullan**'ı seçin.

    [![Onboard şablonunda giriş sekmesi](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)

2. Metni gerektiği gibi çağırmak veya görüntü ya da bağlantı eklemek için biçimlendirme düğmelerini kullanın.
3. İşinizi kaydetmek için **Kaydet**'i seçin.

## <a name="add-or-edit-activities"></a>Faaliyet ekle veya düzenle

1. **Aktiviteler** sekmesinde, maddeleri sağdan düzenleme alanına sürükleyin.
2. Kılavuzunuz ile bölümler arasında düzenleme yapmak için, **Yeni bölüm** öğesini düzenleme alanına sürükleyin ve bölüm için bir ad ve isteğe bağlı açıklama girin.

    ![[İşe alma kılavuzuna veya şablona yeni bölüm ekleme] (./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. Yeni işe alma yaptığınız aktiviteleri tamamlamak için, **yeni aktivite** öğesini düzenleme alanına sürükleyin ve etkinliğin adını ve açıklamasını girin.

    ![[Ekleme kılavuzuna veya şablona yeni faaliyet ekleme] (./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. İşe alım kılavuzuna zengin içerik ekleyin:

    - YouTube videosu eklemek için, **YouTube** öğesini düzenleme alanına sürükleyin, etkinliğin adını ve açıklamasını girin ve YouTube videonun URL'sini girin.
    - Sway sunusu veya haber bülteni eklemek için, **Sway** öğesini düzenleme alanına sürükleyin, etkinliğin adını ve açıklamasını girin ve Sway sunusu veya Bülteninizin katıştırılmış URL'sini girin.
    - Bir PowerApps uygulaması eklemek için **PowerApps** öğesini düzenleme alanına sürükleyin, etkinliğin adını ve açıklamasını girin ve PowerApps uygulamasını seçin veya PowerApps uygulama kimliğini girin.
    - Microsoft Stream videosu eklemek için, **Microsoft Stream** öğesini düzenleme alanına sürükleyin, etkinliğin adını ve açıklamasını girin ve Microsoft Stream videonun URL'sini girin.
    - Microsoft Forms formu eklemek için, **Microsoft Forms** öğesini düzenleme alanına sürükleyin, aktivitenin adını ve açıklamasını girin, Microsoft Forms form için URL'yi girin ve ekran alanının boyutunu belirtin.
    - Web içeriği barındıran iframe eklemek için, **Web İçeriği (iframe)** öğesini düzenleme alanına sürükleyin, aktivitenin adını ve açıklamasını girin, web içeriği için URL'yi girin ve ekran alanının boyutunu belirtin.

    ![[Ekleme kılavuzuna veya şablona zengin içerik ekleme] (./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. İsteğe bağlı: Her faaliyetin sağındaki alanda, aktiviteyi belirli bir kişiye veya role atayın, bir son tarih ve ilgili kişi ekleyin ve bir kategori rengi atayın. Bir kişiye veya role faaliyet atadığınızda, her birey için bir görev oluşturulur. Bu görev, Onboard'da **Görevler** menüsünde görünür.

    [![Ekleme kılavuzunda veya şablonunda faaliyet atama](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)

3. İşinizi kaydetmek için **Kaydet**'i seçin.

Bir aktivite veya bölümü silmek için, etkinliğin veya bölümün sağ üst köşesindeki **Sil** düğmesini (çöp tenekesi simgesi) seçin.

Aktiviteleri ve bölümleri yeniden düzenlemek için, onları yeni bir konuma sürükleyin.

## <a name="add-or-edit-contacts"></a>Kişi ekle veya düzenle

Yeni işe alma sisteminizin ilk gününden başarılı olmasını sağlamaya yardımcı olabilecek kişileri ekleyebilirsiniz. Bu kişiler; işe alanlar, ekip üyeleri, işe alma ekibi, akıl hocaları, yöneticiler ve BT destek personeli olabilir.

1. **Kişiler** sekmesinde, **Yeni kişi**'yi seçin.
2. **Takım üyesi ekle** iletişim kutusunda ilgili kişinin adını veya e-posta adresini girin, ilgili kişinin yeni işe alma konusunda nasıl yardımcı olduğunu açıklayan kısa bir açıklama girin ve sonra **Ekle**'yi seçin. 

    ![[Ekleme kılavuzuna veya şablona kişiler ekleme] (./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    Alternatif olarak, **Öneriler** altında bir veya daha fazla ilgili kişi seçebilirsiniz.

3. İşinizi kaydetmek için **Kaydet**'i seçin.

Bir ilgili kişiyi silmek için, ilgili kişinin sağındaki **Sil** düğmesini (çöp tenekesi simgesi) seçin.

Bir kişiyi düzenlemek için, ilgili kişinin sağındaki **Düzenle** düğmesini (kalem simgesi) seçin.

## <a name="add-or-edit-resources"></a>Kaynaklar ekle veya düzenle

İşe alım kılavuzunun **Kaynaklar** bölümüne yararlı dosyalar, haritalar ve bağlantılar ekleyebilirsiniz.

1. **Kaynaklar** sekmesinde, **Yeni kaynak**'ı seçin.
2. Şu adımlardan birini izleyin:

    - Bir dosya eklemek için **Dosya** sekmesini seçin ve dosyayı belirtilen alana sürükleyin. (Alternatif olarak, bu alanda herhangi bir yeri tıklatarak dosyayı bilgisayarınızda bulun veya **OneDrive'a Gözat**'ı seçin.) Dosya için bir ad girin ve **Ekle**'yi seçin.
    - Bağlantı eklemek için **Bağlantı** sekmesini seçin, bağlantı için bir ad ve adres girin ve sonra **Ekle**'yi seçin.
    - Harita eklemek için **Harita** sekmesini seçin, harita için bir ad ve adres girin ve sonra **Ekle**'yi seçin. Onboard, belirttiğiniz adresin bir haritasını içerecektir.

    ![[Ekleme kılavuzuna veya şablona kaynak ekleme] (./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. İşinizi kaydetmek için **Kaydet**'i seçin.

Bir ilgili kaynağı silmek için, ilgili kaynağın sağındaki **Sil** düğmesini (çöp tenekesi simgesi) seçin.

Bir kişiyi düzenlemek için, ilgili kaynağın sağındaki **Düzenle** düğmesini (kalem simgesi) seçin.

## <a name="next-steps"></a>Sonraki adımlar

- [İçeriği diğer katkıda bulunanlarla paylaşın](./onboard-share-template.md)
- [Görevlerin ve işe alınan çalışanların durumunu görüntüleme](./onboard-view-status.md)
- [Onboard'da işe alma ekipleri oluşturun](./onboard-create-team.md)

### <a name="see-also"></a>Ayrıca bkz.

- [Onboard uygulamasını deneyin veya satın alın](https://dynamics.microsoft.com/talent/onboard/)
- [Yenilikler](./whats-new.md)
- [Sürüm notları](https://docs.microsoft.com/business-applications-release-notes/index)
- [Destek alma](./talent-support.md)

---
title: Teams'de izin isteklerini yönetme
description: Bu konuda Microsoft Teams uygulamasındaki Dynamics 365 Human Resources uygulamasında, nasıl izin isteneceği gösterilmektedir.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b3daa76385518ad4c7150fa93ce33be0351bfd57
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428840"
---
# <a name="manage-leave-requests-in-teams"></a>Teams'de izin isteklerini yönetme

[!include [banner](includes/preview-feature.md)]

Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, hızlı bir şekilde izin isteğinde bulunmanıza ve izin bakiyesi bilgilerinizi doğrudan Microsoft Teams platformunda görüntülemenize olanak tanır. Bilgi istemek için bir botla etkileşime geçebilirsiniz. **İzin** sekmesi, daha ayrıntılı bilgi sağlar.

## <a name="install-the-app"></a>Uygulamayı yükleme

Human Resources uygulamasını Teams mağazasında bulabilirsiniz.

1. Microsoft Teams platformuna üç nokta simgesini seçin.

   ![Human Resources Teams izin uygulaması üç nokta simgesi](./media/hr-teams-leave-app-ellipses.png)
 
2. Dynamics 365 Human Resources uygulamasını arayın ve ardından **Human Resources** kutucuğunu seçin.

   ![Human Resources Teams izin uygulaması HR kutucuğu](./media/hr-teams-leave-app-human-resources-tile.png)

3. Uygulamayı yüklemek için **Ekle** düğmesini seçin.

   ![Human Resources Teams izin uygulaması yükleme](./media/hr-teams-leave-app-in-store.png)

Uygulama otomatik olarak oturum açmazsa oturum açmak için **Ayarlar** sekmesini seçin.

![Human Resources Teams izin uygulaması Ayarlar sekmesi](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin. 

Birden fazla Human Resources örneğine erişiminiz varsa **Ayarlar** sekmesinden, hangi ortama bağlanmak istediğinizi seçebilirsiniz.

> [!WARNING]
> Uygulama, şu anda Sistem Yöneticisi güvenlik rolünü desteklememektedir ve bir Sistem Yöneticisi hesabıyla oturum açarsanız hata iletisi görüntüler. Farklı bir hesapla oturum açmak için **Ayarlar** sekmesinde **Hesap değiştir** düğmesini seçin ve ardından Sistem Yöneticisi ayrıcalıklarına sahip olmayan bir kullanıcı hesabıyla oturum açın.
 
## <a name="use-the-bot"></a>Bot kullanma

Uygulama yüklendikten sonra botun, sizin adınıza gerçekleştirebileceği eylem türlerini bildiren bir hoş geldiniz iletisi görüntülenir.

![Human Resources Teams izin uygulaması botun hoş geldiniz iletisi](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Bot ile ilk kez etkileşimde bulunurken oturum açmanız gerekebilir. Oturum açma iletişim kutusunu görmüyorsanız açılır pencerelere izin vermek için tarayıcı ayarlarınızı kontrol edin.

Bottan şunları isteyebilirsiniz:

- Kayıtlı olduğunuz her izin türü için izin bakiyesi bilgisini göstermesini.

   ![Human Resources Teams izin uygulaması bakiyeleri gösterme](./media/hr-teams-leave-app-bot-balances.png)
 
- Belirli bir izin türü hakkında ek ayrıntıların gösterilmesi.

   ![Human Resources Teams izin uygulaması ayrıntıları gösterme](./media/hr-teams-leave-app-bot-details.png)

- Kendiniz için bir izin isteği başlatın.

   ![Human Resources Teams izin uygulaması izin isteği](./media/hr-teams-leave-app-bot-request.png)
 
İzin isteğini başlattıktan sonra günleri kartın içinden ayarlayabilir veya isteğinize ek bilgi eklemek için **Ayrıntıları düzenle**'yi seçebilirsiniz.

![Human Resources Teams izin uygulaması isteği düzenleme](./media/hr-teams-leave-app-bot-edit.png)
 
Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın. Daha sonra geri dönmek için **Taslak olarak kaydet**'e de basabilirsiniz.

![Human Resources Teams izin uygulaması istek gönderme](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Teams'de izninizi yönetme

**İzin** sekmesi şunları görüntülemenizi sağlar:

- Kayıtlı olduğunuz her izin türü için bakiye bilgisini

- Yaklaşan izin istekleri

- İzin süresi istekleri

- Taslak izin istekleri

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Yeni bir istek oluşturma

1. Yeni bir izin isteği oluşturmak için **Yeni istek** seçeneğini belirleyin.

   ![Human Resources Teams izin uygulaması Yeni istek](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Talep ettiğiniz izin süresi için gün veya günleri girin ve ardından **Ekle**'yi seçin.

   ![Human Resources Teams izin uygulaması izin ekleme](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Uygunsa, bir neden kodu girin. Ayrıca açıklama girin ve herhangi bir ek ekleyin.

4. Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın. Daha sonra geri dönmek için **Taslak olarak kaydet**'e de basabilirsiniz.

### <a name="manage-draft-requests"></a>Taslak istekleri yönetme

1. **Taslaklar** sekmesini seçin.

   ![Human Resources Teams izin uygulaması Taslaklar sekmesi](./media/hr-teams-leave-app-drafts-tab.png)

2. İsteği düzenlemek için kalemi veya isteği silmek için çöp kutusunu seçin.

3. Gerekli tüm değişiklikleri yapın. Bilgi girişini tamamladığınızda onay için göndermek üzere **Gönder**'e basın. Daha sonra geri dönmek için **Taslak olarak kaydet**'i de seçebilirsiniz.

   ![Human Resources Teams izin uygulaması taslağı düzenleme](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a>Gizlilik bildirimi

Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir. Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir. LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz. LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar. Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft’un  [Azure bot çerçevesine](https://azure.microsoft.com/services/bot-service/)  aktarılır. 

Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar. LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir. LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir. 

Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz. Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz. 

Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin. 

## <a name="see-also"></a>Ayrıca bkz.

[Microsoft Teams platformunu indirme ve yükleme](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams yardım merkezi](https://support.office.com/teams)</br>
[Teams'de Human Resources uygulaması](hr-admin-teams-leave-app.md)

---
title: Teams'de izin isteklerini yönetme
description: Bu konuda Microsoft Teams uygulamasındaki Dynamics 365 Human Resources uygulamasında, nasıl izin isteneceği gösterilmektedir.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
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
ms.openlocfilehash: c6856e417ee47f8f582f797c5bcedcff23a1432f
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930005"
---
# <a name="manage-leave-requests-in-teams"></a>Teams'de izin isteklerini yönetme

[!include [banner](includes/preview-feature.md)]

Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, hızlı bir şekilde izin isteğinde bulunmanıza ve izin bakiyesi bilgilerinizi doğrudan Microsoft Teams platformunda görüntülemenize olanak tanır. Bilgi istemek ve bir izin isteğini başlatmak için bir sohbet botu ile etkileşim kurabilirsiniz. **İzin** sekmesi, daha ayrıntılı bilgi sağlar. Ek olarak, ekipte yaklaşan izinler hakkında kişilere bilgi ve Human Resources uygulamasının dışındaki sohbetleri gönderebilirsiniz.

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

> [!NOTE]
> Uygulama artık Sistem Yöneticisi güvenlik rolünü destekliyor.
 
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
 
Bir izin talebini başlattıktan sonra, kartın içindeki günleri ayarlayabilirsiniz.

![Human Resources Teams izin uygulaması isteği düzenleme](./media/hr-teams-leave-app-bot-edit.png)
 
Bilgi girişini tamamladığınızda onaya göndermek için **Gönder** öğesini seçin. Daha sonra geri dönmek için **Taslak olarak kaydet**'i de seçebilirsiniz.

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
   
### <a name="respond-to-teams-notifications"></a>Teams bildirimlerini yanıtlama

Siz veya onaylayan taraf olduğunuz bir çalışan izin talebi gönderdiğinde, Teams'de Human Resources uygulamasından bir bildirim alırsınız. Görüntülemek için bildirimi seçebilirsiniz. Bildirimler **Sohbet** alanında da görünür.

Onaylayan iseniz, bildirimden **Onayla** veya **Reddet** seçeneklerini belirleyebilirsiniz. Ayrıca, isteğe bağlı bir ileti de sağlayabilirsiniz.

![Human Resources Teams uygulamasında izin talebi bildirimi](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Yaklaşan izin bilgilerini iş arkadaşlarınıza gönderme

Teams için Human Resources uygulamasını yükledikten sonra, ekiplere veya sohbetlere karşı iş arkadaşlarınıza yaklaşan izinler hakkında bilgi gönderebilirsiniz.

1. Ekipte veya Teams'deki bir sohbette, sohbet penceresinin altındaki Human Resources düğmesini seçin.

   ![Sohbet penceresinin altında Human Resources düğmesi](./media/hr-teams-leave-app-chat-button.png)

2. Paylaşmak istediğiniz izin isteğini seçin. Bir taslak olarak izin isteğini paylaşmak istiyorsanız, önce **Taslaklar**'ı seçin.

   ![Paylaşılacak bir yaklaşan izin isteğini seçme](./media/hr-teams-leave-app-chat-search.png)

İzin talebiniz sohbette gösterilir.

![Human Resources izin istek kartı](./media/hr-teams-leave-app-chat-card.png)

Bir taslak talep paylaştıysanız, taslak olarak görüntülenecektir:

![Human Resources taslak izin istek kartı](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>Ekip izin takviminizi görüntüleme

Astları bulunan bir yönetici iseniz, takımınızın onaylanmış ve bekleyen izinlerini görebilirsiniz.

1. Teams'de Human Resources uygulamasında, **İzin**'i seçin.

2. **Ekip takvimi**'ni seçin.

   ![Human Resources Teams uygulamasında takvimi görüntüleme](./media/hr-teams-leave-app-view-calendar.png)

Takvim, doğrudan astlarınıza ait onaylı ve beklemede olan izinleri görüntüler.

![Human Resources Teams uygulamasında izin takvimi](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a>Sorun Giderme

Human Resources Teams uygulamasında oturum açarken veya uygulamayı kullanırken sorun yaşıyorsanız, bu sorun giderme yönergelerini izleyin. Sorun giderme işleminden sonra hala sorun yaşıyorsanız, desteğe başvurun. Daha fazla bilgi için [Destek alma](hr-admin-troubleshooting-support.md) bölümüne bakın.

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Teams'de Human Resource uygulaması oturumu açılamıyor

Uygulamada oturum açamazsınız, Microsoft Teams'de oturum açarken kullandığınız hesap Dynamics 365 Human Resources'taki bir personel kaydıyla ilişkilendirilmemiş olabilir. Çalışan kaydınızın doğru bir şekilde ilişkilendirildiğinden emin olmak için sistem yöneticinize başvurun.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Teams'deki Human Resources uygulamasındaki izin isteklerini onaylarken hata oluştu

Teams uygulamasında izin isteklerini onaylamaya çalışırken hata alırsanız, aşağıdaki sorun giderme adımlarını gerçekleştirin:

1. Microsoft Teams'te Oturum açmak için kullandığınız hesabın Dynamics 365 Human Resources'a erişmek için kullandığınız hesapla aynı olduğunu doğrulayın.

2. İzin onayı için iş akışı ayarlarını denetleyerek istek için geçerli bir onaylayan olduğunuzu doğrulayın. İzin isteği iş akışları hakkında daha fazla bilgi için bkz. [İzin isteği iş akışı oluşturma](hr-leave-and-absence-workflow.md).

## <a name="privacy-notice"></a>Gizlilik bildirimi

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir. Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir. LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz. LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar. Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft'un  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) servisine aktarılır. 

Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar. LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir. LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir. 

Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz. Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz. 

Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid ve Azure Cosmos DB

Microsoft Teams'de Dynamics 365 Human Resources uygulamasını kullanılırken, belirli müşteri verileri kiracının Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışına akabilir.

Dynamics 365 Human Resources çalışanın izin talebini ve iş akışı görev ayrıntılarını Microsoft Azure Event Grid ve Microsoft Teams uygulamalarına iletir. Bu veriler 24 saate kadar Microsoft Azure Event Grid uygulamasında saklanabilir ve Amerika Birleşik Devletlerinde işlenir, iletim ve bekleyen veri şifrelenir ve eğitim veya hizmet iyileştirmeleri için Microsoft veya onun alt işlemcileri tarafından kullanılmaz. Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).

Human Resources uygulamasında sohbet botu ile konuşurken, görüşme içeriği Azure Cosmos DB uygulamasında depolanabilir ve Microsoft Teams uygulamasına iletilebilir. Bu veriler, Azure Cosmos DB uygulamasında 24 saate kadar depolanabilir ve kiracınızın Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışında işlenerek, aktarım ve geri kalanında şifrelenir ve Microsoft 'un veya hizmet geliştirmeleri için bunların alt işlemcileri tarafından kullanılmaz. Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).
 
Kuruluşunuz veya kuruluşunuzdaki kullanıcılarınız için Microsoft Teams içinde Human Resources uygulamasına erişimi kısıtlamak için, bkz. [Microsoft Teams'deki uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Ayrıca bkz.

[Microsoft Teams platformunu indirme ve yükleme](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams yardım merkezi](https://support.office.com/teams)</br>
[Teams'de Human Resources uygulaması](hr-admin-teams-leave-app.md)

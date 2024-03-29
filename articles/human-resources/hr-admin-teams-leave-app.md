---
title: Teams'te Human Resources uygulaması
description: Bu makale sizi Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulamasıyla tanıştırır.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d29802bdf3411c93f20d710e1f26e541e5022d57
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812199"
---
# <a name="human-resources-app-in-teams"></a>Teams'te Human Resources uygulaması


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, çalışanların hızlı bir şekilde izin istemelerine ve izin bakiyesi bilgilerini Microsoft Teams platformunda görüntülemelerine olanak tanır. Çalışanlar, bilgi istemek için bir botla etkileşime geçebilir. **İzin** sekmesi, daha ayrıntılı bilgi sağlar. Ek olarak, ekipte yaklaşan izinler hakkında kişilere bilgi ve Human Resources uygulamasının dışındaki sohbetleri gönderebilirler.

![Human Resources Teams izinler uygulaması botu.](./media/hr-teams-leave-app-bot.png)

![Human Resources Teams izin uygulaması İzin sekmesi.](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources izin istek kartı.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Yükleme ve ayarlama

Dynamics 365 Human Resources uygulamasını Teams mağazasında bulabilirsiniz. Teams uygulamasını yükleme hakkında bilgi için bkz. [Teams'de izin isteklerini yönetme](hr-teams-leave-app.md).

Teams'de uygulama izinlerini yönetme hakkında bilgi için bkz. [Microsoft Teams platformunda uygulama izin ilkelerini yönetme](/MicrosoftTeams/teams-app-permission-policies).

Kullanıcılarınızın uygulamadaki İzin ve devamsızlık takvimini görüntülemesini istiyorsanız Özellik yönetimindeki **Teams'de İzin ve devamsızlık takvimi** özelliğini etkinleştirmeniz gerekir. Özellikleri etkinleştirme hakkında daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

## <a name="update-app"></a>Uygulamayı güncelleştirme
>[!NOTE]
> 20 Aralık 2021 itibarıyla, Microsoft kiracısında barındırılan Human Resources Uygulaması bot hizmetleri kullanımdan alınacaktır. Yükleme için kullanıma sunulan güncel uzantı (sürüm 1.1.5) etkilenmeyecektir. Ana etki, güncel olmayan uzantı (sürüm 1.1.4) üzerinde olacaktır. Bu sürümdeki sohbet botu çalışmayı durduracaktır. **İzin** sekmesi her iki uzantıda da çalışmaya devam edecek.

1.1.4 sürümünde sohbet botu, iletilere yanıt vermeyi durduracaktır. Örneğin, **Oturum aç**, **Bakiyeleri görüntüle** ve **İzni gör**. Uygulama en son sürüme el ile güncelleştirilmelidir. Daha fazla bilgi için bkz. [Microsoft Teams'de uygulamaları güncelleştirme](/MicrosoftTeams/apps-update-experience).

1.1.5 sürümüne güncelleştirmek için aşağıdaki adımları tamamlayın:
1. Microsoft Teams'de **Uygulamalar**'a gidin.
2. **Human Resources** uygulamasını bulun.
3. **Yükselt**'i seçin.

**Hakkında** sekmesine giderek veya **Kişisel uygulama** bölümüne giderek Human Resources uygulamasının sürümünü kontrol edebilirsiniz. 

![Human Resources **Hakkında** sekmesi.](./media/HR-teams-about.png)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Teams'de Human Resources uygulaması için bildirimleri etkinleştirme

Kullanıcıların Teams uygulamasında izin talebi bildirimlerini almasını istiyorsanız Dynamics 365 Human Resources uygulamasında bildirimleri etkinleştirmelisiniz.

>[!NOTE]
>Yalnızca Teams'e kaydolan ve Dynamics 365 Human Resources Teams uygulamasını kullanan kullanıcılar bildirim alır.

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Bağlantılar**'ı seçin.

3. **Kurulum** altında **Sistem parametreleri**'ni seçin.

4. **Genel** sekmesinde, **Teams uygulaması için bildirimleri etkinleştir** ayarını **Evet** olarak ayarlayın.

   ![Sistem parametrelerinde Teams uygulama bildirimlerini etkinleştirme.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Tüm kullanıcılar için Teams bildirimlerini açmak için sorulduğunda **Evet**'i seçin.

   ![Tüm kullanıcılar için Teams bildirimlerini etkinleştirme.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Bireysel kullanıcılar için Teams bildirimlerini açma veya kapatma

Dynamics 365 Human Resources Teams uygulaması için bildirimleri etkinleştirdikten sonra, bireysel kullanıcılar için bildirimleri açıp kapatabilirsiniz.

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Bağlantılar**'ı seçin.

3. **Kullanıcılar** altında, **Kullanıcı seçenekleri**'ni belirleyin.

4. **İş akışı** sekmesini seçin.

5. Kullanıcı için bildirimleri etkinleştirmek için **Teams uygulaması için bildirimleri etkinleştir** ayarını **Evet** olarak veya kullanıcı için bildirimleri devre dışı bırakmak için **Hayır** olarak ayarlayın.

   ![Kullanıcı seçenekleri İş Akışı sekmesinde Teams uygulaması bildirimlerini etkinleştirme.](./media/hr-admin-teams-leave-app-notifications.png)

6. **Kaydet**'i seçin.

## <a name="supported-languages"></a>Desteklenen diller

Teams'deki Dynamics 365 Human Resources uygulaması aşağıdaki dilleri destekler:

| Yerel Ayar Kimliği | Dil |
| --- | --- |
| de-DE | Almanca (Almanya) |
| es-ES | İspanyolca (İspanya) |
| es-MX | İspanyolca (Meksika) |
| fr-CA | Fransızca (Kanada) |
| fr-FR | Fransızca (Fransa) |
| it-IT | İtalyanca (İtalya) |
| nl-NL | Felemenkçe (Hollanda) |
| pt-BR | Portekizce (Brezilya) |
| tr-TR | Türkçe (Türkiye) |
| zh-CN | Çince (Basitleştirilmiş) |

## <a name="notes"></a>Notlar

Aşağıdaki iş öğeleri gelecekteki sürümler için planlanmıştır:

| İş maddesi | Durum |
| --- | --- |
| İleriki bir tarih için izin işlenirken bakiye yanlıştır. | Tahmin, henüz mevcut değil. Bakiye, geçerli tarih için görüntülenir. |
| **İncelemede** isteği iptal edilemiyor. | Bu işlev şu anda desteklenmemektedir ve gelecekteki bir sürümde eklenecektir. |
| Bakiye bilgileri, bugün itibarıyla hesaplanmaktadır. | Sistem şu anda **İzin ve devamsızlık parametreleri** sayfasında yapılandırılmış olsa bile tahakkuk dönemi itibariyle bakiyeleri göstermemektedir. |

## <a name="troubleshooting"></a>Sorun Giderme

Bir kullanıcı Human Resources Teams uygulamasında oturum açarken veya uygulamayı kullanırken sorun yaşarsa bu sorun giderme yönergelerini izleyin. Sorun giderme işleminden sonra hala sorun yaşıyorsanız, desteğe başvurun. Daha fazla bilgi için [Destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) bölümüne bakın.

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Teams İnsan Kaynakları uygulamasının güncel olduğundan emin olun
Teams İnsan Kaynakları uygulamasıyla ilgili sorunlarla karşılaşırsanız en son sürümü çalıştırdığınızı onaylamanız gerekir. Varsayılan sürüm 1.1.5'tir. Teams uygulamasını güncelleştirme hakkında yönergeler için [Teams belgelerine](/MicrosoftTeams/apps-update-experience) bakın.

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Teams'de Human Resource uygulaması oturumu açılamıyor

Bir kullanıcı uygulamada oturum açamadığı için sizinle iletişim kurarsa kullanıcının Human Resources'ta ilişkili bir çalışan kaydı olduğunu doğrulayın.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Teams'deki Human Resources uygulamasındaki izin isteklerini onaylarken hata oluştu

Kullanıcı Teams uygulamasında izin isteklerini onaylamaya çalışırken hata alırsa aşağıdaki sorun giderme adımlarını deneyin:

1. Teams hesabının Human Resources'a erişmek için kullanılan hesapla aynı olduğunu doğrulayın.

2. İzin onayı için iş akışı ayarlarını denetleyerek istek için geçerli bir onaylayan olduklarını doğrulayın. İzin isteği iş akışları hakkında daha fazla bilgi için bkz. [İzin isteği iş akışı oluşturma](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>İzin onaylayanları, izin taleplerini onaylamak üzere Teams sohbet iletilerini almıyor

1. Ortam ve kullanıcı için bildirimlerin etkinleştirildiğinden emin olun. Daha fazla bilgi için bkz. [Teams'teki Human Resources uygulamasında bildirimleri etkinleştirme](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ve [Bireysel kullanıcılar için Teams bildirimlerini etkinleştirme](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Kullanıcıların, **Sohbet** sekmesinde izin isteklerini onaylamak için kullandıkları kimlik bilgileriyle oturum açtığından emin olun. Doğru kimlik bilgileriyle oturum açmak için "oturumu Kapat" ve ardından "oturum aç" iletilerini kullanın.

3. Sorun devam ederse, sistem yöneticisi olarak **İş Olayları sistem** toplu işinin durumunu denetleyin. **Bekleme** veya **Yürütme** aşamasındaysa, birkaç dakika sonra yeniden denetleyin. Durum değişmeden kalırsa, bir destek bileti oluşturun. Böylece ekibimiz sorunu gidermeye yardımcı olur.

## <a name="privacy-notice"></a>Gizlilik bildirimi

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir. Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir. LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz. LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar. Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft'un  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) servisine aktarılır.

Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar. LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir. LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure Bot Framework'e gönderilebilir. 

Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz. Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz. 

Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin.

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure Event Grid ve Azure Cosmos DB

Microsoft Teams'te Dynamics 365 Human Resources uygulamasını kullanılırken, belirli müşteri verileri kiracının Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışına akabilir.

Dynamics 365 Human Resources çalışanın izin talebini ve iş akışı görev ayrıntılarını Microsoft Azure Event Grid ve Microsoft Teams uygulamalarına iletir. Bu veriler 24 saate kadar Microsoft Azure Event Grid uygulamasında saklanabilir ve Amerika Birleşik Devletlerinde işlenir, iletim ve bekleyen veri şifrelenir ve eğitim veya hizmet iyileştirmeleri için Microsoft veya onun alt işlemcileri tarafından kullanılmaz. Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Human Resources uygulamasında sohbet botu ile konuşurken, görüşme içeriği Azure Cosmos DB uygulamasında depolanabilir ve Microsoft Teams uygulamasına iletilebilir. Bu veriler, Azure Cosmos DB uygulamasında 24 saate kadar depolanabilir ve kiracınızın Human Resources hizmetinin dağıtıldığı coğrafi bölgenin dışında işlenerek, aktarım ve geri kalanında şifrelenir ve Microsoft 'un veya hizmet geliştirmeleri için bunların alt işlemcileri tarafından kullanılmaz. Verilerinizin Teams içinde nerede depolandığını anlamak için bkz. [Microsoft Teams içinde verilerin konumu](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Kuruluşunuz veya kuruluşunuzdaki kullanıcılarınız için Microsoft Teams içinde Human Resources uygulamasına erişimi kısıtlamak için, bkz. [Microsoft Teams'deki uygulama izin ilkelerini yönetme](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Ayrıca bkz. 

[Microsoft Teams platformunu indirme ve yükleme](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams yardım merkezi](https://support.office.com/teams)</br>
[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

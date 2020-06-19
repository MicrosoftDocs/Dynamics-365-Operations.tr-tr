---
title: Teams'de Human Resources uygulaması
description: Bu konu sizi Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulamasıyla tanıştırır.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431142"
---
# <a name="human-resources-app-in-teams"></a>Teams'de Human Resources uygulaması

[!include [banner](includes/preview-feature.md)]

Microsoft Teams platformundaki Microsoft Dynamics 365 Human Resources uygulaması, çalışanların hızlı bir şekilde izin istemelerine ve izin bakiyesi bilgilerini Microsoft Teams platformunda görüntülemelerine olanak tanır. Çalışanlar, bilgi istemek için bir botla etkileşime geçebilir. **İzin** sekmesi, daha ayrıntılı bilgi sağlar.

![Human Resources Teams izinler uygulaması botu](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teams izin uygulaması İzin sekmesi](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Yükleme ve ayarlama

Human Resources uygulamasını Teams mağazasında bulabilirsiniz. Teams uygulamasını yükleme hakkında bilgi için bkz. [Teams'de izin isteklerini yönetme](hr-teams-leave-app.md).

Teams'de uygulama izinlerini yönetme hakkında bilgi için bkz. [Microsoft Teams platformunda uygulama izin ilkelerini yönetme](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="known-issues"></a>Bilinen sorunlar

| Çıkış | Durum |
| --- | --- |
| Hata: Bağlanılacak ortam bulunurken bir sorun oluştu. | Kullanıcının bir veya daha fazla İnsan Kaynakları ortamına erişebileceğini doğrulasanız bile bu hatayı alabilirsiniz. Ayrıca, beklediğiniz tüm ortamları görmeyebilirsiniz. Bu sorunu düzeltdik, sorunu gidermek için kullanıcıyı silin ve yeniden içe aktarın. |
| İleriki bir tarih için izin işlenirken bakiye yanlıştır. | Tahmin, henüz mevcut değil. Bakiye, geçerli tarih için görüntülenir. |
| Var olan bir istekteki alınan izin saatlerini düşerken **Kalan bakiye** artacağına azalır. | Gelecekte, bu bilinen sorunu ele alacağız. Görüntü yanlış, ancak gönderildikten sonra doğru miktarlara ayarlanır. |
| Aynı tarihler için iki **Yaklaşan izin** kartı görüntülenir. | Kartlar, ayrı gönderimleri temsil eder. Geri bildirim almaya ve ayarlamalar yapmaya devam edeceğiz. |
| **İncelemede** isteği iptal edilemiyor. | Bu işlev şu anda desteklenmemektedir ve gelecekteki bir sürümde eklenecektir. |
| Bakiye bilgileri, bugün itibarıyla hesaplanmaktadır. | Sistem şu anda İzin ve devamsızlık parametrelerinde yapılandırılmış olsa bile tahakkuk dönemi itibariyle bakiyeleri göstermemektedir. |

## <a name="privacy-notice"></a>Gizlilik bildirimi

Microsoft Teams platformundaki Dynamics 365 Human Resources botu ile kullanıcının metin girişleri, temel alınan sorguyu/amacı anlamak için analiz edilir. Kullanıcının "Arama hesabı Contoso" şeklindeki girişi Microsoft’un Cognitive Service'lerinden biri olan Language Understanding Intelligent Service (LUIS) adındaki hizmete yönlendirilir. LUIS hakkında daha fazla bilgiyi  [buradan](https://www.luis.ai/) edinebilirsiniz. LUIS hizmeti, kullanıcı girdisinin amacı (bu durumda amaç bilgi bulmaktır) ile amaçlanan hedef varlığı (bu durumda, amaçlanan varlık Contoso adlı bir hesaptır) belirginleştirir veya anlar. Bu bilgiler daha sonra, Dynamics 365 Human Resources uygulamasından gelen verilerle etkileşime giren ve kullanıcı sorgusu için istenen bilgileri alan Microsoft’un  [Azure bot çerçevesine](https://azure.microsoft.com/services/bot-service/)  aktarılır. 

Botu kurarak ve kullanıma erişimine izin vererek LUIS hizmetinin ve Azure bot çerçevesinin, girdinin arkasındaki amacı işlemesine izin vermesini kabul edersiniz; bu da gelişmiş bir etkileşimli kullanıcı deneyimi sağlar. LUIS hizmeti ve Azure bot çerçevesi, Dynamics 365 Human Resources ile karşılaştırıldığında farklı uyum düzeylerine sahip olabilir. LUIS hizmeti, yalnızca kullanıcı sorgularına erişebilecek ve kullanıcının Dynamics 365 Human Resources verilerine veya hesabına bağlanacak şekilde tasarlanmamış olmasına rağmen Dynamics 365 Human Resources botunun bir kullanıcısı; Müşteri Verilerini, Kişisel Verileri veya diğer verileri içeren bir sorguya gönüllü olarak girebilir ve bu sorgu içeriğini LUIS hizmetine ve Azure bot çerçevesine gönderilebilir. 

Kullanıcıya ait sorguların ve iletilerin içeriği LUIS sisteminde en fazla 30 gün saklanır, bekleme sırasında şifrelenir ve eğitim veya hizmet iyileştirmesi için kullanılmaz. Cognitive Services hakkında daha fazla bilgiyi  [buradan](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/) edinebilirsiniz. 

Microsoft Teams platformundaki uygulamaların yönetici ayarlarını yönetmek için [Microsoft Teams yönetici merkezi](https://admin.teams.microsoft.com/)'ne gidin. 

## <a name="see-also"></a>Ayrıca bkz. 

[Microsoft Teams platformunu indirme ve yükleme](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams yardım merkezi](https://support.office.com/teams)</br>
[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md)


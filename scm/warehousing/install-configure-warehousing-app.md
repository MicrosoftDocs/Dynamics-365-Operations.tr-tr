---
title: "Yükleme ve Microsoft Dynamics 365 yapılandırmak için işlemleri & #8211; Depolama"
description: "Bu konuda, yükleme ve yapılandırma işlemlerini - depolama için Microsoft Dynamics 365 açıklamaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Yükleme ve Microsoft Dynamics 365 yapılandırmak için işlemleri & #8211; Depolama

Bu konuda, yükleme ve yapılandırma işlemlerini - depolama için Microsoft Dynamics 365 açıklamaktadır.

Dynamics 365 işlemleri - depolama için bir kullanılabilir Google kullan mağaza ve mağaza Windows uygulamasıdır. Microsoft Dynamics 365 işlemleri için geçerli sürümü için bu app ambar görevler için kullanılan aygıtlar kendinden dağıtım anlamına gelir tek başına bir bileşen olarak sağlanır. App, Dynamics 365 içinde işlem ortamını kullanmak için her aygıt üzerindeki uygulama yükleme ve işlem ortamı için Dynamics 365 bağlanmak için yapılandırın. Bu konuda aygıtlarınızda app yükleneceğini açıklar. App, Dynamics 365 işlem ortamı için bağlanmak için yapılandırmak nasıl da açıklamaktadır.

## <a name="prerequisites"></a>Önkoşullar
App Android ve Windows işletim sistemlerinde kullanılabilir. Bu uygulamayı kullanmak için aşağıdaki desteklenen işletim sistemlerinin aygıtlarınızda yüklü olması gerekir. Dynamics 365 işlemleri için desteklenen sürümlerinden biri olmalıdır. Bilgileri aşağıdaki tabloda yüklemeyi desteklemek donanım ve yazılım ortamınızın hazır olmadığını değerlendirmek için kullanın.

| Platform                    | Sürüm                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (tüm sürümler)                                                                                                                                                   |
| Dynamics 365 işlemleri için | Microsoft Dynamics 365 işlemleri sürüm 1611 - veya - Microsoft Dynamics Dynamics AX sürüm 7.0/7.0.1 için ve Microsoft Dynamics AX platform 2 KB 3210014 düzeltme ile güncelleştirin. |

## <a name="get-the-app"></a>App alın
-   Windows (UWP) - [Dynamics Windows deponun depolama işlemleri - 365](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics Google kullan deposu depolama işlemleri - 365](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Active Directory içinde bir web hizmeti uygulaması oluştur
Server işlemleri için belirli bir Dynamics 365 ile etkileşimli çalışmak uygulamayı etkinleştirmek için web hizmeti uygulaması Azure Active Directory'de işlemleri Kiracı için Dynamics 365 için kaydetmeniz gerekir. Güvenlik nedenleriyle, kullandığınız her aygıt için bir web hizmeti uygulaması oluşturmanızı öneririz. Azure Active Directory (AD Azure) bir web hizmeti uygulaması oluşturmak için aşağıdaki adımları izleyin:

1.  Bir web tarayıcısında Git <https://manage.windowsazure.com>.
2.  Azure abonelik erişimi olan kullanıcı adını ve parolasını girin.
3.  Azure Portal'da, sol gezinti bölmesinde tıklatın **Active Directory**. [](./media/wh-01-active-directory-example.png)[![ne-01-etkin-dizin-örnek](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Kılavuzda, Dynamics 365 tarafından işlemleri için kullanılan Active Directory örneği seçin.
5.  Üstteki araç çubuğunda tıklatın **uygulamalar**. [![ne-02-etkin-dizin-uygulamalar](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Alt bölmede **Ekle**. **Uygulama eklemek** Sihirbazı'nı başlatır.
7.  Seçin ve uygulama için bir ad girin **Web uygulaması ve/veya API web**. [![wh-03-Active-Directory-Add-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Uygulama URL'SİYLE kök URL işlemleri, Kiracı olan oturum açma URL'si girin. Oturum açma URL'si etkin olarak app kimlik doğrulamasına kullanılmakta olan değil, ancak zorunlu bir alandır. Aynı URL'ye uygulaması kimliği URI'si alanına girin. [![ne-04-ad-Ekle-Özellikler](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Git **yapılandırma** sekme. [![ne-05-ad-yapılandırma-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Gördüğünüz kadar aşağı kaydırın **diğer uygulamalara izin** bölüm. ' I **uygulama eklemek**. [![wh-06-ad-App-Add-Permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Seçin **Microsoft Dynamics ERP** listesinde. ' I **tamamlamak onay** sayfanın sağ köşedeki düğme. [![ne-07-ad-select-izinleri](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. İçinde **temsilci izinleri** listesinde, tüm onay kutularını seçin. Click **Save**. [![ne-08-ad-temsilci-izinleri](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Aşağıdaki bilgileri not alın:
    -   **İstemci kimliği** - page up göreceğiniz kaydırırken **istemci kimliği** görüntülenir.
    -   **Anahtar** - de **tuşları** bölümünde süre seçerek bir anahtar oluşturun ve anahtar kopyalayın. Bu anahtar daha sonra için olarak anılacaktır **istemci gizli**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Oluşturma ve Dynamics 365 işlemleri için bir kullanıcı hesabı yapılandırma
Dynamics 365 Azure AD uygulamanızı kullanmak işlemleri için etkinleştirmek için aşağıdaki yapılandırma adımları izlemeniz gerekir:

1.  Kiracı işlemleri için Dynamics 365 Azure Active Directory'de yeni bir kullanıcı hesabı oluşturun. Server işlemleri için Dynamics 365 sunan ambar App'in özel hizmete erişmek için bu kullanıcı hesabının amacı budur. Bu adımı tamamladıktan sonra WMDP e-posta adresi ve parola WMDP oluşan WMDP kullanıcı kimlik olacaktır. Kullanıcılar için Azure AD eklemek için temel adımlar hakkında bilgi edinmek için ve işlemleri için Dynamics 365 başvurmak için Bu öğretici: [için Microsoft Dynamics 365 abonelik işlemleri için kaydolun](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Dynamics 365 ambar app kullanıcı kimlik bilgilerini karşılık gelen kullanıcı işlemleri için oluşturun.
    1.  İşlemler için Dynamics 365 içinde gitmek **Sistem Yönetimi**&gt;**ortak**&gt;**kullanıcı**.
    2.  Yeni bir kullanıcı oluşturun.
    3.  Aşağıdaki ekran görüntüsünde gösterildiği gibi ambar mobil aygıt kullanıcı atayın. [![wh-09-Add-User-Security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Azure Active Directory uygulamanızın ambar app kullanıcı ile ilişkilendirir.
    1.  İşlemler için Dynamics 365 içinde gitmek **Sistem Yönetimi**&gt;**Kurulum**&gt;**Azure Active Directory uygulamaları**.
    2.  Yeni satır oluşturun.
    3.  Girin **istemci kimliği** (son bölümde elde edilen) bir ad verin ve önceden oluşturulmuş kullanıcı seçin. Kayıp olasılığına kolayca kendi erişim Dynamics 365 işlemleri için bu sayfadan kaldırabilirsiniz, böylece tüm aygıtlarınızın etiketi öneririz. [![ne-10-ad-uygulamalar-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Uygulama yapılandırma
Azure Reklam uygulaması aracılığıyla server işlemleri için Dynamics 365 bağlanmak için aygıt üzerindeki uygulama yapılandırmanız gerekir. Bunu yapmak için aşağıdaki adımları izleyin.

1.  App içinde gitmek **bağlantı ayarlarını**.
2.  NET **Demo modunda** alan. [![wh-11-App-Connection-Settings-Demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Aşağıdaki bilgileri girin:- **Azure Active directory istemci kimliği** -istemci kimliği "Active Directory web hizmeti uygulaması oluştur" 13 adımda elde edilir. - **Azure Active directory istemci gizli** -istemci gizli, "Active Directory web hizmeti uygulaması oluştur" 13 adımda elde edilir. - **Azure Active directory kaynak** -Azure AD dizini kaynak Dynamics 365 işlemleri kök URL'sini gösterir. **Not**: Bu alanda bir eğik çizgi (/) ile bitmez. - **Azure Active directory Kiracı** -Azure AD dizini Kiracı ile Dynamics 365 server işlemleri için kullanılan: https://login.windows.net/&lt;your-AD-Kiracı-ID&gt;. Örneğin: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Not**: Bu alanda bir eğik çizgi (/) ile bitmez. - **Şirket** -tüzel kişilik içinde Dynamics 365 uygulama bağlanmak istediğiniz işlemleri için girin. [![ne-12-app-bağlantı-ayarları](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Seçin **geri** uygulama sol üst köşesindeki düğmesini. Uygulama şimdi, Dynamics 365 server işlemleri için bağlanacak ve ambar çalışanı için oturum açma ekranı görüntülenir. [![ne 13 oturum açma ekranı](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Bir aygıtı Kaldır
Durumunda kayıp ya da güvenliği aşılmış bir aygıt, aygıt işlemleri için Dynamics 365 erişimi kaldırmanız gerekir. Erişimi kaldırmak için önerilen işlemi aşağıdaki adımları açıklanmaktadır.

1.  İşlemler için Dynamics 365 içinde gitmek **Sistem Yönetimi**&gt;**Kurulum**&gt;**Azure Active Directory uygulamaları**.
2.  Erişimi kaldırmak istediğiniz aygıta karşılık gelen satırı silin. DOWN Not **istemci kimliği** kaldırılan aygıt için kullanılır.
3.  Azure Klasik portalında oturumu <https://manage.windowsazure.com>.
4.  ' I **Active Directory** sol menüsünde simgesini ve ardından istediğiniz dizini tıklatın.
5.  Üst menüsünde **uygulamalar**ve sonra yapılandırmak istediğiniz uygulamayı tıklatın. **Hızlı Başlat** çoklu oturum açma ve diğer yapılandırma bilgilerini sayfa görüntülenir.
6.  ' I **yapılandırma** sekme, aşağı kaydırın ve emin olmak **istemci kimliği** uygulaması adım 2'de bu bölümde olduğu gibi aynıdır.
7.  ' I **Sil** Komut çubuğundaki düğmesini.
8.  ' I **Evet** onay iletisinde.




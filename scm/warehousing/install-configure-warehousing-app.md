---
title: "Microsoft Dynamics 365 for Operations &#8211; Ambarlama yükleme ve yapılandırma"
description: "Bu konu, Microsoft Dynamics 365 for Operations - Ambarlama&quot;nın nasıl yükleneceğini ve yapılandırılacağnı açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 46b4809ae89f90295766e95ce78a8f019de0cdae
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Operations &#8211; Ambarlama yükleme ve yapılandırma

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Operations - Ambarlama'nın nasıl yükleneceğini ve yapılandırılacağnı açıklar.

Dynamics 365 for Operations - Ambarlama, Google Play Store ve Windows Mağazası'nda bulunan bir uygulamadır. Microsoft Dynamics 365 for Operations'un geçerli sürümü için bu uygulama, tek başına bir bileşen olarak sağlanır, bu da ambar görevleri için kullanılan cihazlarda kendinden dağıtım anlamına gelir. Uygulamayı Dynamics 365 for Operations ortamınızda kullanmak için uygulamayı tüm cihazlarınıza indirmeli ve sizin Dynamics 365 for Operations ortamınıza bağlanmak üzere yapılandırmalısınız. Bu konu, cihazlarınıza uygulamanın nasıl yükleneceğini açıklar. Ayrıca uygulamanın Dynamics 365 for Operations ortamınıza nasıl bağlanacağını da açıklar.

## <a name="prerequisites"></a>Önkoşullar
Uygulama Android ve Windows işletim sistemlerinde kullanılabilir. Bu uygulamayı kullanmak için aşağıda belirtilen, desteklenen işletim sistemlerinin cihazlarınızda yüklü olması gerekir. Dynamics 365 for Operations'un aşağıda belirtilen, desteklenen sürümlerinden birine de sahip olmalısınız. Aşağıdaki tabloda belirtilen verileri, donanım ve yazılım ortamınızın kurulumu desteklemeyi hazır olup olmadığını değerlendirmek için kullanın.

| Platform                    | Sürüm                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (tüm sürümler)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations sürüm 1611 veya Microsoft Dynamics AX sürüm 7.0/7.0.1 ve Microsoft Dynamics AX platform güncelleştirmesi 2 düzeltme KB 3210014 |

## <a name="get-the-app"></a>Uygulamayı edinin
-   Windows (UWP) - [Dynamics 365 for Operations - Ambarlama Windows Mağazası'nda](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Ambarlama Google Play Mağazası'nda](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Active Directory içinde bir web hizmeti uygulaması oluştur
Uygulamanın belirli bir Dynamics 365 for Operations sunucusu ile etkileşime girmesini etkinleştirmek için önce bir web hizmet uygulamasını, Dynamics 365 for Operations kiracısında bir Azure Active Directory içinde kaydetmelisiniz. Güvenlik nedeniyle, kullandığınız her cihaz için bir web hizmeti uygulaması oluşturmanızı öneririz. Azure Active Directory (AD Azure) içinde bir web hizmeti uygulaması oluşturmak için aşağıdaki adımları izleyin:

1.  Bir web tarayıcısında <https://manage.windowsazure.com> adresine gidin.
2.  Azure aboneliğine erişimi olan kullanıcının adını ve parolasını girin.
3.  Azure Portal'da, sol gezinti bölmesinde tıklatın **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-örnek](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Kılavuzda, Dynamics 365 for Operations tarafından kullanılan Active Directory örneğini seçin.
5.  Üstteki araç çubuğunda **Uygulamalar** üzerine tıklatın. [![wh-02-active-directory-uygulamaları](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Alt panoda, **Ekle** üzerine tıklatın. **Uygulama eklemek** sihirbazı başlar.
7.  Uygulama için bir ad girin ve **Web uygulaması ve/veya web API'si** seçin. [![wh-03-active-directory-uygulama-ekle](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Kiracınızın uygulama URL'si olan, kök Operations URL'si oturum açma URL'sini girin. Oturum açma URL'si uygulamanın kimlik doğrulamasında şu an aktif olarak kullanılmamaktadır, ancak zorunlu bir alandır. Aynı URL'yi Uygulama kimliği URI alanına girin. [![wh-04-ad-özellikler-ekle](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  **Yapılandır** sekmesine git. [![wh-05-ad-yapılandırma-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. **İzinler ve diğer uygulamalar** bölümünü görene kadar aşağı kaydırın. **Başvuru ekle** üzerine tıklayın. [![wh-06-ad-uygulama-izinleri-ekle](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Listede **Microsoft Dynamics ERP**'yi seçin. Sayfanın sağ köşesindeki **Tam denetim** düğmesini tıklatın. [![wh-07-ad-izinleri-seç](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. **Temsilci İzinleri** listesinde, tüm onay kutularını seçin. **Kaydet**'i tıklatın. [![wh-08-ad-temsilci-izinleri](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Aşağıdaki bilgileri not alın:
    -   **İstemci kimliği** - Sayfada yukarı kaydırırken **İstemci kimliği**'nin görüntülendiğini görürsünüz.
    -   **Anahtar** - **Anahtarlar** bölümünde, süre seçerek bir anahtar oluşturun ve anahtarı kopyalayın. Bu anahtar daha sonra **İstemci sırrı** olarak anılacaktır.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Dynamics 365 for Operations içinde bir kullanıcı hesabı oluşturma ve yapılandırma
Dynamics 365 for Operations'ın Azure AD uygulamanızı kullanmasını sağlamak için, aşağıdaki yapılandırma adımlarını tamamlamanız gerekir:

1.  Dynamics 365 for Operations kiracısı için Azure Active Directory'de yeni bir kullanıcı hesabı oluşturun. Bu kullanıcı hesabının amacı, Dynamics 365 for Operations sunucusunun açığa çıkarttığı ambarlama uygulamasının belirli özel hizmetlerine erişmektir. Bu adımı tamamladıktan sonra, bir WMDP e-posta adresi ve WMDP parolasından oluşan WMDP kullanıcı kimlik bilgilerine sahip olacaksınız. Azure AD ve Dynamics 365 for Operations için kullanıcılar eklemek hakkında temel adımları öğrenmek için bu eğitime göz atın: [Bir Microsoft Dynamics 365 for Operations aboneliğine kaydolun](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Ambarlama uygulaması kullanıcı kimlik bilgilerine karşılık gelne bir Dynamics 365 for Operations kullanıcı oluşturun.
    1.  Dynamics 365 for Operations içerisinde **Sistem Yönetimi** &gt; **Ortak** &gt; **Kullanıcılar** konumuna gidin.
    2.  Yeni bir kullanıcı oluşturun.
    3.  Ambarı, mobil cihaz kullanıcısına, aşağıdaki ekran görüntüsünde görüldüğü gibi atayın. [![wh-09-kullanıcı-güvenlik-rolü-ekle](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Azure Active Directory uygulamanızı, ambar uygulaması kullanıcısı ile ilişkilendirin.
    1.  Dynamics 365 for Operations içerisinde **Sistem yönetimi** &gt; **Kurulum** &gt; **Azure Active Directory uygulamaları** konumuna gidin.
    2.  Yeni satır oluşturun.
    3.  **İstemci kimliği**'ni (son bölümde elde edilen) girin, bir ad verin ve önceki oluşturulan kullanıcıyı seçin. Tüm cihazlarınızı etiketlemenizi öneririz, böylece kayboldukları takdirde onların Dynamics 365 for Operations erişimlerini bu sayfadan kolayca kaldırabilirsiniz. [![wh-10-ad-uygulamalar-formu](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Uygulamayı yapılandır
Azure AD uygulaması aracılığıyla Dynamics 365 for Operations sunucusuna erişebilmek için cihaz üzerindeki uygulamayı yapılandırmanız gerekir. Bunu yapmak için aşağıdaki adımları tamamlayın.

1.  Uygulamanın içinde **Bağlantı ayarları**'na gidin.
2.  **Demo modu** alanını temizleyin. [![wh-11-uygulama-bağlantı-ayarları-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Aşağıdaki bilgiyi girin: - **Azure Active directory istemci kimliği** - İstemci kimliği, "Active Directory'de bir web hizmeti uygulaması oluştur" içindeki 13. adımdan edinilir. **Azure Active directory istemci sırrı** - İstemci sırrı, "Active Directory'de bir web hizmeti uygulaması oluştur" içindeki 13. adımdan edinilir. - **Azure Active directory kaynağı** -Azure AD dizini kaynağı, Dynamics 365 for Operations kök URL'sini gösterir. **Not**: Bu alanı bir eğik çizgi (/) ile bitirmeyin. - **Azure Active directory kiracısı** - Dynamics 365 for Operations sunucusu ile kullanılan Azure AD dizini kiracısı: https://login.windows.net/&lt;sizin-AD-kiracı-kimliğiniz&gt;. Örneğin: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Not**: Bu alanı bir eğik çizgi (/) ile bitirmeyin. - **Şirket** - Uygulamanın bağlanmasını istediğiniz tüzel varlığı, Dynamics 365 for Operations içerisinde girin. [![wh-12-uygulama-bağlantı-ayarları](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Uygulamanın sol üst köşesindeki **Geri** düğmesini seçin. Uygulama şimdi, Dynamics 365 for Operations sunucunuza bağlanır ve ambar çalışanı için oturum açma ekranı görüntülenir. [![wh-13-oturum-açma-ekranı](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Cihazın erişimini kaldır
Kayıp veya güvenliği aşılmış bir cihaz durumunda, bu cihaz için Dynamics 365 for Operations erişimini kaldırmanız gerekir. Aşağıdaki adımlar, erişimi kaldırmak için önerilen adımları açıklar.

1.  Dynamics 365 for Operations içerisinde **Sistem yönetimi** &gt; **Kurulum** &gt; **Azure Active Directory uygulamaları** konumuna gidin.
2.  Erişimini kaldırmak istediğiniz cihaza karşılık gelen satırı silin. Kaldırılan cihaz için **İstemci Kimliğini** not alın.
3.  <https://manage.windowsazure.com> adresinden Azure klasik portala oturum açın.
4.  Sol menüdeki **Active Directory** menüsüne tıklayın ve daha sonra istediğiniz dizine tıklayın.
5.  Üst menüde, **Uygulamalar**üzerine tıklayın ve daha sonra yapılandırmak istediğiniz uygulamayı tıklatın. **Hızlı Başlat** sayfası, tek oturum açma ve diğer yapılandırma bilgilerine sahip bir sayfayla görüntülenir.
6.  **Yapılandır** sekmesini tıklatın, aşağı kaydırın ve uygulamanın **İstemci kimliği**'nin bu bölümün 2. adımındaki ile aynı olduğundan emin olun.
7.  Komut çubuğunda **Sil** düğmesini tıklatın.
8.  Onay iletisinde **Evet**'i tıklatın.






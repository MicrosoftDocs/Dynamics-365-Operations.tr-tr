---
title: "Microsoft Dynamics 365 for Finance and Operations &#8211; Ambarlama yükleme ve yapılandırma"
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations - Ambarlama'nın nasıl yükleneceğini ve yapılandırılacağnı açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 2e6b0fb81396eef945dbce3be8aee17c9fd455bc
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Finance and Operations &#8211; Ambarlama yükleme ve yapılandırma

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Finance and Operations - Ambarlama'nın nasıl yükleneceğini ve yapılandırılacağnı açıklar.

Finance and Operations - Ambarlama, Google Play Store ve Windows Mağazası'nda bulunan bir uygulamadır. Finance and Operations'un geçerli sürümü için bu uygulama, tek başına bir bileşen olarak sağlanır, bu da ambar görevleri için kullanılan cihazlarda kendinden dağıtım anlamına gelir. Uygulamayı Finance and Operations ortamınızda kullanmak için uygulamayı tüm cihazlarınıza indirmeli ve sizin Finance and Operations ortamınıza bağlanmak üzere yapılandırmalısınız. Bu konu, cihazlarınıza uygulamanın nasıl yükleneceğini açıklar. Ayrıca uygulamanın Finance and Operations ortamınıza nasıl bağlanacağını da açıklar.

## <a name="prerequisites"></a>Ön koşullar
Uygulama Android ve Windows işletim sistemlerinde kullanılabilir. Bu uygulamayı kullanmak için aşağıda belirtilen, desteklenen işletim sistemlerinin cihazlarınızda yüklü olması gerekir. Finance and Operations'un aşağıda belirtilen, desteklenen sürümlerinden birine de sahip olmalısınız. Aşağıdaki tabloda belirtilen verileri, donanım ve yazılım ortamınızın kurulumu desteklemeyi hazır olup olmadığını değerlendirmek için kullanın.

| Platform                    | Sürüm                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (tüm sürümler)                                                                                                                                                   |
| Finance and Operations | Microsoft Finance and Operations sürüm 1611 <br>-veya- <br>Microsoft Dynamics Dynamics AX sürüm 7.0/7.0.1 ve Microsoft Dynamics AX platform güncelleştirmesi 2, KB 3210014 düzelmesiyle |

## <a name="get-the-app"></a>Uygulamayı edinin
-   Windows (UWP) - [Finance and Operations - Ambarlama Windows Mağazası'nda](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - [Finance and Operations - Ambarlama Google Play Mağazası'nda](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operations - Ambarlama Zebra App Galerisi'nde](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>Active Directory içinde bir web hizmeti uygulaması oluştur
Uygulamanın belirli bir Finance and Operations sunucusu ile etkileşime girmesini etkinleştirmek için önce bir web hizmet uygulamasını, Finance and Operations kiracısında bir Azure Active Directory içinde kaydetmelisiniz. Güvenlik nedeniyle, kullandığınız her cihaz için bir web hizmeti uygulaması oluşturmanızı öneririz. Azure Active Directory (AD Azure) içinde bir web hizmeti uygulaması oluşturmak için aşağıdaki adımları izleyin:

1.  Bir web tarayıcısında <https://manage.windowsazure.com> adresine gidin.
2.  Azure aboneliğine erişimi olan kullanıcının adını ve parolasını girin.
3.  Azure Portal'da, sol gezinti bölmesinde tıklatın **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-örnek](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Kılavuzda, Finance and Operations tarafından kullanılan Active Directory örneğini seçin.
5.  Üstteki araç çubuğunda **Uygulamalar** üzerine tıklatın. [![wh-02-active-directory-uygulamaları](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Alt panoda, **Ekle** üzerine tıklatın. **Uygulama eklemek** sihirbazı başlar.
7.  Uygulama için bir ad girin ve **Web uygulaması ve/veya web API'si** seçin. [![wh-03-active-directory-uygulama-ekle](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Web uygulamanızın URL'si olan oturum açma URL'sini girin. Bu URL, dağıtım URL'niz ile aynıdır, ancak sonuna oauth eklenir. Uygulama Kodu URI'sini girin, bu değer zorunludur, ancak kimlik doğrulaması için gerekli değildir. Bu Uygulama Kodu URI'sinin, https://contosooperations/wmapp gibi bir sahte URI olduğundan emin olun çünkü dağıtım URL'nizi kullanmak, Excel eklentisi gibi diğer AAD uygulamaları ile oturum açma sorunlarına sebep olabilir. [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  **Yapılandır** sekmesine git. [![wh-05-ad-yapılandırma-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. **İzinler ve diğer uygulamalar** bölümünü görene kadar aşağı kaydırın. **Başvuru ekle** üzerine tıklayın. [![wh-06-ad-uygulama-izinleri-ekle](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Listede **Microsoft Dynamics ERP**'yi seçin. Sayfanın sağ köşesindeki **Tam denetim** düğmesini tıklatın. [![wh-07-ad-izinleri-seç](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. **Temsilci İzinleri** listesinde, tüm onay kutularını seçin. **Kaydet**'i tıklatın. [![wh-08-ad-temsilci-izinleri](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Aşağıdaki bilgileri not alın:
    -   **İstemci kimliği** - Sayfada yukarı kaydırırken **İstemci kimliği**'nin görüntülendiğini görürsünüz.
    -   **Anahtar** - **Anahtarlar** bölümünde, süre seçerek bir anahtar oluşturun ve anahtarı kopyalayın. Bu anahtar daha sonra **İstemci sırrı** olarak anılacaktır.

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Finance and Operations içinde bir kullanıcı hesabı oluşturma ve yapılandırma
Finance and Operations'ın Azure AD uygulamanızı kullanmasını sağlamak için, aşağıdaki yapılandırma adımlarını tamamlamanız gerekir:

1.  Finance and Operations kiracısı için Azure Active Directory'de yeni bir kullanıcı hesabı oluşturun. Bu kullanıcı hesabının amacı, Finance and Operations sunucusunun açığa çıkarttığı ambarlama uygulamasının belirli özel hizmetlerine erişmektir. Bu adımı tamamladıktan sonra, bir WMDP e-posta adresi ve WMDP parolasından oluşan WMDP kullanıcı kimlik bilgilerine sahip olacaksınız. Azure AD ve Finance and Operations için kullanıcılar eklemek hakkında temel adımları öğrenmek için bu eğitime göz atın: [Bir Finance and Operations aboneliğine kaydolun](/dynamics365/unified-operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Ambarlama uygulaması kullanıcı kimlik bilgilerine karşılık gelen bir Finance and Operations kullanıcı oluşturun.
    1.  Finance and Operations içerisinde **Sistem Yönetimi** &gt; **Ortak** &gt; **Kullanıcılar** konumuna gidin.
    2.  Yeni bir kullanıcı oluşturun.
    3.  Ambarı, mobil cihaz kullanıcısına, aşağıdaki ekran görüntüsünde görüldüğü gibi atayın. [![wh-09-kullanıcı-güvenlik-rolü-ekle](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Azure Active Directory uygulamanızı, ambar uygulaması kullanıcısı ile ilişkilendirin.
    1.  Finance and Operations içerisinde **Sistem yönetimi** &gt; **Kurulum** &gt; **Azure Active Directory uygulamaları** konumuna gidin.
    2.  Yeni satır oluşturun.
    3.  **İstemci kimliği**'ni (son bölümde elde edilen) girin, bir ad verin ve önceki oluşturulan kullanıcıyı seçin. Tüm cihazlarınızı etiketlemenizi öneririz, böylece kayboldukları takdirde onların Finance and Operations erişimlerini bu sayfadan kolayca kaldırabilirsiniz. [![wh-10-ad-uygulamalar-formu](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Uygulamayı yapılandır
Azure AD uygulaması aracılığıyla Finance and Operations sunucusuna erişebilmek için cihaz üzerindeki uygulamayı yapılandırmanız gerekir. Bunu yapmak için aşağıdaki adımları tamamlayın.

1.  Uygulamanın içinde **Bağlantı ayarları**'na gidin.
2.  **Demo modu** alanını temizleyin. <br>[![wh-11-uygulama-bağlantı-ayarları-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Aşağıdaki bilgileri girin: 
    + **Azure Active directory istemci kodu** - İstemci kodu, "Active Directory'de bir web hizmeti uygulaması oluştur" içindeki 13. adımdan edinilir. 
    + **Azure Active directory istemci sırrı** - İstemci sırrı, "Active Directory'de bir web hizmeti uygulaması oluştur" içindeki 13. adımdan edinilir. 
    + **Azure Active directory kaynağı** -Azure AD dizini kaynağı, Finance and Operations kök URL'sini gösterir. **Not**: Bu alanı bir eğik çizgi (/) ile bitirmeyin. 
    + **Azure Active directory kiracısı** - Finance and Operations sunucusu ile kullanılan Azure AD dizini kiracısı: https://login.windows.net/sizin-AD-kiracı-kimliğiniz. Örneğin: https://login.windows.net/contosooperations.onmicrosoft.com. 
    <br>**Not**: Bu alanı bir eğik çizgi (/) ile bitirmeyin. 
    + **Şirket** - Uygulamanın bağlanmasını istediğiniz tüzel varlığı, Finance and Operations içerisinde girin. <br>[![wh-12-uygulama-bağlantı-ayarları](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Uygulamanın sol üst köşesindeki **Geri** düğmesini seçin. Uygulama şimdi, Finance and Operations sunucunuza bağlanır ve ambar çalışanı için oturum açma ekranı görüntülenir. <br>[![wh-13-oturum-açma-ekranı](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Cihazın erişimini kaldır
Kayıp veya güvenliği aşılmış bir cihaz durumunda, bu cihaz için Finance and Operations erişimini kaldırmanız gerekir. Aşağıdaki adımlar, erişimi kaldırmak için önerilen adımları açıklar.

1.  Finance and Operations içerisinde **Sistem yönetimi** &gt; **Kurulum** &gt; **Azure Active Directory uygulamaları** konumuna gidin.
2.  Erişimini kaldırmak istediğiniz cihaza karşılık gelen satırı silin. Kaldırılan cihaz için **İstemci Kimliğini** not alın.
3.  <https://manage.windowsazure.com> adresinden Azure klasik portala oturum açın.
4.  Sol menüdeki **Active Directory** menüsüne tıklayın ve daha sonra istediğiniz dizine tıklayın.
5.  Üst menüde, **Uygulamalar** üzerine tıklayın ve daha sonra yapılandırmak istediğiniz uygulamayı tıklatın. **Hızlı Başlat** sayfası, tek oturum açma ve diğer yapılandırma bilgilerine sahip bir sayfayla görüntülenir.
6.  **Yapılandır** sekmesini tıklatın, aşağı kaydırın ve uygulamanın **İstemci kimliği**'nin bu bölümün 2. adımındaki ile aynı olduğundan emin olun.
7.  Komut çubuğunda **Sil** düğmesini tıklatın.
8.  Onay iletisinde **Evet**'i tıklatın.






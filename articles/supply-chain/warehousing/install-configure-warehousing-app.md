---
title: Microsoft Dynamics 365 for Finance and Operations &#8211; Ambarlama yükleme ve yapılandırma
description: Bu konuda Microsoft Dynamics 365 for Finance and Operations - Ambarlama yükleme ve yapılandırmayı açıklar.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5e99351d79cb5898c6d5565d3d3197a8fe860df
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559198"
---
# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Finance and Operations &#8211; Ambarlama yükleme ve yapılandırma

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Bu konu bulut dağıtımları için ambarlamanın nasıl yapılandırılacağını açıklar. Ambarlamanın şirket içi dağıtımlar için nasıl yapılandırılacağını öğrenmek istiyorsanız bkz. [Şirket için dağıtımlar için ambarlama](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Bu konuda Microsoft Dynamics 365 for Finance and Operations - Ambarlama yükleme ve yapılandırmayı açıklar.

Finance and Operations - Ambarlama, Google Play Store ve Windows Mağazası'nda bulunan bir uygulamadır. Finance and Operations'un geçerli sürümü için bu uygulama, tek başına bir bileşen olarak sağlanır, bu da ambar görevleri için kullanılan cihazlarda kendinden dağıtım anlamına gelir. Uygulamayı Finance and Operations ortamınızda kullanmak için uygulamayı tüm cihazlarınıza indirmeli ve sizin Finance and Operations ortamınıza bağlanmak üzere yapılandırmalısınız. Bu konu, cihazlarınıza uygulamanın nasıl yükleneceğini açıklar. Ayrıca uygulamanın Finance and Operations ortamınıza nasıl bağlanacağını da açıklar.

## <a name="prerequisites"></a>Önkoşullar
Uygulama Android ve Windows işletim sistemlerinde kullanılabilir. Bu uygulamayı kullanmak için aşağıda belirtilen, desteklenen işletim sistemlerinin cihazlarınızda yüklü olması gerekir. Finance and Operations'un aşağıda belirtilen, desteklenen sürümlerinden birine de sahip olmalısınız. Aşağıdaki tabloda belirtilen verileri, donanım ve yazılım ortamınızın kurulumu desteklemeyi hazır olup olmadığını değerlendirmek için kullanın.

| Platform                    | Sürüm                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (tüm sürümler)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, sürüm 1611 <br>-veya- <br>Microsoft Dynamics AX sürüm 7.0/7.0.1 ve Microsoft Dynamics AX platform güncelleştirmesi 2, düzeltme KB 3210014 ile |

## <a name="get-the-app"></a>Uygulamayı edinin
-   Windows (UWP)
     - [Finance and Operations - Windows Mağazasında Ambarlama](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Ambarlama Google Play Mağazası'nda](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra Uygulama Galerisi kaldırıldı, bu da Finance and Operations - Ambarlama uygulamasının bu konumdan artık indirilemeyeceği anlamına geliyor.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Azure Active Directory içinde bir web hizmeti uygulaması oluşturun
Uygulamanın belirli bir Finance and Operations sunucusu ile etkileşime girmesini etkinleştirmek için önce bir web hizmet uygulamasını, Finance and Operations kiracısında bir Azure Active Directory içinde kaydetmelisiniz. Güvenlik nedeniyle, kullandığınız her cihaz için bir web hizmeti uygulaması oluşturmanızı öneririz. Azure Active Directory (Azure AD) içinde bir web hizmeti uygulaması oluşturmak için aşağıdaki adımları tamamlayın:

1.  Web tarayıcısında <https://portal.azure.com> adresine gidin.
2.  Azure aboneliğine erişimi olan kullanıcının adını ve parolasını girin.
3.  Azure Portalında, sol gezinme bölmesinde **Azure Active Directory** öğesine tıklayın.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Active Directory örneğinin Finance and Operations tarafından kullanılan örnek olduğundan emin olun.
5.  Listede **Uygulama kayıtları**'na tıklayın. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Üst bölmede **Yeni uygulama kaydı**'na tıklayın. **Uygulama eklemek** sihirbazı başlar.
7.  Uygulama için bir ad girin ve **Web application/web API** seçeneğini seçin. Web uygulamanızın URL'si olan oturum açma URL'sini girin. Bu URL, dağıtım URL'niz ile aynıdır, ancak sonuna oauth eklenir. **Oluştur**'a tıklayın. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Listeden yeni uygulamayı seçin. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Daha sonra ihtiyacınız olacağından **Uygulama Kodunu** unutmayın. **Uygulama Kodu** daha sonra **İstemci Kodu** olarak ifade edilecektir.
10. **Ayarlar bölmesi**'nde **Anahtarlar**'a tıklayın. **Parolalar** bölümüne bir anahtar açıklaması ve bir süre girerek bir anahtar oluşturun. 
11. **Kaydet**'i tıklayın ve anahtarı kopyalayın. Bu anahtar daha sonra **İstemci sırrı** olarak anılacaktır. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Finance and Operations içinde bir kullanıcı hesabı oluşturma ve yapılandırma
Finance and Operations'ın Azure AD uygulamanızı kullanmasını sağlamak için, aşağıdaki yapılandırma adımlarını tamamlamanız gerekir:

1.  Ambarlama uygulaması kullanıcı kimlik bilgilerine karşılık gelen bir Finance and Operations kullanıcı oluşturun.
    1.  Finance and Operations içerisinde **Sistem Yönetimi** &gt; **Ortak** &gt; **Kullanıcılar** konumuna gidin.
    2.  Yeni bir kullanıcı oluşturun.
    3.  Ambarı, mobil cihaz kullanıcısına, aşağıdaki ekran görüntüsünde görüldüğü gibi atayın. [![wh-09-kullanıcı-güvenlik-rolü-ekle](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Azure Active Directory uygulamanızı, ambar uygulaması kullanıcısı ile ilişkilendirin.
    1.  Finance and Operations içerisinde **Sistem Yönetimi** &gt; **Kurulum** &gt; **Azure Active Directory uygulamalarına** gidin.
    2.  Yeni satır oluşturun.
    3.  **İstemci kimliği**'ni (son bölümde elde edilen) girin, bir ad verin ve önceki oluşturulan kullanıcıyı seçin. Tüm cihazlarınızı etiketlemenizi öneririz, böylece kayboldukları takdirde onların Finance and Operations erişimlerini bu sayfadan kolayca kaldırabilirsiniz. [![wh-10-ad-uygulamalar-formu](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Uygulamayı yapılandır
Azure AD uygulaması aracılığıyla Finance and Operations sunucusuna erişebilmek için cihaz üzerindeki uygulamayı yapılandırmanız gerekir. Bunu yapmak için aşağıdaki adımları tamamlayın.

1.  Uygulamanın içinde **Bağlantı ayarları**'na gidin.
2.  **Demo modu** alanını temizleyin. <br>[![wh-11-uygulama-bağlantı-ayarları-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Aşağıdaki bilgileri girin: 
    + **Azure Active directory istemci kodu** - İstemci kodu, "Active Directory'de bir web hizmeti uygulaması oluştur" içindeki 9. adımdan edinilir. 
    + **Azure Active directory istemci sırrı** - İstemci sırrı, "Active Directory'de bir web hizmeti uygulaması oluştur" içindeki 11. adımdan edinilir. 
    + **Azure Active directory kaynağı** - Azure AD dizini kaynağı, Finance and Operations kök URL'sini gösterir. **Not**: Bu alanı bir eğik çizgi (/) ile bitirmeyin. 
    + **Azure Active directory kiracısı** - Finance and Operations sunucusu ile kullanılan Azure AD dizini kiracısı: `https://login.windows.net/your-AD-tenant-ID`. Örnek olarak: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Not**: Bu alanı bir eğik çizgi (/) ile bitirmeyin. 
    + **Şirket** - Uygulamanın bağlanmasını istediğiniz tüzel varlığı, Finance and Operations içerisinde girin. <br>[![wh-12-uygulama-bağlantı-ayarları](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Uygulamanın sol üst köşesindeki **Geri** düğmesini seçin. Uygulama şimdi, Finance and Operations sunucunuza bağlanır ve ambar çalışanı için oturum açma ekranı görüntülenir. <br>[![wh-13-oturum-açma-ekranı](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Bir mobil cihazdaki kamerayı barkod taramak için kullanmak üzere  Dynamics 365 for Finance and Operations - Ambarlama kurulumu hakkında daha fazla bilgi için bkz. [Dynamics 365 for Finance and Operations - Ambarlama içinde barkodları kamera kullanarak taratın](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Cihazın erişimini kaldır
Kayıp veya güvenliği aşılmış bir cihaz durumunda, bu cihaz için Finance and Operations erişimini kaldırmanız gerekir. Aşağıdaki adımlar, erişimi kaldırmak için önerilen adımları açıklar.

1.  Finance and Operations içerisinde **Sistem Yönetimi** &gt; **Kurulum** &gt; **Azure Active Directory uygulamalarına** gidin.
2.  Erişimini kaldırmak istediğiniz cihaza karşılık gelen satırı silin. Daha sonra ihtiyacınız olacağından kaldırılan cihaz için kullanılan **İstemci Kodu**'nu unutmayın.
3.  Azure portalında <https://portal.azure.com> adresinden oturum açın.
4.  Sol menüde **Active Directory** simgesine tıklayın ve doğru dizinde olduğunuzdan emin olun.
5.  Listede **Uygulama kayıtları**'na ve daha sonra yapılandırmak istediğiniz uygulamaya tıklayın. **Ayarlar** sayfası yapılandırma bilgileriyle birlikte görüntülenir.
6.  Uygulamanın **İstemci kodunun** bu bölümdeki adım 2'deki kodla aynı olduğundan emin olun.
7.  Üst bölmedeki **Sil** düğmesine tıklayın.
8.  Onay iletisinde **Evet**'i tıklatın.

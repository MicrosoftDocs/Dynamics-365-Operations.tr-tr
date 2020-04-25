---
title: Ambarlama uygulamasını yükleme ve yapılandırmaya genel bakış
description: Bu konu Dynamics 365 for Finance and Operations - Ambarlama uygulamasını yükleme ve yapılandırmayı açıklar.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52882ef7542bfedebdae4a08de8404cddd01ed55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205610"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Ambarlama uygulamasını yükleme ve yapılandırmaya genel bakış

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Bu konu bulut dağıtımları için ambarlamanın nasıl yapılandırılacağını açıklar. Ambarlamanın şirket içi dağıtımlar için nasıl yapılandırılacağını öğrenmek istiyorsanız bkz. [Şirket için dağıtımlar için ambarlama](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Bu konu Dynamics 365 for Finance and Operations - Ambarlama uygulamasını yükleme ve yapılandırmayı açıklar.

Ambarlama uygulaması Google Play Store ve Windows Mağazası'nda bulunur. Dynamics 365 Supply Chain Management'ın geçerli sürümü için bu uygulama, tek başına bir bileşen olarak sağlanır, bu da ambar görevleri için kullanılan cihazlarda kendinden dağıtım anlamına gelir. Uygulamayı Supply Chain Management ortamınızda kullanmak için uygulamayı tüm cihazlarınıza indirmeli ve ortamınıza bağlanmak üzere yapılandırmalısınız. Bu konu, cihazlarınıza uygulamanın nasıl yükleneceğini açıklar. Ayrıca uygulamanın Supply Chain Management ortamınıza nasıl bağlanacağını da açıklar.

## <a name="prerequisites"></a>Önkoşullar
Uygulama Android ve Windows işletim sistemlerinde kullanılabilir. Bu uygulamayı kullanmak için aşağıda belirtilen, desteklenen işletim sistemlerinin cihazlarınızda yüklü olması gerekir. Aşağıda belirtilen, desteklenen sürümlerden birine de sahip olmalısınız. Aşağıdaki tabloda belirtilen verileri, donanım ve yazılım ortamınızın kurulumu desteklemeyi hazır olup olmadığını değerlendirmek için kullanın.

| Platform                    | Sürüm                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (tüm sürümler)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, sürüm 1611 <br>-veya- <br>Microsoft Dynamics AX sürüm 7.0/7.0.1 ve Microsoft Dynamics AX platform güncelleştirmesi 2, düzeltme KB 3210014 ile |

## <a name="get-the-app"></a>Uygulamayı edinin
-   Windows (UWP)
     - [Finance and Operations - Windows Mağazası'nda Ambarlama](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations - Google Play Store'da Ambarlama](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra Uygulama Galerisi kaldırıldı, bu da Ambarlama uygulamasının bu konumdan artık indirilemeyeceği anlamına geliyor.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Azure Active Directory içinde bir web hizmeti uygulaması oluşturun
Uygulamanın belirli bir Supply Chain Management sunucusu ile etkileşime girmesini etkinleştirmek için önce bir web hizmet uygulamasını, Supply Chain Management kiracısında bir Azure Active Directory içinde kaydetmelisiniz. Güvenlik nedeniyle, kullandığınız her cihaz için bir web hizmeti uygulaması oluşturmanızı öneririz. Azure Active Directory (Azure AD) içinde bir web hizmeti uygulaması oluşturmak için aşağıdaki adımları tamamlayın:

1.  Web tarayıcısında <https://portal.azure.com> adresine gidin.
2.  Azure aboneliğine erişimi olan kullanıcının adını ve parolasını girin.
3.  Azure Portalında, sol gezinti bölmesinde, **Azure Active Directory**'e tıklayın.

    [![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)

4.  Active Directory örneğinin Supply Chain Management tarafından kullanılan örnek olduğundan emin olun.
5.  Listede **Uygulama kayıtları**'na tıklayın. 

    [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)

6.  Üst bölmede **Yeni kayıt**'a tıklayın. **Uygulama kaydetme sihirbazı** başlar.
7.  Uygulama için bir ad girin ve **Yalnızca bu kuruluş dizinindeki hesaplar**'ı seçin. **Kayıt**'a tıklayın.  

    [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)

8.  Yeni uygulama kaydınız açılır. 

    [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)

9.  Daha sonra ihtiyacınız olacağından **Uygulama Kodunu** unutmayın. **Uygulama Kodu** daha sonra **İstemci Kodu** olarak ifade edilecektir.
10. **Yönet** bölmesinde **Sertifika ve parolalar**'a tıklayın. **Yeni istemci parolası**'na tıklayın. 

    [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

11. **Parolalar** bölümüne bir anahtar açıklaması ve bir süre girerek bir anahtar oluşturun. **Ekle**'ye tıklayın ve anahtarı kopyalayın. Bu anahtar daha sonra **İstemci sırrı** olarak anılacaktır. 

    [![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Supply Chain Management içinde bir kullanıcı hesabı oluşturma ve yapılandırma
Supply Chain Management'ın Azure AD uygulamanızı kullanmasını sağlamak için, aşağıdaki yapılandırma adımlarını tamamlamanız gerekir:

1.  Ambarlama uygulaması kullanıcı kimlik bilgilerine karşılık gelen bir kullanıcı oluşturun.
    1.  **Sistem yönetimi** &gt; **Genel** &gt; **Kullanıcılar**'a gidin.
    2.  Yeni bir kullanıcı oluşturun.
    3.  Ambarı, mobil cihaz kullanıcısına, aşağıdaki ekran görüntüsünde görüldüğü gibi atayın. 
    
        [![wh-09-kullanıcı-güvenlik-rolü-ekle](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Azure Active Directory uygulamanızı, ambar uygulaması kullanıcısı ile ilişkilendirin.
    1.  Supply Chain Management içerisinde **Sistem Yönetimi** &gt; **Kurulum** &gt; **Azure Active Directory uygulamaları**'na gidin.
    2.  Yeni satır oluşturun.
    3.  **İstemci kimliği**'ni (son bölümde elde edilen) girin, bir ad verin ve önceki oluşturulan kullanıcıyı seçin. Tüm cihazlarınızı etiketlemenizi öneririz, böylece kayboldukları takdirde onların Supply Chain Management erişimlerini bu sayfadan kolayca kaldırabilirsiniz. 
    
        [![wh-10-ad-uygulamalar-formu](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Uygulamayı yapılandır
Azure AD uygulaması aracılığıyla Supply Chain Management sunucusuna erişebilmek için cihaz üzerindeki uygulamayı yapılandırmanız gerekir. Bunu yapmak için aşağıdaki adımları tamamlayın.

1.  Uygulamanın içinde **Bağlantı ayarları**'na gidin.
2.  **Demo modu** alanını temizleyin. <br>

    [![wh-11-uygulama-bağlantı-ayarları-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)

3.  Aşağıdaki bilgileri girin: 
    + **Azure Active directory istemci kodu** - İstemci kodu, "Active Directory'de bir web hizmeti uygulaması oluştur" içindeki 9. adımdan edinilir. 
    + **Azure Active directory istemci sırrı** - İstemci sırrı, "Active Directory'de bir web hizmeti uygulaması oluştur" içindeki 11. adımdan edinilir. 
    + **Azure Active directory kaynağı** - Azure AD dizini kaynağı, Supply Chain Management kök URL'sini gösterir. 
    
        > [!NOTE]
        > Bu alanı bir eğik çizgi (/) ile bitirmeyin. 

    + **Azure Active directory kiracısı** - Supply Chain Management sunucusu ile kullanılan Azure AD dizini kiracısı: `https://login.windows.net/your-AD-tenant-ID`. Örneğin: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    
        > [!NOTE]
        > Bu alanı bir eğik çizgi (/) ile bitirmeyin. 
    
    + **Şirket** - Uygulamanın bağlanmasını istediğiniz tüzel varlığı, Supply Chain Management'ta girin. <br>
    
    [![wh-12-uygulama-bağlantı-ayarları](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)

4.  Uygulamanın sol üst köşesindeki **Geri** düğmesini seçin. Uygulama şimdi, Supply Chain Management sunucunuza bağlanır ve ambar çalışanı için oturum açma ekranı görüntülenir.

    [![wh-13-oturum-açma-ekranı](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Bir mobil cihazda kamera kullanarak barkodları taramak için Ambarlama uygulamasını ayarlama hakkında bilgi için bkz. [Dynamics 365 for Finance and Operations - Ambarlama uygulamasında kamera kullanarak barkodları tarama](scan-bar-codes-using-a-camera.md).

## <a name="remove-access-for-a-device"></a>Cihazın erişimini kaldır
Kayıp veya güvenliği aşılmış bir cihaz durumunda, bu cihaz için Supply Chain Management erişimini kaldırmanız gerekir. Aşağıdaki adımlar, erişimi kaldırmak için önerilen adımları açıklar.

1.  **Sistem yönetimi** &gt; **Kurulum** &gt; **Azure Active Directory uygulamaları**'na gidin.
2.  Erişimini kaldırmak istediğiniz cihaza karşılık gelen satırı silin. Daha sonra ihtiyacınız olacağından kaldırılan cihaz için kullanılan **İstemci Kodu**'nu unutmayın.
3.  Azure portalında <https://portal.azure.com> adresinden oturum açın.
4.  Sol menüde **Active Directory** simgesine tıklayın ve doğru dizinde olduğunuzdan emin olun.
5.  Listede **Uygulama kayıtları**'na ve daha sonra yapılandırmak istediğiniz uygulamaya tıklayın. **Ayarlar** sayfası yapılandırma bilgileriyle birlikte görüntülenir.
6.  Uygulamanın **İstemci kodunun** bu bölümdeki adım 2'deki kodla aynı olduğundan emin olun.
7.  Üst bölmedeki **Sil** düğmesine tıklayın.
8.  Onay iletisinde **Evet**'i tıklatın.

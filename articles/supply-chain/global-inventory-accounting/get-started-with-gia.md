---
title: Global Stok Muhasebesi kullanmaya başlama
description: Bu konuda, Global Stok Muhasebesi kullanmaya nasıl başlayabileceğiniz açıklanmaktadır.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 90fcbdc5c9dd4301225952d885794bd4d03ef825fd5590896be13eacfad1f979
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773308"
---
# <a name="get-started-with-global-inventory-accounting"></a>Global Stok Muhasebesi kullanmaya başlama

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Global Stok Muhasebesi, ayarlamış olduğunuz Global Stok Muhasebesi defterlerinde çoklu stok muhasebesi yapmanıza olanak tanır. Her bir Global Stok Muhasebesi genel defterini bir *kural* ile ilişkilendirmeniz gerekir. Kural, aşağıdaki muhasebe ilkesi türlerinin bir koleksiyondur:

- Maliyet nesnesi
- Giriş ölçümü esası
- Maliyet akışı varsayımı
- Maliyet öğesi

> [!NOTE]
> Global Stok Muhasebesi'ni açıktan sonra da Microsoft Dynamics 365 Supply Chain Management'ta stok muhasebesini her zamanki gibi yapmaya devam edebilirsiniz.

Global Stok Muhasebesi bir eklentidir. Özelliklerini kullanılabilir hale getirmek için Microsoft Dynamics Lifecycle Services'tan (LCS) yüklemeniz gerekir. Üretim ortamları için etkinleştirmeden önce bir test ortamında değerlendirmeyi seçebilirsiniz.

Global Stok Muhasebesi, Supply Chain Management'ta yerleşik olan tüm maliyet yönetimi özelliklerini desteklememektedir. Bu nedenle, şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>Global Stok Muhasebesi genel önizlemesi nasıl alınır

> [!IMPORTANT]
> Global Stok Muhasebesi kullanmak için, LCS etkin bir yüksek kullanılabilirlik ortamına sahip olmanız (OneBox ortamı değil) gerekir. Ek olarak, Supply Chain Management sürüm 10.0.19 veya üstünü çalıştırıyor olmalısınız.

Global Stok Muhasebesi genel önizlemesine kaydolmak için, LCS ortam kimliğinizi e-posta ile [Global Stok Muhasebesi ekibine gönderin](mailto:GlobalInvAccount@microsoft.com). Program için onaylandıktan sonra, takım Global Stok Muhasebesi Beta anahtarı ve servis uç noktalarınızı içeren bir takip e-postası gönderir. Beta anahtarını aldıktan sonra [eklentiyi yükleyebilirsiniz](#install).

## <a name="licensing"></a>Lisans

Global Stok Muhasebesi, Supply Chain Management için kullanılabilir olan stok muhasebesi standart özellikleri ile birlikte lisanslanır. Global Stok Muhasebesini kullanmak için ek lisans satın almanız gerekmez.

## <a name="prerequisites"></a>Önkoşullar

### <a name="set-up-microsoft-power-platform-integration"></a>Microsoft Power Platform entegrasyonunu ayarla

Eklenti işlevselliğini etkinleştirebilmek için, aşağıdaki adımları izleyerek Microsoft Power Platform ile tümleştirmeniz gerekir.

1. Hizmeti eklemek istediğiniz LCS ortamını açın.
1. **Tüm ayrıntılar**'a gidin.
1. **Power Platform Tümleştirme** bölümünde **Kurulum** öğesini seçin.
1. **Power Platform ortam kurulumu** iletişim kutusunda, onay kutusunu seçin ve sonra **Kurulum**'u seçin. Kurulum genellikle 60 ila 90 dakika arasında sürer.
1. Microsoft Power Platform ortam kurulumu tamamlandıktan sonra, sayfa ortamınızın adını gösterir. Ayrıca, **Power Platform Tümleştirmesi** vbölümünde "Power Platform ortam kurulumu tamamlandı" ifadesi gösterilir. Global Stok Muhasebesi, çift yazma uygulaması gerektirmez.

Daha fazla bilgi için bkz. [Ortam dağıtımından sonra ayarlama](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).

### <a name="set-up-dataverse"></a>Dataverse Kurma

Dataverse kurulumundan önce, aşağıdaki adımları izleyerek Global Stok Muhasebesi ilkelerini kiracınıza ekleyin.

1. Wşndowa PowerShell v2 için Azure AD Modülünü [Graph için Azure Active Directory PowerShell'i Yükleme](/powershell/azure/active-directory/install-adv2) bölümünde açıklandığı gibi yükleyin.
1. Aşağıdaki PowerShell komutunu çalıştırın.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Sonra, aşağıdaki adımları izleyerek, Dataverse'de Global Stok Muhasebesi için uygulama kullanıcıları oluşturun.

1. Dataverse ortamınızın URL'sini açın.
1. **Gelişmiş Ayar \> Sistem \> Güvenlik \> Kullanıcılar**'a gidin ve bir uygulama kullanıcısı oluşturun. Sayfa görünümünü **Uygulama Kullanıcıları** olarak değiştirmek için *Görünüm* alanını kullanın.
1. **Yeni**'yi seçin.
1. **Uygulama Kimliği** alanını *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9* olarak ayarlayın.
1. **Rol Ata**'yı ve sonra *Sistem Yöneticisi*'ni seçin. *Common Data Service Kullanıcısı* adlı bir rol varsa onu da seçin.
1. Önceki adımları yineleyin, ancak **Uygulama kodu** alanını *5f58fc56-0202-49a8-ac9e-0946b049718b* olarak ayarlayın.

Daha fazla bilgi için bkz. [Uygulama kullanıcısı oluşturma](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Dataverse yüklemenizin varsayılan dili İngilizcedeğilse, aşağıdaki adımları izleyin.

1. **Gelişmiş Ayar \> Yönetim \>Diller**'e gidin.
1. *İngilizce* (*LanguageCode=1033*) dilini ve **Uygula**'yı seçin.

## <a name="install-the-add-in"></a><a name="install"></a>Eklentiyi yükleme

Global Stok Muhasebesi kullanabilmeniz için eklentiyi yüklemek üzere bu adımları izleyin.

1. Global Stok Muhasebesi genel önizlemesi için [kaydolma](#sign-up).
1. [LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın
1. **Özellik yönetimi önizlemesi**'ne gidin.
1. Artı işaretini (**+**) seçin.
1. **Kod** alanına Global Stok Muhasebesi için eklenti beta anahtarınızı girin. (Kaydolduğunuzda Beta anahtarınızı e-posta ile almış olmanız gerekir.)
1. **Engellemeyi Kaldır**'ı seçin.
1. Hizmeti eklemek istediğiniz LCS ortamını açın.
1. **Tüm ayrıntılar**'a gidin.
1. **Power Platform Tümleştirmesi**'ne gidin **Kurulum**'u seçin.
1. **Power Platform ortam kurulumu** iletişim kutusunda, onay kutusunu seçin ve sonra **Kurulum**'u seçin. Kurulum genellikle 60 ila 90 dakika arasında sürer.
1. Microsoft Power Platform ortamı kurulumu tamamlandıktan sonra, **Ortam eklentileri** hızlı sekmesinde, **Yeni eklenti yükle**'yi seçin.
1. **Global stok muhasebesi**'ni seçin.
1. Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.
1. **Yükle**'yi seçin.
1. **Ortam eklentileri** hızlı sekmesinde, Global Stok Muhasebesi'nin yüklenmekte olduğunu görmelisiniz. Birkaç dakika sonra, durum *Yükleniyor* yerine *Yüklü* olarak değişmelidir. (Bu değişikliği görmek için sayfayı yenilemeniz gerekebilir.) Bu noktada, Global Stok Muhasebesi kullanıma hazırdır.

## <a name="set-up-the-integration"></a>Tümleştirmeyi ayarlama

Global Stok Muhasebesi ile Supply Chain Management arasındaki tümleştirmeyi ayarlamak için bu adımları izleyin.

1. Supply Chain Management'ta oturun açın.
1. **Sistem yönetimi \> Özellik Yönetimi** bölümüne gidin.
1. **Güncelleştirmeleri denetle**'yi seçin.
1. **Tümü** sekmesinde, *Global stok muhasebesi* olarak adlandırılan özelliği arayın.
1. **Şimdi etkinleştir**'i seçin.
1. **Global stok muhasebesi \> Kurulum \> Global stok muhasebesi parametreleri \> Tümleştirme parametreleri**'ne gidin.
1. **Veri hizmeti uç noktası** ve **Global stok muhasebesi uç noktası** alanlarında, önizleme Için kayıt olduğunuzda Global Stok Muhasebesi takımının gönderdiği e-postadaki URL'leri girin.

Global Stok Muhasebesi artık kullanıma hazır.

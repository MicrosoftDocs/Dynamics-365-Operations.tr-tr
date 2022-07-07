---
title: Global Stok Muhasebesi kullanmaya başlama
description: Bu makalede, Global Stok Muhasebesi kullanmaya nasıl başlayabileceğiniz açıklanmaktadır.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cbe6bff6fab96900b8bd4e112a8858363fff86d1
ms.sourcegitcommit: 9870b773a2ea8f5675651199fdbc63ca7a1b4453
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013569"
---
# <a name="get-started-with-global-inventory-accounting"></a>Global Stok Muhasebesi kullanmaya başlama

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Global Stok Muhasebesi, ayarlamış olduğunuz Global Stok Muhasebesi defterlerinde çoklu stok muhasebesi yapmanıza olanak tanır. Her bir Global Stok Muhasebesi genel defterini bir *kural* ile ilişkilendirmeniz gerekir. Kural, aşağıdaki muhasebe ilkesi türlerinin bir koleksiyondur:

- Maliyet nesnesi
- Giriş ölçümü esası
- Maliyet akışı varsayımı
- Maliyet öğesi

> [!NOTE]
> Global Stok Muhasebesi'ni açıktan sonra da Microsoft Dynamics 365 Supply Chain Management'ta stok muhasebesini her zamanki gibi yapmaya devam edebilirsiniz.

Global Stok Muhasebesi bir eklentidir. Özelliklerini kullanılabilir hale getirmek için Microsoft Dynamics Lifecycle Services'tan (LCS) yüklemeniz gerekir. Üretim ortamları için etkinleştirmeden önce bir test ortamında değerlendirmeyi seçebilirsiniz.

Global Stok Muhasebesi, Supply Chain Management'ta yerleşik olan tüm maliyet yönetimi özelliklerini desteklememektedir. Bu nedenle, şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>Global Stok Muhasebesi eklentisi nasıl alınır?

> [!IMPORTANT]
> Global Stok Muhasebesi kullanmak için, LCS etkin bir yüksek kullanılabilirlik ortamına sahip olmanız (OneBox ortamı değil) gerekir. Ek olarak, Supply Chain Management sürüm 10.0.19 veya üstünü çalıştırıyor olmalısınız.

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management sürüm 10.0.19 ila 10.0.26

Supply Chain Management sürüm 10.0.19 ila 10.0.26 için Genel Stok Muhasebesi'ni yüklemek üzere, [eklentiyi yükleyerek başlayın](#install). Daha sonra, LCS ortam kimliğinizi ve şirket adınızı e-posta ile [Genel Stok Muhasebesi ekibine](mailto:GlobalInvAccount@microsoft.com) gönderin. Ekip Global Stok Muhasebesi ve servis uç noktalarınızı içeren bir takip e-postası gönderir.

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Management 10.0.27 sürümü ve sonraki sürümler

Supply Chain Management sürüm 10.0.27 ve sonrası için Genel Stok Muhasebesi'ni yüklemek üzere, [eklentiyi yükleyin](#install). Bu Supply Chain Management sürümleri için Global Stok Muhasebesi servis uç noktaları otomatik olarak ayarlanır, böylece bunları el ile bulmanız gerekmez. Eklentiyi yüklerken herhangi bir sorunla karşılaşırsanız lütfen [Global Stok Muhasebesi ekibine](mailto:GlobalInvAccount@microsoft.com) başvurun.

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

Daha fazla bilgi için bkz. [Ortam dağıtımından sonra etkinleştirme](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="install-the-add-in"></a><a name="install"></a>Eklentiyi yükleme

Global Stok Muhasebesi kullanabilmeniz için eklentiyi yüklemek üzere bu adımları izleyin.

1. [LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın
1. Hizmeti eklemek istediğiniz LCS ortamını açın.
1. **Tüm ayrıntılar**'a gidin.
1. **Power Platform Tümleştirmesi**'ne gidin **Kurulum**'u seçin.
1. **Power Platform ortam kurulumu** iletişim kutusunda, onay kutusunu seçin ve sonra **Kurulum**'u seçin. Kurulum genellikle 60 ila 90 dakika arasında sürer.
1. Microsoft Power Platform ortam kurulumu tamamlandıktan sonra, [Power Platform yönetim merkezinde](https://admin.powerplatform.microsoft.com) oturum açın ve aşağıdaki adımları gerçekleştirerek Genel Stok Muhasebesi eklentisini yükleyin:
   1. Eklentiyi yüklemek istediğiniz ortamı seçin.
   1. **Dynamics 365 uygulamaları**'nı seçin.
   1. **Uygulamayı Yükle**'yi seçin.
   1. **Dynamics 365 Genel Stok Muhasebesi**'ni seçin.
   1. Yüklemek için **İleri**'yi seçin.
1. LCS ortamına geri dönün. **Ortam eklentileri** hızlı sekmesinde, **Yeni eklenti yükle**'yi seçin.
1. **Global stok muhasebesi**'ni seçin.
1. Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.
1. **Yükle**'yi seçin.
1. **Ortam eklentileri** hızlı sekmesinde, Global Stok Muhasebesi'nin yüklenmekte olduğunu görmelisiniz. Birkaç dakika sonra, durum *Yükleniyor* yerine *Yüklü* olarak değişmelidir. (Bu değişikliği görmek için sayfayı yenilemeniz gerekebilir.) Bu noktada, Global Stok Muhasebesi kullanıma hazırdır.

Dataverse yüklemenizin varsayılan dili İngilizce değilse, aşağıdaki adımları izleyin:
1. **Gelişmiş Ayar \> Yönetim \>Diller**'e gidin.
1. *İngilizce* (*LanguageCode=1033*) dilini ve **Uygula**'yı seçin.

## <a name="set-up-the-integration"></a>Tümleştirmeyi ayarlama

Global Stok Muhasebesi ile Supply Chain Management arasındaki tümleştirmeyi ayarlamak için bu adımları izleyin.

1. Supply Chain Management'ta oturun açın.
1. **Sistem yönetimi \> Özellik Yönetimi** bölümüne gidin.
1. **Güncelleştirmeleri denetle**'yi seçin.
1. **Tümü** sekmesinde, *(Önizleme) Global stok muhasebesi* olarak adlandırılan özelliği arayın.
1. **Şimdi etkinleştir**'i seçin.
1. **Global stok muhasebesi \> Kurulum \> Global stok muhasebesi parametreleri \> Tümleştirme parametreleri**'ne gidin.
1. Çalıştırdığınız Supply Chain Management sürümüne bağlı olarak aşağıdaki adımlardan birini uygulayın:
    - **Supply Chain Management sürüm 10.0.19 ila 10.0.26**: **Veri servisi uç noktası** ve **Genel stok muhasebesi uç noktası** alanlarına, Genel Stok Muhasebesi ekibinin e-postayla gönderdiği URL'leri girin (ayrıca bkz. [Genel Stok Muhasebesi eklentisini edinme](#sign-up)).
    - **Supply Chain Management sürüm 10.0.27 ve daha yeni sürümler**: Uç noktaları girmeniz gerekmediği için bu adımı atlayabilirsiniz.

Global Stok Muhasebesi artık kullanıma hazır.

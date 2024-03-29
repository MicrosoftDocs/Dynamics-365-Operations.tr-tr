---
title: Regulatory Configuration Service
description: Bu makalede, Regulatory Configuration Service (RCS) özelliklerine genel bir bakış sağlanmakta ve hizmete nasıl erişebileceğiniz açıklanmaktadır.
author: kfend
ms.date: 06/04/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
ms.openlocfilehash: c04b13ef05424b27b5abcc2ac7490a7b75797bf5
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713935"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS), kodsuz/az kodlu genelleştirme işlevi için bağımsız bir tasarımcı ve yaşam döngüsü yönetim hizmetidir. RCS, genelleştirme paydaşlarının geliştiricilere gereksinim duymadan vergi, e-faturalama, yasal raporlama, banka ve iş belgelerine ilişkin temel genelleştirme alanlarını genişletmesine ve özelleştirmesine olanak tanır. Bu kodsuz/az kodlu genelleştirme yaklaşımı genelleştirmenin daha kolay, hızlı ve daha düşük maliyetli şekilde oluşturulmasını veya genişletilmesini sağlar.

RCS aşağıdaki özellikleri sunar:

- Elektronik raporlama (ER) tarafından sağlanan tüm işlevler için destek.
- Yeni genelleştirme mikro hizmetlerini yapılandırmaya yönelik bir önkoşul.
- Elektronik Faturalama desteği. Daha fazla bilgi için bkz. [Elektronik Faturalama](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Vergi Hesaplama destekleri. Daha fazla bilgi için bkz. [Vergi hizmeti](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Çok bileşenli özelliklerinin yaşam döngüsü yönetimini basitleştiren ve eylemleri yapılandırmak ve özellik parametrelerini ayarlamak için ek yetenek sağlayan yeni genelleştirme özelliği işlevselliği için destek. Daha fazla bilgi için bkz. [Regulatory Configuration Service – genelleştirme hizmetleri için basitleştirilmiş genelleştirme özelliği yönetimi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Microsoft Dynamics Lifecycle Services (LCS) kullanılmasına gerek kalmadan, yapılandırma yönetimini basitleştirmek için Genel depodaki özel yapılandırmaları merkezi olarak yayımlama, depolama ve paylaşma desteği.

## <a name="access-rcs"></a>RCS'ye erişim

RCS'ye [Regulatory Configuration Service sayfasından](https://marketing.configure.global.dynamics.com/) kaydolabilir veya oturum açabilirsiniz.

![RCS kaydolma/oturum açma.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

**Regulatory Configuration Service** sayfasında, hizmetin ek kullanım hüküm ve koşullarını inceleyin ve kabul edin ve ardından aşağıdaki düğmelerden birini seçin:

- **Kaydol**: Hizmeti ilk kez kullanacaksanız ve kuruluşunuza servis ortamı sağlamak için iş e-posta adresi kullanıyorsanız
- **Oturum aç**: Hizmete daha önce kaydolduysanız ve kuruluşunuzun ortamına erişmek istiyorsanız

> [!NOTE] 
> Kaydolduktan sonra RCS ortamına ek bir SysAdmin kullanıcısı eklemenizi öneririz. Bu kullanıcı, ortam için ortak yönetici olarak sağlanır. Bu, SysAdmin rolü bu ortamın kullanıcılarını yöneteceğinden RCS ortamına erişim için kararlılık sağlamaya yardımcı olur. **RCS çalışma alanı > Sistem Yönetimi**'ni kullanarak kullanıcı ekleyebilirsiniz.

## <a name="regional-availability"></a>Bölgesel kullanılabilirlik

RCS, aşağıdaki bölgelerde genel kullanıma sunulmuştur:

- Amerika Birleşik Devletleri
- Hindistan
- Fransa
- Avrupa

Bölgelerin tam listesi için bkz. [Dynamics 365 ve Power Platform: Kullanılabilirlik, veri konumu, dil ve yerelleştirme](https://aka.ms/dynamics_365_international_availability_deck).

> [!NOTE] 
> Şu anda Government Community Cloud (GCC) için RCS kullanıma sunulmamaktadır.

## <a name="rcs-default-company"></a>RCS varsayılan şirket

RCS'de kullanılan tasarım zamanı işlevi tüm şirketler arasında paylaşılır. Şirkete özgü işlevler yoktur. Bu nedenle, RCS ortamınızla bir şirket, **DAT**, kullanmanızı öneririz.

Ancak bazı senaryolarda, ER biçimlerinin belirli bir tüzel kişilikle ilişkili parametreleri kullanmasını isteyebilirsiniz. Yalnızca bu senaryolarda, varsayılan şirket değiştiricisini kullanmalısınız. Örneğin, bkz. [ER biçimini her tüzel kişilik için belirtilen parametreleri kullanmak üzere yapılandırma](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md)

## <a name="related-rcs-documentation"></a>İlgili RCS belgeleri

İlgili bileşenler hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- **RCS:**

    - [RCS'de ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme](rcs-global-repo-upload.md)

- **Genel depo:**

    - [ER yapılandırması oluşturma ve Genel depoya yükleme](rcs-global-repo-upload.md)
    - [Genel depoda yapılandırma paylaşma](rcs-global-repo-share-configuration.md)
    - [Genel depoda gelişmiş filtre uygulama](enhanced-filtering-global-repo.md)
    - [Genel depodan ER yapılandırmalarını indirme](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Genel depodaki yapılandırmaları durdurma](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) depolama kullanımdan kalkma](rcs-lcs-repo-dep-faq.md)

- **Genelleştirme özelliği:**

    - [Regulatory Configuration Service (RCS) - Genelleştirme özelliği](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>RCS'ye kaydolmayla ilgili sorunları giderme

Hizmet sayfasından RCS'ye kayolduğunuzda Azure Active Directory (Azure AD) ile ilgili bir sorunla karşılaşabilirsiniz. Aldığınız hata iletisi, RCS kaydolma işleminin şu an kapalı olduğunu ve kaydolma işlemini tamamlayabilmeniz için etkinleştirilmesi gerektiğini gösterir.

![RCS kaydolma hata iletisi.](media/01_RCSSignUpError.jpg)

Sorun, dinamik aboneliklere kaydolma izniniz olmadığını ve `AllowAdHocSubscriptions` özelliğinin kiracınızda etkin olması gerektiğini gösterir. 

- BT departmanınız, kuruluşunuzun Azure kiracılarını yönetiyorsa sorunu bildirmek için BT departmana başvurun.
- Azure kiralamalarınızı yönetmekten siz sorumluysanız, [Azure Active Directory için self servis kaydolma nedir](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings) bölümündeki adımları izleyerek bu sorunları çözebilirsiniz.

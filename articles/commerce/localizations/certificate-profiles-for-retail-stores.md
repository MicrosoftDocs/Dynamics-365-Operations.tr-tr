---
title: Perakende mağazaları için kullanıcı tarafından tanımlanmış sertifika profilleri
description: Bu makale, Microsoft Dynamics 365 Commerce içinde kullanılabilen sertifika profillerine genel bakış sağlar.
author: josaw1
ms.date: 09/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: v-chgriffin
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.search.industry: Retail
ms.search.form: RetailFormLayout, RetailParameters
ms.openlocfilehash: 5baf043a43210d819b605546089e981c86922ca9
ms.sourcegitcommit: 4f28f262cfb8f047cb5c0070261aa0748835e74b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/21/2022
ms.locfileid: "9558450"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Perakende mağazaları için kullanıcı tarafından tanımlanmış sertifika profilleri

[!include [banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce içinde kullanılabilen sertifika profillerine genel bakış sağlar. Bu işlevsellik, yerel Sertifikalar için destek ekleyerek, [Perakende kanalları için gizli anahtarları yönetme](../dev-itpro/manage-secrets.md) özelliğini genişletir.

Satış noktası (POS) çevrimdışı modda çalışırken, Microsoft Azure Key Vault'ta depolanan sertifikalara erişemez. Bunun yerine yerel sertifika kullanılmalıdır. Aşağıdaki özellikler desteklenir:

- Key Vault temel senaryolarında yerel sertifikaları kullanma
- Yerel sertifikaları Key Vault olmadan kullanma (örneğin, şirket içi kurulumda)
- Sertifikaların aşamalı güncelleştirmesi: bazı mağaza ve terminaller sertifikanın yeni bir sürümünü kullanır, ancak diğer mağazalar ve terminaller önceki sürümü kullanmaya devam eder

Sertifika profilleri işlevi, varsayılan bir sertifika belirtmenize ve aynı sertifika profilindeki sertifikaların aranacağı sırayı ayarlamanıza olanak tanır. Bu işlev ayrıca yerel sertifikalara ve Key Vault sertifikalarına benzer bir kurulum yaklaşımı sağlar. Sertifikalar için şirkete özgü ayarlar ekleyebilirsiniz ancak her bir sertifika için benzersiz şirketler arası tanımlayıcı Commerce kanallarında kullanılabilir.

### <a name="scenarios"></a>Senaryolar

Sertifika profilleri işlevi, Commerce kanallarında aşağıdaki senaryoları destekler:

- Key Vault temel senaryolarında yerel bir sertifika kullanın. Aşağıda bazı temel senaryo örnekleri verilmiştir:

    - Anahtar kasası depolama alanına erişilemiyor.
    - Anahtar kasası depolama alanında bir sertifika bulunamadı.
    - POS, çevrimdışı modda çalışıyor.

- Yerel sertifikalar kullanın ancak bunları Key Vault'a kaydetmeyin (örneğin, şirket içi kurulumda).
- Sertifikanın yeni bir sürümünün yalnızca mağazalarda veya yeni sürümün zaten kullanılabilir olduğu terminallerde kullanıldığı aşamalı sertifika güncelleştirmesi yapın.
- Aynı sertifikayı birkaç şirkette kullanın.

## <a name="set-up-certificate-profiles"></a>Sertifika profilleri ayarlama

Aşağıdaki yordamda sertifika profillerinin nasıl ayarlanacağı açıklanmaktadır.

### <a name="set-up-key-vault"></a>Key Vault ayarlama

Key Vault depolama alanında depolanan bir dijital sertifikayı kullanabilmeniz için aşağıdaki adımları tamamlamalısınız.

1. Key Vault depolama hesabı oluşturun. Depolama hesabını Commerce Scale Unit ile aynı coğrafi bölgede dağıtmanız önerilir.
1. Dijital sertifikayı, Key Vault depolama hesabına yükleyin.
1. Uygulama Nesne Sunucusu (AOS) uygulamasına, Key Vault depolama hesabındaki gizli dizileri okuma yetkisi verin.

Key Vault ile nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Azure Key Vault'u kullanmaya başlama](/azure/key-vault/key-vault-get-started).

### <a name="set-up-system-parameters"></a>Sistem parametrelerini ayarla

Commerce kanallarda sertifika profillerini konfigüre etmeden önce, Commerce'in her iki sertifikayı da Key Vault ve sertifika profillerinde kullanmaları için etkinleştirmelisiniz.

Commerce headquarters'ta sistem parametreleri ayarlamak için bu adımları izleyin.

1. **Sistem parametreleri** sayfasında **Gelişmiş Sertifika deposunu kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özellik Yönetimi** çalışma alanında, **Perakende mağazaları için kullanıcı tanımlı sertifika profilleri** özelliğini açın.

### <a name="set-up-key-vault-parameters"></a>Key Vault parametreleri ayarlama

**Key Vault parametreleri** sayfasında, Key Vault depolama alanına erişmeye yönelik aşağıdaki parametreleri belirtmeniz gerekir:

- **Ad** ve **Açıklama** – Key Vault depolama hesabının adı ve açıklaması.
- **Key Vault URL'si** – Key Vault depolama hesabının URL'si.
- **Key Vault istemcisi** – Kimlik doğrulaması amaçlarıyla, Key Vault depolama hesabıyla ilişkili Azure Active Directory (Azure AD) uygulamasının etkileşimli istemci kimliği. Bu istemcinin, depolama hesabındaki gizli dizileri okuma erişimine sahip olması gerekir.
- **Key Vault gizli anahtarı** – Key Vault depolama hesabında kimlik doğrulaması için kullanılan Azure AD uygulamasıyla ilişkili gizli anahtar.
- **Ad**, **Açıklama** ve **Gizli dizi başvurusu** – Sertifikanın adı, açıklaması ve gizli dizi başvurusu.

Daha fazla bilgi için bkz. [Azure Key Vault istemcisini ayarlama](../../finance/localizations/setting-up-azure-key-vault-client.md).

### <a name="configure-a-certificate-profile"></a>Sertifika profili konfigüre etme

Commerce Headquarters'da sertifika profilini yapılandırmak için şu adımları izleyin.

1. **Sistem yönetimi \> Kurulum \> Sertifika profilleri** seçeneğine gidin.
1. Eylem bölmesinde **Yeni**'yi seçerek kayıt oluşturun.
1. **Sertifika profili**, **Ad** ve **Açıklama** alanlarına değer girin.

    > [!NOTE]
    > Sertifika profili, tüm şirketler ve Commerce bileşenleri arasındaki sertifikanın benzersiz tanımlayıcısıdır.

1. **Tüzel kişilikler** hızlı sekmesinde satır eklemek için **Ekle**'yi seçin.
1. **Tüzel kişilikler** altında geçerli sertifika profilinin kullanılması gereken tüzel kişiliği (şirket) seçin.

    Sertifika profili birden çok tüzel kişilik için kullanılacaksa, her ek tüzel kişilik için bir satır eklemek üzere 4 ve 5. adımı tekrarlayın.

1. Sertifika profili için şirkete özgü ayarları girebileceğiniz **Sertifika profili ayarları** sayfasını açmak için **Ayarlar**'ı seçin. Geçerli sertifika profili Commerce kanallarında çağrıldığında hangi sertifikaların kullanılabileceğini belirtin. Gereksinim duyduğunuz kadar çok sertifika ekleyin ve bunlarla ilgili öncelikleri ayarlayın. Önceliği yüksek olan bir sertifika yoksa, öncelik temelinde bir sonraki sertifika kullanılır. Daha fazla bilgi için bkz: [İş akışı: Commerce Runtime'da sertifika arama](#workflow-searching-certificates-in-the-commerce-runtime) bölümü.

    > [!NOTE]
    > **Öncelik** alanı otomatik olarak ayarlanır. **1** değeri en yüksek önceliği temsil eder. **Sertifika profili ayarları** sayfasında yeni bir satır eklendiğinde, önceliği önceki satırın önceliğinden bir fazla olan bir sayıya ayarlanır. Belirli bir satırın önceliğini değiştirmek için satırı seçin ve önceliği artırmak için **Yukarı taşı** veya önceliği azaltmak için **Aşağı taşı**'yı seçin.

1. **Sertifika profili ayarları** sayfasında yeni bir satır eklediğinizde , aşağıdaki alanları ayarlayın:

    - **Konum türü** – Sertifikanın saklandığı konumu seçin. Bu alan iki olası değere sahiptir: **Yerel sertifika** ve **Key Vault**.
    - **Key Vault sertifikası** – Bu alan, **Konum türü** alanını **Key Vault** olarak ayarlarsanız gereklidir. Key Vault sertifikası gizli anahtarı belirtmek için bunu kullanın.
    - **Mağaza adı** – Bu alan isteğe bağlıdır ve yalnızca **Konum türü** alanını **Yerel sertifika** olarak ayarladığınızda kullanılabilir. Yerel sertifikaları aramak için kullanılacak varsayılan bir mağaza adı belirtmek için bunu kullanın.
    - **Mağaza konumu** – Bu alan isteğe bağlıdır ve yalnızca **Konum türü** alanını **Yerel sertifika** olarak ayarladığınızda kullanılabilir. Yerel sertifikaları aramak için kullanılacak varsayılan bir mağaza konumu belirtmek için bunu kullanın.

        > [!NOTE]
        > Varsayılan mağaza adı ve mağaza konumu, Commerce runtime içindeki yerel sertifikaları arama işlemini kolaylaştırmak için eklenir. X509StoreProvider, sertifikaların depolandığı klasörlerin listesine sahiptir. Varsayılan mağaza adı ve varsayılan mağaza konumu belirtilmezse, X509StoreProvider kendi listesindeki diğer klasörlerde bir sertifika bulmaya çalışır. Mağaza adı ve depolama konumu için kullanılabilir değerler hakkında daha fazla bilgi için, bkz: [StoreName Enum](/dotnet/api/system.security.cryptography.x509certificates.storename) ve [StoreLocation Enum](//dotnet/api/system.security.cryptography.x509certificates.storelocation).

    - **Parmak izi** – Bu alan gereklidir ve yalnızca **Konum türü** alanını **Yerel sertifika** olarak ayarladığınızda kullanılabilir. Sertifika parmak izini belirtmek için bunu kullanın.

        > [!IMPORTANT]
        > Yerel sertifikayı (örneğin, çevrimdışı moddaki Modern POS) kullanması gereken uygulamayı çalıştıran kullanıcının sertifikanın özel anahtarına en azından salt okunur erişimi olduğundan emin olmalısınız.

    - **Açıklamalar** – Bu alan isteğe bağlıdır ve kullanıcıların not girmesine izin verir.

## <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>İş akışı: Commerce runtime'da sertifikaları arama

Burada, Commerce runtime içinde bir sertifika profili çağrıldığında bir sertifikayı aramak için kullanılan temel iş akışı verilmektedir.

1. Sistem, sertifika profilinin geçerli tüzel kişilik için şirkete özel ayarlar içerip içermediğini tanımlar.
1. Sistem, **Öncelik** alanının **1** olarak ayarlandığı satır için **Sertifika profili ayarları** sayfasındaki değerleri kullanarak sertifikayı bulmaya çalışır.

    - **Konum türü** alanı **Key Vault** olarak ayarlanmışsa, **Anahtar kasası parametreleri** sayfasında sertifikayı aramak için **Key Vault sertifikası gizli anahtarı** alanının değeri kullanılır. Daha sonra sertifika, anahtar kasası depolama alanında aranır.
    - **Konum türü** alanı **Yerel sertifika** olarak ayarlanırsa X509StoreProvider, bu parametreler belirtilmişse, önce varsayılan mağaza adını ve mağaza konumunu kullanarak sertifikayı arar. Daha sonra kendi klasör listesindeki tüm klasörlerde arama yapar.

1. Sertifika bulunamazsa, **Öncelik** alanının **2** olarak ayarlandığı satır için bu işlem yinelenir ve bu şekilde devam eder.

> [!NOTE]
> Sertifika profilinin geçerli tüzel kişilik için ayarı yoksa veya sertifika araması **Sertifika profil ayarları** sayfasındaki tüm satırlar için başarısız olursa, sertifika bulunamaz.

### <a name="caching-the-results-of-certificate-searches"></a>Sertifika aramalarının sonuçlarını önbelleğe alma

Sertifika aramalarının sonuçları önbelleğe alınır. Önbelleğin varsayılan son kullanma tarihi bir saattir. Ancak, bu süre özelleştirilebilir ve maksimum değer olan 24 saate ayarlanabilir.

## <a name="gradual-update"></a>Aşamalı güncelleştirme

Sertifikanın yeni bir sürümü tanıtılırsa ancak aynı anda tüm mağazalarda güncelleştirilemezse, sertifika profilleri işlevi sertifikanın aşamalı olarak güncelleştirilmesini sağlar.

1. Bir sertifika profili ve güncelleştirilmesi gereken satırı bulun ve **Ayarlar**'ı seçin.
1. Bir satır ekleyin ve sertifikanın en son sürümüyle ilgili ayarları belirtin.
1. Yeni satırın **Öncelik** değerini artırın. Satırı, aynı sertifikanın önceki sürümünün satırı üzerinde olacak şekilde taşımak için **Yukarı taşı** düğmesini kullanın.
> [!NOTE]
> Commerce runtime'da ilk olarak sertifikanın yeni sürümü çağırılır. Sertifika henüz belirli bir mağazada veya belirli bir terminalde güncelleştirilmediyse, önceki sürüm çağrılır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

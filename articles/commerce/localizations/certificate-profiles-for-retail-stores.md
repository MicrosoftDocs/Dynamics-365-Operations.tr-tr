---
title: Perakende mağazaları için kullanıcı tarafından tanımlanmış sertifika profilleri
description: Bu konu, perakende mağazalarında sertifikaların nasıl kullanıldılarıyla ilgili genel bir bakış sağlar.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 03fe3d7fb64b2e9d0a06dc56654933f0c672782a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225757"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a>Perakende mağazaları için kullanıcı tarafından tanımlanmış sertifika profilleri

[!include [banner](../includes/banner.md)]


## <a name="overview"></a>Genel bakış

Bu konu, Microsoft Dynamics 365 Commerce içinde kullanılabilen sertifika profillerine genel bakış sağlar. Bu işlevsellik, yerel Sertifikalar için destek ekleyerek, [Perakende kanalları için gizli anahtarları yönetme](../dev-itpro/manage-secrets.md) özelliğini genişletir.

Satış noktası (POS) çevrimdışı modda çalışırken, anahtar kasasında depolanan sertifikalara erişemez. Bunun yerine yerel sertifika kullanılmalıdır. Aşağıdaki özellikler desteklenir:

- Anahtar kasası temel senaryolarında yerel sertifikaları kullanma
- Yerel sertifikaları anahtar kasası olmadan kullanma (örneğin, şirket içi kurulumda)
- Sertifikaların aşamalı güncelleştirmesi: bazı mağaza ve terminaller sertifikanın yeni bir sürümünü kullanır, ancak diğer mağazalar ve terminaller önceki sürümü kullanmaya devam eder

Sertifika profilleri işlevi, varsayılan bir sertifika belirtmenize ve aynı sertifika profilindeki sertifikaların aranacağı sırayı ayarlamanıza olanak tanır. Bu işlev ayrıca yerel sertifikalara ve Key Vault sertifikalarına benzer bir kurulum yaklaşımı sağlar. Sertifikalar için şirkete özgü ayarlar ekleyebilirsiniz ancak her bir sertifika için benzersiz şirketler arası tanımlayıcı Commerce kanallarında kullanılabilir.

### <a name="scenarios"></a>Senaryolar

Sertifika profilleri işlevi, Commerce kanallarında aşağıdaki senaryoları destekler:

- Anahtar kasası temel senaryolarında yerel bir sertifika kullanın. Aşağıda bazı temel senaryo örnekleri verilmiştir:

    - Anahtar kasası depolama alanına erişilemiyor.
    - Anahtar kasası depolama alanında bir sertifika bulunamadı.
    - POS, çevrimdışı modda çalışıyor.

- Yerel sertifikalar kullanın ancak bunları anahtar kasasına kaydetmeyin (örneğin, şirket içi kurulumda).
- Sertifikanın yeni bir sürümünün yalnızca mağazalarda veya yeni sürümün zaten kullanılabilir olduğu terminallerde kullanıldığı aşamalı sertifika güncelleştirmesi yapın.
- Aynı sertifikayı birkaç şirkette kullanın.

## <a name="set-up-certificate-profiles"></a>Sertifika profilleri ayarlama

Aşağıdaki yordamda sertifika profillerinin nasıl ayarlanacağı açıklanmaktadır. Commerce kanallarında sertifika profillerini kullanmadan önce, ayarları yapılandırmak için aşağıdaki adımları izleyin.

1. **Özellik Yönetimi** çalışma alanında, **Perakende mağazaları için kullanıcı tanımlı sertifika profilleri** özelliğini açın.
2. **Sistem yönetimi \> Kurulum \> Sertifika profilleri** seçeneğine gidin.
3. Kayıt oluşturun ve bunun için **Sertifika profili**, **Ad** ve **Açıklama** alanlarını ayarlayın.

    > [!NOTE]
    > Sertifika profili, tüm şirketler ve Commerce bileşenleri arasındaki sertifikanın benzersiz tanımlayıcısıdır.

3. **Tüzel kişilikler** sekmesinde bir satır ekleyin ve geçerli sertifika profilinin kullanılması gereken tüzel kişiliği (şirket) seçin. Sertifika profili birden çok tüzel kişilik için kullanılacaksa, her ek tüzel kişilik için bir satır eklemek üzere bu adımı tekrarlayın.
4. Sertifika profili için şirkete özgü ayarları girebileceğiniz **Sertifika profili ayarları** sayfasını açmak için **Ayarlar**'ı seçin.

### <a name="certificate-profile-settings"></a>Sertifika profili ayarları

Sertifika profili satırları için **Ayarlar**'ı seçtiğinizde, **Sertifika profili ayarları** sayfası görüntülenir. Bu sayfa, geçerli sertifika profili Commerce kanallarında çağrıldığında hangi sertifikaların kullanılabileceğini belirtmenizi sağlar. Ayrıca, sertifikaların aranacağı sırayı da belirtebilirsiniz.

> [!NOTE]
> **Öncelik** alanı otomatik olarak ayarlanır. **1** değeri en yüksek önceliği temsil eder. **Sertifika profili ayarları** sayfasında yeni bir satır eklendiğinde, önceliği önceki satırın önceliğinden bir fazla olan bir sayıya ayarlanır. Belirli bir satırın önceliğini değiştirmek için satırı seçin ve önceliği artırmak için **Yukarı taşı** veya önceliği azaltmak için **Aşağı taşı**'yı seçin.

**Sertifika profili ayarları** sayfasına yeni bir satır eklediğinizde , aşağıdaki alanları ayarlayın:

- **Konum türü** – Sertifikanın saklandığı konumu seçin. Bu alan iki olası değere sahiptir: **Yerel sertifika** ve **Key Vault**.
- **Key Vault sertifikası** – Bu alan, **Konum türü** alanını **Key Vault** olarak ayarlarsanız gereklidir. Key Vault sertifikası gizli anahtarı belirtmek için bunu kullanın.

    > [!NOTE]
    > Sertifika profillerinde Key Vault sertifikası kullanmadan önce, anahtar kasası depolama alanına bir sertifika yüklediğinizden emin olun ve [Azure Key Vault istemcisini ayarlama ](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client) yönergelerini izleyin.

- **Mağaza adı** – Bu alan isteğe bağlıdır ve yalnızca **Konum türü** alanını **Yerel sertifika** olarak ayarladığınızda kullanılabilir. Yerel sertifikaları aramak için kullanılacak varsayılan bir mağaza adı belirtmek için bunu kullanın.
- **Mağaza konumu** – Bu alan isteğe bağlıdır ve yalnızca **Konum türü** alanını **Yerel sertifika** olarak ayarladığınızda kullanılabilir. Yerel sertifikaları aramak için kullanılacak varsayılan bir mağaza konumu belirtmek için bunu kullanın.

    > [!NOTE]
    > Varsayılan mağaza adı ve mağaza konumu, Commerce Runtime içindeki yerel sertifikaları arama işlemini kolaylaştırmak için eklenir. X509StoreProvider, sertifikaların depolandığı klasörlerin listesine sahiptir. Varsayılan mağaza adı ve varsayılan mağaza konumu belirtilmezse, X509StoreProvider kendi listesindeki diğer klasörlerde bir sertifika bulmaya çalışır.

- **Parmak izi** – Bu alan gereklidir ve yalnızca **Konum türü** alanını **Yerel sertifika** olarak ayarladığınızda kullanılabilir. Sertifika parmak izini belirtmek için bunu kullanın.
- **Açıklamalar** – Bu alan isteğe bağlıdır ve kullanıcıların not girmesine izin verir.

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a>İş akışı: Commerce Runtime'da sertifikaları arama

Burada, Commerce runtime içinde bir sertifika profili çağrıldığında bir sertifikayı aramak için kullanılan temel iş akışı verilmektedir.

1. Sistem, sertifika profilinin geçerli tüzel kişilik için şirkete özel ayarlar içerip içermediğini tanımlar.
1. Sistem, **Öncelik** alanının **1** olarak ayarlandığı satır için **Sertifika profili ayarları** sayfasındaki değerleri kullanarak sertifikayı bulmaya çalışır.

    - **Konum türü** alanı **Key Vault** olarak ayarlanmışsa, **Anahtar kasası parametreleri** sayfasında sertifikayı aramak için **Key Vault sertifikası gizli anahtarı** alanının değeri kullanılır. Daha sonra sertifika, anahtar kasası depolama alanında aranır.
    - **Konum türü** alanı **Yerel sertifika** olarak ayarlanırsa X509StoreProvider, bu parametreler belirtilmişse, önce varsayılan mağaza adını ve mağaza konumunu kullanarak sertifikayı arar. Daha sonra kendi klasör listesindeki tüm klasörlerde arama yapar.

1. Sertifika bulunamazsa, **Öncelik** alanının **2** olarak ayarlandığı satır için bu işlem yinelenir ve bu şekilde devam eder.

> [!NOTE]
> Sertifika profilinin geçerli tüzel kişilik için ayarı yoksa veya sertifika araması **Sertifika profil ayarları** sayfasındaki tüm satırlar için başarısız olursa, sertifika bulunamaz.

#### <a name="caching-the-results-of-certificate-searches"></a>Sertifika aramalarının sonuçlarını önbelleğe alma

Sertifika aramalarının sonuçları önbelleğe alınır. Önbelleğin varsayılan son kullanma tarihi bir saattir. Ancak, bu süre özelleştirilebilir ve maksimum değer olan 24 saate ayarlanabilir.

### <a name="gradual-update"></a>Aşamalı güncelleştirme

Sertifikanın yeni bir sürümü tanıtılırsa ancak aynı anda tüm mağazalarda güncelleştirilemezse, sertifika profilleri işlevi sertifikanın aşamalı olarak güncelleştirilmesini sağlar.

1. Bir sertifika profili ve güncelleştirilmesi gereken satırı bulun ve **Ayarlar**'ı seçin.
1. Bir satır ekleyin ve sertifikanın en son sürümüyle ilgili ayarları belirtin.
1. Yeni satırın **Öncelik** değerini artırın. Satırı, aynı sertifikanın önceki sürümünün satırı üzerinde olacak şekilde taşımak için **Yukarı taşı** düğmesini kullanın.

> [!NOTE]
> Commerce runtime'da ilk olarak sertifikanın yeni sürümü çağırılır. Sertifika henüz belirli bir mağazada veya belirli bir terminalde güncelleştirilmediyse, önceki sürüm çağrılır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
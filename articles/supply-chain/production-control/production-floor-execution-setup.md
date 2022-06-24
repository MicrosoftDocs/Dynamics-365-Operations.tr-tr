---
title: Üretim katı yürütme arabirimini çalıştıracak bir cihaz ayarlama
description: Üretim katı yürütme arabirimi, üretim katındaki her cihaz için ayarlanır. Şirketler, genellikle cihazın hizmet verdiği amaca bağlı olarak her bir cihazı farklı şekilde kurar. Örneğin, bir şirketin teslim alma alanında, çalışanların giriş ve çıkış saatlerini girdikleri bir cihazı ve atölye katında çalışanların işlerini yönettiği başka bir cihazı olabilir.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0ae9ca901a7af8275db419e25a7297a77aab284e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857416"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimini çalıştıracak bir cihaz ayarlama

[!include [banner](../includes/banner.md)]

Üretim katı yürütme arabirimi, üretim katındaki her cihaz için ayarlanır. Şirketler, genellikle cihazın hizmet verdiği amaca bağlı olarak her bir cihazı farklı şekilde kurar. Örneğin, bir şirketin teslim alma alanında, çalışanların giriş ve çıkış saatlerini girdikleri bir cihazı ve atölye katında çalışanların işlerini yönettiği başka bir cihazı olabilir.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Belirli bir cihaz için konfigürasyon ve filtreleri ayarla

Bir cihazın konfigürasyon ve iş filtrelerini ayarlamak için, *Zaman gözetimini koru* görevini içeren güvenlik rolüne sahip bir hesabı kullanarak **Üretim katı yürütme** sayfasında oturum açın. (Kullanıma hazır güvenlik rolleri arasında, yalnızca *Atölye gözetmeni* bu göreve sahiptir.) Sonra aşağıdaki adımları izleyin.

1. Ayarlamak istediğiniz cihaza gidin ve Microsoft Dynamics 365 Supply Chain Management'ta atölye gözetmeni olarak oturum açın. (*Zaman gözetimini koru* görevini içeren bir hesap kullanın.)
1. Ayarlamakta olduğunuz cihaz için kullanılabilir bir konfigürasyon olduğundan emin olun. Herhangi bir konfigürasyon bulunmuyorsa, varsayılan konfigürasyon sağlanır. Konfigürasyon ayarlama hakkında daha fazla bilgi için bkz[Üretim katı yürütme arabirimini yapılandırma](production-floor-execution-configure.md).
1. **Üretim denetimi \> Üretim yürütme \> Üretim katı yürütmesi**'ne gidin.

    Üretim katı yürütme arabirimi geçerli cihazda en az bir kez yapılandırıldıysa, bir oturum açma sayfası görüntülenir. Aksi durumda karşılama sayfası görüntülenir.

1. Oturum açma sayfasında veya karşılama sayfasında, **Yapılandır**'ı seçin.
1. Listeden konfigürasyon seçin.
1. **Sonraki**'yi seçin.
1. Geçerli cihaza uygulamak için bir veya daha fazla filtre seçin. Bu filtreler, yalnızca ilgili işlerin cihazda gösterildiğinden emin olmanıza yardımcı olur. Filtre ayarlamak için, bir değer listesi açmak üzere filtre türünü seçin ve sonra filtre uygulanacak değeri seçin. Aşağıdaki filtreler kullanılabilir:

    - **Üretim birimi**: Bu filtre en üst düzey filtredir. Genellikle, birçok kaynak grubu ve bağımsız kaynak içeren büyük bir çalışma alanı anlamına gelir.
    - **Kaynak grubu**: Bu filtre bir orta düzey filtredir. Genellikle çalışma alanının sınırlı alanındaki bir ilgili kaynaklar koleksiyonu anlamına gelir. Önce bir **üretim birimi** filtresi seçerseniz, kaynak grupları listesi yalnızca bu birimdeki grupları gösterir. Aksi durumda, kullanılabilir tüm kaynak gruplarını gösterir.
    - **Kaynak**: Bu filtre en spesifik filtredir. Genellikle belirli bir makine veya tek bir kaynağı ifade eder. Önce bir **Kaynak grubu** ve/veya **üretim birimi** filtresi seçerseniz, kaynak listesi yalnızca bu grup ve/veya birimdeki kaynakları gösterir. Aksi durumda, kullanılabilir tüm kaynakları gösterir.

1. **Tamam**'ı seçin.
1. Oturum açma sayfası görünür ve cihazınız kullanıma hazırdır.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Bir çalışanın varsayılan filtreleri geçersiz kılmasına izin ver

Belirli çalışanlara, kullandıkları tüm cihazların filtre ayarlarını değiştirme izni verebilirsiniz. Bu izne sahip olan çalışanlar için, üretim katı yürütme arabirimi **tüm işler** ve **etkin iş** sayfalarında bir **filtre** düğmesi sağlar.

> [!NOTE]
> Bir çalışan bir filtreyi değiştirirse, cihazda oturum açan tüm kullanıcılar için yeni filtre o andan itibaren uygulanır.

Bir çalışanın bir cihaz için ayarlanmış olan varsayılan iş filtrelerini geçersiz kılmasına izin vermek için, aşağıdaki adımları izleyin.

1. **Saat ve işe devam \> Kurulum \> Zaman kayıtlı çalışanlar**'a gidin.
1. Bu çalışanın **Zaman kayıtlı çalışanlar** sayfasını açmak için listeden bir çalışan seçin.
1. **Zaman kaydı** sekmesinde, **filtre ayarla** seçeneğini *Evet* olarak ayarlayın.

## <a name="run-the-interface-in-full-screen-mode"></a>Arabirimi tam ekran modunda çalıştırma

Genellikle, üretim katı yürütme arabirimini o amaçla özel olarak kullanılan bir cihazda çalıştırırsınız. Bu nedenle, herhangi bir gezinti ve/veya Chrome tarayıcı göstermeden, arabirimi tam ekran modunda çalıştırmak mantıklı olabilir.

- Supply Chain Management'ta gösterilen gezinme bölmesini gizlemek için, tarayıcının adres çubuğunda şu metni URL'nin sonuna ekleyin:`\&limitednav=true`.
- Tarayıcının adres çubuğunu gizlemek için de tarayıcının yerel tam ekran modunu kullanın. (Yönergeler için, tarayıcınızın belgelerine bakın.)

Aşağıdaki çizimin üst bölümünde arabirimin varsayılan olarak nasıl göründüğü gösterilmektedir. Alt bölüm, gezinti bölmesi gizli olduğunda tam ekran modunda nasıl göründüğünü gösterir.

![Standart ve tam ekran arabirim karşılaştırması.](media/pfei-full-screen.png "Standart ve tam ekran arabirim karşılaştırması")

## <a name="extend-the-session-past-12-hours"></a>Oturumu 12 saatten fazla uzatma

Varsayılan olarak, üretim katı yürütme arabirimi hiç kimse tarafından 12 saat boyunca kullanılmazsa otomatik olarak oturumu kapatır. Bir Supply Chain Management kullanıcısının yeniden oturum açması gerekir. Ancak, zaman aşımı limitini 90 güne kadar uzatabilirsiniz.

Zaman aşımı limitini uzatmak için, Supply Chain Management'ta oturum açın ve **Sistem Yönetimi \> kullanıcıları \> oturum uzantılarına** gidin. Cihazda oturum açmak için kullanılan Supply Chain Management kullanıcı hesabını ve oturumun etkin kalacağı saat sayısını belirtin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

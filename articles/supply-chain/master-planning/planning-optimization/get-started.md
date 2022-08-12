---
title: Planlama Optimizasyonunu kullanmaya başlama
description: Bu makalede, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: e853c8a482b8fd0b92c9861fe022c056915ab405
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112225"
---
# <a name="get-started-with-planning-optimization"></a>Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama

[!include [banner](../../includes/banner.md)]

[Daha önce duyurulduğu](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) gibi, Planlamayı En İyi Duruma Getirme varolan yerleşik master planlama altyapısının yerini almak üzere planlanmıştır.

Yerleşik Master planlama altyapısını kullanıyorsanız, şimdi Planlamayı En İyi Duruma Getirme için geçişinizi planlamaya başlamanız gerekir. Yükseltme işlemi zorlandığında işlemleriniz etkilenebileceğinden, geçiş işlemini hemen başlatmak önemlidir. Kullanımdan kaldırma zorunlu olduğunda yaşanacak son dakika sorunlarını önlemek için geçişi 1 Aralık 2020'den önce tamamlamanızı öneririz. 

Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir. Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir. Planlamayı En İyi Duruma Getirme işlevi şu anda Dynamics Lifecycle Services (LCS)'de varsayılan olarak etkin değil; bu nedenle özellik açılmadan önce değerlendirme yapma fırsatına sahipsiniz.

> [!NOTE]
> Master planlama işleminiz üretim (Master planlamayla oluşturulmuş planlanmış üretim emirleri) içermiyorsa ve yerleşik Master planlama altyapısının 10.0.15 üstü sürümü olmasını istiyorsanız, Planlamayı En İyi Duruma Getirme işlevine geçiş için bir özel durum istemeniz gerekir. Sürüm 10.0.16 itibarıyla, planlı üretim emirleri olmadan yerleşik master planlama çalıştırıldığında ortamlarda bir hata gösterilecektir. Master planlama sırasında planlı üretim emirleri oluşturmayan tüm yeni dağıtımlar için Planlamayı En İyi Duruma Getirme işlevi kullanılmalıdır. Planlı üretim emirleri olmadan Yerleşik Master planlama altyapısını çalıştıran mevcut ortamların sahipleri, özel durum işlemiyle ilgili ayrıntıların bulunduğu bir posta alacaktır. Planlamayı En İyi Duruma Getirme için geçişi değerlendirmek ve planlamak üzere bir iş ortağı ile çalışmanız önerilir.

Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).

## <a name="availability"></a>Kullanılabilirlik

Planlamayı En İyi Duruma Getirme şu anda şu Azure coğrafi bölgelerinde kullanılabilir: Amerika Birleşik Devletleri, Kanada, Brezilya, Avrupa, Fransa, Birleşik Krallık, Avustralya, Asya Pasifik, Japonya ve Hindistan. Eklentiyi başka bir coğrafi bölgeden yüklemeye çalışırsanız, LCS bu coğrafi bölgenin desteklenmediğini belirten bir ileti gösterir. Azure Geographies ve ilgili bölgeler hakkında daha fazla bilgi için bkz. [Azure bölgeleri](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Planlamayı En İyi Duruma Getirme'nin Dynamics 365 Supply Chain Management şirket içi dağıtımlarını desteklemediğini unutmayın.

## <a name="licensing"></a>Lisans

Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.

## <a name="install-and-enable-planning-optimization"></a>Planlamayı En İyi Duruma Getirmeyi yükleme ve etkinleştirme

Planlamayı En İyi Duruma Getirme'yi kullanmak için, sisteminizin tüm ön koşulları karşıladığından emin olmanız ve ardından lisans anahtarını etkinleştirip Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yüklemeniz gerekir.

### <a name="prerequisites"></a>Önkoşullar

Planlamayı En İyi Duruma Getirme Eklentisini yüklemeden önce aşağıdaki ön koşulların karşılanması gerekir:

- Supply Chain Management'da şurada çalıştırıyor olmanız gerekir: LCS etkin yüksek kullanılabilirlik ortamı, katman 2 veya üstü (OneBox ortamı değil); Dynamics 365 Supply Chain Management sürüm 10.0.7 veya sonraki bir sürüm. Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz ve yükleme işlemini iptal etmeniz gerekir.

- Sisteminiz, Power Platform tümleştirmesi için ayarlanmış olmalıdır. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamaları ile Microsoft Power Platform tümleştirmesi](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Planlamayı En İyi Duruma Getirme lisansını etkinleştirme

Planlamayı En İyi Duruma Getirme eklentisini kullanabilmek için yapılandırma anahtarını etkinleştirmeniz gerekir. Bunun için:

1. Sisteminizi [Bakım modu](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım moduna alın.
1. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
1. **Yapılandırma anahtarları** sekmesinde, **Planlamayı En İyi Duruma Getirme** onay kutusunu seçin.
1. [Bakım modu](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım modunu kapatın.

### <a name="install-the-planning-optimization-add-in"></a>Planlamayı En İyi Duruma Getirme Eklentisini Yükleme

Eklentiyi LCS projenizden yüklemeniz ve Supply Chain Management kullanıcı arabiriminden Planlamayı En İyi Duruma Getirme işlevini açmanız gerekir.

Planlamayı En İyi Duruma Getirme Eklentisini yüklemek için:

1. LCS'de oturum açın ve istediğiniz ortamı açın.
1. **Tüm ayrıntılar**'a gidin.
1. **Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.
1. **Yeni eklenti yükle**'yi seçin.
1. **Planlamayı En İyi Duruma Getirme**'yi seçin.
1. Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.
1. **Yükle**'yi seçin.
1. **Ortam eklentileri** hızlı sekmesinde, Planlamayı En İyi Duruma Getirme'nin yüklendiğini görmeniz gerekir.
1. Birkaç dakika sonra **Yükleniyor** durumu **Yüklendi** olarak değişecektir (sayfayı yenilemeniz gerekebilir). Yüklendiğinde, Planlamayı En İyi Duruma Getirme'yi Dynamics 365 Supply Chain Management'ta etkinleştirmeye hazırsınız demektir.

Planlamayı En İyi Duruma Getirme Eklentisini yüklemenin temel amacı, hizmet ile ortamı bağlamaktır. Bu nedenle, ortamlar arasına taşınacak kod ne olursa olsun, eklentiyi, Planlama İyileştirmesi'ni kullanacağınız her ortama ayrı ayrı yüklemelisiniz.

## <a name="integrate-planning-optimization-with-your-system"></a>Planlamayı En İyi Duruma Getirme ile sisteminizi tümleştirme

Planlamayı En İyi Duruma Getirme eklentisinin master planlama için kullanılması gerekip gerekmediğini yapılandırmak üzere **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme parametreleri**'ne gidin.

### <a name="connection-status"></a>Bağlantı durumu

Bağlantı durumu, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasındaki bağlantının geçerli durumunu belirtir. Aşağıdaki tabloda, olası değerler gösterilmektedir.

| Bağlantı durumu | Tanım | Planlamayı En İyi Duruma Getirme kullanılabilir mi? |
|---|---|---|
| Bağlı | Planlamayı En İyi Duruma Getirme hizmeti ile Supply Chain Management arasında bir bağlantı oluşturuldu. | Evet |
| Bağlantı etkinleştiriliyor | Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı açma isteği şu anda devam ediyor. | Hayır |
| Bağlantı kesildi | Planlamayı En İyi Duruma Getirme hizmeti için bağlantı mevcut değil. Bağlantı, bu makalede daha önce açıklandığı gibi LCS'den açılabilir. | No. |
| Bağlantı devre dışı bırakılıyor | Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı kapatma isteği şu anda devam ediyor. | Hayır |
| Durum alınıyor | Sistem, Planlamayı En İyi Duruma Getirme hizmetinden durum bilgisi bekliyor. | Hayır |

### <a name="the-use-planning-optimization-option"></a>Planlamayı En İyi Duruma Getirmeyi Kullan seçeneği

**Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği, master planlama için hangi planlama altyapısının kullanılacağını belirler:

- **Evet**: Master planlama için Planlamayı En İyi Duruma Getirme hizmeti kullanılır.
- **Hayır**: Master planlama için yerleşik Supply Chain Management planlama altyapısı kullanılır.

Bu ayar tüm tüzel kişilikler (şirketler) için geçerlidir. Planlamayı En İyi Duruma Getirme bazı tüzel kişiliklerde mümkün değildir. Bazı tüzel kişiliklerde ise master planlama kullanılamaz.

> [!NOTE]
> Yerleşik Supply Chain Management planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.

### <a name="integration-with-the-setup"></a>Ayarla tümleştirme

Planlama İyileştirmesi açıksa master planlama, Planlama İyileştirmesi Eklentisi'ni kullanarak yapılır. Bu durumda, master planlama sonuçları ve özellikleri etkilenir.

## <a name="additional-resources"></a>Ek kaynaklar

[Önizleme için hüküm ve koşullar](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planlamayı En İyi Duruma Getirmeye genel bakış](planning-optimization-overview.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)

[Planlama işini iptal etme](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


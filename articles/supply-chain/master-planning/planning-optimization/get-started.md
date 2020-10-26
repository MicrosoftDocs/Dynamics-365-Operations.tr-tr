---
title: Planlamayı En İyi Duruma Getirmeye başlayın
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973488"
---
# <a name="get-started-with-planning-optimization"></a>Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama

[!include [banner](../../includes/banner.md)]

[Daha önce duyurulduğu](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios) gibi, Planlamayı En İyi Duruma Getirme varolan yerleşik master planlama altyapısının yerini almak üzere planlanmıştır.

Yerleşik Master planlama altyapısını kullanıyorsanız, şimdi Planlamayı En İyi Duruma Getirme için geçişinizi planlamaya başlamanız gerekir. Yükseltme işlemi zorlandığında işlemleriniz etkilenebileceğinden, geçiş işlemini hemen başlatmak önemlidir. Kullanımdan kaldırma zorunlu olduğunda yaşanacak son dakika sorunlarını önlemek için geçişi 1 Aralık 2020'den önce tamamlamanızı öneririz. 

Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir. Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir. Planlamayı En İyi Duruma Getirme işlevi şu anda Dynamics Lifecycle Services (LCS)'de varsayılan olarak etkin değil; bu nedenle özellik açılmadan önce değerlendirme yapma fırsatına sahipsiniz.

> [!NOTE]
> Master planlama işleminiz üretim (Master planlamayla oluşturulmuş planlanmış üretim emirleri) içermiyorsa ve yerleşik Master planlama altyapısının 10.0.15 üstü sürümü olmasını istiyorsanız, Planlamayı En İyi Duruma Getirme işlevine geçiş için bir özel durum istemeniz gerekir. Sürüm 10.0.16 itibarıyla, planlı üretim emirleri olmadan yerleşik master planlama çalıştırıldığında ortamlarda bir hata gösterilecektir. Master planlama sırasında planlı üretim emirleri oluşturmayan tüm yeni dağıtımlar için Planlamayı En İyi Duruma Getirme işlevi kullanılmalıdır. Planlı üretim emirleri olmadan Yerleşik Master planlama altyapısını çalıştıran mevcut ortamların sahipleri, özel durum işlemiyle ilgili ayrıntıların bulunduğu bir posta alacaktır. Planlamayı En İyi Duruma Getirme için geçişi değerlendirmek ve planlamak üzere bir iş ortağı ile çalışmanız önerilir.

Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).

### <a name="availability"></a>Kullanılabilirlik
Planlamayı En İyi Duruma Getirme şu anda şu Azure coğrafi bölgelerinde kullanılabilir: Amerika Birleşik Devletleri, Kanada, Avrupa, Birleşik Krallık ve Avustralya. Eklentiyi başka bir coğrafi bölgeden yüklemeye çalışırsanız, LCS bu coğrafi bölgenin desteklenmediğini belirten bir ileti gösterir.

Planlamayı En İyi Duruma Getirme'nin Dynamics 365 Supply Chain Management şirket içi dağıtımlarını desteklemediğini unutmayın.

### <a name="licensing"></a>Lisans

Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.

### <a name="install-the-add-in"></a>Eklentiyi yükleme

Planlamayı En İyi Duruma Getirme hizmetini kullanmak üzere Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yükleyin. Eklentiye LCS projenizden ulaşabilir ve Supply Chain Management kullanıcı arabiriminden (UI) Planlamayı En İyi Duruma Getirme hizmetini açabilirsiniz.

> [!NOTE]
> Planlamayı En İyi Duruma Getirme için gereksinim, bir LCS etkin yüksek kullanılabilirlik ortamı, katman 2 veya üstüdür (OneBox ortamı değil); Dynamics 365 Supply Chain Management sürüm 10.0.7 veya daha yenisine sahip olmalıdır. Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz ve yükleme işlemini iptal etmeniz gerekir.

1. LCS'de oturum açın ve istediğiniz ortamı açın.
1. **Tüm ayrıntılar**'a gidin.
1. **Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.
1. **Yeni eklenti yükle**'yi seçin.
1. **Planlamayı En İyi Duruma Getirme**'yi seçin.
1. Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.
1. **Yükle**'yi seçin.
1. **Ortam eklentileri** hızlı sekmesinde, Planlamayı En İyi Duruma Getirme'nin yüklendiğin görmeniz gerekir.
1. Birkaç dakika sonra **Yükleme** durumunun değişip **Yüklendi**olarak değişecektir (sayfayı yenilemeniz gerekebilir). Yüklendiğinde, Planlamayı En İyi Duruma Getirme'yi Dynamics 365 Supply Chain Management'ta etkinleştirmeye hazırsınız demektir.

### <a name="planning-optimization-integration"></a>Planlamayı En İyi Duruma Getirme tümleştirmesi

Planlamayı En İyi Duruma Getirme eklentisinin master planlama için kullanılması gerekip gerekmediğini yapılandırmak üzere **Master planlama** \> **Ayar** \> **Planlamayı En İyi Duruma Getirme parametreleri**'ne gidin.

#### <a name="connection-status"></a>Bağlantı durumu

Bağlantı durumu, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasındaki bağlantının geçerli durumunu belirtir. Aşağıdaki tabloda, olası değerler gösterilmektedir.

| Bağlantı durumu | Tanım | Planlamayı En İyi Duruma Getirme kullanılabilir mi? |
|---|---|---|
| Bağlı | Planlamayı En İyi Duruma Getirme hizmeti ile Supply Chain Management arasında bir bağlantı oluşturuldu. | Evet |
| Bağlantı etkinleştiriliyor | Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı açma isteği şu anda devam ediyor. | Hayır |
| Bağlantı kesildi | Planlamayı En İyi Duruma Getirme hizmeti için bağlantı mevcut değil. Bağlantı, bu konuda daha önce açıklandığı gibi LCS'den açılabilir. | Hayır |
| Bağlantı devre dışı bırakılıyor | Planlamayı En İyi Duruma Getirme hizmeti için bağlantıyı kapatma isteği şu anda devam ediyor. | Hayır |
| Durum alınıyor | Sistem, Planlamayı En İyi Duruma Getirme hizmetinden durum bilgisi bekliyor. | Hayır |

#### <a name="the-use-planning-optimization-option"></a>Planlamayı En İyi Duruma Getirmeyi Kullan seçeneği

**Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği, master planlama için hangi planlama altyapısının kullanılacağını belirler:

- **Evet**: Master planlama için Planlamayı En İyi Duruma Getirme hizmeti kullanılır.
- **Hayır**: Master planlama için yerleşik Supply Chain Management planlama altyapısı kullanılır.

> [!NOTE]
> Yerleşik Supply Chain Management planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlamayı En İyi Duruma Getirmeyi Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.

### <a name="integration-with-the-setup"></a>Ayarla tümleştirme

Planlamayı En İyi Duruma Getirme önizlemesi açıksa master planlama, Planlamayı En İyi Duruma Getirme Eklentisi'ni kullanarak yapılır. Bu durumda, master planlama sonuçları ve özellikleri etkilenir.

## <a name="additional-resources"></a>Ek kaynaklar

[Önizleme için hüküm ve koşullar](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planlamayı En İyi Duruma Getirmeye genel bakış](planning-optimization-overview.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)

[Planlama işini iptal etme](cancel-planning-job.md)

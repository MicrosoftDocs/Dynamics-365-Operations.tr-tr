---
title: Planlamayı En İyi Duruma Getirmeye başlayın
description: Bu konuda, Planlamayı En İyi Duruma Getirme işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
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
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213527"
---
# <a name="get-started-with-planning-optimization"></a>Planlamayı En İyi Duruma Getirmeye başlayın

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Planlamayı En İyi Duruma Getirme işlevi şu anda Microsoft Dynamics 365 Supply Chain Management'ta yerleşik olan planlama altyapısında kullanılabilen tüm özellikleri desteklememektedir. Bu nedenle, Planlamayı En İyi Duruma Getirme hizmetinde şu anda mevcut olan özellik kümesinin gereksinimlerinizi karşılayıp karşılamadığını değerlendirmeniz önemlidir. Varsayılan olarak, Planlamayı En İyi Duruma Getirme işlevi Dynamics Lifecycle Services'ta (LCS) açılmaz. Bu nedenle, açılmadan önce değerlendirme yapma fırsatınız vardır.

Sonuç olarak, Planlamayı En İyi Duruma Getirme hizmeti var olan yerleşik Supply Chain Management planlama altyapısının yerini alacaktır.

Planlamayı En İyi Duruma Getirme hizmetini açmadan önce Planlamayı En İyi Duruma Getirme uygunluk analizinin sonuçlarını değerlendirmenizi öneririz. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Lisans

Geçerli lisansınızı kullanarak master planlamayı çalıştırabilirseniz Planlamayı En İyi Duruma Getirme hizmetini kullanmaya başlamak için ek lisans satın almanız gerekmez.

### <a name="install-the-add-in"></a>Eklentiyi yükleme

Planlamayı En İyi Duruma Getirme hizmetini kullanmak üzere Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi'ni yükleyin. Eklentiye LCS projenizden ulaşabilir ve Supply Chain Management kullanıcı arabiriminden (UI) Planlamayı En İyi Duruma Getirme hizmetini açabilirsiniz.

> [!NOTE]
> En iyi duruma getirme planlaması için gereksinim, bir LCS etkin yüksek kullanılabilirlik ortamıdır (OneBox ortamı değil); Dynamics 365 Supply Chain Management sürüm 10.0.7 veya daha yenisine sahip olmalıdır.

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

## <a name="related-resources"></a>İlgili kaynaklar

[Önizleme için hüküm ve koşullar](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planlamayı En İyi Duruma Getirmeye genel bakış](planning-optimization-overview.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)

[Planlama işini iptal etme](cancel-planning-job.md)

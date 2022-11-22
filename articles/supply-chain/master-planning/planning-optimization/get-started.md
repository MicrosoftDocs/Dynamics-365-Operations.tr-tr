---
title: Master planlamayı kullanmaya başlama
description: Bu makalede, Dynamics 365 Supply Chain Management uygulamasında master planlama işlevini kullanmaya nasıl başlanacağı açıklanmaktadır.
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
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780420"
---
# <a name="get-started-with-master-planning"></a>Master planlamayı kullanmaya başlama

[!include [banner](../../includes/banner.md)]

Supply Chain Management'ta master planlama işlevi Dynamics 365 Supply Chain Management için Planlama Optimizasyonu Eklentisi adlı harici bir hizmet tarafından sağlanır. Bu konuda, bu hizmetin nasıl edinilip ayarlanacağı açıklanmaktadır.

## <a name="availability"></a>Kullanılabilirlik

Planlamayı En İyi Duruma Getirme şu anda şu Azure coğrafi bölgelerinde kullanılabilir: Amerika Birleşik Devletleri, Kanada, Brezilya, Avrupa, Fransa, Birleşik Krallık, Norveç, İsviçre, Avustralya, Asya Pasifik, Japonya ve Hindistan. Eklentiyi başka bir coğrafi bölgeden yüklemeye çalışırsanız, LCS bu coğrafi bölgenin desteklenmediğini belirten bir ileti gösterir. Azure Geographies ve ilgili bölgeler hakkında daha fazla bilgi için bkz. [Azure bölgeleri](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

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
- **Hayır** – Master planlama için kullanımdan kaldırılan master planlama altyapısı kullanılır.

Bu ayar tüm tüzel kişilikler (şirketler) için geçerlidir. Planlama Optimizasyonu bazı tüzel kişiliklerde kullanılamaz. Bazı tüzel kişiliklerde ise kullanımdan kaldırılan master planlama altyapısı kullanılamaz.

> [!NOTE]
> Kullanımdan kaldırılan master planlama altyapısı için oluşturulan mevcut planlama toplu işleri, **Planlama Optimizasyonunu Kullan** seçeneği **Evet** olarak ayarlanırken tetiklenirse bu işler başarısız olur.

### <a name="integration-with-the-setup"></a>Ayarla tümleştirme

Planlama İyileştirmesi açıksa master planlama, Planlama İyileştirmesi Eklentisi'ni kullanarak yapılır. Bu durumda, master planlama sonuçları ve özellikleri etkilenir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

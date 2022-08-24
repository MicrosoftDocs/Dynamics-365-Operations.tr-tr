---
title: Lifecycle Services'dan çift yazma kurulumu
description: Bu makalede, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: laswenka
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: dda0b20492a109e4c3781db520ac19c325e0b403
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289193"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services'dan çift yazma kurulumu

[!include [banner](../../includes/banner.md)]



Bu makalede, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

Müşterilerin, Power Platform tümleştirmesini aşağıdaki konularda açıklandığı gibi tamamlaması gerekir:

- Henüz Microsoft Power Platform'u kullanmıyorsanız ve platform özelliklerini ekleyerek finans ve operasyon ortamlarınızı genişletmek istiyorsanız bkz. [Power Platform Tümleştirmesi - Ortam dağıtımı sırasında etkinleştirme](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Zaten Dataverse ve Power Platform ortamlarınız varsa ve bunları finans ve operasyon ortamlarına bağlamak istiyorsanız bkz. [Power Platform tümleştirmesi - Ortam dağıtımından sonra etkinleştirme](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Yeni veya mevcut Dataverse ortamları için çift yazmayı ayarlama

LCS **Ortam Ayrıntıları** sayfasından çift yazma ayarlamak için şu adımları izleyin:

1. **Ortam Ayrıntıları** sayfasında **Power Platform Tümleştirme** bölümünü genişletin.

2. **Çift yazma uygulaması** düğmesini seçin.

    ![Power Platform tümleştirmesi.](media/powerplat_integration_step2.png)

3. Hüküm ve koşulları inceleyin ve ardından **Yapılandır**'ı seçin.

4. Devam etmek için **Tamam**'ı seçin.

5. Ortam ayrıntıları sayfasını düzenli aralıklarla yenileyerek ilerleme durumunu izleyebilirsiniz. Kurulum genellikle 30 dakika veya daha az sürer.  

6. Kurulum tamamlandığında, işlemin başarılı olup olmadığını veya bir hata olup olmadığını bildiren bir ileti bildirir. Kurulum başarısız olursa, ilgili bir hata iletisi görüntülenir. Sonraki adıma geçmeden önce hataları düzeltmeniz gerekir.

7. Geçerli ortamın veritabanları ile Dataverse arasında bağlantı oluşturmak için **Power Platform Ortama bağla**'yı seçin. Bu genellikle 5 dakikadan daha az sürer.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Power Platform ortamı bağlantısı.":::

8. Bağlama tamamlandığında, bir köprü görüntülenir. Finans ve operasyon ortamındaki çift yazma yönetim alanına giriş yapmak için bağlantıyı kullanın. Buradan varlık eşlemeleri ayarlayabilirsiniz.

## <a name="linking-mismatch"></a>Bağlama uyuşmazlığı

Çift yazma ortamınız Dataverse örneğine bağlıyken LCS, Power Platform tümleştirmesi için ayarlanmamış olabilir. Bu bağlama uyuşmazlığı, beklenmeyen davranışlara neden olabilir. LCS ortam ayrıntılarının, çift yazmada bağlı olduğunuz örnekle eşleşmesi önerilir. Böylece iş olayları, sanal tablolar ve eklentiler aynı bağlantıyı kullanır.

Ortamınızda bağlama uyuşmazlığı varsa LCS'de ortam ayrıntıları sayfanızda şu örneğe benzer bir uyarı gösterilir: "Microsoft, ortamınızın Çift yazma aracılığıyla Power Platform Tümleştirmesi'nde belirtilenden farklı bir hedefe bağlandığını algıladı; bu önerilen bir durum değildir".

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform tümleştirme bağlantısı eşleşmiyor.":::

Bu uyarıyı alırsanız aşağıdaki çözümlerden birini deneyin:

- LCS ortamınız daha önce Power Platform tümleştirmesi için ayarlanmadıysa bu makaledeki yönergeleri izleyerek çift yazmada yapılandırılan Dataverse örneğine bağlanabilirsiniz.
- LCS ortamınız zaten Power Platform tümleştirmesi için ayarlandıysa, çift yazma bağlantısını kaldırmalı ve [Senaryo: Bağlamayı sıfırlama veya değiştirme](relink-environments.md#scenario-reset-or-change-linking) makalesini kullanarak LCS'de belirtilen bağlantıya bağlanmalısınız.

Geçmişte, el ile destek bileti oluşturma seçeneği sunuluyordu ancak bu dönemde henüz 1. seçenek yoktu.  Microsoft, artık Destek biletleri aracılığıyla el ile bağlantı oluşturma isteklerini desteklememektedir.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


---
title: Veri tümleştirme sorunlarını giderme kılavuzu
description: Bu konu, Finance and Operations uygulamaları ile Common Data Service arasında veri tümleştirme hakkında sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 35c0a1e6342008bc2ee6ff25a1663e199c8cb985
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771037"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Veri tümleştirme sorunlarını giderme kılavuzu

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Common Data Service'teki Eklenti izleme günlüklerini etkinleştirin ve çift yazma eklentisi hata ayrıntılarını kontrol edin

[!include [banner](../includes/banner.md)]

Çift-yazma eşitleme sırasında bir sorunla veya hatayla karşılaşırsanız izleme günlüğündeki hataları denetlemek için aşağıdaki adımları izleyin.

1. Hataları incelemeniz için önce eklenti izleme günlüklerini etkinleştirmelisiniz. Yönergeler için [Öğretici: Bir ekletiyi yazma ve kaydetme](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)'deki "İzleme günlüğü görüntüle" bölümüne bakınız.

    Şimdi hataları inceleyebilirsiniz.

2. Microsoft Dynamics 365 Sales'te oturum açın.
3. **Ayarlar** düğmesini (çark simgesi) seçin ve sonra **Gelişmiş ayarlar**'ı seçin.
4. **Ayarlar** menüsünde **Özelleştirme \> Eklenti izleme günlüğü**'nü seçin.
5. Hata ayrıntılarını görüntülemek için **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**'i tür adı olarak seçin.

## <a name="inspect-dual-write-synchronization-errors"></a>Çift yazma eşitleme hatalarını denetleyin

Test sırasında hataları incelemek için bu adımları izleyin.

1. Microsoft Dynamics Lifecycle Services (LCS)'de oturum açın.
2. Çift-yazma testi yapmak için LCS projesini açın.
3. **Bulutta barındırılan ortamlar**'ı seçin.
4. LCS 'de gösterilen yerel hesabı kullanarak uygulama sanal makinesinde (VM) Uzak Masaüstü bağlantısı oluşturun.
5. Olay Görüntüleyiciyi açın. 
6. **Uygulamalar ve Hizmetler günlükleri \> Microsoft \> Dynamics \> AX-DualWriteSync \> İşletim**'e gidin. Hatalar ve ayrıntılar görüntülenir.

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>Uygulamadan bir Common Data Service ortam bağlantısını kaldırın ve başka bir ortama bağlayın

Bağlantıları güncelleştirmek için bu adımları izleyin.

1. Uygulama ortamına gidin.
2. Veri Yönetimini açın.
3. **Uygulamalar için CDS bağlantısı**'nı seçin.
4. Çalışan tüm eşlemeleri seçin ve **Durdur**'u seçin.
5. Tüm eşlemeleri seçin ve **Sil**'i seçin.

    > [!NOTE]
    > **CustomerV3-Account** şablonu seçiliyse **Sil** seçeneği uygun olmaz. Bu şablonun seçimini gerektiği gibi temizleyin. **CustomerV3-Account** eski bir sağlanan şablondur ve Müşteri Adayı'ndan Nakde çözümü ile çalışır. Genel olarak yayımlandığından tüm şablonlar altında gösterir.

6. **Ortam bağlantısını kaldırma**'yı seçin.
7. Operasyonu onaylamak için **Evet**'i seçin.
8. Yeni ortamı bağlamak için, [yükleme kılavuzundaki](https://aka.ms/dualwrite-docs) adımları izleyin.

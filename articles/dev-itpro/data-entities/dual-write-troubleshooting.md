---
title: Veri tümleştirme sorunlarını giderme kılavuzu
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations ile Common Data Service arasında veri tümleştirme hakkında sorun giderme bilgileri sağlar.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797287"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Veri tümleştirme sorunlarını giderme kılavuzu

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Common Data Service'teki Plugin Trace'i etkinleştirin ve çift yazma eklentisi hata ayrıntılarını kontrol edin

Bir sorun veya çift yazma eşitlemesi hatasıyla karşı karşıya iseniz, izleme günlüğünde hataları inceleyebilirsiniz:

1. Hataları incelemek için önce Eklenti izlemeyi etkinleştirmek için [Kayıt eklentisi](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) yönergelerini kullanarak Eklenti izlemeyi etkinleştirmeniz gerekir. Şimdi hataları inceleyebilirsiniz.
2. Dynamics 365 for Sales'de oturum açın.
3. Ayarlar simgesine (dişli) tıklayın ve **Gelişmiş ayarlar**'ı seçin.
4. **Ayarlar** menüsünde **Özelleştirme > Eklenti izleme günlüğünü**seçin.
5. Hata ayrıntılarını görüntülemek için **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** türü adını tıklatın.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Finance and Operations'ta çift yazma eşitleme hatalarını denetle

Aşağıdaki adımları izleyerek test sırasında hataları denetleyebilirsiniz:

+ LifeCycle Services (LCS)'ye giriş yapın.
+ Çift yazma sınaması gerçekleştirmek için seçtiğiniz LCS projesini açın.
+ Bulutta Barındırılan Ortamlar'a gidin.
+ LCS'de görüntülenen yerel hesabı kullanarak Finance and Operations VM'ye uzak masaüstü.
+ Olay görüntüleyiciyi açın. 
+ **Uygulamalar ve Hizmetler günlükleri > Microsoft > Dynamics > AX-DualWriteSync > İşletim**'e gidin. Hatalar ve ayrıntılar görüntülenir.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Finance and Operations'tan başka bir Common Data Service ortam bağlantısını kaldırma

Aşağıdaki adımları izleyerek bağlantıları güncelleştirebilirsiniz:

+ Finance and Operations ortamınıza gidin.
+ Veri Yönetimini açın.
+ **Uygulamalar için CDS bağlantısı**'na tıklayın.
+ Çalışan tüm eşlemeleri seçin ve **Durdur**'u tıklatın. 
+ Tüm eşlemeleri seçin ve **Sil**'i tıklatın.

    > [!NOTE]
    > **CustomerV3-Account** şablonu seçiliyse **Sil** seçeneği görüntülenmez. Gerekirse seçimi kaldırın. **CustomerV3-Account** eski bir sağlanan şablondur ve Müşteri Adayı'ndan Nakde çözümü ile çalışır. Genel olarak yayımlandığından tüm şablonlar altında gösterir.

+ **Ortam bağlantısını kaldırma**'yı tıklatın.
+ Onay için **Evet**'i tıklatın.
+ Yeni ortamı bağlamak için, [yükleme kılavuzundaki](https://aka.ms/dualwrite-docs) adımları izleyin.


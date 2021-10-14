---
title: Dataverse eşitlemeyi sıfırlama
description: Bu konuda, Microsoft Dynamics 365 Human Resources ile Microsoft Dataverse'teki İnsan sermayesi yönetimi (HCM) Ortak çözümü arasında doğru şekilde eşitlenmeyen kayıtlarda nasıl sorun giderileceği açıklanmaktadır.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d88f538fbf22313feaca6771b7cb1757a3c3fbad
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559688"
---
# <a name="reset-dataverse-synchronization"></a>Dataverse eşitlemeyi sıfırlama

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Sorun

Kayıtlar, Microsoft Dynamics 365 Human Resources ile Microsoft Dataverse'teki İnsan sermayesi yönetimi (HCM) Ortak çözümündeki varlıklar arasında eşitlenmez. Eşitleme hakkında daha fazla bilgi için [Dataverse tümleştirmesini yapılandırma](hr-admin-integration-common-data-service.md) bölümüne gidin. **Dataverse tümleştirmesini yeniden dene** veya **Dataverse tümleştirmesi, istek eşitlemesini atladı** toplu işi **Yürütülüyor** durumunda takıldığında doğru eşitlenemeyebilir.

## <a name="resolution"></a>Çözüm

**Dataverse tümleştirmesini yeniden dene** veya **Dataverse tümleştirmesi, istek eşitlemesini atladı** toplu işi **Yürütülüyor** veya **İptal ediliyor** durumunda takıldığında, durumu sıfırlayabilirsiniz. Bu, [Takılmış toplu işleri sıfırlama](hr-admin-troubleshooting-batch-execution.md) bölümündeki kılavuzu izleyerek toplu işi iptal edilerek yapılabilir. Toplu işi iptal ettikten sonra, toplu işi **Bekliyor** durumuna ayarlayarak sıfırlayabilirsiniz. Böylece toplu iş, sonraki planlanmış çalışma zamanı boyunca çalışır.

1. Henüz yapmadıysanız **Özellik yönetimi** bölümünde **Geliştirilmiş toplu iş formları** özelliğini etkinleştirin.
   1. **Özellik yönetimi** (**Sistem yönetimi** > **Özet** > **Özellik yönetimi**) sayfasına gidin.
   2. **Tümü** sekmesini seçin.
   3. **Özellik adı** sütununu seçin ve **Geliştirilmiş toplu işi durdurma** seçeneğine göre filtreleyin.
   4. Henüz etkinleştirilmemişse **Etkinleştir** eylemini seçin.

2. Dataverse tümleştirmesini kapatın.
   1. **Microsoft Dataverse tümleştirmesi** sayfasına (**Sistem yönetimi**, **Bağlantılar** > **Tümleştirmeler** > **Dataverse yapılandırması**) gidin.
   2. **Dataverse tümleştirmesini etkinleştir**'i **Hayır** olarak ayarlayın.

3. **Dataverse tümleştirmesini yeniden dene** toplu işini iptal edin.
   1. **Toplu işler** (**Sistem yönetimi** **Bağlantılar** > **Toplu işler** > **Toplu işler**) sayfasına gidin.
   2. **İş açıklaması** sütununu **Tümleştirme** seçeneğine göre filtreleyin.
   3. **Dataverse tümleştirmesini yeniden dene** toplu işini seçin.
   4. Eylem şeridinde, **Toplu İş**, **İptal etmeye zorla**'yı ve ardından onaylamak için **Evet**'i seçin.

   > [!NOTE]
   > Tümleştirmenin ilk ne zaman etkinleştirildiğine bağlı olarak, toplu işin açıklaması **Common Data Service tümleştirmesini yeniden dene** olabilir. Listeleniyorsa, **Dataverse tümleştirmesini yeniden dene** toplu işi yerine bu toplu işi seçin.

4. Tüm Dataverse tümleştirmesi toplu işlerini silin.
   1. **Toplu işler** sayfasında, **Dataverse tümleştirmesi, istek eşitlemesini atladı**, **Dataverse tümleştirmesini yeniden dene** ve **Dataverse tümleştirmesi ilk eşitleme** toplu işlerini seçin.
   2. Eylem şeridinde **Durumu değiştir** eylemini seçin. 
   3. **Durduruldu** ve **Tamam**'ı seçin.
   4. Eylem şeridinde, **Sil** eylemini seçin ve ardından eylemi onaylamak için **Evet**'i seçin.

5. Dataverse tümleştirmesi toplu işlerini açın.
   1. **Microsoft Dataverse tümleştirmesi** sayfasına gidin (**Sistem yönetimi** > **Bağlantılar** > **Tümleştirme** > **Dataverse yapılandırması**).
   2. **Dataverse tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.

6. **Toplu işler** sayfasına gidin ve **Dataverse tümleştirmesi yeniden dene** ve **Dataverse tümleştirmesi, istek eşitlemesini atladı** toplu işlerinin oluşturulduğunu onaylayın.

Toplu işler yeniden oluşturulduğunda artık işin yürütülmesinin ne kadar sürdüğünü görmek için **Dataverse tümleştirmesini yeniden dene** toplu işini izleyebilirsiniz. Daha sonra kayıtların Microsoft Dataverse'teki HCM Ortak çözümüyle düzgün şekilde eşitlendiğini doğrulayabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

[Dataverse tümleştirmesini yapılandırma](hr-admin-integration-common-data-service.md)<br>
[Takılmış toplu işleri sıfırlama](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

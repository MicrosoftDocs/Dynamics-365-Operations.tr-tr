---
title: Kalite ve uygunsuzluk yönetimini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite ve uygunsuzluk yönetimi özelliklerini ayarlama ve yapılandırma işlemine genel bakış sağlar.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956266"
---
# <a name="enable-quality-and-nonconformance-management"></a>Kalite ve uygunsuzluk yönetimini etkinleştirme

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite ve uygunsuzluk yönetimi özelliklerini ayarlama ve yapılandırma işlemine genel bakış sağlar.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Kalite ve uygunsuzluk yönetimini etkinleştirme

Sisteminizde kalite yönetimini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Stok ve ambar yönetim parametreleri**'ne gidin.
1. **Kalite yönetimi** sekmesinde, **Kalite yönetimi kullan** seçeneğini *Evet* olarak ayarlayın.
1. **Saatlik ücret** alanına saatlik işçilik ücretini yerel para birimi cinsinden girin. Saatlik ücret, uygunsuzlukla ilgili operasyonlar için maliyetlerin hesaplanmasında kullanılır. Saatlik ücret ve hesaplanan maliyetler bir uyumsuzluk için referans bilgileri sağlar. Diğer işlevlerle bir etkileşimi yoktur.
1. **Rapor kurulumu**'nu seçin.
1. Çeşitli rapor türleri için yeni satırlar ekleyin ve her raporda kullanılacak belge türünü seçin.
1. Sayfayı kapatın.
1. Sayfayı kapatın.

## <a name="quality-management-configuration-process"></a>Kalite yönetimini yapılandırma işlemi

Kalite yönetimi özelliklerini kullanmaya ve kalite emirleri oluşturmaya başlamadan önce, sistemi ve önkoşulları yapılandırmanız gerekir. Kalite yönetimini yapılandırmak için gerekli adımların listesini aşağıda bulabilirsiniz.

1. [Kalite ve uygunsuzluk yönetimini etkinleştirme](#enable-qm).
1. İsteğe bağlı: [Test araçlarını yapılandırma](quality-test-instruments.md).
1. [Testleri yapılandırma](quality-tests.md)
1. [Test değişkenlerini ve sonuçları yapılandırma](quality-test-variables.md).
1. [Test gruplarını yapılandırma](quality-test-groups.md).
1. İsteğe bağlı: [Kalite gruplarını yapılandırma ve ürünlerle ilişkilendirme](quality-groups.md).
1. İsteğe bağlı: [Kalite ilişkilendirmelerini yapılandırma](quality-associations.md).

Yapılandırma tamamlandıktan sonra, kalite emirleri oluşturmaya ve işlemeye başlayabilirsiniz. Kalite emirleriyle çalışma hakkında daha fazla bilgi için bkz. [Kalite emirleri](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Uygunsuzluk yönetimini yapılandırma işlemi

Uygunsuzluk yönetimi özelliklerini kullanmaya ve uygunsuzluklar oluşturmaya başlamadan önce, sistemi ve önkoşulları yapılandırmanız gerekir. Uygunsuzluk yönetimini yapılandırmak için gerekli adımların listesini aşağıda bulabilirsiniz.

1. [Kalite ve uygunsuzluk yönetimini etkinleştirme](#enable-qm).
1. [Uygunsuzlukları onaylamaktan sorumlu çalışanları yapılandırma](quality-responsible-workers.md).
1. [Sorunlu türlerini yapılandırma](quality-problem-types.md).
1. [Karantina bölgelerini yapılandırma](quality-quarantine-zones.md).
1. [Tanılama türlerini yapılandırma](quality-diagnostic-types.md).
1. [İşlemleri yapılandırma](quality-operations.md).
1. İsteğe bağlı: [Kalite giderlerini yapılandırma](quality-charges.md).

Yapılandırma tamamlandıktan sonra, uygunsuzluklar oluşturmaya ve işlemeye başlayabilirsiniz. Uygunsuzluk oluşturma ve bunlarla çalışma hakkında daha fazla bilgi için bkz. [Uygunsuzluklar oluşturma ve işleme](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimine genel bakış](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

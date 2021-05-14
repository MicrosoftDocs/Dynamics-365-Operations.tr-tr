---
title: Uygunsuzluklar için tanılama türleri
description: Bu konu, uygunsuzluklar ile kullanılabilecek tanılama türlerinin nasıl kullanılacağını ve oluşturulacağını açıklar.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19fcd57e28efabd6ca32c444ab961b876bde424d
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956858"
---
# <a name="diagnostic-types-for-nonconformances"></a>Uygunsuzluklar için tanılama türleri

[!include [banner](../includes/banner.md)]

Bu konu, uygunsuzluklar ile kullanılabilecek tanılama türlerinin nasıl kullanılacağını ve oluşturulacağını açıklar.

Tanılama işlemleri için bir sınıflandırma tanımlamak için **Tanılama türleri** sayfasını kullanın. Daha sonra, uygunsuzluk için bir düzeltme oluşturduğunuzda bir tanı seçersiniz. Bir düzeltme, onaylanan bir uyumsuzluk için hangi türde tanılama işleminin yürütülmesi ve bu işlemin kimin tarafından gerçekleştirilmesi gerektiğini tanımlar. Ayrıca, istenen tamamlanma tarihi ve planlanan tamamlanma tarihini belirtir.

## <a name="examples-of-diagnostic-types"></a>Tanılama türlerine örnekler

Bir üretim şirketi için çalışıyorsunuz ve birkaç maddenin kalite testi başarısız oldu. Bu maddeler, karantina alanına taşınır ve uygunsuz ürün olarak işaretlenir. Microsoft Dynamics 365 Supply Chain Management'ta sorun çözme yoluyla ayrıntıları izlemek için bir uygunsuzluk kaydı oluşturulur.

Bu durumda; kalite sorunları, maddeleri paketleyen makinedeki rulmanlar bozuk olduğundan ve aşırı ısındığından ortaya çıkmıştır. Bu sorunla ilgili düzeltme, makine parçalarını değiştirmektir.

Tanılama türlerini yapılandırdığınızda, birden fazla kayıt oluşturabilirsiniz ve bunlardan her biri makinenin sahip olabileceği farklı türde bir sorunu temsil eder. Alternatif olarak, makine onarımını temsil eden genel bir tanılama türü oluşturabilirsiniz.

## <a name="create-a-diagnostic-type"></a>Tanılama türü oluşturma

1. **Stok yönetimi \> Kurulum \> Kalite yönetimi \> Tanı türleri** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Tanılama** – Tanılama türünün benzersiz tanımlayıcı kodunu veya adını girin.
    - **Açıklama** – Tanılama türünün detaylı bir açıklamasını girin.

1. Sayfayı kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimine genel bakış](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Uygunsuzlukları onaylamaktan sorumlu çalışanlar](quality-responsible-workers.md)
- [Uygunsuzluklar için karantina bölgeleri](quality-quarantine-zones.md)
- [Uygunsuzluklar için sorun türleri](quality-problem-types.md)
- [Uygunsuzluklar için kalite masrafları](quality-charges.md)
- [Uygunsuzluklar için işlemler](quality-operations.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

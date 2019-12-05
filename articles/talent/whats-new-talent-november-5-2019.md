---
title: Dynamics 365 Talent'daki yenilikler veya değişiklikler (5 Kasım 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778394"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Dynamics 365 Talent'daki yenilikler veya değişiklikler (5 Kasım 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2598 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="copy-a-core-hr-instance"></a>Core HR kurulumunu kopyalama

Bu haftanın sürümünde, Microsoft Dynamics 365 Talent: Core HR veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz. Başka bir korumalı alan ortamınız varsa veritabanını bu ortamdan hedeflenen korumalı alan ortamına da kopyalayabilirsiniz. Daha fazla bilgi için bkz:

- Dynamics 365'te [Daha kapsamlı ortam yönetimi](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management): 2019 sürüm dalgası 2 planı

- Talent belgelerinde [Core HR kurulumunu kopyalama](hr-copy-instance.md)

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service tümleştirmesi etkinleştirildiğinde Common Data Service tümleştirmesi toplu işleri oluşturulmaz (388030)

Bu değişiklik, etkinleştirildiğinde Common Data Service tümleştirmesi için toplu işler oluşturur.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity varlığı karşıya yüklendiğinde kişi görüntüsünü yeniden boyutlandırmaz (369469)

Bu haftanın sürümünde, veri yönetimi aracılığıyla içe aktarıldığında daha iyi bir performans için görüntüleri yeniden boyutlandırma şekli değiştirilmiştir.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Konumun Atama için uygun tarihi Etkinleştirme tarihinden daha önce olabilir (340103)

Bu değişiklikle **Atama için uygun tarihi** için konumun **Etkinleştirme tarihi**'nden önceki bir tarih seçerseniz bir uyarı görüntülenir.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Adım tabanlı planlar için personel self servis bölümünde bir ücret değişikliği isteği oluşturulamıyor (376872)

Bu sürümde, adım tabanlı planlar için personel self servis bölümü aracılığıyla ücret değişiklikleri istendiğinde karşılaşılan sorun düzeltilmiştir. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Açıklama 30 karakterden uzunsa neden kodu Common Data Service ile eşitlenmiyor, Core HR 60 karaktere izin verir (352682)

Bu değişiklikle, 30 karakterden uzun neden kodları Common Data Service'te güncelleştirilir. Common Data Service'te yapılan değişiklikler Talent'e de yansıtılır.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Talent ile Finance and Operations arasında adres tümleştirmesi (351961)

Bu sürümde Talent'te güncelleştirilen adreslerin Finance and Operations'ta güncelleştirilmemesi sorunu düzeltilmiştir. Adres bloklarında yapılan değişiklikler artık güncelleştirilmiştir.

## <a name="coming-soon"></a>Çok yakında

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Dynamics 365: 2019 sürüm dalgası 2 planındaki [Performans incelemelerini yazdır](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) konusuna bakın.

### <a name="feature-management-workspace"></a>Özellik yönetimi çalışma alanı

Özellikler, her sürümüne eklenir ve güncelleştirilir. Özellik yönetimi deneyimi, her sürümde teslim edilen özelliklerin listesini görüntüleyebileceğiniz bir çalışma alanı sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz.

Özellik yönetimiyle gelen değişiklikler hakkında daha fazla bilgi edinmek için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

---
title: Uygunsuzluklar için karantina bölgeleri
description: Bu konu, uygunsuzluklar için karantina bölgelerinin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 207950a2ff4057853488f75d0e302a049d228b76
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578476"
---
# <a name="quarantine-zones-for-nonconformances"></a>Uygunsuzluklar için karantina bölgeleri

[!include [banner](../includes/banner.md)]

Bu konu, uygunsuzluklar için karantina bölgelerinin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.

Uygunsuzluklara atanabilecek bölgeleri tanımlamak için **Karantina bölgeleri** sayfasını kullanın. Uygunsuzluk oluşturduğunuz zaman, **Uygunsuzluklar** sayfasının **Genel** sekmesindeki **Karantina bölgesi** ve **Karantina türü** alanlarını ayarlayabilirsiniz. **Karantina bölgesi** alanı, genellikle maddenin bulunduğu alanı veya konumu gösterir. **Karantina türü** alanı, maddeyi *Kısıtlı kullanım* veya *Kullanılamaz* olarak tanımlar.

,Uygunsuzluk için uygunsuzluk veya düzeltme raporu yazdırdığınızda, maddenin bulunduğu karantina bölgesini görüntüleyebilirsiniz.

Uyum yapılamayan bir etiketi de yazdırabilirsiniz. Bu rapor, kusurlu malzemelerin nasıl işlenmesi gerektiği hakkında kılavuz sağlamak için, atanan karantina bölgesini ve kullanım hakkında bilgiler içerir. Karantina bölgeleri, envanter konumlarına veya operasyon kaynaklarına karşılık gelebilir.

## <a name="examples-of-quarantine-zones"></a>Karantina bölgelerine örnekler

### <a name="example-1"></a>Örnek 1

Televizyon, hoparlör ve medya oynatıcı üreten ve dağıtan bir elektronik üretim şirketinde çalışıyorsunuz. Bu durumda, her bir ürün türünü temsil edecek bir karantina bölgesi yapılandırabilirsiniz.

### <a name="example-2"></a>Örnek 2

Uygunsuz maddeleri depolamak için üç bölme ve iki raf kullanılır. Bu durumda, her bir bölme ve raf için olmak üzere beş karantina bölgesi yapılandırabilirsiniz.

## <a name="create-a-quarantine-zone"></a>Karantina bölgesi oluşturma

1. **Stok yönetimi \> Kurulum \> Kalite yönetimi \> Karantina bölgeleri** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Karantina bölgesi** – Karantina bölgesi için benzersiz bir kod veya ad girin.
    - **Açıklama** – Karantina bölgesinin detaylı bir açıklamasını girin.

1. Sayfayı kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimine genel bakış](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Uygunsuzlukları onaylamaktan sorumlu çalışanlar](quality-responsible-workers.md)
- [Uygunsuzluklar için sorun türleri](quality-quarantine-zones.md)
- [Uygunsuzluklar için tanılama türleri](quality-diagnostic-types.md)
- [Uygunsuzluklar için kalite masrafları](quality-charges.md)
- [Uygunsuzluklar için işlemler](quality-operations.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

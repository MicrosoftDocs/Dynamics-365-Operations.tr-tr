---
title: Uygunsuzluklar için işlemler
description: Bu makale, uygunsuzluklar için işlemlerin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2e63156dd2b230da7f1ea89e2c2006c1b4f3eeb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848005"
---
# <a name="operations-for-nonconformances"></a>Uygunsuzluklar için işlemler

[!include [banner](../includes/banner.md)]

Bu makale, uygunsuzluklar için işlemlerin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.

Onaylanan bir uygunsuzluk için gerçekleştirilebilecek işin sınıflandırmasını tanımlamak için **İşlemler** sayfasını kullanabilirsiniz. Bir uygunsuzluğa ilgili bir işlem atadığınızda, işlemi gerçekleştirmek için gerekli ilgili malzemeler, işçilik saatleri ve ücretler vb. gibi ayrıntılar sağlayabilirsiniz. Sistem, bu bilgileri işlem için tahmini maliyetini hesaplanmasında kullanılır. Ayrıntılı bilgiler ve tahmini maliyetler bilgi amaçlıdır. Kalite için ilgili operasyonlar, bir üretim rotası için tanımlanabilecek operasyonlardan farklıdır.

> [!NOTE]
> Uygunsuzlukla ilgili bir işlemde kullanılan maliyetleri, zamanı ve maddeleri izleyebilmenize karşın, girdiğiniz veriler yalnızca bilgilendirme amaçlıdır. Genel muhasebe, stok alt muhasebeyle veya **Zaman ve katılım** modülüyle otomatik olarak tümleştirilmez.

## <a name="examples-of-operations"></a>İşlem örnekleri

Bir üretim şirketi için çalışırsınız. Kalite testi başarısız olan maddeler için bir uygunsuzluk oluşturuldu ve onaylandı. Sorunun, bir makinedeki bozuk bir rulman ile ilişkili olduğunu göstermek için bir düzeltme oluşturuldu. Rulmanı değiştirmek için birkaç adım gereklidir ve her işlemin sorumluluğu izlenir. Örneğin, aşağıdaki adımlar gerekli olabilir:

1. Üretim hattı durdurulur ve temizleme prosedürü gerçekleştirilir.
1. Bakım personeli, rulmanı değiştirir.
1. Kalite güvence personeli, makineyi yeniden açılmadan önce denetler.

Bu örnekte, gerçekleştirilmesi gereken işi temsil etmek üzere aşağıdaki işlemler oluşturulabilir:

- Üretim hattını durdurun.
- Üretim hattını temizleyin.
- Makine bakımı gerçekleştirin.
- Makineyi inceleyin.

## <a name="create-an-operation"></a>Bir işlem oluşturma

1. **Stok yönetimi \> Kurulum \> Kalite yönetimi \> Operasyonlar** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **İşlem** – İşlem için benzersiz bir kod ya da ad girin.
    - **Açıklama**: – İşlemin detaylı bir açıklamasını girin.
    - **Tür** – İşlem yalnızca belirli bir sipariş türüyle ilişkili uygunsuzluklarla kullanılabiliyorsa, sipariş türünü (*Satınalma siparişi* veya *Satış siparişi*) seçin.

1. Sayfayı kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimine genel bakış](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Uygunsuzluk oluşturma ve işleme](tasks/create-process-non-conformance.md)
- [Uygunsuzlukları onaylamaktan sorumlu çalışanlar](quality-responsible-workers.md)
- [Uygunsuzluklar için karantina bölgeleri](quality-quarantine-zones.md)
- [Uygunsuzluklar için tanılama türleri](quality-diagnostic-types.md)
- [Uygunsuzluklar için kalite masrafları](quality-charges.md)
- [Uygunsuzluklar için sorun türleri](quality-operations.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

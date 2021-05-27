---
title: Uygunsuzluklar için sorun türleri
description: Bu konu, uygunsuzluklar için sorun türlerinin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 742edec8570610efe41a2c627efd1df586e0733e
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022168"
---
# <a name="problem-types-for-nonconformances"></a>Uygunsuzluklar için sorun türleri

[!include [banner](../includes/banner.md)]

Bu konu, uygunsuzluklar için sorun türlerinin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.

Çeşitli uygunsuzluk türleri için karşılaşabileceğiniz kalite sorunlarıyla ilgili bir sınıflandırma tanımlamak için **Sorun türleri** sayfasını kullanın. Oluşturduğunuz her sorun türü için, sorun türünün kullanılabileceği uygunsuzlukları belirlemeniz gerekir. Aşağıdaki uygunsuzluk türlerini ayarlayabilirsiniz:

- **Dahili** – Bu tip uygunsuzluklar, eldeki stokla ilgilidir (örneğin, kalite emirleri veya karantina emirleri).
- **Müşteri** – Bu tip uygunsuzluklar, satış siparişleriyle ilgilidir.
- **Satıcı** – Bu tip uygunsuzluklar, satınalma siparişleriyle ilgilidir.
- **Hizmet talebi** – Bu tip uygunsuzluklar, hizmet siparişleriyle ilgilidir.
- **Üretim** – Bu tip uygunsuzluklar, toplu siparişler veya üretim emirleriyle ilgilidir.
- **Ortak ürün üretimi** – Bu tip uygunsuzluklar, toplu siparişler veya ortak ürünlerle ilgilidir.

Yeni bir sorun türü oluşturduğunuzda, sorun türü için yetkili olan bir veya daha fazla uygunsuzluk türünün listesini oluşturmak Için, Eylem Bölmesinde **Uygunsuzluk türleri**'ni seçin. Örneğin, bir koduyla ilgili bir sorun tipi, tüm uygunsuzluk tipleri için geçerli olabilmelidir. Ancak, müşteri şikayetleriyle ilgili bir sorun türü yalnızca **Müşteri** ve **Hizmet talebi** uygunsuzluk türlerine uygulanabilir.

## <a name="examples-of-problem-types"></a>Sorun türlerine örnekler

Aşağıda, farklı uygunsuzluk tipleri ile kullanılabilecek sorun türleri için bazı senaryo örnekleri verilmiştir:

- **Müşteri:** Bir müşteri şikayette bulundu, müşteri bir iade yaptı veya kalite gereksinimleri karşılanmadı.
- **Satıcı:** Ürün zarar görmüş, kalite gereksinimleri karşılanmamış veya yanlış ürün alınmış.
- **Hizmet talebi:** Kalite gereksinimleri karşılanmadı, müşteri bir şikayette bulundu veya makineye bakım yapılması gerekti.
- **Üretim:** Kalite gereksinimleri karşılanmadı, makineye bakım yapılması gerekti veya ürün hasarlıydı.
- **Ortak ürün üretimi:** Kalite gereksinimleri karşılanmadı, makineye bakım yapılması gerekti veya ürün hasarlıydı.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Sorun türü oluşturma ve bunu uygunsuzluk türlerine atama

1. **Stok yönetimi \> Kurulum \> Kalite yönetimi \> Problem türleri** öğesine gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Sorun türü** – Sorun türünün benzersiz tanımlayıcı kodunu veya adını girin.
    - **Açıklama** – Sorun türünün detaylı bir açıklamasını girin.

1. Yeni satır seçiliyken, Eylem Bölmesinde **Uygunsuzluk türleri**'ni seçin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Daha sonra yeni satır için, **Uygunsuzluk türü** alanını, sorunlu tür için izin vermek istediğiniz uygunsuzluk türüne ayarlayın.
1. Sorun türü için yetkilendirmek istediğiniz her ek uygunsuzluk türü için önceki adımı yineleyin.
1. Sayfaları kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimine genel bakış](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Uygunsuzlukları onaylamaktan sorumlu çalışanlar](quality-responsible-workers.md)
- [Uygunsuzluklar için karantina bölgeleri](quality-quarantine-zones.md)
- [Uygunsuzluklar için tanılama türleri](quality-diagnostic-types.md)
- [Uygunsuzluklar için kalite masrafları](quality-charges.md)
- [Uygunsuzluklar için işlemler](quality-operations.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

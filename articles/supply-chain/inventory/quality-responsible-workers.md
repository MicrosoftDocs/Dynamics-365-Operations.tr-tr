---
title: Uygunsuzlukları onaylamaktan sorumlu çalışanlar
description: Bu konuda, uygunsuzlukları onaylamaktan sorumlu çalışanları yapılandırma yöntemi açıklanmıştır.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021792"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Uygunsuzlukları onaylamaktan sorumlu çalışanlar

[!include [banner](../includes/banner.md)]

Bu konuda, uygunsuzlukları onaylamaktan sorumlu çalışanları yapılandırma yöntemi açıklanmıştır.

Kullanıcılar düzeltme veya işlemler gibi ayrıntıları girmeye başlamadan önce uygunsuzluklar onaylanmalıdır. Kullanıcılar uygunsuzlukları onaylayabilmeden veya reddetmeden önce, kullanıcı kimliklerinin (kullanıcı kaydı) bir çalışan kaydıyla bağlantılı olması gerekir. İsteğe bağlı olarak, kaliteden sorumlu çalışanları yapılandırabilir ve bir çalışanın başka bir çalışanın adına işi onaylamasına izin verebilirsiniz.

## <a name="enable-a-user-for-nonconformance-processing"></a>Bir kullanıcıyı uygunsuzluk işleme için etkinleştirme

Bir kullanıcı uygunsuzlukları onaylayabilmeden veya reddetmeden önce, kullanıcı kimliklerini (kullanıcı kaydı) bir çalışan kaydıyla bağlamanız gerekir. Böylece, onay alanları otomatik olarak ayarlanabilir ve geçerli kullanıcı, zaman çizelgesi için otomatik olarak doldurulabilir. Kullanıcı belge notlarını kullanabilmeden önce kullanıcı seçeneklerinde belge işleme seçeneğini etkinleştirmeniz gerekir.

1. **Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.
1. Uygunsuzlukları onaylayabilmek veya reddetme iznine sahip olacak kullanıcıyı bulun ve açın.
1. **Kişi** alanını, geçerli kullanıcı kaydıyla ilişkili çalışanın adı olarak ayarlayın.
1. Eylem Bölmesinde, **Kullanıcı seçenekleri**'ni seçin.
1. Geçerli kullanıcı kaydının **Seçenekler** sayfasında **Tercihler** sekmesinde, **Belge işlemeyi etkinleştir** seçeneğini *Evet* olarak ayarlayın.
1. Sayfaları kapatın.

## <a name="define-workers-that-are-responsible-for-quality"></a>Kaliteden sorumlu çalışanları tanımlama

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Kaliteden sorumlu çalışanlar**'a gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Çalışan** alanında, kalite verilerini giren çalışanı seçin.
4. **Sorumlu çalışan** alanında, seçili çalışanın adına işleri girdiği çalışanı seçin. Uygunsuzluklar oluşturulup güncelleştirilirken bu çalışan, **Çalışan** alanlarına varsayılan olarak girilir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimine genel bakış](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Kalite giderleri](quality-charges.md)
- [Uygunsuzluklar için karantina bölgeleri](quality-quarantine-zones.md)
- [Uygunsuzluklar için tanılama türleri](quality-diagnostic-types.md)
- [Uygunsuzluklar için kalite masrafları](quality-charges.md)
- [Uygunsuzluklar için işlemler](quality-operations.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

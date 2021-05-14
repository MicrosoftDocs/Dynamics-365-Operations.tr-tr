---
title: Uygunsuzlukları onaylamaktan sorumlu çalışanlar
description: Bu konuda, uygunsuzlukları onaylamaktan sorumlu çalışanları yapılandırma yöntemi açıklanmıştır.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956867"
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

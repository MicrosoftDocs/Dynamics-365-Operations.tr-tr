---
title: Planlı yürütme
description: Bu makalede Varlık Yönetimi'nde zamanlanmış yürütmeyi açıklanmaktadır.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e9d6af5c224f683481378da57708fda3c1b7207
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848063"
---
# <a name="scheduled-execution"></a>Planlı yürütme

[!include [banner](../../includes/banner.md)]

 

Zamanlanmış yürütmeyi ayarlamak için iş emri servis düzeylerini kullanabilirsiniz. (İş emri hizmet düzeyleri hakkında daha fazla bilgi için bkz [Hizmet düzeyi ve açıklaması](service-level-and-description.md).) İş emrinin tamamlanması gereken aralık için daha ayrıntılı veya daha az ayrıntılı gereksinimleri ayarlayabileceğiniz için, zamanlanan yürütme, bakım görevlileri için iş planlamasında esneklik sağlar. Örneğin, bir üretim aracında beklenenden daha hızlı bir iş tamamlayan bir bakım görevlisi, geçerli hafta için planlanan, ancak geçerli gün için gerekli olan başka bir yakındaki işe geçebilir. Bu yaklaşım, çalışan planlama ve iş tamamlama işleminin en iyi duruma getirilmesini sağlar.

İş emirleriyle ilgili olan zamanlanmış yürütme kurulumu genel veya özel olabilir. Belirli iş emri türleri, kıymet türleri, vb. ile sınırlı olmayan genel satırları ayarlayabilirsiniz. Alternatif olarak, belirli bir iş emri türü, kıymet türü, bakım iş türü vb. için geçerli olan planlı yürütme satırları oluşturabilirsiniz.

1. **Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Planlanmış yürütme**'yi seçin.
2. Planlanmış yürütme satırı oluşturmak için **Yeni**'yi seçin.
3. **İşlem yapılacak yerleşim**, **İş emri türü**, **Kıymet türü**, **Üretici**, **Model**, **Bakım iş türü kategorisi**, **Bakım iş türü**, **Bakım iş türü varyantı** ve **Ticari** alanlarında, gereksinim duyduğunuz şekilde değerleri seçin.
4. **Servis düzeyi** alanında, bir iş emri servis düzeyi seçin. Bu alanı boş bırakırsanız, en genel zamanlanmış yürütme satırı türünü yaparsınız. Genel bir satır örneği için, aşağıdaki çizimdeki ilk kayda bakın. Bu satır, iş emri servisi düzeyi olmayan tüm iş emirlerinin belirli bir tarih ve saat için zamanlanmasına olanak tanır.
5. **Zamanlanmış yürütme** alanında zaman aralığını seçin.
6. **Kaydet**'i seçin.

![Planlı yürütme.](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
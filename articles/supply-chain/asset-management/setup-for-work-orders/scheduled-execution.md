---
title: Planlı yürütme
description: Bu konuda Varlık Yönetimi'nde zamanlanmış yürütmeyi açıklanmaktadır.
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
ms.openlocfilehash: fae899bcfa8bb2566d1a9aee3f0dbe22bc219edf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825650"
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

![Planlı yürütme](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
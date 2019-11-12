---
title: Planlı yürütme
description: Bu konuda Varlık Yönetimi'nde zamanlanmış yürütmeyi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89e13179e17b7cf075d631bc65d82da5f24da624
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569858"
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

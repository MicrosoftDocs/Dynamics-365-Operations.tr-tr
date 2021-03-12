---
title: Günlük başına defter sayısı
description: Bu konu, bir toplu iş aracılığıyla sabit varlık alımı veya amortisman teklifi oluşturduğunuzda günlükler ve varlık defterleri arasındaki ilişkiyi açıklar. Her bir alım ve amortisman için dahil edilen maksimum defter sayısını tanımlayabilirsiniz.
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cfb9a9e1456a7d9067e3c4369a7eb7150326655d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988964"
---
# <a name="number-of-books-per-journal"></a>Günlük başına defter sayısı

[!include [banner](../includes/banner.md)]

Bu konu, bir toplu iş aracılığıyla sabit varlık alımı veya amortisman teklifi oluşturduğunuzda günlükler ve varlık defterleri arasındaki ilişkiyi açıklar. Her bir alım ve amortisman için dahil edilen maksimum kitap sayısını **Sabit varlıklar parametreleri** sayfasındaki (**Sabit varlıklar \> Kurulum \> Sabit varlıklar parametreleri**) **Genel** sekmesinde yer alan **Günlük başına defter sayısı**'ndaki alanları kullanaraktanımlayabilirsiniz. Bu alanlar, her bir alım günlüğü ve amortisman günlüğü başına varlık defteri sayısını dağıtmanıza olanak sağlar.

Bir alım teklifi için varsayılan değer en az 10.000 defterdir. Bir amortisman teklifi için varsayılan değer en az 2.000 defterdir.

Örneğin, 4.000 sabit varlık varsa ve her bir varlık ile iki defter ilişkilendirilmişse, geçerli katmana bir defter nakledilir ve diğer defter vergi katmanına nakledilir. Toplu iş yoluyla 4.000 sabit varlık alımı yapıyorsanız tek bir sabit varlık alım günlüğü oluşturan toplu iş 4.000 varlık defteri içerecektir.

> [!NOTE]
> Oluşturulan günlük, toplu iş tamamlanana kadar kullanılmaya devam eder.
>
> Türetilmiş defterler günlük başına maksimum defter sayısına dahil edilmez.

Toplu işi, aynı alınan varlık kümesiyle ilgili amortismanı çalıştırmak için kullanabilirsiniz. Örneğin, bir toplu iş, her biri 2.000 varlık defterinden oluşan iki amortisman günlüğü oluşturuyor. İlk günlükte 1 ile 2.000 arasında numaralandırılmış sabit varlıklarla ilişkili defterler yer alır. İkinci günlükte 2.001 ile 4.000 arasında numaralandırılmış sabit varlıklarla ilişkili defterler yer alır.

Toplu işi kapalı defterleri dışarıda tutar. Örneğin, amortisman için bir toplu işte, ilk 2.000 defterin 10'unun kapalı olduğunu düşünelim. Bu durumda, ilk günlükte 1 ile 2.011 arasında numaralandırılmış sabit varlıklarla ilişkili defterler yer alır. İkinci günlükte 2.012 ile 4.000 arasında numaralandırılmış sabit varlıklarla ilişkili defterler yer alır.

Aynı günlükte yinelenen öğe kimlikleri yoksa defter sayısı sınırı uygulanır. Ancak, varlık kodu defter koduyla aynıysa, varlık kimliğini aynı günlükte tutmak için günlük başına defter sayısı aşılabilir.

Örneğin 5.001 sabit varlık var, her bir sabit varlık kimliğiyle üç defter ilişkilendirilmiş ve her varlık defteri aynı deftere nakil katmanına nakledilmiş. Özetleme yapmadan art arda üç ay boyunca amortisman uyguluyorsunuz.  Amortisman günlüğü toplu iş aracılığıyla oluşturulur ve sistem, 667 sabit varlık kimliği bulunan yedi günlük ve her bir sabit varlık kimliği için üç defter oluşturur. Sonuç, 2.001 defter olacaktır. Bu nedenle, aynı varlık kimliğini aynı günlükte tutmak için üç ay içinde 6.003 günlük satırı olacaktır. Ayrıca sistem, 332 sabit varlık kimliği bulunan bir günlük ve her sabit varlık kimliği için üç defter oluşturacaktır. Üç ayda, 2.988 satır olacaktır.

> [!Note] 
> Bir amortisman teklifi oluştururken **Özet amortisman** parametresi açıksa, **Günlük başına defter sayısı-amortisman teklifi** alanındaki değerin hiçbir etkisi olmaz. Bu durumda günlük başına düşen defter sayısı, dahili sınır olarak tanımlanan 6000'dir.

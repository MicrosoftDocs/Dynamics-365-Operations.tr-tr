---
title: Bireysel olarak numara serileri ayarlama
description: Bu konuda bireysel olarak numara serileri ayarlama işlemi açıklanmaktadır.
author: sericks007
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58e69b680c006c814e9408135b6947161ad7c4f3
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738893"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Bireysel olarak numara serileri ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konuda bireysel olarak numara serileri ayarlama işlemi açıklanmaktadır. Numara serileri, ana veri kayıtları ve bunları gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılarını oluşturmada kullanılır. Tanımlayıcı gerektiren bir ana veri veya hareket kaydı, referans olarak adlandırılır. Bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz. Tüm gerekli numara serilerini aynı zamanda, **Numara serileri ayarla** sihirbazını kullanarak ayarlayabilir veya **Numara serileri** sayfasından tek tek numara serilerini oluşturabilir ya da değiştirebilirsiniz.

1. **Gezinti bölmesi > Modüller > Kuruluş yönetimi > Numara serileri > Numara serileri**'ne gidin.
2. **Numara serisi**'ni seçin.
3. **Numara serisi kodu** alanına bir değer yazın.
4. **Ad** alanına bir değer yazın.
5. **Kapsam parametreleri** hızlı sekmesinde, numara serisi için bir kapsam seçin ve açılır listeden kapsam değerlerini belirleyin. Kapsam, hangi kuruluşların numara serisini kullandığını tanımlar. Ayrıca, **Paylaşılan** dışındaki bir kapsama sahip numara serileri, kendi kapsamlarına karşılık gelen segmentler içerebilir. Örneğin, **Tüzel kişilik** kapsamını içeren bir numara serisi, bir tüzel kişilik segmentine sahip olabilir. Kapsamlar hakkında daha fazla bilgi için bkz. [Numara serilerine genel bakış](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/fin-and-ops/organization-administration/number-sequence-overview.md).  
6. **Segmentler** bölümünü genişletin.
    - Segment ekleyerek, çıkararak veya yeniden düzenleyerek numara serisi için biçimi tanımlayın.  
    - Tüm kapsamlardan numara serileri *Sabit parçalar* ve *Alfasayısal parçalar* içerebilir. Sabit parçalar, değişmeyen bir dizi alfasayısal karakter içerirler. Bu segment türünü, numara serisi segmentleri arasına tire veya başka ayırıcılar eklemek için kullanın. Alfasayısal segmentler, numara işaretleri (#) ve ampersanların (&) bir kombinasyonunu içerirler. Bu karakterler, numara serisinden her bir numara kullanıldığında artan harfler ve numaraları temsil eder. Artan sayıları göstermek için numara işaretini (#) ve artan harfleri göstermek için bir ampersanı (&) kullanın. Örneğin `#####_2014` biçimi `00001_2014`, `00002_2014` serisini ve devamını oluşturur. En az bir alfasayısal segment bulunması gerekir. Şirket veya tüzel kişilik gibi kapsam segmentleri zorunlu değildir. Ancak, biçim içerisinde kapsam segmentleri eklemezseniz, seçili referans için numaralar yine de kapsama göre oluşturulacaktır.  
7. **Referanslar** bölümünü genişletin. Bu numara serisinin atanacağı belge türü veya kaydı seçin. Bu adım özel uygulama kullanım modelleri için tanımlanmış sıralamalar için isteğe bağlıdır. Bu senaryolarda, bir numara serisi kodu ya da kimliği kullanarak, bir referans olmadan yeni bir numara oluşturulur. Özel uygulama kullanım modeline bir örnek, belirli günlük isimleri için kullanılan fiş serileridir. Ancak, bu tür modeller kullanmanızı önermeyiz.  
8. **Genel** bölümünü genişletin. Genel hızlı sekmesinde, numara serisinin el ile ve sürekli veya süreksiz olup olmadığını belirtin. Ek olarak, numara serisinde kullanılabilecek en düşük ve en yüksek numaraları girin. Sürekli olmayan bir numara sırasını, sürekli bir numara sırasına değiştirmenizi önermeyiz. Numara serisi gerçekten sürekli olmayacaktır. Ayrıca, bu değişiklik veritabanında yinelenen anahtar hatalarına neden olabilir. Ayrıca, sürekli numara serilerinin performans üzerindeki etkisi daha büyüktür.   
9. **Kaydet**'e tıklayın.


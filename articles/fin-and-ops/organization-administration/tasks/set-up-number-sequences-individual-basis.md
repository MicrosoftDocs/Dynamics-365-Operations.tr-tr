---
title: Bireysel olarak numara serileri ayarlama
description: Numara serileri, ana veri kayıtları ve bunları gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılarını oluşturmada kullanılır.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 6734d66a06f8a8dc90a48bd68b7b4e22177b4672
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560602"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Bireysel olarak numara serileri ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Numara serileri, ana veri kayıtları ve bunları gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılarını oluşturmada kullanılır. Tanımlayıcı gerektiren bir ana veri veya hareket kaydı, referans olarak adlandırılır. Bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz. Tüm gerekli numara serilerini aynı zamanda, Numara serileri ayarla sihirbazını kullanarak ayarlayabilir veya Numara serileri sayfasından tek tek numara serilerini oluşturabilir, değiştirebilirsiniz.

1. (Kuruluş yönetim > Numara serileri > Numara serileri'ne tıklayın.
2. Numara serisine tıklayın.
3. Numara serisi kodu alanında, bir değer girin.
4. İsim alanına bir değer yazın.
5. Kapsam parametreleri bölümünü genişletin.
    * Kapsam parametreleri hızlı sekmesinde, numara serisi için bir kapsam seçin ve kapsam değerlerini seçin.     Kapsam, hangi kuruluşların numara serisini kullandığını tanımlar. Ek olarak, Paylaşımlı dışındaki bir kapsama sahip numara serileri, kendi kapsamlarına karşılık gelen segmentler içerebilir. Örneğin, Tüzel kişilik kapsamını içeren bir numara serisi, bir tüzel kişilik segmentine sahip olabilir. Kapsamlar hakkında daha fazla bilgi için "Numara serileri genel bakış" yardım başlığına göz atın.  
6. Segmentler bölümünü genişletin.
    * Segmentler Hızlı Sekmesinde, segment ekleyerek, çıkararak veya yeniden düzenleyerek numara serisi için biçimi tanımlayın.  
    * Tüm kapsamlardan numara serileri Sabit parçalar ve Alfasayısal parçalar içerebilir. Sabit parçalar, değişmeyen bir dizi alfasayısal karakter içerirler. Bu segment türünü, numara serisi segmentleri arasına tire veya başka ayırıcılar eklemek için kullanın. Alfasayısal segmentler, numara işaretleri (#) ve ampersanların (&) bir kombinasyonunu içerirler. Bu karakterler, numara serisinden her bir numara kullanıldığında artan harfler ve numaraları temsil eder. Artan sayıları göstermek için numara işaretini (#) ve artan harfleri göstermek için bir ampersanı (&) kullanın. Örneğin, #####_2014 biçimi, sıra 00001_2014, 00002_2014 ve devamını oluşturur.     En az bir alfasayısal segment bulunması gerekir. Şirket veya tüzel kişilik gibi kapsam segmentleri zorunlu değildir. Ancak, biçim içerisinde kapsam segmentleri eklemezseniz, seçili referans için numaralar yine de kapsama göre oluşturulacaktır.  
7. Referanslar bölümünü genişletin.
    * Referanslar hızlı sekmesinde, bu numara serisinin atanacağı belge türü veya kaydı seçin.     Bu adım özel uygulama kullanım modelleri için tanımlanmış sıralamalar için isteğe bağlıdır. Bu senaryolarda, bir numara serisi kodu ya da kimliği kullanarak, bir referans olmadan yeni bir numara oluşturulur. Özel uygulama kullanım modeline bir örnek, belirli günlük isimleri için kullanılan fiş serileridir. Ancak, bu tür modeller kullanmanızı önermeyiz.  
8. Genel bölümünü genişletin.
    * Genel hızlı sekmesinde, numara serisinin el ile ve sürekli veya süreksiz olup olmadığını belirtin. Ek olarak, numara serisinde kullanılabilecek en düşük ve en yüksek numaraları girin.     Sürekli olmayan bir numara sırasını, sürekli bir numara sırasına değiştirmenizi önermeyiz. Numara serisi gerçekten sürekli olmayacaktır. Ayrıca, bu değişiklik veritabanında yinelenen anahtar hatalarına neden olabilir. Ayrıca, sürekli numara serilerinin performans üzerindeki etkisi daha büyüktür.   
9. Kaydet'e tıklayın.


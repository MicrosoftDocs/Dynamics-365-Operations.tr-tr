--- 
title: "Konteyner kullanımını ayarlama"
description: "Bu yordam, Ambar yönetimindeki yüklerin konteyner kullanımının nasıl otomatikleştirileceğini açıklar."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-containerization"></a>Konteyner kullanımını ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, Ambar yönetimindeki yüklerin konteyner kullanımının nasıl otomatikleştirileceğini açıklar. Otomatik konteyner kullanımı, bir dalga işlendiğinde sevkiyatlar için konteynerleri ve çekme işini oluşturur ve iş satırları, konteynerlere sığacak miktarlara bölünür. Bu, ambar çalışanlarına, maddeleri doğrudan seçilen konteynere çekmelerine yardımcı olur. El ile yapılan paketleme işlemi ile karşılaştırıldığında, örneğin konteynerler oluşturma, maddeler atama ve konteyner kapanışı gibi işlemler, sistem tarafından otomatikleştirilir. Bu yordam, USMF demo şirketin kullanır ve Ambar Yöneticisi tarafından gerçekleştirilir.


## <a name="set-up-a-wave-template"></a>Dalga şablonu ayarlama
1. Ambar yönetimi > Kurulum > Dalgalar > Dalga şablonları öğesine gidin.
2. Yeni'ye tıklayın.
3. Dalga şablonu adı alanına bir değer girin.
4. Dalga şablonu açıklaması alanında bir değer girin.
5. Tesis alanına bir değer girin veya buradan bir değer seçin.
6. Ambar alanında bir değer girin veya bir değer seçin.
7. Yöntemler bölümünü genişletin.
    * Seçili yöntemler bölmesi, seçili dalga şablon türü için yöntemleri listeler. Dalga şablonu, konteynerli yöntemi içermelidir.  
8. Listede, istenen kaydı bulun ve seçin.
9. Dalga adımı kodu alanına bir değer girin.
    * Eklenen yöntem için herhangi bir kod olabilecek Dalga adım kodu girin. Yöntemi birden çok kez eklemek ve farklı dalga adım kodları atamak da mümkündür. Bunu yapmak için bu yöntemin dalga işlem yöntemleri sayfasında Tekrar edilebilir'i seçin.  
10. Kaydet'e tıklayın.
11. Sayfayı kapatın.

## <a name="set-up-a-container-type"></a>Konteyner türü ayarlama
1. Ambar yönetimi > Kurulum > Konteynerler > Konteyner türleri öğesine gidin.
    * Konteyner türleri sayfasında, konteynerlerinizi tanımlayabilirsiniz. Konteynerlerin fiziksel boyutlarını, dara ağırlığı, maksimum ağırlık, maksimum hacim, uzunluk, genişlik ve yükseklik dahil olmak üzere yapılandırabilirsiniz. Bu örnekte, üç farklı boyutta kutulara sahibiz.  
2. Yeni'ye tıklayın.
3. Konteyner türü alanına bir değer girin.
4. Dara alanına bir sayı girin.
5. Maksimum ağırlık alanında bir sayı girin.
6. Hacim alanına bir sayı girin.
7. Uzunluk alanına bir sayı girin.
8. Genişlik alanına bir sayı girin.
9. Yükseklik alanına bir sayı girin.
10. Açıklama alanına bir değer girin.
11. Kaydet'e tıklayın.
12. Yeni'ye tıklayın.
13. Konteyner türü alanına bir değer girin.
14. Açıklama alanına bir değer girin.
15. Dara alanına bir sayı girin.
16. Maksimum ağırlık alanında bir sayı girin.
17. Hacim alanına bir sayı girin.
18. Uzunluk alanına bir sayı girin.
19. Genişlik alanına bir sayı girin.
20. Yükseklik alanına bir sayı girin.
21. Kaydet'e tıklayın.
22. Yeni'ye tıklayın.
23. Konteyner türü alanına bir değer girin.
24. Açıklama alanına bir değer girin.
25. Dara alanına bir sayı girin.
26. Maksimum ağırlık alanında bir sayı girin.
27. Hacim alanına bir sayı girin.
28. Uzunluk alanına bir sayı girin.
29. Genişlik alanına bir sayı girin.
30. Yükseklik alanına bir sayı girin.
31. Kaydet'e tıklayın.
32. Sayfayı kapatın.

## <a name="set-up-a-container-group"></a>Bir konteyner grubu ayarla
1. Ambar yönetimi > Kurulum > Konteynerler > Konteyner grupları öğesine gidin.
2. Yeni'ye tıklayın.
    * Konteyner türleri için mantıksal grupları ayarlayabilirsiniz. Her bir grup için, konteynerlerin paketleneceği sıralamayı ve konteynerlerin doldurulacağı yüzdeyi belirtebilirsiniz. Maddenin ebat boyutları, bir konteynere sığı sığmayacağını belirlemekte kullanılır. Maddenin ebat boyutuna en yakın olan konteyner kullanılacaktır. Bir grup içinde birden çok konteyner türü varsa, sırayı boyuta göre düzenlemenizi öneririz, böylelikle en büyük konteyner birinci, sıralama içerisinde birinci numarada olur ve en küçük konteyner en sona kalır.    
3. Konteyner grubu numarası alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Yeni'yi tıklatın.
6. Listede, seçili satırı işaretleyin.
7. Konteyner türü alanında bir değer girin veya seçin.
8. Yeni'yi tıklatın.
9. Listede, seçili satırı işaretleyin.
10. Konteyner türü alanında bir değer girin veya seçin.
11. Yeni'yi tıklatın.
12. Listede, seçili satırı işaretleyin.
13. Konteyner türü alanında bir değer girin veya seçin.
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.

## <a name="set-up-a-container-build-template"></a>Bir konteyner yapılandırma şablonu
1. Ambar yönetimi > Kurulum > Konteynerler > Konteyner yapı şablonu öğesine gidin.
2. Yeni'ye tıklayın.
    * Konteyner yapılandırma şablonu, hangi konteyner kullanım işleminin gerçekleştirildiğine dayalıdır. Her bir konteyner yapılandırma şablonu, bir dalga şablonu tarafından kullanılacak bir konteyner kullanım işlemini tanımlar. Sorguyu düzenle seçeneği, seçili şablonun işleneceği koşulları tanımlamanızı sağlar. Örneğin, yalnızca belirli müşteriler, ürünler veya ambarlar için konteyner kullanmayı çalıştırmak isteyebilirsiniz veya karşılık gelen sorgu aralıklarını şablona ekleyebilirsiniz. Dalga adım kodu alanı, konteyner yapılandırma şablonunun dalga şablonundaki adımlara nasıl bağlandığını gösteren alandır. Bir dalga yürütüldüğünde hangi kapsayıcı yapı şablonunun konteyner kullanımını başlatmak için kullanılacağını belirler. Taban sorgu türü alanı, neyin paketleneceğini ve filtre sorgusunun neye dayandırılacağını belirler.  
3. Listede, seçili satırı işaretleyin.
4. Konteyner şablonu kimliği alanında bir değer girin.
5. Konteyner grup kimliği alanında bir değer girin veya bir değer seçin.
6. Dalga adımı kodu alanına bir değer girin.
7. Bölünmüş çekmelere izin ver onay kutusunu işaretleyin.
8. Kaydet'e tıklayın.
9. Konteyner karıştırma sınırlamalarına tıklayın.
    * Mantık bölümlerini karıştırmak, konteynerler içindeki paketleme tahsisat satırları için kurallar eklemenize olanak sağlar. Örneğin, maddeler konteynerlere atandığında Madde numarası alanını eklerseniz, yeni bir madde numarası olduğunda, yeni bir konteyner oluşturulur. Bu, çalışanların aynı konteyner içerisindeki iki farklı müşteri için tahsisat satırlarını paketlemelerinin önüne geçer.  
10. Yeni'ye tıklayın.
11. Tablo alanında, bir seçenek seçin.
12. Alan Seç alanına bir değer girin veya buradan bir değer seçin.
13. Tamam'a tıklayın.



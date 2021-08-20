---
title: Stok sayımı işlemlerini tanımlama
description: Bu konu, size, bir sayım grubu ve bir sayım günlüğü oluşturarak, temel stok sayım işlemlerini yapılandırmayı açıklar.
author: MarkusFogelberg
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 535fa6cfcf1f966b02ee7b391bb41dcbc2c2ac1fc85bcd09e3811fc027621cc4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755407"
---
# <a name="define-inventory-counting-processes"></a>Stok sayımı işlemlerini tanımlama

[!include [banner](../../includes/banner.md)]

Bu konu, size, bir sayım grubu ve bir sayım günlüğü oluşturarak, temel stok sayım işlemlerini yapılandırmayı açıklar. Ayrıca, ambar ve madde düzeyinde sayım ilkelerinin nasıl etkinleştirileceğini de göreceksiniz. Bu görevler genellikle bir ambar gözetmeni tarafından yerine getirilir. Biraz serbest bırakılmış ürün ve ambar bulundurmak önkoşuldur. Demo veri şirketi kullanıyorsanız, bu prosedürü USMF şirketinde herhangi bir stoklu maddeyle çalıştırabilirsiniz.


## <a name="create-a-counting-group"></a>Sayım grubu oluşturun
1. Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok > Sayım grupları**'a gidin.
2. **Yeni**'yi seçin.
3. Yeni satırdaki **Sayım grubu** alanına bir değer girin.
4. **Ad** alanına bir değer yazın.
5. **Sayım kodu** alanında bir seçenek belirtin.

    - **El ile** – İşi her çalıştırmanızda satırları dahil eder. Diğer bir deyişle, sayım grubu için sayım aralığına karar vermiş olursunuz.  
    - **Dönem** – Dönem aralığı sona erdiğinde, sayım günlüğündeki dönem için satırları dahil eder.  
    - **Stok sıfır** – Eldeki stok sıfıra (0) inerse, bu iş çalıştırıldığında sayım günlüğünde satırlar oluşturulur. Eldeki stok bir sayımın ardından 0'a inerse, satırlar sayımı bir sonraki çalıştırmanızda oluşturulacaktır.  
    - **Minimum** – Eldeki stok belirtilen minimuma eşitse veya bundan küçükse, sayım günlüğüne satırlar ekler.  
    - İsteğe bağlı: **Sayım Kodu** alanında **Dönem**'i belirttiyseniz, **Sayım dönemi** alanında dönemin aralığını yazmanız gerekir. Aralıklar için birim gündür.  
    - Sayım günlüğünde yeni satırları oluşturma işini çalıştırdığınız zaman bu aralıkta belirtilen aralıklarla yeni satırlar oluşturulur (aynı işi ne sıklıkta çalıştırdığınız önemli değildir). Örneğin, **Sayım dönemi** 7'ye ayarlandıysa ve son olarak 1 Ocak tarihindeki bir sayım için günlük satırları oluşturulduysa, 5 Ocak'ta başka bir iş başlatıldığı zaman yedi gün geçmediği için o dönem aralığına ait günlükte satır oluşturulmaz. İşi 8 Ocak'ta yine başlatırsanız, 7 gün geçmiş olduğu için sayım günlüğünde o dönem için satırlar oluşturulur.  

6. **Kaydet**'i seçin.

## <a name="create-a-counting-journal-name"></a>Sayım günlüğü adı oluşturun
1. Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Günlük adları > Stok**'a gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
5. **Günlük türü** alanında **Sayım**'ı seçin. İsteğe bağlı: Sayım günlükleri oluşturma sırasında oluşturulan fiş kodları için belirli bir numara sırası istiyorsanız farklı bir fiş serisi kodu seçebilirsiniz. Fiş serileri **Numara sıraları** sayfasında oluşturulur.  
6. **Ayrıntı düzeyi** alanında bir seçenek belirtin.  

    - Günlük deftere nakledilirken uygulanan ayrıntı düzeyi.  
    - İsteğe bağlı: Rezervasyon alanındaki değeri değiştirebilirsiniz. Bu, sayım sırasında madde rezerve etmek için kullanılan yöntemdir.   
    - **El ile** – Rezervasyon formunda maddeler el ile rezerve edilir.  
    - **Otomatik** – Sipariş miktarı, maddenin eldeki kullanılabilir stoğundan rezerve edilir.   
    - **Açılım** – Rezervasyon, hareket master planlamasının bir parçasıdır.  

7. **Kaydet**'i seçin.

## <a name="set-standard-counting-journal-name"></a>Standart sayım günlüğü adı ayarlayın
1. Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok ve ambar yönetim parametreleri**'ne gidin.
2. **Günlükler** sekmesini seçin.
3. **Sayım** alanının açılır menüsünde, önceden oluşturduğunuz günlüğü seçin. Bu günlük, daha sonra, **Sayım** türündeki stok günlükleri için varsayılan bir günlük adı olur.  
4. **Genel** sekmesini seçin. İsteğe bağlı: Sevk irsaliyeleri, malzeme çekme listeleri veya malzeme çekme listesi kayıtları gibi güncelleştirmeleri önlemek için sayım işlemi sırasında maddeyi kilitlemek üzere bu seçeneği belirtin.  

## <a name="set-the-counting-policy-for-an-item"></a>Bir maddenin sayım ilkesini ayarlayın
1. Gezinti panosunda **Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.
2. Listede, sayım ilkelerini ayarlamak istediğiniz ürünün madde numarasına ait bağlantıyı seçin. Stoğu izlenen bir madde seçmeniz gerektir. Stoğu olmayan bir ürün sayılamaz. USMF demo verilerini kullanıyorsanız, madde olarak A0001'i seçebilirsiniz.  
3. **Düzenle** öğesini seçin.
4. **Stok yönetimi** bölümünün genişletilmiş görünümüne geçin.
5. **Sayım grubu** alanının açılır menüsünde, önceden oluşturduğunuz sayım grubunu seçin. Bu ürün, artık bu sayım grubu kullanılarak stok sayım günlüğü satırları oluşturulurken dahil edilir.  
6. **Kaydet**'i seçin.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Belirli bir ambardaki bir maddenin sayım ilkesini ayarlayın
1. Eylem Bölmesinde, **Stok yönetimi**'ni seçin.
2. **Ambar maddeleri**'ni seçin.
3. **Yeni**'yi seçin.
4. **Ambar** alanının açılan menüsünde, belirli sayım ilkelerini ayarlamak istediğiniz ambarı seçin.
5. **Sayım grubu** alanının açılan menüsünde bir sayım grubu seçin. Seçtiğiniz belirli bir ambardaki maddeye uygulanması gereken belirli bir sayım grubunu seçebilirsiniz. O ambarda sayım işlemi yapılırken, bu sayım ilkesi, maddeye ilişkin genel sayım ilkesinin yerine geçer.  
6. **Kaydet**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
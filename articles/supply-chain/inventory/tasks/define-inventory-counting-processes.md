--- 
title: "Stok sayımı işlemlerini tanımlama"
description: "Bu prosedürde, size, bir sayım grubu ve bir sayım günlüğü oluşturarak, temel stok sayım işlemlerini yapılandırma gösterilecek."
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c14c846c55a3d821945160835817cd4f467deda9
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="define-inventory-counting-processes"></a>Stok sayımı işlemlerini tanımlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedürde, size, bir sayım grubu ve bir sayım günlüğü oluşturarak, temel stok sayım işlemlerini yapılandırma gösterilecek. Ayrıca, ambar ve madde düzeyinde sayım ilkelerinin nasıl etkinleştirileceğini de göreceksiniz. Bu görevler genellikle bir ambar gözetmeni tarafından yerine getirilir. Biraz serbest bırakılmış ürün ve ambar bulundurmak önkoşuldur. Demo veri şirketi kullanıyorsanız, bu prosedürü USMF şirketinde herhangi bir stoklu maddeyle çalıştırabilirsiniz.


## <a name="create-a-counting-group"></a>Sayım grubu oluşturun
1. Stok yönetimi > Kurulum > Stok > Sayım grupları öğesine gidin.
2. Yeni'ye tıklayın.
3. Sayım grubu alanına bir değer girin.
4. İsim alanına bir değer yazın.
5. Sayım kodu alanında bir seçenek belirtin.
    * El ile – İşi her çalıştırmanızda satırları dahil eder. Diğer bir deyişle, sayım grubu için sayım aralığına karar vermiş olursunuz.  Dönem – Dönem aralığı sona erdiğinde, sayım günlüğündeki dönem için satırları dahil eder.   Stok sıfır – Eldeki stok sıfıra (0) inerse, bu iş çalıştırıldığında sayım günlüğünde satırlar oluşturulur. Eldeki stok bir sayımın ardından 0'a inerse, satırlar sayımı bir sonraki çalıştırmanızda oluşturulacaktır.   Minimum – Eldeki stok belirtilen minimuma eşitse veya bundan küçükse, sayım günlüğüne satırlar ekler.  
    * İsteğe bağlı: Sayım Kodu alanında Dönem'i belirttiyseniz, Sayım dönemi alanında dönemin aralığını yazmanız gerekir. Aralıklar için birim gündür.  
    * Sayım günlüğünde yeni satırları oluşturma işini çalıştırdığınız zaman bu aralıkta belirtilen aralıklarla yeni satırlar oluşturulur (aynı işi ne sıklıkta çalıştırdığınız önemli değildir). Örneğin, Sayım dönemini 7'ye ayarlandıysa ve son olarak 1 Ocak tarihindeki bir sayım için günlük satırları oluşturulduysa, 5 Ocak'ta başka bir iş başlatıldığı zaman yedi gün geçmediği için o dönem aralığına ait günlükte satır oluşturulmaz. İşi 8 Ocak'ta yine başlatırsanız, 7 gün geçmiş olduğu için sayım günlüğünde o dönem için satırlar oluşturulur.  
6. Kaydet'e tıklayın.

## <a name="create-a-counting-journal-name"></a>Sayım günlüğü adı oluşturun
1. Stok yönetimi > Kurulum > Günlük adları > Stok öğesine gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. Günlük türü alanında "Sayım"ı seçin.
    * İsteğe bağlı: Sayım günlükleri oluşturma sırasında oluşturulan fiş kodları için belirli bir numara sırası istiyorsanız farklı bir fiş serisi kodu seçebilirsiniz. Fiş serileri Numara sıraları sayfasında oluşturulur.  
6. Ayrıntı düzeyi alanında bir seçenek belirtin.
    * Günlük deftere nakledilirken uygulanan ayrıntı düzeyi.  
    * İsteğe bağlı: Rezervasyon alanındaki değeri değiştirebilirsiniz. Bu, sayım sırasında madde rezerve etmek için kullanılan yöntemdir.   
    * El ile – Rezervasyon formunda maddeler el ile rezerve edilir.   Otomatik – Sipariş miktarı, maddenin eldeki kullanılabilir stoğundan rezerve edilir.   Açılım – Rezervasyon, hareket master planlamasının bir parçasıdır.  
7. Kaydet'e tıklayın.

## <a name="set-standard-counting-journal-name"></a>Standart sayım günlüğü adı ayarlayın
1. Stokyönetimi > Kurulum > Stok ve ambar yönetim parametreleri'ne gidin.
2. Günlükler sekmesine tıklayın.
3. Sayım alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Daha önce oluşturduğunuz günlüğü seçin.
    * Bu günlük, daha sonra, Sayım türündeki stok günlükleri için varsayılan bir günlük adı olur.  
5. Genel sekmesine tıklayın.
    * İsteğe bağlı: Sevk irsaliyeleri, malzeme çekme listeleri veya malzeme çekme listesi kayıtları gibi güncelleştirmeleri önlemek için sayım işlemi sırasında maddeyi kilitlemek üzere bu seçeneği belirtin.  

## <a name="set-the-counting-policy-for-an-item"></a>Bir maddenin sayım ilkesini ayarlayın
1. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
2. Listede, sayım ilkelerini ayarlamak istediğiniz ürünün madde numarasına ait bağlantıya tıklayın.
    * Stoğu izlenen bir madde seçmeniz gerektiğini unutmayın. Stoğu olmayan bir ürün sayılamaz. USMF demo verilerini kullanıyorsanız, madde olarak A0001'i seçebilirsiniz.  
3. Düzenle öğesine tıklayın.
4. Stok yönetimi bölümünün genişletilmiş görünümüne geçin.
5. Sayım grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
6. Listede, önceden oluşturduğunuz sayım grubuna tıklayın.
    * Bu ürün, artık bu sayım grubu kullanılarak stok sayım günlüğü satırları oluşturulurken dahil edilir.  
7. Kaydet'e tıklayın.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Belirli bir ambardaki bir maddenin sayım ilkesini ayarlayın
1. Eylem Bölmesinde, Stok yönetimi'ne tıklayın.
2. Ambar maddeleri'ne tıklayın.
3. Yeni'yi tıklatın.
4. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
5. Listede, sayım belirli ilkelerini ayarlamak istediğiniz ambarı seçin.
6. Sayım grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
7. Listeden bir sayım grubu seçin.
    * Burada, seçtiğiniz belirli bir ambardaki maddeye uygulanması gereken belirli bir sayım grubunu seçebilirsiniz. O ambarda sayım işlemi yapılırken, bu sayım ilkesi, maddeye ilişkin genel sayım ilkesinin yerine geçer.  
8. Kaydet'e tıklayın.



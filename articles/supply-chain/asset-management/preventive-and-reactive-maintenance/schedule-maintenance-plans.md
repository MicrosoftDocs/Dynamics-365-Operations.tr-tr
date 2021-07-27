---
title: Bakım planlarını zamanla
description: Bu konuda Varlık Yönetimi'nde bakım planlarını zamanlama işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a447dee71e57df07d1e7709bc8e4d075fcc803b8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343688"
---
# <a name="schedule-maintenance-plans"></a>Bakım planlarını zamanla

[!include [banner](../../includes/banner.md)]

 

Önleyici bakım zamanlaması, varlıklarda ayarlanan bakım planlarını temel alarak varlıklar üzerinde takvim girişleri oluşturur. Takvim girişlerini seçilen bakım planlarını, varlık türlerini ve varlıkları temel alarak zamanlayabilirsiniz.

1. **Varlık yönetimi** > **Dönemsel** > **Önleyici bakım** > **Bakım planlarını zamanla**'ya tıklayın.

2. **Dönem** ve **Dönem sıklığı** alanlarında bir zaman aralığı seçebilirsiniz.

>[!NOTE]
>**Dönem** ve **Dönem sıklığı** alanları, oluşturduğunuz bakım planlarını temel alarak (zaman temelli veya sayaç temelli) bakım zamanlaması satırlarını ne kadar ileri bir zamanda oluşturmak istediğinizi belirtir. Aşağıdaki şekilde, bakım zamanlaması satırları (= iş emri teklifleri) güncel tarihten itibaren ve üç ay sonrası için oluşturulur.

3. Bakım planı satırına göre iş emirlerinin otomatik olarak oluşturulması gerekiyorsa **Satırda belirtildiyse otomatik oluştur** geçiş düğmesinde "Evet"i seçin.

>[!NOTE]
>Bu geçiş düğmesi "Evet" olarak ayarlanırsa *ve* **Bakım planları**'ndaki bakım planı satırlarında **Otomatik oluştur** onay kutusu da seçilirse iş emirleri, bakım planı satırları temel alınarak oluşturulur ve "Oluşturulan iş emri" durumuna sahip bakım zamanlaması satırları da oluşturulur. Yalnızca bir seçenek belirlenirse (Bu iletişim kutusunda **Satırda belirtildiyse otomatik oluştur** geçiş düğmesi veya **Bakım planları** formundaki **Otomatik oluştur** onay kutusu) yalnızca "Oluşturuldu" durumuna sahip bakım zamanlaması satırları oluşturulur. Bu durumda, iş emri oluşturulmaz.

4. Bakım planlarını (zaman veya sayaç), varlıkları, varlık türlerini, işlem yapılacak yerleşimleri ve işlem yapılacak yerleşim türlerini temel alan takvim girişleri oluşturmak mümkündür. **Filtre** düğmesine tıklayın ve gerekirse seçimlerinizi yapın.

- İşlem yapılacak yerleşimlerde bakım planlarının zamanlanmasıyla ilgili olarak: Bakım planlarını zamanladıktan sonra **Tüm işlem yapılacak yerleşimler** > **Bakım planları** hızlı sekmesindeki bakım planlarında varlık türleri, üreticiler ve modellerin ayarını güncelleştirirseniz, bu işlem yapılacak yerleşimle ilgili mevcut bakım zamanlaması girişleri otomatik olarak silinir. İşlem yapılacak yerleşimdeki güncelleştirilmiş bakım planı ayarına karşılık gelen yeni takvim girişleri oluşturmak için, bu işlem yapılacak yerleşim için yeni bir bakım planı zamanlaması çalıştırmanız gerekir. [İşlem yapılacak yerleşimler oluşturma](../functional-locations/create-functional-locations.md) bölümünde işlem yapılacak yerleşimlerde varlık türleri, üreticiler ve modelleri ayarlama hakkında daha fazla bilgi edinin.

>*Örnek:* Belirli bir işlem yapılacak yerleşim için bir bakım planı oluşturmak isterseniz bu, bakım planını zamanladığınızda belirli bir sürede bu işlem yapılacak yerleşimdeki tüm varlık ayarlarının dahil edileceği anlamına gelir. Bu durumda, bir bakım planı oluşturabilir ve belirli bir işlem yapılacak yerleşimi seçebilirsiniz ancak bakım planına herhangi bir varlık EKLEYEMEZSİNİZ. Bunun sonucunda, bu bakım planını zamanladığınızda bu süre içinde işlem yapılacak yerleşimle ilgili tüm varlıklar için bakım zamanlaması satırları oluşturulur.

- **Varlık Türleri**'ndeki varlık türlerini, üreticileri ve modelleri değiştirirseniz bu değişiklikler yalnızca güncelleştirilmiş varlık türünü kullanan yeni varlıkları etkiler. [Varlık türleri](../setup-for-objects/object-types.md) bölümünde varlık türü ayarlama hakkında daha fazla bilgi edinin.  

5. Varlıklarda bakım zamanlaması girişlerinin oluşturulmasını başlatmak için **Tamam**'a tıklayın. Oluşturulan girişler **Tüm bakım zamanlaması** liste sayfasında gösterilir. Aşağıdaki şekilde bir **Bakım planlarını zamanla** iletişim kutusu örneği gösterilmektedir.

![Şekil 1.](media/09-preventive-maintenance.png)

- **Bakım planlarını zamanla** iletişim kutusunda düzenli aralıklarla otomatik olarak takvim girişleri oluşturmak için **Arka planda çalıştır** hızlı sekmesinde toplu işler ayarlayabilirsiniz.  
- Önleyici bakım zamanladığınızda sistem tarihi ve saatinden önceki beklenen başlangıç tarihi ve saatine sahip bakım zamanlaması satırları oluşturulmaz.  

Aşağıdaki şekilde zaman temelli bir bakım planı hesaplamasının grafik resmi gösterilmektedir.  

![Şekil 2.](media/10-preventive-maintenance.jpg)

Sayaç temelli bakım planlarıyla ilgili olarak: Aşağıdaki şekillerde, iki farklı sayaç kaydı döngüsü gösterilmektedir. Bunlar, varlığın (araç) her ay yaklaşık 2.000 km çalışmasının beklendiği "V0001" varlığı için ayarlanan bir bakım planını temel alır.

İlk örnekte, beklenen 2.000 km'ye her ay ulaşılmaz. Sayaç temelli bakım planına göre, eşik değer 2.000 km'dir. Bu, bir bakım planı zamanlaması çalıştırdığınızda 2.000 kilometre eşik değerine her ulaşıldığında bir bakım zamanlaması satırının oluşturulması gerektiği anlamına gelir. Örnek 1'de, 4 kayıt satırı bulunur ancak 2.000 kilometre eşik değerine yalnızca bir kez ulaşılır. Bu, örneğin 3 aylık bir dönem için bu varlığa yönelik bakım planlarını zamanlamayı çalıştırdığınızda yalnızca bir bakım zamanlaması satırı oluşturulacağı anlamına gelir.

Sonraki şekilde, her ay 2.000 km veya daha fazla değer kaydedilir. Bu nedenle, bu varlığın bakım planlarını 3 aylık bir dönem için zamanlarsanız üç bakım satırı oluşturulur. 

Burada açıklanan örnekler, bir varlıkta gerçekleştirilen tüm sayaç kayıtlarının, varlığın aşınma ve yıpranma eğilimini gösterdiğini belirtir. Bu eğilim, bakım planı zamanlaması sırasında hesaplamaya dayalı olarak kullanılır.

![Şekil 3.](media/11-preventive-maintenance.png)

![Şekil 4.](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
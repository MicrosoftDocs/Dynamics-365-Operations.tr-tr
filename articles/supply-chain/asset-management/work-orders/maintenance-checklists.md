---
title: Bakım denetim listeleri
description: Bu konuda Varlık Yönetimi'ndeki bakım denetim listelerini açıklar.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875951"
---
# <a name="maintenance-checklists"></a>Bakım denetim listeleri


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bakım denetim listeleri, bakım işi türlerinde ayarlanır ve bir iş emri üzerinde çalıştığınızda kullanılır. Bakım denetim listelerini doldurma, iş emrini tamamlamanın bir parçasıdır. **Bakım işi türü varsayılanları** formunda bakım denetim listelerinin nasıl ayarlanacağına ilişkin daha fazla bilgi için bkz. [Bakım işi türü kategorileri ve bakım işi türleri, bakım işi türü çeşitleri, bakım işi işlemleri  ve bakım denetim listeleri](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Bir iş emrindeki bakım denetim listeleri ile çalışırken, bakım işi türleriyle ilgili önceden tanımlanmış bakım denetim listelerini doldurabilirsiniz. Ek bakım denetim listeleri eklemek de mümkündür.

## <a name="fill-out-a-maintenance-checklist"></a>Bakım denetim listesi doldurma

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İş emrini seçin ve **Bakım denetim listesi**'ne tıklatın.

3. **İş emri bakım işi denetim listesinde**, tüm iş emri işleri için bakım denetim listeleri görüntülenir. İş emri işlerinin farklı bakım işi türleri varsa, bakım denetim listeleri her bir iş emri işinde farklı olabilir. İlgili bakım denetim listesiyle çalışacak bir iş emri işi seçin. Seçilen bir bakım denetim listesi satırının ayrıntıları **Satır ayrıntıları** hızlı sekmesinde gösterilir.

4. Tüm bakım denetim listesi satırlarını gösterildikleri sırayla, birer birer doldurun. "Başlık" türündeki bir bakım denetim listesi satırı, altındaki bakım denetim listesi satırlarını gruplamak için başlık olarak kullanılır. Bir başlığı doldurmanız gerekmez, ancak tüm bakım denetim listesi satırı türleri için, başlığa bir **Not** eklemek mümkündür.

5. Yönergeler bir bakım denetim listesi satırıyla ilişkiliyse, **Yönergeler** onay kutusu işaretlenir. **Satır ayrıntıları** hızlı sekmesi > **Yönergeler** bölümünde seçilen bakım denetim listesi satırı için yönergeleri okuyun.

6. Bakım denetim listesi satırını doldurmak için gereken bilgiler, ilgili bakım denetim listesi türüne bağlı olarak değişebilir. Bir bakım denetim listesi satırını **Satır ayrıntıları** hızlı sekmesindeki alanları doldurarak tamamlayın. Örneğin, "Metin" türündeki bir satırda, o denetim listesi satırının sonucunu açıklayan bir **Not** ekleyin. "Ölçüm" türündeki bir satırda, donanımda okuduğunuz **Sayaç değerini** ekleyin; gerekirse bir **Not** da ekleyebilirsiniz.

- Bir bakım denetim listesi satırını tamamladığınızda, satırı tamamlandı olarak işaretlemek **Denetlendi** onay kutusunu seçin. İş emri işiyle ilgili olmadığı için bakım denetim listesi satırını atmak istiyorsanız, satırda **Yok** onay kutusunu seçin. Bakım denetim listesi satırı **Zorunlu** olarak işaretlenmişse, bunu "Denetlendi" veya "Yok" olarak işaretlemeniz gerekir.  
- Bakım denetim listesi kayıtlarını yalnızca, iş emri [Etkin](../setup-for-work-orders/work-order-lifecycle-states.md) bir yaşam döngüsü durumunda olduğunda güncelleştirebilirsiniz.  


## <a name="add-a-maintenance-checklist-line"></a>Bakım denetim listesi satırı ekleme

Bakım denetim listeleri varsayılan bakım iş türü tanımından oluşturulur ve bir iş emri işine aktarılır. Gerekirse, bir iş emri işine bakım denetim listesi satırları ekleyebilirsiniz. El ile eklenen bakım denetim listesi satırları "El ile" referansı alır.

1. **İş emri bakım işi denetim listesinde**, bir bakım denetim listesi eklemek istediğiniz iş emri işini seçin.

2. **Bakım denetim listesi satırları** hızlı sekmesinde, bir bakım kontrol denetim listesi satırı seçin ve seçili bakım denetim listesi satırının arkasına yeni bir satır eklemek istiyorsanız klavyenizdeki aşağı ok düğmesine basın. Sıradaki takip eden numara, otomatik olarak **Satır numarası** alanına eklenir. Ayrıca, bir bakım denetim listesi satırı seçebilir ve seçili bakım denetim listesi satırının üstüne yeni bir satır eklemek istiyorsanız **Satır ekle** düğmesine tıklayabilirsiniz.

3. **Ad** alanında bakım denetim listesi satırı için bir ad girin.

4. **Tür** alanında bakım denetim listesi satırı için bir tür seçin. Her bakım denetim listesi türü için ilgili alanlar **Satır ayrıntıları** hızlı sekmesinde gösterilir.  
  a. "Metin", yapılacak olanların metin açıklamasıyla birlikte bir bakım denetim listesi satırı eklemek için kullanılır. Bir çalışanın bir şeyleri denetlemesini veya incelemesini istiyor ancak belirli (ölçülebilir) bir sonuç beklemiyorsanız bu bakım denetim listesi türü kullanılabilir. **Satır ayrıntıları** hızlı sekmesindeki **Yönergeler** bölümünde yapılacaklar için bir açıklama girin. b. "Başlık" başlığın altında görüntülenen bakım denetim listesi satırlarını gruplamak için başlık olarak kullanılır. Bu, belirli alanlara bölünebilen birkaç bakım denetim listesi satırı varsa yararlıdır. **Ad** alanına açıklayıcı bir ad yazın.  
  c. "Şablon" bir iş emri işine el ile bakım denetim listesi satırı eklediğinizde kullanılamaz.  
  d. "Değişken", bakım denetim listesi satırında bir aralıktaki olası bir sonucu tanımlamak için kullanılır. Bakım denetim listesi değişkenleri ayarı [Bakım işi türü kategorileri ve bakım iş türleri, bakım iş türü çeşitleri, bakım işi işlemleri ve bakım denetim listeleri](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) bölümünde açıklanır. **Ad** alanına değişkeni tanımlamak için bir ad girin. **Değişken** alanında değişkeni seçin. **Satır ayrıntıları** hızlı sekmesindeki **Yönergeler** bölümünde yapılacaklar için bir açıklama girin.  
  e. "Ölçüm" belirli bir ölçümü kaydetmek için kullanılır. **Ad** alanında ölçüm için bir ad girin. **Satır ayrıntıları** hızlı sekmesinde **Sayaç** ve **Birim**'i seçin. **Yönergeler** bölümüne ne yapılacağını açıklayan bir açıklama ekleyin.  

5. Bakım denetim listesi satırlarını el ile eklemeyi bitirdiğinizde, satırları yukarıdaki bölümde açıklandığı gibi doldurun.

>[!NOTE]
>**İş emri bakım işi denetim listesinde**, "İş türü" referanslı bakım denetim listesi satırlarını silemezsiniz. Yalnızca siz veya diğer bakım görevlileri tarafından oluşturulmuş "El ile" referansına sahip olan bakım denetim listesi satırlarını silebilirsiniz.


![Şekil 1](media/14-work-orders.png)


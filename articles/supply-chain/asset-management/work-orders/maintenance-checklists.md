---
title: Bakım denetim listeleri
description: Bu konuda Varlık Yönetimi'ndeki bakım denetim listelerini açıklar.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4ffdf2a997eab741521745ec8207f4f980740ecf
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626282"
---
# <a name="maintenance-checklists"></a>Bakım denetim listeleri

[!include [banner](../../includes/banner.md)]



Bakım denetim listeleri bakım işi türlerinde ayarlanır. Bakım denetim listelerini iş emrini tamamlama işleminin bir parçası olarak doldurursunuz. **Bakım işi türü varsayılanları** sayfasında bakım denetim listelerinin nasıl ayarlanacağına ilişkin daha fazla bilgi için bkz. [Bakım işi türü kategorileri ve bakım işi türleri, bakım işi türü çeşitleri, bakım işi zanaatları ve bakım denetim listeleri](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Bir iş emrindeki bakım denetim listeleri ile çalışırken, bakım işi türleriyle ilgili önceden tanımlanmış bakım denetim listelerini doldurabilirsiniz. Ayrıca, daha fazla bakım denetim listesi ekleyebilirsiniz.


## <a name="fill-in-a-maintenance-checklist"></a>Bakım denetim listesi doldurma

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İş emrini seçin ve sonra Eylem bölmesinde **iş emri** sekmesinde, **Satırlar** grubunda **Bakım denetim listesi** öğesini seçin.

3. **İş emri bakım işi denetim listesi**, tüm iş emri işleri için bakım denetim listelerini görüntüler. İş emri işlerinin farklı bakım işi türleri varsa, bakım denetim listeleri her bir iş emri işinde farklı olabilir. İlgili bakım denetim listesiyle çalışacak bir iş emri işi seçin. Seçilen bir bakım denetim listesi satırının ayrıntıları **Satır ayrıntıları** hızlı sekmesinde gösterilir.

4. Tüm bakım denetim listesi satırlarını gösterildikleri sırayla, birer birer doldurun. Bir bakım denetim listesi satırını **Satır ayrıntıları** hızlı sekmesindeki alanları doldurarak tamamlayın. Bir satırı tamamlamak için gereken bilgiler satır türüne bağlı olarak değişebilir. Örneğin, **Metin** türündeki bir satırda, denetimin sonucunu açıklayan bir not ekleyin. **Ölçüm** türündeki bir satırda, donanımda okuduğunuz sayaç değerini girin ve gerekirse bir not ekleyebilirsiniz. **Başlık** türündeki bir bakım denetim listesi satırı, altındaki bakım denetim listesi satırlarını gruplamak için başlık olarak kullanılır. Başlığı doldurmanız gerekmez. Diğer tüm bakım denetim listesi satırları gibi, **Başlık** türü satırına bir not ekleyebilirsiniz.

5. Yönergeler bir bakım denetim listesi satırıyla ilişkiliyse, **Yönergeler** onay kutusu işaretlenir. **Satır ayrıntıları** hızlı sekmesindeki **Yönergeler** alanında seçilen bakım denetim listesi satırı için yönergeleri okuyun.

6. Bir bakım denetim listesi satırını tamamladığınızda, satırı tamamlandı olarak işaretlemek için **Denetlendi** onay kutusunu seçin. İş emri işiyle ilgili olmadığı için bakım denetim listesi satırını atmak üzere, satırda **Yok** onay kutusunu seçin. Bakım denetim listesi satırında **Zorunlu** onay kutusu işaretlenmişse **Denetlendi** veya **Yok** onay kutusunu seçmeniz gerekir.

>[!NOTE]
>Bakım denetim listesi kayıtlarını yalnızca, iş emri [Etkin](../setup-for-work-orders/work-order-lifecycle-states.md) bir yaşam döngüsü durumunda olduğunda güncelleştirebilirsiniz.  


## <a name="add-a-maintenance-checklist-line"></a>Bakım denetim listesi satırı ekleme

Bakım denetim listeleri varsayılan bakım işi türü tanımından oluşturulur ve bir iş emri işine aktarılır. Gerekirse, bir iş emri işine bakım denetim listesi satırları ekleyebilirsiniz. El ile eklediğiniz bakım denetim listesi satırları **El ile** referansı alır.

1. **İş emri bakım işi denetim listesi** sayfasında bir bakım denetim listesi eklemek istediğiniz iş emri işini seçin.

2. **Bakım denetim listesi satırları** hızlı sekmesinde bir bakım denetim listesi satırı seçin. Sonra, seçili satırdan sonra yeni bir satır eklemek için **Aşağı ok** tuşuna basın. Sıradaki takip eden numara, otomatik olarak **Satır numarası** alanına eklenir. Seçili satırdan önce yeni bir satır eklemek için **Satır ekle**'yi seçin. 

3. **Ad** alanında bakım denetim listesi satırı için bir ad girin.

4. **Tür** alanında bakım denetim listesi satırı için bir tür seçin. Her bakım denetim listesi türü için **Satır ayrıntıları** hızlı sekmesi ilgili alanları içerir.
    - **Metin** - Yapılması gerekenleri açıklayan bir metin içeren bakım denetim listesi satırı eklemek için bu türü kullanın. Örneğin, bir çalışanın bir şeyleri denetlemesini veya incelemesini istiyor ancak belirli (ölçülebilir) bir sonuç beklemiyorsanız bu bakım denetim listesi türünü kullanabilirsiniz. Bu türü seçtikten sonra **Satır ayrıntıları** hızlı sekmesinde, **Yönergeler** alanına, ne yapılması gerektiğini açıklayan bir metin girin.
    - **Başlık** - Bu türdeki bir bakım denetim listesi satırı, altındaki bakım denetim listesi satırlarını gruplamak için başlık olarak kullanılır. Bu tür, belirli alanlara bölünebilen birkaç bakım denetim listesi satırı varsa yararlıdır. Bu türü seçtikten sonra **Ad** alanına açıklayıcı bir ad girin.
    - **Şablon**: Bu tür, bir iş emri işine el ile bakım denetim listesi satırı eklediğinizde kullanılamaz.  
    - **Değişken** - Bakım denetim listesi satırında bir aralıktaki olası bir sonucu tanımlamak için bu türü kullanın. Bakım denetim listesi değişkenleri ayarı hakkında daha fazla bilgi için bkz. [Bakım işi türü kategorileri ve bakım iş türleri, bakım iş türü çeşitleri, bakım işi işlemleri ve bakım denetim listeleri](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Bu türü seçtikten sonra **Ad** alanına değişken için açıklayıcı bir ad girin. **Satır ayrıntıları** hızlı sekmesinde, **Değişken** alanında, değişkeni seçin. **Yönergeler** alanına nelerin yapılması gerektiğin açıklayan bir metin girin.
    - **Ölçüm** - Kakım denetim listesi satırına belirli bir ölçümü kaydetmek için bu türü kullanın. Bu türü seçtikten sonra **Ad** alanına ölçüm için bir ad girin. **Satır ayrıntıları** hızlı sekmesinde, **Sayaç** ve **Birim** alanlarında, uygun değerleri seçin. **Yönergeler** alanına nelerin yapılması gerektiğin açıklayan bir metin girin.

5. Bakım denetim listesi satırlarını el ile eklemeyi bitirdiğinizde, satırları yukarıdaki **Bakım denetim listesini doldurma** bölümünde açıklandığı şekilde doldurun.

>[!NOTE]
>**İş emri bakım işi denetim listesi** sayfasında, **İş türü** referanslı bakım denetim listesi satırlarını silemezsiniz. Yalnızca siz veya diğer bakım görevlileri tarafından oluşturulmuş ve **El ile** referansına sahip olan bakım denetim listesi satırlarını silebilirsiniz.

Aşağıdaki şekilde bir bakım denetim listesi örneği gösterilmiştir.

![Şekil 1](media/14-work-orders.png)


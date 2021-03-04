---
title: Bakım zamanlaması
description: Bu konuda Varlık Yönetimi'nde bakım zamanlaması açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 351e088ece0512fee1bb5f9dad020f32f7728fe4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439329"
---
# <a name="maintenance-schedule"></a>Bakım zamanlaması

[!include [banner](../../includes/banner.md)]

 

Bakım zamanlaması, gerçekleştirilecek tüm beklenen önleyici bakım planlarının, bakım isteklerinin ve bakım kayıtlarının bir listesini içerir. Bazı zamanlama satırları iş emirlerine dönüştürülmüş olabilir.

Dört bakım zamanlaması görünümü, görmek istediğiniz bakım zamanlaması satırlarına bağlı olarak birbirinden biraz farklıdır.

| Menü Öğesi                  | İçeriklerin açıklaması                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tüm bakım zamanlamaları       | Tüm bakım zamanlaması satırları gösterilir.     |
| Kıymet planım        | Çalışan olarak ilgili olduğunuz (şurada ayarlanır: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md)) işlem yapılacak yerleşimlerde yüklü olan varlıkları içeren tüm bakım zamanlaması satırları bu listede gösterilir. |
| Bakım zamanlaması satırlarını aç | "oluşturuldu" durumundaki bakım zamanlaması satırları (henüz iş emrine dönüştürülmemiş veya atılmamış) bu listede görüntülenir.                                            |
| Bakım zamanlaması havuzlarını aç | Bir iş emri havuzuyla ilgili bakım zamanlaması satırları bu listede gösterilmektedir.                                                                                                                  |

>[!NOTE]
>Bakım zamanlaması satırı birkaç iş emri havuzuna dahil edilirse (bkz. [İş emri havuzları](../work-orders/work-order-pools.md)) bir kayıt her bir havuz için **Bakım zamanlaması havuzları aç** seçeneğinde gösterilir. Bu işlem, iş emri havuzlarındaki filtre seçeneklerini en iyi duruma getirmek için gerçekleştirilir.

Bakım zamanlamasını açmak için:

1. **Varlık yönetimi** > **Ortak** > **Bakım zamanlaması** > **Tüm bakım zamanlamaları** veya **Bakım zamanlaması satırlarını aç** veya **Bakım zamanlaması havuzlarını aç** öğesine tıklayın.

2. Bakım zamanlamasını güncelleştirmek için **Bakım planı** veya **Bakım sıraları**'na tıklayın. 

3. Bir bakım zamanlaması satırını, satırı seçip **Düzenle**'ye tıklayarak düzenleyebilirsiniz. Örneğin, servis düzeyini veya işin sorumlu çalışanını kolayca güncelleştirebilirsiniz. Yalnızca henüz bir iş emrine bağlanmamış bakım çizelgesi satırlarını düzenleyebilirsiniz.

4. Bir bakım zamanlaması satırını, liste sayfasında seçip **Sil**'i tıklatarak silebilirsiniz.

5. Bir bakım zamanlaması satırını, liste sayfasında seçip **At**'ı tıklatarak atabilirsiniz. Örneğin, bir varlığın 2.000 km bakım planı ve 10.000 km bakım planı varsa, bu işlev yararlıdır. Daha sonra, 2.000 km bakım planından oluşturulan satırı 10.000 km, 20.000 km, 30.000 km vb. ile oluşturulan satırla denk geldiğinde atmak isteyebilirsiniz. Bir bakım planıyla ilgili bakım zamanlaması satırını iptal ederseniz, bu satır bu bakım planı zamanlandığında tekrar görünmeyecektir.

6. Tüm seçili satırların aynı iş emri havuzuna dahil edilmesini istiyorsanız **Tüm bakım zamanlamaları** ve **İş emri havuzu**'ndaki çok sayıda bakım zamanlaması satırı seçebilirsiniz.

7. **Tüm bakım zamanlamaları** veya **Bakım zamanlaması satırlarını aç** ya da **Bakım zamanlaması havuzlarını aç**'ta bir dizi bakım zamanlaması satırı seçebilir ve birçok satırda aynı düzenlemeyi yapmak istiyorsanız **Zamanlamayı ayarla**'ya tıklayabilirsiniz. Seçilen bakım zamanlaması satırlarıyla ilgili beklenen başlangıç ve bitiş tarihlerini, hizmet düzeyini ve sorumlu bakım çalışanı grubunu veya sorumlu bakım görevlisini değiştirebilisiniz.

- Bir bakım zamanlaması satırı bir iş emriyle ilişkili olduğunda, iş emri kodu **İş emri** alanında görüntülenir.  
- **Tüm varlıklar** ayrıntılı görünümünde > **Varlık bakım planları** hızlı sekmesinde, varlık için bakım planlarını seçebilirsiniz. Daha sonra, **Tüm Varlıklar**'da bir varlıkla ilgili bakım planı satırını silerseniz, bu bakım planını temel alarak oluşturulan "Oluşturuldu" durumundaki tüm bakım zamanlaması satırlarını da otomatik olarak silersiniz. Ayrıca bkz. [Varlık oluşturma](../objects/create-an-object.md).

Aşağıdaki çizimde **Tüm bakım zamanlamaları** liste sayfası gösterilmektedir.

![Şekil 1](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
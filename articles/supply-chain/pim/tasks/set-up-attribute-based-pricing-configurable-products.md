---
title: Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama
description: Bu yordam, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba84fa4de660d16b266763fff5b0b794ed327c81
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844213"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını gösterir. Önkoşul olarak bir veya daha fazla bileşen ve özniteliğe sahip bir ürün yapılandırma modeline sahip olmalısınız. Bu yordam, USMF demo veri şirketindeki Son Teknoloji Hoparlör ürün modelini kullanır. Genel olarak bu yordamı bir ürün yöneticisi kullanır.


## <a name="create-a-new-price-model"></a>Yeni bir fiyat modeli oluşturma
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün yapılandırma modelleri'ne tıklayın.
3. Listede, Son Teknoloji Hoparlör satırını seçin ancak ad bağlantısına tıklamayın.
4. Eylem Bölmesinde,Model öğesine tıklayın.
5. Fiyat modelleri'ne tıklayın.
6. Yeni'ye tıklayın.
7. Fiyat modeli ad alanına bir değer yazın.
    * Modelin tanımlanmasını kolaylaştıracak bir ad kullanın.  
8. Açıklama alanına bir değer girin.
9. Kaydet'e tıklayın.

## <a name="add-price-elements"></a>Fiyat öğeleri ekleme
1. Düzenle öğesine tıklayın.
    * Ürün modelindeki her bileşen, taban fiyat öğesine ve istenen sayıda fiyat ifade kuralına sahip olabilir. Ayrıca farklı para birimlerinde fiyatlar da ekleyebilirsiniz.  
2. Taban fiyat ifadesi alanına bir değer yazın.
    * Örneğin 100 yazın.   Taban fiyat ifadesi sayısal bir değer olabilir veya bir veya daha fazla özniteliği kapsayan aritmetik hesaplamadan oluşabilir.  
3. Ekle öğesini tıklatın.
4. Ad alanına "Rosewood" yazın.
    * Fiyat ifadesi adı fiyat öğesinin neyi temsil ettiğini tanımlamaya yardımcı olur. Bu örnekte, Rosewood hoparlör kabini rengi seçeneği için bir fiyat öğesi oluşturuyoruz.  
5. Koşulu düzenle'ye tıklayın.
    * Fiyat koşulu, yalnızca özniteliklerin belirli bir birleşimi varsa bir fiyat ifadesinin satış fiyatına dahil edilmesini garanti etmeye yardımcı olur.  
6. ConstraintBody alanına "CabinetFinish=="Rosewood"" yazın.
7. Tamam'a tıklayın.
8. İfade alanına bir değer yazın.
    * Örneğin 50 yazın.  
9. Sayfayı kapatın.
10. Sayfayı kapatın.


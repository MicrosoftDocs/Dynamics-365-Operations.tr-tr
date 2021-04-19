---
title: Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama
description: Bu konu, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını açıklar.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f54d0ea87d8ce5ffdf5600995004e558ddd86fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833269"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama

[!include [banner](../../includes/banner.md)]

Bu konu, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını açıklar. Önkoşul olarak bir veya daha fazla bileşen ve özniteliğe sahip bir ürün yapılandırma modeline sahip olmalısınız. Bu yordam, USMF demo veri şirketindeki Son Teknoloji Hoparlör ürün modelini kullanır. Genel olarak bu yordamı bir ürün yöneticisi kullanır.


## <a name="create-a-new-price-model"></a>Yeni bir fiyat modeli oluşturma
1. Giriş sayfasında **Ürün çeşidi model tanımı**'nı seçin.
2. **Bağlantılar** bölümünde **Ürün yapılandırma modelleri**'ni seçin.
3. Listede, **Son Teknoloji Hoparlör** satırını seçin ancak ad bağlantısını seçmeyin.
4. Eylem Bölmesinde, **Model**'i seçin.
5. **Fiyat modelleri**'ni seçin.
6. **Yeni**'yi seçin.
7. **Fiyat modeli adı** alanına bir değer yazın. Modelin tanımlanmasını kolaylaştıracak bir ad kullanın.  
8. **Tanım** alanına bir değer girin.
9. **Kaydet**'i seçin.

## <a name="add-price-elements"></a>Fiyat öğeleri ekleme
1. **Düzenle** öğesini seçin. Ürün modelindeki her bileşen, taban fiyat öğesine ve istenen sayıda fiyat ifade kuralına sahip olabilir. Ayrıca farklı para birimlerinde fiyatlar da ekleyebilirsiniz.  
2. **Taban fiyat ifadesi** alanına bir değer yazın. Örneğin 100 yazın. Taban fiyat ifadesi sayısal bir değer olabilir veya bir veya daha fazla özniteliği kapsayan aritmetik hesaplamadan oluşabilir.  
3. **Ekle**'yi seçin.
4. **Ad** alanına `Rosewood` yazın. Fiyat ifadesi adı fiyat öğesinin neyi temsil ettiğini tanımlamaya yardımcı olur. Bu örnekte, Rosewood hoparlör kabini rengi seçeneği için bir fiyat öğesi oluşturuyoruz.  
5. **Koşulu düzenle**'yi seçin. Fiyat koşulu, yalnızca özniteliklerin belirli bir birleşimi varsa bir fiyat ifadesinin satış fiyatına dahil edilmesini garanti etmeye yardımcı olur.  
6. **ConstraintBody** alanına `CabinetFinish=="Rosewood"` girin.
7. **Tamam**'ı seçin.
8. **İfade** alanına bir değer yazın. Örneğin, `50` yazın. 
9. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
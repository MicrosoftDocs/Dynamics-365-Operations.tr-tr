---
title: Ölçü birimini yönetme
description: Bu yordam, bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8d9b6f18fdc1c47d6a695ca6a2330f6f02fc1bd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439154"
---
# <a name="manage-unit-of-measure"></a>Ölçü birimini yönetme

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir. Bu yordamı demo verileri veya kendi verilerinizi kullanarak adım adım yerine getirebilirsiniz.

1. **Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürün bakımı**'na gidin.
2. **Birimler**'e tıklayın.

## <a name="create-a-unit-of-measure"></a>Bir ölçü birimi oluşturun
1. **Yeni**'ye tıklayın.
2. **Birim** alanına bir değer yazın. Bir ölçü birimini referans gösterirken Kimliğini veya sembolünü girin.  
3. **Tanım** alanına bir değer girin. Sistem dilinde ölçü için açıklayıcı bir ad girin.  
4. **Birim sınıfı** alanında, bir seçenek seçin. Birimi sınıfı, ölçü biriminin alan, hacim veya miktar gibi mantıksal bir gruplandırmalardan hangisinin parçası olduğunu tanımlar.  
5. **Ondalık hassasiyeti** alanına bir numara girmelisiniz. Ölçü birimi için hesaplama tamamlandığında, çevirilen ölçü biriminin kaç ondalık basamağa yuvarlanacağını belirtin.  
6. **Kaydet**'e tıklayın.

## <a name="define-unit-translations"></a>Birim çevirilerini tanımlayın
1. **Eylem Bölmesi**'nde, **Birim metinleri**'ne tıklayın.
2. **Yeni**'ye tıklayın. Müşteri veya satıcıya özgü dillerde ölçü birimini temsil edecek bir sembol veya Kimliğin çevirisini oluştururken birim yazısı kullanın.  
3. **Dil** alanına bir değer girin veya buradan bir değer seçin.
4. **Metin** alanına bir değer yazın.
5. **Kaydet**'e tıklayın.
6. Sayfayı kapatın.
7. **Eylem Bölmesi**'nde, **Çevrilmiş birim açıklamaları**'na tıklayın.
8. **Yeni**'ye tıklayın. Ölçü birimi için dile özgü açıklamalar tanımlayın.  
9. **Dil** alanına bir değer girin veya buradan bir değer seçin.
10. **Tanım** alanına bir değer girin.
11. **Kaydet**'e tıklayın.
12. Sayfayı kapatın.

## <a name="define-unit-conversion-rules"></a>Birim dönüştürme kurallarını tanımlayın
1. **Eylem Bölmesi**'nde, **Birim dönüştürmeleri**'ne tıklayın. Ölçü birimini seçili birim sınıfında bir başka ölçü birimine dönüştürmek için kurallar tanımlayın.  
2. Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.
3. **Faktör** alanına bir sayı girin. İlk birim ve son birim arasında dönüştürme faktörü. Örneğin, bir metrede 100 santimetre olduğu için santimetreden metreye dönüştürme faktörü 100'dür.  
4. **Hedef birim** alanına bir değer girin veya bir değer seçin.
5. **Yuvarlama** alanında, bir seçenek seçin. Çevrilen değerin nasıl yuvarlanması gerektiğini tanımlayın  
6. **Tamam**'a tıklayın.
7. Sayfayı kapatın.


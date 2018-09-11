--- 
title: "Ölçü birimini yönetme"
description: "Bu yordam, bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir."
author: sorenva
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6bb7a5133e9412f4ed6fb74f0d3ee595c07a0c4b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="manage-unit-of-measure"></a>Ölçü birimini yönetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir. Bu yordamı demo verileri veya kendi verilerinizi kullanarak adım adım yerine getirebilirsiniz.

1. Serbest bırakılan ürün bakımı'na gidin.
2. Birimleri'ni tıklatın.

## <a name="create-a-unit-of-measure"></a>Bir ölçü birimi oluşturun
1. Yeni'ye tıklayın.
2. Birim alanına bir değer yazın.
    * Bir ölçü birimini referans gösterirken Kimliğini veya sembolünü girin.  
3. Açıklama alanına bir değer girin.
    * Sistem dilinde ölçü için açıklayıcı bir ad girin.  
4. Birim sınıfı alanında, bir seçenek seçin.
    * Birimi sınıfı, ölçü biriminin alan, hacim veya miktar gibi mantıksal bir gruplandırmalardan hangisinin parçası olduğunu tanımlar.  
5. Ondalık hassasiyeti alanına bir numara girmelisiniz.
    * Ölçü birimi için hesaplama tamamlandığında, çevirilen ölçü biriminin kaç ondalık basamağa yuvarlanacağını belirtin.  
6. Kaydet'e tıklayın.

## <a name="define-unit-translations"></a>Birim çevirilerini tanımlayın
1. Birim metinleri'ne tıklayın.
2. Yeni'ye tıklayın.
    * Müşteri veya satıcıya özgü dillerde ölçü birimini temsil edecek bir sembol veya Kimliğin çevirisini oluştururken birim yazısı kullanın.  
3. Dil alanına bir değer girin veya buradan bir değer seçin.
4. Metin alanına bir değer yazın.
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.
7. Çevrilmiş birim açıklamaları'na tıklayın.
8. Yeni'ye tıklayın.
    * Ölçü birimi için dile özgü açıklamalar tanımlayın.  
9. Dil alanına bir değer girin veya buradan bir değer seçin.
10. Açıklama alanına bir değer girin.
11. Kaydet'e tıklayın.
12. Sayfayı kapatın.

## <a name="define-unit-conversion-rules"></a>Birim dönüştürme kurallarını tanımlayın
1. Birim dönüştürmeleri'ne tıklayın
    * Ölçü birimini seçili birim sınıfında bir başka ölçü birimine dönüştürmek için kurallar tanımlayın.  
2. Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.
3. Faktör alanına bir sayı girin.
    * İlk birim ve son birim arasında dönüştürme faktörü. Örneğin, bir metrede 100 santimetre olduğu için santimetreden metreye dönüştürme faktörü 100'dür.  
4. Hedef birim alanına bir değer girin veya bir değer seçin.
5. Yuvarlama alanında, bir seçenek seçin.
    * Çevrilen değerin nasıl yuvarlanması gerektiğini tanımlayın  
6. Tamam'a tıklayın.
7. Sayfayı kapatın.



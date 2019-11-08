---
title: Bakım öznitelik türleri
description: Bu konuda Kıymet Yönetimi'nde öznitelik türleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c07f303b72f286c33979181fca1592b47efa1303
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571243"
---
# <a name="maintenance-attribute-types"></a>Bakım öznitelik türleri

[!include [banner](../../includes/banner.md)]

 

Bu konuda Kıymet Yönetimi'nde öznitelik türleri oluşturma işlemi açıklanmaktadır. Öznitelikler, çeşitli öğelerin özelliklerini açıklamak için kullanılır. Aşağıdaki öğelerin özniteliklerini ayarlayabilirsiniz:

- [İşlem yapılacak yerleşim türleri](../setup-for-functional-locations/functional-location-types.md)
- [İşlem yapılacak yerleşimler](../functional-locations/create-functional-locations.md)
- [Kıymet türleri](../setup-for-objects/object-types.md)
- Varlıklar

Ayarlayabileceğiniz öznitelikler öğeye bağlı olarak değişir. Örneğin işlem yapılacak yerleşim için yerleşimin fiziksel boyutu ile yapılandırma özniteliklerini ayarlayabilirsiniz. Bir kıymet türü veya bir kıymet için motor hacmi, güç tüketimi ve farklı koşullarda maksimum yük kapasitesi özniteliklerini ayarlayabilirsiniz.

## <a name="create-attribute-types"></a>Öznitelik türleri oluştur

Kendi öznitelik türlerinizi oluşturabilirsiniz. Ayrıca, ürün boyutlarını **Öznitelik türleri** sayfasına aktarabilirsiniz.

1. **Kıymet yönetimi** \> **Kurulum** \> **Öznitelik türleri** öğesini seçin.
2. Öznitelik türlerini ilk kez ayarladığınızda standart ürün boyutlarını otomatik olarak aktarmak için **Ürün boyutları oluştur** öğesini seçin.
3. Yeni bir öznitelik türü oluşturmak için **Yeni**'yi seçin.
4. **Öznitelik türü** alanına, öznitelik türü için bir ad girin.
5. **Açıklama** alanına bir açıklama girin.
6. **Birim** alanında, gerektiği şekilde, ilgili öznitelik birimini seçin.
7. **Veri türü** alanında birim için bir veri türü seçin.
8. Veri türü olarak **Dize** seçtiyseniz öznitelik türü değeri oluşturmak için aşağıdaki adımları izleyin:

    1. Öznitelik türünü ve ardından **Değerler**'i seçin.
    2. **Öznitelik değerleri** alanında, **Yeni**'yi seçin.
    3. **Öznitelik türü** alanında bir öznitelik türü (boyut) seçin.
    4. **Değer** alanına ilgili değeri girin.
    5. **Açıklama** alanına bir açıklama girin.
    6. Kaydı kaydedin.
    7. **Öznitelik türleri** sayfasına dönün.

9. Kaydı kaydedin.

    **İşlem yapılacak yerleşim türleri** alanında öznitelik türünü kullanan işlem yapılacak yerleşimlerin sayısını gösterir. **Kıymet türleri** alanı bunu kullanan kıymet türlerinin sayısını gösterir.

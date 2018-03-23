---
title: "Ürün kategorisi yönetimi"
description: "Bu konu alım satım yöneticilerinin, Perakende ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasındaki ilişkileri yönetmek için Perakende ürün kategorilerini nasıl kullanacağını açıklar."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: tr-tr
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a>Gelişmiş ürün ve kategori yönetimi

[!include[banner](./includes/banner.md)]

Bu konu,Dynamics 365 for Retail'de Perakende ürün kategorilerini ve ürünlerini yönetmenin gelişmiş bir yolunu açıklar. Bu geliştirmeler alım satım yöneticilerinin Perakende ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasındaki ürün özelliklerinin genel yapısını görüntülemesine olanak tanır.

Perakende ürün kategorilerini yönetme hakkında daha fazla bilgi için **Kategori ve ürün yönetimi** çalışma alanından **Perakende ürün hiyerarşisi**'ne gidin ve **Perakende ürün kategorisi** sayfasının gelişmiş yapısını not edin.

![Kategori ve ürün yönetimi çalışma alanı](media/LaunchRetailProductHierarchy.png)

Önceki sürümlerde, ürün özellikleri uygulanabilirliklerinin kapsamına dayalı olarak **Temel ürün özellikleri** ve **Perakende ürün özelliklerine** ayrılmıştı. **Perakende ürün özellikleri**'nin uygulanabilirlik kapsamı *genel*di; bu, belirli bir **Perakende ürün özelliği** için tüm tüzel kişilikler arasında aynı değerin paylaşıldığı anlamına gelir. **Temel ürün özellikleri** *tüzel kişiliğe* özeldir. Başka bir deyişle, belirli bir **Temel ürün özelliği** için değer, tekil iş gereksinimlerine dayanarak tüzel kişilikler arasında fark gösterebiliyordu.

Gelişmiş Perakende ürün kategorisi yapısında, ürün özellikleri, serbest bırakılan ürün ayrıntıları form yapısını yansıtmak amacıyla bir grup içerisindeki uygulanabilirlikleri temel alınarak ayrılır.

![Alanları uygulanabilirlik kapsamlarına göre gruplandırma](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Tüm tüzel kişilikler arasında tüzel varlığa özel şirketleri yönetmek ve bunları özel bir tüzel kişilik için yönetmek arasında geçiş yapabilirsiniz. Bunu yapmak için, **Tüm tüzel kişilikleri görüntüle/düzenle** veya **Belirli bir tüzel kişiliği görüntüle/düzenle**'yi seçin.

![Tek ve tüm tüzel kişilikler arasında geçiş yapma](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Tek ve tüm tüzel kişilikler arasında geçiş yapma](media/ToggleToEditForAllLegalEntities.PNG)  

Önceki sürümlerle karşılaştırıldığında, yeni Perakende ürün kategorisi yapısında bir alım satım yöneticisi tek kategori düzeyindeki ek bir ürün özellikleri kümesi için varsayılan değerler de tanımlayabilir. Ürün oluşturma sırasında, bu varsayılan ürün özellik değerleri, Perakende ürün hiyerarşisindeki ayrı bir kategori ile olan ilişkisi temel alınarak bir ürün tarafından devralınabilir. Her bir ürün için devralınan bu ürün özellikleri, tekil işletme gereksinimlerini karşılamak üzere değiştirilebilir.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Perakende ürün kategorisi formundan ürünleri güncelleştirmek için özellikleri seçin 
 
Hangi güncelleştirilmiş ürün özelliklerinin ilişkili ürünlere gönderileceğini seçmek amacıyla ürün özellikleri için geliştirilmiş bu yeni yapıyı kullanabilirsiniz. 

![Güncelleştirilmiş ürünlerin yeni gelişmiş görünümü](media/NewUpdateProductsEnhancedView.PNG) 

Satış yöneticileri, her bir ürün için devralınan bu ürün özelliklerini, tekil işletme gereksinimlerini karşılamak üzere değiştirebilirler.



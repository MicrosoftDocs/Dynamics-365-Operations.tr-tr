---
title: Ürün kategorilerini ve ürünlerini yönetme
description: Bu konu alım satım yöneticilerinin, Commerce ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasındaki ilişkileri yönetmek için Commerce ürün kategorilerini nasıl kullanacağını açıklar.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cee79d6937afeec1e607abde49d52790c51e98a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001086"
---
# <a name="manage-product-categories-and-products"></a>Ürün kategorilerini ve ürünlerini yönetme

[!include [banner](./includes/banner.md)]

Bu konu, Dynamics 365 Commerce'de ürün kategorilerini ve ürünlerini yönetmenin gelişmiş bir yolunu açıklar. Geliştirmeler alım satım yöneticilerinin ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasında paylaşılan ürün özelliklerinin yapısını görüntülemesine olanak tanır.

Ürün kategorilerinin nasıl yönetileceği hakkında daha fazla bilgi için **Kategori ve ürün Yönetimi** çalışma alanında **Commerce ürün hiyerarşisi** kutucuğunu seçin.

Görüntülenen **Commerce ürün hiyerarşisi** sayfasının gelişmiş yapısını not edin. Uygulamanın önceki sürümlerinde, ürün özellikleri uygulanabilirliklerinin kapsamına dayalı olarak *temel ürün özellikleri* ve *Retail ürün özelliklerine* ayrılmıştı. Perakende ürün özellikleri kendi uygulanabilirlik kapsamı içinde *genel*'dir. Başka bir deyişle, belirli bir ürün özelliği için, aynı değer farklı tüzel kişilikler arasında paylaşılıyor. Aksine, temel ürün özellikleri *tüzel kişiliğe özeldir*. Başka bir deyişle, belirli bir temel ürün özelliği için değer, tekil iş gereksinimlerine bağlı olarak tüzel kişilikler arasında fark gösterebilir.

Gelişmiş ürün kategorisi yapısında, ürün özellikleri, serbest bırakılan ürün ayrıntıları form yapısını yansıtmak amacıyla bir grup içerisindeki uygulanabilirlikleri temel alınarak ayrılır.

![Özelliklerin uygulanabilirlik kapsamlarına göre gruplandırılan alanlar](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Tüm tüzel kişilikler arasında tüzel varlığa özel şirketleri yönetmek ve bunları özel bir tüzel kişilik için yönetmek arasında geçiş yapabilirsiniz.

Tüzel kişiliklerdeki özellikleri yönetmek için **Tüm tüzel kişilikleri görüntüle** (veya **Tüm tüzel kişilikleri düzenle**) öğesini seçin.

![Tüm tüzel kişilikleri görüntüle/düzenle](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Belirli bir tüzel kişilik özelliklerini yönetmek için **Belirli bir tüzel kişiliği görüntüle** (veya **Belirli bir tüzel kişiliği düzenle**) öğesini seçin.

![Belirli bir tüzel kişiliği görüntüle/düzenle](media/ToggleToEditForAllLegalEntities.PNG)

Buna ek olarak, geliştirilmiş Retail ürün kategorisi yapısında bir alım satım yöneticisi tek kategori düzeyindeki ek bir ürün özellikleri kümesi için varsayılan değerler de tanımlayabilir. Böylece, ürünler oluşturulduğunda, ürün özellikleri için ürün hiyerarşisindeki tek bir kategori ile bu özelliklerin ilişkisi temel alınarak varsayılan değerleri devralırlar. Her bir ürün için devralınan bu ürün özellikleri, tekil işletme gereksinimlerini karşılamak üzere değiştirilebilir.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Commerce ürün hiyerarşisi sayfasında ürünleri güncelleştirmek için özellikleri seçme

Hangi güncelleştirilmiş ürün özelliklerinin ilişkili ürünlere gönderileceğini seçmek amacıyla ürün özellikleri için geliştirilmiş yeni yapıyı kullanabilirsiniz. Eylem bölmesindeki **Commerce ürün hiyerarşisi** sayfasında **Kategori**'yi seçin ve ardından **Ürünleri güncelleştir**'i seçerek **Ürünleri güncelleştir** iletişim kutusunu açın.

![Ürünleri güncelleştir iletişim kutusu](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
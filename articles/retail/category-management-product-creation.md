---
title: "Ürün kategorisi yönetimi ve oluşturulması"
description: "Bu konu, Perakende ürün kategorileri için yönetim deneyimine yapılan geliştirmeleri açıklar. Bu geliştirmeler alım satım yöneticilerinin Perakende ürün hiyerarşisi ve serbest bırakılan ürün ayrıntıları arasında bir ilişkiye sahip olmalarını imkan verir."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 74a8fa863736177bcf8cb4b3d90911c78122252b
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---

# <a name="product-category-management-and-creation"></a>Ürün kategorisi yönetimi ve oluşturulması

[!include[banner](./includes/banner.md)]

Perakende ürün kategorileri için yönetim deneyiminde yapılmış geliştirmeler alım satım yöneticilerinin Perakende ürün hiyerarşileri ve serbest bırakılan ürün ayrıntıları arasında bir ilişkiye sahip olmalarına olanak verir. Bu geliştirmeleri görüntülemek için **Kategori ve ürün yönetimi**  çalışma alanında **Perakende ürün kategorisi yeni yapısı** sayfasını açmak için **Perakende ürün hiyerarşisi**'ni seçin. 

Önceki sürümlerde, ürün özellikleri temel ürün özellikleri ve Perakende ürün özelliklerine ayrılmıştı; uygulanabilirliklerinin kapsamına dayanarak. Perakende ürün *genel* özelliklerdi. Başka bir deyişle, belirli bir ürün özelliği için, aynı değer farklı tüzel kişilikler arasında paylaşılıyor. Temel ürün özellikleri *tüzel kişiliğe özel* idi. Başka bir deyişle, bir ürün özelliği, tekil iş gereksinimlerine dayanarak tüzel kişilikler arasında fark gösterebiliyordu.

Bu geliştirmelerle, Perakende ürün kategorisi içindeki bir ürün özelliği için alanları ayırmaya devam ediyoruz, bir grup içerisindeki uygulanabilirliklerine dayanarak; serbest bırakılan ürün ayrıntıları form yapısını yansıtmak için.

Tüm tüzel kişilikler arasında tüzel varlığa özel şirketleri yönetmek ve bunları özel bir tüzel kişilik için yönetmek arasında geçiş yapabilirsiniz. **Tüm tüzel kişilikleri görüntüle/düzenle** veya **Belirli bir tüzel kişiliği görüntüle/düzenle**'yi ihtiyaç duyduğunuz şekilde seçin.

Satış yöneticileri ayrıca tekil kategori düzeyinde ürün özellikleri için ek varsayılan değerler de tanımlayabilirler. Bu özellik değerleri ürün başına, ürün oluşturulması sırasında bir kategori ile ilişkilendirmelerine dayanarak devralınır.

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>Perakende ürün kategorisi formundan ürünleri güncelleştirmek için özellikleri seçin

Hangi güncelleştirilen ürün özelliklerinin ilişkilendirilmiş ürünlere gönderileceğini seçmek için mantıksal gruplama özelliklerini kullanabilirsiniz.

Satış yöneticileri, her bir ürün için devralınan bu ürün özelliklerini, tekil işletme gereksinimlerini karşılamak üzere değiştirebilirler.


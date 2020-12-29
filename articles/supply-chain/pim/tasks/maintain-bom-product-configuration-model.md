---
title: Ürün yapılandırma modeli için ürün reçetesini koruma
description: Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcdf4b735587b76b7f761f59c56da1ca358a2e37
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439156"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Ürün yapılandırma modeli için ürün reçetesini koruma

[!include [banner](../../includes/banner.md)]

Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir. Bu yordamı oluşturmak için USMF demo şirketindeki son teknoloji hoparlör modeli kullanılır.


## <a name="add-a-bom-line"></a>Bir ürün reçetesi satırı ekleme
1. Ürün varyantı model tanımı'na tıklayın.
2. Ürün yapılandırma modelleri'ne tıklayın.
3. Listede, istenen kaydı bulun ve seçin.
    * Bu yordam için son teknoloji hoparlörü seçin.  
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Ürün reçetesi satırları bölümünü genişletin.
6. Ekle öğesini tıklatın.
7. İsim alanına bir değer yazın.
8. Açıklama alanına bir değer girin.
9. Kaydet'e tıklayın.

## <a name="add-bom-line-details"></a>Ürün reçetesi satırı ayrıntılarını ekleme
1. Ürün reçetesi satır ayrıntılarını tıklatın.
2. Madde numarası alanında bir değer girin veya seçin.
    * Örneğin, ürün M0055'i seçebilirsiniz.  
    * Her ürün reçetesi satırı özelliği için sabit bir değer mi alacağını yoksa bir özniteliğe mi eşleneceğini seçebilirsiniz.  
3. Ayarla onay kutusunu işaretleyin.
4. Hesaplama alanında Evet'i seçin.
    * Hesaplama özelliğini Evet olarak ayarladığınızda, ürün reçetesi satırının maliyet hesaplamalarına dahil edildiğinden emin olursunuz.  
5. Kurulum sekmesine tıklayın.
6. Ayarla onay kutusunu işaretleyin.
7. Miktar alanına bir sayı girin.
    * Miktar alanı, ürünün ne kadarının ürün reçetesine dahil edileceğini belirler. Bu, özellik eşleme için kullanılabilecek kesin bir seçenek olabilir.  
8. Boyut sekmesini tıklatın.
    * Ürün boyutlarından herhangi birinin etkin olup olmadığını ve ardından bir değerin eklenmiş veya özniteliğin atanmış olduğunu doğrulayın.  
9. Tamam'a tıklayın.


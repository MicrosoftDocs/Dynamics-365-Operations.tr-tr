---
title: Ürün yapılandırma modeli için ürün reçetesini koruma
description: Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921329"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Ürün yapılandırma modeli için ürün reçetesini koruma

[!include [banner](../../includes/banner.md)]

Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir. Bu yordamı oluşturmak için USMF demo şirketindeki son teknoloji hoparlör modeli kullanılır.

## <a name="add-a-bom-line"></a>Bir ürün reçetesi satırı ekleme

1. **Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.
1. Listede, istenen kaydı bulun ve seçin.
    * Bu yordam için son teknoloji hoparlörü seçin.  
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **Ürün reçetesi satırları** bölümünü genişletin.
1. **Ekle**'yi seçin.
1. **Ad** alanına bir değer yazın.
1. **Tanım** alanına bir değer girin.
1. **Kaydet**'i seçin.

## <a name="add-bom-line-details"></a>Ürün reçetesi satırı ayrıntılarını ekleme

1. **Ürün reçetesi satırı ayrıntıları**'nı seçin.
2. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
    * Örneğin, ürün M0055'i seçebilirsiniz.  
    * Her ürün reçetesi satırı özelliği için sabit bir değer mi alacağını yoksa bir özniteliğe mi eşleneceğini seçebilirsiniz.  
3. **Ayarla** onay kutusunu işaretleyin.
4. **Hesaplama** alanında *Evet*'i seçin.
    * **Hesaplama** özelliğini *Evet* olarak ayarladığınızda, ürün reçetesi satırının maliyet hesaplamalarına dahil edildiğinden emin olursunuz.  
5. **Kurulum** sekmesini seçin.
6. **Ayarla** onay kutusunu işaretleyin.
7. **Miktar** alanına bir sayı girin.
    * Miktar alanı, ürünün ne kadarının ürün reçetesine dahil edileceğini belirler. Bu, özellik eşleme için kullanılabilecek kesin bir seçenek olabilir.  
8. **Boyut** sekmesini seçin.
    * Ürün boyutlarından herhangi birinin etkin olup olmadığını ve ardından bir değerin eklenmiş veya özniteliğin atanmış olduğunu doğrulayın.  
9. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
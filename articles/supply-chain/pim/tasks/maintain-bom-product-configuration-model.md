---
title: Ürün yapılandırma modeli için ürün reçetesini koruma
description: Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd78b06f10d0c9b1df57dacdd824b06ebe414b3b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577300"
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
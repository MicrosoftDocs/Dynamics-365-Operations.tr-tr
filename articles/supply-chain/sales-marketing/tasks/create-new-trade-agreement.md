---
title: Yeni bir ticari sözleşme oluşturma
description: Bu yordam belirli bir müşteri ile üzerinde anlaştığınız yeni bir ürün satış fiyatını kaydetmek için bir ticari sözleşmenin nasıl oluşturulacağını gösterir.
author: omulvad
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43426e77c30e46f4dd1cc117c38cf6ba5437655b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439103"
---
# <a name="create-a-new-trade-agreement"></a>Yeni bir ticari sözleşme oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam belirli bir müşteri ile üzerinde anlaştığınız yeni bir ürün satış fiyatını kaydetmek için bir ticari sözleşmenin nasıl oluşturulacağını gösterir. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Eğer kendi verilerinizi kullanıyorsanız, bu kılavuz başlamadan önce varsayılan ilişkisi "Fiyat (satış)" olarak ayarlanan bir ticari sözleşmenin günlük adının var olduğundan emin olmanız gerekir.


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Yeni bir ticari sözleşme günlüğü oluşturun ve deftere nakledin.
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Fiyatlar ve indirimler > Ticari sözleşme günlükleri**'ne gidin.
2. **Yeni**'ye tıklayın.
3. **Ad** alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, istenen kaydı bulun ve seçin.
5. **Eylem Bölmesi**'nde, **Satırlar**'a tıklayın.
6. **Hesap kodu** alanında "Tablo" seçeneğini seçin.
    
    Bu örnekte, belirli bir müşteri için fiyat güncelleştirmesi yapıyorsunuz bu yüzden de Tablo seçmeniz lazım. Ürünün liste fiyatını güncelleştiriyor olsaydınız yeni fiyatın tüm müşteriler için geçerli olmasını sağlamak için "Tümü" seçeneğini seçecektiniz. Müşteri segmentleri arasında fiyat farklılaştırması yapacak olsaydınız, Grup seçeneğini seçmeniz gerekirdi. Grup'u seçmek için müşteri fiyat grupları ayarlamış olmanız gerekir.  

7. **Hesap seçimi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
8. Listede, istenen kaydı bulun ve seçin.
9. **Madde kodu** alanında "Tablo" seçeneğini seçin.
    
    "Fiyat (satışlar)" türünde bir ticari anlaşmaya girecek olduğunuzda, **Item code** alanında sadece "Tablo" seçeneğini seçmelisiniz. Bunun sebebi bir fiyatın mutlak değerde olmasıdır ve tüm ürünler veya ürün grupları için aynı olamayışıdır.
    
10. **Madde ilişkisi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
11. Listede, sözleşmeye dahil etmek istediğiniz ürünü seçin. Hangi ürünü seçtiğinizi not alın.  
12. **Başlangıç** alanında bir minimum miktar girin.
    - Müşterinin yeni fiyata hak kazanmadan önce sipariş etmesi gereken minimum bir miktar varsa, bu miktarı burada belirtmeniz gerekir.  
    - Anlaşması fiyatının daha fazlasında geçerli olmayacağı bir maksimum miktar belirtmek için **Bitiş** alanına bir değer girin. Fiyatlar ve indirimleri temel alan birden fazla miktar kırılması sunacaksanız her miktar aralığını bir çift minimum ve maksimum miktar olarak **Başlangıç** ve **Bitiş** alanları ile belirtin.
13. **Para birimi cinsinden tutar alanına** bir fiyat girin.
14. **Ayrıntılar** bölümünün altındaki **Başlangıç tarihi** alanına bu anlaşmanın geçerliliğinin başlayacağı tarihi girin.
15. **Kaydet**'e tıklayın.
16. **Doğrula**'ya tıklayın.
17. **Seçilen satırları doğrula**'ya tıklayın.
18. **Tamam**'a tıklayın.
19. **Naklet**'e tıklayın.
20. **Tamam**'a tıklayın.

## <a name="view-trade-agreements-for-a-product"></a>Bir ürün için ticari sözleşmeleri görüntüleyin
1. **Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.
2. Listede, fiyatını az önce güncelleştirdiğiniz ürünü bulun ve seçin.
3. **Eylem bölmesi**'nde, **Satış**'a tıklayın.
4. **Ticaret anlaşmalarını görüntüle**'ye tıklayın.
    
    Yeni oluşturduğunuz fiyat ticari sözleşmesinin ayrıntılarını gözden geçirin.    

5. Sayfayı kapatın.

## <a name="additional-resources"></a>Ek kaynaklar
### <a name="community-blogs"></a>Topluluk blogları
- [Dynamics 365 for Finance and Operations içindeki satış fiyatları](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)

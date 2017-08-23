--- 
title: "Yeni bir ticari sözleşme oluşturma"
description: "Bu yordam belirli bir müşteri ile üzerinde anlaştığınız yeni bir ürün satış fiyatını kaydetmek için bir ticari sözleşmenin nasıl oluşturulacağını gösterir."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1178c7a5db129801f83afa8b4caf9357ccf76b71
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-new-trade-agreement"></a>Yeni bir ticari sözleşme oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam belirli bir müşteri ile üzerinde anlaştığınız yeni bir ürün satış fiyatını kaydetmek için bir ticari sözleşmenin nasıl oluşturulacağını gösterir. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Eğer kendi verilerinizi kullanıyorsanız, bu kılavuz başlamadan önce varsayılan ilişkisi "Fiyat (satış)" olarak ayarlanan bir ticari sözleşmenin günlük adının var olduğundan emin olmanız gerekir.


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Yeni bir ticari sözleşme günlüğü oluşturun ve deftere nakledin.
1. Sales and marketing > Prices and discounts > Trade agreement journals (Satış ve pazarlama > Fiyatlar ve iskontolar > Ticari anlaşma günlükleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Satırlar seçeneğine tıklayın.
7. Hesap kodu alanında 'Tablo'yu seçin.
    * Bu örnekte, belirli bir müşteri için fiyat güncelleştirmesi yapıyorsunuz bu yüzden de Tablo seçmeniz lazım. Ürünün liste fiyatını güncelleştiriyor olsaydınız, yeni fiyatın tüm müşteriler için geçerli olmasını sağlamak için, Tümü seçeneğini seçecektiniz. Müşteri segmentleri arasında fiyat farklılaştırması yapacak olsaydınız, Grup seçeneğini seçmeniz gerekirdi. Grup'u seçmek için müşteri fiyat grupları ayarlamış olmanız gerekir.  
8. Hesap seçimi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, istenen kaydı bulun ve seçin.
10. Madde kodu alanında 'Tablo'yu seçin.
    * "Fiyat (satışlar)" türünde bir ticari anlaşmaya girecek olduğunuzda, madde kodu alanında sadece Tablo'yu seçmelisiniz. Bunun sebebi bir fiyatın mutlak değerde olmasıdır ve tüm ürünler veya ürün grupları için aynı olamayışıdır.  
11. Madde ilişkisi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
12. Listede, sözleşmeye dahil etmek istediğiniz ürünü seçin.
    * Hangi ürünü seçtiğinizi not alın.  
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. Başlangıç alanında bir minimum miktar girin.
    * Eğer müşterinin yeni bir fiyata hak kazanmadan önce sipariş etmesi gereken minimum bir miktar varsa, bu miktarı burada belirtin.  
    * Anlaşması fiyatının daha fazlasında geçerli olmayacağı bir maksimum miktar belirtmek için Bitiş alanına bir değer girin. Fiyatlar ve indirimleri temel alan birden fazla miktar kırılması sunacaksanız, her miktari aralığını bir çift minimum ve maksimum miktar olarak 'Başlangıç' ve 'Bitiş' alanları ile belirtin.  
15. Para birimi miktarı alanına bir fiyat girin.
16. Başlangıç tarihi alanına bu sözleşmenin geçerliliğin başlayacağı tarihi girin.
17. Kaydet'e tıklayın.
18. Doğrula'ya tıklayın.
19. Seçilen satırları doğrula'ya tıklayın.
20. Tamam'a tıklayın.
21. Deftere Naklet öğesine tıklayın.
22. Tamam'a tıklayın.

## <a name="view-trade-agreements-for-a-product"></a>Bir ürün için ticari sözleşmeleri görüntüleyin
1. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
2. Listede, fiyatını az önce güncelleştirdiğiniz ürünü bulun ve seçin.
3. Eylem Bölmesinde, Satış'a tıklayın.
4. Ticari sözleşmeleri görüntüle'ye tıklayın.
    * Yeni oluşturduğunuz fiyat ticari sözleşmesinin ayrıntılarını gözden geçirin.    
5. Sayfayı kapatın.



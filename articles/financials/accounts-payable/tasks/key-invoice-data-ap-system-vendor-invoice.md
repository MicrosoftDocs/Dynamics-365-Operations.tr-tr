--- 
title: "Satıcı faturası kullanarak fatura verilerini borç hesaplarına girme"
description: "Bu görev kılavuzu, bir satınalma siparişinden satıcı faturası oluşturmanıza ve satınalma siparişi, giriş ve fatura eşleştirme (3 yönlü eşleştirme) sonuçlarını görüntülemenize yardımcı olur."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a365c52af49a66d6af5bb38f0053bd9c0fd34301
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a>Satıcı faturası kullanarak fatura verilerini borç hesaplarına girme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu, bir satınalma siparişinden satıcı faturası oluşturmanıza ve satınalma siparişi, giriş ve fatura eşleştirme (3 yönlü eşleştirme) sonuçlarını görüntülemenize yardımcı olur.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Seçmek üzere bir satıcı bulun. Örneğin aşağıya kayarak ABD-104'e gelin.
5. Satıcı ABD-104'ü seçin.
6. Tamam'ı tıklatın.
7. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
8. Bir stok maddesi seçin. Örneğin, madde numarası olarak 1000 seçin.
9. Satır ayrıntıları bölümünü genişletin veya daraltın.
10. Kurulum sekmesine tıklayın.
    * Eşleştirme ilkesini eşleştirme kullanmamak, 2 yönlü eşleştirme ya da 3 yönlü eşleştirme kullanmak üzere geçersiz kılabilirsiniz.  
11. Satır ayrıntıları bölümünü genişletin veya daraltın.
12. Eylem Bölmesinde, Satınalma öğesine tıklayın.
13. Onayla seçeneğine tıklayın.

## <a name="receive-the-products"></a>Ürünleri alma
1. Eylem Bölmesinde, Al öğesine tıklayın.
2. Ürün girişi seçeneğine tıklayın.
3. Ürün girişi alanına ürün giriş numarasını girin. Örneğin PR123 yazın.
4. Ürün girişini deftere nakletmek için Tamam'a tıklayın.
5. Sayfayı kapatın.

## <a name="create-a-vendor-invoice"></a>Satıcı faturası oluşturma
1. Alacak hesapları > Satınalma siparişleri > Alınan ancak faturalanmayan satınalma siparişleri'ne gidin.
2. Oluşturduğunuz satınalma siparişini seçin.
3. Eylem Bölmesinde Fatura öğesine tıklayın.
4. Fatura'ya tıklayın.
5. Numara alanına fatura numarasını girin.
6. Fatura açıklaması alanına bir değer girin.
7. Fatura tarihi alanına bir tarih girin.
8. Birim fiyatı alanına 1200 yazın.
9. Satır ekle'ye tıklayın.
10. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
11. Listede kurulum masrafı madde numarasını bulun. Örneğin S0001
12. Kurulum masrafı madde numarasını seçin.
    * Yaptığınız değişikliklerden sonra eşleştirme yapılmadığına dikkat edin.  
13. Eşleştirme durumunu güncelleştir öğesine tıklayın.
14. Eylem Bölmesinde, Gözden geçir öğesine tıklayın.
15. Eşleşme ayrıntıları öğesine tıklayın.
    * Hizmetlerin bulunduğu yeni satırın eşleştirilmesi gerekmediği için durumu "Gerçekleştirilmedi" olarak kalır.  
16. Aldığınız stok maddesi için ürün girişini seçin.
    * Ürün girişini içeren satır eşleştirildi ancak miktar veya fiyat uyuşmazlığı olduğundan başarısız oldu.  
17. Birim fiyatı alanına bir sayı girin.
    * Artık birim fiyatı eşleştiğinden durum Başarılı olarak güncelleştirilir. İlkeniz uyuşmazlıklara izin veriyorsa veya eşleşme yalnızca bir uyarıysa, faturayı deftere nakledebilirsiniz.  
18. Sayfayı kapatın.
19. Deftere Naklet öğesine tıklayın.
20. Formu kapatın.
    * Satınalma siparişinin artık alındı ancak faturalanmadı olarak listelenmediğine dikkat edin.  



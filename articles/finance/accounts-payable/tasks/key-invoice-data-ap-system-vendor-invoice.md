---
title: Satıcı faturası kullanarak fatura verilerini AP'ye gir
description: Bu görev kılavuzu, bir satınalma siparişinden satıcı faturası oluşturmanıza ve satınalma siparişi, giriş ve fatura eşleştirme (3 yönlü eşleştirme) sonuçlarını görüntülemenize yardımcı olur.
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f80c88b7fb3542f624d233f670cd7cd6ccd48b94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448651"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>Satıcı faturası kullanarak fatura verilerini AP'ye gir

[!include [banner](../../includes/banner.md)]

Bu görev kılavuzu, bir satınalma siparişinden satıcı faturası oluşturmanıza ve satınalma siparişi, giriş ve fatura eşleştirme (3 yönlü eşleştirme) sonuçlarını görüntülemenize yardımcı olur.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. Gezinti bölmesinde **Modüller > Borç hesapları > Satınalma siparişleri > Tüm satın alma siparişleri** öpesine gidin.
2. **Yeni**'ye tıklayın.
3. **Satıcı hesabı** alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Seçmek üzere bir satıcı bulun. Örneğin aşağıya kayarak ABD-104'e gelin.
5. Satıcı ABD-104'ü seçin.
6. **Tamam**'a tıklayın.
7. **Madde numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.
8. Bir stok maddesi seçin. Örneğin, madde numarası olarak 1000 seçin.
9. **Satır ayrıntıları** hızlı sekmesini genişletin.
10. **Kurulum** sekmesine tıklayın. Eşleştirme ilkesini eşleştirme kullanmamak, 2 yönlü eşleştirme ya da 3 yönlü eşleştirme kullanmak üzere geçersiz kılabilirsiniz.  
11. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
12. **Onayla**'yı tıklatın.

## <a name="receive-the-products"></a>Ürünleri alma
1. Eylem Bölmesinde, **Teslim al** öğesine tıklayın.
2. **Ürün girişi** öğesine tıklayın.
3. **Ürün girişi** alanına ürün giriş numarasını girin. Örneğin PR123 yazın.
4. Ürün girişini deftere nakletmek için **Tamam**'a tıklayın.
5. Sayfayı kapatın.

## <a name="create-a-vendor-invoice"></a>Satıcı faturası oluşturma
1. Gezinti bölmesinde **Modüller > Borç hesapları > Satınalma siparişleri > Alınan ancak faturalanmayan satınalma siparişleri** öğesine gidin.
2. Oluşturduğunuz satınalma siparişini seçin.
3. Eylem Bölmesinde **Fatura** öğesine tıklayın.
4. **Fatura** öğesine tıklayın.
5. **Numara** alanına fatura numarasını girin.
6. **Fatura açıklaması** alanına bir değer girin.
7. **Fatura tarihi** alanına bir tarih girin.
8. **Birim fiyatı** alanına 1200 yazın.
9. **Satır ekle**'ye tıklayın.
10. **Madde numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.
11. Listede kurulum masrafı madde numarasını bulun. Örneğin S0001
12. Kurulum masrafı madde numarasını seçin. Yaptığınız değişikliklerden sonra eşleştirme yapılmadığına dikkat edin.  
13. **Eşleştirme durumunu güncelleştir**'e tıklayın.
14. Eylem Bölmesinde, **Gözden geçir** öğesine tıklayın.
15. **Eşleşme ayrıntıları** öğesine tıklayın. Hizmetlerin bulunduğu yeni satırın eşleştirilmesi gerekmediği için durumu "Gerçekleştirilmedi" olarak kalır.  
16. Aldığınız stok maddesi için ürün girişini seçin. Ürün girişini içeren satır eşleştirildi ancak miktar veya fiyat uyuşmazlığı olduğundan başarısız oldu.  
17. **Birim fiyatı** alanına bir sayı girin. Artık birim fiyatı eşleştiğinden durum Başarılı olarak güncelleştirilir. İlkeniz uyuşmazlıklara izin veriyorsa veya eşleşme yalnızca bir uyarıysa, faturayı deftere nakledebilirsiniz.  
18. Sayfayı kapatın.
19. **Naklet**'e tıklayın.
20. Formu kapatın. Satınalma siparişinin artık alındı ancak faturalanmadı olarak listelenmediğine dikkat edin.  


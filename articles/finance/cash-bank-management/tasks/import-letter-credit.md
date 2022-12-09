---
title: İthalat kredi mektubu
description: Bu yordam, bir kredi mektubunun içeri alınması sürecini adım adım anlatır.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a79b3c391c15099aee0a8d34419e1cf48fafbc
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804004"
---
# <a name="import-letter-of-credit"></a>İthalat kredi mektubu

[!include [banner](../../includes/banner.md)]

Bu yordam, bir kredi mektubunun içeri alınması sürecini adım adım anlatır. Bu yöntemi tamamlamadan önce aşağıdakiler ayarlanmış olmalıdır: Banka tesisleri, deftere nakil profilleri, bir banka tesisi anlaşması ve satıcı bankası.

Bu yordam, USMF demo şirketini kullanır.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Akreditif Mektubu ile satınalma siparişi oluşturma
1. **Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri**'ne gidin.
2. **Yeni**'yi tıklatın.
3. **Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **Genel** bölümünü genişletin.
7. **Tesis** alanına bir değer girin veya buradan bir değer seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. **Ambar** alanında bir değer girin veya bir değer seçin.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. **Muhasebe tarihi** alanına bir tarih girin.
12. **Teslimat tarihi** alanına bir tarih girin.

>[!Note] 
>**Banka belge türü** alanında **Kredi mektubu** seçilmelidir.  

13. **Tamam**'a tıklayın.
14. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
15. Listede, istenen kaydı bulun ve seçin.
16. Listede, seçili satırdaki bağlantıya tıklayın.
17. **Satır ayrıntıları** bölümünü genişletin.
18. **Teslimat** sekmesine tıklayın.
19. **Teslimat tarihi** alanına bir tarih girin.
20. **Teyit edilmiş teslimat tarihi** alanına bir tarih girin.
21. **Birim fiyatı** alanına bir sayı girin.
    * Kredi mektubunun ayrıntılarını tanımlayın.  
22. Eylem Bölmesi'nde **Yönet**'e tıklayın.
23. **Kredi mektubu/ithalat tahsilatı**'na tıklayın.
24. **Uygulama tarihi** alanına bir tarih ve saat girin.
    * **Banka hesabı** alanının, uygulama tarihini baz alan, varsayılan etkin banka hesabı değerinde olduğunu doğrulayın.  
25. **Banka belgesi numarası** alanına bir değer girin.
26. **Teslim alma tarihi** alanına bir tarih ve saat girin.
27. **Banka belgesi** bölümünü genişletin.
28. **Bitiş tarihi** alanına bir tarih ve saat girin.
29. **Banka ayrıntıları** bölümünü genişletin.
30. **Muhbir banka** alanına bir değer girin veya buradan bir değer seçin.
31. Listede, seçili satırdaki bağlantıya tıklayın.
32. **Kaydet**'e tıklayın.
33. **Satınalma siparişi sevkiyatlarını al**'a tıklayın.
34. Sayfayı kapatın.
35. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
36. **Onayla**'yı tıklatın.
37. Eylem Bölmesi'nde **Yönet**'e tıklayın.
38. **Kredi mektubu/ithalat tahsilatı**'na tıklayın.
39. **İşle**'ye tıklayın.
40. **Onayla**'yı tıklatın.
    * Tesis bakiyesinin satın alma sipariş miktarını azalttığını doğrulayın. Bu örnekte, satın alma tutarı = 500,00,  tesis sınırı 10000,00,  bu nedenle, tesis Bakiyesi = 9500,00 =.  
41. Sayfayı kapatın.
42. **Birim fiyatı** alanına bir sayı girin.
43. **Kaydet**'e tıklayın.
44. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
45. **Onayla**'yı tıklatın.
    * Birim fiyat değişikliği nedeniyle kredi mektubunu düzeltin.  
46. Eylem Bölmesi'nde **Yönet**'e tıklayın.
47. **Kredi mektubu/ithalat tahsilatı**'na tıklayın.
    * Akreditif Mektubunu, Satınalma birim fiyatı değişikliği nedeniyle düzeltmek.  
48. **İşle**'ye tıklayın.
49. **Düzelt**'e tıklayın.
50. **Kaldır**'a tıklayın.
51. **Evet** seçeneğini tıklatın.
52. **Satınalma siparişi sevkiyatlarını al**'a tıklayın.
53. **İşle**'ye tıklayın.
54. **Onayla**'yı tıklatın.
    * Tesis bakiyesinin satın alma sipariş miktarını azalttığını doğrulayın. Bu örnekte, değiştirilmiş satın alma tutarı = 600,00,  tesis sınırı 10000,00,  bu nedenle, tesis Bakiyesi = 9400,00 =  
55. Sayfayı kapatın.

## <a name="post-packing-slip"></a>Sevk irsaliyesini deftere naklet
1. Eylem Bölmesinde, **Teslim al** öğesine tıklayın.
2. **Ürün girişi** öğesine tıklayın.
3. **PurchParmTable_Num** alanına bir değer yazın.
    * Kredi mektubuna ilişkin oluşturulan **Sevkiyat numarasını** seçin.  
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. **Ürün giriş tarihi** alanına bir tarih girin.
6. **Tamam**'a tıklayın.
7. Sayfayı kapatın.
8. Sayfayı kapatın.

## <a name="verify-import-letter-of-credit-status"></a>İthalat kredi mektubunun durumunu onaylayın.
1. **Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı**'na tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * **İthalat kredi mektubu durumunu** onaylayın.     
4. Sayfayı kapatın.
5. Sayfayı kapatın.

## <a name="post-purchase-invoice"></a>Satınalma faturasını deftere naklet
1. **Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri**'ne gidin.
    * Kredi mektubu ile oluşturulan satınalma siparişini seçin.  
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Eylem Bölmesinde **Fatura** öğesine tıklayın.
5. **Fatura** öğesine tıklayın.
6. **Numara** alanına bir değer girin.
7. **Sevkiyat numarası** alanına bir değer girin veya buradan bir değer seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. **Fatura tarihi** alanına bir tarih girin.
10. **Eşleştirme durumunu güncelleştir**'e tıklayın.
11. **Naklet**'e tıklayın.
12. Sayfayı kapatın.
13. Sayfayı kapatın.

## <a name="verify-import-letter-of-credit-status-and-printing"></a>İthalat kredi mektubunun durumunu ve yazdırmayı onaylama

1. **Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı**'na tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * İthalat kredi mektubu2'yi doğrulayın.  
    * Doğrula:  **Sevkiyat durumu** = **Faturalandı**  Banka tesisi ayrıntıları  
4. **Görüntüle**'ye tıklayın.
5. **Başvuruyu yazdır**'a tıklayın.
6. **Tamam**'a tıklayın.
    * Akreditif Mektubu uygulama yazdırılmaz doğrulayın.  
7. Sayfayı kapatın.
8. Sayfayı kapatın.
9. Sayfayı kapatın.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Kredi mektubu ile oluşturulmuş satınalma faturası için satıcı ödeme günlüğünü deftere naklet
1. **Borç hesapları > Ödemeler > Ödeme günlüğü'ne** gidin.
2. **Yeni**'yi tıklatın.
3. **Ad** alanına bir değer girin veya buradan bir değer seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. **Satırlar**'a tıklayın.
6. **Tarih** alanına bir tarih girin.
7. **Hesap** alanında istediğiniz değerleri belirtin.
8. **Hareketleri kapat**'a tıklayın.
9. **Toplamlar** bölümünü genişletin.
10. **Göster** alanında, bir seçenek seçin.
    * **Banka belge numarası** ve **Sevkiyat numarası** alanlarının güncelleştirildiğini doğrulayın.  
11. **İşaretle** onay kutusunu seçin.
12. **Tamam**'a tıklayın.
13. Ödeme sekmesine tıklayın.
    * **Banka belge numarası** ve **Sevkiyat numarası** alanlarının güncelleştirildiğini doğrulayın.  
14. **Naklet**'e tıklayın.
15. Sayfayı kapatın.
16. Sayfayı kapatın.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Öndemiş faturadan sonra Kredi Mektubu durumunu doğrulayın.
1. **Nakit ve Banka yönetimi > Kredi mektupları > İthalat Kredi Mektubu ve İthalat Tahsilatı**'na tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * **İthalat kredi mektubu durumunu** onaylayın.   
4. Sayfayı kapatın.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Banka hizmet limiti ve kullanım raporu doğrula
1. **Nakit ve Banka yönetimi > Sorgular ve raporlar > Kredi veya teminat mektupları > Banka tesisleri ve kullanım raporu**'na gidin.
2. **Eklenecek kayıtlar** bölümünü genişletin.
3. **Filtrele** öğesine tıklayın.
    * Gerekli banka hesabıyla ilgili **Ölçüt** alanını tanımlayın.  
4. **Ölçütler** alanında bir değer girin veya seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **Tamam**'a tıklayın.
7. **Tamam**'a tıklayın.
    * Hareketleri listeleyen raporu doğrulayın.  
    * Hareketleri banka belge numarası, tesis sınırı, kullanılan tutar ve tesis bakiye tutarı ile rapor listeleri doğrulayın.  
8. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Kredi mektubunu dışa aktar
description: Bu yordam, bir ihracat kredi mektubu sürecini adım adım anlatır.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779567"
---
# <a name="export-letter-of-credit"></a>Kredi mektubunu dışa aktar

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ihracat kredi mektubu sürecini adım adım anlatır.

Bir kredi mektubu, bir banka tarafından verilen ve bu bankanın, alıcı ve satıcı arasındaki sözleşmenin koşullarını yerine getirilirse, alıcı adına ödeme yapmayı kabul ettiği bir anlaşmadır.



Bu yordamdan önce **Kredi Mektubu_Banka tesisi anlaşması yarat** yordamını ve **Banka tesisleri ve nakil profilleri ayarlama** yordamını çalıştırın. Bu yordamın başarıyla çalışması için, USMF demo şirketi seçili olmalıdır.


## <a name="create-sales-order-for-export-letter-of-credit"></a>İhraç kredi mektubu için satış siparişi oluşturma
1. **Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi tıklatın.
3. **Müşteri hesabı** alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **Genel** bölümünü genişletin veya daraltın.
7. **Site** alanında, aramayı açmak için aşağı açılır düğmeyi tıklayın.
    * Çıkarılcak maddenin stoğunun tutulduğu **Tesis**'i seçin.  
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. **Ambar** alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Çıkarılacak maddenin stoğunun tutulduğu **Ambar**'ı seçin.  
10. Listede, seçili satırdaki bağlantıya tıklayın.
    * Not: **Banka belge türü** alanında **Kredi Mektubu** değerinin seçilmesi gerekir.  
11. **Banka belge türü** alanında **Kredi Mektubu**'nu seçin.
12. **Teslimat** bölümünü genişletin veya daraltın.
    * **Teslimat tarihi kontrolü** = **Yok** olarak seçin.  
13. **Talep edilen teslim alma tarihi** alanına bir tarih girin.
14. **Tamam**'a tıklayın.
15. **Madde numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Verilmek/Satılmak için gerekli maddeyi seçin.  
16. Listede, istenen kaydı bulun ve seçin.
17. Listede, seçili satırdaki bağlantıya tıklayın.
18. **Birim fiyatı** alanına bir sayı girin.
19. **Satır ayrıntıları** bölümünü genişletin veya daraltın.
20. **Teslimat** sekmesine tıklayın.
21. **Talep edilen sevk tarihi** alanına bir tarih girin.
22. **Onaylanan sevk tarihi** alanına bir tarih girin.
23. Eylem Bölmesi'nde **Yönet**'e tıklayın.
24. **Kredi mektubu**'na tıklayın.
25. **Banka belgesi numarası** alanına bir değer girin.
26. **Bitiş tarihi** alanına bir tarih ve saat girin.
27. **Banka detayları** bölümünü genişletin veya daraltın.
28. **Veren banka** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
29. Listede, seçili satırdaki bağlantıya tıklayın.
30. **Muhabir banka** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
31. Listede, istenen kaydı bulun ve seçin.
32. Listede, seçili satırdaki bağlantıya tıklayın.
33. **Satış siparişi sevkiyatlarını al**'a tıklayın.
34. **Banka belgesini yayımla**'ya tıklayın.
35. Sayfayı kapatın.

## <a name="post-packing-slip"></a>Sevk irsaliyesini deftere naklet
1. Eylem Bölmesi'nde **Çek ve paketle**'ye tıklayın.
2. **Sevk irsaliyesini deftere naklet**'e tıklayın.
3. **Parametreler** bölümünü genişletin veya daraltın.
4. **Miktar** alanında **Tümü** seçeneğini seçin.
5. **Kurulum** bölümünü genişletin veya daraltın.
6. **Sevk irsaliyesi tarihi** alanına bir tarih girin.
7. Sevkiyat numarasını seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. **Tamam**'a tıklayın.
10. **Tamam**'a tıklayın.

## <a name="post-sales-invoice"></a>Satış faturası deftere nakletme
1. Eylem Bölmesinde **Fatura** öğesine tıklayın.
2. **Fatura** öğesine tıklayın.
3. **Genel bakış** bölümünü genişletin veya daraltın.
4. **Sevkiyat numarasını** seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **Kurulum** bölümünü genişletin veya daraltın.
7. **Fatura tarihi** alanına bir tarih girin.
8. **Tamam**'a tıklayın.
9. **Tamam**'a tıklayın.

## <a name="shipment-document-submitted-status"></a>Sevkiyat belgeleri gönderim durumu
1. Eylem Bölmesi'nde **Yönet**'e tıklayın.
2. **Kredi mektubu**'na tıklayın.
3. **Satırlar** bölümünü genişletin veya daraltın.
    * Not: **Gönderilen belge** alanı **Evet** olarak ayarlanmalıdır.  

## <a name="verify-export-letter-of-credit"></a>İhracat kredi mektubunu onaylayın
1. **Nakit ve Banka yönetimi > Kredi mektupları > İhracat Kredi Mektubu ve İthalat Tahsilatı**'na tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * **İhracat kredi mektubu** **sevkiyat durumunun** **Faturalandı** olduğunu doğrulayın.  

## <a name="customer-payment"></a>Müşteri ödemesi
1. **Alacak hesapları > Ödemeler > Ödeme günlüğü**'ne gidin.
2. **Yeni**'yi tıklatın.
3. Listede, seçili satırı işaretleyin.
4. **Ad** alanında, açılır menü düğmesine tıklayarak aramayı açın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **Satırlar**'a tıklayın.
7. **Tarih** alanına bir tarih girin.
8. **Hesap** alanında istediğiniz değerleri belirtin.
9. **Kapatma** öğesine tıklayın.
10. Toplam başlığındaki onay kutusunu seçin.
    * Not: **Göster** alanını **Kredi mektubu** olarak ayarlayın.  
11. Listede, istenen kaydı bulun ve seçin.
12. **İşaretle** onay kutusunu seçin veya temizleyin.
13. **Tamam**'a tıklayın.
14. **Ödeme** sekmesine tıklayın.
    * Banka belge numarası ve sevk irsaliyesi numarası ayrıntılarını doğrulayın  
15. **Naklet**'e tıklayın.

## <a name="verify-export-letter-of-credit-after-payment"></a>İhracat kredi mektubunu ödeme sonrasında doğrulayın
1. **Nakit ve Banka yönetimi > Kredi mektupları > İhracat Kredi Mektubu ve İthalat Tahsilatı**'na tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * **Sevkiyat durumu** = **Ödeme alındı** ve **Bakiye tutarı** = **0,00** olduğunu doğrulayın.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

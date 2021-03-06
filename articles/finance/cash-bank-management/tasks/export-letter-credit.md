---
title: Kredi mektubunu dışa aktar
description: Bu yordam, bir ihracat kredi mektubu sürecini adım adım anlatır.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 260ef2d05e1f21708817346af2db2841aa6acdd9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834800"
---
# <a name="export-letter-of-credit"></a>Kredi mektubunu dışa aktar

[!include [banner](../../includes/banner.md)]

Bu yordam, bir ihracat kredi mektubu sürecini adım adım anlatır.

Bir kredi mektubu, bir banka tarafından verilen ve bu bankanın, alıcı ve satıcı arasındaki sözleşmenin koşullarını yerine getirilirse, alıcı adına ödeme yapmayı kabul ettiği bir anlaşmadır.



'Önce 'Kredi Mektubu_Banka tesisi anlaşması yarat' yordamını, daha sonra da 'Banka tesisleri ve nakil profillerini ayarlama' yordamını çalıştırın. Bu yordamın başarıyla çalışması için, USMF demo şirketi seçili olmalıdır.




## <a name="create-sales-order-for-export-letter-of-credit"></a>İhraç kredi mektubu için satış siparişi oluşturma
1. Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Genel bölümünü genişletin veya daraltın.
7. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * İhraç edilecek maddenin stoğunun nerede tutulduğunu seçin.  
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * İhraç edilecek maddenin stoğunun hangi ardiye tutulduğunu seçin.  
10. Listede, seçili satırdaki bağlantıya tıklayın.
    * Not: 'Banka belge türü' alanında 'Kredi Mektubu' değerinin seçilmesi gerekir.  
11. Banka belge türü alanında Kredi Mektubu'nu seçin.
12. Teslimat bölümünü genişletin veya daraltın.
    * Teslimat tarihi kontrolünü seçin = Yok.  
13. Talep edilen teslim alma tarihi alanına bir tarih girin.
14. Tamam'a tıklayın.
15. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Verilmek/Satılmak için gerekli maddeyi seçin.  
16. Listede, istenen kaydı bulun ve seçin.
17. Listede, seçili satırdaki bağlantıya tıklayın.
18. Birim fiyatı alanına bir sayı girin.
19. Satır ayrıntıları bölümünü genişletin veya daraltın.
20. Teslimat sekmesini tıklatın.
21. Talep edilen sevk tarihi alanına bir tarih girin.
22. Teyit edilen sevk tarihi alanına bir tarih girin.
23. Eylem Bölmesinde, Yönet'i tıklatın.
24. Kredi mektubu'na tıklayın.
25. Banka belgesi numarası alanına bir değer girin.
26. Bitiş tarihi alanına bir tarih ve saat girin.
27. Banka detayları bölümünü genişletin veya daraltın.
28. Amir banka alanında, aramayı açmak için açılır menü düğmesine tıklayın.
29. Listede, seçili satırdaki bağlantıya tıklayın.
30. Muhabir banka alanında, aramayı açmak için açılır menü düğmesine tıklayın.
31. Listede, istenen kaydı bulun ve seçin.
32. Listede, seçili satırdaki bağlantıya tıklayın.
33. Satış siparişi sevkiyatlarını al'a tıkla.
34. Banka belgesini yayımla'ya tıkla.
35. Sayfayı kapatın.

## <a name="post-packing-slip"></a>Sevk irsaliyesini deftere naklet
1. Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.
2. Sevk irsaliyesini deftere naklet öğesine tıklayın.
3. Parametreler bölümünü genişletin veya daraltın.
4. Miktar alanında 'Tümü'nü seçin.
5. Kurulum bölümünü genişletin veya daraltın.
6. Sevk irsaliyesi tarihi alanına bir tarih girin.
7. Sevkiyat numarasını seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Tamam'a tıklayın.
10. Tamam'a tıklayın.

## <a name="post-sales-invoice"></a>Satış faturası deftere nakletme
1. Eylem Bölmesinde, Fatura öğesine tıklayın.
2. Fatura'ya tıklayın.
3. Genel bakış bölümünü genişletin veya daraltın.
4. Sevkiyat numarasını seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Kurulum bölümünü genişletin veya daraltın.
7. Fatura tarihi alanına bir tarih girin.
8. Tamam'a tıklayın.
9. Tamam'a tıklayın.

## <a name="shipment-document-submitted-status"></a>Sevkiyat belgeleri gönderim durumu
1. Eylem Bölmesinde, Yönet'i tıklatın.
2. Kredi mektubu'na tıklayın.
3. Satırlar bölümünü genişletin veya daraltın.
    * Not: 'Gönderilen belge' alanı 'Evet' olarak ayarlanmalıdır.  

## <a name="verify-export-letter-of-credit"></a>İhracat kredi mektubunu onaylayın
1. Nakit ve Banka yönetimi > Kredi mektupları > İhracat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * Ihracat kredi mektubu sevkiyat durumunun 'Faturalandı' olduğunu doğrulayın.  

## <a name="customer-payment"></a>Müşteri ödemesi
1. Alacak hesapları > Ödemeler > Ödeme günlüğü'ne gidin.
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Satırlar seçeneğini tıklatın.
7. Tarih alanına bir tarih girin.
8. Hesap alanında istediğiniz değerleri belirtin.
9. Kapatma öğesini tıklatın.
10. Toplam başlığındaki onay kutusunu seçin.
    * Not: Göster alanını 'Kredi mektubu' olarak ayarlayın.  
11. Listede, istenen kaydı bulun ve seçin.
12. İşaret onay kutusunu seçin veya temizleyin.
13. Tamam'a tıklayın.
14. Ödeme sekmesine tıklayın.
    * Banka belge numarası ve sevk irsaliyesi numarası ayrıntılarını doğrulayın  
15. Deftere Naklet öğesine tıklayın.

## <a name="verify-export-letter-of-credit-after-payment"></a>İhracat kredi mektubunu ödeme sonrasında doğrulayın
1. Nakit ve Banka yönetimi > Kredi mektupları > İhracat Kredi Mektubu ve İthalat Tahsilatı'na tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * Sevkiyat durumu'nun = Ödeme alındı ve bakiye tutarı'nın = 0,00 olduğunu doğrulayın.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
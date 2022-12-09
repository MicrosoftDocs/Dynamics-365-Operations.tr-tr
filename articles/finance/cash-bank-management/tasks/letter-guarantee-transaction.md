---
title: Teminat mektubu hareketi
description: Bu yöntem Teminat Mektubu sürecini anlatmaktadır.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 786aecf69bae3d07ac80a55b4dc835dd8129bd59
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803977"
---
# <a name="letter-of-guarantee-transaction"></a>Teminat mektubu hareketi

[!include [banner](../../includes/banner.md)]

Bu yöntem Teminat Mektubu sürecini anlatmaktadır.



Bu yordamı tamamlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir:

- Teminat mektubu için banka tesisleri ve deftere nakil profilleri ayarlama.

- Teminat mektubu için banka tesisi anlaşması oluşturun.



Bu yordam, USMF demo şirketini kullanır.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Teminat mektubu ile satış emri yaratın
1. **Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi tıklatın.
3. **Müşteri hesabı** alanında bir değer girin veya seçin.
4. **Genel** bölümünü genişletin.
5. **Tesis** alanına bir değer girin veya buradan bir değer seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. **Ambar** alanında bir değer girin veya bir değer seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. **Banka belge türü** alanında **Teminat Mektubu**'nu seçin.
10. **Tamam**'a tıklayın.
11. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
12. **Birim fiyatı** alanına bir sayı girin.
13. **Satır ayrıntıları** bölümünü genişletin.
14. **Teslimat** sekmesine tıklayın.

>[!Note] 
>**Teslimat tarihi kontrolü** = **Yok** olarak seçin  

15. **Talep edilen sevk tarihi** alanına bir tarih girin.
16. **Onaylanan sevk tarihi** alanına bir tarih girin.

## <a name="process-letter-of-guarantee_request"></a>Teminat mektubu isteği işlemden geçirin.
1. Eylem Bölmesi'nde **Yönet**'e tıklayın.
2. **Teminat mektubu**'na tıklayın.
3. Eylem bölmesinde, **Teminat mektubu**'na tıklayın.
4. İletişim kutusu formunu açmak için **Talep** seçeneğine tıklayın.
5. **Tür** alanına bir değer girin veya buradan bir değer seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. **Değer** alanına bir sayı girin.
8. **Bitiş tarihi** alanına bir tarih ve saat girin.
9. **Tamam**'a tıklayın.
10. Sayfayı kapatın.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Teminat mektubunu bankaya işleyin bankaya gönderin
1. **Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları** öğesine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. **Bankaya gönder** iletişim kutusunu açmak için tıklayın.
4. **Banka hesabı** alanında bir değer girin veya seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **Tamam**'a tıklayın.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Bankadan teminat mektubunu alın işleyin
1. **Bankadan al** iletişim kutusunu açmak için tıklayın.
2. **Banka numarası** alanına alanına bir değer girin.
    * Hesaplanan **Marj** ve **Gider** alanlarını doğrulayın.  
3. **Tamam**'a tıklayın.
4. **Eylemler** bölümünü genişletin.
    * 'Bankadan alma' kaydını doğrulayın.  
5. **Günlük toplu iş numarası** alanındaki bağlantıyı izlemek için tıklayın.
6. **Satırlar**'a tıklayın.
    * Günlük girişlerinin kaydını doğrulayın.  
7. Sayfayı kapatın.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Teminat mektubu lehtara vermeyi işleyin
1. **Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
3. Eylem Bölmesi'nde **Yönet**'e tıklayın.
4. **Teminat mektubu**'na tıklayın.
5. Eylem bölmesinde, **Teminat mektubu**'na tıklayın.
6. **Lehtara gönder** iletişim kutusunu açmak için tıklayın.
7. **Tamam**'a tıklayın.
8. **Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları** öğesine gidin.
9. Listede, istenen kaydı bulun ve seçin.
10. **Lehtara gönder** iletişim kutusunu açmak için tıklayın.
11. **Tamam**'a tıklayın.
12. **Eylemler** bölümünü genişletin.
    * 'Lehtara ver' kaydını doğrulayın.  

## <a name="process-letter-of-guarantee_increase-value"></a>Teminat mektubunun değerini artırmayı işleyin
1. **Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
3. Eylem Bölmesi'nde **Yönet**'e tıklayın.
4. **Teminat mektubu**'na tıklayın.
5. Eylem bölmesinde, **Teminat mektubu**'na tıklayın.
6. **Değeri artır** iletişim kutusunu açmak için tıklayın.
7. **Eklenecek değer** alanına bir numara girin.
8. **Tamam**'a tıklayın.
9. **Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları** öğesine gidin.
10. Listede, istenen kaydı bulun ve seçin.
11. **Değeri artır** iletişim kutusunu açmak için tıklayın.
12. **Tamam**'a tıklayın.
13. **Eylemler** bölümünü genişletin.
    * 'Değer artır' kaydını doğrulayın.  
14. Listede, istenen kaydı bulun ve seçin.
15. **Günlük toplu iş numarası** alanındaki bağlantıyı izlemek için tıklayın.
16. **Satırlar**'a tıklayın.
    * Mevcut günlük girişlerinin kaydını doğrulayın.  

## <a name="process-letter-of-guarantee_liquidate"></a>Teminat mektubunu nakde çevirmeyi işleyin
1. **Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
3. Eylem Bölmesi'nde **Yönet**'e tıklayın.
4. **Teminat mektubu**'na tıklayın.
5. Eylem bölmesinde, **Teminat mektubu**'na tıklayın.
6. **Nakte çevir** iletişim kutusunu açmak için tıklayın.
7. **Tamam**'a tıklayın.
8. **Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları** öğesine gidin.
9. Listede, istenen kaydı bulun ve seçin.
10. **Nakte çevir** iletişim kutusunu açmak için tıklayın.
11. **Tamam**'a tıklayın.
12. **Eylemler** bölümünü genişletin.
    * 'Nakte çevirme' kaydını doğrulayın.  
13. Listede, istenen kaydı bulun ve seçin.
14. **Günlük toplu iş numarası** alanındaki bağlantıyı izlemek için tıklayın.
15. **Satırlar**'a tıklayın.
    * Mevcut günlük girişlerinin kaydını doğrulayın.  
16. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

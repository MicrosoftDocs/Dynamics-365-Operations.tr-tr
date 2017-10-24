--- 
title: Teminat mektubu hareketi
description: "Bu yöntem Teminat Mektubu sürecini anlatmaktadır."
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c2e215f1ae16f907c8b64ea1f05cf67bfb0a04b6
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="letter-of-guarantee-transaction"></a>Teminat mektubu hareketi

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yöntem Teminat Mektubu sürecini anlatmaktadır.



Bu yordamı tamamlamadan önce aşağıdaki görevlerin tamamlanması gerekmektedir:

- Teminat mektubu için banka tesisleri ve deftere nakil profilleri ayarlama.

- Teminat mektubu için banka tesisi anlaşması oluşturun.



Bu yordam, USMF demo şirketini kullanır.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Teminat mektubu ile satış emri yaratın
1. Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer girin veya seçin.
4. Genel bölümünü genişletin.
5. Tesis alanına bir değer girin veya buradan bir değer seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Ambar alanında bir değer girin veya bir değer seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Banka belge türü alanında Teminat Mektubu'nu seçin.
10. Tamam'ı tıklatın.
11. Madde numarası alanında bir değer girin veya seçin.
12. Birim fiyatı alanına bir sayı girin.
13. Satır ayrıntıları bölümünü genişletin.
14. Teslimat sekmesine tıklayın.
    * Not: Teslimat tarihi kontrolünü seçin = Yok  
15. Talep edilen sevk tarihi alanına bir tarih girin.
16. Teyit edilen sevk tarihi alanına bir tarih girin.

## <a name="process-letter-of-guaranteerequest"></a>Teminat mektubu isteği işlemden geçirin.
1. Eylem Bölmesinde, Yönet'i tıklatın.
2. Teminat mektubuna tıklayın.
3. Eylem bölmesinde, teminat mektubuna tıklayın.
4. İletişim kutusu formunu açmak için talep seçeneğine tıklayın.
5. Tür alanına bir değer girin veya buradan bir değer seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Değer alanına bir sayı girin.
8. Bitiş tarihi alanına bir tarih ve saat girin.
9. Tamam'a tıklayın.
10. Sayfayı kapatın.

## <a name="process-letter-of-guaranteesubmit-to-bank"></a>Teminat mektubunu bankaya işleyin bankaya gönderin
1. Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Bankaya gönder kutusunu açmak için tıklayın.
4. Banka hesabı alanında bir değer girin veya seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Tamam'a tıklayın.

## <a name="process-letter-of-guaranteereceive-from-bank"></a>Bankadan teminat mektubunu alın işleyin
1. Bankadan al kutusunu açmak için tıklayın.
2. Banka numarası alanına alanına bir değer girin.
    * Hesaplanan marj ve gider alanları doğrulayın.  
3. Tamam'a tıklayın.
4. Eylemler bölümünü genişletin.
    * 'Bankadan alma' kaydını doğrulayın.  
5. Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.
6. Satırlar seçeneğine tıklayın.
    * Günlük girişlerinin kaydını doğrulayın.  
7. Sayfayı kapatın.

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a>Teminat mektubu lehtara vermeyi işleyin
1. Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
3. Eylem Bölmesinde, Yönet'i tıklatın.
4. Teminat mektubuna tıklayın.
5. Eylem bölmesinde, teminat mektubuna tıklayın.
6. Tahsildara gönder kutusunu açmak için tıklayın.
7. Tamam'a tıklayın.
8. Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.
9. Listede, istenen kaydı bulun ve seçin.
10. Tahsildara gönder kutusunu açmak için tıklayın.
11. Tamam'a tıklayın.
12. Eylemler bölümünü genişletin.
    * 'Lehtara ver' kaydını doğrulayın.  

## <a name="process-letter-of-guaranteeincrease-value"></a>Teminat mektubunun değerini artırmayı işleyin
1. Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
3. Eylem Bölmesinde, Yönet'i tıklatın.
4. Teminat mektubuna tıklayın.
5. Eylem bölmesinde, teminat mektubuna tıklayın.
6. Değeri artır kutusu formunu açmak için tıklayın
7. Eklenecek alanına bir numara girin.
8. Tamam'a tıklayın.
9. Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.
10. Listede, istenen kaydı bulun ve seçin.
11. Değeri artır kutusu formunu açmak için tıklayın
12. Tamam'a tıklayın.
13. Eylemler bölümünü genişletin.
    * 'Değer artır' kaydını doğrulayın.  
14. Listede, istenen kaydı bulun ve seçin.
15. Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.
16. Satırlar seçeneğine tıklayın.
    * Mevcut günlük girişlerinin kaydını doğrulayın.  

## <a name="process-letter-of-guaranteeliquidate"></a>Teminat mektubunu nakde çevirmeyi işleyin
1. Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.
2. Listede, seçili satırdaki bağlantıya tıklayın.
3. Eylem Bölmesinde, Yönet'i tıklatın.
4. Teminat mektubuna tıklayın.
5. Eylem bölmesinde, teminat mektubuna tıklayın.
6. Nakte çevir kutusu formunu açmak için tıklayın.
7. Tamam'a tıklayın.
8. Nakit ve Banka yönetimi > Teminat mektupları > Teminat mektupları seçeneğine gidin.
9. Listede, istenen kaydı bulun ve seçin.
10. Nakte çevir kutusu formunu açmak için tıklayın.
11. Tamam'a tıklayın.
12. Eylemler bölümünü genişletin.
    * 'Nakte çevirme' kaydını doğrulayın.  
13. Listede, istenen kaydı bulun ve seçin.
14. Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.
15. Satırlar seçeneğine tıklayın.
    * Mevcut günlük girişlerinin kaydını doğrulayın.  
16. Sayfayı kapatın.



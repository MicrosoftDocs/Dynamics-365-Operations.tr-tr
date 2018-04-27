--- 
title: "Müşteri için silme günlüğü oluşturma"
description: "Bu görev kılavuzunda, silme işlemleri parametrelerinin ve ardından silme hareketlerinin Tahsilatlar sayfasından, Açık müşteri faturaları sayfasından ve Müşteri sayfasından nasıl ayarlanacağını göreceksiniz."
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 19a816f04283ce4f200de7396617313e45e057db
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-write-off-journal-for-a-customer"></a>Müşteri için silme günlüğü oluşturma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzunda, silme işlemleri parametrelerinin ve ardından silme hareketlerinin Tahsilatlar sayfasından, Açık müşteri faturaları sayfasından ve Müşteri sayfasından nasıl ayarlanacağını göreceksiniz. Bu görevde USMF demo şirketi kullanılmaktadır.


## <a name="set-up-the-write-off-parameters"></a>Silme parametrelerini ayarlayın
1. Alacak ve tahsilatlar > Kurulum > Alacak hesapları parametreleri'ne gidin.
2. Tahsilatlar sekmesine tıklayın.
3. Silme bölümünü genişletin veya daraltın.
    * Silme günlüğü, oluşturduğunuz silme hareketlerini tutan yevmiye defteridir.  
    * Her silme işlemine bir neden kodu ekleyebilirsiniz. Bu varsayılan değeri silme işlemi sırasında geçersiz kılabilirsiniz.  
    * Silme işleminde satış vergisini orijinal hareketten ayırmak isterseniz bu ayarı Evet yapın.  
4. Sayfayı kapatın.
5. Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri'ne gidin.
    * Silme hesabı gider hesabı olarak veya yevmiye defterinde rezerv düzeltme olarak kullanılır   
6. Sayfayı kapatın.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Bir müşteri bakiyesini yaşlandırılmış bakiyeler sayfasında silin
1. Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler.
2. Silme işlemi yapmak istediğiniz müşterinin satırını işaretleyin. Örneğin, Birch şirketinin bulunduğu satırı işaretleyin.
3. Eylem Bölmesinde, Tahsil et'e tıklayın.
4. Silme'ye tıklayın.
5. Tamam'a tıklayın.
6. Sayfayı kapatın.
7. Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.
8. Silme işleminizi içeren günlüğün günlük toplu iş numarasını seçin.
    * Müşteri bakiyesini ters kaydetmek için bir satır oluşturulur. Silme işlemini silme hesabına nakletmek için bir veya birden fazla satır oluşturulur.  
9. Sayfayı kapatın.
10. Sayfayı kapatın.

## <a name="write-off-transactions-from-the-collections-form"></a>Hareketleri tahsilatlar formunda silin.
1. Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler.
2. Silmek istediğiniz hareketlerin sahibi olan müşterinin adını seçin. Örneğin Cave Wholesales (US-004) adını seçin.
3. İlk hareketin satırını işaretleyin.
4. İkinci hareketin satırını işaretleyin.
5. Silme'ye tıklayın.
6. Neden yorumu alanına "Ödenmeyen borçlar" yazın.
7. Tamam'a tıklayın.
8. Sayfayı kapatın.
9. Sayfayı kapatın.
10. Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.
11. Silme işleminizi içeren günlüğün günlük toplu iş numarasını seçin.
    * Müşteri bakiyesini ters kaydetmek için bir satır oluşturulur. Silme işlemini silme hesabına nakletmek için bir veya birden fazla satır oluşturulur.  
12. Sayfayı kapatın.
13. Sayfayı kapatın.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Bir faturayı Açık müşteri faturaları sayfasında silin
1. Alacak hesapları > Faturalar > Açık müşteri faturaları'na gidin.
2. Bir faturanın satırını işaretleyin. Örneğin, CIV-000667'ye ait satırı işaretleyin.
3. Eylem Bölmesinde, Fatura öğesine tıklayın.
4. Silme'ye tıklayın.
5. Tamam'a tıklayın.
6. Sayfayı kapatın.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Bir müşteri bakiyesini müşteri sayfasında silin
1. Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.
2. Bir müşteri hesabı seçin. Örneğin, US-001 (Contoso Retail San Diego) değerini seçin.
3. Eylem Bölmesinde, Tahsil et'e tıklayın.
4. Silme'ye tıklayın.
5. Tamam'a tıklayın.
6. Sayfayı kapatın.



---
title: Müşteri için silme günlüğü oluşturma
description: Bu görev kılavuzunda, silme işlemleri parametrelerinin ve ardından silme hareketlerinin Tahsilatlar sayfasından, Açık müşteri faturaları sayfasından ve Müşteri sayfasından nasıl ayarlanacağını göreceksiniz.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6526e57cf2ed84161eb7a92c031127bb6c6536a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003316"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Müşteri için silme günlüğü oluşturma

[!include [banner](../../includes/banner.md)]

Bu görev kılavuzunda, silme işlemleri parametrelerinin ve ardından silme hareketlerinin Tahsilatlar sayfasından, Açık müşteri faturaları sayfasından ve Müşteri sayfasından nasıl ayarlanacağını göreceksiniz. Bu görevde USMF demo şirketi kullanılmaktadır.


## <a name="set-up-the-write-off-parameters"></a>Silme parametrelerini ayarlayın
1. **Gezinti bölmesi > Modüller > Alacak ve tahsilatlar > Kurulum > Alacak hesapları parametreleri**'ne gidin.
2. **Tahsilatlar**  sekmesine tıklayın.
3. **Silme bölümünü** genişletin veya daraltın.
    - **Silme günlüğü**, oluşturduğunuz silme hareketlerini tutan yevmiye defteridir.  
    - Her silme işlemine bir neden kodu ekleyebilirsiniz. Bu varsayılan değeri silme işlemi sırasında geçersiz kılabilirsiniz.  
    - Silme işleminde satış vergisini orijinal hareketten ayırmak isterseniz **Satış vergisini ayır**'ı Evet yapın.  
4. Sayfayı kapatın.
5. **Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri**'ne gidin. Silme hesabı gider hesabı olarak veya yevmiye defterinde rezerv düzeltme olarak kullanılır.
6. Sayfayı kapatın.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Bir müşteri bakiyesini yaşlandırılmış bakiyeler sayfasında silin
1. **Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler**'e gidin.
2. Silme işlemi yapmak istediğiniz müşterinin satırını işaretleyin. Örneğin, Birch şirketinin bulunduğu satırı işaretleyin.
3. **Eylem Bölmesinde**, **Tahsil et** öğesine tıklayın.
4. **Sil**'e tıklayın.
5. **Tamam**'a tıklayın.
6. Sayfayı kapatın.
7. **Gezinti bölmesi > Modüller > Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin.
8. Silme işleminizi içeren günlüğün günlük toplu iş numarasını seçin. Müşteri bakiyesini ters kaydetmek için bir satır oluşturulur. Silme işlemini silme hesabına nakletmek için bir veya birden fazla satır oluşturulur.  
9. Sayfayı kapatın.
10. Sayfayı kapatın.

## <a name="write-off-transactions-from-the-collections-form"></a>Hareketleri tahsilatlar formunda silin.
1. **Alacak ve tahsilatlar > Tahsilatlar > Yaşlandırılmış bakiyeler**'e gidin.
2. Silmek istediğiniz hareketlerin sahibi olan müşterinin adını seçin. Örneğin Cave Wholesales (US-004) adını seçin.
3. İlk hareketin satırını işaretleyin.
4. İkinci hareketin satırını işaretleyin.
5. **Sil**'e tıklayın.
6. **Neden açıklaması** alanına "Ödenmeyen borçlar" yazın.
7. **Tamam**'a tıklayın.
8. Sayfayı kapatın.
9. Sayfayı kapatın.
10. **Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin.
11. Silme işleminizi içeren günlüğün günlük toplu iş numarasını seçin. Müşteri bakiyesini ters kaydetmek için bir satır oluşturulur. Silme işlemini silme hesabına nakletmek için bir veya birden fazla satır oluşturulur.  
12. Sayfayı kapatın.
13. Sayfayı kapatın.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Bir faturayı Açık müşteri faturaları sayfasında silin
1. **Gezinti bölmesi > Modüller > Alacak hesapları > Faturalar > Açık müşteri faturaları**'na gidin.
2. Bir faturanın satırını işaretleyin. Örneğin, CIV-000667'ye ait satırı işaretleyin.
3. **Eylem Bölmesinde** **Fatura** öğesine tıklayın.
4. **Sil**'e tıklayın.
5. **Tamam**'a tıklayın.
6. Sayfayı kapatın.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Bir müşteri bakiyesini müşteri sayfasında silin
1. **Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.
2. Bir müşteri hesabı seçin. Örneğin, US-001 (Contoso Retail San Diego) değerini seçin.
3. **Eylem Bölmesinde**, **Tahsil et** öğesine tıklayın.
4. **Sil**'e tıklayın.
5. **Tamam**'a tıklayın.
6. Sayfayı kapatın.


--- 
title: "ISO20022 hesaptan ödemeleri için müşterileri ve müşteri banka hesaplarını ayarlama"
description: "Bu görev, ISO20022 hesaptan ödeme gibi müşteri ödeme dosyası oluşturmak için gereken bir müşteri banka hesabı ve bir müşteri hesaptan ödeme talimatı ayarlamada size yol gösterir."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7aac1af99f2b5a7b1a123a8e3d3d6ddcaaa39b8d
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>ISO20022 hesaptan ödemeleri için müşterileri ve müşteri banka hesaplarını ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev, ISO20022 hesaptan ödeme gibi müşteri ödeme dosyası oluşturmak için gereken bir müşteri banka hesabı ve bir müşteri hesaptan ödeme talimatı ayarlamada size yol gösterir. Ayarlanan müşteri ödeme biçimlerine bağlı olarak bir müşteri veya müşteri banka hesabı için bu yordamda incelenmeyen ek bilgiler gerekebilir. 

Bu görev, tüzel kişilik birincil adresi Almanya'da olan demo veri şirketi DEMF'yi kullanarak oluşturulmuştur.



Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın dördüncüsüdür.


## <a name="set-up-a-customer-bank-account"></a>Bir müşteri banka hesabı ayarlayın
1. Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Hesap alanına "DE-010" değeriyle filtre uygulayın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Eylem Bölmesinde, Müşteri'ye tıklayın.
5. Banka hesapları'na tıklayın.
6. Yeni'ye tıklayın.
7. Banka hesabı alanına bir değer girin.
8. İsim alanına bir değer yazın.
    * Örneğin, "EUR bankası" girin.  
9. Banka grupları alanında bir değer girin veya seçin.
10. IBAN alanına bir değer girin.
    * Örneğin, "DE36200400000628808808" girin.  
11. SWIFT kodu alanına bir değer girin.
    * Örneğin: "COBADEFFXXX" girin.  Birçok ödeme biçimi için SWIFT \ BIC zorunlu değildir ancak yine de bir banka hesabı için kayıtlı bulunması önerilir.  
12. Kaydet'e tıklayın.
13. Sayfayı kapatın.
14. Düzenle öğesine tıklayın.
15. Ödeme varsayılanları bölümünü genişletin.
16. Banka hesabı alanında bir değer girin veya seçin.

## <a name="add-a-direct-debit-mandate"></a>Hesaptan ödeme talimatı ekleyin
1. Hesaptan ödeme talimatları bölümünü genişletin.
2. Ekle öğesini tıklatın.
3. Alacaklı banka hesabı alanına bir değer girin veya seçin.
    * Örneğin, DEMF OPER'i seçin.  
4. İmza tarihi alanına bir tarih girin.
5. Tarih güncelleştirmesini onaylamak için Evet'e tıklayın.
6. İmza konumu alanında bir değer girin veya seçin.
7. Beklenen ödeme sayısı alanına bir sayı girin.
8. Tamam'a tıklayın.
9. Kaydet'e tıklayın.



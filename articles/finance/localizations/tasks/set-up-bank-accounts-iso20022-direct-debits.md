---
title: ISO20022 hesaptan ödemeleri için müşterileri ve müşteri banka hesaplarını ayarlama
description: Bu görev, ISO20022 hesaptan ödeme gibi müşteri ödeme dosyası oluşturmak için gereken bir müşteri banka hesabı ve bir müşteri hesaptan ödeme talimatı ayarlamada size yol gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d097caf3ad097e3107708c426ef668c70298c4f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209863"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>ISO20022 hesaptan ödemeleri için müşterileri ve müşteri banka hesaplarını ayarlama

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
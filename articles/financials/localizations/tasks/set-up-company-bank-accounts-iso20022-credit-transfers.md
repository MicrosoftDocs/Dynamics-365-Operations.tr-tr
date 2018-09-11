--- 
title: "ISO20022 alacak transferleri için şirket banka hesapları ayarlama"
description: "Bu yordam, ödeme dosya oluşturması için gerekli olan şirkete özel banka hesap bilgilerinin nasıl ayarlanacağını gösterir."
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>ISO20022 alacak transferleri için şirket banka hesapları ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, ödeme dosya oluşturması için gerekli olan şirkete özel banka hesap bilgilerinin nasıl ayarlanacağını gösterir. ISO 20022 alacak transferi biçimi oluşturmak için gereken bilgileri ayarladınız ancak biçime bağlı olarak Şirket Kodu veya Sıralama kodu gibi başka bilgiler de gerekebilir. 

Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.

Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın ikincisidir. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="set-up-iban-and-swift-code"></a>IBAN ve SWIFT kodunu ayarlama
1. Nakit ve banka yönetimi > Banka hesapları'na gidin.
2. Banka hesabı alanında "DEMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.
3. Banka hesabı ayrıntılarını açmak için DEMF OPER'e tıklayın.
4. Düzenle öğesine tıklayın.
5. Ek kimlik bölümünü genişletin.
6. IBAN alanına "DE89370400440532013000" yazın.
7. SWIFT kodu alanına "DEUTDEFF" yazın.
    * Birçok ödeme biçimi için SWIFT\BIC gerekli değildir ancak yine de bir banka hesabı için kayıtlı bulunması önerilir.  
8. Kaydet'e tıklayın.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Tüzel kişilik için banka hesabını ayarlama
1. Organizasyon yönetimi > Kuruluşlar > Tüzel kişilikler'e gidin.
2. Düzenle öğesine tıklayın.
3. Banka hesabı bilgileri bölümünü genişletin.
4. Banka hesabı alanında bir değer girin veya seçin.
5. Kaydet'e tıklayın.



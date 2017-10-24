--- 
title: "ISO20022 hesaptan ödemeleri için şirket banka hesapları ayarlama"
description: "Bu görev, müşteri ödeme dosyaları oluşturmak için gerekli olan, şirkete özel banka hesap bilgilerini ayarlamada size yol gösterir."
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 6b61495342b18d6dbadb36d8ca146f5a68ba9f6c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>ISO20022 hesaptan ödemeleri için şirket banka hesapları ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev, müşteri ödeme dosyaları oluşturmak için gerekli olan, şirkete özel banka hesap bilgilerini ayarlamada size yol gösterir. Bu yordam örnek olarak ISO 20022 hesaptan ödeme biçimini kullanır. Diğer biçimler Şirket Kimliği veya Sıralama Kodu gibi ek kurulum bilgileri gerektirebilir.



Bu görev, DEMF demo veri şirketi kullanarak oluşturulmuştur.



Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın ikincisidir.


## <a name="set-up-the-iban-and-swift-codes"></a>IBAN ve SWIFT kodlarını ayarlayın
1. Nakit ve banka yönetimi > Banka hesapları'na gidin.
2. Banka hesabı alanında "DEMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * Örneğin: banka hesabı ayrıntılarını açmak için "DEMF OPER"e tıklayın.  
4. Düzenle öğesine tıklayın.
5. Ek kimlik bölümünü genişletin veya daraltın.
6. IBAN alanına bir değer girin.
    * Örneğin, "DE89370400440532013000" girin.  
7. SWIFT kodu alanına bir değer girin.
    * Örneğin "DEUTDEFF" girin.    Birçok ödeme biçimi için SWIFT \ BIC zorunlu değildir ancak yine de bir banka hesabı için kayıtlı bulunması önerilir.  
8. Kaydet'e tıklayın.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Tüzel kişilik için bir banka hesabı ayarlayın
1. Organizasyon yönetimi > Kuruluşlar > Tüzel kişilikler'e gidin.
2. Düzenle öğesine tıklayın.
3. Banka hesabı bilgileri bölümünü genişletin veya daraltın.
4. Banka hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
    * Örneğin, "DEMF OPER" banka hesabını seçin.  
6. Kaydet'e tıklayın.



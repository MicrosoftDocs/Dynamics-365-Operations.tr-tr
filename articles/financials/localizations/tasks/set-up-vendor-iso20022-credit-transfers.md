---
title: ISO20022 alacak transferleri için satıcıları ve satıcı banka hesaplarını ayarlama
description: Bu yordam, ISO20022 Alacak transferi veya başka bir satıcı ödemesi dosyası oluşturma işlemi için gereken, satıcı ve satıcıya özel banka hesabı bilgilerinin nasıl ayarlanacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13b3c37f5d013dd896a456018813f20e5e70350b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "311623"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>ISO20022 alacak transferleri için satıcıları ve satıcı banka hesaplarını ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, ISO20022 Alacak transferi veya başka bir satıcı ödemesi dosyası oluşturma işlemi için gereken, satıcı ve satıcıya özel banka hesabı bilgilerinin nasıl ayarlanacağını gösterir. 

Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.
Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın dördüncüsüdür. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="set-up-bank-details"></a>Banka ayrıntılarını ayarlayın
1. Borç hesapları > Satıcılar > Tüm satıcılar seçeneğine gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Satıcı hesabı alanında "DE-001" değerini girerek filtreleme yapın.
3. Satıcı ayrıntılarını açmak için DE-001'e tıklayın.
4. Eylem Bölmesinde, Satıcı'ya tıklayın.
5. Banka hesapları'na tıklayın.
6. Düzenle öğesine tıklayın.
    * Kullanılabilir herhangi bir banka hesabı yoksa, yeni bir banka hesabı oluşturmanız gerekir.  
7. SWIFT kodu alanına "COBADEFFXXX" yazın.
8. IBAN alanına "DE36200400000628808808" yazın.
9. Sayfayı kapatın.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Satıcı için ödeme yöntemi ayarlama
1. Düzenle öğesine tıklayın.
2. Ödeme bölümünü genişletin veya daraltın.
3. Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, SEPA CT satırındaki bağlantıya tıklayın.
5. Kaydet'e tıklayın.


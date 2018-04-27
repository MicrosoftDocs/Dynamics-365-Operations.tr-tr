--- 
title: "ISO20022 alacak transferi için ödeme yöntemini ayarlama"
description: "Bu yordam, elektronik raporlama kullanılarak bir dosya oluşturmak için ISO20022 alacak transferi için satıcı ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bed51f8749dfa0264ad39f51f9ceb295ac46fe93
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>ISO20022 alacak transferi için ödeme yöntemini ayarlama

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, elektronik raporlama kullanılarak bir dosya oluşturmak için ISO20022 alacak transferi için satıcı ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir. 

Bu görevi tamamlamadan önce biçim yapılandırmalarını dışa aktarmanız ve ödeme hesaplarını ayarlamanız gerekir.

Bu görev, DEMF demo veri şirketi kullanarak oluşturulmuştur.

Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın üçüncüsüdür. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.

1. Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ödeme yöntemi alanına "SEPA CT" değeriyle filtre uygulayın.
3. Düzenle'yi tıklatın.
4. Dönem alanında "Toplam"ı seçin.
5. Dönem türü alanında "Elektronik ödeme"yi seçin.
6. Dosya biçimleri bölümünü genişletin.
7. Genel elektronik raporlama alanında Evet'i seçin.
8. Biçim yapılandırmasını dışa aktar alanında bir değer girin veya seçin.
    * Listede ISO20022 Alacak Transferi (DE) değerini seçin. Liste boşsa, satıcı ödemesi biçim yapılandırması içe aktarılmamıştır ve etkin değildir.  
9. Hesap türü alanında "Banka"yı seçin.
10. Ödeme hesabı alanında "DEMF OPER" değerlerini belirtin.
11. Kaydet'e tıklayın.



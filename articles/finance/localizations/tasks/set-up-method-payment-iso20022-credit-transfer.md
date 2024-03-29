---
title: ISO20022 alacak transferi için ödeme yöntemini ayarlama
description: Bu yordam, elektronik raporlama kullanılarak bir dosya oluşturmak için ISO20022 alacak transferi için satıcı ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f87cc0dfa47295f047ef97732f60733c362ca4066d9070418322b34934e3ce3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773672"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>ISO20022 alacak transferi için ödeme yöntemini ayarlama

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
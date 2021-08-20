---
title: ISO20022 hesaptan ödeme için ödeme yöntemi ayarlama
description: Bu yordam, elektronik raporlama kullanılarak ISO20022 hesaptan ödeme için müşteri ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127d5402abfedcce124b39b76a6c1036a6c818a7c1318aaeabdb0688b50f738e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779773"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>ISO20022 hesaptan ödeme için ödeme yöntemi ayarlama

[!include [banner](../../includes/banner.md)]

Bu yordam, elektronik raporlama kullanılarak ISO20022 hesaptan ödeme için müşteri ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir. 



Bu görevi tamamlamadan önce dışa aktarma biçim yapılandırmalarını ve ödeme hesaplarını ayarlamanız gerekir.



Bu yöntem oluşturulurken DEMF demo verisi şirketi kullanılmıştır.



Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın üçüncüsüdür.

1. Alacak hesapları > Ödeme kurulumu > Ödeme yöntemi'ne gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ödeme yöntemi alanına "ELECTRONIC" değeriyle filtre uygulayın.
3. Düzenle'yi tıklatın.
4. Ödeme hesabı alanında "DEMF OPER" değerlerini belirtin.
5. Dosya biçimleri bölümünü genişletin.
6. Genel elektronik raporlama alanında Evet'i seçin.
7. Biçim yapılandırmasını dışa aktar alanında bir değer girin veya seçin.
    * Listede ISO20022 Hesaptan ödeme (DE) seçeneğini belirleyin.  Liste boşsa, müşteri ödemesi biçim yapılandırması içe aktarılmamıştır ve etkin değildir.  
8. Talimat iste alanında Evet'i seçin.
    * Müşteri ödeme biçimleri için SEPA hesaptan ödemesi gibi ödeme iletisinde talimat bilgilerini içermesini gerektiren, Talimat iste parametresini seçin.  
9. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
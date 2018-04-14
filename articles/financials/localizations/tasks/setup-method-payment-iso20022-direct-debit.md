--- 
title: "ISO20022 hesaptan ödemesi için ödeme yöntemini ayarlama"
description: "Bu yordam, elektronik raporlama kullanılarak ISO20022 hesaptan ödeme için müşteri ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3a884837ab0b5a1f4211532969619b54206bbef4
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>ISO20022 hesaptan ödemesi için ödeme yöntemini ayarlama

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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



---
title: İleri tarih atılmış çekleri ayarlama
description: Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc1798836d9b905d991adb4c87d55ddce41d260bdbfdad6bf0c4b4feb846ee57
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743085"
---
# <a name="set-up-postdated-checks"></a>İleri tarih atılmış çekleri ayarlama

[!include [banner](../../includes/banner.md)]

Bu başlık vadeli çekler için defter girişlerinin nakledilip edilmemesini ve satıcı ödemeleri için giriş temizliğinde hangi nakil günlüklerinin kullanılacağını açıklamaktadır. Ayrıca, verilen çekler, alınan çekler ve stopaj vergisi takas hesaplarını belirtebilirsiniz. Gelecekte ödeme yapmak veya almak için çıkartılan vadeli çekler. Çekin hesap defterlerinde, vade tarihinden önce yansıtılmasına gerek olup olmadığını belirtebilirsiniz.



Bu yordamın rolü Haznedar'dır. Bu yordam, USMF demo şirketini kullanır.


## <a name="set-up-postdated-checks"></a>İleri tarih atılmış çekleri ayarlama
1. Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.
2. Vadeli çekler sekmesini tıklatın.
3. Vadeli çekleri etkinleştirin onay kutusunu işaretleyin veya işareti kaldırın.
4. Vadeli çekler için defter girişlerini nakletme onay kutusunu temizleyin veya seçin.
5. Verilen çekler için takas hesabı alanında için istediğiniz değerleri belirtin.
6. Alınan çekler için takas hesabı alanında için istediğiniz değerleri belirtin.
7. Takas girişleri yevmiye defterine, bir değer yazın.
8. İleri tarih atılmış çekleri bu satıcı ödeme günlüğüne transfer et alanına bir değer yazın.
9. Stopaj vergisi takas hesabı alanına, istediğiniz değerleri belirleyin.
10. Kaydet'e tıklayın.
11. Sayfayı kapatın.
12. Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.
13. Yeni'ye tıklayın.
14. Ödeme yöntemi alanına bir değer girin.
15. Çek miktarının takas hesabına nakledildiğini belirtmek için vadeli hesap takas nakli seçeneğini işaretleyin.
16. Hesap türü alanında "Banka"yı seçin.
    * Ödeme yönteminin mahsup hesabı bir banka olacaktır.  
17. Ödeme hesabı alanında istediğiniz değerleri belirtin.
    * Fatura miktarının çekilmesi için kullanılacak banka hesabını seçin.  
18. Kaydet'e tıklayın.
19. Sayfayı kapatın.
> [!NOTE]
> Oturum tarihi, vade tarihinden büyük veya bu tarihe eşit olduğunda, bir banka hesabına ileri tarihli bir çek nakledebilmek için, **Ödeme günlüğünü naklinin banka hesabına yatırılan ileri tarihli çeklerle vade tarihi doğrulaması** özelliğini etkinleştirmeniz gerekir. Bu özellik, oturum tarihi vade tarihine eşit veya bun tarihten büyük olduğunda satıcılar veya müşteriler için ödeme günlüklerini deftere nakletmenize olanak sağlar.
> 
> **Ödeme yöntemi**'ni ayarlarken ( **Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri**), **Bağlantılı hesap** alanını doldurmayın. Bu durumda, mahsup hesap, **Ödeme yöntemi**'nde ayarlanan banka hesabıyla doldurulur.
>  
> Özellik etkinleştirildiğinde ve oturum tarihi vade tarihinden erken bir tarihteyse, ödeme günlüğü deftere nakledilirken şu hata iletisi görüntülenir: "Mahsup hesap türü Banka ise, vade tarihinin oturum tarihine eşit veya bu tarihten erken olması gerekir". Özellik etkinleştirilmemişse, oturum tarihi vade tarihinden erken olduğunda ödeme günlüğünü ileri tarihli bir çekle deftere nakledebilirsiniz.
> Bu özellik 10.0.21 sürümü ve sonrasında bulunur.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

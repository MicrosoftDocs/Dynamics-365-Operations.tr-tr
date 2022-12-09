---
title: İleri tarih atılmış çekleri ayarlama
description: Bu makalede, vadeli çekler için defter girişlerinin nakledilip edilmeyeceğinin yanı sıra kliring girişleri ve satıcı ödemeleri için hangi deftere nakil günlüklerinin kullanılacağının nasıl belirtileceği açıklanmaktadır.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5ef9aa6b67eb630713dd1f15b2ae49c358edae9
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804195"
---
# <a name="set-up-postdated-checks"></a>İleri tarih atılmış çekleri ayarlama

[!include [banner](../../includes/banner.md)]

Bu makalede, vadeli çekler için defter girişlerinin nakledilip edilmeyeceğinin yanı sıra kliring girişleri ve satıcı ödemeleri için hangi deftere nakil günlüklerinin kullanılacağının nasıl belirtileceği açıklanmaktadır. Ayrıca, verilen çekler, alınan çekler ve stopaj vergisi takas hesaplarını belirtebilirsiniz. Gelecekte ödeme yapmak veya almak için çıkartılan vadeli çekler. Çekin hesap defterlerinde, vade tarihinden önce yansıtılmasına gerek olup olmadığını belirtebilirsiniz.



Bu yordamın rolü Haznedar'dır. Bu yordam, USMF demo şirketini kullanır.


## <a name="set-up-postdated-checks"></a>İleri tarih atılmış çekleri ayarlama
1. **Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri**'ne gidin.
2. **İleri tarihli çekler** sekmesine tıklayın.
3. **İleri tarihli çekleri etkinleştir** onay kutusunu işaretleyin veya işareti kaldırın.
4. **İleri tarihli çekler için defter girişlerini deftere naklet** onay kutusunu temizleyin veya seçin.
5. **Verilen çekler için takas hesabı** alanında için istediğiniz değerleri belirtin.
6. **Alınan çekler için takas hesabı** alanında için istediğiniz değerleri belirtin.
7. **Takas girişleri yevmiye defteri** alanına bir değer yazın.
8. **İleri tarihli çekleri bu satıcı ödeme günlüğüne transfer et** alanına bir değer yazın.
9. **Stopaj vergisi takas hesabı** alanında istediğiniz değerleri belirtin.
10. **Kaydet**'e tıklayın.
11. Sayfayı kapatın.
12. **Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri**'ne gidin.
13. **Yeni**'yi tıklatın.
14. **Ödeme yöntemi** alanına bir değer girin.
15. Çek miktarının takas hesabına nakledildiğini belirtmek için **İleri tarihli çek takas deftere nakli** seçeneğini işaretleyin.
16. **Hesap türü** alanında **Banka**'yı seçin.
    * Ödeme yönteminin mahsup hesabı bir banka olacaktır.  
17. **Ödeme hesabı** alanında istediğiniz değerleri belirtin.
    * Fatura miktarının çekilmesi için kullanılacak banka hesabını seçin.  
18. **Kaydet**'e tıklayın.
19. Sayfayı kapatın.
> [!NOTE]
> Oturum tarihi, vade tarihinden büyük veya bu tarihe eşit olduğunda, bir banka hesabına ileri tarihli bir çek nakledebilmek için, **Ödeme günlüğünü naklinin banka hesabına yatırılan ileri tarihli çeklerle vade tarihi doğrulaması** özelliğini etkinleştirmeniz gerekir. Bu özellik, oturum tarihi vade tarihine eşit veya bun tarihten büyük olduğunda satıcılar veya müşteriler için ödeme günlüklerini deftere nakletmenize olanak sağlar.
> 
> **Ödeme yöntemi**'ni ayarlarken ( **Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri**), **Bağlantılı hesap** alanını doldurmayın. Bu durumda, mahsup hesap, **Ödeme yöntemi**'nde ayarlanan banka hesabıyla doldurulur.
>  
> Özellik etkinleştirildiğinde ve oturum tarihi vade tarihinden erken bir tarihteyse, ödeme günlüğü deftere nakledilirken şu hata iletisi görüntülenir: **Mahsup hesap türü Banka ise, vade tarihinin oturum tarihine eşit veya bu tarihten erken olması gerekir**. Özellik etkinleştirilmemişse, oturum tarihi vade tarihinden erken olduğunda ödeme günlüğünü ileri tarihli bir çekle deftere nakledebilirsiniz.
> Bu özellik 10.0.21 sürümü ve sonrasında bulunur.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

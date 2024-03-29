---
title: ER Biçim yapılandırmayı kullanarak ödemeler için elektronik belgeler oluşturma
description: Bu makalede, ödemeleri işlemek üzere elektronik belgeler oluşturmak için yeni bir Elektronik raporlama (ER) biçimi yapılandırmasının nasıl kullanılacağı açıklanmaktadır.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
ms.openlocfilehash: b70b246e3618e8f083e5f6757ee8a97d8072a635
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290889"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>ER Biçim yapılandırmayı kullanarak ödemeler için elektronik belgeler oluşturma

[!include [banner](../../includes/banner.md)]

Aşağıdaki yordamlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının yeni bir Elektronik Raporlama (ER) biçim yapılandırmasını kullanarak, ödemeleri işlemek için elektronik belgeleri nasıl oluşturabileceğini açıklar. Bu adımlar GBSI örnek şirketinde gerçekleştirilebilir.

Bu adımları tamamlamak için, öncelikle "Ödeme belgesi biçimi ile bir yapılandırma oluşturun" yordamındaki adımları tamamlamanız gerekir.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Elektronik ödeme yönteminin yapılandırmasını değiştirin
1. Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.
2. Gerekirse, genişletmek için Dosya biçimi bölümünü değiştirin.
3. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ödeme yöntemi alanına 'Elektronik' değeriyle filtre uygulayın.
4. Düzenle öğesine tıklayın.
5. Genel elektronik raporlama alanını Evet olarak ayarlayın.
    * Ödeme dosyaları oluşturmak için genel elektronik raporlama deseni kullanmak için Evet'i seçin.  
6. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
7. BACS (UK hayali) yapılandırma biçimini seçin.
8. Kaydet'e tıklayın.
9. Sayfayı kapatın.

## <a name="test-the-format-of-generated-payment-files"></a>Oluşturulan ödeme dosyalarının biçimini sınayın
1. Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
    * VendPay seçin.  
6. Kaydet'e tıklayın.
7. Satırlar seçeneğine tıklayın.
8. Şirket alanına 'DEMF' yazın.
    * DEMF  
9. Hesap alanında, 'DE-01001' değerlerini belirtin.
    * DE-01001  
10. Tanım alanına 'Ödeme' yazın.
    * Ödeme  
11. Borç alanına bir sayı girin.
    * 1000  
12. Ödeme sekmesine tıklayın.
13. Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.
14. Listede, istenen kaydı bulun ve seçin.
    * Elektronik değeri seçin.  
15. Listede, seçili satırdaki bağlantıya tıklayın.
16. Kaydet'e tıklayın.
17. Ödemeler oluştur'u tıklatın.
18. Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.
19. Listede, istenen kaydı bulun ve seçin.
    * Elektronik değeri seçin.  
20. Listede, seçili satırdaki bağlantıya tıklayın.
    * Elektronik değeri seçin.  
21. Dosya adı alanına bir değer girin.
    * Örneğin 'ödemeler' yazın.  
22. Banka hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
23. Listede, seçili satırdaki bağlantıya tıklayın.
    * GBSI OPER değerini seçin.  
24. Tamam'a tıklayın.
25. Tamam'a tıklayın.
    * XML biçiminde oluşturulan ödeme dosyasının çözümleyin. Bunu, tasarlanmış belge düzeni ve tanımlanan ödeme işlem özniteliklerini ile karşılaştırın.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

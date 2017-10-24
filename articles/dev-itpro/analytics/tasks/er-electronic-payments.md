--- 
title: "Elektronik raporlama (ER) için biçim yapılandırması kullanarak ödemelere ilişkin elektronik belgeler oluşturma"
description: "Aşağıdaki yordamlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının yeni bir Elektronik Raporlama (ER) biçim yapılandırmasını kullanarak, ödemeleri işlemek için elektronik belgeleri nasıl oluşturabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için biçim yapılandırması kullanarak ödemelere ilişkin elektronik belgeler oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

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



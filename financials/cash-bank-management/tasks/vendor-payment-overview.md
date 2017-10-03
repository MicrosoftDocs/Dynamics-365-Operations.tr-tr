--- 
title: "Satıcı ödemesine genel bakış"
description: "Bu görev kılavuzu size satıcı ödemeleri oluşturmak için çeşitli yöntemleri gösterecektir. Bunların arasında ödeme teklifi veya tek seferlik bir ödemeyi elden girmek de bulunmaktadır."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 44b7c02e7c238dcea83c5900620731a7befbbb42
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="vendor-payment-overview"></a>Satıcı ödemesine genel bakış

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu size satıcı ödemeleri oluşturmak için çeşitli yöntemleri gösterecektir. Bunların arasında ödeme teklifi veya tek seferlik bir ödemeyi elden girmek de bulunmaktadır. Bu yordam, USMF demo şirketini kullanır.

1. Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.
2. Yeni'ye tıklayın.
3. Satıcı ödemelerinin kaydedileceği ödeme günlüğünü seçin. 
4. Bir günlüğü seçin veya el ile girin.
5. Satırlar seçeneğine tıklayın.
6. Ödeme teklifi'ne tıklayın.
7. Ödeme teklifi oluştur'a tıklayın.
    * Ödeme teklif, ödeme için faturaları seçmede kullanılan bir sorgudur. Satıcı ödemelerini oluşturmadan veya yaratmadan önce, ödenecek faturaların listesini düzenleyebilirsiniz.  
8. Ödeme için faturaları vade tarihi, nakit iskontosu veya her ikisini birden kullanarak seçin. 
9. Vade tarihi veya nakit iskontosu ile karşılaştırmak için tarihi girin. 
10. İsteğe bağlı: Tüm ödemeler için kullanılacak ödeme tarihi girin.
    * Buraya girilen tarihi, nakit iskontosu tarihi veya vade tarihi ne olursa olsun, tüm ödemeler için geçerli ödeme tarihi olacaktır.  
11. İsteğe bağlı: Ödeme tarihi olarak kullanılabilecek bir minimum ödeme tarihini girin.
    * Minimum ödeme tarihi, ödemeler oluşturulurken kullanılan en erken tarihi olacaktır. Örneğin, bir faturanın vade tarihi, minimum ödeme tarihinden sonraysa, vade tarihi minimum ödeme tarihi yerine vade tarihi ödeme yapmak için kullanılır ve bu sayede faturayı mümkün olan en geç şekilde ödeme imkanı doğar.  
12. Ek sorgu kısıtlamalarını, Dahil edilecek kayıtları altında girin.
    * Filtre, genellikle satıcı tarafından ödeme için seçilen faturaları veya ödeme yöntemini kısıtlamakta için kullanılır. Örneğin, bu ödeme işleminde faturaları sadece çek ile ödemek için bir filtre ekleyebilirsiniz.  
13. Ek sorgu kısıtlaması veya ödeme varsayılan değerleri girin. 
    * Ek parametreler ödemenin yapılacağı para birimini tanımlamada veya merkezi ödemeleri bu ödeme işlemi için etkinleştirmede kullanılabilir.  
14. Tamam'a tıklayın.
    * Tamam'ı tıklattıktan sonra sorgu sonuçları görüntülenir. Ödenmek üzere seçilen faturaların listesini önizlemek istemiyorsanız, Parametreler hızlı sekmesine geri giderek Ödemeleri fatura önizlemesi olmadan oluştur seçeneğini Evet olarak seçebilirsiniz.  
15. Seçili faturayla ilgili satıcı için oluşturulan ödemeleri görüntülemek için Ödeme genel bakış göster düğmesini seçin.
16. Ödemeleri gizlemek için Ödeme genel bakışı gizle düğmesini seçin. 
17. Ödemeleri oluştur'a tıklayın.
    * Ödemeleri oluştur'u seçmeden önce kılavuzun üzerinde sağ tıklatıp, faturaların listesini Excel'e aktarabilirsiniz. Ödemeleri Oluştur düğmesi, satıcı ödemelerini ödeme günlüğünde oluşturur.  
18. Ödemelerinizi tarayın ve ödeme yönteminin tüm ödemeler için tanımlanmış olduğundan emin olun. 
    * Çek yazdırma ve elektronik ödeme oluşturma gibi ödemeleri oluşturursanız, öncelikle ödeme yöntemini tanımlamalısınız. Ödeme yöntemi aynı zamanda ödemenin yapılacağı banka hesabını da varsayılan olarak ayarlar.  
19. Tek seferlik ödeme oluşturmak için Yeni'yi tıklatın.
    * Tek seferlik bir ödeme, deftere nakledilmeden önce herhangi bir zamanda ödeme günlüğüne eklenebilir. Bu ekleme, ödeme teklifini kullanmak yerine, Yeni düğmesini tıklatarak ve sonra ödeme bilgilerini el ile girerek yapılır.  
20. Ödemenin yapılacağı satıcıyı seçin.
21. Bir faturayı ödemek için varsa, ödeme için faturayı seçmek için, Kapanış hareketleri'ni seçin.
    * Bu bir ön ödeme ise, bu adım isteğe bağlıdır. Bir fatura seçmeden ödemeyi oluşturabilirsiniz.  
22. Ödenecek faturaları işaretleyin.
    * Kapanış hareketlerimi için ödeme faturaları seçmek için kullanırsanız, ödeme tutarı otomatik olarak hangi faturaları ödeme için seçtiğiniz ve Tutar bölümüne kapatmak için hangi tutarı girdiğiniz ile hesaplanır.  
23. Tamam'a tıklayın.
24. Bir ödemeyi silmek isterseniz, satırı işaretleyin.
25. Sil'i tıklatın.
    * Bir ödemeyi silmek yalnızca ödemenin silinmesine neden olur. Ödeme için işaretlenmiş herhangi bir fatura, başka bir ödeme tarafından ödenebilir olmaya devam edecektir.  
26. Evet'i tıklatın.
27. Ödeme oluştur'u seçerek Çekleri yazdırmak veya elektronik ödeme dosyası oluşturabilirsiniz.
28. Oluşturmak istediğiniz ödeme türünü seçin.
    * Ödeme günlüğü hem Çekler hem de elektronik ödemeler için ödemeler içerebilir fakat bir seferde sadece bir ödeme türü oluşturabilirsiniz.  
29. Ödemeler oluşturmak için kullanmak istediğiniz banka hesabını seçin.
30. Tamam'a tıklayın.
    * Ödemeler yalnızca ödeme yöntemiyle ve seçtiğiniz banka hesabıyla eşleşen ödemeler için oluşturulur.  
31. Çek oluşturuyorsanız, Çekler için doğru yazdırma hedefinin sağlamak için Belge'yi seçin.
32. Tamam'a tıklayın.
33. Tamam'ı tıklayarak ödemeleri oluşturun.
34. Tüm ödemeler oluşturuldu ve onaylandıysa, Deftere Naklet'i tıklatın. 



---
title: Satıcı ödemesine genel bakış
description: Bu görev kılavuzu size satıcı ödemeleri oluşturmak için çeşitli yöntemleri gösterecektir. Bunların arasında ödeme teklifi veya tek seferlik bir ödemeyi elden girmek de bulunmaktadır.
author: kweekley
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3216e0479851e58b345508e27c97b69d8a1077b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236383"
---
# <a name="vendor-payment-overview"></a>Satıcı ödemesine genel bakış

[!include [banner](../../includes/banner.md)]

Bu görev kılavuzu size satıcı ödemeleri oluşturmak için çeşitli yöntemleri gösterecektir. Bunların arasında ödeme teklifi veya tek seferlik bir ödemeyi elden girmek de bulunmaktadır. Bu yordam, USMF demo şirketini kullanır.

1. **Gezinti bölmesi > Modüller > Borç hesapları > Ödemeler > Ödeme günlüğü**'ne gidin.
2. **Yeni**'ye tıklayın.
3. Satıcı ödemelerinin kaydedileceği ödeme günlüğünü seçin. 
4. Bir günlüğü seçin veya el ile girin.
5. **Satırlar**'a tıklayın.
6. **Eylem bölmesinde**, **Ödeme teklifi**'ne tıklayın.
7. **Ödeme teklifi oluştur**'a tıklayın. Ödeme teklif, ödeme için faturaları seçmede kullanılan bir sorgudur. Satıcı ödemelerini oluşturmadan veya yaratmadan önce, ödenecek faturaların listesini düzenleyebilirsiniz.
8. Ödeme için faturaları vade tarihi, nakit iskontosu veya her ikisini birden kullanarak seçin. 
9. Vade tarihi veya nakit iskontosu ile karşılaştırmak için tarihi girin. 
10. İsteğe bağlı: Tüm ödemeler için kullanılacak ödeme tarihi girin. Buraya girilen tarihi, nakit iskontosu tarihi veya vade tarihi ne olursa olsun, tüm ödemeler için geçerli ödeme tarihi olacaktır.  
11. İsteğe bağlı: Ödeme tarihi olarak kullanılabilecek bir minimum ödeme tarihini girin. Minimum ödeme tarihi, ödemeler oluşturulurken kullanılan en erken tarihi olacaktır. Örneğin, bir faturanın vade tarihi, minimum ödeme tarihinden sonraysa, vade tarihi minimum ödeme tarihi yerine vade tarihi ödeme yapmak için kullanılır ve bu sayede faturayı mümkün olan en geç şekilde ödeme imkanı doğar.
12. Ek sorgu kısıtlamalarını, **Dahil edilecek kayıtlar** bölümüne girin. Filtre, genellikle satıcı tarafından ödeme için seçilen faturaları veya ödeme yöntemini kısıtlamakta için kullanılır. Örneğin, bu ödeme işleminde faturaları sadece çek ile ödemek için bir filtre ekleyebilirsiniz.
13. Ek sorgu kısıtlaması veya ödeme varsayılan değerleri girin. Ek parametreler ödemenin yapılacağı para birimini tanımlamada veya merkezi ödemeleri bu ödeme işlemi için etkinleştirmede kullanılabilir.  
14. **Tamam**'a tıklayın. **Tamam**'a tıkladıktan sonra sorgunun sonuçları görünür. Ödenmek üzere seçilen faturaların listesini önizlemek istemiyorsanız, **Parametreler** hızlı sekmesine geri giderek **Ödemeleri fatura önizlemesi olmadan oluştur** ayarını "Evet" olarak değiştirebilirsiniz.  
15. Seçili faturayla ilgili satıcı için oluşturulan ödemeleri görüntülemek için **Ödeme özetini göster** düğmesini seçin.
16. Ödemeleri gizlemek için **Ödeme özetini gizle** düğmesini seçin. 
17. **Ödemeleri oluştur**'a tıklayın. **Ödemeleri oluştur**'u seçmeden önce kılavuza sağ tıklayıp, faturaların listesini Excel'e aktarabilirsiniz. **Ödemeleri oluştur** düğmesi, satıcı ödemelerini ödeme günlüğünde oluşturur.  
18. Ödemelerinizi tarayın ve ödeme yönteminin tüm ödemeler için tanımlanmış olduğundan emin olun. Çek yazdırma ve elektronik ödeme oluşturma gibi ödemeleri oluşturursanız, öncelikle ödeme yöntemini tanımlamalısınız. Ödeme yöntemi aynı zamanda ödemenin yapılacağı banka hesabını da varsayılan olarak ayarlar.  
19. Tek seferlik ödeme oluşturmak için **Yeni**'ye tıklayın. Tek seferlik bir ödeme, deftere nakledilmeden önce herhangi bir zamanda ödeme günlüğüne eklenebilir. Bu, **Ödeme teklifini** kullanmak yerine **Yeni** düğmesine tıklayarak ve ödeme bilgilerini el ile ekleyerek yapılır.  
20. Ödemenin yapılacağı satıcıyı seçin.
21. Ödenecek bir fatura varsa, ödeme için faturayı seçmek için **Hareketleri kapat**'ı seçin. Bu bir ön ödeme ise, bu adım isteğe bağlıdır. Bir fatura seçmeden ödemeyi oluşturabilirsiniz. 
22. Ödenecek faturaları işaretleyin. Ödenecek faturaları seçmek için **Hareketleri kapat**'ı kullanırsanız, ödeme tutarı, otomatik olarak ödeme için işaretlediğiniz faturalara ve **Kapatılacak tutar** bölümüne girdiğiniz tutara göre hesaplanır.
23. **Tamam**'a tıklayın.
24. Bir ödemeyi silmek isterseniz, satırı işaretleyin.
25. **Sil** öğesini tıklayın. Bir ödemeyi silmek yalnızca ödemenin silinmesine neden olur. Ödeme için işaretlenmiş herhangi bir fatura, başka bir ödeme tarafından ödenebilir olmaya devam edecektir.
26. **Evet** seçeneğini tıklatın.
27. Çekleri yazdırmak için **Ödeme oluştur**'u seçin veya elektronik ödeme dosyasını oluşturun.
28. Oluşturmak istediğiniz ödeme türünü seçin. Ödeme günlüğü hem Çekler hem de elektronik ödemeler için ödemeler içerebilir fakat bir seferde sadece bir ödeme türü oluşturabilirsiniz.
29. Ödemeler oluşturmak için kullanmak istediğiniz banka hesabını seçin.
30. **Tamam**'a tıklayın. Ödemeler yalnızca **Ödeme yöntemi** ve seçtiğiniz **Banka hesabı** ile eşleşen ödemeler için oluşturulur.
31. **Çek** oluşturuyorsanız, çekler için doğru yazdırma hedefini sağlamak için **Belge**'yi seçin.
32. **Tamam**'a tıklayın.
33. Ödemeleri oluşturmak için **Tamam**'a tıklayın.
34. Tüm ödemeler onaylanır ve oluşturulursa **Deftere naklet**'e tıklayın. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
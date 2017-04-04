---
title: "Tahmin Temel İstatistik oluştur"
description: "Bu makalede, talep tahmini hesaplamasında kullanılan parametreler ve filtreler hakkında bilgiler verilmektedir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Tahmin Temel İstatistik oluştur

Bu makalede, talep tahmini hesaplamasında kullanılan parametreler ve filtreler hakkında bilgiler verilmektedir. 

Bir temel tahmini oluştururken, öncelikle hesaplamada kullanılan parametreleri ve filtreleri belirtmelisiniz. Örneğin, belli bir şirket için, gelecek ay için ve belli bir seçilen madde grubu için önceki yıla ait hareket verilerine göre talebi tahmin eden bir temel tahmin oluşturabilirsiniz. 

Tahmini bir istek oluşturmak için aşağıdaki adrese gidin **Master planlama &gt;tahmin &gt;talep tahmin &gt;Tahmin oluştur istatistiksel temel**. 

Tahmin aralığı tahmin oluşturma zamanında seçilebilir. Kullanılabilir değerler: Gün, Hafta ve Ay. 

Bir tahminin oluşturulduğu aralıkların sayısı,** Tahmin dönemi** alanında ayarlanır. 

Tahmin stratejisi **Geçmişteki talep üzerine kopyala** olarak ayarlandığında, geçmiş dönem sonu yok sayılır. Sistem belirtilen demetleri sayısını kopyalar **tahmin ufku** alan kümesinde tarihinden başlayarak tahmin talep **tarihinden** altında alan **geçmiş ufku**. Geçmiş talebi belli bir tarihten ileriye doğru kopyalamakla, üretim planlayıcıları sonraki üç aylık dönemin planını iki şekilde yapabilir:

-   Talebi geçen yılki aynı üç aydan başlayarak kopyalamak suretiyle.
-   Talebi önceki üç aydan başlayarak kopyalamak suretiyle.

Üretim planlarında karışıklığı önlemek için, belirli bir sayıda tahmin aralığı dondurulabilir. Bu numara **Dondurma zaman dilimi** alanında ayarlanır. **Düzeltilmiş talep tahmini **sayfasında, dondurulan aralık hücreleri, bu değerlerin değiştirilmemesi gerektiğine dair görsel bir uyarı vermek için devre dışı bırakılır. 

Temel Talep tahmini için başlangıç tarihinin geçerli tarih veya gelecekteki bir tarih olması gerekmez. Farklı bir başlangıç tarihi ayarlamak için, **Temel tahmin Başlangıç tarihi - Başlangıç tarihi** alanı. Örneğin, Haziran ayında, kullanıcılar gelecek yıl için tahmin oluşturabilir. Geçmiş talebin sonu ile temel başlangıcı arasındaki tahmin aralıkları eksik olduğu için, öngörüler doğru olmayabilir. Microsoft Dynamics 365 işlemleri Talep tahmini hizmeti kullanıyorsanız, eksik boşlukları doldurmak için dört yolu vardır. EKSİK ayarlayarak istediğiniz yöntemi seçebilirsiniz\_değer\_yerine KOYMA parametresi **isteğe bağlı parametreleri tahmin** sayfa. 

**Temel başlangıç tarihini tahmin** - **tarihinden** tahmin kova, örneğin, başlangıcına kadar Amerika Birleşik Devletleri'nde bir pazar hafta tahmin kova ise ayarlanacak alanı vardır. Sistem otomatik olarak ayarlar **temel başlangıç tarihini tahmin** - **tarihinden** tahmin kova başlangıcını eşleştirmek için alan. 

**Temel başlangıç tarihini tahmin** - **tarihinden** alan, geçmişteki bir tarih için ayarlanabilir. Diğer bir deyişle, geçmişte bir talep tahminini oluşturmak mümkündür. Bu işlem, kullanıcıların tahmin hizmet parametrelerinde geçmişte üretilen istatistiksel tahminin gerçek geçmiş talebiyle eşleşecek şekilde ufak düzeltmeler yapmasına olanak verdiği için yararlıdır. Daha sonra kullanıcılar geleceğe yönelik istatistik temel tahmini oluşturmak için bu parametre ayarlarını kullanmaya devam edebilir. 

**Manüel ayarlamaları talep tahminine aktar** onay kutusu seçiliyse, önceki talep tahmini yinelemelerinde yapılan manüel ayarlamalar, yeni temel tahmine otomatik olarak uygulanabilir. Onay kutusu temizlenirse, manüel ayarlamalar temel tahmine eklenmez, ancak silinmezler. Bir tahminde yapılan manüel ayarlamalar, yalnızca tahmini içe aktarma sırasında, **Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusundaki işaret kaldırılarak silinebilir. Manüel ayarlamalar yetkilendirme anında kaydedilir. Bu nedenle, bir kullanıcı, tahmin için el ile ayarlama yapar ancak tahmine Dynamics 365 işlemleri için yetki vermez, değişiklikler kaybolur. El ile ayarlama ve nasıl çalıştıkları hakkında daha fazla bilgi için bkz: [ayarlanmış tahmin yetkilendirme](authorize-adjusted-forecast.md). 

Talep tahmini oluşturmada, kullanıcıların oluşturulan tahmini tanımalarına yardımcı olacak bir ad ve yorumlar bulunabilir. Bu değerler **İstatistik temel tahmin oluşturma geçmişi** sayfasındaki tahmin oluşturma geçmişinde görülür. 

Tahmin oluşturma zamanında şirketlerarası planlama grubu, madde tahsisat anahtarları ve diğer filtreler uygulanabilir. Bunlar, performansı artırmak veya verileri yönetilebilir parçalara bölmek için kullanılabilir. Ancak, sorguda madde tahsisat anahtarı seçilse bile, şirketlerarası planlama grubu ile ilişkili olmayan hiçbir madde tahsisat anahtarının üyeleri için bir talep tahmini oluşturulmayacağını unutmayın. 

**İpucu**: Bazen kullanıcılar bir talep tahmini oluştururken veya tahmin oluşturma hiçbir oturum günlüğü olmadan tamamlandığında hata iletisi alabilir. Bu durum, daha önce tahmin oluşturmak için kullanılan sorguda arda kalan veriler nedeniyle oluşabilir. Bu sorunu gidermek amacıyla, **Sorgu** sayfasını açmak için **Seç** öğesine tıklayın, **Sıfırla** öğesine tıklayın ve sonra temel tahmini yeniden oluşturun. 

Tahmin büyük öğeler kümesi için ancak, örneğin, bir öğe veya bir madde tahsisat anahtarı için bir kerede oluşturulmaz sonra daha iyi performans almak için seçebileceğiniz **istek yanıt modu kullan** onay kutusunu **Master planlama - Setup - Talep tahmini** - **isteğe bağlı parametreler - Azure makine öğrenme tahmin** sekme.

<a name="see-also"></a>Ayrıca bkz.
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)



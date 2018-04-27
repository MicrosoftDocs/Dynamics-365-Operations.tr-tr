---
title: "Bir istatistik temel tahmin oluştur"
description: "Bu makalede, talep tahmini hesaplamasında kullanılan parametreler ve filtreler hakkında bilgiler verilmektedir."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c71d7632cfdafe48eee49c848982dfa85116df75
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="generate-a-statistical-baseline-forecast"></a>Bir istatistik temel tahmin oluştur

[!INCLUDE [banner](../includes/banner.md)]

Bu makalede, talep tahmini hesaplamasında kullanılan parametreler ve filtreler hakkında bilgiler verilmektedir. 

Bir temel tahmini oluştururken, öncelikle hesaplamada kullanılan parametreleri ve filtreleri belirtmelisiniz. Örneğin, belli bir şirket için, gelecek ay için ve belli bir seçilen madde grubu için önceki yıla ait hareket verilerine göre talebi tahmin eden bir temel tahmin oluşturabilirsiniz. 

Bir talep tahmini oluşturmak için **Master planlama &gt; Tahmin &gt; Talep tahmini &gt; İstatistik temel tahmin oluştur** menüsüne gidin. 

Tahmin aralığı tahmin oluşturma zamanında seçilebilir. Kullanılabilir değerler: Gün, Hafta ve Ay. 

Bir tahminin oluşturulduğu aralıkların sayısı,**Tahmin dönemi** alanında ayarlanır. 

Tahmin stratejisi **Geçmişteki talep üzerine kopyala** olarak ayarlandığında, geçmiş dönem sonu yok sayılır. Sistem, **Tahmin dönemi** alanında belirtilen aralıkların sayısını **Geçmiş dönem** öğesi altındaki **Başlangıç tarihi** alanından başlayarak tahmini talebe kopyalar. Geçmiş talebi belli bir tarihten ileriye doğru kopyalamakla, üretim planlayıcıları sonraki üç aylık dönemin planını iki şekilde yapabilir:

-   Talebi geçen yılki aynı üç aydan başlayarak kopyalamak suretiyle.
-   Talebi önceki üç aydan başlayarak kopyalamak suretiyle.

Üretim planlarında karışıklığı önlemek için, belirli bir sayıda tahmin aralığı dondurulabilir. Bu numara **Dondurma zaman dilimi** alanında ayarlanır. **Düzeltilmiş talep tahmini** sayfasında, dondurulan aralık hücreleri, bu değerlerin değiştirilmemesi gerektiğine dair görsel bir uyarı vermek için devre dışı bırakılır. 

Temel Talep tahmini için başlangıç tarihinin geçerli tarih veya gelecekteki bir tarih olması gerekmez. Farklı bir başlangıç tarihi ayarlamak için, **Temel tahmin Başlangıç tarihi - Başlangıç tarihi** alanı. Örneğin, Haziran ayında, kullanıcılar gelecek yıl için tahmin oluşturabilir. Geçmiş talebin sonu ile temel başlangıcı arasındaki tahmin aralıkları eksik olduğu için, öngörüler doğru olmayabilir. Microsoft Dynamics 365 for Finance and Operations Talep tahmini hizmeti kullanıyorsanız, eksik boşlukları doldurabileceğiniz dört yolu vardır. İstediğiniz yöntemi **Talep tahmini parametreleri** sayfasındaki MISSING\_VALUE\_SUBSTITUTION parametresini ayarlayarak seçebilirsiniz. 

**Temel tahmin başlangıç tarihi** - **Başlangıç tarihi** alanının, bir tahmin aralığının başlangıcına, örneğin ABD'de, tahmin aralığı hafta ise, Pazar gününe ayarlanması gerekir. Sistem, **Temel tahmin başlangıç tarihi** - **Başlangıç tarihi** alanını bir tahmin aralığının başlangıcıyla eşleşecek şekilde otomatik olarak ayarlar. 

**Temel tahmin başlangıç tarihi** - **Başlangıç tarihi** alanı geçmişteki bir tarihe ayarlanabilir. Diğer bir deyişle, geçmişte bir talep tahminini oluşturmak mümkündür. Bu işlem, kullanıcıların tahmin hizmet parametrelerinde geçmişte üretilen istatistiksel tahminin gerçek geçmiş talebiyle eşleşecek şekilde ufak düzeltmeler yapmasına olanak verdiği için yararlıdır. Daha sonra kullanıcılar geleceğe yönelik istatistik temel tahmini oluşturmak için bu parametre ayarlarını kullanmaya devam edebilir. 

**Manüel ayarlamaları talep tahminine aktar** onay kutusu seçiliyse, önceki talep tahmini yinelemelerinde yapılan manüel ayarlamalar, yeni temel tahmine otomatik olarak uygulanabilir. Onay kutusu temizlenirse, manüel ayarlamalar temel tahmine eklenmez, ancak silinmezler. Bir tahminde yapılan manüel ayarlamalar, yalnızca tahmini içe aktarma sırasında, **Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusundaki işaret kaldırılarak silinebilir. Manüel ayarlamalar yetkilendirme anında kaydedilir. Bu nedenle, bir kullanıcı, tahminde manüel ayarlamalar yapar, ancak tahmini Finance and Operations'ta yeniden yetkilendirmezse, değişiklikler kaybolur. Manüel ayarlamalar ve bunların çalışma şekilleri hakkında daha fazla bilgi için, bkz. [Ayarlanmış tahmini yetkilendirme](authorize-adjusted-forecast.md). 

Talep tahmini oluşturmada, kullanıcıların oluşturulan tahmini tanımalarına yardımcı olacak bir ad ve yorumlar bulunabilir. Bu değerler **İstatistik temel tahmin oluşturma geçmişi** sayfasındaki tahmin oluşturma geçmişinde görülür. 

Tahmin oluşturma zamanında şirketlerarası planlama grubu, madde tahsisat anahtarları ve diğer filtreler uygulanabilir. Bunlar, performansı artırmak veya verileri yönetilebilir parçalara bölmek için kullanılabilir. Ancak, sorguda madde tahsisat anahtarı seçilse bile, şirketlerarası planlama grubu ile ilişkili olmayan hiçbir madde tahsisat anahtarının üyeleri için bir talep tahmini oluşturulmayacağını unutmayın. 

**İpucu**: Bazen kullanıcılar bir talep tahmini oluştururken veya tahmin oluşturma hiçbir oturum günlüğü olmadan tamamlandığında hata iletisi alabilir. Bu durum, daha önce tahmin oluşturmak için kullanılan sorguda arda kalan veriler nedeniyle oluşabilir. Bu sorunu gidermek amacıyla, **Sorgu** sayfasını açmak için **Seç** öğesine tıklayın, **Sıfırla** öğesine tıklayın ve sonra temel tahmini yeniden oluşturun. 

Tahmin büyük öğeler kümesi için oluşturulmamış, ancak söz gelimi, bir öğe veya bir madde tahsisat anahtarı için bir kerede oluşturulmuşsa, bu durumda daha iyi performans almak için, **Master planlama - Ayar - Talep tahmini** - **Talep tahmini parametreleri - Azure Machine Learning** sekmesindeki **Talep yanıt modunu kullan** onay kutusunu seçebilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Talep tahmini kurulumu](demand-forecasting-setup.md)

[Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)

[Ayarlanmış tahmini yetkilendirme](authorize-adjusted-forecast.md)





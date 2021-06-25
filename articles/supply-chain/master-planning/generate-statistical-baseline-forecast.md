---
title: İstatistik temel tahmini oluşturma
description: Bu konu, talep tahmini hesaplamasında kullanılan parametreler ve filtreler hakkında bilgiler verilmektedir.
author: roxanadiaconu
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 780d1e1307b69ec9a31d032039970de454160d6f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189704"
---
# <a name="generate-a-statistical-baseline-forecast"></a>İstatistik temel tahmini oluşturma

[!include [banner](../includes/banner.md)]

Bu konu, talep tahmini hesaplamasında kullanılan parametreler ve filtreler hakkında bilgiler verilmektedir. 

Bir temel tahmini oluştururken, öncelikle hesaplamada kullanılan parametreleri ve filtreleri belirtmelisiniz. Örneğin, belli bir şirket için, gelecek ay için ve belli bir seçilen madde grubu için önceki yıla ait hareket verilerine göre talebi tahmin eden bir temel tahmin oluşturabilirsiniz. 

Bir talep tahmini oluşturmak için **Master planlama &gt; Tahmin &gt; Talep tahmini &gt; İstatistik temel tahmin oluştur** menüsüne gidin. 

Tahmin aralığı tahmin oluşturma zamanında seçilebilir. Kullanılabilir değerler: Gün, Hafta ve Ay. 

Bir tahminin oluşturulduğu aralıkların sayısı,**Tahmin dönemi** alanında ayarlanır. 

Tahmin stratejisi **Geçmişteki talep üzerine kopyala** olarak ayarlandığında, geçmiş dönem sonu yok sayılır. Sistem, **Tahmin dönemi** alanında belirtilen aralıkların sayısını **Geçmiş dönem** öğesi altındaki **Başlangıç tarihi** alanından başlayarak tahmini talebe kopyalar. Geçmiş talebi belli bir tarihten ileriye doğru kopyalamakla, üretim planlayıcıları sonraki üç aylık dönemin planını iki şekilde yapabilir:

-   Talebi geçen yılki aynı üç aydan başlayarak kopyalamak suretiyle.
-   Talebi önceki üç aydan başlayarak kopyalamak suretiyle.

Üretim planlarında karışıklığı önlemek için, belirli bir sayıda tahmin aralığı dondurulabilir. Bu numara **Dondurma zaman dilimi** alanında ayarlanır. **Düzeltilmiş talep tahmini** sayfasında, dondurulan aralık hücreleri, bu değerlerin değiştirilmemesi gerektiğine dair görsel bir uyarı vermek için devre dışı bırakılır. 

Temel Talep tahmini için başlangıç tarihinin geçerli tarih veya gelecekteki bir tarih olması gerekmez. Farklı bir başlangıç tarihi ayarlamak için, **Temel tahmin Başlangıç tarihi - Başlangıç tarihi** alanı. Örneğin, Haziran ayında, kullanıcılar gelecek yıl için tahmin oluşturabilir. Geçmiş talebin sonu ile temel başlangıcı arasındaki tahmin aralıkları eksik olduğu için, öngörüler doğru olmayabilir. Talep tahmini hizmeti kullanıyorsanız, eksik boşlukları doldurmak için dört yol vardır. İstediğiniz yöntemi **Talep tahmini parametreleri** sayfasındaki MISSING\_VALUE\_SUBSTITUTION parametresini ayarlayarak seçebilirsiniz. 

> [!NOTE]
> Eksik değer değiştirme yalnızca geçmişe ait verilerin başlangıç ve bitiş tarihleri arasındaki boşluklar için çalışır. Veri, son fiziksel veri noktasından önce veya sonra doldurmaz, yalnızca gerçek mevcut veri noktaları arasında tahmin edilecek şekilde işlev gösterir. 

**Temel tahmin başlangıç tarihi** - **Başlangıç tarihi** alanının, bir tahmin aralığının başlangıcına, örneğin ABD'de, tahmin aralığı hafta ise, Pazar gününe ayarlanması gerekir. Sistem, **Temel tahmin başlangıç tarihi** - **Başlangıç tarihi** alanını bir tahmin aralığının başlangıcıyla eşleşecek şekilde otomatik olarak ayarlar. 

**Temel tahmin başlangıç tarihi** - **Başlangıç tarihi** alanı geçmişteki bir tarihe ayarlanabilir. Diğer bir deyişle, geçmişte bir talep tahminini oluşturmak mümkündür. Bu işlem, kullanıcıların tahmin hizmet parametrelerinde geçmişte ayarlanan istatistiksel tahminin gerçek geçmiş talebiyle eşleşecek şekilde ufak düzeltmeler yapmasına olanak verdiği için yararlıdır. Daha sonra kullanıcılar geleceğe yönelik istatistik temel tahmini oluşturmak için bu parametre ayarlarını kullanmaya devam edebilir. 

**Manüel ayarlamaları talep tahminine aktar** onay kutusu seçiliyse, önceki talep tahmini yinelemelerinde yapılan manüel ayarlamalar, yeni temel tahmine otomatik olarak uygulanabilir. Onay kutusu temizlenirse, manüel ayarlamalar temel tahmine eklenmez, ancak silinmezler. Bir tahminde yapılan manüel ayarlamalar, yalnızca tahmini içe aktarma sırasında, **Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusundaki işaret kaldırılarak silinebilir. Manüel ayarlamalar yetkilendirme anında kaydedilir. Bu nedenle, bir kullanıcı, tahminde manüel ayarlamalar yapar, ancak tahmini Supply Chain Management'ta yeniden yetkilendirmezse, değişiklikler kaybolur. El ile düzeltmeler ve bunların çalışma şekilleri hakkında daha fazla bilgi için bkz. [Düzeltilen tahmini yetkilendirme](authorize-adjusted-forecast.md). 

Talep tahmini oluşturmada, kullanıcıların oluşturulan tahmini tanımalarına yardımcı olacak bir ad ve yorumlar bulunabilir. Bu değerler **İstatistik temel tahmin oluşturma geçmişi** sayfasındaki tahmin oluşturma geçmişinde görülür. 

Tahmin oluşturma zamanında şirketlerarası planlama grubu, madde tahsisat anahtarları ve diğer filtreler uygulanabilir. Bunlar, performansı artırmak veya verileri yönetilebilir parçalara bölmek için kullanılabilir. Ancak, sorguda madde tahsisat anahtarı seçilse bile, şirketlerarası planlama grubu ile ilişkili olmayan hiçbir madde tahsisat anahtarının üyeleri için bir talep tahmini oluşturulmayacağını unutmayın. 

> [!TIP]
> Bazen kullanıcılar bir talep tahmini oluştururken veya tahmin oluşturma hiçbir oturum günlüğü olmadan tamamlandığında hata iletisi alabilir. Bu durum, daha önce tahmin oluşturmak için kullanılan sorguda arda kalan veriler nedeniyle oluşabilir. Bu sorunu gidermek amacıyla, **Sorgu** sayfasını açmak için **Seç** öğesini seçin, **Sıfırla** öğesine tıklayın ve sonra temel tahmini yeniden oluşturun. 

Tahmin büyük öğeler kümesi için oluşturulmamış, ancak söz gelimi, bir öğe veya bir madde tahsisat anahtarı için bir kerede oluşturulmuşsa, bu durumda daha iyi performans almak için, **Master planlama - Ayar - Talep tahmini** - **Talep tahmini parametreleri - Azure Machine Learning** sekmesindeki **Talep yanıt modunu kullan** onay kutusunu seçebilirsiniz.

> [!NOTE]
> Potansiyel olarak sabit görünümlü bir tahmin daha uzun bir tarihsel zaman diliminde olması gereken tarihsel verilerden kaynaklanabilir (aylık tahmini ile 3 yıl gibi bir model seçmek için en az 3 zaman dilimi). Daha iyi sonuç elde etmek için zaman aralığının parçalı yapısını değiştirmeyi deneyebilir veya zaman aralığını artırabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

- [Talep tahmini kurulumu](demand-forecasting-setup.md)

- [Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)

- [Düzeltilen tahmini yetkilendirme](authorize-adjusted-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
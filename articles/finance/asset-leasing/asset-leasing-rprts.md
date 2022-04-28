---
title: Varlık kiralama raporları
description: Bu konuda, Varlık kiralamaları için kullanılabilen raporlar listelenmekte ve kısaca açıklanmaktadır.
author: moaamer
ms.date: 04/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cb1c994fee6efff82dd1cba1e71c6af49b384208
ms.sourcegitcommit: 722854cb0d302d01ce3d9580ac80dc7c23d19bf5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/06/2022
ms.locfileid: "8550053"
---
# <a name="asset-leasing-reports"></a>Varlık kiralama raporları

[!include [banner](../includes/banner.md)]

Bu konuda, Varlık kiralamaları için kullanılabilen raporlar listelenmekte ve kısaca açıklanmaktadır. Çoğu rapor, belirtildiği gibi bu adımları veya bunlara çok benzer adımları tamamlayarak görüntülenir. 

- Çoğu varlık kiralama raporunu görüntülemek için **Varlık Kiralama > Sorgular ve raporlar > Kiralama raporları**'na gidin ve ardından görüntülenecek bir rapor seçin. Farklı seçim yolu gerektiren raporlarda, raporu açma adımları raporun açıklamasına eklenir. 
- Yazdırılacak raporu seçtiğinizde, rapora dahil edilen bilgileri filtrelemenizi sağlayan bir parametreler sayfası açılır. Filtre ölçütlerini girin ve raporu oluşturmak için **Tamam**'ı seçin. Oluşturulan rapor, belirttiğiniz filtreler kapsamındaki bilgileri gösterir.

## <a name="asset-movement"></a>Kıymet hareketi
Varlık hareketi raporu, her kiralamanın kullanım hakkı varlığı bakiyeleri için ileri taşıma raporu görevi görür. Bu rapor, belirli bir dönem boyunca bir kiralamanın varlık hareketlerini görüntülemenizi sağlar. Rapor aşağıdaki alanları içerir. 

|     Rapor alanları                  |     Tanım                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Başlangıç tarihi              |     Kiralamanın en eski sürümünün başlangıç tarihi.                     |   
|     Kiralama süresi                     |     Kiralama süresinin mevcut sürümü.                            |
|     Kısa süreli Kiralama               |     Kiralama kısa süreli kiralama olarak sınıflandırılmışsa bu alanda **Evet** değeri görünür.         |
|     Düşük değerli Kiralama                |     Kiralama düşük değerli kiralama olarak sınıflandırılmışsa bu alanda **Evet** değeri görünür.          |
|     Başlangıçtaki kullanım hakkı varlığı     |     İlk kabul günlüğü girişindeki kullanım hakkı varlığının asıl değeri.      |
|     Başlangıç bakiyesi              |     **Başlangıç tarihi** itibarıyla kullanım hakkı varlığının net defter değeri.                         |
|     Dönem amortisman gideri    |     Rapor için tanımlanan tarih aralığı içinde alınan amortisman gideri tutarı.        |
|     Birikmiş amortisman       |     **Başlangıç tarihi** itibarıyla birikmiş amortisman tutarı.                               |
|     Değer düşüşü                     |     Rapor için tanımlanan tarih aralığı içinde varlığın değerinin düşme tutarı.               |
|     Değişiklikler                  |     Tarih parametreleri arasında kullanım hakkı varlığındaki düzeltmelerin tutarı.                            |
|     Net defter değeri                 |     **Bitiş tarihi** itibarıyla net birikmiş tutarı olan kullanım hakkı varlığının son net defter değeri.    |

## <a name="differences-report"></a>Fark raporu
Farklar raporu, Kiralama içeri aktarma çerçevesine yüklenen bilgiler ile sistemdeki güncel bilgiler arasındaki farkları gösterir. Bu, Kiralama içeri aktarma çerçevesi aracılığıyla düzeltilmiş, güncelleştirilmiş veya eklenmiş bilgileri karşılaştırmanıza olanak sağlar.  

Rapordaki değerler seçilen kiralamaya göre değişir. Rapor yalnızca sistemde var olan ile hazırlama tabloları arasında farklı olan alanları gösterir. Eski değer, içeri aktarma işleminin çalıştırılıp çalıştırılmamasına bağlı olarak o an sistemde var olan değer veya geçmişte sistemde olan değerdir. Yeni değer, eski değerin yerini alacak hazırlama tablosundaki değeri gösterir.

## <a name="five-years-undiscounted-payment-forecast"></a>Beş yıllık iskontosuz ödeme tahmini
Beş yıllık iskontosuz ödeme tahmini raporu, rapor parametrelerinde belirtilen tarihten sonraki beş yıl içinde ödenecek iskontosuz tahmini kira ödemelerini gösterir. Rapor aşağıdaki alanları içerir. 

|     Rapor alanları         |     Tanım                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Kiralama Açıklaması     |     Kiralama üst bilgisindeki kiralama açıklaması.                                                      |
|     Kiralama kodu              |     Benzersiz kiralama kodu.                                                                              |
|     Rezerve et                  |     Defter koduyla ilişkilendirilmiş kiralama defteri.                                                         |
|     Sınıflandırma        |     Kiralama sınıflandırması.                                                                  |
|     Deftere Nakletme Katmanı         |     Bu kiralamanın deftere nakledildiği katman.                                                         |
|     Para Birimi              |     Kira para birimi.                                                                        |
|     Cari               |     Raporlama tarihinden sonraki 12 ay içinde ödenecek tüm kira ödemelerinin toplamı.          |
|     13-24 Ay          |     Raporlama tarihinden itibaren 13-24 ay arasında ödenecek tüm kira ödemelerinin toplamı.           |
|     25-36 Ay          |     Raporlama tarihinden itibaren 25-36 ay arasında ödenecek tüm kira ödemelerinin toplamı.           |
|     37-48 Ay          |     Raporlama tarihinden itibaren 37-48 ay arasında ödenecek tüm kira ödemelerinin toplamı.           |
|     49-60 Ay          |     Raporlama tarihinden itibaren 49-60 ay arasında ödenecek tüm kira ödemelerinin toplamı.           |
|     Sonrasında            |     Raporlama tarihinde veya raporlama tarihinden 61 ay sonra ödenecek tüm kira ödemelerinin toplamı.              |

## <a name="gaap-cash-flows-report"></a>GAAP nakit akışları raporu
GABH bilgileri açıklama raporu, 842-20-50-4(g)(1) ile açıklanan ABD GAAP bilg açıklama gereksinimini karşılar. Bu raporu görüntülemek için **Varlık kiralama > Sorgular ve raporlar > Bilgi Açıklama > GAAP – nakit akışları** bölümüne gidin. 

|     Rapor alanları                                 |     Tanım                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Başlangıç tarihi <br> Bitiş tarihi                        |     Rapora dahil edilen bilgileri kısıtlamak için kullanılan tarih aralığını tanımlar.      |
|     Tüzel Kişilik                                  |     Kiralamaların bağlı olduğu tüzel kişilik.                                      |
|     Kiralama Türü                                    |     Kiralamanın sınıflandırması (finansal kiralama veya işletme kiralaması).           |
|     Kiralama kodu                                      |     Benzersiz kiralama kodu.                                                      |
|     Kiralama Açıklaması                             |     Kiralama üst bilgisindeki kiralama açıklaması.                              |
|     Kiralama Defteri                                    |     Satırın başvurduğu kiralama defteri.                        |
|     Deftere Nakletme Katmanı                                 |     Sabit bir değere bağlı her defter genel amortisman amacını içeren belirli bir nakil katmanı için ayarlanır.                          |
|     Kiralama Grubu                                   |     Kiralamanın bağlı olduğu grup.                                     |
|     Para Birimi                                      |     Kullanılan işlem para biriminin kısaltması. Tüm raporlar, işlem para birimini raporlama para birimine dönüştürür.                      |
|     Finansal Kiralamalar - İşletme Nakit Akışları         |     Tarih parametreleri arasında deftere nakledilen değişken ödemelerin toplamı ve amortisman planlamasındaki toplam faiz ödemeleri.        |
|     Finansal Kiralamalar - Finans Nakit Akışları           |     Tarih parametreleri arasında amortisman planlamasından toplam anapara ödemelerinin toplamı.       |
|     İşletme Kiralamaları - İşletme Nakit Akışları       |     Tarih parametreleri arasında deftere nakledilen tüm kira ödemelerinin toplamı ve deftere nakledilen değişken ödemeler.            |

## <a name="lease-balances-forecast"></a>Kiralama bakiyeleri tahmini
Kiralama bakiyeleri tahmini, doğrudan yükümlülük amortisman planlaması ve varlık amortisman planındaki bilgileri listeler. Rapor, belirli bir süre için tahmini kiralama yükümlülüğü ve kullanım hakkı varlıklarının tahmini tutarlarını (bu kiralamalar için tüm tahmini giderler dahil) gösterir. Rapor aşağıdaki alanları içerir.

|     Rapor alanları                 |     Tanım                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Başlangıç bakiyesi             |     Raporun başlangıç tarihini içeren dönem için kiralama amortismanı planındaki başlangıç bakiyesi.            |
|     Başlangıçtaki kabul           |     Kiralamanın başlangıç tarihi, rapor için tanımlanan tarih aralığına denk gelirse bu sütunda ilk kabul günlüğü girişinin kiralama hesabı değeri gösterilir.      |
|     Ödemeler                      |     Rapor için tanımlanan tarih aralığı içinde kalan kira ödemelerinin toplamı.                               |
|     İlgi Alanı                      |     Rapor için tanımlanan tarih aralığı içinde kalan kiralama faiz giderlerinin toplamı.                    |
|     Kapanış bakiyesi                |     **Bitiş tarihi** itibarıyla kiralamanın yükümlülük bakiyesi.                                                             |
|     Kısa süreli yükümlülük          |     **Bitiş tarihi** itibarıyla kiralama amortisman planlamasındaki kısa süreli yükümlülük tutarı.                           |
|     Uzun vadeli pasif           |     **Bitiş tarihi** itibarıyla kiralama amortisman planlamasındaki uzun süreli yükümlülük tutarı.                            |
|     Başlangıç Net Defter Değeri      |     Raporun başlangıç tarihini içeren dönem için kiralamanın varlık amortisman planındaki "Başlangıç Net Defter Değeri"      |
|     Başlangıçtaki kabul           |     Kiralamanın başlangıç tarihi, raporun tarih parametreleri arasında olursa bu sütunda ilk kabul günlüğü girişinin varlık hesabı değeri gösterilir.            |
|     Amortisman gideri          |     Rapor için tanımlanan tarih aralığı içinde kalan kiralamanın amortisman giderlerinin toplamı.                  |
|     Kapanış bakiyesi                |     **Bitiş tarihi** itibarıyla kiralamanın varlık bakiyesi.                                                              |
|     Öz varlık düzeltmesi             |     Başlangıç bakiyesi eksi başlangıç net defter değeri.                                                             |

## <a name="lease-commencements-report"></a>Kiralama başlangıçları raporu
Kiralama başlangıçları raporu, belirli bir tarih aralığında içinde başlayan tüm kiralamaları (başlangıç yükümlüğü ve kullanım hakkı varlığı bakiyeleri dahil) gösterir. Rapor aşağıdaki alanları içerir. 

|     Rapor alanları                 |     Tanım                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Başlangıç Tarihi             |     Belirli bir kiralama sürümü için deftere nakledilen ilk kabul günlüğü girişinin tarihi.         |
|     Başlangıçtaki pasif tutarı      |     İlk kabul günlüğü girişindeki yükümlülük tutarı.                                  |
|     Başlangıçtaki kıymet tutarı          |     İlk kabul günlüğü girişindeki varlık tutarı.                                      |

## <a name="lease-modification-report"></a>Kiralama değiştirme raporu
Kiralama değiştirme raporu, belirli bir tarih aralığında değiştirilmiş olan tüm kiralamaları gösterir. Raporda ayrıca kirayı değiştiren kullanıcı ve düzeltilen toplam yükümlülük tutarı da gösterilir. Rapor aşağıdaki alanları içerir. 

|     Rapor alanları                 |     Tanım           |
|---------------------------------  |-------------------------  |
|     Düzelten                   |     Kiralamayı değiştiren kişinin kullanıcı adı.                                |
|     Düzeltme tarihi               |     Düzeltme günlük girişinin deftere nakledildiği tarih.                        |
|     Düzeltmeler                   |     Tarih parametreleri arasında kiralama yükümlülüğü hesabına nakledilen tüm düzeltme günlük girişlerinin tutarı. Alacaklar pozitif, borçlar ise negatif olarak gösterilir.       |
|     Kazanç (kayıp) tutarı            |     Tarih parametreleri arasında kiralamanın kazanç/kayıp hesabına nakledilen tüm düzeltme günlük girişlerinin tutarı. Alacaklar pozitif, borçlar ise negatif olarak gösterilir.       |
|     Yedek akçe             |     Tarih parametreleri arasında kiralamanın kalan kazançlar hesabına nakledilen tüm düzeltme günlük girişlerinin tutarı.      |
|     Son pasif bakiyesi      |     Kiralamanın düzeltme tarihi itibarıyla sonuçta elde edilen yükümlülük bakiyesi.           |

## <a name="lease-movement-report"></a>Kiralama hareketi raporu
Kiralama hareketi raporu, her kiralamanın kiralama yükümlülüğü bakiyeleri için ileri taşıma raporu görevi görür. Bu rapor, kullanıcının belirli bir dönem içinde bir kiralamanın yükümlülük hareketleri görüntülemesini sağlar.

|     Rapor alanları             |     Tanım                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Başlangıç tarihi         |     Kiralamanın en eski sürümünün başlangıç tarihi.    |
|     Kiralama süresi                |     Kiralamanın en eski sürümünün kiralama süresi.           |
|     Kalan ödemeler        |     Henüz kiralama için deftere nakledilmeyen ödemelerin sayısı.                       |
|     Başlangıç bakiyesi         |     Raporun başlangıç tarihinden önce oluşan ve kiralama yükümlülüğünü etkileyen tüm hareketlerin toplamı.             |
|     Başlangıçtaki kabul       |     Rapor için tanımlanan tarih aralığı içinde deftere nakledilmiş olan kiralama ilk kabul hareketlerinin tutarı.     |
|     Ödemeler                  |     Rapor için tanımlanan tarih aralığı içinde deftere nakledilen kira ödeme hareketlerinin toplamı. Ödemeler kiralamanın yükümlülük bakiyesini azalttığından, bu sütundaki değerler negatif tutarlar olarak gösterilir.  |
|     İlgi Alanı                  |     Rapor için tanımlanan tarih aralığı içinde kiralamaya göre deftere nakledilen faiz tahakkuklarının toplamı.            |
|     Düzeltmeler               |     Rapor için tanımlanan tarih aralığı içinde kiralamanın deftere nakledilen düzeltme hareketlerinin toplamı.                               |
|     Kapanış bakiyesi            |     Raporun **Bitiş tarihi** itibarıyla deftere nakledilen tüm kiralama yükümlülük hareketlerinin bakiyesi.                  |

## <a name="lease-transactions-report"></a>Kiralama hareketleri raporu
Kiralama hareketleri sorgusu, Varlık kiralama tarafından oluşturulan tüm günlük girişlerini gösterir. Her bir günlük girişi, oluşturulduğu defter koduna bağlıdır. Bu sayede günlük girişini ilgili kiralamayla kolayca ilişkilendirebilirsiniz. Kiralama hareketleri sorgusu, Genel muhasebedeki **Fiş hareketleri**'ne benzer şekilde çalışır.

## <a name="weighted-average-discount-rate-report"></a>Ağırlıklı ortalama iskonto oranı raporu
Ağırlıklı ortalama iskonto oranı raporu, ağırlıklı ortalama iskonto oranı için ASC 842-20-50-4(g)(4) ile belirtilen ABD GAAP bilgi açıklama gereksinimini karşılar. Bu raporu görüntülemek için **Varlık kiralama > Sorgular ve raporlar > Bilgi Açıklama > Ağırlıklı ortalama iskonto oranı** bölümüne gidin. Rapor aşağıdaki alanları içerir. 

|     Rapor alanları                     |     Tanım                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Başlangıç tarihi                        |     Bu rapor, **Başlangıç** tarih parametresinde başlayan veya bu tarihten önceki tüm kiralamaları içerir. Bu rapor, açıklanacak dönemin son günü itibarıyla çalıştırılmalıdır.      |
|     Tüzel kişilik                      |     Kiralamaya bağlı olan tüzel kişilik.                           |
|     Kiralama kodu                          |     Benzersiz kiralama kodu.                                                  |
|     Kiralama açıklaması                 |     Kiralama üst bilgisindeki kiralama açıklaması.                          |
|     Rezerve et                              |     Görüntülenen kiralamanın belirli defter türü.                                                                                                                                            |
|     Deftere nakil katmanı                     |     Sabit bir değere bağlı her defter genel amortisman amacını içeren belirli bir nakil katmanı için ayarlanır.      |
|     Kiralama grubu                       |     Kiralamanın ait olduğu grup.                                 |
|     İskonto oranı                     |     Kira ödemelerine iskonto uygulamak için kullanılan oran.                             |
|     Para Birimi                          |     Kullanılan işlem para biriminin kısaltması. Tüm raporlar, işlem para birimini raporlama para birimine dönüştürür.  |
|     Kalan kira ödemeleri          |     **Başlangıç** tarihi itibarıyla ödeme planındaki kalan ödenmemiş kira ödemelerinin toplam tutarı.            |
|     Kalan ağırlıklı ödemeler       |     Kullanılan iskonto oranıyla çarpılmış kalan kira ödemeleri.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

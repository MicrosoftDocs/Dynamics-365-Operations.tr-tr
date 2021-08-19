---
title: Varlık kiralamaya başlama
description: Bu konu, Varlık kiralama özelliğini açıklar ve varlık kiralaması oluşturma ve bu kiralamalarla ilgili bilgileri görüntüleme adımları konusunda rehberlik sağlar.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeasingWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "4464"
- intro-internal
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40e2bb78e6a4db51f61f4197a9cd444226e7f71b012468274b85306bb8f185d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726146"
---
# <a name="asset-leasing-get-started"></a>Varlık kiralamaya başlama

[!include [banner](../includes/banner.md)]

Bu konu, Varlık kiralama özelliğini açıklar ve varlık kiralaması oluşturma ve bu kiralamalarla ilgili bilgileri görüntüleme adımları konusunda rehberlik sağlar. Konu ayrıca kullanıcı arabiriminde ve belgelerinde kullanılan terminolojiyi tanımlar. Varlık kiralama, Microsoft Dynamics 365 Finance'ta kiralanmış varlıklar için mali hareketleri yönetme, izleme ve otomatikleştirmeye yönelik gelişmiş bir özelliktir. Varlık kiralama Uluslararası muhasebe standartları (IFRS 16) ve US GAAP standartları (ASC 842) ile uyumludur. Varlık kiralama, kiralama bilgilerini yakalıp işler ve ilk kabul ve aylık günlük girişlerinden kira değerinin düşmesi ve kiranın sonlanmasına kadar kiranın yaşam döngüsü aracılığıyla günlük girişleri oluşturmaya yardımcı olur. Varlık kiralama Sabit kıymetler, Borç hesapları ve Genel muhasebe dahil Dynamics 365 Finance'ın diğer bileşenleriyle ile sorunsuz tümleşir.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için **özellik yönetimi** çalışma alanını kullanabilir. **Özellik yönetimi** çalışma alanında, **Varlık kiralama** olarak adlandırılan özelliği bulup seçin ve **Şimdi etkinleştir** düğmesine tıklayın.

Muhasebe standartları hakkında daha fazla bilgi için IFRS 16 ve US GAAP ASC 842 standart belgelerine başvurun.

## <a name="asset-leasing-elements"></a>Varlık kiralama öğeleri
Aşağıdaki diyagram kiralamalar için iş sürecinin ana öğelerini gösterir.

[![Varlık kiralama öğeleri.](./media/overview-01.png)](./media/overview-01.png)

Kiralanan varlık aşağıdaki ana bileşenleri içerir:

- **Kira sözleşmesi** - Kiraya veren varlığını sahibidir ve kiracıya bir varlığı periyodik kira ödemeleri için belirli bir dönemde karşılık alarak kiralamayı kabul eder. Kiraya veren ve kiracı arasındaki yasal Sözleşmeye ek olarak, kira anlaşması, yenileme seçeneğini ve sahiplik aktarımını kullanma olasılığı gibi yönetim kararlarını yakalar.

- **Kira hesaplaması ve muhasebe standardına göre sınıflandırma** - Kira hesaplaması ve sınıflandırması, kira tipinin ne olacağını belirleyen sınıflandırma sınamasının yanı sıra, ilk ve sonraki ölçümde uygulanacak muhasebe standardını tanımlar. Kira, bir finansal kiralama, işletme kiralama, kısa vadeli kiralama veya düşük değerli kiralama olabilir. Sistem ayrıca, değerlendirme ve sınıflandırma amacıyla gelecekteki minimum kira ödemelerinin net mevcut değerini de hesaplar.

- **Kira hareketleri** - Varlık kiralama, bilançodaki kiralar için kullanım hakkı varlığının ilk kabulünü ve bilanço kiralamaları veya bilanço dışı kiralamalar için sonraki ölçümü destekler. İlk kabul hareketi, gelecekteki minimum kira ödemelerinin net mevcut değerini ölçer. Bu veriler, kuruluşun bilançosunu kullanım hakkı varlığı ve kiralama yükümlülüğü değerini belirlemek için kullanılır. Aylık kiralama hareketlerinin sonraki ölçümü, kira yükümlülüğündeki faiz birikmesiyle ilgilidir ve bu da kira yükümlülüğünün artmasına neden olur. Ayrıca kira yükümlülüğünü azaltan kira ödemeleri tahakkukunu ölçer ve bu daha sonra kiraya verene ödenir. Ölçüm ayrıca kullanım hakkı varlığının amortismanını da içerir.

  Sistem, bilanço dışı kiralamalar için, şu ikisi üzerinden hangisi daha azsa sabit kiralama giderini hesaplar: varlığını ekonomik ömrü veya kiralama süresi. Kira ayarlamaları kiralamayı uzatma veya genişletme gibi sözleşme değişikliklerini ve geri alınamaz maliyetler için kullanım hakkı varlığını kullanan değer düşüşü hareketini hesaplar.

  Varlık kiralama, deftere nakledilen tüm kiralama hareketlerinin hesap planınızı güncelleştirmesini sağlamak için genel muhasebe ile tümleşir. Varlık Kiralama, Borç hesaplarındaki kiraya veren faturalarının izlenmesi için Borç hesaplarıyla tümleştirilir ve buradan gelecek ödemeleri alır. Sabit kıymetlerle tümleştirme, sabit kıymetler kaydındaki kiraları izlemenizi ve Sabit kıymetler içinden kıymetin ilk kabulü, amortismanı ve değer düşüşü dahil olmak üzere, kullanım hakkı varlığı hareketlerini deftere nakletmenizi sağlar.   

## <a name="asset-leasing-components"></a>Varlık kiralama bileşenleri 
Kıymet kiralama kira bilgilerini, ödeme planlarını, başlangıç ve bitiş tarihlerini ve ödeme sıklığını eşler. Ayrıca, net mevcut değer, aylık kira ödemeleri, vade farkı ve kiralama amortismanı için hesaplamaları otomatikleştirir. Sistem konfigürasyona bağlı olarak kira sınıflandırması sınamaları yapar. Sistem ayrıca, takip ettiğiniz muhasebe standardı tarafından tanımlanan çerçeveye dayalı olarak, ilgili kira hareketlerini oluşturur ve deftere nakleder.

Aşağıdaki diyagramda kira defteri, kiralama, hesaplanan ödeme planı, kiralama ve kiralama defterleri için sınıflandırma sınamaları ve buna karşılık gelen hesap hareketleri gösterilmektedir.

[![Kiralama, kiralama defteri ve ödeme planı.](./media/overview-02.png)](./media/overview-02.png)

- **Kira defteri** - Kiralama defteri kira koşulları, adil değer ve kira ödemeleri gibi tüm kira sözleşmesi bilgilerini içerir. Ayrıca, takip ettiğiniz muhasebe standardını, kira türü ve kiralama sınıflandırması testinde dikkate alınan eşikleri içerir. Kira defteri ayrıca genel muhasebeye nakledilen kira hareketlerini de içerir. 
  
- **Kira** - Kira, varlık kiralama temelini temsil eden varlık kiralama bilgilerini içerir, kira bilgileri kaynağı Dynamics 365 Finance dışında yapılan kira sözleşmesi ve yönetim kararlarıdır. Kıymetin adil değeri, ölçüm tarihindeki bir harekette bir kıymet için ödenmesi gereken fiyattır. Bu değer, değerlendirme sırasında dikkate alınacak varlık türüne, pazar koşullarına ve diğer ölçütlere bağlı olabilir. Kıymet adil değeri, sınıflandırma test denkleminde dikkate alınır.

- **Varlık kullanım ömrü** - Bir varlığın kullanım ömrünün kalan dönemini kira başlangıç tarihinden itibaren gösterir. Bir kıymetin faydalı kullanım ömrü, sınıflandırma test denkleminde dikkate alınır. Sabit kıymetlerde tanımlanan faydalı kullanım ömründen farklıdır.

- **Alternatif borçlanma oranı** - Bu, net mevcut değeri hesaplamak için kullanılacak olan faiz oranıdır. Kira verilerinde tanımlandığı takdirde, sistem kirala ödemelerinin net mevcut değerini hesaplamak için bu dolaylı oranı kullanır. Dolaylı oran tanımlanmamışsa, sistem alternatif borçlanma oranını kullanır.

- **Yıllık ödeme türü** - Bu, ödeme döneminin başlangıcında veya dönem sonunda olan kira ödemesidir. Bu, ön ödeme veya yıllık ödeme (kira ödeme döneminin başlangıcında) veya olağan yıllık ödeme (kira ödeme döneminin sonunda) olabilir.

  Ön ödeme için ilk ay dönem numarası sıfır olarak kabul edilir; ilk ay, ödeme gecikmeleri için dönem bir olarak kabul edilir.

- **Bileşim aralığı** - Bu, faizin yıl başına bileşik olduğu dönem sayısını temsil eder. Aylık (yılda 12 dönem), üç ayda bir (yıllık olarak 4 dönem), yarı yıllık (yılda 2 dönem) veya yıllık (yıl başına 1 dönem) olabilir. Dönem sayısı, net mevcut değer hesaplamasında dikkate alınır.

- **Başlangıç tarihi** - Bu, kıymetin kiraya veren tarafından kiracı için kullanılabilir hale getirildiği tarihtir. Tüm kira hesaplamaları ve hareketleri, başlangıç tarihini temel alır. Sonraki hesaplamaların doğruluğunu garantilemek için, başlangıç tarihinin bir dönemin başında (ayın ilk günü) olması gerekir. Sözleşme imzalandığında gerçek tarihi girmek için **Sözleşme imzalama tarihi** alanını kullanabilirsiniz.

- **Kiralama süresi** - Bu, ay cinsinden kira döneminin uzunluğudur.

> [!NOTE] 
> Kiralama süresi tanımı, ödeme planı satırlarındaki dönem veya aralık sayısına bağlıdır. Tanımlanan aralık sayısı aylara dönüştürülecektir.

- **Ödeme planı satırı** - Bu, dönem başına kira ödemelerini yakalar. Ayrıca, yenileme döneminin uygulanıp uygulanmayacağını ve kullanım hakkı varlığı ve kiralama yükümlülüğünün ilk ölçümüne dahil edilip edilmeyeceğini belirtir. Kira vadesi ödemelerinin başlangıç tarihini ve kira süresini temsil eden (günler, aylar veya yıllar olabilir) dönem aralıklarını tanımlayabilirsiniz.

- **Ödeme sıklığı** - Bu, ödemenin aylık, üç aylık, altı aylık veya yıllık olduğunu belirtir. Bitiş tarihi, başlangıç tarihi ve girilen dönem sayısı temel alınarak otomatik olarak hesaplanır.

- **Ödeme planı** - Bu, kira ödemeleri kapsamındaki zamana, ödemelerin miktarına, bileşik dönemlere ve yıllık ödeme türüne göre hesaplanan geçerli net mevcut değerdir.

- **Dönemler** - Bunlar, bileşik dahili ve yıllık ödeme türünü oluşturan kira dönemlerdir. Bileşik aralık, dönemlerin nasıl bölüneceğini belirler. Aşağıdaki bileşik aralıkları ayarlayabilirsiniz:

  - Aylık, yıllık 12 dönem
  - Üç aylık, yıllık 4 dönem
  - Altı aylık, yıllık 2 dönem
  - Yıllık, yılda 1 dönem

Yıllık ödeme türü yıllık ödeme ise, ilk dönem dönem sıfır ile başlar. Aksi takdirde, yıllık ödeme türü ödeme gecikmeleri ise, ilk dönem bir ile başlar.

- **Aylar** - Bu, kira süresindeki takvim ayların sayısını belirtir. Ödeme tutarı, ödeme sıklığında tanımlananan ödenmesi gereken tutardır. Hesaplanan net mevcut değer, dönem başına net mevcut değer tabanlı kira ödemesi, bileşik aralıklar ve alternatif borçlanma oranıdır.

> [!NOTE] 
> Net mevcut değer, indirimli nakit akışı denklemi temel alınarak hesaplanır.

- **Defterler** - Her kiralama ile ilişkilendirilecek önceden yapılandırılmış kurulumdur. Defter, uygulanan muhasebe standardını, kira türlerini ve sınıflandırma sınamaları için temel olarak kullanılan eşiği tanımlar. Sınıflandırma sınamaları, kira türünü otomatik olarak belirtmek için kullanılır.

- **Muhasebe çerçevesi** - Desteklediğiniz muhasebe standardını (IFRS 16 veya ASC 842) gösterir. Muhasebe standardı, kira ile ilişkili kitapta atanır. Muhasebe standardı, deftere nakil profilinde belirtilen genel muhasebe hesaplarını belirleyecektir.

- **Kiralama türleri** İki kiralama türünden hangisinin kullanılacağını belirtir: finansal kiralama veya işletme kiralaması. Finansal kiralamada, kiralanan varlıkla ilgili riskler ve ödüller kiracıya aktarılır. İşletme kiralamasında, kiralanan varlıkla ilgili riskler ve geri ödüller kiraya veren de kalır. Üçüncü seçenek ise, defterde tanımlanan eşikler temel alarak, kiralama türünün finansal veya işletme olarak otomatik tanımlamasıdır. Bu otomatik tanımlama, kira yeniden sınıflandırma testi sırasında gerçekleştirilir.

- **Eşikler** - Varlığın aşağıdakilerden biri olarak sınıflandırılıp sınıflandırılmayacağının belirlenmesi için kira sınıflandırması testlerinde kullanılır:

  - **Kiralama süresi** - Sınıflandırma testinde kullanılacak yararlı kullanım ömrü yüzdesidir. Kira türü otomatik olarak ayarlanmışsa ve varlığın faydalı ömrü üzerinden kiralama süresi burada tanımlanan yüzdeye eşit veya bundan fazlaysa, sistem kiralamayı finansal olarak sınıflandıracaktır.

  - **Net mevcut değer** - Sınıflandırma testinde kullanılacak varlık adil değeri yüzdesidir. Kira türü otomatik olarak ayarlanmışsa ve varlığın adil değeri üzerinden gelecek kira ödemelerinin net mevcut değeri burada tanımlanan yüzdeye eşit veya bundan fazlaysa, sistem kiralamayı finansal olarak sınıflandıracaktır.

  - **Kısa süreli kiralama** - Kiralama süresi tanımlanan değerden az veya bu değere eşitse, kiralama kısa süreli kiralama olarak sınıflandırılacaktır.

  - **Düşük değer** - Varlığın adil değeri tanımlanan değerden az veya bu değere eşitse, kiralama düşük değerli kiralama olarak sınıflandırılacaktır.

  - **Kiralama sınıflandırması ve hareketleri** Kira sınıflandırması, kiralamanın finansal kiralama mı, işletme kiralaması mı, kısa süreli kiralama mı yoksa düşük değerli kiralama mı olduğunu tanımlamak için diğer sınıflandırma testi ölçütlerinin yanı sıra defterlerdeki tanımlanmış eşiklere göre kiralamaları sınıflandıran otomatik bir süreçtir. Bu, aynı zamanda ertelenen kira işleminin izlenip izlenmediğini tanımlamak için kullanılır.

Sınıflandırma sınamaları Sahiplik aktarını, Satınalma seçeneği, Kiralama süresi, Net mevcut değer ve Benzersiz varlığı içerir. Aşağıdaki diyagram kira sınıflandırması sınamalarını gösterir.

[![Kira sınıflandırması sınamaları.](./media/overview-03.png)](./media/overview-03.png)

Her kira türü, farklı kira hareketleri için muhasebeyi farklı şekilde işler. Hareketler arasında ilk kabul, faiz gideri, kiralama vadesi ödemesi ve kira amortismanı bulunur ve bunlar takip ettiğiniz muhasebe standartlarına dayalıdır (IFRS 16 veya ASC 842). Genel muhasebe hesapları, her hareket türü ve muhasebe çerçevesi için kiralama deftere nakil profili altında tanımlanır.

## <a name="asset-leasing-transactions"></a>Varlık kiralama hareketleri

#### <a name="initial-recognition"></a>Başlangıçtaki kabul 
Kiralanan varlığın ilk kabulü, hesaplanan net mevcut değeri kullanır ve böylece bilançoda rapor edilebilir. Bunun için olan muhasebe girişi otomatik olarak oluşturulur. Bu hareket, kullanım hakkı varlığı hesabını borçlandırır ve işletme kiralaması yükümlülüğü hesabını alacaklandırır. Sabit kıymet kiralama ile ilişkilendirilmişse, ilk kabul girişi sabit kıymet alımı olarak yansıtılır. Bu senaryoda, kullanım hakkı varlığı hesabına nakil için sabit kıymet deftere nakil profili tanımlamanız gerekir. 

> [!NOTE]
> İşletme kiralamaları yalnızca US GAAP ASC 842 tarafından desteklenir.

|     Türü                                          |     Borç                     |     Kredi                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     US GAAP altında işletme kiralaması            |     Kullanım hakkı varlığı        |     İşletme kiralama yükümlülüğü     |
|     IFRS ve US GAAP altında finansal kiralama      |     Kullanım hakkı varlığı        |     Finansal kiralama yükümlülüğü       |

#### <a name="lease-liability-amortization-interest-expense"></a>Kiralama yükümlülüğü amortismanı (faiz gideri) 
Kiralama için faiz, kiralamanın başlangıç bakiyesi, dönem kira ödemesi, alternatif borçlanma oranı ve yıl başına birleşik aralık dönemleri için faiz hesaplanarak kabul edilir. Faiz tutarı, işletme kiralama yükümlülüğü hesabını alacaklandırarak artırır ve bu, kuruluşun bilançosunda yansıtılır. Hareket ayrıca faiz gideri hesabına borç girişi içerir; bu, finansal kiralamalar için kar ve zarar raporuna, işletme kiralamaları için kira gideri hesabına yansıtılır.

|     Türü                                          |     Borç                     |     Kredi                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     US GAAP ASC 842 altındaki işletme kiralaması yükümlülüğü girişi    |     Kiralama gideri         |     İşletme kiralama yükümlülüğü         |
|     IFRS ve US GAAP altında finansal kiralama yükümlülüğü girişi      |     Vade farkı gideri          |     Finansal kiralama yükümlülüğü           |

#### <a name="accrued-lease-payment"></a>Tahakkuk eden kira ödemesi
Tahakkuk eden bir kira ödemesi, banka veya nakit hesaplarından ödeme hareketi olarak işlem yapılması nedeniyle gelecek bir kira ödemesi olarak tanınır. Ödenecek kira ödemesi, kira yükümlülüğü hesabını kiraya verenin satıcı olarak tanımlanması durumunda satıcı alt muhasebesine karşı borçlandırarak veya alacak tarafını borç notları genel muhasebe hesabına naklederek kiralama yükümlülüğünü düşürür ardından ödeme satıcıya veya borç notlarına karşı yürütülür.

|     Türü                                          |     Borç                     |     Kredi                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     US GAAP altında işletme kiralaması              |  İşletme kiralama yükümlülüğü    |   Satıcı yükümlülüğ (genel muhasebe)/Senet borçları  |
|     IFRS ve US GAAP altında finansal kiralama        |  Finansal kiralama yükümlülüğü      |   Satıcı yükümlülüğ (genel muhasebe)/Senet borçları  |

#### <a name="asset-depreciation"></a>Varlık amortismanı
Kullanım hakkı varlığı amortismanı, varlık faydalı kullanım ömrü veya kiralama süresi (hangisi azsa) üzerinden yapılır. US GAAP işletme kiralaması (ASC 842) için amortismanı hesaplama yöntemi, sabit kiralama gideri ile faiz tutarı arasındaki farka dayanır. Finansal kiralamalarla ilgili amortisman standart sabit yöntem kullanılarak hesaplanır. Kira amortismanı, faiz giderinin borçlandırılması yoluyla kar ve zarar raporunu etkiler. Bilanço, finansal kiralamalar için birikmiş kullanım hakkı varlığı hesabını borçlandırarak etkilenir. Kira bir sabit kıymete bağlıysa, amortisman hareketleri yalnızca sabit kıymetler modülünden yürütülür. 

|     Türü                                          |     Borç                     |     Kredi                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     US GAAP altında işletme kiralaması              |  Kiralama gideri                |   Kullanım hakkı varlığı birikmiş amortismanı     |
|     IFRS ve US GAAP altında finansal kiralama        |   Kullanım hakkı varlığı gideri amortismanı   |   Kullanım hakkı varlığı birikmiş amortismanı    |

#### <a name="short-term-lease"></a>Kısa süreli kiralama
Kısa süreli kiralama, bir kuruluşun gelir tablosunu etkileyecek şekilde gider olarak kabul edilir. Oluşturulan vadesi gelmiş kira ödemesi, kira gideri hesabını borçlandırır ve borç seneti veya satıcı yardımcı muhasebe hesabını alacaklandırır.

|     Türü                                          |     Borç                     |     Kredi                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     IFRS ve US GAAP altında kısa süreli kiralama girişi     |  Kiralama gideri                |   Satıcı yükümlülüğ (genel muhasebe)/Senet borçları  |

#### <a name="low-value-lease"></a>Düşük değerli kiralama
Düşük değerli kiralama, kuruluşun gelir tablosunu etkileyecek olan bir gider olarak kabul edilir. Oluşturulan vadesi gelmiş kira ödemesi, kira gideri hesabını borçlandırır ve borç seneti veya satıcı yardımcı muhasebe hesabını alacaklandırır.

|     Türü                                          |     Borç                     |     Kredi                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     IFRS ve US GAAP altında düşük değerli kiralama girişi      |  Kiralama gideri                |   Satıcı yükümlülüğ (genel muhasebe)/Senet borçları  |


#### <a name="index-revaluation"></a>Endeks yeniden değerlemesi
Bu, bir endeks oranıyla ölçülen değişken kira ödemeleri için varlık kiralama hesabıdır. Endeks oranı dalgalanmaları nedeniyle kira ödemelerinde yapılan değişiklikler, IFRS 16 altında bir kira ayarlaması oluşturur. Kiralama yükümlülüğü ve kullanım hakkı varlıkları yeni ödemelerin hesabına göre ayarlanacaktır. 

|     Türü                                          |     Borç                             |     Kredi                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Artış durumunda, IFRS altında dizin yeniden değerleme girişi  |  Kullanım hakkı varlığı       |   İşletme kiralama yükümlülüğü |
|   Azalma durumunda, IFRS altında dizin yeniden değerleme girişi  |  İşletme kiralama yükümlülüğü  |   Kullanım hakkı varlığı      |

Endeks oranında değişiklik olması nedeniyle ödemelerde değişiklik olduğunda, nakit akışlarında US GAAP ASC 842 altındaki faiz oranlarıyla ilgili kiralama sürelerindeki bir değişiklik gibi ek değişiklikler olmadıkça, yalnızca değişken ödemeler değişir.

#### <a name="lease-adjustment"></a>Kiralama düzeltmesi
Kira koşulları değiştirilirse, kiralama uzatılırsa veyakira ayarlaması gereken ek koşullar varsa, varlık kiralama kiraların ayarlanmasına olanak tanır. Kira ayarlamaları, kullanım hakkı varlığı ve kiralama yükümlülüğünün artırılması veya azaltılması için deftere nakledilir. Ayarlama süreci, yükümlülük amortismanı devredilen bitiş bakiyesini ve ayarlama tarihindeki varlık bakiyesini alır. Sabit kıymete bir kira bağlandığında, kullanım hakkı ayarlaması Sabit kıymetlerde atanan kimliği kullanarak deftere nakledilir. 

|     Türü                                          |     Borç                             |     Kredi                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Artış durumunda IFRS ve US GAAP için kira ayarlama girişi     |  Kullanım hakkı varlığı       |   İşletme kiralama yükümlülüğü |
|   Azalma durumunda IFRS ve US GAAP için kira ayarlama girişi     |  İşletme kiralama yükümlülüğü  |   Kullanım hakkı varlığı      |


#### <a name="lease-impairment"></a>Kira değer düşüşü
Bu, kullanım hakkı varlığının devredilen bakiye düşüşünü temsil eder. Değer düşüşü tutarını, hareket tarihini ve kalan dönemi tanımlayın. Kalan kullanım hakkı varlığı amortisamanı sabit esasa göre gerçekleştirilir. Kira değer düşüşü mantığı, varlık amortisman planında mevcut olan varlık devredilen değerini dikkate alır.  

|     Türü                                          |     Borç                             |     Kredi                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   IFRS ve US GAAP için değer düşüşü girişi           |  Değer düşüşü gideri                   |    Kullanım hakkı varlığı     |

>[!NOTE]
> Kira bir sabit kıymete bağlıysa, kira değer düşüşü Sabit kıymetlerden deftere nakledilmelidir çünkü varlık amortismanı Sabit kıymetler modülünden çalıştırılır.

**Çift para birimi** Kiralama hareketleri muhasebe ve raporlama para birimi dışında bir para biriminde deftere nakledilebilir. Para birimi döviz kuru, başlangıç tarihinde Genel muhasebede tanımlanır. Kiralamayı oluştururken **sabit oran** alanını **Evet** olarak ayarlayarak döviz kurlarını değiştirebilirsiniz . Kira hareketlerini girdiğinizde, ilk kabul ve sonraki amortisman hareketleri, başlangıç tarihi itibariyle döviz kurunu kullanır. Sonraki ödeme ve faiz hareketleri geçerli etkin döviz kurunu kullanır. 

## <a name="create-an-asset-lease"></a>Varlık kiralama oluşturma
Yeni bir kiralama oluşturmak için aşağıdaki adımları tamamlayın. 

1. **Varlık kiralama**'yı kullanmak için **Özellik yönetimi** çalışma alanında etkinleştirmeniz gerekir. **Özellik yönetimi** çalışma alanından **Tümü**'nü seçtiğinizde, tüm özellikler sayfada listelenir. **Varlık kiralama**'yı seçin ve ardından **Şimdi etkinleştir**'i seçin.
2. **Varlık kiralama > Ortak > Kiralama özeti**'ne gidin. **Genel** hızlı sekmesinde gerekli alanları girin. 
   - **Kiralama ayrıntıları**
   - **Kıymet faydalı ömrü (Ay)**
   - **Kiralama grubu**
   - **Alternatif borçlanma oranı (%)**
   - **Bileşim aralığı**
   - **Yıllık ödeme türü**
   - **Para Birimi**
   - **Başlangıç tarihi**

3. **Ödeme planı satırları** hızlı sekmesine gidin ve bir ödeme satırı girip **Planlama oluştur**'u seçin.

4. **Defterler**'i seçin. 

5. **Genel** Hızlı sekmesine geçin. **Başlangıçtaki kullanım hakkı varlığı** ve **kiralama yükümlülüğ** hesaplanır. 

6. **Kiralama sınıflandırması tesi** hızlı sekmesine giderek **Kiralama türü** alanındaki değeri kontrol edin. 

   Otomatik **Kiralama türü** **Defterler** sayfasında tanımlanan ölçütlere göre sınıflandırılır.

7.  **İşlev** bölümünün altında **Ödeme planı**'na gidin.  

   **Ödeme planı** sayfası bir kiralama kodu için gelecekteki ödeme planlamalarını listeler. **İlk kabul** hareketlerini deftere nakledebilmek için **Planlamayı onayla**'yı seçin. 

[![İlk kabul işlevi.](./media/overview-13.png)](./media/overview-13.png)

8. İlk kabul günlüğünü oluşturmak için **İlk kabul**'ü seçin. 

9. İlk kabul hareketini deftere nakletmek için **Varlık kiralama günlükleri**'ni seçin. 

   Ödeme planında, kullanım hakkı varlığı hareketlerini listeleyen ayrıntılı sayfayı açabilirsiniz. 
 
   **Kira yükümlülüğü amortisman planlaması**, her dönem için hesaplanan faiz tutarını gösterir.
   
10. Günlüğü oluşturun ve ardından **Varlık kiralama günlükleri**'ne gidin. **Kira yükümlülüğü amortisman planlaması** faiz hareketlerinde de gösterilir.

   **Varlık amortisman planlaması** sayfası, seçilen kira koduyla ilgili amortisman hareketlerini gösterir. 

   [![ROU varlığı hareketleri sayfası.](./media/overview-20.png)](./media/overview-20.png)

   **ROU varlığı hareketleri** sayfası ilk kabulü, birikmiş amortismanı ve varlık bakiyesini listeler. 

   **Kira yükümlülüğü hareketleri** sayfası ilk kabulü, kira faizi ödemesini, kira ödemesini ve kira yükümlülüğü bakiyesini gösterir. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

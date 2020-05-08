---
title: Kılavuz yetenekleri
description: Bu konu, kılavuz denetiminin çeşitli güçlü özelliklerini açıklamaktadır. Bu yeteneklere erişim sahibi olmak için yeni kılavuz özelliğinin etkinleştirilmesi gerekir.
author: jasongre
manager: AnnBe
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: fd45f71fc15e467c461433682310ab7b7cc0158a
ms.sourcegitcommit: 0d7b700950b1f95dc030ceab5bbdfd4fe1f79ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284416"
---
# <a name="grid-capabilities"></a>Kılavuz yetenekleri

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Yeni kılavuz denetimi, kullanıcı üretkenliğini artırmak, verilerinizin daha ilginç görünümlerini elde etmek ve verilerinize anlamlı bilgiler yüklemek için kullanılabilecek bir dizi yararlı ve güçlü yetenek sağlar. Bu makalede aşağıdaki yetenekler ele alınıyor: 

-  Toplamlar hesaplanıyor
-  Verileri gruplandırma
-  Sistemi önceden hazırlama
-  Matematik ifadelerini değerlendirme 

## <a name="calculating-totals"></a>Toplamlar hesaplanıyor
Finance and Operations uygulamalarında kullanıcılar toplamları ızgaralardaki sayısal sütunların alt kısmında görebilme yeteneğine sahiptir. Bu toplamlar, kılavuzun alt kısmındaki bir alt bilgi bölümünde gösterilir. 

### <a name="showing-the-grid-footer"></a>Kılavuz alt bilgisini gösterme
Finance and Operations uygulamalarda her sekmeli kılavuzun altında altbilgi alanı vardır. Altbilgi, kılavuzda görülen verilerle ilgili değerli bilgileri gösterebilir. Aşağıda bu bilgilerin örnekleri verilmiştir:

- Tablodaki seçili satır sayısı (birden fazla kayıt seçiliyken)
- Yapılandırılan sayısal sütunların en altındaki genel toplamlar
- Veri kümesindeki satır sayısı 

Bu alt bilgi varsayılan olarak gizlidir ancak kolayca etkinleştirilebilir. Bir kılavuzun alt bilgisini göstermek için, kılavuzda bir sütun başlığına sağ tıklayın ve **Alt bilgiyi göster** seçeneğini belirleyin. Alt bilgi belirli bir kılavuz için etkinleştirildikten sonra, kullanıcı bir sütun başlığına sağ tıklayıp **Alt bilgiyi gizle**'yi seçerek alt bilgiyi gizlemeyi seçene kadar bu ayar hatırlanır.  **Alt bilgiyi göster/Alt bilgiyi gizle** eylem yerinin ilerideki bir güncelleştirmede değiştirilmesi bekleniyor. 

### <a name="specifying-columns-with-totals"></a>Sütunları toplamlarla belirtme
Şu anda, sütunlar varsayılan olarak toplamları gösterecek şekilde yapılandırılmayacak. Bunun yerine, bu, ızgaralardaki sütunların genişliklerini ayarlamaya benzer şekilde bir kerelik kurulum faaliyeti olarak görülüyor. Bir sütunun toplamlarını görmek istediğinizi belirttiğinizde, sayfayı bir sonraki ziyaretinizde bu ayar hatırlanır.  

Bir sütunu toplam gösterecek şekilde yapılandırmanın iki yolu vardır: 

- Bir toplam görmek istediğiniz sütuna sağ tıklayın ve **Bu sütunun toplamını al**'ı seçin. Bu eylem üç olayın oluşmasına neden olur:

    1. Altbilgi görünür hale gelir. 
    2. Bu sütunda bir toplam görme tercihiniz kaydedilir. 
    3. Bu sütun ve toplamlarını görmek istediğiniz diğer sütunlar için bir toplam hesaplaması başlatır. Bir toplamı göstermek için gerekli olan zaman, topladığınızdan önce veri kümesinin boyutuna bağlıdır.

- Altbilgi görünür olduktan sonra, toplam görmek istediğiniz sütunun alt bilgi alanında **toplamı göster** 'i seçin. Yapılandırılmış sütun yoksa, **Toplamı göster** düğmesi tüm sayısal sütunlarda görünür. 

    Toplamlar için en az bir sütun yapılandırıldıktan sonra, **Toplamı göster** düğmeleri yalnızca üzerine gelindiği veya odaklanıldığı zaman ortaya çıkacaktır. **Toplamı göster** eylemi, yalnızca bu sütunda bir toplamı görmek için tercihlerinizi kaydeder; böylece, daha sonra sayfaya yapılan ziyaretlerin tercihi uygulanır. Altbilgide, bu durum sütunda görünen bir çizgiyle belirtilir. (Alternatif olarak, veri kümesi yeterince küçükse, toplam olarak derhal gösterilir.)

Bir hata yapar ve artık belirli bir sütundaki toplamı artık görmek istemezseniz, sütuna sağ tıklayın ve **Toplamı gizle**'yi seçin veya bu sütundaki alt bilgide bulunan **Toplamı gizle** düğmesini seçin. Bu tercih, sayfaya ileride yapılacak ziyaretler için de kaydedilecektir. 

### <a name="calculating-totals"></a>Toplamlar hesaplanıyor
Alt bilginin görünür olduğu ve sütunların toplamlar için daha önce yapılandırıldığı bir sayfaya geldiğiniz zaman, toplamlar alt bilgide gösterilebilir veya gösterilmeyebilir. Bu durum sayfadaki veri kümesinin boyutuna bağlıdır. Veri kümesi yeterince küçükse, veri kümesindeki satır sayısıyla birlikte toplamlar otomatik olarak gösterilecektir. Toplamlar için yapılandırdığınız sütunların altındaki alt bilgide tireler varsa, veri kümesi sistemin toplamları hemen gösteremeyeceği kadar büyüktür ve toplamları hesaplamak için belirli bir eylem gerekir. Bunu yapmak için, alt bilgideki **Hesapla** düğmesine tıklayın veya toplamını almak istediğiniz bir sütuna sağ tıklayın ve **Bu sütunun toplamını al**'ı seçin.  

Hesaplama çok uzun sürerse, **İptal** düğmesini seçerek işlemi iptal edebilirsiniz. Ancak bazen veri kümesi toplamları hesaplamak için çok büyük olur (kuruluşunuz tarafından uygulanan bir sınıra göre) ve bunun yerine size verilerinizi daha fazla filtrelemeniz gerektiği bildirilir.

Siz veri kümesinde güncelleştirme, silme veya satır oluşturma işlemleri yaptıkça toplamlar otomatik olarak güncelleştirilir.  

## <a name="grouping-data"></a>Verileri gruplandırma
İş kullanıcılarının sıklıkla anlık olarak veri analizi yapmaları gerekir. Bu işlem Microsoft Excel'e veri aktararak ve özet tablolar kullanarak yapılırken, sekmeli kılavuzlardaki **Gruplandırma** yeteneği sayesinde kullanıcılar verilerini Finance and Operations uygulamalarında ilginç yollarla organize edebilirler. Bu özellik **Toplamlar** özelliğini genişlettiği için, **Gruplandırma** da grup düzeyinde alt toplamlar sunarak verilere anlamlı bilgiler yüklemenize olanak sağlar.

Bu özelliği kullanmak için, gruplandırmada kullanmak istediğiniz sütuna sağ tıklayın ve **Bu sütuna göre gruplandır**'ı seçin. Bu eylem, verileri, seçilen sütuna göre sıralar, kılavuzun başına yeni bir Tabloya göre gruplandır özelliği ve her grubun başına "üst bilgi satırları" ekler. Bu üst bilgi satırları her grup hakkında aşağıdaki bilgileri sağlar: 
-  Grubun veri değeri 
-  Sütun etiketi (Bu bilgiler özellikle birden çok gruplandırma düzeyi desteklendikten sonra yararlı olacaktır.)
-  Bu gruptaki veri satırlarının sayısı
-  Toplamları gösterecek şekilde yapılandırılan sütunların alt toplamları

[Kayıtlı görünümler](saved-views.md) etkinleştirildiğinde, sayfayı bir sonraki ziyaretinizde hızlı erişim için bir görünümün parçası olarak bu gruplandırma kişiselleştirerek gruplandırılabilir.  

Başka bir sütunda **Bu sütuna göre gruplandır**'ı seçerseniz, 10.0.9/Platform güncelleştirmesi 33'te yalnızca gruplandırma düzeyi desteklendiği için, özgün gruplandırma değiştirilecektir.

Bir kılavuzda gruplandırmayı geri almak için, gruplandırma sütununa sağ tıklayın ve **Grubu çöz**'ü seçin.  

## <a name="typing-ahead-of-the-system"></a>Sistemi önceden hazırlama
Birçok iş senaryosunda, sisteme verileri hızlı şekilde girebilme çok önemlidir. Yeni kılavuz denetimi tanıtılmadan önce, kullanıcılar yalnızca geçerli satırdaki verileri değiştirebiliyordu. Yeni bir satır oluşturmadan veya farklı bir satıra geçiş yapmadan önce, sistemin herhangi bir değişikliği başarıyla doğrulamasını beklemek zorundaydılar. Kullanıcıların bu doğrulamaların tamamlanmasını beklediği süreyi azaltmak ve kullanıcı üretkenliğini artırmak için, yeni kılavuz bu doğrulamaları zaman uyumsuz olacak şekilde ayarlıyor. Bu nedenle, kullanıcı önceki satır doğrulamaları beklenirken değişiklik yapmak için diğer satırlara geçebiliyor. 

Bu yeni davranışı desteklemek için, kılavuz düzenleme modundayken, satır durumu için yeni bir sütun kılavuzun en üstüne eklenir. Bu sütun aşağıdaki durumlardan birini gösterir:

- **Boş** – Herhangi bir durum görüntüsü satırın sistem tarafından başarıyla kaydedildiğini göstermez.
- **İşlem beklemede** – Bu durum, satırdaki değişikliklerin sunucu tarafından henüz kaydedilmediğini, ancak işlenmesi gereken değişiklikler sırasında olduğunu gösterir. Kılavuzun dışında bir eylem gerçekleştirmeden önce, bekleyen tüm değişikliklerin işlenmesi için beklemeniz gerekir. Ek olarak, bu satırlardaki metinler, satırların kaydedilmemiş durumunu gösterecek şekilde italik yapılır. 
- **Doğrulama uyarısı** – Bu durum, bazı doğrulama sorunları nedeniyle sistemin satırdaki değişiklikleri kaydedemediğini gösterir. Eski kılavuzda, sorunu hemen düzeltmek için satıra geri dönmeniz gerekiyordu. Ancak, yeni kılavuzda bir doğrulama sorunuyla karşılaşıldığı size bildirilir, ancak satırdaki sorunları ne zaman düzeltmek istediğinize karar verebilirsiniz. Sorunu düzeltmeye hazır olduğunuzda, odağı yeniden el ile satıra taşıyabilirsiniz. Alternatif olarak, **Bu sorunu düzelt** eylemini seçebilirsiniz. Bu eylem, odağı hemen sorunun bulunduğu satıra geri taşır ve kılavuzun içinde veya dışında düzenlemeler yapmanıza olanak sağlar. Bu doğrulama uyarısı giderilene kadar sonraki bekleyen satırların işlenmesinin durdurulduğunu unutmayın. 
- **Duraklatıldı** – Bu durum, bir satırın doğrulanması kullanıcı girişi gerektiren bir açılan iletişim kutusunu tetiklediği için işlemin sunucu tarafından duraklatıldığını belirtir. Kullanıcı başka bir satıra veri giriyor olabileceğinden açılır iletişim kutusu o kullanıcıya hemen sunulmayacaktır. Bunun yerine, kullanıcı işlemeyi sürdürmeyi seçtiğinde gösterilecektir. Bu durum, kullanıcıyı durumla ilgili bilgilendiren bir bildirimle birlikte gösterilir. Bildirim, açılır iletişim kutusunu tetikleyecek bir **İşlemeyi sürdür** eylemi içerir.  
    
Kullanıcılar, sunucunun işlediği yerin önüne veri girerken arama eksikliği, denetim düzeyinde doğrulama ve varsayılan değerlerin girişi gibi veri giriş deneyimlerinde bazı aksaklıklarla karşılaşabilirler. Bir değerin bulunması için açılan listeye gereksinim duyan kullanıcıların, sunucunun geçerli satırı yakalamasını beklemeleri önerilir. Sunucu o satırı işlediğinde, denetim düzeyinde doğrulama ve varsayılan değerlerin girişi de gerçekleşir.   

### <a name="pasting-from-excel"></a>Excel'den yapıştırma
Kullanıcılar her zaman Finance and Operations uygulamalarındaki kılavuzlardan Excel'e **Excel'e aktar** mekanizmasını kullanarak veri aktarabiliyordu. Ancak, sistemden önce veri girebilme özelliği, yeni kılavuzun Excel'den tablo kopyalanmasına ve onları Finance and Operations uygulamalarında doğrudan ızgaralara yapıştırmasına olanak tanır. Yapıştırma işleminin başlatıldığı kılavuz hücresi kopyalanan tablonun nereye yapıştırılacağını belirler. Şu iki durum dışında, kılavuzun içeriği üzerine kopyalanan tablonun içeriği yazılır:

- Kopyalanan tablodaki sütun sayısı, yapıştırma konumundan başlayarak kılavuzda kalan sütun sayısını aşarsa, kullanıcıya ek sütunların yok sayıldığı bildirilir. 
- Kopyalanan tablodaki satır sayısı, yapıştırma konumundan başlayarak kılavuzdaki satır sayısını aşarsa, yapıştırılan içerik için varolan hücrelerin üzerine yazılır ve kopyalanan tablodaki tüm ek satırlar kılavuzun en altına yeni satırlar olarak eklenir. 

## <a name="evaluating-math-expressions"></a>Matematik ifadelerini değerlendirme
Verimlilik rampa olarak, kullanıcılar bir kılavuzdaki sayısal hücrelere matematiksel formüller girebilecek. Bu kullanıcılar, sistem dışındaki bir uygulamada hesaplama yapmaları gerekmez. Örneğin **= 15\*4** girerseniz ve alanın dışına gitmek için **sekme** tuşuna basarsanız, sistem ifadeyi değerlendirir ve alan için **60** değerini kaydeder.

Sistemin bir değeri ifade olarak tanımasını sağlamak için, değeri bir eşittir işaretiyle (**=**) başlatın. Desteklenen işleçler ve söz dizimi hakkında daha fazla bilgi edinmek için bkz. [Desteklenen matematik simgeleri](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="frequently-asked-questions"></a>Sık sorulan sorular
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Yeni kılavuz denetimini ortamımda nasıl etkinleştirebilirim? 

**10.0.9 / Platform güncelleştirmesi 33 ve sonrası** **Yeni kılavuz denetimi** özelliği, herhangi bir ortamda doğrudan Özellik yönetiminde kullanılabilir. Diğer genel Önizleme özellikleri gibi, üretim için bu özelliğin etkinleştirilmesi, [Tamamlayıcı Kullanım Koşulları Sözleşmesine](https://go.microsoft.com/fwlink/?linkid=2105274) tabidir.  

**10.0.8/Platform güncelleştirmesi 32 ve 10.0.7 / Platform güncelleştirmesi 31** **Yeni kılavuz denetimi** özelliği, aşağıdaki adımları izleyerek ek test ve tasarım değişiklikleri sağlamak amacıyla Katman 1 (geliştirme/test) ve Katman 2 (korumalı alan) ortamlarında etkinleştirilebilir.

1.  **Uçuşu etkinleştirin**: Aşağıdaki SQL beyanını yürütün: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. Statik deneme sürümü önbelleğini temizlemesi için **IIS'yi Sıfırla**'yın. 

3.  **Özelliği bulun**: **Özellik Yönetimi** çalışma alanına gidin. **Yeni kılavuz denetimi** tüm özellikler listesinde görünmezse, **Güncelleştirmeleri denetle**'yi seçin.   

4.  **Özelliği etkinleştirin**: Özellikler listesinde **Yeni kılavuz denetimi** özelliğini bulun ve Ayrıntılar bölmesindeki **Şimdi etkinleştir**'i seçin. Tarayıcı yenilemenin gerekli olduğunu unutmayın. 

Sonraki tüm kullanıcı oturumları yeni ızgara denetimi etkin olarak başlayacaktır.

## <a name="known-issues"></a>Bilinen sorunlar
Bu bölüm, özellik bir önizleme durumundayken yeni kılavuz denetimiyle ilgili bilinen sorunların listesini içerir.  

### <a name="open-issues"></a>Açık sorunlar

- Birden çok sütun olarak işlenen kart listeleri şimdi tek bir sütun olarak işleniyor.
- Gruplanmış listeler grup olarak veya ayrı sütunlarda işlenmiyor.
- Araç ipuçları resimler için gösterilmiyor.
- Kılavuz çizgileri görünümü tüm alan türleri için çalışmıyor.
- Aralıklı olarak, bazı satırları çoklu olarak seçtikten sonra kılavuzun dışına tıklayamıyorsunuz.
- **Doğrula** ve **Kopyala** Görev Kaydedicisi seçenekleri tarih/sayı denetimleri için kullanılamıyor.

### <a name="fixed-as-part-of-10012"></a>10.0.12'nin parçası olarak düzeltildi

> [!Note]
> Aşağıdaki bilgiler sağlanmıştır, buna göre plan yapabilirsiniz. sürüm 10.0.12 için hedeflenen sürüm zamanlaması hakkında daha fazla bilgi için bkz. [Hizmet güncelleştirmesi kullanılabilirliği](../../fin-ops/get-started/public-preview-releases.md).

- [Sorun 429126] Son kayıt silindikten sonra kılavuzun dışındaki denetimler güncelleştirilemiyor.
- [Sorun 430575] Tablo denetimleri, görüntülenen öğelerin içeriğini güncelleştirmiyor.
- [KB 4558570] Kayıt silindikten sonra öğeler hala sayfada gösteriliyor.
- [KB 4558584] Eksi sayılar doğru işlenmiyor.
- [KB 4558575] Alanlar satır değişikliğinden sonra güncelleştirilimiyor / Kılavuz işleme satır silme işleminden takılıyor.
- [Sorun 436980] Liste Paneli **ExtendedStyle** ile ilişkilendirilmiş uygulanmıyor.
- [KB 4558573] Gerekli değişiklik kılavuzun dışında olduğunda doğrulama hataları düzeltilemiyor.
    
### <a name="quality-update-for-10011"></a>10.0.11 için kalite güncelleştirmesi

- [KB 4558381] Eksi sayılar doğru işlenmiyor / Kullanıcılar bazen doğrulama sorunlarıyla karşılaştıktan sonra takılıyor.

### <a name="fixed-as-part-of-10011"></a>10.0.11'nin parçası olarak düzeltildi

- [KB 4558374] Çok biçimli seçici iletişim kutusu gerektiren kayıtlar oluşturulamıyor.
- [KB 4558382] Beklenmeyen istemci hataları oluşuyor.
- [KB 4558375] Yardım metni yeni kılavuzdaki sütunlarda gösterilmiyor.
- [KB 4558376] Liste Paneli ızgaraları, Internet Explorer'da doğru yükseklikte işlenmiyor.
- [KB 4558377] **SizeToAvailable** genişliği olan birleşik açılan kutu sütunları bazı sayfalarda işlenmiyor.
- [KB 4549711] Yeni kılavuz denetimi etkinleştirildikten sonra ödeme teklifindeki satırlar doğru şekilde kaldırılamıyor.
- [KB 4558378] Detaya gitme bazen yanlış kaydı açıyor.
- [KB 4558379] **ReplaceOnLookup**=**Hayır** olduğunda aramalar açıldığında hata oluşuyor.
- [KB 4558380] Kılavuzdaki kullanılabilir alan, sayfanın bir bölümü daraltıldıktan hemen sonra doldurulmuyor.
- [Sorun 432458] Boş veya yinelenen satırlar bazı alt koleksiyonların başlangıcında gösteriliyor.
- [KB 4558587] Değiştirme alanları için birleşik kutular içeren referans grupları değerleri göstermiyor.

### <a name="fixed-as-part-of-10010"></a>10.0.10'un parçası olarak düzeltildi

- [Sorun 414301] Yeni satırlar oluşturulduğunda, önceki satırlardaki veriler kayboluyor.
- [KB 4550367] Zaman değerleri doğru şekilde biçimlendirilmiyor.
- [KB 4549734] İşaretleme sütunu gizli ise, etkin satırlar işaretlenmiş olarak kabul edilmiyor.
- [Hata 417044] Liste stili kılavuzlar için boş kılavuz iletisi yok.
- [KB 4558367] Satırlar değiştiğinde metin seçimi tutarsız.
- [KB 4558372] Yapıştırıldığı içerikteki sütun sayısı kılavuzdaki kalan sütunların sayısını aşarsa, yeni kılavuz işleme modunda takılıyor.
- [KB 4558368] Tek seçimli senaryolarda klavyeyle çoklu seçim yapılmasına izin veriliyor.
- [KB 4539058] Bazı kılavuzlar (genellikle hızlı sekmelerde) bazen işlenmiyor (ancak, uzaklaştırdığınızda işleniyorlar).
- [KB 4558369] Durum görüntüleri hiyerarşik kılavuzda kayboluyor.
- [KB 4558370] Yeni bir satır görünüme kaydırılmıyor.
- [KB 4549796] Bir kılavuzda görünüm modundayken değerler düzenlenemiyor.

### <a name="quality-update-for-1009platform-update-33"></a>10.0.9/Platform güncelleştirmesi 33 için kalite güncelleştirmesi

- [KB 4550367] Zaman değerleri doğru şekilde biçimlendirilmiyor.

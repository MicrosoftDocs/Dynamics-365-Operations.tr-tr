---
title: Oranları yapılandırma
description: Microsoft Dynamics 365 Human Resources'ta oranlar bir kazanç için katkıda bulunan ne kadar işveren ve çalışanların olduğunu tanımlar.
author: andreabichsel
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e397e20b6b6307349020c8dfd238b4b59eeca527
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420962"
---
# <a name="configure-rates"></a>Oranları yapılandırma

Microsoft Dynamics 365 Human Resources'ta oranlar bir kazanç için katkıda bulunan ne kadar işveren ve çalışanların olduğunu tanımlar. Konfigürasyonunuza bağlı olarak değer bir tutar veya esnek jenerik olabilir.

Çeşitli etkenlere bağlı olarak, her bir kazançla ilgili ve işverenler ne kadar çalışanın ödeme yapıldığını belirlemek için oranları kullanın. Kapsam oranlarının geçerlilik tarihi olduğundan, oranların geçmiş kaydını tutabilirsiniz. 

## <a name="set-up-rates"></a>Oranlarını ayarla

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Oranlar**'nı seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Ücret** | Kazanç oranı tanımlayan benzersiz ad. |
   | **Tanım** | Kazanç oranının açıklaması. |
   | **Yürürlüğe giriş** | Oranın etkin olduğu tarihi. Geçerli sistem tarihi varsayılan değerdir. 
   | **Bitiş tarihi** | Oranın bitiş tarihi. Varsayılan değer 12/31/2154'dir ve hiçbir zaman bunu belirtir. |
   | **Katmanları kullan** | Kazanç oranı hesaplamasında kullanılacak katman. Bir katman için tek katman kazanç oranı veya iki katmanlı bir kazanç oranı için çift katman. Çift katmanlı bir örnek, cinsiyet ve yaşına dayalı bir katmana örnektir. |
   | **Ödeme sıklığı** | En prim oranının kazanç sağlayıcısına nasıl ödeneceğini belirleyen ödeme sıklığı. Örneğin, ödeme sıklığı aylık ise, kazanç oranı aylık ödeme tutarını gösterir. |
   | **Ödeme sıklığı oran yuvarlaması** | Hızı yuvarlama yöntemi: Standart veya kesilmiş. |
   | **Sigara İçmeyen Personel tutarı** | Sigara olmayan çalışan için kazanç sağlayıcısı masrafın tutarı. Bu, işverenin kazanç sağlayıcısına ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **Sigara İçmeyen İşveren tutarı** | Sigara olmayan çalışan için kazanç sağlayıcısı masrafın tutarı. Bu, işverenin kazanç sağlayıcısına ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **Sigara İçen Personel tutarı** | Sigara içen çalışan için kazanç sağlayıcısı masrafın tutarı. Bu, işverenin kazanç sağlayıcısına ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **Sigara İçen İşveren tutarı** | Sigara içen çalışan için kazanç sağlayıcısı masrafın tutarı. Bu, işverenin kazanç sağlayıcısına ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **İdari tutar** | Üçüncü şahıs Yöneticisi tarafından Masraflandırılan yönetim tutarı. Bu, işverenin üçüncü taraf yöneticiye ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **Esnek kredi oranı** | Kazanç maliyetlerinin esnek kredi sayısı. Bu yalnızca esnek kredi programlarıyla ilgili kazanç planları için olan oranlar için geçerlidir. Katman oranları kullanırsanız, esnek kredi oranı eylemler > katman hızlarında tanımlanmıştır. |
   | **Yürürlük tarihini değiştir** | Kazanç oranı değişikliğinin yürürlüğe gireceği tarih Sistem, kazanç oranını otomatik olarak değiştirir ve güncelleştirme işlemini çalıştırdığınız sürece, bu Oran ile ilişkili tüm kazanç planlarını güncelleştirir. Sistemin, çalışan kazanç planlarını bu oranı temel alarak otomatik olarak güncelleştirmesini istiyorsanız bu tarihi ayarlamayın. Bu normalde otomatik olarak gelecekteki Kur değişikliği işlemine ayrılmıştır. Değişiklik geçerlilik tarihi, kullanım oranı etkili ve son kullanma tarihleri arasında olmalıdır. |
   | **Oran değişikliği tamamlandı** | Kazanç oranı değişiklikleri kesinti ile yapılan güncelleştirme değişikliği işlemesi ile tamamlandıktan sonra **Oran değişikliği tamamlandı** onay kutusu otomatik olarak seçilir. |

4. Hazırlık oranı kurulumunda yapılan değişiklikleri izlemek ve sürdürmek için **eylemler**'i seçin ve **sürümleri koru**'yu seçin.

5. **Kaydet**'i seçin. 

## <a name="set-up-tier-rates"></a>Katman oranlarını ayarlama

Oran çeşitli etkenlere bağlı olarak farklılık gösterdiği takdirde, katman oranlarını Kur içinde kullanabilirsiniz. Örneğin, yaşınız 34,99'dan küçükse sigara içilmeyen tutarın 2 olması için katman oranlarını konfigüre edebilirsiniz. Yaşınız 39,99'dan küçükse sigara olmayan tutar 3 ' dir.

Çift katman da kullanabilirsiniz. **Oranı ayarla** formunda **katman kullan** değeri için **çift katman**'ı seçerseniz, iki boyuta dayalı oranlar tanımlayabilirsiniz. Örneğin, erkekseniz ve yaşınız 34,99'dan küçükse sigara içilmeyen tutarın 2 olması için çift katman sistemini konfigüre edebilirsiniz. Erkekseniz ve Yaşınız 39,99'dan küçükse sigara olmayan tutar 3 ' dir. Kadınsanız ve Yaşınız 34,99'dan küçükse sigara olmayan tutar 1,8 ' dir. Kadınsanız ve Yaşınız 39,99'dan küçükse sigara olmayan tutar 2,8 ' dir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Oranlar**'nı seçin.

2. Listeden bir veya daha fazla oran seçin, **eylemler**'i seçin ve **katman oranları**'nı seçin.

3. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- | 
   | **Açıklama** | **Açıklama** alanının değeri Kur ayarlama kaydındaki tanımlamadan uygulanacak. Bu, katman fiyatlarının hangi fiyat kurulumunda bağlantılı olduğunu belirlemenize yardımcı olur. |
   | **Katman kodu** | Katman kodu seçin. Katman kodları katman kodları formunda tanımlanmıştır. Sistem, kılavuzdaki katman kodunun açıklamasını otomatik olarak görüntüleyecektir. |
   | **Katman türü** | Katman oranı hesaplama işlemi için seçim ölçütü olarak kullanılacak alanı belirtir. Örneğin:</br></br><ul><li>**Yaş** kullanılırsa, sistem çalışanın ilk tarihini kazanç oranı hesaplama sürecinde kullanır.</li><li>**Maaş** kullanılırsa, sistem çalışanın yıllık kazanç maaşı kazanç oranı hesaplama sürecinde kullanır.</li><li>**İş türü** kullanılıyorsa, sistem pozisyonla bağlantılı iş kaydına göre iş türünü belirlemek için çalışanın geçerli etkin pozisyon kaydını kullanır.</li></ul></br></br>Katman türleri **yaş**, **maaş**, **fiziksel**, **cinsiyet**, **tam zaman eşdeğeri**, **iş türü**, **ücret bölgesi** ve **düzeydir**. | 
   | **Raf** | Kazanç oranı hesaplama işlemi sırasında katman türüyle kullanılacak değer. Örneğin:</br></br><ul><li>Katman türü **yaş** ise, bu yaş değeri olacaktır.</li><li>Katman türü **Maaş** ise, bu maaş tutarı olacaktır.</li><li> Katman türü **İş türü** ise, bu iş türü olacaktır.</li></ul></br></br>**Yaş** veya **maaş** katman türü ile , **düzey** alanındaki değer katmanın üst sınırını temsil eder. **İş türü** katman türünde ise, sistem katman hızı seçimi sırasında tam eşleşme yaklaşımı kullanır. |
   | **Hesaplama türü** | Hesaplama Tutarı alanında tutarın nasıl kullanılacağını ve gerektiğinde hangi matematik hesaplamasının gerçekleştirileceğini belirtir. Hesaplama türü sabit bir tutarsa, sistem tutar alanlarını olduğu gibi kullanır. Hesaplama türü maaş veya kapsamın $ tutarı başınaysa sistem kendi matematik hesaplamasında hesaplama tutarı ve hesaplama yönünü kullanır.</br></br>Hesaplama türü maaşın $ tutarı başına ise, sistem aşağıdaki matematik denklemini kullanır:</br></br>Hesaplama tutarıyla (yukarı veya aşağı yuvarlanmış) bölünen yıllık kazanç maaşı sigara içen veya içmeye bir çalışan ya da işveren için tutarla çarpılır.</br></br>Hesaplama türü kapsamın $ tutarı başına ise, sistem aşağıdaki matematik denklemini kullanır:</br></br>Hesaplama tutarıyla (yukarı veya aşağı yuvarlanmış) bölünen kapsam miktarı sigara içen veya içmeye bir çalışan ya da işveren için tutarla çarpılır.</br></br>Her iki hesaplamada de, yıllık kazanç maaş veta Kapsam tutarının hesaplama tutarı yukarı veya aşağı bölünmesiyle ayrılmayacağını belirlemek için hesaplama yönü kullanılır. |
   | **Hesaplama tutarı** | Kazanç oranı hesaplamasında kullanılacak tutar. Bu tutar, katman oranının matematik hesaplaması sırasında bölendir olur. |
   | **Hesaplama yönü** | Hesaplanan sonuç tutarının yuvarlanması gereken yönü gösteren yön. Sistem üç hesaplama yönü destekliyor: boş (tam Yöntem), **artış** ve **azalma**.</br></br><ul><li>Boş bırakılırsa, sistem maaş/kapsam tutarının hesaplama tutarına bölünmesiyle elde edilen tam hesaplamayı kullanır. Bu değerin bir kesri varsa, sistem bu değeri kendi hesaplamasında kullanır.</li><li>**Artış** ise, sistem maaş/kapsam tutarının hesaplama tutarına bölünmesiyle elde edilen matematiksel hesaplama tutarını sonraki tamsayıya büyütür, bu sayı 12,25 artırmak için 13'e kadar artar.</li><li>**Azalma** ise, sistem maaş/kapsam tutarının hesaplama tutarına bölünmesiyle elde edilen matematiksel hesaplama tutarını geçerli tamsayıya azalır, bu sayı 12,25'den 12'e azalır.</li></ul> |
   | **Sigara İçmeyen Personel tutarı** | Sigara olmayan çalışan için kazanç sağlayıcısı masrafın tutarı. Bu, işverenin kazanç sağlayıcısına ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **Sigara İçmeyen İşveren tutarı** | Sigara olmayan çalışan için kazanç sağlayıcısı masrafın tutarı. Bu, işverenin kazanç sağlayıcısına ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **Sigara İçen Personel tutarı** | Sigara olmayan çalışan için kazanç sağlayıcısı masrafın tutarı. Bu, işverenin kazanç sağlayıcısına ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **Sigara İçen İşveren tutarı** | Sigara olmayan çalışan için kazanç sağlayıcısı masrafın tutarı. Bu, işverenin kazanç sağlayıcısına ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **İdari tutar** | Üçüncü şahıs Yöneticisi tarafından Masraflandırılan yönetim tutarı. Bu, işverenin üçüncü taraf yöneticiye ödediği tutardır ve Kurun oran ayarına göre ödeme sıklığını temel almak zorunda değildir. |
   | **Esnek Kredi Sigara İçmeyen Oranı** | Sigara içmeyenler için bir katman düzeyi için tanımlanan hesaplamaya göre, esnek kredi kazanç masraflarının sayısı. Örneğin, hesaplama türü **$ başına kapsam tutarı** ise, hesaplama tutarı 10.000'dır ve sigara içmeyen esnek alacak oranı 6'dır. Yani, Sigara içmeyen çalışan 10.000 $ kapsamını seçerse maliyet 6 esnek alacak olacaktır. Kapsamı $20.000 seçerse maliyet 12 esnek kredi olur vb. |
   | **Esnek Kredi Sigara İçen Oranı** | Sigara içenler için bir katman düzeyi için tanımlanan hesaplamaya göre, esnek kredi kazanç masraflarının sayısı. |

5. **Kaydet**'i seçin. 

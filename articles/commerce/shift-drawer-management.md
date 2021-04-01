---
title: Vardiya ve kasa çekmecesi yönetimi
description: Bu konu, Commerce satış noktasında (POS) vardiyaların nasıl kurulup kullanılacağını açıklamaktadır.
author: jblucher
manager: AnnBe
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c1038b0ec80ec3441e508bcf51bca0dac01cbd0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234473"
---
# <a name="shift-and-cash-drawer-management"></a>Vardiya ve kasa çekmecesi yönetimi

[!include [banner](includes/banner.md)]

Bu konu, Commerce satış noktasında (POS) vardiyaların nasıl kurulup kullanılacağını açıklamaktadır.

Dynamics 365 Commerce'de *vardiya* terimi, zamanda iki nokta arasındaki POS hareket veri ve etkinliklerinin toplamını ifade eder. Her bir vardiya için, beklenen para tutarı, sayılıp bildirilen tutarla karşılaştırılır.

Vardiyalar genellikle iş gününün başlangıcında açılır. Bu noktada, kullanıcı, kasa çekmecesindeki başlangıç tutarını bildirir. Bunun ardından, gün içinde satış hareketleri gerçekleştirilir. Son olarak, günün sonunda çekmece sayılır ve kapanış tutarları bildirilir. Vardiya kapatılır ve bir Z raporu oluşturulur. Z raporu, fazlalık veya eksiklik olup olmadığını gösterir.

## <a name="typical-shift-scenarios"></a>Tipik vardiya senaryoları

Commerce, POS için geniş bir gün sonu işletme işlemi yelpazesini desteklemek üzere çeşitli yapılandırma seçenekleri ve POS işlemleri sunar. Bu bölümde, bazı tipik vardia senaryoları açıklanmaktadır.

### <a name="fixed-till"></a>Sabit kasa çekmecesi

Geleneksel olarak bu senaryo en sık kullanılan senaryo olmuştur. Halen yaygın olarak kullanılmaktadır Bir "sabit kasa çekmecesinde" vardiya ve kasa çekmecesi belirli bir kasayla ilişkilidir. Bunlar bir kayıttan diğerine geçmez. "Sabit kasa çekmeceli" bir vardiya tek bir kullanıcı tarafından veya birden fazla kullanıcıyla paylaşılarak kullanılabilir. "Sabit kasa çekmeceli" vardiyalarda özel bir yapılandırma gerekmez.

### <a name="floating-till"></a>Devredilen kasa çekmecesi

"Devredilen kasa çekmeceli" vardiyada vardiya ve para çekmecesi bir kasadan diğerine geçirilebilir. Bir kasada para çekmecesi başına yalnızca bir etkin vardiya olabilir ancak vardiyalar askıya alınıp daha sonra veya başka bir kasada devam ettirilebilir.

Diyelim ki bir mağazada iki kasa var. Her kasa günün başlangıcında açılıyor ve o anda kasiyer yeni bir vardiya açıp başlangıç tutarını giriyor. Bir kasiyer mola vermeye hazır olduğu zaman vardiyasını askıya alır ve kasa çekmecesini para çekmecesinden alır. O kasa bundan sonra diğer kasiyerlerin kullanımına uygun hale gelir. Başka bir kasiyer o kasada kendi vardiyasına girip vardiyasını açabilir. İlk kasiyerin molası sona erince, kullanılabilir hale gelen diğer kasalardan birinde vardiyasına devam edebilir. "Devredilen kasa çekmeceli" vardiyalarda özel bir yapılandırma veya izin gerekmez.

### <a name="single-user"></a>Tek kullanıcı

Birçok perakendeci, para çekmecesindeki nakdin sayılabilirlik düzeyini en yüksekte tutmaya yardımcı olması için vardiya başına bir kullanıcıya izin vermeyi tercih etmektedir. Bir vardiyayla ilişkili kasa çekmecesini yalnızca bir kişinin kullanmasına izin verilirse, o kullanıcı tüm uyuşmazlıkların tek sorumlusu sayılabilir. Bir vardiyayı birden fazla kullanıcı kullanıyorsa, hatayı kimin yaptığını veya kasa çekmecesinden kimin para çalmaya çalıştığını belirlemek güç olur.

### <a name="multiple-users"></a>Birden çok kullanıcı

Bazı perakendeciler tek kullanıcılı vardiyaların sağladığı hesaplanabilirlik düzeyinden ödün vererek vardiya başına birden fazla kullanıcıya izin vermeyi tercih ediyor. Bu yaklaşım genellikle mevcut kasa sayısından daha fazla kullanıcı olduğu, esneklik ve hız gereksiniminin olası kayıplardan daha öncelikli olduğu durumlar için geçerlidir. Ayrıca, mağaza yöneticilerinin kendi vardiyalarının olmadığı ve gerektiğinde kasiyerlerinin vardiyalarını kullandıkları durumlarda da yaygındır. Başka bir kullanıcının açtığı vardiyada oturum açıp kullanmak isteyen kullanıcının **Çoklu oturum açmaya izin ver** POS iznine sahip olması gerekir.

### <a name="shared-shift"></a>Paylaşılan vardiya

"Paylaşılan vardiya" yapılandırması, perakendecilerin birden fazla kasa, para çekmecesi ve kullanıcı için tek bir vardiyaya sahip olmasına olanak sağlar. Paylaşılan vardiyada, tüm para çekmeceleri genelinde özetlenen tek bir başlangıç tutarı ve tek bir kapanış tutarı vardır. Paylaşılan vardiyalar en çok mobil cihazlarda kullanılır. Bu senaryoda her kasa için ayrı birer para çekmecesi tahsis edilmemiştir. Bunun yerine, tüm kasalar tek bir para çekmecesini paylaşabilir.

Bir mağazada paylaşılan vardiyaların kullanılabilmesi için, para çekmecesinin **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> Donanım profilleri \> Çekmece**'de bir "paylaşılan vardiya çekmecesi" olarak yapılandırılması gerekir. Ayrıca, kullanıcılar, paylaşılan vardiya izinlerinin ("Paylaşılan vardiyayı yönetmeye izin ver" ve "Paylaşılan vardiyayı kullanmaya izin ver") birine veya her ikisine birden sahip olmalıdır.

> [!NOTE]
> Her bir mağazada aynı anda yalnızca bir paylaşılan vardiya açılabilir. Aynı mağazada paylaşılan vardiyalar ve bağımsız vardiyalar kullanılabilir.

## <a name="shift-and-drawer-operations"></a>Vardiya ve çekmece işlemleri

Bir vardiyanın durumunu değiştirmek veya para çekmecesindeki para tutarını artırmak ya da azaltmak için çeşitli işlemler yapılabilir. Bu konu Modern POS ve Bulut POS için vardiya operasyonlarını açıklar.

### <a name="open-shift"></a>Açık vardiya

POS, kullanıcıların satış, iade veya müşteri siparişi gibi mali bir hareket üretecek herhangi bir işlem gerçekleştirebilmesi için etkin ve açık vardiyasının olmasını gerektirir.

Bir kullanıcı POS'ta oturum açtığı zaman sistem ilk olarak mevcut kasada o kullanıcı için etkin bir vardiya olup olmadığını doğrular. Etkin bir vardiya yoksa, kullanıcı, sistem yapılandırmasına ve sahip olduğu izinlere bağlı olarak yeni bir vardiya açabilir, mevcut bir vardiyayı sürdürebilir veya "çekmece yok" modunda oturum açabilir.

### <a name="declare-start-amount"></a>Başlangıç tutarını beyan et

Bu işlem genellikle yeni açılan bir vardiya için yapılan ilk işlemdir. Bu işlem için, kullanıcılar vardiya için para çekmecesindeki başlangıç nakit tutarını belirtir. Bu işlem önemlidir çünkü bir vardiya kapatılırken yapılan fazlalık/eksiklik hesaplamasında başlangıç tutarı dikkate alınır.

### <a name="float-entry"></a>Kasa devri girişi

*Kasa devri girişleri*, para çekmecesindeki nakit tutarını artırmak için etkin bir vardiyada gerçekleştirilen satış dışı hareketlerdir. Kasa devri girişine tipik bir örnek, azalmaya başladığında çekmeceye ilave para ekleme hareketidir.

### <a name="tender-removal"></a>Ödeme kaldırma

*Ödeme kaldırma işlemleri*, etkin bir vardiyada para çekmecesindeki nakit tutarını azaltmak için gerçekleştirilen satış dışı hareketlerdir. Bu işlem çoğunlukla farklı bir vardiyadaki Kasa devri giriş işlemiyle birlikte kullanılır. Örneğin kasa 1'de para azalmaktadır ve kasa 2'deki kullanıcı para çekmecesinin tutarını azaltmak için bir ödeme kaldırma işlemi gerçekleştirmektedir. Bu durumda kasa 1'deki kullanıcı, para çekmecesindeki tutarı artırmak için bir kasa devri girişi yapar.

### <a name="suspend-shift"></a>Vardiyayı askıya al

Kullanıcılar, kasayı başka bir kullanıcıya bırakmak için etkin vardiyalarını askıya alabilir veya vardiyalarını farklı bir kasaya taşıyabilir (bu durumda vardiyaya genellikle "devredilen kasalı" vardiya denir).

Vardiyanın askıya alınması, vardiya yeniden başlatılana kadar yeni hareketleri veya değişiklikleri önler.

### <a name="resume-shift"></a>Vardiyayı devam ettir

Bu işlem, kullanıcılara etkin vardiyası olmayan bir kasada daha önce askıya alınmış bir vardiyayı devam ettirme olanağı sağlar.

### <a name="tender-declaration"></a>Kasa sayımı

Bu işlem, para çekmecesindeki mevcut para tutarı toplamını belirtmek için yapılır. Kullanıcılar bu işlemi çoğu zaman bir vardiyayı kapatmadan önce yapar. Belirtilen tutar, beklenen vardiya tutarıyla karşılaştırılarak fazla/eksik tutar hesaplaması yapılır.

### <a name="safe-drop"></a>Kasaya para nakli

Kasaya para nakli etkin bir vardiya sırasında istenildiği zaman gerçekleştirilebilir. Bu işlem parayı para çekmecesinden çıkarır ve para böylece arka odadaki bir kasa gibi daha güvenli bir yere aktarılır. Kasaya para nakilleri için kaydedilen toplam tutar vardiya toplamlarına dahil edilir ancak kasa sayımının bir parçası olarak sayılması gerekmez.

### <a name="bank-drop"></a>Bankaya para nakli

Kasaya para nakli gibi, bankaya para nakli de etkin vardiyalarda gerçekleştirilir. Bu işlem bankaya yatırılmak üzere hazırlamak için parayı vardiyadan çıkarır.

### <a name="blind-close-shift"></a>Vardiyayı tamamen kapat

*Tamamen kapalı vardiyalar*, artık etkin olmayan ama tam kapatılmamış vardiyalardır. Askıya alınan vardiyalardan farklı olarak, tamamen kapalı vardiyalar devam ettirilemez. Bununla birlikte, bu vardiyalardaki "Başlangıç tutarını beyan et" ve "Kasa sayımı" gibi işlemler daha sonra veya farklı bir kasada yapılabilir.

Tamamen kapalı vardiyalar genellikle kasayı önce tamamen sayım saymadan, mutabakat sağlamadan veya vardiyayı kapatmadan yeni bir kullanıcıya veya vardiyaya bırakmak için kullanılır.

### <a name="close-shift"></a>Vardiyayı kapat

Bu işlem vardiya toplamlarını, fazla/eksik tutarları hesaplar ve ardından etkin veya tamamen kapalı vardiyayı sonlandırır. Kullanıcı izinlerine bağlı olarak, vardiya için bir Z raporu da yazdırılır. Kapatılan vardiyalar devam ettirilemez veya değiştirilemez.

### <a name="print-x"></a>X Yazdır

Bu işlem, mevcut etkin vardiya için bir X raporu oluşturup yazdırır.

### <a name="reprint-z"></a>Z'yi yeniden yazdır

Bu işlem, bir vardiya kapatılırken sistemin oluşturduğu son Z raporunu yeniden yazdırır.

### <a name="manage-shifts"></a>Vardiyaları yönet

Bu işlem, kullanıcıların mağazaya ilişkin tüm etkin, askıya alınmış veya tamamen kapalı vardiyaları görmesini sağlar. Kullanıcılar kendi izinlere bağlı olarak, tamamen kapalı vardiyalar için Kasa sayımı ve Vardiyayı kapat gibi işlemleri gibi son kapanış yordamlarını uygulayabilirler. Bu işlem kullanıcıların, çevrimdışı ve çevrimiçi modlar arasında geçiş yapıldıktan sonra vardiyaların kötü durumda bırakıldığı ender durumlarda geçersiz vardiyaları görüntülemesine ve silmesine olanak sağlar. Bu geçersiz vardiyalar mutabakat için gerekli herhangi bir mali bilgi veya hareket verisi içermez.

## <a name="shift-and-drawer-permissions"></a>Vardiya ve çekmece izinleri

Aşağıdaki POS izinleri, bir kullanıcının çeşitli senaryolarda yapabileceklerini ve yapamayacaklarını belirler:

- **Tamamen kapatmaya izin ver**
- **X raporu yazdırmaya izin ver**
- **Z raporu yazdırmaya izin ver**
- **Kasa sayımına izin ver**
- **Kasada kalan tutar bildirimine izin ver**
- **Satış olmadan çekmeceyi aç**
- **Çoklu oturum açmaya izin ver** – Bu izin, kullanıcının başka bir kullanıcı tarafından açılan bir vardiyada oturum açıp o vardiyayı kullanmasına olanak sağlar. Bu izne sahip olmayan kullanıcılar yalnızca kendi açtıkları vardiyalarda oturum açıp kullanabilir.
- **Paylaşılan vardiyayı yönetmeye izin ver** – Kullanıcılar, paylaşılan bir vardiyayı açmak veya kapatmak için bu izne sahip olmalıdır.
- **Paylaşılan vardiyayı kullanmaya izin ver** – Kullanıcılar, paylaşılan bir vardiyada oturum açıp kullanmak için bu izne sahip olmalıdır.

## <a name="back-office-end-of-day-considerations"></a>Arka ofis gün sonu ile ilgili notlar

POS'ta vardiyaların ve para çekmecesi mutabakatının kullanılma yöntemi, ekstre hesaplaması sırasında hareket verilerinin özetlenme yönteminden farklıdır. Bu farkı anlamanız önemlidir. Yapılandırmanıza ve iş süreçlerinize bağlı olarak, POS'taki vardiya verileri (Z raporu) ve arka ofisteki hesaplanan bir ekstre size farklı sonuçlar verebilir. Bu fark mutlaka vardiya verilerinden veya hesaplanan ekstreden birinin yanlış olduğu veya verilerle ilgili bir sorun olduğu anlamına gelmez. Bu, yalnızca, belirtilen parametrelerin daha fazla veya daha az hareket içerebileceği ya da hareketlerin farklı özetlendiği anlamına gelir.

Her perakendecinin iş gereksinimleri farklı olmakla birlikte, sisteminizi bu türde farkların oluştuğu durumları önleyecek şekilde kurmanızı tavsiye ederiz:

**Retail ve Commerce \> Kanallar \> mağazaları \> Tüm mağazaları \> Ekstre/kapanış**'a gidin ve her mağaza için hem **Ekstre yöntemi** alanının hem de **Kapatma yöntemi** alanının ayarını **Vardiya** yapın.

Bu kurulum, arka ofis ekstrelerinde POS'taki vardiyalarınkiyle aynı hareketleri içermesinin ve verilerin o vardiyayla özetlenmesinin garanti edilmesine yardımcı olur.

Ekstre ve kapatma yöntemleri hakkında daha fazla bilgi için bkz. [Perakende ekstreleri için mağaza yapılandırmaları](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
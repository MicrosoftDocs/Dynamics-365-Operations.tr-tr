---
title: Konsolide mali tabloları oluşturma
description: Bu konuda, konsolide mali tabloları oluşturabileceğiniz çeşitli senaryolar açıklanmaktadır.
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a32fb8cce4353f57155fc7a723aa90e3c17178e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448865"
---
# <a name="generate-consolidated-financial-statements"></a>Konsolide mali tabloları oluşturma

[!include [banner](../includes/banner.md)]

Bu konuda, konsolide mali tabloları oluşturabileceğiniz çeşitli senaryolar açıklanmaktadır.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Tüzel kişilikler arasındaki tek düzeyli ve birden fazla düzeyli konsolidasyonlar
Mali raporlamayı kullanarak konsolide etmek için en kolay yöntem aynı hesap planı ve mali dönemlere sahip şirketler arasında verileri toplamak için raporlama ağaçları kullanmaktır. Raporlama ağacı kullanarak konsolide etmek için üst düzey adımlar şunlardır.

1. Satır tanımı oluşturun ve tüm şirketlerdeki tüm uygun hesapların satırlarda bulunduğundan emin olun.
2. Oluşturduğunuz rapor için gerekli olan tüm sütunları içeren bir sütun tanımı yapın.
3. Konsolide raporları kullandığınız her şirket için raporlama düğümü içeren bir raporlama ağacı oluşturun.

> [!TIP]
> Satır tanımlarının, sütun tanımlarının ve raporlama ağaçlarının nasıl oluşturulacağı ve yönetileceği hakkında daha fazla bilgi için bkz. [Mali rapor bileşenleri](../../dev-itpro/analytics/financial-report-components.md).

Aşağıdaki çizim, konsolide edeceğiniz her bir şirketi tanımlamak için Mali raporlamada raporlama ağacı tanımını nasıl kullanabileceğinizi gösterir.

![Raporlama ağacı tanımı](./media/reporting-tree-definition.png "Raporlama ağacı tanımı")

Aşağıdaki çizimde, konsolide edilen raporun gösterdiği üzere raporlama ağacını rapor tanımı ile birlikte kullanırken her bir şirketi ayrı ayrı görüntüleyebilirsiniz. Özet düzeyinde konsolide tutarlar gösterilir.

![Tutar özet düzeyini konsolide etme](./media/consolidate-amount-summary-level.png "Tutar özet düzeyini konsolide etme")

İhtiyaç duyduğunuz birçok düzeyi içeren çok düzeyli bir raporlama ağacı da oluşturabilirsiniz. Aşağıdaki çizim, dünya çapında bölgelere göre toplamlara sahip olan çok düzeyli bir raporlama ağacı tanımını gösterir.

![Bölgelere göre toplamları olan çok düzeyli raporlama ağacı tanımı](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Bölgelere göre toplamları olan çok düzeyli raporlama ağacı tanımı")

Aşağıdaki çizim, dünya çapında işlevlere göre toplamlara sahip olan çok düzeyli bir raporlama ağacı tanımını gösterir.

![İşlevlere göre toplamları olan çok düzeyli raporlama ağacı tanımı](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "İşlevlere göre toplamları olan çok düzeyli raporlama ağacı tanımı")

### <a name="viewing-companies-side-by-side"></a>Şirketleri yan yana görüntüleme
Birçok müşteri şirketlerin yan yana görüldüğü ve bir sütunun konsolide toplamı gösterdiği raporları tercih etmektedir. Raporlama ağacı oluşturduktan sonra bu biçimi kolaylıkla elde edebilirsiniz. Konsolide mali tablolarda şirketleri yan yana görüntülemek için üst düzey adımlar şunlardır.

1. Her bir şirket için bir **Mali Boyut** içeren bir sütun tanımı yapın.
2. Her sütun için ağaç ve raporlama birimi seçmek üzere **Raporlama Birimi** alanını kullanın.
3. İsteğe bağlı: Başlıkları ve toplam sütunlarını ekleyin.

Aşağıdaki çizim, yan yana biçimdeki bir sütun tanımını gösterir.

![Yan yana biçimdeki sütun tanımı](./media/column-definition-side-by-side-format.png "Yan yana biçimdeki sütun tanımı")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Tüzel kişilikten oluşturulan kuruluş yapılarını kullanan konsolidasyonlar
Boyutları veya tüzel kişilikleri içeren kuruluş hiyerarşileri Mali raporlamada dinamik olarak raporlama ağacı tanımlarını oluşturur. Konsolidasyonları kolaylaştırmanın kolay bir yolu Mali raporlamada raporunuza bir kuruluş hiyerarşisi eklemektir. Mali raporlama aşağıdaki çizimde gösterildiği üzere rapor tarihine bağlı olarak yürürlük tarihinde veya öncesinde kuruluş hiyerarşisini seçer.

![Dinamik olarak raporlama ağacı tanımı oluşturma](./media/dynamically-create-reporting-tree-definitions.png "Dinamik olarak raporlama ağacı tanımı oluşturma")

## <a name="consolidations-that-involve-eliminations"></a>Elemeleri içeren konsolidasyonlar
Eliminasyon hareketleri, konsolidasyon işleminin ortak bir bölümüdür. Bu örnekte konsolidasyon sırasında beş hesap elenmektedir: 142600, 211400, 401420, 401180 ve 510820. Şirketler, şirketlerarası hesaplarını farklı şekilde ayarlayabilir. Örneğin, hesap şirketlerarası hareketlerde kullanılıyorsa bazı şirketler son basamağı 9 olarak ayarlayabilir. Yöntemden bağımsız olarak, şirketlerarası hesapları biliyorsanız konsolide mali tablolarınızda eliminasyonları gösterebilirsiniz.

Aşağıdaki çizim, konsolide gelir tablosu için bir sütun tanımı gösterir. Boyut filtresi kullanılarak her bir şirket için üç adet şirketlerarası kar ve zarar hesabı tanımlanır. D sütunu sadece USMF şirketi için eliminasyon hesapları içerir. E sütunu ise sadece DEMF şirketi için eliminasyonlar içerir. D sütunu da E sütunu da mali tabloda **yazdırılmayacak şekilde** ayarlanır.

![Sütun tanımı konsolide gelir tablosu](./media/column-definition-consolidated-income-statement.png "Sütun tanımı konsolide gelir tablosu")

Rapor oluşturulurken eliminasyon tutarları F, G ve H sütunlarında hesaplanır ve I sütununda toplanır. J sütunu konsolide tutarları gösterir. Bu konsolidasyon tutarlarına USMF, USRT ve DEMF şirketleri için olan eliminasyonlar dahil değildir.

> [!TIP]
> Sadece eliminasyon girişlerini gösteren ikinci bir rapor oluşturun ve bunu konsolide raporunuzu içeren bir rapor grubunda kullanın. Bu şekilde, gerekli olan günlük girişlerini oluşturmak için gerekli tüm bilgilere sahip olursunuz.

Aşağıdaki çizim, konsolide raporu gösterir.

![Konsolide rapor gelir tablosu](./media/consolidated-report-income-statement.png "Konsolide rapor gelir tablosu")

Hesapları, boyutları veya her ikisini birden kullansanız da Mali raporlama size boyut filtreleme yeteneklerini kullanarak eliminasyon girişlerini filtreleme olanağı tanır.

## <a name="minority-interest"></a>Azınlık hissesi
Bir şirket başka bir şirketin sadece bir miktarına sahip olabilir. Bu durumda bir konsolide rapor oluştururken sadece şirketin sahip olduğu yüzde için hesap yapmanız önemlidir. Kullanıcı tercihine bağlı olarak, azınlık hisseyi göstermek için birden fazla Mali raporlama yolu vardır. Bir tanesi raporlama ağacı tanımında toplam yüzdeyi kullanmaktır. Diğer bir yol raporda azınlık sahipliğini ayrı bir satır olarak göstermektir.

### <a name="using-the-reporting-tree-definition"></a>Raporlama ağacı tanımını kullanma
Aşağıdaki çizimde gösterildiği üzere raporlama ağacı tanımında **Toplama %'si** sütununa (H sütunu) sahiplik yüzdesini girin. Rapor oluşturulurken bu yüzde konsolide tutarı hesaplamak için kullanılır. Bu örnekte Contoso, Contoso Germany'nin sadece yüzde 80'ine sahiptir. **Toplama %'si** sütununda **80** veya **.8** değerini girebilirsiniz ve konsolide düzey için yüzde 80 toplanır.

> [!NOTE]
> Bu sahiplik yüzdesini sadece şirket düzeyinde değil herhangi bir raporlama birimi için de uygulayabilirsiniz. 

![Raporlama ağacı tanım yüzdesini kullanma](./media/Using-reporting-tree-definition-percentage.png "Raporlama ağacı tanım yüzdesini kullanma")

Rapor oluşturulurken Contoso Germany raporu satış tutarının yüzde 100'ünü gösterir ve tutarın yüzde 80'i satışlar için konsolide düzeyde tahsis edilir ve toplanır.

Aşağıdaki çizimde gösterildiği üzere bir şirketin yüzde 1'inden azına sahipseniz **Rapor Ayarları** sayfasının **Ek Seçenekler** sekmesinde **%1'den az toplamaya izin ver** onay kutusunu seçebilirsiniz. Bu durumda raporlama ağacında **Toplama %'si** sütunundaki değerler yüzde 1'den az olarak değerlendirilir. Örneğin **,8** girerseniz konsolide düzey için yüzde 80 değil, yüzde 0,8 toplanır. Alternatif olarak **% 1'den az toplamaya izin ver** onay kutusunu boş bırakarak ve **Toplama %'si** sütununa **,008** girerek de aynı sonuca ulaşabilirsiniz.

![Raporlama ayarı seçenekleri](./media/reporting-setting-options.png "Raporlama ayarı seçenekleri")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Konsolide raporda sahipliği ayrı bir satır olarak gösterme
Azınlık hissesi için başka bir seçenek raporda her bir satırda yan kuruluşu yüzde 100 göstermek ama net gelirden kontrol gücü olmayan hisseyi çıkarmaktır.

Aşağıdaki çizimde gösterildiği üzere mali raporlarda azınlık hissesini hesaplamak için satır tanımında bir **IF THEN ELSE** belirtimi ve sütun kısıtlaması kullanılabilir.

![Konsolide raporda sahipliği ayrı bir satır olarak gösterme](./media/Showing-ownership-separate-row-consolidated-report.png "Konsolide raporda sahipliği ayrı bir satır olarak gösterme")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Tüzel kişilikler arasındaki birden fazla hesap planları
Çoğunlukla farklı tüzel kişilikler farklı hesap planlarına sahiptir ama hala konsolide mali tablolar oluşturmak isterler. Bu durumda verileri konsolide etmek için mali raporlama kullanılabilir, böylece konsolide mali raporlar oluşturabilirsiniz. Tüzel kişilikler arasında farklı hesap planları varken konsolide etmek için üst düzey adımlar şunlardır.

1. Mali boyutlara birden fazla bağlantısı olan bir satır tanımı oluşturun. Her bir hesap planı için bir bağlantı olmalıdır.
2. Her bir şirketi uygun sütuna atamak için sütun tanımında raporlama birimi kısıtlaması kullanın.


Mali boyutlar için birden fazla bağlantı her bir benzersiz şirket hesap planı için satır tanımında her bir satıra eklenebilir. Aşağıdaki çizimde USMF şirketi ilk **Mali Boyutlarla İlişkilendir** sütununda (J sütunu) hesap kümesi kullanmakta ve DEMF şirketi ikinci **Mali Boyutlarla İlişkilendir** sütununda (K sütunu) hesaplar kullanmaktadır.

> [!TIP]
> **Mali Boyutlarla İlişkilendir** hücresi hakkında daha fazla bilgi için Mali Boyutlarla İlişkiyi Belirtin hücresine bakın.

![İlk mali boyutlarla ilişkilendirme hesaplarını ayarlama](./media/set-accounts-first-Link-to-Financial-Dimensions.png "İlk mali boyutlarla ilişkilendirme hesaplarını ayarlama")

Her bir şirket için satır tanımından hangi mali boyutlarla ilişkilendirmenin kullanılacağını tanımlamak için raporlama ağacı kullanabilirsiniz. Aşağıdaki çizimde gösterildiği üzere E sütununda satır tanımını seçin ve sonrasında F sütununda uygun satır bağlantısını seçin.

![Kullanılan mali boyutlar satır tanımını ilişkilendirme](./media/link-financial-dimensions-row-definition-used.png "Kullanılan mali boyutlar satır tanımını ilişkilendirme")

> [!TIP]
> Mali boyutlar için ilişkilendirmeler oluştururken her bir ilişkilendirmenin uygulanacağı şirketi tanımlamak için açıklama kullanın. Bu şekilde, raporlama ağacı oluştururken doğru şirketi çok daha kolay seçebilirsiniz. Sütun tanımında **Raporlama Birimi** alanı her bir sütunu raporlama ağacının bir birimi için kısıtlamanıza olanak sağlar, böylece verileri yan yana görüntüleyebilirsiniz. Bir sütun için belirli bir şirket belirtmezseniz tüm şirketler için konsolide veriler gösterilir.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Birden fazla tüzel kişilik arasındaki farklı mali takvimler
Farklı tüzel kişilikler farklı hesap planlarına sahip olabilir ama hala konsolide mali tablolar oluşturmaları gerekir. Tüzel kişilikler arasında farklı mali dönemler mevcutken konsolide etmenin iki yolu vardır:

- Bir sütun tanımı oluşturun ve her bir şirket için uygun dönemleri eşleştirmek için dönem ve yıl kullanın.
- **Ayarlar** \> **Diğer** \> **Ek Seçenekler** altında, konsolide etmek için ya dönem bitiş tarihini ya da dönem numarasını kullanmayı seçin.

Farklı mali dönemlere sahip birden fazla şirket için sütun tanımı tasarlarken hangi şirketin rapor tanımında **Şirket adı** alanına atanacağına dikkat etmeniz önemlidir. Bu şirketin mali takvimi, rapor tanımı için temel mali takvim olarak kullanılır. Örneğin, aşağıdaki tablo USMF ve INMF şirketleri için mali dönem ayarını göstermektedir. Konsolide raporlar için USMF'nin kullandığı mali takvimi kullanmak istersiniz. Rapor 30 Haziran 2018 için oluşturulursa "Eşleştirme" sütunu her bir şirket için eşdeğer dönem ve yılı gösterir.

| Şirket   | Mali yıl                                  | Eşleştirme                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Mali yıl, 1 Temmuz ila 30 Haziran          | 12 dönem, 2018 mali yılı | 
| INMF      | Takvim yılı, 1 Ocak ila 31 Aralık | 6 dönem, 2018 mali yılı  |

Aşağıdaki çizimde, USMF şirketi rapor tanımında **Şirket adı** alanında belirtilmektedir. Bu nedenle USMF şirketinin mali takvimi, temel mali takvim olarak kullanılır. Bu örnekte rapor 30 Haziran 2018 için oluşturulurken USMF şirketi rapor tanımında 12 dönem olarak tanımlanan ESAS dönemi kullanır. INMF şirketi 6 dönem olan TEMEL-6'yı kullanır. Her iki sütun da Temmuz 2018 verilerini içerir.

![Esas dönemi raporlama](./media/report-base-period.png "Esas dönemi raporlama")

Aşağıdaki çizim, rapor tanımında konsolidasyon için kullanılmak üzere dönem numarasını veya dönem bitiş tarihini seçmenize olanak tanıyan seçenekleri gösterir.

![Rapor tanımı dönem numarası seçenekleri](./media/options-report-definition-period-number.png "Rapor tanımı dönem numarası seçenekleri")

## <a name="business-unit-consolidations"></a>İş birimi konsolidasyonları
Bu konuda, konsolidasyon amaçları için Mali raporlamada raporlama ağacı tanımlarının ve kuruluş hiyerarşisinin kullanılmasına odaklanılmaktadır. Ayrıca dünya çapında satışlar veya işlemlerle ilgili raporlar gibi iş birimi konsolidasyon raporları oluşturmak için raporlama ağacını kullanabilirsiniz. Bu raporlar ortak bir ihtiyaçtır. Bunları oluşturmak isterseniz konsolide etmek istediğiniz her bir birim için bir şirket ve bir boyut seçin. Örneğin, aşağıdaki çizimde iş birimi toplamı **Şirket** sütunundaki (A sütunu) her bir şirketi yineleyerek ve **Boyutlar** sütunundaki (D sütunu) her şirket için bir Departman boyut değerleri grubu tanımlayarak gerçekleştirilir.

![İş birimi konsolidasyon raporları](./media/business-unit-consolidation-reports.png "İş birimi konsolidasyon raporları")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Birden fazla raporlama para birimi içeren konsolidasyonlar
Mali raporlama, birden fazla para biriminde gerçek değer, bütçe, bütçe kontrolü ve bütçe planlama verilerini görüntülerken daha fazla esneklik sağlar. Karşıdan anahtar ayarlama verilerini getirerek, herhangi bir kullanıcı için herhangi bir zamanda herhangi bir para biriminde herhangi bir raporu görüntülemek için Mali raporlamada ek ayarlama yapmanıza gerek kalmaz.

### <a name="prerequisites"></a>Ön koşullar
Dönüştürülen bakiyeleri doğru şekilde hesaplamak için Mali raporlamaya göre **Yedek Akçe Hesabı** kategorisinin **Ana hesap** listesindeki Yedek Akçe hesabına atanması gerekir. Mali raporlama, Yedek Akçe hesabı için deftere nakletmeyi desteklemez. Hareketler Yedek Akçe hesabı için deftere nakledilirse dönüştürülen bakiyeler doğru şekilde hesaplanmaz. Kullanıcılara Yedek Akçe hesabı için düzeltmeleri deftere kaydetmek üzere ek bir Yedek Akçe hesabı ayarlamaları önerilir.

Aşağıdaki çizimde gösterildiği üzere her bir hesap için ana hesapta **Mali raporlama** hızlı sekmesinde **Mali raporlama döviz kuru türü** ve **Para birimi dönüştürme türü** alanları ayarlanmalıdır. Bu görevi hesaptan hesaba geçerek tamamlayabilir veya değişiklikleri aşağı kolayca yuvarlamak için hesap şablonlarını kullanabilirsiniz.

- **Mali raporlama döviz kuru türü** alanında, hesaba uygulamak için para birimlerini ve döviz kurlarını içeren döviz kuru türünü seçin. Bu para birimleri ve döviz kurları tablosu, Mali raporlamada gerçek verilere uygulanır.
- **Para birimi dönüştürme türü** alanında, hesap için döviz kurunu hesaplamada kullanılacak yöntemi seçin. Bu para birim yöntemi, Mali raporlamada hem gerçek değerler hem bütçe verileri için kullanılır.

![Mali raporlama ana hesapları](./media/Financial-reporting-main-accounts.png "Mali raporlama ana hesapları")

Bütçe, bütçe kontrolü ve bütçe planlama verileri için döviz kuru türü **Genel Muhasebe** sayfasında tanımlıdır. Döviz kurlarını çekmek için bu tablo kullanılır ve hesap için atanan para birimi dönüştürme türü kullanılır.

### <a name="currency-translation-methods"></a>Para birimi çevirme yöntemleri
Mali raporlamada döviz kurlarını hesaplamak için dört seçenek vardır:

- **Ağırlıklı ortalama**: Bu yöntem en çok kar ve zarar hesapları için kullanılır. Aşağıdaki formül kullanılır:

    (Döviz kuru × Geçerli olduğu gün sayısı) ÷ Dönemdeki gün sayısı

- **Ortalama**: Bu yöntem, kar ve zarar hesapları için alternatif bir yöntemdir. Aşağıdaki formül kullanılır:

    Döviz kurları toplamı ÷ Döviz kurları sayısı

- **Cari**: Bu yöntem en çok bilanço hesapları için kullanılır. Kullanılan döviz kuru, Mali raporlamada rapor veya sütun tarihinde veya daha öncesindeki kurdur.
- **Hareket tarihi**: Bu yöntem, sabit kıymet hesapları için kullanılır. Kullanılan döviz kuru, kıymetin alındığı gündeki kurdur. Kur o tarihte girilmezse kıymetin alınma tarihine en yakın girilmiş olan önceki kur kullanılır.

### <a name="report-designer-options-for-currency-translation"></a>Para birimi çevirme için rapor tasarımcısı seçenekleri
Mali raporlamada herhangi bir rapor herhangi bir sayıda raporlama para biriminde gösterilebilir. Aşağıdaki rapor tanımındaki alanlar bu özelliği destekler:

- **Rapor Tanımı** sayfasındaki **Para Birimi Bilgileri** bölümü. Bu bölüm, rapor oluşturulurken değerlerin gösterildiği para birimini gösterir.
- Yeni bir **Tüm raporlama para birimlerini ekle** onay kutusu. Bu onay kutusu seçildiğinde, şirketin işlevsel para birimini kullanan rapor oluşturulduktan sonra rapor kuyruğuna her bir raporlama para birimi için bir rapor eklenir. Onay kutusu işaretli değilse Web Görüntüleyici'de hala bir raporlama para birimi seçebilirsiniz. Bu durumda sadece seçtiğiniz zaman raporlama para birimi işlenir.

Rapor tanımındaki seçenekler bir raporu kolaylıkla tüm raporlama para birimlerinize dönüştürmenize olanak sağlar. Bu nedenle sadece kullanılan para birimlerinde farklılık gösteren yinelenen rapor tanımlarını eleyebilirsiniz. Yan yana birden fazla para birimini gösteren bir rapor gerekiyorsa raporun sadece o sütununu farklı bir raporlama para birimine dönüştürmek için **Sütun Tanımı** sayfasında **Para birimi ekranı** alanını kullanmaya devam edebilirsiniz.

### <a name="currency-translation-adjustment"></a>Para birimi dönüştürme düzeltmesi
Para birimi dönüştürme düzeltmesi (CTA), bilanço hesaplarını hesaplamak için kullanılan kurlar ile gelir tablosu hesapları için kullanılan kur arasındaki farktır. Bu fark, bilançonun bakiye dışı olmasına neden olur. Mali raporlamayı CTA'yı hesaplamak için iki şekilde kullanabilirsiniz:

- Aşağıdaki çizimde gösterildiği üzere satır tanımında **Yuvarlama Ayarlamaları** sayfasını kullanın.

    ![Para birimi dönüştürme düzeltmesi yuvarlama ayarlamaları](./media/Currency-translation-adjustment-rounding-adjustments.png "Para birimi dönüştürme düzeltmesi yuvarlama ayarlamaları")

    Yuvarlama ayarlamasını (CTA), toplam kıymetler satırını, toplam borçlar ve öz varlık satırını ve memnun olduğunuz eşiği göstermesi gereken satırı belirttiğinizde, Mali raporlama farkı hesaplar ve istenilen satıra koyar. Aşağıdaki çizimde gösterildiği üzere **Yuvarlama Ayarlaması** adlı bir satır oluşturulur ve detaya gidilerek gösterilir.

    ![Yuvarlama ayarlaması detayı](./media/rounding-adjustment-drill-down.png "Yuvarlama ayarlaması detayı")

- Tüm hesapları kıymetlerden giderlere bir aralığa koyun. Aşağıdaki çizimde gösterildiği üzere fark, yuvarlama ayarlaması (CTA) ile aynı tutarda olur. Bu nedenle bunu, yuvarlama ayarlaması sayfasında atlanan herhangi bir hesap bakiyesi olmadığından emin olmak için denetim toplamı olarak kullanabilirsiniz.

    ![Yuvarlama ayarlaması form denetimi](./media/rounding-adjustment-form-check.png "Yuvarlama ayarlaması form denetimi")

### <a name="balance-calculation-approach"></a>Bakiye hesaplama yaklaşımı
Mali raporlama, para birimleri kullanılırken doğru şekilde dönüştürülmüş tutarlar elde etmek üzere bakiyeler için aşağıdaki hesaplama yöntemlerini kullanır:

- **Ağırlıklı ortalama ve ortalama**: Her bir dönem, ağırlıklı ortalamasında hesaplanır ve üç aylık ve yılbaşından bugüne kadar gibi sütunlar için toplamı alınır.
- **Geçmiş**: Geçmiş çeviri yöntemini kullanan hesaplar daima hareket tarihinden geriye gider. Alım tarihi hareketle ilişkili ise bu tarih döviz kurunu almak için kullanılır. Hesaplama zamanını iyileştirmek için her bir dönem toplanır ve depolanır.
- **Geçerli**: Üç aylık ve yılbaşından bugüne kadar için olan sütunlar gibi hesaplanan ve toplanan sütunlar, sütunda veya raporda belirtilen spot kurda hesaplanır. Örneğin, **1. Üç aylık dönem** sütunu, takvim yılı kullanılıyorsa 31 Mart kurunu kullanır.

## <a name="additional-resources"></a>Ek kaynaklar

Konsolidasyon ve para birimi dönüştürmeleri hakkında daha fazla bilgi için bu konunun ana konusuna bakın: [Mali konsolidasyonlar ve para birimi dönüştürmeye genel bakış](./financial-consolidations-currency-translation.md).

Konsolidasyon bilgilerini çevrimiçi olarak nasıl gireceğiniz hakkında daha fazla bilgi için bkz. [Çevrimiçi mali konsolidasyonlar](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
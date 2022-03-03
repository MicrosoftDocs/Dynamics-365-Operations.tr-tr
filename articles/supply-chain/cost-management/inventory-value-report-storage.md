---
title: Stok değeri raporları
description: Bu konu stok değer rporlarıın nasıl kurulacağı, oluşturulacağı ve kullanılacağını açıklar. Bu raporlar, stoğunuzun fiziksel ve mali miktarları ve tutarlarınız hakkında ayrıntılar sağlar.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3da92c384d3074335067433120eccc97d11b6b81
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103952"
---
# <a name="inventory-value-reports"></a>Stok değeri raporları

[!include [banner](../includes/banner.md)]

Stok değer raporları, stoğunuzun fiziksel ve mali miktarları ve tutarlarınız hakkında ayrıntılar sağlar. Raporları birçok farklı şekilde görüntüleyebilirsiniz. Örneğin, toplamları veya hareketleri gösterebilir ya da maddelere veya bir zaman aralığına göre filtre uygulayabilirsiniz. Satılan malların maliyeti (SMM) değerlerinin veya süren iş (süren iş) değerlerinin maliyetini görüntüleyebilir ve diğer seçenekleri ayarlayabilirsiniz.

Stok değeri raporları aşağıdaki görevleri gerçekleştirmenize olanak sağlar:

- Genel muhasebe ile stok arasında mutabakat gerçekleştirin.
- Belirli bir döneme ait eldeki stok ve değerlere bakın.
- Belirli bir amaca uyarlanmış rapor konfigürasyonları oluşturun.
- Birden çok kez kullanılabilmeleri için rapor yapılandırmalarını kaydedin.
- Raporu çalıştırdığınızda filtre verilerine aralıklar ekleyin.

## <a name="types-of-inventory-value-report"></a>Stok değer raporu türleri

İki tip stok değeri raporu vardır: **Stok değeri** (Standart rapor) ve **Stok değeri rapor depolaması**.

### <a name="standard-inventory-value-report"></a>Standart Stok değeri raporu

Standart **Stok değeri** raporu, dahil edilen bilgileri seçmenizi ve bu bilgileri ekranda göstermenizi sağlayan basit bir rapordur. Sonuçları kaydetmez. Filtre uygulama, ayrıntıya inme, göz atma veya dışa aktarma için etkileşimli özellikler sağlamaz. Bu nedenlerden dolayı, çoğu durumda bunun yerine **Stok değeri raporu depolama** raporunu kullanmanızı öneririz.

### <a name="inventory-value-report-storage-report"></a>Stok değeri raporu depolama raporu

**Stok değeri raporu depolama** raporu, Microsoft Dynamics 365 Supply Chain Management'ta etkileşimli bir sayfa ya da birkaç biçimden birinde dışa aktarılan belge olarak dijital biçimlerde çıktı sunar.

Raporu tarayıcınızda görüntülediğinizde, sütunlar ve toplam bakiyeler yapılandırdığınız düzene göre dinamik olarak ayarlanır. Sonuçları sıralayabilir, filtreleyebilir ve verilerde detaya inebilir ve daha fazlasını yapabilirsiniz.

Rapor sonuçları **Stok değeri** veri varlığında depolanır. Bu nedenle, sonuçlara filtre uygulayabilir ve sonuçları virgülle ayrılmış değerler (CSV) veya Microsoft Excel biçimi gibi bir biçimde dışa aktarabilirsiniz.

**Stok değeri raporu depolama** raporu, çıktı birçok satır içerdiğinde yararlı olur. Örneğin, 50.000 maddeniz ve ambar olarak oluşturulmuş 300 mağazanız var. Bu durumda, stok sona erme bakiyelerini maddeye, tesise ve ambara göre talep ederseniz çıktı birçok satır içerir.

> [!NOTE]
> **Stok değeri raporu depolama** raporu düzeninde tanımlanan alt toplamları içermez. Ayrıca, rapor düzeninde tanımlansa bile genel muhasebe bakiyelerini de içermez. Genel muhasebe defterine mutabakat mizan kullanılarak yapılmalıdır. Ancak, standart **Stok değeri** raporu bu alt toplamları ve bakiyeleri içerir.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Stok değeri raporu depolama özelliğini açma veya kapatma

Supply Chain Management sürüm 10.0.25 itibariyle, bu özellik varsayılan olarak açıktır. Yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Stok değeri raporu depolama* özelliğini bularak bu işlevi açabilir veya kapatabilir.

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>Stok değeri rapor yapılandırmalarını tanımla

Farklı tipte stok değeri raporuna dahil edilen içeriği ayarlamak için **Stok değeri raporları** sayfasını kullanın. Herhangi bir sayıda rapor türü tanımlayabilirsiniz. Her iki stok değeri raporu oluşturduğunuzda, bir rapor türü seçersiniz.

1. **Maliyet Yönetimi \> Stok muhasebe ilkeleri kurulumu \> Stok değeri raporları**'na gidin.
1. Şu adımlardan birini izleyin:

    - Var olan bir raporu düzenlemek için bunu liste bölmesinden seçin ve sonra Eylem bölmesinden **Düzenle**'yi seçin.
    - Yeni bir rapor oluşturmak için: Eylem Bölmesi'nde **Yeni**'yi seçin.

1. Yeni veya seçili raporun üst bilgisinde aşağıdaki alanları ayarlayın:

    - **Kimlik** - Rapor satırı için kısa bir tanımlayıcı girin. Bu değer, tüm stok değer raporu konfigürasyonlarının içinde benzersiz olmalıdır. Yeni konfigürasyonu kaydettikten sonra düzenlenemez.
    - **Ad**: Rapor için açıklayıcı bir ad girin.

1. Yeni bir rapor konfigürasyonu oluşturuyorsanız, kalan alanları kullanılabilir yapmak için Eylem Bölmesindeki **Kaydet**'i seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Tarih aralığı** – Önceden tanımlanmış bir tarih aralığı seçin. Raporu çalıştırdığınızda, bu tarih aralığını geçersiz kılabilirsiniz.
    - **Aralık** – Kayıtlar rapor için alındığında kullanılması gereken tarih ve saate bağlı olarak, *Deftere nakil tarihini* veya *Hareket Süresini* seçin.
    - **Boyut kümesi** - Verilerin çalışacağı boyut kümesini seçin. (Boyutlar genel muhasebede tanımlanmıştır.) Örneğin, verileri *Ana firma* için veya *Ana Firma + Departman* için kullanabilirsiniz. Seçtiğiniz boyut kümesinin ikiden fazla boyutu olmamalıdır. Daha fazla bilgi için bkz. [Mali boyut kümeleri](../../finance/general-ledger/financial-dimension-sets.md).

1. **Sütunlar** hızlı sekmesinde, aşağıdaki alanları ayarlayın. Bu alanlar, raporunuzun eklediği sütunları ve bu sütunların içerdiği veri türlerini denetler.

    - **Stok** – Stok değerlerini göstermek için bu seçeneği *Evet* olarak ayarlayın. Böylece, bu değerleri genel muhasebe hesabı bakiyeleriyle mutabık kılabilirsiniz.
    - **Süren iş** – Süren iş değerlerini göstermek için bu seçeneği *Evet* olarak ayarlayın. Böylece, bu değerleri genel muhasebe hesabında süren iş hesap bakiyeleriyle mutabık kılabilirsiniz. Bu seçeneği *Evet* olarak ayarladığınızda, rapor yalnızca süren iş durumuna sahip fiziksel miktarları ve tutarları gösterir. Süren iş durumu bulunan üretim emirleri çekildi veya tamamlandı olarak bildirildi, ancak bunlar sonlandırılmadı.
    - **Ertelenen SMM** – Ertelenen SMM için fiziksel miktarları ve stok tutarlarını gösteren bir sütun görüntülemek için bu seçeneği *Evet* olarak ayarlayın. Ertelenen SMM, fiziksel miktarlar ve tutarlar kullanılarak gösterilir, çünkü sevk irsaliyesi miktarlarını ve tutarlarını kaydırır.
    - **SMM** – SMM için mali miktarları ve stok tutarlarını gösteren bir sütun görüntülemek için bu seçeneği *Evet* olarak ayarlayın. SMM, mali miktarlar ve tutarlar kullanılarak gösterilir, çünkü fatura miktarlarını ve tutarlarını kaydırır.
    - **Kar ve zarar** – Stok için kar ve zarar hesaplarına nakledilen mali tutarı gösteren bir sütun görüntülemek için bu seçeneği *Evet* olarak ayarlayın.
    - **Karşılaştırma için birikmeli hesap değerlerini yazdır** – Genel muhasebe hesabı bakiyesini gösteren bir sütun görüntülemek için bu seçeneği *Evet* olarak ayarlayın. Bu şekilde, bilanço bakiyesini kontrol etmek zorunda kalmazsınız. Bu seçenek, **Stok değeri raporu depolama** raporuyla değil yalnızca standart **Stok değer** raporuyla çalışır. Bu seçeneği *Evet* olarak ayarladıktan sonra, etkinleştirdiğiniz **Mali pozisyon** seçeneklerine bağlı olarak, listelemek istediğiniz her genel muhasebe hesabını belirtmek için aşağıdaki alanları kullanmanız gerekir.

        > [!NOTE]
        > Bu alanlardan herhangi biri için bir *toplam* hesabı seçerseniz, hem toplam hesaba dahil edilen her stok hesabının tutarı, hem de toplam hesabının tutarı gösterilir.

        - **Stok hesabı** – Stok bilgilerinin gösterileceği genel muhasebe hesabını belirtin. (Her ikisi **Stok** seçeneği ve **Karşılaştırma için kümülatif hesap değerlerini yazdır** seçeneğinin *Evet* olarak ayarlanmış olması gerekir.)
        - **Süren iş hesabı** – Süren iş bilgilerinin gösterileceği genel muhasebe hesabını belirtin. (Her ikisi **Süren iş** seçeneği ve **Karşılaştırma için kümülatif hesap değerlerini yazdır** seçeneğinin *Evet* olarak ayarlanmış olması gerekir.)
        - **Ertelenmiş SMM hesabı** – Ertelenen SMM bilgilerinin gösterileceği genel muhasebe hesabını belirtin. (Hem **Ertelenen SMM** seçeneği ve **Karşılaştırma için kümülatif hesap değerlerini yazdır** seçeneğinin *Evet* olarak ayarlanmış olması gerekir.)
        - **COGS hesabı** – COGS bilgilerinin gösterileceği genel muhasebe hesabını belirtin. (Her ikisi **COGS** seçeneği ve **Karşılaştırma için kümülatif hesap değerlerini yazdır** seçeneğinin *Evet* olarak ayarlanmış olması gerekir.)

    - **Fiziksel ve mali değerleri özetleme** – Toplam stok miktarını ve stok tutarını (hem fiziksel, hem de mali stok değerlerinin özeti) gösteren bir sütunu görüntülemek için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Hayır* olarak ayarlanırsa rapor hem fiziksel, hem de mali stok değerlerini gösterir.
    - **Genel muhasebeye nakledilmemişleri dahil et** Genel muhasebeye hiçbir zaman nakledilmemiş hareketleri gösteren bir sütun görüntülemek için bu seçeneği *Evet* olarak ayarlayın. Aşağıdaki madde türleri için hareketler genel muhasebeye nakledilemez:

        - İlgili madde modeli grubu için **Fiziksel stoğu deftere naklet** seçeneğinin işareti kaldırıldığında alınmış ancak faturalanmamış maddeler.
        - **Borç hesapları parametreleri** sayfasında **Genel** sekmesinde **Ürün makbuzu** hızlı sekmesinde **Ürün makbuzunu genel muhasbeye naklet** seçeneği (**Borç hesapları \> Kurulum \> Borç hesapları parametreleri**) işareti kaldırıldığında alınmış ancak faturalanmamış maddeler.

    - **Ortalama birim maliyeti hesapla** - Ortalama birim maliyeti gösteren bir sütun görüntülemek için bu seçeneği *Evet* olarak ayarlayın. Ortalama birim maliyeti toplam tutara bölünen toplam miktardır.
    - **Toplam miktar ve değer** – Fiziksel stok (ve mali miktarlar) ve fiziksel stok toplam tutarı (ve mali tutarlar) görüntüleyen sütunları göstermek için bu seçeneği *Evet* olarak ayarlayın. Bu seçeneği yalnızca, **Fiziksel ve mali değerleri özetle** seçeneği *Hayır* olarak ayarlanmışsa *Evet* olarak ayarlayabilirsiniz .
    - **Stok boyutları** - Bu kılavuzda, raporda göstermek istediğiniz her boyut için **Görünüm** onay kutusunu işaretleyin. Yalnızca **Mali stok** seçeneğinin etkinleştirildiği boyutlar rapordaki değerleri gösterir. Diğer boyutlar yalnızca boş sütunları gösterir. Göstermeyi seçtiğiniz boyutlar için toplamları dahil etmek üzere **Toplam** onay kutusunu seçebilirsiniz.
    - **Kaynak Kodu** – Her satırın maddesini tanımlayan bir sütun görüntülemek için **Görünüm** seçeneğini *Evet* olarak ayarlayın. Toplamları dahil etmek için **Toplam** seçeneğini *Evet* olarak ayarlayın. Sütun, her satırda listelenen öğenin türüne bağlı olarak, aşağıdaki bilgi türlerinden birini gösterir:

        - **Malzeme** – Sütun, ilgili malzeme kaydının `ItemID` alan değerini gösterir.
        - **İşçilik** – Sütun, ilgili işçilik kaydının `WorkCenterID` alan değerini gösterir.
        - **Dolaylı maliyet** – Sütun, ilgili maliyet kaydının `CodeID` alan değerini gösterir.

        **Görünüm** seçeneği hem **Kaynak Kodu** alanı hem de **Kaynak Grubu** alanı için *Hayır* olarak ayarlanırsa, yalnızca seçtiğiniz stok boyutlarına dayalı olarak toplam bir stok değeri görürsünüz.

    - **Kaynak Grubu** – Her satırın kaynak grubunu tanımlayan bir sütun görüntülemek için **Görünüm** seçeneğini *Evet* olarak ayarlayın. Toplamları dahil etmek için **Toplam** seçeneğini *Evet* olarak ayarlayın. Sütun, her satırda listelenen öğenin türüne bağlı olarak, aşağıdaki bilgi türlerinden birini gösterir:

        - **Malzeme** – Sütun, ilgili malzeme kaydının `ItemGroup` alan değerini gösterir.
        - **İşçilik** – Sütun, ilgili işçilik kaydının `WorkcenterGroup` alan değerini gösterir.
        - **Dolaylı maliyet** – Sütun, ilgili maliyet kaydının `CostGroup` alan değerini gösterir. (`CostGroupType` değeri *Dolaylı* olmalıdır.)

        **Görünüm** seçeneği hem **Kaynak Kodu** alanı hem de **Kaynak Grubu** alanı için *Hayır* olarak ayarlanırsa, yalnızca seçtiğiniz stok boyutlarına dayalı olarak toplam bir stok değeri görürsünüz.

1. **Satırlar** hızlı sekmesinde, aşağıdaki alanları ayarlayın. Bu alanlar ilgili süren işle ilişkili alt bölümleri rapora eklemenizi veya bunları kaldırmanızı sağlar.

    - **Malzeme** – Malzemelerin bilgilerini göstermek için bu seçeneği *Evet* olarak ayarlayın. *Malzeme*, güvenilir çıkış oluşturmak için malzemelerin tüm rapor konfigürasyonlarına eklenmesi gerektiğinden, varsayılan bir kaynak türüdür.
    - **İşçilik** – Süren işin işçilik maliyetini göstermek için bu seçeneği *Evet* olarak ayarlayın.
    - **Dolaylı maliyet** – Süren işin dolaylı maliyetini göstermek için bu seçeneği *Evet* olarak ayarlayın.
    - **Doğrudan dış kaynak** – Süren işin doğrudan dış kaynak maliyetini göstermek için bu seçeneği *Evet* olarak ayarlayın. Bu bilgiler alt sözleşme için kullanışlıdır.
    - **Ayrıntı Düzeyi** – Rapor için bir görünüm seçeneği belirleyin:

        - *Hareketler* - Rapordaki tüm ilgili hareketleri görüntüleyin. Büyük miktarda hareket içeren raporları görüntülerken performans sorunlarıyla karşılaşabileceğini unutmayın. Bu nedenle, bu görünüm seçeneğini kullanmak istiyorsanız, **Stok değeri raporu depolama** raporunu kullanmanızı öneririz.
        - *Toplamlar* – Toplam sonucu görüntüleyin.

    - **Başlangıç bakiyesini dahil et** – Başlangıç bakiyesini göstermek için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek, yalnızca **Ayrıntı düzeyi** alanı *Hareketler* olarak ayarlandığında kullanılabilir.

## <a name="generate-an-inventory-value-report-storage-report"></a>Stok değeri rapor depolama raporu oluşturma

Bir **Stok değeri rapor depolama** raporu oluşturmak ve depolamak için aşağıdaki adımları izleyin.

1. **Maliyet yönetimi \> Sorgular ve raporlar \> Stok değeri raporu depolama**'ya gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Stok değeri** iletişim kutusunda, **Parametreler** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **Ad**: Rapor için benzersiz bir ad girin.
    - **Kod** – Rapor için kullanılacak [stok değeri rapor konfigürasyonunu](#report-configuration) seçin. Konfigürasyon, raporunuza eklenecek olan sütun ve satırlara ilişkin seçenekleri oluşturur.
    - **Tarih aralığı** – Rapora hangi kayıtların ekleneceğini tanımlamak için bu bölümdeki alanları kullanın. Tarih aralığını tanımlamak için **Tarih aralığı kodu** alanında önceden ayarlanmış bir aralık seçebilirsiniz (rapor oluşturma tarihine göre) veya **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında belirli tarihleri seçebilirsiniz.

1. **Dahil edilecek kayıtlar** hızlı sekmesinde, rapora dahil edilecek verileri tanımlamak için filtreler ve sınırlamalar ayarlayın. Standart sorgu düzenleyicisi iletişim kutusunu açmak için **Filtre**'yi seçin. Burada ölçütü ve birleşimleri tanımlayabileceğiniz standart bir sorgu iletişim kutusu görüntülenir. Alanlar, Supply Chain Management'ta bulunan diğer sorgular için çalıştıkları gibi çalışır. Tüm bu filtreler stok hareketlerine uygulanacak, ancak genel muhasebe bakiyesine uygulanmayacak. Filtrelerinizi ayarlarken bu davranışı aklınızda bulundurun. Aksi durumda, stok ve genel muhasebe arasında bir tutarsızlık görebilirsiniz.
1. **Arka planda çalıştır** hızlı sekmesinde raporun nasıl, ne zaman ve ne sıklıkta oluşturulacağını belirtin. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.

    > [!NOTE]
    > Bu rapor her zaman bir toplu işin parçası olarak çalıştırılır.

1. Ayarlarınızı uygulayıp iletişi kutusunu kapatmak için **Tamam**'ı seçin.

Toplu iş tamamlandıktan sonra rapor **Stok değeri raporu depolama alanı** sayfasında listelenir. Raporu görmek için sayfayı yenilemeniz gerekebilir.

> [!IMPORTANT]
> Seçili stok değeri raporu konfigürasyonunda, hem **Başlangıç tarihi** alanında, hem de **Bitiş tarihi** alanında aynı tarihi seçerseniz ve ayrıca, **Başlangıç bakiyesini dahil et** seçeneğini *Evet* olarak ayarladıysanız, yanlış bir başlangıç bakiyesi elde edebilirsiniz.

## <a name="explore-an-inventory-value-report-storage-report"></a>Stok değeri rapor depolama raporunu keşfetme

Raporu oluşturduktan sonra, istediğiniz zaman aşağıdaki adımları izleyerek görüntüleyebilir ve keşfedebilirsiniz:

1. **Maliyet yönetimi \> Sorgular ve raporlar \> Stok değeri raporu depolama**'ya gidin.
1. Listeden bir rapor seçin. Sayfa, seçili raporu oluşturmak için kullanılan [stok değer raporu konfigürasyonu](#report-configuration) ayrıntılarını gösterir.
1. Eylem Bölmesinde, rapor içeriğini görüntülemek için **Ayrıntıları görüntüle**'yi seçin.
1. Aşağıdaki adımlardan birini izleyerek raporu keşfedin:

    - Tabloları, Supply Chain Management'taki standart formların çoğunda olduğu gibi, o sütundaki değerlere göre sıralamak veya filtrelemek için neredeyse her sütun başlığını seçebilirsiniz.
    - Raporu kullanılabilir sütunlardan herhangi birinde herhangi bir değere göre filtrelemek için **Filtre** alanını kullanın.
    - Sıralama ve filtreleme seçeneklerinin sık kullanılan birleşimlerini kaydetmek ve yüklemek için görünüm menüsünü (**Filtre** alanının üzerinde) kullanın.

## <a name="export-an-inventory-value-report-storage-report"></a>Stok değeri rapor depolama raporunu dışa aktarma

Oluşturduğunuz her rapor **Stok değeri** veri varlığında depolanır. Bu varlıktaki verileri CSV veya Excel gibi desteklenen herhangi bir veri biçiminde dışa aktarmak için Supply Chain Management'ın standart veri yönetimi özelliklerini kullanabilirsiniz.

Aşağıdaki örnekte **Stok değeri raporu depolama** raporunun nasıl dışa aktarılacağı gösterilir.

1. **Sistem Yönetimi \> Çalışma alanları \> Veri yönetimi** seçeneğine gidin.
1. **İçe/dışa aktar** bölümünde **Dışa aktar** kutucuğunu seçin.
1. Görüntülenen **Dışa aktar** sayfasında dışa aktarma işini ayarlarsınız. Öncelikle iş için bir grup adı girin.
1. **Seçili varlıklar** bölümünde, **Varlık ekle**'yi seçin.
1. Görüntülenen iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Varlık adı** - *Stok değeri*'ni seçin.
    - **Hedef veri biçimi** – Verilerin dışa aktarılacağı biçimi seçin.

1. Yeni satırı eklemek için **Ekle**'yi, iletişim kutusunu kapatmak için ise **Kapat**'ı seçin.
1. Genellikle bir seferde tek bir rapor dışa aktarabilirsiniz. Tek bir raporu dışa aktarmak için, **Sorgu** iletişim kutusuna yeni eklediğiniz satır için bir filtre ayarlayın. Bu şekilde, **Stok değeri** varlığındaki hangi raporun dışa aktarma işlemine dahil edileceğini tanımlayabilirsiniz. Tek bir raporu dışa aktarmak için aşağıdaki filtre seçeneklerini ayarlamak üzere bu adımları izleyin:

    1. **Aralık** sekmesinde, satır eklemek için **Ekle**'yi seçin.
    2. **Tablo** alanını *Stok değeri* olarak ayarlayın.
    3. **Türetilen tablo** alanını *Stok değeri* olarak ayarlayın.
    4. **Alan** alanını filtrelemek istediğiniz alan olarak ayarlayın. Genellikle, **Yürütme adı** alanını ve/veya **Yürütme zamanı** alanını kullanırsınız.
    5. **Ölçüt** alanını, seçili alanda aramak istediğiniz değere ayarlayın. (Önceki adımda **Yürütme adı** alanını seçtiyseniz, bu değer raporun adı olacaktır. **Yürütme zamanı** alanını seçtiyseniz, raporun oluşturulduğu saat olacaktır.)
    6. Gerekirse aradığınız raporu benzersiz olarak tanımlayıncaya kadar **Aralık** sekmesine daha fazla satır ekleyin.

1. Ayarlarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Dışa aktarma ayarınızı kaydetmek için **Kaydet**'i seçin.
1. **Dışa aktarma seçenekleri** sekmesinde dışa aktarma dosyasını oluşturmak için **Şimdi dışa aktar**'ı seçin.
1. Görüntülenen **Yürütme özeti** sayfasında dışa aktarma işinizin durumunu ve dışa aktarılan varlıkların listesini görebilirsiniz. **Varlık işleme durumu** bölümünde,  listeden **Stok değeri** varlığını seçin ve ardından söz konusu varlıktan dışa aktarılan verileri indirmek için **Dosyayı indir**'i seçin.

Veri yönetimini kullanarak verileri dışa aktarma hakkında daha fazla bilgi için bkz. [Veri içe ve dışa aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="generate-a-standard-inventory-value-report"></a>Standart Stok değeri raporu oluşturma

Aşağıdaki yordamı kullanarak standart **Stok değeri** raporu oluşturun.

1. **Maliyet yönetimi \> Sorgular ve raporlar \> Stok muhasebsesi - durum raporları \> Stok değeri**'ne gidin.
1. **Stok değeri raporu** iletişim kutusunda, **Parametreler** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **Ad**: Rapor için benzersiz bir ad girin.
    - **Kod** – Rapor için kullanılacak [stok değeri rapor konfigürasyonunu](#report-configuration) seçin. Konfigürasyon, raporunuza eklenecek olan sütun ve satırlara ilişkin seçenekleri oluşturur.
    - **Tarih aralığı** – Rapora hangi kayıtların ekleneceğini tanımlamak için bu bölümdeki alanları kullanın. Tarih aralığını tanımlamak için **Tarih aralığı kodu** alanında önceden ayarlanmış bir aralık seçebilirsiniz (rapor oluşturma tarihine göre) veya **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında belirli tarihleri seçebilirsiniz.

1. **Dahil edilecek kayıtlar** hızlı sekmesinde, rapora dahil edilecek verileri tanımlamak için filtreler ve sınırlamalar ayarlayın. Standart sorgu düzenleyicisi iletişim kutusunu açmak için **Filtre**'yi seçin. Burada ölçütü ve birleşimleri tanımlayabileceğiniz standart bir sorgu iletişim kutusu görüntülenir. Alanlar, Supply Chain Management'ta bulunan diğer sorgular için çalıştıkları gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinde raporun nasıl, ne zaman ve ne sıklıkta oluşturulacağını belirtin. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. Ayarlarınızı uygulayıp iletişi kutusunu kapatmak için **Tamam**'ı seçin. Rapor görüntülenir.

## <a name="reading-inventory-value-reports"></a>Stok değer raporlarını okuma

Bu bölümde, stok değeri raporunun nasıl okunacağı ve anlaşılması hakkında bir rehberlik sunulmaktadır.

Supply Chain Management, stok durumuyla ilgili aşağıdaki iki önemli kavramı destekler:

- **Mali olarak güncelleştirildi** – Bu kavram, stok hareketlerinin zaten faturalanmış olduğunu gösterir. Üretim emirleri söz konusu olduğunda, bir üretim emrinin sonunu gösterir.
- **Fiziksel olarak güncelleştirilen** – Bu kavram stok hareketlerinin henüz faturalanmadığını, ancak teslim alındığını veya sevk edildiğini gösterir. Üretim emirleri için, malzemenin çekildiği veya üretim emrinin tamamlandı olarak rapor edildiğini gösterir.

Bu iki kavramı anladığınızda, rapor çıktısında aşağıdaki sütunların anlaşılması kolay olmalıdır:

- **Stok: Mali Miktar** - Mali olarak güncelleştirilmiş miktarın stok değeri.
- **Stok: Mali Tutar** - Mali olarak güncelleştirilmiş stok değeri tutarı.
- **Stok: Nakledilen Fiziksel Miktar** - Fiziksel olarak güncelleştirilmiş miktarın stok değeri.
- **Stok: Nakledilen Fiziksel Tutar** - Fiziksel olarak güncelleştirilmiş stok değeri tutarı.
- **Stok: Nakledilmemiş Fiziksel Miktar** – Stok hareketleri içeren, ancak genel muhasebeye nakledilmeyen miktar. Örneğin, **Fiziksel stokları deftere naklet** ve **Mali stoğu deftere naklet** seçeneklerinin işaretinin kaldırıldığı bir madde model grubunuz varsa ve bu gruba bağlı bir maddeniz varsa. Daha sonra bir satınalma siparişi oluşturur, alır ve faturalandırırsınız. Bu aşamada, madde için stok değeri raporunu gözden geçirmeniz durumunda, satınalma siparişindeki miktarın ve değerin, **Stok: Nakledilmemiş Fiziksel Miktar** ve **Stok: Nakledilmemiş Fiziksel Tutar** sütunlarında gösterildiğini görürsünüz.
- **Stok: Nakledilmemiş Fiziksel Tutar** – Raporlarınızı, deftere nakledilmeyen tutarları görüntüleyecek şekilde ayarlayabilirsiniz. Ancak, raporu stok mutabakatı için kullanıyorsanız bu değeri kullanmayın. Aksi durumda, tutar genel muhasebeye nakledilemez.
- **Stok: Miktar** - Rapordaki tüm miktar sütunlarının toplam miktarı.
- **Stok: Tutar** - Rapordaki tüm miktar sütunlarının toplam tutarı. Stok mutabakatı gerçekleştirdiğinizde, raporunuzda **Stok: Nakledilmemiş Fiziksel Tutar** sütunu bulunuyorsa bu sütunu kullanmayın. Bu durumda, toplam tutardan **Stok: Nakledilmemiş Fiziksel Tutar** tutarını hariç tutmanız gerekir.
- **Ortalama birim maliyeti** - Toplam miktara bölünen toplam tutardır.

Genellikle stok değerini ve miktarını görüntülemek için bir stok değeri raporu kullanırsınız. Ancak, bazen rapor ilgili tüm stok boyutlarını göstermez. Beklediğiniz boyutları göremiyorsanız, aşağıdaki ayarları doğrulayın:

- Madde depolama ve izleme gruplarını inceleyin. Yalnızca **Mali stok** seçeneğinin etkinleştirildiği boyutlar rapordaki değerleri gösterebilir.
- **Maliyet yönetimi \> Stok muhasebesi ilkeleri kurulumu \> Stok değer raporları**'na gidin, raporu oluşturmak için kullandığınız rapor konfigürasyonunu seçin ve **Görüntüle** sütununda gerekli stok boyutlarının seçildiğinden emin olun.

Örneğin, madde numarası *A0001* olan bir madde vardır. Depolama boyutları grubunda, yalnızca tesis mali stok için etkindir. Tesis ve ambarın her ikisi de fiziksel stok için etkinleştirilir. İzleme boyutu grubunda, toplu iş numarası fiziksel stok için etkinleştirilir, ancak mali stok için etkinleştirilmedi. Böylece, tesis, ambar ve toplu iş numarasının tümünün seçildiği bir rapor konfigürasyonu kullanılır. Raporu görüntülediğinizde, yalnızca tesis için bir değer görürsünüz. Ambar ve toplu iş numarasına ait sütunlar boş. Bu örnekte görüldüğü gibi, stok değeri raporları yalnızca mali stok için etkinleştirilen stok boyutunu gösterebilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

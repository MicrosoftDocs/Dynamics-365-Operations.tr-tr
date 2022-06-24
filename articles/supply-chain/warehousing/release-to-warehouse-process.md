---
title: Ambara serbest bırakma
description: Bu makalede, ambara serbest bırakma işlemi hakkında ayrıntılı bilgi sağlanmaktadır. Burada, ambara sipariş serbest bıraktığınızda oluşturulan varlıklar ve işlemi başlatmak için kullanabileceğiniz seçenekler tanımlanmaktadır.
author: Mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: c3280b2e39d7af5ca99cad703cad6ecc7b307bff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893192"
---
# <a name="release-to-warehouse"></a>Ambara serbest bırakma

[!include [banner](../../includes/banner.md)]

Bu makalede, ambara serbest bırakma işlemi hakkında ayrıntılı bilgi sağlanmaktadır. Burada, ambara sipariş serbest bıraktığınızda oluşturulan varlıklar ve işlemi başlatmak için kullanabileceğiniz seçenekler tanımlanmaktadır.

## <a name="release-to-warehouse-overview"></a>Ambara serbest bırakmaya genel bakış

Ambara serbest bırakma, gönderme işlemleri için stoku hazır hale getirme işlemidir. Ambara sipariş serbest bıraktığınızda sistem, yük satırları ve sevkiyatlar oluşturur. Otomatik dalga işleme ayarlanırsa yükler ve gerekli işler de oluşturulur. Dahil edilen varlıkların yapılandırması, sistem ayarlarına bağlıdır. Makalenin bu bölümünde, ambara serbest bırakma işlemi sırasında oluşturulan varlıklar ve bunları tanımlayan sistem ayarları incelenmektedir.

*Sevkiyat*, aynı müşteri veya aynı teslimat adresi için bir grup satış siparişi veya transfer emri satırıdır.

*Yük*, birlikte gruplanan ve genellikle tek bir kamyon, vagon veya diğer taşıma modu ile gönderilen bir grup satış siparişi ya da transfer emri satırıdır. Yükte bir veya birden fazla sevkiyat olabilir. Yeni bir yüke sipariş satırları ekleyerek el ile yük oluşturabilirsiniz. Bu durumda sipariş satırları, ambara serbest bırakma işlemi başlatılmadan önce yüke atanır ve yalnızca **Yük planlama workbench'i** sayfasından serbest bırakılabilir.

Ambar *işi* bir ambar çalışanı tarafından gerçekleştirilen ambar operasyonlarıdır. Genellikle ambar işi operasyonları en az iki ardışık eylemden oluşur: Bir ambar çalışanı eldeki stoku bir konumdan çeker ve ardından bunu başka bir konuma koyar.

Siparişler ambara serbest bırakıldığında sistem, *yük satırları* oluşturur ve bunları sevkiyatlarda gruplar. Sevkiyat konsolidasyonu işlemi, ambara serbest bırakma işlemi sırasında otomatik sevkiyat konsolidasyonuna olanak tanır. Daha fazla bilgi için bkz. [Sevkiyat konsolidasyonu ilkeleri](about-shipment-consolidation-policies.md).

Sistem, sevkiyat için çekme işi ve yükler oluşturmak üzere *dalgaları* kullanır. *Dalga şablonu*, oluşturmak istediğiniz dalganın türü ve sipariş satırının ambarı için kullanılabilir olmalıdır. *Sevkiyat* türünün dalga şablonları, satış siparişleri ve transfer emirleri için maddeleri sevk etmek üzere kullanılır.

Her dalga şablonu, *dalga yöntemleri* içerir. Dalga yöntemleri, dalga için iş oluşturma veya yük oluşturma gibi eylemler gerçekleştirir. Örneğin, sevkiyat dalgasının dalga şablonu, yük oluşturma, dalgalara satır tahsis etme, stok yenileme ve dalga için malzeme çekme işi oluşturma yöntemleri içerebilir. Dalga şablonu, hangi adımların elle hangi adımların otomatik olarak gerçekleştirilmesi gerektiğine dair, dalganın nasıl oluşturulacağını ve işleneceğini tanımlayan ayarlar oluşturur. Daha fazla bilgi için bkz. [Dalga şablonları](wave-templates.md). Bu nedenle, dalga şablonunuzun yapılandırmasına bağlı olarak ambara sipariş serbest bıraktığınızda otomatik olarak bir dalga oluşturulur, işlenir ve serbest bırakılır veya bu eylemlerden bazıları ya da tümü, ambara serbest bırakma işlemi tamamlandıktan sonra el ile gerçekleştirilir.

Dalga işlendiğinde sistem, uygun bir *iş şablonu* ve *konum yönergesine* bağlı olarak çekme işi oluşturur ve bunu mobil cihazlarda kullanılabilir hale getirir. İş şablonu, her ambar işlemi için işin nasıl gerçekleşeceğini tanımlar ve konum yönergesi, stok hareketi için çekme ve yerine koyma konumlarını belirtir. Daha fazla bilgi için bkz. [İş şablonları ve yerleşim yönergeleri kullanarak ambar işini denetleme](control-warehouse-location-directives.md).

> [!NOTE]
> Varsayılan olarak, dalgalar toplu iş modunda işlenir.

Dalga işleme sırasında, sistem genellikle, yükleme atanmamış her sevkiyat için yeni bir yük oluşturur. Bunun yerine sistemin mevcut yüklere atanmamış sevkiyatlar atamasını isterseniz gelişmiş dalga yükü oluşturma işlevini kullanabilirsiniz. Daha fazla bilgi için bkz. [Dalga sırasında gelişmiş yük oluşturma](advanced-load-building-during-wave.md).

**Satış siparişleri** ve **Transfer emirleri** sayfalarında, ambara serbest bırakma işlemi sırasında satış siparişleri için oluşturulan varlıkları inceleyebilirsiniz.

- **Satış siparişleri** sayfası:

    - **Satış siparişi satırları** hızlı sekmesinde, **Ambar**'ı seçin ve ardından menüde, ilgili sevkiyatları açmak için **Sevkiyat ayrıntıları** seçeneğini, ilgili yükleri açmak için **Yük ayrıntıları** seçeneğini veya ilgili iş ayrıntılarını açmak için **İş ayrıntıları** seçeneğini belirleyin.
    - **Satır ayrıntıları** hızlı sekmesinde, ilgili yükleri incelemek için **Yük** sekmesini seçin.

- **Transfer emirleri** sayfası:

    - Eylem Bölmesi'nde, **Sevk** sekmesinde, ilgili sevkiyatları açmak için **Sevkiyat ayrıntıları**'nı veya ilgili yükleri açmak için **Yük ayrıntıları**'nı seçin.
    - **Transfer emri satırları** hızlı sekmesinde, ilgili iş ayrıntılarını açmak için **İş ayrıntıları**'nı seçin.

Sonuç olarak, ambara bir sipariş serbest bırakıldığında en otomatik akış aşağıdaki şekilde çalışır:

1. Sistem, sipariş için bir sevkiyat ve bir dalga oluşturur.
1. Dalga işlenir.
1. Sistem bir yük ve bir iş kodu oluşturur.

Dalga şablonları, iş şablonları ve konum yönergeleri ayarlarına bağlı olarak, bu akıştaki bazı adımlar el ile yapılabilir. Ancak genel akış aynı kalır.

Ambara sipariş serbest bırakma işlemi için birkaç seçeneğiniz vardır. İşlemi el ile gerçekleştirebilir veya bir toplu iş ayarlayabilirsiniz. Bu makalenin geri kalan bölümlerinde, ambara serbest bırakma operasyonu gerçekleştirebileceğiniz çeşitli yollar ayrıntılı olarak incelenmektedir.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Satış siparişleri ve Transfer emirleri sayfalarından ambara el ile serbest bırakma

**Satış siparişleri** sayfası veya **Transfer emirleri** sayfasından, **Ambara serbest bırak** seçeneğini belirleyerek siparişi ambara serbest bırakabilirsiniz.

- **Satış siparişleri** sayfasında düğme, Eylem Bölmesi'nin **Ambar** sekmesindedir.
- **Transfer emirleri** sayfasında düğme, Eylem Bölmesi'nin **Sevk** sekmesindedir.

**Satış siparişleri** sayfasından, eş zamanlı olarak birkaç satış siparişini serbest bırakabilirsiniz.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Ambara serbest bırakma sayfalarından ambara el ile serbest bırakma

Sistem şu anda birden çok sipariş için satırları inceleyebileceğiniz ve bunları ambara serbest bırakabileceğiniz üç sayfa sağlamaktadır:

- **Ambara serbest bırak** (**Ambar yönetimi \> Ambara serbest bırak \> Ambara serbest bırak**): Bu sayfa hem satış siparişleri hem de transfer emirleri ile çalışmanıza olanak tanır. Ancak bu, diğer iki sayfadan daha yavaş performans sağlar. Bu sayfa yakında kullanım dışı bırakılacaktır.
- **Satış siparişlerini ambara serbest bırak** (**Ambar yönetimi \> Ambara serbest bırak \> Satış siparişlerini ambara serbest bırak**): Bu sayfa yalnızca satış siparişleri ile çalışmanıza olanak tanır. Ancak bu, **Ambara serbest bırak** sayfasından daha iyi performans sağlar.
- **Transfer emirlerini ambara serbest bırak** (**Ambar yönetimi \> Ambara serbest bırak \> Transfer emirlerini ambara serbest bırak**): Bu sayfa yalnızca transfer emirleri ile çalışmanıza olanak tanır. Ancak bu, **Ambara serbest bırak** sayfasından daha iyi performans sağlar.

Üç sayfa da bu bölümün geri kalanında anlatıldığı gibi benzer işlevler sağlar. Sayfaların tümü, sipariş satırlarını veya tüm siparişleri seçmenize ve ardından bunları ambara serbest bırakmanıza olanak tanır.

Her sayfa, sipariş satırlarını seçebileceğiniz bir üst bölümden ve ambara serbest bırakma işlemini başlatabileceğiniz bir alt bölümden oluşur. Serbest bırakmak istediğiniz satış siparişi satırlarını aramak için üst bölümdeki filtreleri kullanabilirsiniz. **Ambara serbest bırak** sayfası, üst bölümde satış siparişleri ve transfer emirleri için ayrı bir sekme sağlar ve burada diğer iki sayfada yalnızca bir sipariş türü gösterilir.

Üst bölümdeki araç çubuğunda, ambara serbest bırakmak için sipariş satırlarını seçmek üzere kullanabileceğiniz aşağıdaki düğmeler bulunur:

- **Ekle**: Üst bölümde bir veya birden fazla sipariş satırı seçin ve ardından alt bölümde bu satırlar için bu düğmeyi belirleyin.
- **Tümünü ekle**: Tüm satırları üst bölümden alt bölüme ekleyin.
- **Sipariş ekle**: Sipariş seçin ve ardından tüm satırları bu siparişten alt bölüme eklemek için bu düğmeyi belirleyin.

Alt bölüme satır eklemeyi tamamladıktan sonra serbest bırakmak istediğiniz her satırı işaretleyin. Ardından bu satırları ambara serbest bırakmak için araç çubuğunda **Ambara serbest bırak**'ı seçin.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Yük planlama workbench'i sayfasından ambara el ile serbest bırakma

Ayrıca **Yük planlama workbench'i** sayfasını kullanarak siparişleri ambara el ile serbest bırakabilirsiniz. Bu sayfa, sipariş satırlarını yüklere göre düzenlemenize ve ardından bu yükleri ambara serbest bırakmanıza olanak tanır.

**Yük planlama workbench'i** sayfasını açmak için **Ambar yönetimi \> Yükler**'e gidin. Ayrıca bunu **Satış siparişleri** ve **Transfer emirleri** sayfalarından da açabilirsiniz. Sayfanın üst bölümünde, **Satış siparişleri** sekmesinde satış siparişi satırlarını ve **Transfer emirleri** sekmesinde transfer emri satırlarını seçebilir ve ardından bu satırları yeni veya mevcut bir yüke ekleyebilirsiniz.

Eylem Bölmesi'nde **Arz ve talep** sekmesi, üst bölümdeki sipariş satırlarını bir yüke eklemek için kullanabileceğiniz aşağıdaki düğmeleri içerir:

- **Yeni yüke**: Üst bölümde bir veya birden fazla sipariş satırı seçin ve ardından yeni yük oluşturup bu satırları yeni yüke eklemek için bu düğmeyi belirleyin.
- **Mevcut yüke**: Üst bölümde bir veya birden fazla sipariş satırı seçin ve ardından bu satırları mevcut yüke eklemek için bu düğmeyi belirleyin.
- **Yeni yüke tüm sipariş**: Siparişleri seçin ve ardından yeni yük oluşturup bu siparişlerdeki tüm satırları yeni yüke eklemek için bu düğmeyi belirleyin.
- **Mevcut yüke tüm sipariş**: Sipariş seçin ve ardından bu siparişteki tüm satırları mevcut yüke eklemek için bu düğmeyi belirleyin.

Alt bölümde, oluşturulan yükleri gözden geçirebilirsiniz. Ambara serbest bırakmak için yükleri seçin ve ardından araç çubuğunda **Serbest bırak \> Ambara serbest bırak** seçeneğini belirleyin. Otomatik dalga işlemeyi kullanıyorsanız yükler zaten sipariş satırlarına atandığından sistem, ambara serbest bırakma işlemi gerçekleştirildiğinde sevkiyatlar ve iş kodları oluşturur.

## <a name="automatic-release-to-the-warehouse"></a>Ambara otomatik serbest bırakma

Siparişleri ambara otomatik olarak serbest bırakmak için **Satış siparişlerini otomatik serbest bırakma** ve **Transfer emirlerini otomatik serbest bırakma** işlerini kullanın.

Satış siparişlerini serbest bırakan toplu işi ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Ambara serbest bırakma \> Satış siparişlerini otomatik serbest bırakma** seçeneğine gidin.
1. **Satış siparişlerini otomatik serbest bırakma** iletişim kutusunda, **Parametreler** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **Serbest bırakılacak miktar**: Ambara serbest bırakılması gereken miktar için tüm miktarı veya yalnızca fiziksel olarak rezerve edilmiş miktarı seçin.
    - **Kısmi serbest bırakılmış siparişlerin serbest bırakılmasına izin ver**: Kısmi serbest bırakılmış siparişler için kalan miktarların ambara serbest bırakılması gerekip gerekmediğini belirtin.
    - **Serbest bırakma hatasında rezervasyonları koru**: Satış siparişi için otomatik olarak rezerve edilmiş miktarların, ambara serbest bırakma işlemi başarısız olursa rezerve edilmiş kalması gerekip gerekmediğini belirtin.
    - **Müşteriye göre grup serbest bırakmaları** – Sistemin, her müşteri için ambara gönderme operasyonlarını ayrı olarak mı işleyeceğini yoksa tüm satış siparişlerini aynı anda mı göndereceğini belirtin. Bu seçenek *Evet* olarak belirlendiğinde, sistem seçilen bir müşteriyle ilgili tüm satış siparişi satırlarını toplar, bu siparişleri ambara gönderir ve sonraki müşteriyi işler. Bu seçenek *Hayır* olarak ayarlandığında, sistem tüm kullanılabilir satış siparişi satırlarını tek bir ambara gönderme operasyonu ile yayımlar. Bu seçeneğin etkinleştirilmesi, performansı ve ambara gönderme işleminin esnekliğini yükseltir. Ancak bu birleşim, her biri yalnızca o müşteri için oluşturulmuş iş olan birçok müşteri dalgasını oluşturacağından, bu seçeneği ambara gönderme sırasında işle olarak yapılandırılan dalga şablonları ile birlikte kullanırken dikkatli olmanız gerekir. Birden fazla müşterinin sevkiyatlarını birleştiren bir iş oluşturmak istiyorsanız *Müşteriye göre grup halinde gönderme* seçeneğini kapatmanız veya dalga şablonlarınızı ertelenmiş işlemeyi kullanacak şekilde yapılandırmanız gerekir.
    - **Kilitli sipariş işleme**: Sistemin, diğer kullanıcılar veya işlemler tarafından düzenlendiğinden şu anda kilitli olan satış siparişlerini nasıl işlemesi gerektiğini seçin:

        - *Siparişlerin kilidinin açılmasını bekle*: Sistemin, ambara serbest bırakmadan önce siparişlerin kilidinin açılmasını beklemesi gerekir. Bu durumda, ambara serbest bırakma işlemi daha uzun sürebilir.
        - *Kilitli siparişleri atla*: Sistemin, kilitli siparişleri atlaması gerekir.

    - **Geçerli sipariş türleri**: Toplu işe dahil edilecek satış siparişi türlerini seçin.
    - **Kredi limiti türü**: Kredi limiti denetimlerinin ambara serbest bırakma işlemi sırasında yapılması gerekip gerekmediğini ve gerekiyorsa eklenecek hareket bilgilerini seçin.

1. İşlenmesi gereken siparişleri denetlemek için **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin. Seçim ölçütünü, sıralama ölçütlerini ve birleşimleri tanımlayabileceğiniz standart bir sorgu iletişim kutusu görüntülenir. Alanlar, Microsoft Dynamics 365 Supply Chain Management'taki diğer sorgu türleri için çalıştıkları gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinde, işi toplu iş modunda çalıştırmanın ve/veya yinelenen bir zamanlama ayarlamanın gerekip gerekmediğini seçin. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. Ayarlarınızı uygulamak ve ambara serbest bırakma işlemini başlatmak için **Tamam**'ı seçin.

Transfer emirlerini serbest bırakan toplu işi ayarlamak için adımları izleyin.

1. **Ambar yönetimi \> Ambara serbest bırakma \> Transfer emirlerini otomatik serbest bırakma** seçeneğine gidin.
1. **Transfer emirlerini otomatik serbest bırakma** iletişim kutusunda, **Parametreler** hızlı sekmesinde aşağıdaki alanları ayarlayın:

    - **Serbest bırakılacak miktar**: Ambara serbest bırakılması gereken miktar için tüm miktarı veya yalnızca fiziksel olarak rezerve edilmiş miktarı seçin.
    - **Kısmi serbest bırakılmış siparişlerin serbest bırakılmasına izin ver**: Kısmi serbest bırakılmış siparişler için kalan miktarların ambara serbest bırakılması gerekip gerekmediğini belirtin.
    - **Serbest bırakmaları hedef ambara göre gruplandır**: Sistemin, tüm transfer emirlerini aynı anda serbest bırakması veya serbest bırakmaları hedef ambara göre gruplandırıp ardından her grubu ambara ayrı ayrı serbest bırakması gerekip gerekmediğini belirtin.

1. İşlenmesi gereken siparişleri denetlemek için **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin. Seçim ölçütünü, sıralama ölçütlerini ve birleşimleri tanımlayabileceğiniz standart bir sorgu iletişim kutusu görüntülenir. Alanlar, Supply Chain Management'ta bulunan diğer sorgular için çalıştıkları gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinde, işi toplu iş modunda çalıştırmanın ve/veya yineleme için zamanlama ayarlamanın gerekip gerekmediğini seçin. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. Ayarlarınızı uygulamak ve ambara serbest bırakma işlemini başlatmak için **Tamam**'ı seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

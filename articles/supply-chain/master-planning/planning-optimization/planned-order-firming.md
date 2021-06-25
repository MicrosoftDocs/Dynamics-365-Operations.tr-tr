---
title: Kesinleşmiş planlı siparişler
description: Bu konu, planlı siparişlerin nasıl kesinleştirileceğini açıklar. Planlı siparişler kesinleştirildiğinde, gerçek satınalma siparişlerine, transfer emirlerine veya üretim emirlerine dönüştürülür.
author: ChristianRytt
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e2fc40e3e9874d47dd51e773628ba1ce75b8ebab
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193893"
---
# <a name="firm-planned-orders"></a>Kesinleşmiş planlı siparişler

[!include [banner](../../includes/banner.md)]

Planlı siparişlerin, master planlama sürecinin bir parçası olarak *kesinleştirilmesi* (yani serbest bırakılması) gerekir. Planlı siparişler kesinleştirildiğinde, gerçek satınalma siparişlerine, transfer emirlerine veya üretim emirlerine dönüştürülür. Bu siparişler *serbest bırakılmış siparişler* veya *açık siparişler* olarak da bilinirler.

Planlı siparişleri kesinleştirmek için üç yöntem vardır:

- **El ile kesinleştirme** – Bir listede belirli planlı siparişleri seçin ve işlemi el ile başlatın.
- **Otomatik kesinleştirme** – Kapsama grupları, bağımsız maddeler ve madde birleşimleri ile master plan birleşimleri için varsayılan kesinleştirme zaman dilimini tanımlayın. Daha sonra, master planlama çalışırken sipariş tarihi kesinleştirme için belirtilen zaman dilimi dahilinde olduğunda planlı siparişler otomatik olarak kesinleştirilecektir.
- **Sorgu tabanlı kesinleştirme** – Planlı siparişleri, özelliklerine göre seçmek için bir sorgu tanımlayın. Sorguyu çalıştırmak ve belirli siparişleri düzenli bir planla kesinleştirmek için bir toplu iş ayarlayabilirsiniz.

Bu konuda her yöntem ayrıntılı olarak açıklanmaktadır.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Bu konuda açıklanan özellikleri etkinleştirin

Çoğu planlı sipariş özelliği Microsoft Dynamics 365 Supply Chain Management'ın Planlama Optimizasyonunu kullanan tüm standart yüklemelerinde kullanılabilir. Ancak, bu konuda açıklanan özelliklerden bazılarını kullanabilmeniz için önce bunların Özellik yönetiminde etkinleştirilmesi gerekir.

### <a name="enable-parallelized-firming-of-planned-orders"></a>Planlı siparişler için paralel kesinleştirmeyi etkinleştirme

Paralel kesinleştirme, birden fazla iş parçacığı arasında paralel olarak çalışarak kesinleştirme işlemini hızlandırır. Bu yaklaşım, birçok plan kesinleştirilirken yararlı olabilir.

Bu işlevi sisteminizde kullanmak için, [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Planlı siparişlerin paralel kesinleştirmesi* özelliğini etkinleştirin.

### <a name="enable-planned-order-firming-with-filtering"></a>Filtre ile planlı sipariş kesinleştirmesini etkinleştirme

Süzme ile yapılan planlı sipariş kesinleştirilmesi, hangi Planlı siparişlerin kesinleştirilmesi gerektiğini belirlemek için mantıksal ölçütler tanımlamanıza olanak sağlar. Ayrıca, hangi planlı siparişlerin seçildiği önizleyebilir, işlemi arka planda çalıştırabilir ve/veya bir toplu iş olarak zamanlayabilirsiniz.

Bu işlevi sisteminizde kullanmak için, [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Filtrelemeyle planlı sipariş kesinleştirmesi* özelliğini etkinleştirin.

### <a name="enable-auto-firming-for-planning-optimization"></a>Planlama Optimizasyonu için otomatik kesinleştirmeyi etkinleştirme

Otomatik kesinleştirme, kesinleştirme zaman dilimi sırasında planlı siparişleri master planlama işleminin parçası olarak kesinleştirmenize olanak tanır. Otomatik kesinleştirme, Supply Chain Management'ta dahili olarak yer alan planlama altyapısında her zaman desteklenir. Ancak, bunu Planlama Optimizasyonuyla birlikte kullanmak için özelliği etkinleştirmelisiniz.

Bu işlevi sisteminizde kullanmak için, [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Planlama Optimizasyonu için otomatik kesinleştirme* özelliğini etkinleştirin.

## <a name="manually-firm-planned-orders"></a>Planlı siparişleri el ile kesinleştirme

Planlı siparişleri el ile kesinleştirmek için, kesinleştirmek istediğiniz planlı siparişleri bulup seçin ve kesinleştirme işlemini el ile başlatın.

1. [Herhangi bir planlı siparişler listesi sayfasını açın](approved-planned-order.md#view-planned-orders).
1. Aradığınız planlı siparişleri bulabilmeniz için listeyi filtrelemek ve sıralamak üzere **Filtre** alanını, **Plan** alanını ve sütun başlıklarını kullanın.
1. Kesinleştirmek istediğiniz her planlı sipariş için onay kutusunu işaretleyin. Sayfada listelenen tüm planlı siparişleri (uyguladığınız filtrelere göre) kesinleştirmek istiyorsanız, bu adımı atlayın.
1. Eylem bölmesinde aşağıdaki düğmelerden birini seçin:

    - **Kesinleştir** – Yalnızca seçili planlı siparişleri kesinleştirin.
    - **Tümünü kesinleştir** – Seçili onay kutularından bağımsız olarak, sayfada o sırada listelenen tüm planlı siparişleri (uyguladığınız filtrelere göre) kesinleştirin. Çok sayıda planlı siparişi kesinleştirmek istiyorsanız bu seçenek yararlı olabilir.

1. **Kesinleştirme** iletişim kutusunda, **Parametreler** hızlı sekmesinde aşağıdaki alanları ayarlayın. (Bu alanların çoğu varsayılan değerlerini **Master planlama parametreleri** sayfasındaki **Standart güncelleştirme** sekmesinden alır.)

    - **İşaretlemeyi güncelleştir** – Planlı siparişler kesinleştirilirken kullanılacak stok işaretleme ilkesini seçin.
    - **Bir hata oluşursa kesinleştirmeyi durdur** – Birinde hata oluşursa seçili tüm planlı siparişlerin kesinleştirilmesinin durdurulması için bu seçeneği *Evet* olarak ayarlayın. **Paralel kesinleştirme** seçeneği *Evet* olarak ayarlandığında bu seçenek *Hayır* olarak ayarlanmalıdır.
    - **Paralel kesinleştirme** – Bu seçenek yalnızca sisteminizde [*Planlı siparişlerin paralel kesinleştirilmesi*](#enable-features) özelliği etkinse ve kesinleştirme için iki veya daha fazla planlı sipariş seçtiyseniz kullanılabilir. Kesinleştirme işlemlerini paralel çalıştırmak için *Evet* olarak ayarlayın. Paralel kesinleştirme, performansı artırmaya yardımcı olabilir.
    - **İş parçacığı sayısı**– Bu seçenek yalnızca sisteminizde [*Planlı siparişlerin paralel kesinleştirilmesi* özelliği](#enable-features) etkinse ve **Paralel kesinleştirme** seçeneği *Evet* olarak ayarlanmışsa kullanılabilir. Kesinleştirme işlemini paralelleştirmek için kullanılacak iş parçacığı sayısını girin. Master planlamada bu seçeneğin nasıl kullanılacağı hakkında öneriler için bkz. [Master planlama performansını iyileştirme](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > **İş parçacığı sayısı** alanı için *0* (sıfır) değeri, master planlama çalışma süresini artırır. Bu nedenle, bu alanı her zaman 0' dan büyük bir değere ayarlamanız önerilir.

    - **Satıcıya göre gruplandır** – Kesinleştirme sırasında planlanan satınalma siparişlerini gruplamak ve her satıcı için bir satınalma siparişi oluşturmak için bu seçeneği *Evet* olarak ayarlayın. Alternatif olarak her planlı sipariş için tek satır içeren bir satınalma siparişi oluşturabilirsiniz.
    - **Alıcı grubuna göre gruplandır** – Satıcı ve alıcı grubunu birleştiren tek bir satınalma siparişi oluşturmak ve planlı satınalma siparişlerini gruplandırmak için bu seçeneği *Evet* olarak ayarlayın. Bu seçeneği kullanmak için aynı zamanda **Satıcıya göre gruplandır** seçeneğini *Evet* olarak ayarlamanız gerekir.
    - **Satın alma anlaşmasına göre gruplandır** – Varolan satınalma anlaşmalarıyla aynı satıcıya sahip planlı satınalma siparişlerini gruplandırmak ve satınalma anlaşması başına bir satınalma siparişi oluşturmak için bu seçeneği *Evet* olarak ayarlayın. **Satıcıya göre grupla** etkinleştirildiğinde bu seçenek otomatik olarak etkinleştirilir. **Satın alma sözleşmesine göre gruplandır**'ı kullanmak için **Satın alma sözleşmesini bul**, **Master planlama parametreleri** sayfasında *Evet* olarak ayarlanmalıdır.
    - **Döneme göre grupla** ( **Satınalma siparişleri** bölümünde) – Planlı satınalma siparişlerinin gruplandırılmasını istediğiniz dönemi seçin. Bu seçeneği kullanmak için aynı zamanda **Satıcıya göre gruplandır** seçeneğini seçmeniz gerekir.
    - **Döneme göre grupla** ( **Transferler** bölümünde) – Planlı satınalma siparişlerinin gruplandırılmasını istediğiniz transferi seçin. Siparişler, **Kaynak ambar** ve **Hedef ambar** değerleri temel alınarak gruplandırılır.

    ![Kesinleştirme iletişim kutusundaki parametreler hızlı sekmesi](./media/manual-firming.png "Kesinleştirme iletişim kutusundaki parametreler hızlı sekmesi")

1. **Arka planda çalıştır** hızlı sekmesinde, işi toplu iş modunda çalışacak şekilde ayarlayın. Ancak, el ile kesinleştirme yaparken yinelenen bir zamanlama ayarlamak mantıklı değildir. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır. Ancak, el ile kesinleştirme için toplu işlem yalnızca geçerli olarak seçili planlı siparişleri işler. Sayfada geçerli olarak uygulanan filtrelere uyan siparişleri işlemez.
1. Ayarlarınızı uygulayıp kesinleştirilmiş siparişler oluşturmak için **Tamam**'ı seçin.

## <a name="auto-firm-planned-orders"></a>Planlı siparişleri otomatik kesinleştirme

Otomatik kesinleştirme, planlı siparişleri master planlama işleminin parçası olarak kesinleştirmenize olanak tanır. Kapsama grupları, bağımsız maddeler ve madde birleşimleri ile master plan birleşimleri için varsayılan kesinleştirme zaman dilimini tanımlayabilirsiniz. Daha sonra, master planlama çalışırken sipariş tarihi kesinleştirme için belirtilen zaman dilimi dahilinde olduğunda planlı siparişler otomatik olarak kesinleştirilecektir. Planlama Optimizasyonu ile oluşturulan planlı siparişler ve yerleşik master planlama işlemi, sipariş tarihini (başlangıç tarihi) farklı bir şekilde işler.

> [!NOTE]
> Planlanan satınalma siparişlerinin otomatik kesinleştirilmesi yalnızca bir satıcı ile ilişkilendirilmiş maddeler için gerçekleşir.
> 
> Kesinleştirilmiş türetilmiş siparişler (yani taşeron satınalma siparişleri), servis talebi değişiklik izleme etkin olduğunda *İncelemede* durumuna sahip olur.

> [!IMPORTANT]
> Bu bölümde açıklanan özelliğin Planlama Optimizasyonunda kullanılabilmesi için öncelikle, bu konunun başlangıcında açıklandığı gibi [*Planlama Optimizasyonu için otomatik kesinleştirme* özelliğinin](#enable-features) sisteminizde etkinleştirilmiş olması gerekir. Otomatik kesinleştirme, yerleşik master planlama altyapısıyla her zaman kullanılabilir.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Planlama Optimizasyonu ile otomatik kesinleştirme ile yerleşik planlama altyapısı kıyaslaması

Planlama Optimizasyonu ve yerleşik planlama altyapısı işlevlerinin ikisi de planlı siparişleri kesinleştirmek için kullanılabilir. Ancak, bazı önemli farklar vardır. Örneğin, Planlama Optimizasyonu işlevi hangi planlı siparişlerin kesinleştirileceğini belirlemek için sipariş tarihini (başka bir deyişle, başlangıç tarihi) kullanırken yerleşik planlama altyapısı gereksinim tarihini (başka bir deyişle, bitiş tarihi) kullanır. Aşağıdaki tablo, farkları özetlemektedir.

| Özellik | Planlama Optimizasyonu | Yerleşik planlama altyapısı |
|---|---|---|
| **Tarih esası** | Otomatik kesinleştirme, sipariş tarihini (başlangıç tarihi) temel alır. | Otomatik kesinleştirme, gereksinim tarihini (bitiş tarihi) temel alır. |
| **Sağlama süresi** | Sipariş tarihi (başlangıç tarihi) kesinleştirmeyi tetiklediğinden sağlama süresini kesinleştirme zaman diliminin bir parçası olarak düşünmeniz gerekmez. | Siparişlerin zamanında kesinleştirilmesini garanti etmeye yardımcı olması için kesinleştirme zaman dilimi, sağlama süresinden daha uzun olmalıdır. |
| **Geçerli hafta için siparişler** | Geçerli haftada başlaması gereken tüm siparişleri kesinleştirmek için kesinleştirme zaman dilimi bir hafta olmalıdır. | Geçerli haftada başlaması gereken tüm siparişleri kesinleştirmek için kesinleştirme zaman dilimi, sağlama süresi artı bir hafta olmalıdır. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Otomatik kesinleştirme ve kesinleştirme zaman dilimini ayarlama

Otomatik kesinleştirme özelliğini, ilgili kapsam ayarına, bu bölümün sonraki kısımlarında açıklandığı gibi, otomatik kesinleştirme zaman dilimi atayarak açabilirsiniz. Otomatik kesinleştirme herhangi bir karşılama kurulumu için açık değilse veya planlama belirli bir sayfadan başlatılırsa ( serbest bırakılan bir ürünün **Net gereksinimler** sayfası gibi), otomatik kesinleştirme süreci atlanır.

Otomatik kesinleştirme için gruplandırma ve işaretleme seçenekleri, değerlerini **Master planlama parametreleri** sayfasındaki **Standart güncelleştirme** sekmesinden alır.

Otomatik kesinleştirme zaman dilimi, ilgili kapsama ayarı için girdiğiniz gün sayısıyla tanımlanır. Kesinleştirme zaman dilimini aşağıdaki yollarla etkinleştirebilir ve kontrol edebilirsiniz:

- Bir kapsam grubu için varsayılan kesinleştirme zaman dilimini tanımlamak üzere **Master planlama \> Ayar \> Karşılama \> Karşılama grupları**'na gidin ve bir karşılama grubu seçin. Ardından **Diğer** hızlı sekmesinde, **Otomatik kesinleştirme zaman dilimi (gün sayısı)** alanına gün sayısını girin.
- Belirli bir maddeyle ilgili kapsam grubu için tanımlanan kesinleştirme zaman diliminin üzerine yazmak için, **Ürün bilgileri yönetimi \> Serbest bırakılmış ürünler**'e gidin. Eylem Bölmesi'nde **Plan**'ı ve ardından **Öğe kapsamı**'nı seçin. **Genel** sekmesinde, **Zaman dilimini geçersiz kıl**'ı seçin ve ardından **Otomatik kesinleştirme zaman dilimi (gün)** alanına gün sayısını girin.
- Belirli bir master planın kapsam grubu ve madde kapsamı için tanımlanan kesinleştirme zaman dilimi üzerine yazmak için **Master planlama \> Ayar \> Master planlar**'a gidin ve bir master plan seçin. Ardından **Gün cinsinden zaman dilimi** hızlı sekmesinde **Kesinleştir** seçeneğini *Evet* olarak ayarlayın ve gün sayısını girin.

Daha önce bahsedilen tüm saatleri *0* (sıfır) olarak ayarlarsanız, otomatik kesinleştirme ilgili kapsanan maddeler için etkili şekilde devre dışı bırakılır.

## <a name="firm-planned-orders-by-using-a-query"></a>Sorgu kullanarak planlı siparişleri kesinleştirme

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

Sorgu tabanlı kesinleştirme, önceden tanımlanan ölçütlere dayalı olarak kesinleştirmenizi sağlar. Otomatik kesinleştirmenin aksine sorgu tabanlı kesinleştirme, zaman içinde farklı zamanlarda farklı sipariş alt kümelerinin otomatik olarak kesinleştirilmesi için olanak sağlar. Ek olarak, planlı siparişlerin farklı tiplerini kesinleştirmek için el ile veya otomatikleştirilmiş operasyonları kullanabilirsiniz. Ayrıca, ayarlarınıza bağlı olarak hangi kesinleştirilmiş siparişlerin seçileceğini de önizleyebilirsiniz. Bu nedenle, seçimin beklentilerinize uygun olduğunu doğrulayabilirsiniz.

Otomatik kesinleştirme ile sorgu tabanlı kesinleştirmeyi birlikte kullanabilirsiniz. Örneğin, sorgu tabanlı kesinleştirme işi, eşleşen bir otomatik kesinleştirme kapsamı yapılandırmasının zaman diliminden daha uzun olan bir ileriye doğru zaman dilimine sahiptir. Bu nedenle, sorgu tabanlı kesinleştirme işi otomatik kesinleştirme tetiklenmeden bu planlı siparişleri işler. Belirli satıcıların siparişlerini, diğer satıcılardan gelen benzer ürünlere ait siparişlerden farklı zamanlamak için bu davranıştan yararlanabilirsiniz.

> [!IMPORTANT]
> Bu bölümde açıklanan özelliğin kullanılabilmesi için öncelikle, bu konunun başlangıcında açıklandığı gibi [*Filtrelemeyle planlı sipariş kesinleştirme* özelliğinin](#enable-features) sisteminizde etkinleştirilmiş olması gerekir.

Sorgu tabanlı kesinleştirme işlemini kullanarak planlı bir siparişi kesinleştirmek için aşağıdaki adımları izleyin.

1. **Master planlama \> Master planlama \> Çalıştır \> Planlı sipariş kesinleştirme** öğesine gidin.
1. **Planlı sipariş kesinleştirme** iletişim kutusunda **Parametreler** hızlı sekmesinde, temel işlem, işaretleme ve gruplama seçeneklerini ayarlayın. Bu seçenekler, **Kesinleştirme** iletişim kutusunda olduğu gibi çalışır. (Açıklamalar için önceki bölüme bakın.) Daha sonra **Plan** bölümünde, **Planlı sipariş kesinleştirme** iletişim kutusunda benzersiz olan aşağıdaki alanları ayarlayın:

    - **Plan** – Bu sorgu tarafından bulunan planlı siparişlerin kesinleştirilmesi sırasında uygulanması gereken master planı seçin.
    - **İleriki günler için kesinleştirme zaman dilimi** – Master planlama tarafından gelecekte çeşitli gereksinimlerin ve diğer hangi noktaların hesaplanması gerektiğini seçebilirsiniz.
    - **Geçmişteki günler için kesinleştirme zaman dilimi** – Master planlama tarafından geçmişte çeşitli gereksinimlerin ve diğer hangi noktaların hesaplanması gerektiğini seçebilirsiniz.

    ![Planli sipariş kesinleştirme iletişim kutusundaki parametreler hızlı sekmesi](./media/planned-order-firming-main-1.png "Planli sipariş kesinleştirme iletişim kutusundaki parametreler hızlı sekmesi")

1. Siparişe hangi kayıtların dahil edileceğini belirtmek için **Dahil edilecek kayıtlar** hızlı sekmesinde **Filtre** düğmesini seçin. Seçim ölçütünü, sıralama ölçütlerini ve birleşimleri tanımlayabileceğiniz standart bir sorgu iletişim kutusu görüntülenir. Alanlar, Supply Chain Management'ta bulunan diğer sorgular için çalıştıkları gibi çalışır. Buradaki alanlar salt okunurdur ve sorgunuzla ilgili değerleri gösterir.

    ![Planli sipariş kesinleştirme iletişim kutusundaki Dahil edilecek kayıtlar hızlı sekmesi](./media/planned-order-firming-main-2.png "Planli sipariş kesinleştirme iletişim kutusundaki Dahil edilecek kayıtlar hızlı sekmesi")

1. Şu ana kadarki ayarlarınıza göre kesinleştirilmiş siparişiniz içeriğini önizlemek için **Önizleme**'yi seçin. Kesinleştirilecektir olan planlı siparişlerin listesi bir ileti olarak gösterilir. Daha sonra, önizleme sırasında amaçladığınız siparişi gösterene kadar ayarlarınızı gerektiği şekilde ayarlayabilirsiniz.

    ![Kesinleştirilmiş sipariş önizleme örneği](./media/planned-order-firming-preview.png "Kesinleştirilmiş sipariş önizleme örneği")

    > [!WARNING]
    > Bu özellik, filtre ölçütleriyle eşleşen tüm planlı siparişleri kesinleştirir. Planlı siparişlerin kritik olmayan bir şekilde olarak kesinleştirilmesi, istenmeyen satınalma, transfer ve üretim emirlerinin oluşturulmasına neden olabilir. Devam etmeden önce, dahil edilecek kayıtları doğrulamak için **Önizleme** düğmesini kullanın.

1. **Arka planda çalıştır** hızlı sekmesinde, işi toplu iş modunda çalışacak şekilde ayarlayın ve/veya yinelenen bir zamanlama ayarlayın. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. Ayarlarınızı uygulayıp kesinleştirilmiş siparişler oluşturmak için **Tamam**'ı seçin.

## <a name="track-firmed-orders"></a>Kesinleştirilmiş siparişleri izleme

Kesinleştirilmiş bir planlı siparişi izlemek için aşağıdaki adımları izleyin.

1. [Herhangi bir planlı siparişler listesi sayfasını açın](approved-planned-order.md#view-planned-orders).
1. İzlemek istediğiniz planlı siparişi açın veya seçin.
1. Eylem Bölmesinde **Görünüm** sekmesinde **Görünüm** grubunda **Kesinleştirme geçmişi** öğesini seçin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

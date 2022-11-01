---
title: Konteynerleri sevkiyat için paketleme
description: Bu makalede, stok maddelerini doğrulamanızı ve onları konteynerlerde paketlemenizi sağlayan paketleme işlemi açıklanır.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708796"
---
# <a name="pack-containers-for-shipment"></a>Konteynerleri sevkiyat için paketleme

[!include [banner](../../includes/banner.md)]

Konteyner paketleme işlemi, stok maddelerini doğrulamanızı ve onları konteynerlerde paketlemenizi sağlar. Bu işlem sırasında, ambar çalışanları genellikle toplu depolama alanlarından alınan stok maddelerini çeker ve bunları bir ambalajlama alanına taşır. Burada birden fazla ambar çalışanı madde miktarlarını ve tiplerini kontrol edip uygun konteyner boyutlarına atar. Bir konteyner tam olarak paketlendiğinde, kapatılır ve sevk edilmeye hazır hale getirildiği çıkış noktası alanına taşınır.

Konteynerler maddelerin paketlenebileceği fiziksel yapıları temsil eder ve sistemde konteyner bilgilerini izleyebilirsiniz. Bu bilgiler, özellikle sevkiyat giderlerini konteynerlere dayalı olarak hesaplarsanız, taşıma planlaması sırasında yararlı olabilir. Sevk etmeden önce, bir sevkiyatta kullanılan konteyner sayısını, kullanılan konteyner tiplerini ve her bir konteynerin fiziksel boyutlarını (toplam hacim ve ağırlık gibi) görüntüleyebilirsiniz.

Birbiriyle ilişkili çeşitli giden ambar yetenekleri konteynerler ile kullanılabilir. Daha fazla bilgi edinmek için aşağıdaki makalelere bakın:

- [Dalga konteyner kullanımı](wave-containerization.md)
- [Giden sıralama](outbound-sorting.md)
- [Küçük paket sevkiyatı](small-parcel-shipping.md)
- [Onayla ve aktar](confirm-and-transfer.md)
- [Paketleme ve depolama için farklı boyutlar ayarlama](packing-vs-storage-dimensions.md)
- [Giden konteynerleri paketlemeye ve sevkiyatları işlemeye yönelik paketleme işi](packing-work.md)
- [Konteynerleri Warehouse Management mobil uygulaması ile doldurma](warehouse-app-packing-containers.md)
- [Örnek senaryo: Konteynerleri Warehouse Management mobil uygulaması ile doldurma](warehouse-app-pack-containers-scenario.md)
- [Konteyner etiketleri yazdırma](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>El ile ambalajlama operasyonlarını kullanmak için ambarınızı ayarlama

Giden operasyonlarınızı düzenlemenin iki temel yolu vardır:

- **Dalga oluşturma ve işleme** – Çalışanlar çıkış ambarı çalışmasına dayalı olarak malzeme çeker. Çalışanlar daha sonra, maddeleri hemen sevk edilmeye hazır oldukları bir giden sevkiyat yerleşimine doğrudan koyarlar. Bu işlemi ayarlama ve kullanma hakkında bilgi için bkz. [Dalga oluşturma ve işleme](wave-processing.md).
- **Paketleme istasyonlarında el ile paketleme** – Bu işlem, malzeme çekme ve sevkiyat operasyonları arasında ek bir operasyona sahiptir. Çalışanlar stoğu bir *bölme kapısı sevkiyat yerleşimine* koymak yerine, bunu bir *paketleme yerleşimine* koyar. Böylece, web istemcisindeki **Paket** sayfasını kullanarak paketleme işlemini ambalaj istasyonunda yönetirler. Bu işlemi etkinleştirmek için sisteminizi bu bölümde açıklandığı gibi yapılandırmanız gerekir.

### <a name="set-up-warehouse-locations-for-packing"></a>Paketleme için ambar yerleşimlerini ayarlama

Çalışanların, konteynerlerde paketlenebilmeleri amacıyla stok maddelerini koyacakları en az bir sevk konumunuz olmalıdır. Ambar yerleşimleri oluşturma hakkında daha fazla bilgi için bkz. [WMS özellikli ambarda yerleşimler yapılandırma](tasks\configure-locations-wms-enabled-warehouse.md). Aşağıdaki alt bölümler, paketleme yerleşimlerinin nasıl oluşturulacağını ve ayarlanacağını açıklamaktadır.

#### <a name="set-up-location-types-for-packing"></a>Paketleme için yerleşim türlerini ayarlama

Paketleme yerleşimleri için bir *yerleşim türü* tanımlamanız gerekir. Yerleşim tipleri farklı ambar yönetimi işlemlerini denetlemek için filtreleme seçenekleri olarak kullanılabilir. Her yerleşim türünün adı genellikle bu yerleşim türünün nasıl kullanılacağına ilişkin bir bilgiyi tarif eder. Burada ayarladığınız yerleşim türü, ambalaj operasyonları için kullanılan her bir yerleşimle ilişkilendirilmelidir.

Yerleşim türü ayarlamak için aşağıdaki adımları takip edin.

1. **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşim türleri** öğesine gidin.
1. Eylem Bölmesinde, kılavuza yerleşim türü eklemek için **Yeni**'yi seçin.
1. Yeni yerleşim türü için aşağıdaki alanları ayarlayın:

    - **Yerleşim türü** – Yerleşim türü için bir ad girin. Her ad benzersiz olmalıdır ve yerleşim türünün nasıl kullanılacağına ilişkin bir şeyler açıklamalıdır.
    - **Açıklama** – Yerleşim türü için kısa açıklama girin.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Sistemi paketleme yerleşim türü hakkında bilgilendirme

Bir yerleşim türü oluşturduktan sonra, sisteminizi bu yerleşim türünü ambalaj operasyonları için kullanılacak yerleşim türü olarak tanıması için ayarlamanız gerekir.

Ambalaj operasyonları için kullanılan yerleşim türünü ayarlamak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetimi parametreleri** öğesine gidin.
2. **Genel** sekmesinde yer alan **Yerleşim türleri** hızlı sekmesinde, **Paketleme yerleşimi türü** alanını paketleme istasyonlarını tanımlamak için kullanacağınız yerleşim tipine ayarlayın.

> [!NOTE]
> Microsoft Dynamics AX'in bir sürümünden yükseltme yapıyorsanız *Paketlemede* durumu, tutarlı şekilde çalışmadığından ve fazla veri sağladığından, sevkiyatlardan ve yüklerden kaldırılmıştır. Bu nedenle, **Sevkiyatlarda** ve **Paketlemedeki yükler** liste sayfaları kullanım dışı bırakılmıştır. Paketlenecek konteynerler yerleşim düzeyinde izlenir.
>
> Önceki sürümlerde, bir *yerleşim profili* belirtmek için **Ambar yönetimi parametreleri** sayfasının **Paketleme** sekmesindeki **Paketleme yerleşimi için profil kodu** alanını kullanarak paketleme yerini tanımlardınız. Geçerli sürümde, bu makalede açıklandığı şekilde bir *konum türü* belirtmek için **Ambar yönetimi parametreleri** sayfasının **Genel** sekmesindeki **Paketleme yerleşimi türü** alanını kullanırsınız. Yeni alan, hazırlama yerlerini ve son sevkiyat yerleşimlerini belirlemeye yönelik işlemle daha uyumlu hale getirilmiştir.
>
> Eski **Ambalajlama yerleşimi için profil kodu** alanını kullanmaya devam edebilirsiniz, ancak eski alan zamanla kullanım dışı olacağından, bunun yerine yeni **Ambalajlama yerleşimi türü** alanını kullanmaya başlamanız önerilmektedir.
>
> Eski **Ambalajlama yerleşimi için profil kodu** alanının ayarını temizler ve sayfayı kaydederseniz, alan kalıcı olarak devre dışı bırakılır. **Ambalajlama yerleşimi için profil kodu** alanının hiç kullanılmamış olduğu yüklemelerde her zaman devre dışı bırakılır. **Ambalajlama yerleşimi için profil kodu** alanının ayarını temizledikten sonra, ambalajlama konumunuzu ayarlamak ve tanımlamak için bu makalede açıklanan ayarları kullanın.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Paketleme yerleşimleri için yerleşim profillerini ayarlama

Her *yerleşim profili*, ilişkili konumlara uygulanan bilgileri ve kuralları belirler. Paketleme işlemlerinde kullanılacak en az bir yerleşim gerektiğinden, bunun için yerleşim türüne ek olarak bir yerleşim profili oluşturmanız gerekir. Her profil, herhangi bir sayıda yerleşim tarafından kullanılabilir. Ambalaj için kullanılan yerleşimler, plakaları izleyecek şekilde ayarlanmalıdır.

Paketleme konumu için yerleşim profili ayarlamak üzere bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Liste bölmesinden mevcut bir profil seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir profil oluşturun.
1. Yeni veya seçili profilin üst bilgisinde aşağıdaki alanları ayarlayın:

    - **Yerleşim profili kodu** – Profil için benzersiz bir kod girin.
    - **Ad**: Profil için tanımlayıcı bir ad girin.

1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Yerleşim biçimi** – Geçerli yerleşim için kullanılacak yerleşim biçimini seçin. Yerleşim biçimleri, bir ambar içinde kullanılan farklı yerleşim bölme pozisyonları için tutarlı ve benzersiz adlar oluşturmak üzere kullanılan isimlendirme sistemidir. Gereksinim duyduğunuz biçime henüz sahip değilseniz, **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşim biçimleri**'ne giderek bunu oluşturabilirsiniz. Daha fazla bilgi için bkz. [WMS özellikli ambarda yerleşimler yapılandırma](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Yerleşim türü** – Bu makalede daha önce açıklandığı gibi, **Ambar yönetimi parametreleri** sayfasında paketleme yerleşim türü olarak ayarlanan yerleşim türünü seçin.
    - **Plakayı izlemeyi kullan** – Paketleme yerleşimleri için bu seçeneği *Evet* olarak ayarlayın. Ambalaj sürecini denetleyebilmesi için sistem, ambalaj yerleşimlerinde bulunan plaka kimliklerini izleyebilmelidir.
    - **Negatif stoğa izin ver** – Paketleme yerleşimleri için bu seçeneği *Hayır* olarak ayarlayın.
    - **Karışık maddeler izin ver** – Paketleme yerleşimleri için bu seçeneği *Evet* olarak ayarlayın. Bu ayar, çoğu farklı madde numarası genellikle aynı anda paketleme yerlerine getirildiğinden gereklidir.
    - **Karma stok durumlarına izin ver** – Paketleme yerleşimleri için bu seçeneği *Evet* olarak ayarlayın. Bu ayar, farklı stok durumlarına sahip maddeler genellikle aynı anda paketleme yerlerine getirildiğinden gereklidir.
    - **Karışık stok toplu işlerine izin ver** – Paketleme yerleşimleri için bu seçeneği *Evet* olarak ayarlayın. **Karışık maddelere izin ver** seçeneği *Evet*'e ayarlandığında bu seçenek otomatik olarak *Evet* olarak ayarlanır.

#### <a name="set-up-packing-locations"></a>Paketleme konumları ayarlama

Çalışanların, konteynerlerde paketlenmesi gereken stok maddelerini koyacakları en az bir *konum* olmalıdır.

Paketleme yerleşimi eklemek için aşağıdaki adımları takip edin.

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konumlar** öğesine gidin.
1. Eylem Bölmesinde, bir yerleşim oluşturmak için **Yeni**'yi seçin.
1. Yeni yerleşim için aşağıdaki alanları ayarlayın:

    - **Ambar** – Ambalaj yerleşiminin bulunduğu ambarı belirtin.
    - **Yerleşim** – Yeni yerleşim için bir ad girin.
    - **Yerleşim profili kodu** – Önceki bölümde oluşturduğunuz kodu belirttiğinizden emin olun.

## <a name="set-up-the-packing-process"></a>Paketleme işlemini ayarlama

Bu bölümde, paketleme işlemini etkinleştiren ve çalışanların stoğu konteynerlerde paketlemesini sağlayan ayarları yapılandırma yöntemi açıklanmıştır.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Konteyner paketleme ilkelerini ayarlama

Her *konteyner paketleme ilkesi* bir konteynerin nasıl işlenmesi gerektiğini tanımlar. Her yeni konteyner oluşturduğunuzda, buna uygulanacak bir konteyner paketleme ilkesi de seçersiniz.

Konteyner paketleme ilkesi ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi\> Kurulum \> Konteynerler \> Konteyner paketleme ilkeleri**'ne gidin.
1. Liste bölmesinden mevcut bir ilke seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir profil oluşturun.
1. Yeni veya seçili ilkenin üst bilgisinde aşağıdaki alanları ayarlayın:

    - **Konteyner paketleme ilkesi** – İlke için benzersiz bir ad girin.
    - **Açıklama** – İlke için açıklayıcı bir ad girin.

1. **Genel bakış** sekmesinde, aşağıdaki alanları ayarlayın. Bu alanlar, konteyner kapatıldığında hangi eylemlerin gerçekleştirileceğini, iş oluşturma ile birlikte mi yoksa iş oluşturma olmadan mı çalışılacağını ve hangi konteynerin paketleme istasyonundan serbest bırakılacağını belirtmenize olanak sağlar.

    - **Ambar** – Paketleme ilkesinin geçerli olduğu ambarı seçin.
    - **Son sevkiyat için varsayılan konum** – Kapatıldıktan sonra konteyner için tercih edilen yerleşimi belirtin. Bu alan yalnızca **Konteyner serbest bırakma ilkesi** alanı *Son sevkiyat yerleşiminde kullanılabilir yap* olarak ayarlandığında kullanılabilir.
    - **Sıralama için varsayılan yerleşim** – Bu alan, [giden sıralama](outbound-sorting.md) özelliğiyle kullanılır.
    - **Ağırlık birimi** – Bir konteyner kapatıldığında ve bildirildiğinde kullanılacak varsayılan ölçü birimini seçin. Tipik olarak bu ölçü birimi, paketleme istasyonunda bir ölçek tarafından kullanılan ölçü birimidir. Bu alan, iş oluşturma içeren veya içermeyen ilkelere uygulanır.
    - **Konteyner kapanış ilkesi** – Konteyner kapatıldığında ne olacağını tanımlamak için aşağıdaki seçeneklerden birini belirleyin:

        - *Otomatik serbest bırakma* – Konteyner, paketleme istasyonundan serbest bırakılacaktır ve **Konteyner bırakma ilkesi** alanında belirtilen eylem tetiklenir.
        - *Gecikmeli serbest bırakma* – Konteyner, paketleme istasyonundan hemen serbest bırakılmayacaktır. Bir ambar çalışanının bunu daha sonra el ile serbest bırakması gerekir.
        - *İsteğe bağlı* – Bir çalışan konteyneri kapatırken konteynerin serbest bırakılıp bırakılmayacağını seçebilir.

        Ambalaj istasyonu genellikle doğrudan müşterilere sevk edilen tekli konteynerleri işlediğinden, en doğal yaklaşım konteynerleri hemen serbest bırakmaktır. Ambalaj istasyonu birden fazla konteynerden veya paletten oluşan sevkiyatları işliyorsa, tüm sevkiyat veya palet ambalajlanıp teslim için hazır olana kadar serbest bırakmayı geciktirmek en iyi seçenek olacaktır.

    - **Konteyner serbest bırakma ilkesi** – Konteyner, paketleme yerleşiminden serbest bırakıldığında ne olacağını tanımlamak için aşağıdaki seçeneklerden birini belirleyin:

        - *Son sevk yerleşiminde kullanılabilir hale getir* – Konteyneri son sevkiyat yerleşimiyle güncelleştirin. Bu seçeneği belirlerseniz, kapatıldıktan sonra konteyner için tercih edilen yerleşimi belirtmek için **Son sevkiyat için varsayılan konum** alanını kullanın.
        - *Konteyneri sevk istasyonundan taşımak için iş oluştur* – Konteyneri ambalaj istasyonundan hazırlama alanına veya doğrudan bölme kapısına taşımak için iş oluşturun. Konteyner için iş oluşturulurken uygulanması gereken iş şablonunu belirtmek için **İş şablonu** alanını kullanın.
        - *Giden sıralama konumuna konteyner ata* – Bu seçenek, [giden sıralama](outbound-sorting.md) özelliğiyle kullanılır.

        Çoğu durumda konteynerleri taşımak için iş oluşturmanız önerilir, çünkü bu yaklaşım ambardaki el ile gerçekleştirilen işlemleri daha iyi temsil eder. Ancak, ambalaj istasyonunun doğrudan bölme kapısı alanında bulunduğu basit senaryolarda veya durumlarda, konteynerin son sevkiyat yerleşiminde hemen kullanılabilir olması tercih edilebilir.

    - **İş şablonu** – Konteyner için iş oluşturulurken uygulanması gereken iş şablonunu belirtmek için iş şablonunu seçin. Bu alan yalnızca **Konteyner serbest bırakma ilkesi** alanı, *Konteyneri paketleme istasyonundan taşımak için iş oluştur* olarak ayarlandığında ve *Paketlenmiş konteyner çekme işi* adlı bir iş emri türüyle ilişkili olduğunda kullanılabilir. Daha fazla bilgi için, bkz. [İş şablonları ve yerleşim yönergeleri](control-warehouse-location-directives.md).

    Geri kalan adımlarda, *bildirim* ile ilgili ayarlar yapılandırılacaktır. Bildirim, bir taşıma sağlayıcısından alınan izleme kimliğiyle birlikte bir konteyner, konteyner grubu veya sevkiyatın ağırlığını belirtme işlemidir. Dynamics 365 Supply Chain Management harici taşımacılık sağlayıcı sistemleriyle tümleştirilmez. Bunun yerine ambar işçileri, taşıma sağlayıcısından alınan etiketleri yazdırmalı ve sonra da bildirim yordamını tamamladıklarında bir izleme numarası taramalıdır.

    Bildirim gereksinimleri müşteriden müşteriye hatta sevkiyattan sevkiyata farklı olduğundan, paketleme ilkeleri iş akışında önemli esnekliğe izin verir. Konteynerler, konteyner grupları ve herhangi bir sevkiyat kombinasyonu için bildirimleri ayarlayabilirsiniz.

    Çok düzeyli bir bildirim yordamı kullanıyorsanız, çalışanların ilgili konteyner grubunu bildirdiklerinde önce tüm konteynerleri bildirmeleri ve ilgili sevkiyatı bildirmeden önce tüm konteyner gruplarını bildirmeleri gerekir.

1. **Konteyner bildirimi** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Konteyner kapanışında otomatik bildirim** – Bildirim bilgilerini konteyner kapatma işleminin bir parçası olarak uygulamak için bu seçeneği *Evet* olarak ayarlayın. Taşımacılık tümleştirmesini kullanmıyorsanız, bilgilerin el ile kaydedilmesi gerekir.
    - **Konteyner için bildirim gereksinimleri** – Aşağıdaki seçeneklerden birini belirleyin:

        - *Hiçbiri* – Hiçbir bildirim işlemi kullanılmaz.
        - *El ile* – Bildirim, paketleme iş akışı tarafından zorunlu tutulur. Sistem, bir konteynerin bildirim tamamlanana kadar kapatılmasına veya serbest bırakılmasına izin vermez.
        - *Taşımacılık yönetimi* – Bildirim, taşımacılık yönetimi (TMS) değerlendirme altyapıları aracılığıyla yapılır. Bu seçenek, taşıma sağlayıcısı için belirli bir altyapıyı uygulamak amacıyla özel geliştirme gerektirdiğinden, geçerli sürümde kullanıma hazır olarak çalışmayacaktır.

    - **Konteyner içeriğini yazdır** – Bir konteyner kapalı olarak kaydedilirse, kapsayıcı içeriği raporunu otomatik olarak yazdırmak için bu seçeneği *Evet* olarak ayarlayın. Ayrıca, rapor isteğe bağlı olarak da yazdırılabilir.

1. **Konteyner grup bildirimi** hızlı sekmesinde, **Konteyner grubu için bildirim gereksinimleri** alanında, aşağıdaki seçeneklerden birini belirleyin:

    - *Yok* – Konteyner grubu bildirimi, paketleme iş akışına gereksinim olarak dahil edilmeyecektir.
    - *El ile* – Konteyner grubu bildirimi, paketleme iş akışına gereksinim olarak dahil edilecektir. Grubun bildirilebilmesi için öncelikle gruba dahil edilen tüm konteynerlerin kapatılması gerekir. Paketleme istasyonunda bulunan her bir konteyner grubu için bir bildirim tamamlamanız gerekiyorsa bu seçeneği belirleyin. Konteynerler bir palette paketleniyorsa ve paletin tümü bildirimli ise, genellikle bu seçeneği seçersiniz.

    > [!NOTE]
    > Geçerli sürüm, konteyner grupları için bildirim raporlarını desteklemez ve konteyner grupları için TMS altyapısı desteği yoktur.

1. **Sevkiyat bildirimi** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Sevkiyat için bildirim gereksinimleri** – Aşağıdaki seçeneklerden birini belirleyin:

        - *Yok* – Sevkiyat bildirimi, paketleme iş akışına gereksinim olarak dahil edilmeyecektir.
        - *El ile* – Sevkiyat bildirimi, paketleme iş akışına gereksinim olarak dahil edilecektir. Bildirim tamamlanana kadar bir sevkiyatın konteynerleri serbest bırakılamaz.
        - *Taşımacılık yönetimi* – Bildirim, TMS değerlendirme altyapıları aracılığıyla yapılır. Bu seçenek, taşıma sağlayıcısı için belirli bir altyapıyı uygulamak amacıyla özel geliştirme gerektirdiğinden, geçerli sürümde kullanıma hazır olarak çalışmayacaktır.

        Ambalaj istasyonunda paketlenmiş tüm sevkiyat için bir bildirim doldurmanız gerekiyorsa, sevkiyat bildirimi etkinleştirilmelidir. Sevkiyat birden çok konteyner veya konteyner grubundan oluşsa da, bir konsolide bildirim gerektiğinde kullanılır.

    - **Sevk irsaliyesini yazdır** – Sevk irsaliyesini sevkiyat bildiriminin bir parçası olarak otomatik yazdırmak için bu seçeneği *Evet* olarak ayarlayın. Sevk irsaliyesi isteğe bağlı olarak da yazdırılabilir.

### <a name="set-up-container-types"></a>Konteyner türlerini ayarla

El ile paketleme işlemi sırasında, maddelerin konteynerlerde paketlenebilmesi için önce konteynerler oluşturulmalıdır. Her konteyner, bir konteynerin en yüksek fiziksel hacmini ve ağırlık kapasitesini tanımlayan bir *konteyner türüne* dayandırılmalıdır.

Konteyner türü oluşturmak için aşağıdaki adımları takip edin.

1. **Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner türleri** öğesine gidin.
1. Eylem bölmesinde konteyner türü eklemek için **Yeni**'yi seçin.
1. Yeni konteyner türü için aşağıdaki alanları ayarlayın:

    - **Konteyner türü kodu** – Konteyner türü için benzersiz bir kod girin.
    - **Açıklama** – Yeni konteyner türünün açıklamasını girin.
    - **Dara ağırlık** – Konteynerin gerçek veya tahmini ağırlığını girin.
    - **Maksimum net ağırlık** – Konteynerin alabileceği maksimum ağırlığı girin.

1. **Konteyner boyutları** bölümünde, **Uzunluk**, **Genişlik**, **Yükseklik** ve **Hacim** alanlarına, konteynerin kendisinin fiziksel boyutlarını girin.
1. **Maksimum değerler** bölümünde, **Uzunluk**, **Genişlik**, **Yükseklik** ve **Hacim** alanlarına, konteynerin alabileceği maksimum fiziksel boyutları girin.
1. Konteynerleri kullanan diğer işlemlerle ilişkilendirilmiş kapsayıcı türleri için ek öznitelikler tanımlayabilirsiniz. Daha fazla bilgi için bkz. [Konteyner kullanımı](wave-containerization.md).

> [!NOTE]
> El ile paketleme işlemi için sistem yalnızca, **Maksimum değerler** bölümündeki **Maksimum net ağırlık** alanının değerini ve **Hacim** alanının değerini kullanır.

### <a name="set-up-packing-profiles"></a>Paketleme profilleri ayarla

Paketleme işlemi için *Paketleme profilleri* gereklidir. Bunlar, **Paket** sayfasında bir paketleme işlemi başlattığınızda varsayılan olarak seçilebilir veya ayarlanabilir.

Paketleme profili ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Paketleme \> Paketleme profilleri**'ne gidin.
1. Liste bölmesinden mevcut bir profil seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir profil oluşturun.
1. Yeni veya seçili profilin üst bilgisinde aşağıdaki alanları ayarlayın:

    - **Paketleme profili kodu** – Profil için kısa bir kod girin.
    - **Açıklama** – Paketleme profili için bir açıklama girin.
    - **Konteyner paketleme ilkesi** – Profile uygulanan ambalaj ilkesini seçin. Daha fazla bilgi için bu makalenin [Sevkiyat paketleme ilkelerini ayarlama](#packing-policy) bölümüne bakın.
    - **Konteyner Kimliği modu** – Bir konteyner oluşturulduğunda bir konteyner kimliğinin otomatik olarak mı oluşturulacağını yoksa el ile mi oluşturulacağını belirler.
    - **Konteyner türü** – Yeni konteyner türü oluşturulduğunda varsayılan olarak kullanılacak konteyner türünü seçin.
    - **Konteyner kapatmada konteyneri otomatik oluştur** – Önceki konteyner kapatıldıysa ve geçerli sevkiyatta bir veya daha fazla satır kaldıysa otomatik olarak yeni bir konteyner oluşturmak için bu onay kutusunu seçin.

### <a name="set-up-warehouse-workers"></a>Ambar çalışanlarını ayarlama

Web istemcisinin **Paket** sayfasını kullanarak veya Warehouse Management mobil uygulamasında *Paketleme* faaliyet kodunu kullanarak konteynerleri paketleyen her kullanıcının veya çalışanın, gerekli güvenlik erişim haklarının atandığı bir *çalışan/kişi* kaydıyla ilişkilendirilmiş bir kullanıcı hesabına sahip olması gerekir. (Kullanıcıların nasıl ayarlanacağı konusunda daha fazla bilgi için bkz. [Yeni kullanıcılar oluşturma](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md).)

Paketleme işlemi için bir *çalışan/kişi* kaydı ayarlamak üzere bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Çalışan**'a gidin.
1. Eylem Bölmesi'nde, bir iş kullanıcısı eklemek için **Yeni**'yi seçin.
1. Ambalaj sürecini tamamlayacak kullanıcı için, **Çalışan** alanını **Human resources** modülünde tanımlanan mevcut çalışan kaydına ayarlayın.
1. **Profil** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Konteyner paketleme ilkesi** – Paketleme istasyonunda kapsayıcıların nasıl işlenmesi gerektiğini tanımlayan bir konteyner ambalaj ilkesi seçin. Seçtiğiniz konteyner ambalaj ilkesi, ambalaj istasyonunu açtıklarında çalışan için önceden seçilmiş olacaktır. Daha fazla bilgi için şu blog gönderisine bakın: [İyileştirilmiş paketleme işlevi](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Paketleme profili kodu** – Kullanılması gereken paketleme ilkesi ve konteyner ayarlarını tanımlayan bir ambalaj profili kodu seçin. Seçilen ambalaj profili kodu bir konteyner ambalaj ilkesiyle ilişkilendirilmişse, bu sayfadaki **Konteyner ambalaj ilkesi** alanının ayarını değiştiremezsiniz.

1. **Varsayılan ambalaj istasyonu** hızlı sekmesinde, çalışana uygulanacak varsayılan tesis, ambar ve yerleşimi seçin.
1. Çalışan, konteyner paketleme çalışmalarını yönetmek ve kaydetmek için Warehouse Management mobil uygulamasını kullanacaksa, **Kullanıcılar** hızlı sekmesinde, çalışanın uygulamada oturum açması için kullanabileceği bir veya daha fazla hesap ayarlayın. Daha fazla bilgi için [Mobil aygıt kullanıcı hesapları](mobile-device-work-users.md) bölümüne bakın.

## <a name="example-scenario"></a><a name="scenario"></a>Örnek senaryo

Bu bölüm, bir siparişin nasıl oluşturulacağını ve maddelerin nasıl paketleneceğini gösteren örnek bir senaryo sağlar.

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Bu senaryoyu, özelliği üretim sisteminde kullanmaya yönelik bir kılavuz olarak da kullanabilirsiniz. Ancak, bu durumda, burada açıklanan her ayar için kendi değerlerinizi kullanmanız gerekir.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Ambalaj işi yapabilen bir kullanıcı olarak oturum açma

Konteynerleri paketlemek için gerekli izinlere sahip bir kullanıcı hesabı kullanarak Supply Chain Management'ta oturum açın. *Julia Funderburk* kullanıcısı, demo verilerinin bir parçası olarak dahil edilir ve gerekli izinlere sahiptir. Bu kullanıcının kullanıcı kimliği *Admin*'dir.

### <a name="create-a-sales-order-and-complete-the-work"></a>Satış siparişi oluşturma ve işi tamamlama

Bir satış siparişi oluşturmak ve sipariş edilen maddeleri sevk istasyonuna taşıma işini tamamlamak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanında *ABD-005*'yi seçin.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır ve **Satış siparişi satırları** hızlı sekmesi üzerinde tek bir boş satır içerir. Yeni sipariş satırı için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *2*
    - **Tesis:** *6*
    - **Ambar:** *62*

1. Sipariş satırı hala seçiliyken, **Satış siparişi satırları** hızlı sekmesinin araç çubuğunda **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, Eylem bölmesinde, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Bir ileti siparişin sevkiyat ve dalga kodlarını gösterir.

1. Sipariş satırı hala seçiliyken, **Satış siparişi satırları** hızlı sekmesinin araç çubuğunda **Ambar** \> **İş ayrıntıları**'nı seçin. Dalgalarınızı çalıştırmak için toplu iş işlemeyi kullanıyorsanız, çalışmanın oluşturulması için kısa bir süre beklemeniz gerekebilir.
1. **İş** sayfasındaki Eylem Bölmesi üzerinde, **İş** sekmesinde, **İşi tamamla**'yı seçin.
1. **İşi tamamlama** sayfasındaki **Kullanıcı kimliği** alanında *62* olarak ayarlayın.
1. Eylem Bölmesi'nde **İşi doğrula**'yı seçin.
1. İşin geçerli olduğunu belirten bir ileti aldığınızda, stok maddelerini çekme ve bunları *Paket* yerleşimine koyma işlemini tamamlamak için **İşi tamamla**'yı seçin.
1. Üst kılavuzda iş için gösterilen **Sevkiyat kodu** değerini not edin.

### <a name="pack-the-ordered-items-into-a-container"></a>Sipariş edilen maddeleri bir konteynerde paketleme

Stok maddeleri artık paketleme alanına getirilmiş ve konteynerlerde paketlenmeye hazır durumdadır. Sistemde yeni bir konteyner oluşturmak ve paketlemek için aşağıdaki adımları izleyin.

1. **Ambar Yönetimi \> Paketleme ve Konteyner kullanımı \> Paket**'e gidin.
1. **Sevk istasyonu seç** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Tesis:** *6*
    - **Ambar:** *62*
    - **Yerleşim:** *Paket*
    - **Paketleme profili kodu:** *WH62*

1. **Tamam**'ı seçin.
1. **Paket** sayfasında, **Plaka veya sevkiyat** alanına, daha önce not ettiğiniz sevkiyat kodunu girin. Şimdi, kalan açılmış maddeleri **Açık satırlar** hızlı sekmesinde görmelisiniz.
1. Eylem bölmesinde, sistemde konteyner oluşturmak için **Yeni konteyner**'i seçin.
1. **Yeni konteynerin kodu** iletişim kutusunda **Konteyner türü** alanını *SmallBox* olarak ayarlayın.
1. Konteyneri oluşturmak için **Tamam**'ı seçin.
1. **Paket** sayfasına dönmek için **Tamam**'ı seçin. **Açık konteynerler** hızlı sekmesi şimdi, oluşturduğunuz konteynerin **Konteyner kodu** değerini gösterir.
1. Bu senaryoda, şimdilik sipariş edilen öğelerden yalnızca birini paketlersiniz. Dolayısıyla, **Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Miktar:** *1.00*
    - **Tanımlayıcı:** *A0001*

    **Tanımlayıcı** değerini seçtikten hemen sonra sayfa, bir maddenin paketlendiğini belirtmek için **Açık satırlar** ve **Tüm satırlar** hızlı sekmelerini güncelleştirir. Şimdi, *A0001* maddesinin iki parçasını paketlemiş olmanız gerekir.

1. Eylem Bölmesinde **Konteyneri kapat**'ı seçin.
1. **Konteyneri kapat** iletişim kutusunda, varsayılan **Brüt ağırlık** değerini doldurmak için **Sistem ağırlığını al**'ı seçin.
1. Konteyneri kapatmak için **Tamam** öğesini seçin.

> [!TIP]
> Konteynerleri bağlama göre görüntülemenin çeşitli yolları vardır. Örneğin, bir sevkiyatı paketlediğinizde, sevkiyatın bir parçası olan konteynerleri veya fiziksel olarak bir ambalaj istasyonunda bulunan tüm konteynerleri görüntülemek genellikle yararlıdır. **Ambalaj istasyonu** sayfasında, bir ambalaj istasyonundaki tüm açık ve kapalı konteynerleri görüntülemek için kullanabileceğiniz düğmeler vardır. Bu görünümler belirli bir sevkiyatla sınırlı değildir. Bir çalışanın konteyneri paketlediği ve başka bir çalışanın ise konteyneri bildirip serbest bıraktığı durumlarda çok yararlı olabilir.
>
> Tüm konteynerlerin birleştirilmiş bir görünümü de kullanılabilir. Bu görünüm, çoğunlukla tek bir ambalaj istasyonunun kapsamı dışında çalışan kullanıcılar için yararlıdır. Görmek için **Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Konteynerler**'e gidin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

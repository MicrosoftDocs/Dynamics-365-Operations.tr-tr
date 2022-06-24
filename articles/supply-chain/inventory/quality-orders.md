---
title: Kalite emirleri
description: Bu makalede, kalite emirlerinin el ile veya otomatik olarak nasıl oluşturulacağı ve incelemeler gerçekleştirmek ve Microsoft Dynamics 365 Supply Chain Management'ta test sonuçlarını kaydetmek için bunlarla nasıl çalışılacağı açıklanmaktadır.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb7ab1de0fb4d93ed18f1862630c1af7af7f3095
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857793"
---
# <a name="quality-orders"></a>Kalite emirleri

[!include [banner](../includes/banner.md)]

Bu makalede, kalite emirlerinin el ile veya otomatik olarak nasıl oluşturulacağı ve incelemeler gerçekleştirmek ve Microsoft Dynamics 365 Supply Chain Management'ta test sonuçlarını kaydetmek için bunlarla nasıl çalışılacağı açıklanmaktadır.

## <a name="automatically-created-quality-orders"></a>Otomatik olarak oluşturulan kalite emirleri

Sistemi, madde örnekleme kurallarına göre otomatik olarak kalite emirleri oluşturacak şekilde konfigüre edebilirsiniz. Daha fazla bilgi için bkz. [Kalite yönetimi madde örnekleme](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>El ile kalite emri oluşturma

El ile kalite emri oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Kalite emirleri** iletişim kutusunda, **Referans türü** alanında, kalite emrinizin ilişkilendirileceği stok başvurusunu seçin. Seçim için kullanılabilen referans türlerinin açıklaması için, bu makalenin ilerleyen kısımlarında yer alan [Kalite emri başvuru türleri](#ref-types) bölümüne bakın.

    > [!NOTE]
    > Seçilen referansla ilgili stoğun kullanılabilir durumda olması gerekir. Seçtiğiniz referans türü, miktar ve stok boyutları birleşimi için kullanılabilir bir stok yoksa, bir hata iletisi alırsınız.

1. **Referans türü** alanında seçtiğiniz değere bağlı olarak, aşağıdaki adımlardan birini izleyin:

    - **Stok**'u seçtiyseniz ek referans gerekmez.
    - **Satış** veya **Satınalma** seçeneğini belirlediyseniz, aşağıdaki bilgileri belirtin:

        - **Hesap seçimi** – Müşteri veya satıcı numarasına başvurun.
        - **Referans numarası** – Satış siparişinin veya satınalma siparişi numarasına başvurun.
        - **Referans lotu** – Belirli satış siparişi satırına veya satınalma sipariş satırına başvurun.

    - **Üretim**, **Karantina** veya **Ortak ürün üretimi**'ni seçtiyseniz, **Referans numarası** alanında üretim emri, toplu iş siparişi veya karantina sipariş numarasına başvurun.
    - **Rota işlemi** seçeneğini belirlediyseniz, aşağıdaki bilgileri belirtin:

        - **Referans numarası** – Üretim siparişi veya toplu iş siparişi numarasına başvurun.
        - **Operasyon numarası** – Belirli rota operasyon numarasına başvurun.
        - **Operasyon** – Belirli rota operasyonuna başvurun.
        - **Kaynak** – Rota operasyonunu ile kullanılması gereken belirli bir kaynağa başvurun.

1. **Test grubu** alanında, gerçekleştirilmesi gereken test grubunu seçin.
1. **Miktar** alanında, test edilmesi gereken maddelerin miktarını girin.
1. **Stok boyutları** bölümünde, seçili madde için gerekli tüm ek stok boyutlarını girin.
1. **Tamam**'ı seçin.

Bir kalite emri oluşturulduktan sonra, stok incelemeyi başlatmak ve test sonuçlarını kaydetmek için kullanabilirsiniz. Test sonuçlarını kaydetme ve doğrulama hakkında daha fazla bilgi için bkz. [Malların kalitesini inceleme](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Kalite emri referans türleri

Kalite emirleri, ambarınızda belirli bir stokla ilgili incelemeleri ve test sonuçlarını izlemek için kullanılır. Kalite emri, test edilmekte olan stoğun kaynağını temsil eden bir referans içermelidir. Kalite emirleri aşağıdaki referans türleriyle ilişkili olabilir:

- **Stok** – Bu referans türü, eldeki stoğu inceliyor olduğunuzu gösterir. Bu tür incelemeler genellikle rasgele veya planlanmamıştır ve bir ambar çalışanı bir sorunu belirlediğinde gerçekleştirilir.
- **Satış** – Bu referans türü, belirli bir satış siparişiyle ilişkili stoğu inceliyor olduğunuzu gösterir. Bu tür incelemeler genellikle müşteri belirtimleri veya bir müşteriye sevkiyatın parçası olarak sağlanması gereken bir analiz sertifikası (CoA) ile ilgilidir. (CoA bazen uyumluluk sertifikası olarak \[CoC\] da adlandırılır.)
- **Satınalma** – Bu referans türü, belirli bir satınalma siparişiyle ilişkili stoğu inceliyor olduğunuzu gösterir. Bu tür incelemeler genellikle gelen malları stoğa koymadan veya üretim süreçlerinde tüketilmeden önce incelemek için kullanılır.
- **Üretim** – Bu referans türü, belirli bir üretim siparişiyle ilişkili stoğu inceliyor olduğunuzu gösterir. Bu tür incelemeler genellikle tamamlanan malları stoğa koymadan önce incelemek için kullanılır.
- **Karantina** – Bu referans türü, belirli bir karantina siparişiyle ilişkili stoğu inceliyor olduğunuzu gösterir. Karantina siparişleri, bir ambardaki stoğu veya ambarınızdaki bir alanın stoğunu izleyen özel bir sipariş türüdür. Bu tür incelemeler genellikle, bir müşterinin iade ettiği veya daha fazla analiz amacıyla karantinaya alınmış malları incelemek için kullanılır. Karantina siparişleri, kalite emirlerinden oluşturulabilir. Alternatif olarak, diğer kaynaklardan da oluşturulabilir ve ardından kalite emirleri karantina emirleriyle ilişkilendirilebilir.
- **Rota işlemi** – Bu referans türü, belirli bir üretim siparişiyle ilişkili belirli bir rota adımını inceliyor olduğunuzu gösterir. Bu tür incelemeler genellikle üretim sürecindeki bir sonraki adıma geçmeden önce bir ürünün süren işi (WIP) analiz etmek için kullanılır.
- **Ortak ürün üretimi** – Bu referans türü, belirli bir üretim siparişiyle ilişkili ortak ürünü inceliyor olduğunuzu gösterir. Bu tür incelemeler genellikle ürün stoka eklenmeden önce toplu bir sipariş ortak ürününü denetlemek için kullanılır.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Sistemin çeşitli bölümlerinden kalite emirlerini görüntüleme ve oluşturma

Kalite emirleri el ile oluşturulabilir. Alternatif olarak, tanımladığınız kalite ilişkileri temel alınarak otomatik olarak da oluşturulabilirler. Kalite emirlerini otomatik olarak oluşturma ve yönteme hakkında daha fazla bilgi için, bkz. [Kalite ilişkilendirmeleri](quality-associations.md).

Kalite emri sayfasını, el ile yeni bir kalite emri oluşturmak veya başka bir kayıtla ilişkili kalite emrinin durumunu görüntülemek için kullanabilirsiniz. Kalite emri sayfasına erişmek için çeşitli yollar vardır.

### <a name="from-the-quality-orders-page"></a>Kalite emirleri sayfasından

Kalite emirlerini elle oluşturmak ve mevcut tüm kalite emirlerini görüntülemek için **Stok Yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin. Bu makalenin geri kalan bölümleri, **Kalite emirleri** sayfasıyla nasıl çalışılacağı hakkında daha fazla bilgi sağlar.

### <a name="from-sales-orders"></a>Satış siparişlerinden

Satış siparişleriniz ile ilgili kalite emirleriyle çalışmak için **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin ve aşağıdaki adımlardan herhangi birini izleyin:

- Bir satış siparişi açın veya bunu ızgarada seçin. Sonra, Eylem Bölmesinde, **Çek ve paketle** sekmesinde, **Kalite yönetimi** grubunda, **Kalite emirleri** sayfasını açmak için **Kalite emirleri**'ni seçin. Burada, satış siparişiyle ilişkili kalite emirlerini görüntüleyebilir, oluşturabilir veya güncelleştirebilirsiniz.
- Bir satış siparişi açın ve ardından **Başlık** sekmesinde **Genel** hızlı sekmesini seçin. **Kalite emri durumu** alanı, satış siparişiyle ilişkili tüm kalite emirlerinin genel durumunu gösterir.
- Bir satış siparişi açın ve ardından **Satırlar** sekmesinde **Satış siparişi satırları** hızlı sekmesini seçin. **Kalite emri durumu** sütunu, satış siparişinin her satırının durumunu gösterir.

### <a name="from-purchase-orders"></a>Satınalma siparişlerinden

Satınalma siparişleriniz ile ilgili kalite emirleriyle çalışmak için **Tedarik ve kaynaklar \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin ve aşağıdaki adımlardan herhangi birini izleyin:

- Bir satınalma siparişi açın veya bunu ızgarada seçin. Sonra, Eylem Bölmesinde, **Teslim al** sekmesinde, **Kalite yönetimi** grubunda, **Kalite emirleri** sayfasını açmak için **Kalite emirleri**'ni seçin. Burada, satınalma siparişiyle ilişkili kalite emirlerini görüntüleyebilir, oluşturabilir veya güncelleştirebilirsiniz.
- Bir satınalma siparişi açın ve ardından **Başlık** sekmesinde **Genel** hızlı sekmesini seçin. **Kalite emri durumu** alanı, satınalma siparişiyle ilişkili tüm kalite emirlerinin genel durumunu gösterir.
- Bir satınalma siparişi açın ve ardından **Satırlar** sekmesinde **Satınalma siparişi satırları** hızlı sekmesini seçin. **Kalite emri durumu** sütunu, satınalma siparişinin her satırının durumunu gösterir.

### <a name="from-production-orders"></a>Üretim emirlerinden

Üretim emirlerinizle ile ilgili kalite emirleriyle çalışmak için **Üretim kontrolü \> Üretim emirleri \> Tüm üretim emirleri**'ne gidin ve aşağıdaki adımlardan herhangi birini izleyin:

- Bir üretim emrini açın veya bunu ızgarada seçin. Sonra, Eylem Bölmesinde, **Görüntüle** sekmesinde, **Kalite yönetimi** grubunda, **Kalite emirleri** sayfasını açmak için **Kalite emirleri**'ni seçin. Burada, üretim emriyle ilişkili kalite emirlerini görüntüleyebilir, oluşturabilir veya güncelleştirebilirsiniz.
- Bir üretim emrini açın veya bunu ızgarada seçin. Ardından **Üretim emri** sekmesinde, **Üretim ayrıntıları** grubunda **Üretim rotası** sayfasını açmak için **Rota**'yı açın. Bir rota işlemiyle ilişkili kalite emirlerini görüntülemek için aşağıdaki adımlardan birini izleyin:

    - Izgaradaki hedef rota işlemini seçin. Sonra, Eylem Bölmesinde, **Sorgulamalar \> Kalite emirleri**'ni seçin.
    - **Operasyon Numarası** alanındaki değeri seçin. Böylece hedef rotanın **Üretim rotası** ayrıntıları sayfası açılır. **Genel** hızlı sekmesinde, **Kalite emri durumu** alanı, rota işlemi ile ilgili kalite emirlerinin durumunu gösterir.

- Bir üretim emrini açın ve **Genel** hızlı sekmesini seçin. **Kalite emri durumu** alanı, üretim emriyle ilişkili kalite emirlerinin durumunu gösterir.

### <a name="from-quarantine-orders"></a>Karantina emirlerinden

Karantina emirlerinizle ile ilgili kalite emirleriyle çalışmak için **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Karantina emirleri**'ne gidin ve aşağıdaki adımlardan herhangi birini izleyin:

- **Kalite emri durumu** sütunundaki değerleri gözden geçirin. Bu şekilde, ızgaradaki her karantina emriyle ilişkili tüm kalite emirlerinin durumunu öğrenebilirsiniz.
- Izgarada bir karantina siparişi seçin ve sonra Eylem Bölmesinde karantina emriyle ilişkili kalite emirlerini görüntülemek, oluşturmak veya güncelleştirmek için **Kalite emirleri**'ni seçin.

## <a name="advanced-actions-for-quality-orders"></a>Kalite emirleri için gelişmiş eylemler

Durumu yönetmek, belgeler üretmek ve ek ayrıntılar hakkında sorgulama yapmak için kalite emirleri üzerinde birkaç eylem yapabilirsiniz.

### <a name="reopen-a-quality-order"></a>Kalite emrini yeniden açma

Varsayılan olarak, bir kalite emrini doğruladıktan ve testler geçildikten sonra artık düzenleyemez veya güncelleştiremezsiniz. Ancak, bazı durumlarda, tamamlandıktan sonra kalite emrini yeniden açmanız gerekebilir.

Bir kalite emrini yeniden açmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.
1. Onaylanan kalite emrini açın veya bunu ızgarada seçin.
1. Eylem Bölmesinde **Kalite emrini yeniden aç**'ı seçin.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Kalite emri için analiz sertifikası oluşturma

CoA, bir kuruluşun kalite güvence ekibi tarafından oluşturulan bir rapordur. Bir ürünün belirli düzenlemeleri veya gereksinimleri karşıladığını doğrular. Müşterilerinizin veya coğrafyanızdaki yasal otoriteler, bir CoA hazırlanmasını gerekli kılabilir. Bunlar, sektörünüze ve işlediğiniz, satın aldığınız, ürettiğiniz veya sattığınız ürün türüne göre de gerekli olabilirler.

Supply Chain Management, kalite emrinden bir CoA oluşturmanıza olanak sağlar. Rapor, **Analiz raporu sertifikası** seçeneğinin *Evet* olarak ayarlandığı kalite emrindeki tüm testlerin sonuçlarını dahil eder. Bu seçenek, **Testler** sayfasında tanımladığınız teste bağlı olarak varsayılan değer olarak ayarlanabilir. Ancak, belirli bir kalite emri için belirli testlerdeki ayarı geçersiz kılabilirsiniz.

Bir kalite emri için CoA oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.
1. Adına CoA oluşturmak istediğiniz kalite emrini seçin.
1. Eylem Bölmesinde, **Sorgulamalar \> Analiz sertifikası**'nı seçin.
1. **Analiz sertifikası** sayfasında, Eylem Bölmesinde **Yeni**'yi seçin.
1. İsteğe bağlı: **İlgili kişi** alanında, sertifikanın gönderileceği ilgili kişiyi seçin.
1. Eylem Bölmesinde, **Yazdırma**'yı seçin.
1. **Analiz sertifikası** iletişim kutusunda, raporun nasıl yazdırılması gerektiğini tanımlayın. Raporu bir yazıcıya, ekrana, dosyaya veya e-postaya yazdırmak için **Tamam**'ı seçin.
1. Sayfaları kapatın.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Kalite emri için stoğu durdurma veya durdurmayı kaldırma

Kalite emri kalite ilişkilendirmeden otomatik olarak oluşturulduğunda, kalite ilişkisine atanan madde örnekleme, test edilmekte olan başvurunun tam stok miktarını durduracak şekilde konfigüre edilebilir. Madde örneklemeleri hakkında daha fazla bilgi için bkz. [Kalite yönetimi madde örnekleme](quality-item-sampling.md).

Tam durdurma kullanmıyorsanız veya el ile bir kalite emri oluşturuyorsanız, sistem kalite emrinde test edilmekte olan madde miktarı için otomatik olarak bir stok durdurma kaydı oluşturur. **Stok durdurma** sayfasında oluşturulan kayıtta, **Stok durdurma türü** alanı, *Kalite emri* olarak ayarlanır.

**Stok durdurma** sayfasında seçili bir kalite emrinin stok durdurma işlemini görüntülemek ve düzenlemek için, Eylem Bölmesinde **Sorgulamalar \> Stok durdurma**'yı seçin. Daha fazla bilgi için bkz. [Stok durdurma](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Kalite emrinin ayrıntılarını sorgulama

**Kalite emirleri** sayfasının Eylem Bölmesindeki aşağıdaki düğmeleri kullanarak, kalite emriyle ilgili daha fazla bilgi görüntüleyebilirsiniz:

- **Sorgulamalar \> Çalışma ayrıntıları** – Kalite emriyle ilişkili ambar çalışmasını görüntüleyebileceğiniz bir sayfa açar.
- **Sorgulamalar \>Uygunsuzluklar** – Kalite emriyle ilişkili uygunsuzlukları görüntüleyebileceğiniz bir sayfa açar.
- **Stok** – Bu menüdeki komutlar, tüm stok hareketleri genelinde ortaktır. Bunları kullanarak hareketler, eldeki stok, rezervasyonlar ve işaretleme gibi ayrıntıları görüntüleyebilir veya güncelleştirebilirsiniz.

### <a name="create-cases-related-to-quality-orders"></a>Kalite emirleriyle ilgili servis talepleri oluşturma

Kalite emirleriyle ilgili servis talepleri oluşturabilirsiniz. Bu şekilde, sorunlarla ilgili ayrıntıları izleyebilir ve bir çözüme erişebilirsiniz. Daha sonra, ek onaylar elde etmek veya belirli bir konu hakkında daha fazla bilgi almak için bir servis talebini önceden tanımlanmış bir iş işlemiyle yönlendirmek üzere durum yönetiminin iş akışı özelliklerini kullanabilirsiniz. Genel sorunlar için çözümlerle ilgili bir bilgi bankası oluşturmak için bilgi Bankası makaleleri özelliğini de kullanabilirsiniz.

## <a name="case-management-examples-for-quality-management"></a>Kalite yönetimi için servis talebi yönetimi örnekleri

### <a name="example-1"></a>Örnek 1

Gıda gibi düzenlenmeye tabi ürünlerin üretimiyle ilgili katı düzenlemeleri izlemesi gereken bir üretim şirketi için çalışıyorsunuz. Kalite emirleri, üretim sürecinde maddelerin kalitesiyle ilgili ayrıntıları kaydetmek ve izlemek için kullanılır. Kalite emri belirli testlerde başarısız oluyorsa, ekipmanla ilgili bir sorun olabilir. Servis talepleri, bir iş sürecini takip etmek ve sorunu doğru mühendislere iletmek ve böylece kök nedenin belirlenebilmesi için kullanılır. İş süreçlerini takip etmeyi daha kolay hale getirmek için, şirket kalite emirleri ve ekipman sorunlarıyla ilgili yaygın sorunların bilgi bankasını tutar.

### <a name="example-2"></a>Örnek 2

Çeşitli ülkeler ve bölgeler için özelleştirilebilecek ürünler sevk eden bir dağıtım şirketi için çalışıyorsunuz. Bazı müşterilerin, uyulması gereken katı koşulları vardır. Aksi takdirde ücretler ve iadeler ya da geri ödemeler tahakkuk edilebilir. Kalite emirlerini, müşteri gereksinimleriyle eşleşen her test ve sonuçlarla ilgili ayrıntıları izlemek için kullanırsınız. Servis talepleri, belge oluşturulmadan ve diğer sevkiyat belgeleriyle ilişkilendirilmeden önce CoA'nın ayrıntılarını gözden geçirmek ve onaylamak için kullanılır.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimi işlemleri](quality-management-processes.md)
- [Kalite testi](quality-tests.md)
- [Kalite test grupları](quality-test-groups.md)
- [Kalite ilişkileri](quality-associations.md)
- [Kalite yönetimi işlemleri](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

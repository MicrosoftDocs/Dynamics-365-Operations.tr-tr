---
title: Mühendislik ürünlerindeki değişiklikleri yönetme
description: Bu konu mühendislik değişikliği yönetimi hakkında bilgiler sağlar. Mühendislik değişikliği yönetimi, mühendislik ürünlerindeki değişiklikleri yönetmek için önerme, talepte bulunma ve değişiklik yapmadan değişiklikleri inceleme ve onaylama, mevcut hareketler üzerindeki etkilerini değerlendirme ve bunları takip etme gibi yapılandırılmış süreçler sağlar.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 314563e083434832ee04d9c19deb17cec221ae02
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2020
ms.locfileid: "4439755"
---
# <a name="manage-changes-to-engineering-products"></a>Mühendislik ürünlerindeki değişiklikleri yönetme

[!include [banner](../includes/banner.md)]

Mühendislik değişikliği yönetimi, mühendislik ürünlerindeki değişiklikleri yönetmek için yapılandırılmış süreçler sağlar. Değişiklik önermek ve istekte bulunmak için *mühendislik değişikliği isteği* işlemini kullanabilir ve sonra bu değişiklikleri gerçekten uygulamak için *mühendislik değişikliği* işlemini kullanabilirsiniz. Kullanıcılar mühendislik değişikliği istekleri veya mühendislik değişikliği emirleri oluşturabilir ve daha sonra bunları gözden geçirme ve onaylama, var olan işlemler üzerindeki etkilerini değerlendirme ve bunları izleme süreci uygulanır.

## <a name="engineering-change-requests"></a>Mühendislik değişiklik istekleri

Mühendislik değişikliği isteği süreci, şirketinizdeki tüm ilgili departmanlardan gelen değişiklik isteklerini yakalamanızı sağlar. Mühendis olarak veya Üretim, Kaynak Sağlama, Ambar ya da Satış departmanında çalışıyor olabilirsiniz: Değişiklik istemek için herkes mühendislik değişikliği isteğini kullanabilir. Bu değişiklik yeni bir ürüne yönelik bir fikir, var olan bir ürünle çalışırken keşfettiğiniz bir sorun, var olan bir ürünü veya başka bir şeyi geliştirmek için bir öneri olabilir.

Birisi değişiklik isteği gönderdikten sonra, *gözden geçirme ve onay* süreci, değişikliği kimin (örneğin, ürün sahibi) onaylaması gerektiğini tanımlayan bir iş akışı tarafından yönetilir.

Mühendislik değişikliği emirleri veya mühendislik değişikliği isteklerine yönelik bir iş akışı ayarlamak için **Mühendislik değişikliği yönetimi \> Mühendisli iş akışları**'na gidin. **Yeni**'yi seçin, iş akışının mühendislik değişikliği emirlerini veya mühendislik değişikliği isteklerini gözden geçirmek ve ardından iş akışını yapılandırmak için kullanılıp kullanılmayacağını seçin.

İş akışlarıyla ilgili daha fazla bilgi için bkz. [İş akışı sistemine genel bakış](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md). Ürün sahipleri hakkında daha fazla bilgi için bkz. [Ürün sahipleri](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Yeni mühendislik değişikliği isteği oluşturun

Bir mühendislik değişikliği isteği oluşturmak için aşağıdaki adımlardan birini izleyin.

- **Mühendislik değişikliği yönetimi \> Ortak \> Mühendislik değişikliği yönetimi \> Mühendislik değişiklikği istekleri**'ne gidin ve sonra Eylem Bölmesi'nden **Yeni**'yi seçin.
- Mevcut bir mühendislik ürününün **Ürün ayrıntıları** sayfasını açın. Daha sonra, Eylem Bölmesi'nde, **Mühendis** sekmesinde, **Mühendislik değişikliği yönetimi** grubunda, **Mühendislik değişikliği isteği \> Yeni mühendislik değişikliği isteği**'ni seçin.

Yeni bir değişiklik isteği oluşturulur. Şimdi, aşağıdaki alt bölümlerde açıklandığı gibi, her hızlı sekmedeki alanları ayarlayabilirsiniz.

#### <a name="general-fasttab"></a>Genel FastTab

**Genel** hızlı sekmesi, değişiklik isteğinin temel bir açıklamasını sağlamanıza olanak tanır. Aşağıdaki tabloda, bu hızlı sekmede kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Değişiklik talebi | Mühendislik değişikliği isteği için bir ad girin. |
| Unvan | İstekteki değişiklikleri kısaca açıklayan veya tanımlayan bir metin girin. |
| Öncelik | Değişikliğin önceliğinin ne kadar yüksek olduğunu belirtmek için bir değer seçin. Gerektiğinde şirketiniz için kullanılabilir değerleri özelleştirebilirsiniz. (Daha fazla bilgi için bkz. [Mühendislik değişikliği yönetimi için ortak değerleri oluşturma)](engineering-change-management-setup.md). |
| Kategori | İstediğiniz değişikliğin türünü açıklamak için bir değer seçin. Gerektiğinde şirketiniz için kullanılabilir değerleri özelleştirebilirsiniz. (Daha fazla bilgi için bkz. [Mühendislik değişikliği yönetimi için ortak değerleri oluşturma)](engineering-change-management-setup.md). |
| Önem derecesi | İsteğin uygulanmasıyla düzeltilmesi gereken sorunun önem derecesini belirtmek için bir değer seçin. Gerektiğinde şirketiniz için kullanılabilir değerleri özelleştirebilirsiniz. (Daha fazla bilgi için bkz. [Mühendislik değişikliği yönetimi için ortak değerleri oluşturma)](engineering-change-management-setup.md). |
| Talep eden | İsteği oluşturan kullanıcının adı. |
| Açık | İsteğin oluşturulduğu tarih. |
| Durum | İsteğin durumu. Bir istek ilk oluşturulduğunda, durumu *Oluşturuldu* olur. İstek onaylandığında durum *Onaylandı* olarak değiştirilir. İstek için ilgili bir değişiklik emri oluşturulduysa durum *Takip Edildi* olarak değişir. |
| Değişiklik emri | Değişiklik isteği bir değişiklik emriyle takip edildiyse değişiklik sıra numarası girilir. |

#### <a name="information-fasttab"></a>Bilgi hızlı sekmesi

**Bilgi** hızlı sekmesi, istek hakkında daha fazla bilgi eklemenize olanak sağlar.

Kılavuza satır eklemek için kılavuzun üzerindeki araç çubuğundan **Yeni**'yi seçin ve ardından aşağıdaki seçeneklerden birini belirleyin:

- **Dosya**: Dosya yükleyin.
- **Resim**: Resim dosyası yükleyin.
- **Not**: Doğrudan kılavuza bir not girin.
- **URL**: Doğrudan kılavuza bir URL girin.

Aşağıdaki tabloda, her satırdaki alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Oluşturulma tarihi ve saati | Satırın oluşturulduğu tarih ve saat. |
| Türü | Satırın oluşturulduğu bilgi türü (dosya, resim, not veya URL). |
| Tanım | Satır için açıklama girin. |
| Kısıtlama | Eklenen bilgilerin iç veya dış kaynaktan gelip gelmediğini gösteren bir değer. |
| İliştirilmiş | Seçili onay kutusu, satırın bir ek (dosya veya resim) içerdiğini gösterir. Eki indirmek için satırı seçin ve ardından kılavuzun üzerindeki araç çubuğundan **Aç**'ı seçin. |

#### <a name="products-fasttab"></a>Ürünler hızlı sekmesi

**Ürünler** hızlı sekmesi, değişiklik isteğinden etkilenen her ürünü listelemenizi sağlar. Kılavuza ürün eklemek veya ürünleri kaldırmak için araç çubuğundaki düğmeleri kullanabilirsiniz.

Bu liste yalnızca bilgi amaçlıdır. Bu nedenle, istediğiniz sayıda ilgili olduğunu düşündüğünüz ürün ekleyebilirsiniz. Var olan bir ürün için **Ürün ayrıntıları** sayfasından bir değişiklik isteği oluşturursanız istek kaydını kaydettikten sonra bu ürün, **Ürün** hızlı sekmesinde listelenir.

#### <a name="source-fasttab"></a>Kaynak hızlı sekmesi

**Kaynak** hızlı sekmesi, değişiklik isteğinin başlangıç noktasını izlemenizi sağlar. Örneğin, değişiklik isteğinin bir satış siparişinden oluşturulup oluşturulmadığını, kim tarafından oluşturulduğunu ve hangi şirkette oluşturulduğunu görmek için yararlıdır.

### <a name="evaluate-the-business-impact-of-a-change-request"></a>Değişiklik isteğinin iş üzerindeki etkisini değerlendirme

Bir değişiklik isteğini gözden geçirdiğinizde, bağımlılıkları arayabilirsiniz. Bu şekilde, istenen değişikliğin satış siparişleri, üretim emirleri ve eldeki stok gibi açık hareketler üzerindeki etkisini değerlendirebilirsiniz.

1. **Mühendislik değişikliği yönetimi \> Ortak \> Mühendislik değişikliği yönetimi \> Mühendislik değişikliği istekleri**'ne gidin.
1. Var olan bir değişiklik isteğini açın veya yeni bir değişiklik isteği oluşturmak için Eylem Bölmesi'nden **Yeni**'yi seçin.
1. Eylem Bölmesi'nde, **Değişiklik isteği** sekmesinde, **İş etkisi** grubunda aşağıdaki düğmelerden birini seçin:

    - **Ara**: Tüm açık hareketleri tarar ve ardından değişiklikten etkilenecek tüm hareketleri listeleyen **Açık hareketler üzerindeki iş etkisi** iletişim kutusunu açar.
    - **Önceki aramayı görüntüle**: Önceki aramanın sonuçlarını listeleyen **Açık hareketler üzerindeki iş etkisi** iletişim kutusunu açar. (Yeni bir arama yapılmaz.)

1. Değişiklik gerektiren sorunun kritik olduğu tespit edilirse, **Açık hareketler üzerindeki iş etkisi** iletişim kutusundaki araç çubuğunun düğmelerini kullanarak açık hareketleri engelleyebilir veya sorumlu kullanıcıya bildirebilirsiniz.

### <a name="create-a-change-order-from-a-change-request"></a>Değişiklik isteğinden değişiklik emri oluşturma

Mühendislik değişikliği isteğini gözden geçiren bir mühendis, doğrudan **Mühendislik değişikliği istekleri** sayfasından bir mühendislik değişikliği emri oluşturabilir. Eylem Bölmesi'nde, **Değişiklik isteği** sekmesinde, **Mühendislik değişikliği emri** grubunda, **Bağlantıyı ve ürünleri kopyala**'yı seçin.

## <a name="engineering-change-orders"></a>Mühendislik değişiklik emirleri

Mühendislik değişikliği emirleri, mühendislik ürünlerinde değişiklik yapmak için yapılandırılmış bir süreç sağlar. Mühendislikle ilgili verilerin bir kopyasını kullanarak değişiklik önerirsiniz. Gerçek ana veriler etkilenmez. Mühendislikle ilgili veriler hakkında daha fazla bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).

Onaylı bir mühendislik değişikliği isteğini temel alan bir mühendislik değişikliği emri oluşturabilirsiniz. Mühendisler de sıfırdan mühendislik değişikliği emirleri oluşturabilir. Aşağıdaki adımlardan herhangi birini izleyerek tek bir mühendislik değişikliği emrine birden çok ürünü dahil edebilirsiniz:

- Ürünleri el ile seçin.
- Ürün yapısında daha alt bölümlerde olan ürünleri (diğer bir deyişle alt öğeler) dahil etmek için ürün reçetesini kullanın.
- Ürün yapısında daha üst bölümlerde olan ürünleri (diğer bir deyişle üst öğeler) dahil etmek için kullanıldığı yerde aramayı kullanın.

Değişiklik teklifi tamamlandıktan sonra, gözden geçirme ve onay süreci bir iş akışı tarafından ele alınır. Öncelik ve önem derecesine göre farklı iş akışları ayarlayabilirsiniz.

Mühendislik değişikliği emirleri veya mühendislik değişikliği isteklerine yönelik bir iş akışı ayarlamak için **Mühendislik değişikliği yönetimi \> Mühendisli iş akışları**'na gidin. **Yeni**'yi seçin, iş akışının mühendislik değişikliği emirlerini veya mühendislik değişikliği isteklerini gözden geçirmek ve ardından iş akışını yapılandırmak için kullanılıp kullanılmayacağını seçin.

İş akışlarıyla ilgili daha fazla bilgi için bkz. [İş akışı sistemine genel bakış](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Aşağıda, mühendislik değişikliği emrini onaylaması gerekebilecek bazı genel paydaşlar verilmiştir:

- **Ürün sahipleri**: Ürün sahipleri hakkında daha fazla bilgi için bkz. [Ürün sahipleri](product-owner.md).
- **Sorumlu takım lideri**: Mühendislik değişikliği emrinin **Üst bilgi** görünümündeki **Mühendis** alanı, mühendislik değişikliği emrini oluşturan mühendisi gösterir. Mühendis sistemde tanımlı bir takıma aitse **Sorumlu** alanı, o takımın liderini gösterir.
- **Finans departmanı**: Finans departmanı, değişikliğin yüksek maliyetlere yol açtığı durumları gözden geçirmek zorunda kalabilir.

Mühendislik değişikliği emrinin onaylandıktan sonra iş akışı kapsamında doğrudan işlenmesini veya işlemenin daha sonra el ile bir adım olarak mı yapılacağını seçebilirsiniz. Bir mühendislik değişikliği emrinin işlenmesi sırasında, gerçek ürüne ilişkin mühendislik verileri güncelleştirilir.

Bir değişiklik isteğini gözden geçirirken Eylem Bölmesi'nde, **Değişiklik isteği** sekmesinde, **İş etkisi** grubunda, önerilen değişikliğin satış siparişleri, üretim emirleri ve eldeki stok gibi açık hareketler üzerindeki etkisini değerlendirmek için **Ara**'yı seçin. Sonuçlar, etkilenen hareketleri seçip daha fazla bilgi görüntülemek, sorumlu kullanıcıyı bilgilendirmek veya hareketi engellemek için araç çubuğundaki komutları kullanabileceğiniz **Açık hareketler üzerindeki iş etkisi** iletişim kutusunda gösterilir.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Mühendislik şirketi veya operasyonel şirketlerde mühendislik değişikliği emirleri

[Mühendislik şirketleri ve veri sahipliği kuralları](engineering-org-data-ownership-rules.md) bölümünde açıklandığı gibi, değiştirebileceğiniz ürün verileri, çalıştığınız tüzel kişiliğin türüne (mühendislik şirketi veya operasyonel şirket) bağlı olarak değişir. Veri sahipliği kuralları, mühendislik değişikliği emirlerine de uygulanır. Bu nedenle, mühendislik değişikliği emrini oluşturduğunuz tüzel kişiliğe bağlı olarak farklı türde değişiklikler yapılabilir. Burada bazı örnekler verilmiştir:

- Bir **mühendislik şirketindeki** mühendislik değişikliği emirleri durumunda, mühendislik verilerinde temel değişiklikler yapabilirsiniz. Örneğin, bir ürünün yeni sürümlerini oluşturabilir, ürün reçetesi üzerinden ürün yapısını değiştirebilir ve mühendislik özniteliği değerlerini değiştirebilirsiniz. Etkilenen her ürün için **Etki** alanında aşağıdaki değerlerden birini seçin:

    - **Hiçbiri**: Var olan ürün sürümünü güncelleştirin (sürüm içi güncelleştirme).
    - **Yeni sürüm**: Seçili ürün sürümünü temel alan yeni bir sürüm oluşturun.
    - **Yeni ürün**: Seçili ürün sürümüne dayalı tamamen yeni bir ürün veya ürün varyantı oluşturun.

- Bir **operasyonel şirketteki** mühendislik değişikliği emirleri durumunda, ürünün lojistik verilerini değiştirebilirsiniz. Örneğin, mevcut ürün reçetesini kaynak kullanımı ayarlarıyla zenginleştirebilir, yerel rotalar veya yerel ürün reçeteleri ekleyebilir ve yerel ambalaj malzemeleri, yağlama sıvıları veya yerel dilde talimatlar için yeni ürün reçetesi satırları ekleyerek ürün reçetesini zenginleştirebilirsiniz. Kullanıcıların operasyonel şirkette yaptıkları zenginleştirmeler, mühendislik şirketinden yeni güncellemeler gönderildiğinde korunur. Daha fazla bilgi için bkz. [Mühendislik şirketleri ve veri sahipliği kuralları](engineering-org-data-ownership-rules.md).

    Mühendislik değişikliği emirleri mühendislik şirketinde işlendiğinde, ürünler yalnızca mühendislik şirketinde oluşturulur ve/veya güncelleştirilir. Bu nedenle, ürün ana verilerinin de güncelleştirilmesi gerekiyorsa ürünleri operasyonel şirketlere de serbest bırakmanız gerekir.

- Ürünleri doğrudan mühendislik değişikliği emrinden serbest bırakabilirsiniz. Değişiklik emrini açın ve sonra Eylem bölmesinden **Değişiklik emri** sekmesinde, **Ürün serbest bırakmaları** grubunda **Ürün yapısını serbest bırakma** öğesini seçin. Süreç, **Serbest bırakılan ürünler** sayfasından ürünleri serbest bıraktığınızda olduğu gibi çalışır. Daha fazla bilgi için bkz. [Ürün yapılarını serbest bırakma](release-product-structure.md).
- Aşağıdaki etkenlere bağlı olarak, mühendislik değişikliği emirlerinden ürünlerin otomatik olarak serbest bırakılmasını sağlayabilirsiniz:

    - Ürünlerin daha önce serbest bırakıldığı şirketlere yeniden serbest bırakmalar. Önceki tüm sürümleri taramak için **Ara**'yı ve sonuçları görüntülemek için **Görüntüle**'yi seçin. **Görünüm** sayfası önceki ürün serbest bırakmalarını gösterir ve yeniden serbest bırakmak istediğiniz ürünleri seçebilirsiniz. Daha sonra **Görünüm** sayfasını kapatın ve seçili ürünleri yeniden serbest bırakmak için **İşle**'yi seçin.
    - Mühendislik ürünü kategorisinin serbest bırakma denetimindeki otomatik serbest bırakma ayarları. Bu serbest bırakmayı iş akışının bir parçası olarak yapabilirsiniz. **Serbest bırakma teklifi toplama** bloğu kullanıldığında, serbest bırakma teklifi yeniden serbest bırakma teklifleriyle doldurulur (önceki liste maddesine bakın) ve mühendislik ürünü kategorisinin serbest bırakma denetiminde **Otomatik serbest bırak** onay kutusu seçiliyse ürünler şirketlere serbest bırakılır. Önceki liste maddesinde açıklandığı gibi sonuçları görüntülemek için **Görüntüle**'yi seçebilirsiniz. Ürünler, **işlem serbest bırakma teklifi** bloğu kullanıldığında da serbest bırakılacaktır. İş akışının bir parçası olarak yalnızca serbest bırakma teklifini toplamayı seçerseniz önceki liste maddesinde açıklandığı gibi **İşle**'yi seçerek serbest bırakma işlemini el ile başlatabilirsiniz.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Mühendislik değişikliği isteğinin bir mühendislik değişikliği emri ile takibi

Bir mühendislik değişikliği isteği onaylanır onaylanmaz, bir mühendislik değişikliği emri ile takip edebilirsiniz. Birden çok mühendislik değişikliği isteğini tek bir mühendislik değişikliği emrinde birleştirebilirsiniz. Tek bir mühendislik değişikliği emri birden fazla ürün bile içerebilir. (Genellikle, aynı değişiklik birden çok ürüne uygulanması gerektiğinde bu yaklaşımı kullanın.) Ancak, tek bir mühendislik değişikliği isteğinden birden çok mühendislik değişikliği emri oluşturamazsınız.

Değişiklik emri üzerinden değişiklik isteğini izlemek için değişiklik isteğini açın ve ardından Eylem Bölmesi'nden **Değişiklik emri** sekmesinde, **Mühendislik değişikliği emri** grubunda **Bağlantıyı ve ürünleri kopyala**'yı seçin. Daha sonra değişiklik isteğini bağlamak için var olan bir mühendislik değişikliği emrini seçebilir veya bu özel istek için yeni bir mühendislik değişikliği emri oluşturabilirsiniz.

## <a name="engineering-change-order-report"></a>Mühendislik değişiklik emri raporu

Mühendislik değişikliği emri raporları, bir mühendislik değişikliği emrinde yapılan değişiklikleri açıklar. İnceleme ve onay sürecinde ve sonrasında yararlıdır.

Bir mühendislik değişikliği emri raporunu görüntülemek için ilgili değişiklik emrini açın ve ardından Eylem Bölmesi'nden **Değişiklik emri** sekmesinde, **Görüntüle** grubunda **Mühendislik değişikliği emri raporu**'nu seçin.

## <a name="fields-on-an-engineering-change-order"></a>Mühendislik değişikliği emrindeki alanlar

Mühendislik değişikliği emirlerindeki alanların çoğu, serbest bırakılan ürünler, mühendislik sürümleri, belgeler, ürün reçeteleri (satırlar) ve rotalara (işlemler) yönelik alanlarla aynıdır. Ancak, aşağıdaki tablodaki alanlar değişiklik emirlerine özeldir.

| Alan | Tanım |
|---|---|
| Mühendislik değişiklik nedenleri | Etkilenen ürünü değiştirme nedenini seçin. |
| Değişiklik açıklaması | Değişiklik için açıklama girin. |
| Gerekli özel alet | Değişikliği uygulamak için özel takımın gerekli olup olmadığını belirtin. |
| Mühendislik malzemesi değerlendirmesi | Değişiklik uygulandığında üretilen atıklar için bir malzeme değerlendirme kodu seçin. |
| Müşteri onayı gerekli | Değişiklik uygulanmadan önce müşteri onayı gerekip gerekmediğini belirtin. |
| Alınan müşteri onayı | Müşteri onayının durumunu belirtin. |
| Çevre, sağlık ve güvenlik | Çevre, sağlık ve güvenlik kurallarının değişiklik için geçerli olup olmadığını belirtin. Evetse geçerli kuralları seçebilirsiniz. |

Değişiklik bilgilerini etkilenen ürünler arasında kopyalamak için **Bilgileri koru/kopyala** düğmesini kullanabilirsiniz.

---
title: Kalite ve uygunsuzluk yönetimine genel bakış
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite ve uyumsuzluk yönetimi özelliklerini tanıtır ve bunların tedarik zincirindeki ürün kalitesini geliştirmeye nasıl yardımcı olacağını açıklamaktadır.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11574"
- intro-internal
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bb4bcb7f554c22b4e1ab1b41867bd2d3dcca4d4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985532"
---
# <a name="quality-and-nonconformance-management-overview"></a>Kalite ve uygunsuzluk yönetimine genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite ve uyumsuzluk yönetimi özelliklerini tanıtır ve bunların tedarik zincirindeki ürün kalitesini geliştirmeye nasıl yardımcı olacağını açıklamaktadır.

Kalite güvencesi, ürün testlerini ve uyumsuz malzemelerin yönetimini kapsar. Kalite yönetimi işlemleri, tedarik zinciri içinde yüksek düzeyde ürün kalitesi sağlanmasına yardımcı olur. Bu işlemler ayrıca tedarik zinciri süreçlerini en iyi duruma getirme ve müşteri memnuniyetini artırmaya yardımcı olur. Kalite yönetimi, uyumsuz ürünler ile ilgilenirken , bu ürünlerin kendi başlangıç noktalarını dikkate almadan işleyecek döngü sürelerini yönetmenize yardımcı olabilir. Tanılama sonuçlarını düzeltme görevlerine bağlayabilirsiniz. Sistem sorunları düzeltmek için görevler planlayabilir ve böylece bu sorunların gelecekte yinelenmesini önlemeye yardımcı olur. Kalite yönetimi ayrıca sorunları (dahili problemler dahil) sorun türüne göre izlemenize ve hem kısa vadeli hem de uzun vadeli çözümler belirlemenize olanak sağlar. Anahtar performans göstergeleri (APG) ile ilgili istatistikler, daha önceden oluşan uygunsuzluk sorunları ve bunları düzeltmek için kullanılan çözümler hakkında bir anlayış sağlar. Daha önceden alınan kalite ölçülerinin etkilerini incelemek ve ileride kullanılmaya uygun önlemleri belirlemek için geçmişe dönük verileri kullanabilirsiniz.

Kalite Yönetimi, uyumsuz ürünler,, kendi başlangıç noktalarını dikkate almadan işleyecek döngü sürelerini yönetmenize yardımcı olabilir. Tanı türleri düzeltme raporlaması ile bağlantılı olduğundan, Supply Chain Management sorunları düzeltmek ve oluşmalarını önlemek için görevleri zamanlayabilir.

Uygunsuzluğu yönetmek için daha fazla işlevselliğe ek olarak, Kalite Yönetimi sorun türüne göre sorunları (hatta dahili sorunlar olduğunda bile) izlemek için ve çözümleri kısa vadeli veya uzun vadeli olarak tanımlamak için işlev içerir. Anahtar performans göstergeleri (APG) ile ilgili istatistikler, önceki uygunsuzluk sorunlarının geçmişi ve bunları düzeltmek için kullanılan çözümler hakkında bir anlayış sağlar. Önceki kalite ölçülerinin geçmişteki etkilerini incelemek ve ileride kullanılmaya uygun önlemleri belirlemek için geçmişe dönük verileri kullanabilirsiniz.

Bir kalite ilişkisi ayarladığınızda, Supply Chain Management çeşitli iş süreçleri, olaylar ve koşullar için kalite emirleri oluşturabilir. Kalite ilişkisi, belirli bir madde, belirli bir madde grubu veya tüm öğeleri kapsayabilir.

## <a name="examples-of-the-use-of-quality-management"></a>Kalite yönetimi kullanımına örnekler

Kalite Yönetimi esnektir ve tedarik zinciri işlemlerinin belirli düzeylerdeki gereksinimlerini karşılamak için çeşitli şekillerde uygulanabilir. Aşağıdaki örneklerde, bu özelliklerin olası kullanımı gösterilmektedir:

- Önceden tanımlanmış ölçütlere (örneğin belirli bir satıcı satınalma siparişinden ambar kaydı gerçekleştiğinde) dayalı bir kalite kontrol işlemini otomatik olarak başlatın.
- Onaylanmamış stokun kullanılmasını engellemek için inceleme sırasında stoku bloklayın(Tüm satınalma siparişi miktarlarını engelleme).
- Madde örneklemeyi kalite ilişkilendirmesinin bir parçası olarak, denetlenmesi gereken geçerli fiziksel stok miktarını tanımlamak için kullanın. Örnekleme miktar, yüzde veya tam plaka tabanlı olabilir.
- Kısmi alış irsaliyeleri için kalite emirleri oluşturun. Bir siparişten fiziksel olarak alına miktara bağlı olarak oluşturulan bir kalite emri oluşturmak için **Madde örnekleme** sayfasındaki **Güncelleştirilen miktar başına** onay kutusunu seçmelisiniz.
- Minimum, maksimum ve hedef test değerleri içeren test türleri oluşturun ve doğrulama sonuçları önceden tanımlanmış olan niteliğe karşı nicelik sınamaları gerçekleştirin.
- Kalite Ölçüm toleranslarını kontrol etmek için bir kabul edilebilir kalite düzeyi (AQL) belirtin.
- Denetleme işlemi için gereken test alanı ve test aletleri gibi kaynakları belirtin.

> [!NOTE]
> _Ambar işlemleri için kalite yöntemleri_ özelliği, kalite yönetimi özelliğinin yeteneklerini genişletir. Bu özelliği kullanıyorsanız, kalite yönetiminin etkinleştirildiğinde nasıl çalıştığını gösteren örnekler için [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)'ne bakın.

## <a name="controlling-the-quality-management-process"></a>Kalite yönetimi işlemi denetleme

Kalite yönetimi sürecinin kontrol edebilmeniz için bazı yollar şunlardır:

- Giden işlemler için "ürün alış irsaliyesi" veya giden işlemler için "ürün toplama" gibi tetik noktalarına dayanan kalite emirleri oluşturun.
- Test sonuçlarını belgeleyin ve sonuçların oluşturulan test ölçütleri ve AQL'leri karşıladığını belirleyin.
- Ayrıntılı ürün belirtimleri ve denetleme işlemi sırasında raporlamanın bir parçası olarak kullanıcıya özel notlar için belge yönetimini kullanın.
- Uyumsuz ürünleri koruyun ve bir sorunun asıl nedenini izlemek için ek uygunsuzluk bilgileriyle bu ürünler arasında ilişki kurun.
- Bir uygunsuzluk yönetme maliyetini belgeleyin. Bu maliyet uygunsuzluğu düzeltmek için gereken maddeler (yedek parçalar gibi), sair giderler ve zaman tablosu saatlerini kapsayabilir.
- Kalite emirleri ile bağlantılı düzeltmeyi kullanarak hata düzeltme işlemleri zamanlayın.

[![Kalite yönetimi süreci.](media/quality-management-process-diagram.png)](media/quality-management-process-diagram.png)

## <a name="product-testing-and-quality-orders"></a>Ürün testi ve kalite emirleri

Ürün testleri genel olarak kalite kontrol olarak adlandırılır ve kalite emirlerini kullanır. Kalite kontrol işlevselliğini kullanarak aşağıdakileri yapabilirsiniz:

- Malzeme için gerçekleştirilmesi gereken testleri tanımlayın. Bu testler kalite belirtimleri, uygun test aletleri, testi anlatan belgeler ve örnek alma planı ile kabul edilebilir AQL'leri kapsar.
- Bir satınalma veya üretim emri gibi belirli bir emir veya belirli bir stok miktarı için gerçekleştirilmesi gereken testleri tanımlayan bir kalite emri oluşturun. Kalite yönergelerini temel alarak el ile bir kalite emri oluşturabilir veya kalite emrini otomatik şekilde oluşturabilirsiniz.
- Gelen veya giden malzemelerin test gereksinimlerini tanımlayan bir kalite emrini otomatik şekilde oluşturmak üzere, her iş sürecindeki satınalma, karantina, üretim veya satış emirleriyle ilişkili kalite yönergelerini tanımlayın.
- Bir kalite emri dahilindeki test sonuçlarını kaydedin, test sonuçlarını AQL ile karşılaştırarak doğrulayın ve test sonuçlarını görüntüleyen bir analiz sertifikası yazdırın.

## <a name="nonconformance"></a>Uyumsuzluk

Uygunsuzluk, bir öğenin bir kalite problemine sahip olduğunu açıklar. Uygunsuzluk işlemi, malzemenin miktarını problem kaynağını, problem tipini ve açıklayıcı notları tanımlayan bir uyumsuzluk emri oluşturmanıza izin verir. Uygunsuz malzemenin analizini kolaylaştırmak üzere problem tiplerine yönelik bir sınıflandırmayı tanımlayabilirsiniz. Uygunsuzluk etiketi ve uygunsuz malzeme düzenlemeye kılavuzluk etmek için bir uygunsuzluk raporu da yazdırabilirsiniz. Örneğin, etiket ve rapor **Kullanılamaz** veya **sınırlı kullanım** koşulu belirtebilir.

Aşağıdaki tabloda, altı varsayılan uygunsuzluk türlerini listeler ve her türü için kaydedilmesi gereken bilgiler açıklanır.

| Uyumsuzluk tipi | Kaynak bilgileri |
|---|---|
| Müşteri | Bir satış siparişi hareketinin müşteri hesap numarası, satış siparişi numarası veya lot numarası. Örneğin, uygunsuzluk belirli bir satış siparişi sevkiyatıyla veya ürün kalitesine ilişkin müşteri geri bildirimiyle ilgili olabilir. |
| Servis isteği | Bir satış siparişi hareketinin müşteri hesap numarası, satış siparişi numarası veya lot numarası. Örneğin, uygunsuzluk belirli bir satış siparişi sevkiyatıyla veya madde kalitesine ilişkin müşteri şikayetiyle ilgili olabilir. |
| Satıcı | Bir satınalma emri hareketinin satıcı hesap numarası, satınalma emri numarası veya lot numarası. Örneğin, uygunsuzluk bir satınalma emri girişi veya satıcının tedarik ettiği bir parçayla ilgili kaygısı hakkında olabilir. |
| Üretim | Bir üretim emri hareketinin üretim emri numarası veya lot numarası. Örneğin, uygunsuzluk üretilen belirli bir toplu işle ilgili olabilir. |
| İç | Bir kalite emri hareketinin kalite emri numarası veya lot numarası. Örneğin, uygunsuzluk kalite emrinin bir parçası olarak gerçekleştirilen testler veya bir çalışanın ürün kalitesiyle ilgili kaygısı hakkında olabilir. |
| Ortak ürün üretimi | Toplu üretim emirleri için ilgili ortak ürün üretim emri uygunsuzluğu. |

Uygunsuzluklar bir sorun türü ile ilişkilendirilmiş. Sorun türleri hangi sorun türlerinin uygunsuzluk türü ile ilişkilendirilebileceğini belirttiğiniz **Sorun türleri** sayfasında tanımlanır. Sorun türleri üzerinde tanımlanan. Örneğin, **servis talepleri** için sorun tipleri müşteri şikayetlerinin sınıflandırılmasını yansıtırken, **Dahili** uyumsuzluk için sorun tipleri kusur kodlarının sınıflandırılmasını temsil edebilir.

Yeni bir uygunsuzluk oluşturduğunuzda, uygunsuzluk türünü ve sorun türünü seçin. İlk onay durumu **Yeni**, eylem için bir isteği temsil eder. Bir sonraki adım, uyumsuzluk için işlem yapacağınızı veya yapmayacağınızı göstermek için onaylama durumunu **Onaylandı** veya **Reddedildi** şeklinde değiştirmektir. Ayrıca bir uyumsuzluğu işinizin bittiğini gösterecek şekilde kapatabilir (ayrı bir onay kutusu seçerek) veya ek değerlendirmenin gerektiğini gösterecek şekilde yeniden açabilirsiniz.

Bir belge iliştirerek, bir uygunsuzluk için yorumlar girebilirsiniz. **Belge türü** sayfasını kullanarak uygunsuzluklar için benzersiz bir dosya türü tanımlamak iyi bir fikirdir. Daha sonra **Rapor Kurulumu** sayfasını kullanarak bu belge türü için yorumların uygunsuzluk raporunda ve uygunsuzluk etiketinde yazdırılıp yazdırılmayacağını tanımlayabilirsiniz. Uyum raporu ve uyumsuzluk etiketi, malzeme elden çıkarmaya yardımcı olabilir. Uyumsuzlukla ilgili seçim ölçütlerini temel alarak, rapor ve etiketleri oluşturabilirsiniz. Bu ölçütler, uygunsuzluk numarası, madde, müşteri, satıcı ve durumu içerir.

Uygunsuzluk raporu, uygunsuzluk numarası, madde ve sorun türünü görüntüler. Rapor kurulumu ilkenize bağlı olarak, rapor, uygunsuzlukla ilgili notları da görüntüleyebilir. Uygunsuzluk etiketi benzer bilgileri görüntüler ve kusurlu malzemenin elden çıkarılmasını yönlendirmek için uyumsuzluğa atadığınız karantina bölgesi ve türünü (**Sınırlı kullanım** veya **Kullanılamaz** gibi) içerir.

## <a name="approved-nonconformance"></a>Onaylanan uygunsuzluk

İsteğe bağlı olarak, onaylanan bir uyumsuzluk için bir veya daha fazla ilgili operasyon tanımlayabilirsiniz. İlgili işlem, gerçekleştirilmesi gereken işi açıklar ve tanımladığınız kalite işlemlerinin listesi ile işin nedeni hakkında açıklayıcı bir metin içerir. Bir operasyonu tanımladıktan sonra, isteğe bağlı olarak işi gerçekleştirmek için gereken sair giderleri, maddeleri ve zaman tablosu çalışma saat sayısı tanımlayabilirsiniz. İlgili operasyon için hesaplanan maliyetler gösterilir ve uyumsuzluk için toplam hesaplanan maliyetler gösterilir. Hesaplanan maliyetler ve bunlarla ilişkili ayrıntılar (maddeler, çalışma saat sayısı ve sair giderler hakkında) referans niteliğinde bilgilerdir ve bunlar yalnızca kalite yönetimi işlevi çerçevesinde kullanılır.

İsteğe bağlı olarak, önce kalite emirlerini sorgulayıp daha sonra yeni kalite emrini oluşturarak, uyumsuzluktan bir kalite emri oluşturabilirsiniz. Örneğin, bir kalite emri kusurlu malzemeyi test etme (veya yeniden test etme) gereksinimini tanımlayabilir. Yeni oluşturulan kalite emri, ilk uyumsuzlukla olan bağlantıyı görüntüler.

İsteğe bağlı olarak bir uyumsuzluğu başka bir uyumsuzluğa bağlayabilir ve mevcut bir uyumsuzluktan yeni bir uyumsuzluk oluşturabilirsiniz. Örneğin, bağlantı, kalite sorunlarının birbirine bağlı olmasını sergileyebilir.

## <a name="correction-handling"></a>Düzeltme işleme

**Düzeltmeler** sayfası düzeltilmesi gereken uygunsuzluklar listesi oluşturmanıza olanak sağlar. Her düzeltme maddesi, sorunun bulunabilmesini sağlayan tanı türüyle ilişkilendirilmiştir. **Düzeltmeler** sayfası, düzeltici eylemi kimin ve ne zaman gerçekleştirmesi gerektiği hakkında bilgiler de içerir. Düzeltmeye bir belge ekleyerek sorunun ayrıntılarını ve gerekli düzeltici eylemi açıklayabilirsiniz. Uygunsuzluk gönderildikten veya düzeltildikten sonra, **Tamamlandı** seçeneğini seçerek düzeltme öğesini "kapatırsınız". Ayrıca, çözümün kısa vadeli bir çözüm olduğunu da gösterebilirsiniz.

**belge türünü** sayfasını kullanarak düzeltmeler için benzersiz bir dosya türü tanımlamak iyi bir fikirdir. Daha sonra **Rapor Kurulumu** sayfasını kullanarak bu belge türü için yorumların düzeltme raporunda yazdırıldığını tanımlayabilirsiniz. Yazdırılan düzeltme raporu uygunsuzluk ve ilişkili uygunsuzluk notları hakkında bilgi görüntüler. Rapor ayrıca tanı türü ve ilgili düzeltme notları gibi düzeltme bilgileri içerir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Stok durdurma](inventory-blocking.md)
- [Karantina emirleri](quarantine-orders.md)
- [Malların kalitesini denetleme](tasks/inspect-quality-goods.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

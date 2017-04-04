---
title: "Kalite yönetimi işlemleri"
description: "Bu makalede, uyumsuz ürünler için kalite yönetimi süreci hakkında bilgiler verilmektedir. Makale, kalite kontrol işlevlerini nasıl kullanacağınızı, uygunsuzlukların nasıl tanımlanıp korunacağını ve düzeltmelerin nasıl yapılacağını açıklamaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-10-30 12 - 53 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11574
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 2deec6d262e87daf4704ce21ce64546f9c9d638b
ms.lasthandoff: 03/30/2017


---

# <a name="quality-management-processes"></a>Kalite yönetimi işlemleri

Bu makalede, uyumsuz ürünler için kalite yönetimi süreci hakkında bilgiler verilmektedir. Makale, kalite kontrol işlevlerini nasıl kullanacağınızı, uygunsuzlukların nasıl tanımlanıp korunacağını ve düzeltmelerin nasıl yapılacağını açıklamaktadır.

Kalite güvencesi, ürün testlerini ve uyumsuz malzemelerin yönetimini kapsar. Kalite yönetimi işlemleri, tedarik zinciri içinde yüksek düzeyde ürün kalitesi sağlanmasına yardımcı olur. Bu işlemler ayrıca tedarik zinciri süreçlerini en iyi duruma getirme ve müşteri memnuniyetini artırmaya yardımcı olur. Kalite yönetimi, uyumsuz ürünler ile ilgilenirken , bu ürünlerin kendi başlangıç noktalarını dikkate almadan işleyecek döngü sürelerini yönetmenize yardımcı olabilir. Tanılama sonuçlarını düzeltme görevlerine bağlayabilirsiniz. Sistem sorunlarını düzeltmek ve bu nedenle yinelenmeleri bu sorunların gelecekte oluşmasını sağlamak için görevleri zamanlayabilirsiniz. Kalite Yönetimi de sağlayan sorunun türüne göre (iç sorunlar da dahil olmak üzere) sorunları izlemek ve çözümler kısa vadeli veya uzun vadeli olarak tanımlamanıza olanak sağlar. Anahtar performans göstergeleri (APG) ile ilgili istatistikler, daha önceden oluşan uygunsuzluk sorunları ve bunları düzeltmek için kullanılan çözümler hakkında bir anlayış sağlar. Daha önceden alınan kalite ölçülerinin etkilerini incelemek ve ileride kullanılmaya uygun önlemleri belirlemek için geçmişe dönük verileri kullanabilirsiniz.

## <a name="controlling-the-quality-management-process"></a>Kalite yönetimi işlemi denetleme
Kalite yönetimi sürecinin kontrol edebilmeniz için bazı yollar şunlardır:

-   Giden işlemler için "ürün alış irsaliyesi" veya giden işlemler için "ürün toplama" gibi tetik noktalarına dayanan kalite emirleri oluşturun.
-   Test sonuçlarını belgeleyin ve sonuçların oluşturulan test ölçütleri ve kabul edilebilir kalite düzeylerini karşıladığını belirleyin.
-   Ayrıntılı ürün belirtimleri ve denetleme işlemi sırasında raporlamanın bir parçası olarak kullanıcıya özel notlar için belge yönetimini kullanın.
-   Uyumsuz ürünleri koruyun ve bir sorunun asıl nedenini izlemek için ek uygunsuzluk bilgileriyle bu ürünler arasında ilişki kurun.
-   Bir uygunsuzluk yönetme maliyetini belgeleyin. Bu maliyet uygunsuzluğu düzeltmek için gereken maddeler (yedek parçalar gibi), sair giderler ve zaman tablosu saatlerini kapsayabilir.
-   Kalite emirleri ile bağlantılı düzeltmeyi kullanarak hata düzeltme işlemleri zamanlayın.

[![Kalite yönetimi süreci](./media/quality-management-process-diagram.png)](./media/quality-management-process-diagram.png)  

## <a name="product-testing-and-quality-orders"></a>Ürün testi ve kalite emirleri
Ürün testleri genel olarak kalite kontrol olarak adlandırılır ve kalite emirlerini kullanır. Kalite kontrol işlevselliğini kullanarak aşağıdakileri yapabilirsiniz:

-   Malzeme için gerçekleştirilmesi gereken testleri tanımlayın. Bu testler kalite belirtimleri, uygun test aletleri, testi anlatan belgeler ve örnek alma planı ile kabul edilebilir kalite düzeylerini (AQL) kapsar.
-   Bir satınalma veya üretim emri gibi belirli bir emir veya belirli bir stok miktarı için gerçekleştirilmesi gereken testleri tanımlayan bir kalite emri oluşturun. Kalite yönergelerini temel alarak el ile bir kalite emri oluşturabilir veya kalite emrini otomatik şekilde oluşturabilirsiniz.
-   Gelen veya giden malzemelerin test gereksinimlerini tanımlayan bir kalite emrini otomatik şekilde oluşturmak üzere, her iş sürecindeki satınalma, karantina, üretim veya satış emirleriyle ilişkili kalite yönergelerini tanımlayın.
-   Bir kalite emri dahilindeki test sonuçlarını kaydedin, test sonuçlarını AQL ile karşılaştırarak doğrulayın ve test sonuçlarını görüntüleyen bir analiz sertifikası yazdırın.

## <a name="nonconformance"></a>Uyumsuzluk
Bir nonconformance bir kalite problem.* * içeren bir öğe tanımlayan ** nonconformance işlemi, uyumsuz malzeme, sorunun kaynağı, sorunun türü ve açıklayıcı Notlar miktarını açıklayan bir nonconformance sipariş oluşturmanıza olanak sağlar. Uygunsuz malzemenin analizini kolaylaştırmak üzere problem tiplerine yönelik bir sınıflandırmayı tanımlayabilirsiniz. Uygunsuzluk etiketi ve uygunsuz malzeme düzenlemeye kılavuzluk etmek için bir uygunsuzluk raporu da yazdırabilirsiniz. Örneğin, etiket ve rapor** Kullanılamaz** veya **sınırlı kullanım** koşulu belirtebilir. Aşağıdaki tabloda, altı varsayılan uygunsuzluk türlerini listeler ve her türü için kaydedilmesi gereken bilgiler açıklanır.

| Uyumsuzluk tipi   | Kaynak bilgileri                                                                                                                                                                                                                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Müşteri              | Bir satış emri hareketinin müşteri hesap numarası, satış emri numarası veya lot numarası. Örneğin, uygunsuzluk belirli bir satış emri sevkiyatıyla veya ürün kalitesine ilişkin müşteri geri bildirimiyle ilgili olabilir.       |
| Servis isteği       | Bir satış emri hareketinin müşteri hesap numarası, satış emri numarası veya lot numarası. Örneğin, uygunsuzluk belirli bir satış emri sevkiyatıyla veya madde kalitesine ilişkin müşteri şikayetiyle ilgili olabilir.     |
| Satıcı                | Bir satınalma emri hareketinin satıcı hesap numarası, satınalma emri numarası veya lot numarası. Örneğin, uygunsuzluk bir satınalma emri girişi veya satıcının tedarik ettiği bir parçayla ilgili kaygısı hakkında olabilir. |
| Üretim            | Bir üretim emri hareketinin üretim emri numarası veya lot numarası. Örneğin, uygunsuzluk üretilen belirli bir toplu işle ilgili olabilir.                                                                      |
| İç              | Bir kalite emri hareketinin kalite emri numarası veya lot numarası. Örneğin, uygunsuzluk kalite emrinin bir parçası olarak gerçekleştirilen testler veya bir çalışanın ürün kalitesiyle ilgili kaygısı hakkında olabilir.     |
| Ortak ürün üretimi | Toplu üretim emirleri için ilgili ortak ürün üretim emri uygunsuzluğu.                                                                                                                                                    |

Uygunsuzluklar bir sorun türü ile ilişkilendirilmiş. Sorun türleri hangi sorun türlerinin uygunsuzluk türü ile ilişkilendirilebileceğini belirttiğiniz **Sorun türleri** sayfasında tanımlanır. Sorun türleri üzerinde tanımlanan. Örneğin, sorun türleri için nonconformances **hizmet isteği** sorun türleri için nonconformances ise, tür müşteri şikayetlerini sınıflandırılması yansıtmak ** dahili ** türü bir sınıflandırma hatasını kodları göstermek. 

Yeni bir uygunsuzluk oluşturduğunuzda, uygunsuzluk türünü ve sorun türünü seçin. İlk onay durumu **Yeni**, eylem için bir isteği temsil eder. Bir sonraki adım, uyumsuzluk için işlem yapacağınızı veya yapmayacağınızı göstermek için onaylama durumunu **Onaylandı** veya **Reddedildi** şeklinde değiştirmektir. Ayrıca bir uyumsuzluğu işinizin bittiğini gösterecek şekilde kapatabilir (ayrı bir onay kutusu seçerek) veya ek değerlendirmenin gerektiğini gösterecek şekilde yeniden açabilirsiniz. 

Bir belge iliştirerek, bir uygunsuzluk için yorumlar girebilirsiniz. **Belge türü** sayfasını kullanarak uygunsuzluklar için benzersiz bir dosya türü tanımlamak iyi bir fikirdir. Daha sonra **Rapor Kurulumu** sayfasını kullanarak bu belge türü için yorumların uygunsuzluk raporunda ve uygunsuzluk etiketinde yazdırılıp yazdırılmayacağını tanımlayabilirsiniz. Uyum raporu ve uyumsuzluk etiketi, malzeme elden çıkarmaya yardımcı olabilir. Uyumsuzlukla ilgili seçim ölçütlerini temel alarak, rapor ve etiketleri oluşturabilirsiniz. Bu ölçütler, uygunsuzluk numarası, madde, müşteri, satıcı ve durumu içerir. 

Uygunsuzluk raporu, uygunsuzluk numarası, madde ve sorun türünü görüntüler. Rapor kurulumu ilkenize bağlı olarak, rapor, uygunsuzlukla ilgili notları da görüntüleyebilir. Uygunsuzluk etiketi benzer bilgileri görüntüler ve kusurlu malzemenin elden çıkarılmasını yönlendirmek için uyumsuzluğa atadığınız karantina bölgesi ve türünü (**Sınırlı kullanım** veya **Kullanılamaz** gibi) içerir.

## <a name="approved-nonconformance"></a>Onaylanan uygunsuzluk
İsteğe bağlı olarak, onaylanan bir uyumsuzluk için bir veya daha fazla ilgili operasyon tanımlayabilirsiniz. İlgili bir işlem yapılması gereken ve çalışma nedeni hakkında açıklayıcı metin ve tanımladığınız kalitesi işlemleri listesini içeren çalışma açıklar. Bir operasyonu tanımladıktan sonra, isteğe bağlı olarak işi gerçekleştirmek için gereken sair giderleri, maddeleri ve zaman tablosu çalışma saat sayısı tanımlayabilirsiniz. İlgili operasyon için hesaplanan maliyetler gösterilir ve uyumsuzluk için toplam hesaplanan maliyetler gösterilir. Hesaplanan maliyetler ve bunlarla ilişkili ayrıntılar (maddeler, çalışma saat sayısı ve sair giderler hakkında) referans niteliğinde bilgilerdir ve bunlar yalnızca kalite yönetimi işlevi çerçevesinde kullanılır. İsteğe bağlı olarak, önce kalite emirlerini sorgulayıp daha sonra yeni kalite emrini oluşturarak, uyumsuzluktan bir kalite emri oluşturabilirsiniz. Örneğin, bir kalite emri kusurlu malzemeyi test etme (veya yeniden test etme) gereksinimini tanımlayabilir. Yeni oluşturulan kalite emri, ilk uyumsuzlukla olan bağlantıyı görüntüler. İsteğe bağlı olarak bir uyumsuzluğu başka bir uyumsuzluğa bağlayabilir ve mevcut bir uyumsuzluktan yeni bir uyumsuzluk oluşturabilirsiniz. Örneğin, bağlantı, kalite sorunlarının birbirine bağlı olmasını sergileyebilir.

## <a name="correction-handling"></a>Düzeltme işleme
**Düzeltmeler** sayfası düzeltilmesi gereken uygunsuzluklar listesi oluşturmanıza olanak sağlar. Her düzeltme maddesi, sorunun bulunabilmesini sağlayan tanı türüyle ilişkilendirilmiştir. **Düzeltmeler** sayfa de kimin düzeltici bir eylem gerçekleştirmesi hakkında bilgi içerir ve ne zaman. Sorunu düzeltmeyi bir belgeye ekleyerek gerekli düzeltici eylemi ayrıntılarını açıklayabilirsiniz. Uygunsuzluk gönderildikten veya düzeltildikten sonra, **Tamamlandı** seçeneğini seçerek düzeltme öğesini "kapatırsınız". Ayrıca, çözümün kısa vadeli bir çözüm olduğunu da gösterebilirsiniz. **belge türünü** sayfasını kullanarak düzeltmeler için benzersiz bir dosya türü tanımlamak iyi bir fikirdir. Daha sonra **Rapor Kurulumu** sayfasını kullanarak bu belge türü için yorumların düzeltme raporunda yazdırıldığını tanımlayabilirsiniz. Yazdırılan düzeltme raporu uygunsuzluk ve ilişkili uygunsuzluk notları hakkında bilgi görüntüler. Rapor ayrıca tanı türü ve ilgili düzeltme notları gibi düzeltme bilgileri içerir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Kalite yönetimi etkinleştirmek](enable-quality-management.md)

[Uygunsuzluk yönetiminin etkinleştirilmesi](enable-nonconformance-management.md)

[Inventory blocking](inventory-blocking.md)

[Quarantine orders](quarantine-orders.md)

[(Görev Kılavuzu) kalite siparişlerini kurun](http://ax.help.dynamics.com/en/wiki/set-up-quality-orders/)

[(Görev Kılavuzu) malların kalitesini denetlemek](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)



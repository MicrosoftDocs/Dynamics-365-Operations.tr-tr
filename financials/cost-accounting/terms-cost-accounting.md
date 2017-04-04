---
title: Maliyet muhasebesi terminolojisi
description: "Bu konu, Maliyet muhasebesinde kullanılan önemli terimleri tanımlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 87c13e268ab8825e06095d24e03694cf0f271a63
ms.openlocfilehash: 1ae6b43bdc1812ca822a1abe2a0e823cb797a511
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-terminology"></a>Maliyet muhasebesi terminolojisi

Bu konu, Maliyet muhasebesinde kullanılan önemli terimleri tanımlar.

**Cost accounting**

Maliyet muhasebesi; genel muhasebe, muavin defterler, bütçeler ve istatistiksel bilgiler gibi çeşitli kaynaklardan veri toplamanıza olanak sağlar. Maliyet verilerini analiz edebilir, özetleyebilir ve değerlendirebilirsiniz. Böylelikle yönetim; fiyat güncelleştirmeleri, bütçeler, maliyet kontrolü ve bu gibi konularda en iyi kararı verebilir. Maliyet analizinde kullanılan kaynak verileri, Maliyet muhasebesinde bağımsız olarak ele alınır. Bu nedenle, maliyet muhasebesindeki güncelleştirmeler kaynak veriyi etkilemez. Ancak çeşitli kaynaklardan maliyet verileri toplandığında ve özellikle ana hesapları genel muhasebeden Microsoft Dynamics 365 for Operation'a maliyet öğeleri olarak içe aktardığınızda aynı bilgi hem genel muhasebede hem de maliyet muhasebesinde bulunduğundan veri fazlalığı meydana gelir. Bu fazlalık gereklidir, çünkü harici raporlama için mali yönetimi ve dahili raporlama için maliyet muhasebesini kullanırsınız.

**Cost accounting ledger**

Maliyet muhasebesi defteri; maliyet muhasebesinde belirli bir alan için işlemlerin, değerlerin ve miktarların nasıl girildiğini ve sunulduğunu belirleyen özelleştirilmiş bir çerçevedir. Maliyet muhasebesi defteri, maliyet nesnelerinin maliyetlerinin ölçülmesi için işlemleri ve kuralları tanımlar. Maliyet hareketleriyle ilgilenir ve maliyet hareketlerinin ürettiği değerlerdeki ve miktarlardaki değişiklikleri kaydeden belgeleri yönetir.

**Cost entry**

Maliyet girişleri, genel muhasebe girişlerindeki veri bağlayıcıları aracılığıyla yapılan bir transferin, maliyet tahsisatlarının ve maliyet defterlerine nakledilen maliyet girişlerinin sonucudur.

**Cost object**

Maliyet nesneleri, maliyetlerin tahsis edildiği her türlü nesne türüdür. Bazı genel maliyet nesneleri şunlardır:

-   Ürünler
-   Projeler
-   Kaynaklar
-   Departmanlar
-   Maliyet merkezleri
-   Coğrafi bölgeler

Yönetim, maliyetlerini sayısal olarak ölçmek ve karlılık analizi yapmak için maliyet nesnelerini kullanır.

**Cost element**

Maliyet öğeleri, maliyetlerin aktığı alanları izlemek ve sınıflandırmak için kullanılır. İki tür maliyet öğesi vardır: birincil maliyetler ve ikincil maliyetler. **Birincil maliyetler** birincil maliyet öğeleri akışını gelen finansal muhasebe maliyet muhasebesine temsil eder. Maliyet öğesi yapısı, maliyet öğesinin bir ana hesaba karşılık gelebileceği, genel muhasebe defterindeki kar ve zarar hesabı yapısına karşılık gelir. İş ihtiyaçlarına bağlı olarak tüm ana hesaplar, maliyet öğeleri olarak temsil edilmek zorunda değildir. Aşağıda bazı birincil maliyet öğeleri örnekleri verilmiştir:

-   Satılan malların maliyeti (SMM)
-   Dolaylı malzeme maliyetleri
-   Personel maliyetleri
-   Enerji maliyetleri

**Secondary cost element** 

İkincil maliyet öğeleri yalnızca Maliyet muhasebesinde oluşturulduğundan ve kullanıldığından maliyetlerin dahili akışını temsil eder. İkincil maliyet öğeleri, maliyetlerin kaynağının izlenmesinin garanti altına alınmasına yardımcı olur. Bu maliyet öğeleri, maliyet tahsisatları ve genel gider hesaplamalarında kullanılır. Aşağıda ikincil maliyet öğelerine bazı örnekler verilmiştir:

-   Üretim maliyetleri
-   Üretim, malzeme ve pazarlama genel giderleri

**Cost control unit**

Maliyet kontrol birimi, maliyet yapısını temsil eder. Bu, bir maliyet muhasebesi defterindeki maliyet nesnesi boyutlarıyla ilişkilendirilmelidir.

**Version**

Sürümler, çeşitli sonuçların benzetiminin yapılması, görüntülenmesi ve karşılaştırılması için kullanılır. Tüm fiili maliyetler varsayılan olarak, *gerçek* olarak bilinen bir temel sürümde görüntülenir. Bütçeler ve hesaplamalar için ihtiyaç duyduğunuz kadar çok sürümle çalışabilirsiniz. Örneğin, bütçe verilerini orijinal bir sürüme aktarabilir ve ardından bütçeyi düzeltilmiş bir sürümde gözden geçirebilirsiniz. Hesaplamalar için birden çok sürüm oluşturabilirsiniz. Bu çeşitli sürümlerde, maliyet tahsisatında uygulanacak farklı hesaplama kuralları kullanarak hesaplamalar oluşturabilirsiniz.

**Statement**

Raporlar, maliyet kontrolünden sorumlu yöneticilerin incelemesi içindir. Raporlar, maliyet denetleyicisi tarafından tanımlanır ve fiili ve bütçelenmiş maliyetlerin yanı sıra sapmalar ve hesaplama sürümleri hakkında da hızlı bir genel bakış sağlar. Yöneticilerin yalnızca sorumlu oldukları verileri görüntülemesinin garanti altına alınmasına yardımcı olmak için, raporlarda yer alan veriler erişim kurallarına tabidir.

**Veri Bağlayıcısı**

Veriler, veri bağlayıcıları aracılığıyla harici sistemlerden Maliyet muhasebesine aktarılabilir. Örneğin, hesap yapılarını, boyutları, genel muhasebe girişlerini ve bütçe girişlerini içe aktarabilirsiniz. Veri aktarmak ve veri bağlantıları oluşturmak için önceden yapılandırılmış veri bağlayıcıları veya özel bağlayıcılar kullanabilirsiniz.

**Cost classification**

Maliyet sınıflandırması, maliyetleri ortak özelliklerine göre gruplandırır. Örneğin, maliyetler öğelere, izlenebilirliğe ve davranışa göre gruplandırılabilir.

-   **Öğelere göre**: Malzeme, işçilik ve giderler.
-   **İzlenebilirliğe göre**: Doğrudan maliyetler ve dolaylı maliyetler. Doğrudan maliyetler, maliyet nesnelerine doğrudan atanır. Dolaylı maliyetler, maliyet nesnelerinde doğrudan izlenemez. Dolaylı maliyetler, maliyet nesnelerine tahsis edilir.
-   **Davranışa göre**: Sabit, değişken ve yarı değişken.

**Cost behavior**

Maliyet davranışı, temel iş faaliyetlerindeki değişiklikler ile ilişkili olarak maliyetleri davranışlarına göre sınıflandırır. Maliyetleri etkin bir şekilde kontrol etmek için yönetimin maliyet davranışını anlaması gerekir. Üç tür maliyet davranışı modeli vardır: sabit, değişken ve yarı değişken.

- **Sabit Maliyet** -sabit maliyet etkinlik düzeyi değişiklikleri ne olursa olsun kısa vadeli farklılık yoktur maliyetidir. Sabit maliyet, faaliyet düzeyi artsa veya azalsa bile bundan etkilenmeyecek bir işletmenin, kira gibi, temel bir işletme gideri olabilir.

- **Değişken maliyet** -değişken maliyet etkinlik düzeyi değişiklikleri göre değişir. Örneğin, belirli bir doğrudan malzeme maliyeti, satılan her bir ürün ile ilişkilidir. Ne kadar çok ürün satılırsa doğrudan malzeme maliyeti de o kadar artar.

- **Yarı değişken maliyet** -yarı değişken maliyetleri olan sabit kısmen ve kısmen değişken maliyetler. Örneğin, bir İnternet erişim ücretine standart bir aylık erişim ücreti ve geniş bant kullanım ücreti dahildir. Standart aylık erişim ücreti sabit maliyet iken geniş bant kullanım ücreti değişken maliyettir.

**Overhead cost**

İşletmenin faaliyetlerini sürdürmek için yapılan sürekli giderlere genel giderler denir. Bunlar, belirli iş faaliyetlerine doğrudan bağlanamayan maliyetlerdir. Aşağıda bazı genel gider örnekleri verilmiştir:

-   Muhasebe masrafları
-   Amortismanlar
-   Sigorta
-   İlgi Alanı
-   Yasal masraflar
-   Vergiler
-   Yardımcı hizmetlerin maliyetleri

**Cost allocation**

Maliyet tahsisatı, ortak maliyetleri kök nedenlerine göre atama ve tahsis etme işlemidir. Maliyet tutarlarını ve miktarlarını bir maliyet nesnesinden bir veya birden çok maliyet nesnesine tahsis edersiniz. Örneğin, tüm tesis hizmetleri maliyetleri, ortak ofis binasını kullanan çeşitli departmanlara tahsis edilir.

**Cost allocation policy**

Maliyet tahsisatı ilkesi, tahsis edilmesi gereken tutarları ve miktarları tanımlar. Tahsisat kuralları, tahsis edilmiş maliyetleri belirleyen tahsisat kaynağı kurallarını ve maliyetlerin nerede tahsis edildiğini belirleyen tahsisat hedefleri kurallarını içerir. Örneğin, tesis hizmetleri için tüm maliyetler, bir organizasyondaki çeşitli departmanlara (diğer bir deyişle, tahsisat hedeflerine) tahsis edilebilen bir tahsisat kaynağıdır.

**Allocation base**

Tahsisat tabanı, kullanılan makine saati, tüketilen kilovat saat, harcanan doğrudan işçilik saati veya kullanılan metrekare gibi faaliyetleri ölçmek veya miktarını belirlemek için kullanılabilen tabandır. Maliyetleri bir veya daha fazla maliyet nesnesine tahsis etmek için kullanılır.

**Allocation principle**

Tahsisat ilkelerinden biri, maliyet oranına göre maliyet tahsisatıdır. Fiili dönem oranını veya geçmiş dönem oranını kullanarak maliyet tahsisatı yapmayı seçebilirsiniz. Karşılıklı yöntem kullanılan tahsisat, tahsisat tabanının, tahsisat fiili dönem oranı kullanılarak yapılmadan önce bir dizi eşzamanlı eşitleme tarafından belirlenmesinin garanti altına alınmasına yardımcı olur.

**Cost roll-up**

Maliyet toplamasının amacı, belirli bir maliyet nesnesi için tüm maliyetleri içermektir. Toplama düzeyi kullanıcı tarafından tanımlanır. Bir maliyet nesnesinden diğerine tahsis edilmesi gereken maliyet öğelerini, maliyet toplaması kullanarak toplayabilirsiniz. Maliyet toplama kullanılmadığında, her bir maliyet öğesi bir maliyet nesnesinden diğerine tahsis edilir.

**Maliyet oranı ilkesi**

Maliyet oranı, maliyet nesnesi başına fiyatı hesaplamak için kullanılır. Fiyatın öğelerini anlamak için maliyet oranı ilkeleri tanımlarsınız. İki tür maliyet oranı vardır: geçmiş dönem maliyet oranı ve planlanan maliyet oranı. Geçmiş dönem maliyet oranı, maliyet nesnesinin tahsisat tabanı için bir çarpan olarak kullanılan hesaplanmış bir orandır. Oran, önceki dönemdeki maliyet tahsisatları temel alınarak hesaplanır. Planlanan oran, kullanıcı tanımlı bir orandır.

**Boyut hiyerarşisi**

Boyut hiyerarşileri; tahsisat, maliyet oranı ve maliyet toplaması için kurallar tanımladığınızda, Microsoft Excel'de raporları veya verileri görüntülediğinizde ve toplanan verilere erişim sağladığınızda raporlama yapıları olarak kullanılır. İki tür boyut hiyerarşisi vardır: kümeleme hiyerarşisi ve sınıflandırma hiyerarşisi. Kümeleme hiyerarşisi maliyet öğelerine göre tanımlanırken sınıflandırma hiyerarşisi, maliyet nesnelerine göre tanımlanır.

**Statistical dimension**

İstatistiksel boyut, tahsisatların veya maliyet oranı hesaplamalarının tabanı olarak kullanılabilecek bir nesnenin toplamının veya sayısının ifadesidir. El ile veya kaynak sistemlerden içe aktarılarak oluşturulur. İstatistiksel boyutlara örnek olarak çalışan sayısı, her cihazdaki lisanslı yazılım sayısı, her makinenin enerji tüketimi veya bir maliyet merkezinin metrekaresi verilebilir.

**Statistical entry**

İstatistiksel girişler, belirli bir istatistiksel boyut için kaydedilen toplamı veya sayım değerini saklar. Kaydedilen toplam veya sayım değeri büyüklük olarak da adlandırılır.



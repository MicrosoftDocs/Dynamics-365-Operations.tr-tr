---
title: "Ambar konfigürasyonu"
description: "Bu makalede, bir ambarın nasıl yapılandırılacağı açıklanmaktadır. Konu, ambar düzeninin ve ambar süreçlerinin nasıl etkinleştirileceği hakkında bilgiler içermektedir."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, WHSLocation, WHSLocationBuild, WHSLocationProfile, WHSLocationType, WHSLocDirTable, WHSParameters, WHSWaveTemplateTable, WHSWorkPool, WHSWorkTemplateTable, WHSZone, WHSZoneGroup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 11554
ms.assetid: 262b7b88-2cce-44f7-9a5b-77c12af1be20
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: d38cbe149a2713bddb50a044b77f6e4789b50a21
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-configuration"></a>Ambar konfigürasyonu

[!include[banner](../includes/banner.md)]


Bu makalede, bir ambarın nasıl yapılandırılacağı açıklanmaktadır. Konu, ambar düzeninin ve ambar süreçlerinin nasıl etkinleştirileceği hakkında bilgiler içermektedir.

**Not:** Bu makale **Ambar yönetimi** Modülü (Gelişmiş Depolama) içindeki özellikler için geçerlidir. **Stok yönetimi** modülündeki ambar özellikleri için geçerli değildir.

## <a name="warehouse-layout"></a>Ambar düzeni
Microsoft Dynamics 365 Finance and Operations, Enterprise sürümündeki Ambar yönetim sistemi, değişen gereksinimleri karşılayacak şekilde ambar düzeninizi tanımlamak için esnek yollar sağlar, bu sayede en iyi ambar verimliliğini elde edebilirsiniz.

-   Malların en iyi şekilde yerleştirilmesi için yüksek öncelikli ve düşük öncelikli depolama alanları kurabilirsiniz.
-   Ambarınızı çeşitli depolama ihtiyaçlarını karşılayacak şekilde bölgelere ayırabilirsiniz; maddelerin sıcaklık gereksinimleri veya çeşitli dönüşüm oranları gibi.
-   Herhangi bir düzeyde (örneğin, site, ambar, koridor, dolap, raf ve depo gözü konum) ambar konumu belirtebilirsiniz.
-   Fiziksel kapasite kısıtlama ayarlarını kullanarak konumları gruplandırabilirsiniz.
-   Maddelerin nasıl depolandığını ve çekildiğini, sorgu tarafından tanımlanan kurallara dayalı olarak denetleyebilirsiniz.

Ambar Yönetimi'ni Finance and Operations uygulamasında kullanmak için, bir ambar oluşturmalı ve daha gelişmiş veya özelleştirilmiş ambar yönetimi faaliyetleri için bunu etkinleştirmelisiniz. **Ambarlar** sayfasında, **Ambar yönetimi işlemlerini kullanın** seçeneğini seçin.

### <a name="zone-groups-zones-location-types-and-locations"></a>Bölge grupları, bölgeler, konum türleri ve konumlar

Ambar düzenini etkinleştirme işleminin bir parçası olarak, ambar bölge grupları ve bölgeler, konum profilleri, konum türleri ve konumları tanımlamanız gerekir.

-   **Bölge grupları** – Ambar içindeki bölgelerin mantıksal veya fiziksel bir gruplandırması.
-   **Bölgeler** – Ambar içindeki konumların mantıksal veya fiziksel bir gruplandırması.
-   **Konum profilleri** – Aynı ambar konum işleme ilkelerine sahip (örneğin farklı madde numaraları karışımları burada depolanabilir ve aynı fiziksel kapasite kısıtlamaları uygulanır) konumların mantıksal ve fiziksel bir gruplaması.
-   **Konum türleri** – Ambar konumlarının mantıksal veya fiziksel bir gruplandırması. Örneğin, tüm hazırlama konumları için bir konum türü oluşturabilirsiniz. **Ambar yönetimi parametreleri** sayfasındaki zorunlu ayarlar, hazırlama konum türleri ve son teslim konum türünü tanımlama işlemini çalıştırır.
-   **Konumlar** – En düşük düzeyde konum bilgileri. Konumlar eldeki stokun nerede depolanacağını ve hangi ambardan çekileceğini izlemek için kullanılır.

Ambar düzeninizi tanımlamak için oluşturduğunuz bir varlıklar, ambarda iş siparişlerini başlatmak için oluşturduğunuz iş şablonlarında ayarladığınız sorgularda kullanılır. Bu nedenle, bölgeleri, konum türlerini ve benzerlerini tanımlarken, ambardaki farklı alanların farklı işlemler için nasıl kullanıldığını göz önünde bulundurun. Ayrıca, belirli bir alanın fiziksel özellikleri gibi etkenleri göz önünde bulundurun. Örneğin, yalnızca belirli türde forklift kullanabileceğiniz alanlar olabilir. Veya şirketiniz aynı tesis içerisinde hem üretime yönelik hem de mamul mallara sahipse, Finance and Operations'ta tek bir depo oluşturmak ancak iki bölge grubu oluşturarak iki operasyonu ayırmak isteyebilirsiniz. Varlıklarınıza açıklayıcı adlar verirseniz şablon sorgularında kullanırken tanımanız kolay olur.

### <a name="location-stocking-limits-location-profiles-and-fixed-picking-locations"></a>Konum stoklama sınırları, konum profilleri ve sabit çekme konumları

Ambarın fiziksel düzenini, hem depolama kapasitesini (konum stoklama sınırları ve konum profilleri) belirlemek hem de en iyi ambar işlemlerini elde etme çabanızın bir parçası olarak dikkate almanız gerekir. 

Konum stoklama limitleri, stok miktarını taşıyacak fiziksel kapasitenin mevcut olmadığı konumlara yerleştirilmesini talep edecek işlerin oluşturulmasının önüne geçmeye yardımcı olur. Örneğin, ambardaki bazı konumlarda konum başına yalnızca bir palet tutulabiliyorsa, konum stoklama limitleri etkinleştirilebilir. **Miktar** değeri **1** olarak ayarlanabilir ve **Birim** değeri belirli bir konum profili gruplandırmasında **PL** olarak ayarlanabilir. 

Konum kapasitesi kısıtlamalarını denetlemek için daha gelişmiş hesaplamalar gerekiyorsa, konum profili ayarları kullanılabilir. Bu durumda, ağırlık ve hacim, kapasite hesaplamaları gerçekleştirildiğinde göz önünde tutulur. 

En iyi giden işlemleri elde etmek için, sabit malzeme çekme konumları ve/veya ambalaj konumlarının kullanılıp kullanılmayacağını değerlendirmelidir. Genellikle, minimum/maksimum stok yenileme, toplu alandan sabit malzeme çekme konumları için stok yenileme işlemleri için kullanılır ve birden çok sabit malzeme çekme konumları, aynı ambar içinde ve ürün çeşitleri için etkinleştirilebilir. Sadece dalga/yük yenileme işlemi için kullanılan özel talep stok yenileme taşma konumlarını etkinleştirerek elde edebileceğiniz esnekliği göz önünde bulundurun.

### <a name="location-setup-wizard"></a>Konum kurulum sihirbazı

Konumları ambar içinde hızlı bir şekilde oluşturmak için **Konum kurulumu** sihirbazını kullanabilirsiniz. Bu işlemin bir parçası olarak konum adlarının biçimini kolayca koruyabilirsiniz.

## <a name="warehouse-processes"></a>Ambar işlemleri
Ambar yapılandırmasının bir parçası olarak, ambar işlemlerini iş gereksinimlerine göre etkinleştirmek önemlidir. Yapılandırmanız gereken en önemli bileşenler dalga şablonları, iş şablonları, iş havuzları ve konum yönergeleridir.

### <a name="wave-templates"></a>Dalga şablonları

Dalga şablonları, giden "Ambara serbest bırak" işlemini etkinleştirmeye yardımcı olur. Sipariş satırları serbest bırakıldıktan (toplu işlem aracılığıyla veya önceden oluşturulmuş yükler ile doğrudan kaynak belgelerden) hemen sonra, dalga şablon işlevi kullanılır. 

Üç farklı türde dalga şablonu oluşturabilirsiniz: 
-   **Sevkiyat**
-   **Üretim emri**
-   **Kanban** 

Parametreler, sistemin otomatik olarak giden iş işlenmesinde ne kadar ileri gideceğini tanımlamak için kullanılır. Bir dalga şablonu, dalga şablonu serisi ve şablonda belirtilmiş olan ölçütler temel alınarak seçilir. Eğer bir şablon sıranın başında listeleniyorsa, o şablondaki ölçütler önce denetlenir. Eğer ölçütler karşılanıyorsa, dalga şablonu işlenir. Aksi takdirde, bir sonraki şablonun ölçütleri denetlenir ve bu şekilde devam eder. Bu nedenle, ilk önce işlenmesi için dalga şablonu sıralama listesinin en başına, en fazla belirli ölçüte sahip şablonu koymak için bir fikirdir. Örneğin, belirli bir taşıyıcı için tüm işi bugün işlemek ve diğer taşıyıcılar için işleme işini geçici olarak geciktirmek istiyorsunuz. Bu durumda, söz konusu taşıyıcı için dalga şablonu, sıradaki diğer şablonlardan daha üstte listelenmelidir. Aksi takdirde, bu taşıyıcı için iş tamamlanmadan önce diğer taşıyıcılar için işler, işlemeye girebilir. 

Her dalga şablonundaki dalga işleme yöntemlerini belirtmeniz gerekir. Mevcut olan yöntemler, dalga şablonu türüne göre farklılık gösterir.

### <a name="work-templates"></a>İş şablonları

İş şablonu tanımları, ambar yönetimi iş süreçlerinin tanımında önemli bir rol oynarlar. Hangi iş gerçekleştirileceğini ve işin nasıl yapılacağını tanımlarlar. Şablonlar ayrıca işin nerede gerçekleştirileceğini belirlemek için bir konum yönergesine bağlanan bir yönerge kodu içerebilirler. İş şablonları, iş için ölçütleri belirten sorguyu içerirler. Her şablonun, eldeki stokun bir konumdan diğerine aktarılmasından oluşan temel çalışma işlemini yürütmek için en az bir çekme ve bir indirme işlemini içermesi gerekir. 

Eğer birden çok çalışanın bazı ambar faaliyetleri için işleri işleyebilmeleri gerekiyorsa, stok için *hazırlama* konseptinden faydalanmak ve işin yerine getirilmesini farklı iş sınıflarına ayırmak isteyebilirsiniz.

### <a name="work-pools"></a>İş havuzları

İş havuzları, işi gruplar halinde düzenlemek için kullanılır. Örneğin, belirli bir ambar konumundaki gerçekleşen işi sınıflandırmak için bir iş havuzu oluşturabilirsiniz. Sayım dışındaki tüm iş türleri için bir iş şablonuna bir iş havuzu atayabilirsiniz. Döngü sayımı için aşağıdaki sayfalarda bir iş havuzu atayabilirsiniz:

-   Döngü sayım planları
-   Döngü sayımı eşikleri
-   Yerleşime göre döngü sayımı işi
-   Maddeye göre döngü sayımı işi

İş oluşturmak için iş şablonlarını kullandığınızda, iş havuzu otomatik olarak işe atanır. 

İş havuzu kimlikleri ayrıca belirli bir ambar çalışanına yönlendirilecek işin türünü sınırlamak için kullanılabilir, bu işlevin ilgili mobil cihaz menü öğesinde yapılandırılmış olması şartıyla.

### <a name="location-directives"></a>Konum yönergeleri

Adından da anlaşılacağı gibi, konum yönergeleri iş hareketlerini ambardaki uygun konumlara yönlendirmek için kullanılır. Diğer bir deyişle, nereden çekip nereye koyulacağını tanımlar. 

Her bir konum yönergesi satırı ile ilişkili eylemleri tanımlamak daha hızlı ve kolaylaştırmak için önceden tanımlanmış stratejilerden birini kullanın. Örneğin **Gelen iş olmayan boş konum** stratejisini ambardaki boş konumları aramak için kullanabilirsiniz veya **FEFO toplu iş rezervasyonu** stratejisini giden satış sevki için kullanabilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[WMS etkin bir ambarda konumları yapılandırma (Görev kılavuzu)](tasks/configure-locations-wms-enabled-warehouse.md)





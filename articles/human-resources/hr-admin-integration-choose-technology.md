---
title: Veri tümleştirme teknolojisi seçme
description: Bu makale, tümleştiricilerin gereksinimlerine en uygun teknolojiler konusunda bilinçli kararlar verebilmelerini sağlamak amacıyla farklı tümleştirme teknolojilerinin özelliklerini açıklayarak, İnsan Kaynakları tarafından yönetilen verilerle tümleştirme için farklı seçenekleri tanıtmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029900"
---
# <a name="choose-a-data-integration-technology"></a>Veri tümleştirme teknolojisi seçme

Dynamics 365 Human Resources çeşitli iş süreçlerinde yararlı olan iş verilerini yönetir. Bu makale, tümleştiricilerin gereksinimlerine en uygun teknolojiler konusunda bilinçli kararlar verebilmelerini sağlamak amacıyla farklı tümleştirme teknolojilerinin özelliklerini açıklayarak, İnsan Kaynakları tarafından yönetilen verilerle tümleştirme için farklı seçenekleri tanıtmaktadır.

## <a name="data-integration-vision"></a>Veri tümleştirme vizyonu

Microsoft, iş verilerini şirketinizin benzersiz olmasını sağlayan bir anahtar varlık olarak görür. İşletmenizin verileri çok değerlidir. İşletmenin bir bölümü tarafından toplanan ve tutulan veriler, işletmenin başka bir bölümü tarafından toplanan verilerle ilgilidir ve bu ilişkiler kuruluşunuzda iş süreçlerini ve iş zekasını geliştirmek için kullanılabilir. Verilerin hangi sisteme "ait" olduğuna bakılmaksızın, iş verilerinize kolay, güvenli, kalıcı erişim sağlamak, İnsan Kaynakları ile veri tümleştirme vizyonumuza ilişkin temel bir ilkedir.

Birden çok sistem arasında veri tümleştirme eskiden beri zor olmuştur.
Microsoft, veri tümleştirmeyi daha kolay hale getirmek için gereken adımları ve bu hedefin [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) ile gerçekleştirmesine yönelik büyük bir adım atıyor.

Dahası, İnsan Kaynakları, Common Data Service'i, İnsan Kaynakları verileri için tercih edilen ortak arabirim yapıyor. Zamanla İnsan Kaynakları tarafından yönetilen en önemli verilerin tümünün Common Data Service'te sunulacağını düşünüyoruz. Çoğu tümleştirme uygulaması için teknoloji seçeneği olarak Common Data Service'i öneriyoruz. Uygulamanızın gerektirebileceği tüm verilerin şu anda Common Data Service'te sunulmadığının ve proje zaman çizelgelerin alternatif bir teknoloji gerektirebileceğinin farkındayız ve Common Data Service tümleştirme gereksinimlerinizi karşılamadığı zaman bize bildirmenizi rica ederiz.

## <a name="integration-technologies"></a>Tümleştirme teknolojileri

Aşağıdaki bölümlerde İnsan Kaynakları ile kullanılabilecek farklı veri tümleştirme teknolojileri açıklanmaktadır.

### <a name="common-data-service-entities"></a>Common Data Service varlıkları

Common Data Service, İnsan Kaynakları için tercih edilen ortak veri arabirimidir. Common Data Service, [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) çözümlerinin oluşturulduğu Dynamics 365 "XRM" platformundan doğmuş, olgun bir platform üzerinde inşa edilmiştir.

Common Data Service, veri varlıkları için bir platform ve bu varlıklara erişim için bir API sağlar. İnsan Kaynakları, kuruluşunuzda dağıtılırken, bir Common Data Service örneğine bağlanır ve İnsan Kaynakları verilerini barındıran varlıklar o Common Data Service örneğine dağıtılarak varlıkların ve verilerinin, Common Data Service örneğine bağlanabilen herhangi bir uygulama tarafından kullanılabilmesi sağlanır. Kullandığınız İnsan Kaynakları uygulamalarına bağlı olarak, İnsan Kaynakları, veri işlemlerini doğrudan Common Data Service varlıklarına karşı yapar (Attract and Onboard için durum böyledir) veya Common Data Service varlıklarıyla veri eşitlemesi yapar.

Tümleştirme uygulamalarınızın gerektirdiği verileri ortaya koyan veri varlıkları Common Data Service'te yer aldıktan sonra, [Common Data Service ve desteklediği API 'lerden](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer) tam olarak yararlanabilirsiniz. Desteklenen API'lardan biri, Common Data Service verilerine erişmek için OData uygulaması sağlayan [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api)'dır.

Common Data Service varlıkları ve ilişkili API'lar, web uygulamalarından, web hizmetlerinden/API'lardan ve OData akışlarına bağlanan tüm diğer uygulamalardan İnsan Kaynakları verilerine erişmek için en iyi seçenektir.

> [!NOTE]
> Common Data Service'i İnsan Kaynakları için tercih edilen veri arabirimi yapma kararı henüz yeni olduğu için, tümleştirmenizde gereksinim duyduğunuz İnsan Kaynakları veri varlıklarının henüz Common Data Service<sup>1</sup>'te kullanıma hazır olmadığını görebilirsiniz. Tümleştirmeniz için gereken İnsan Kaynakları varlıkları henüz mevcut değilse, veri varlıklarının kullanılabilir hale gelmesini beklemeniz veya aşağıda açıklanan diğer tümleştirme teknolojilerinden birini kullanmanız gerekecektir.
> 
> Varsayılan olarak, Common Data Service tümleştirmesi, sağlanan demo verilerini içermeyen yeni ortamlarda kapalıdır. Demo verilerini içeren yeni ortamlarda açıktır ve bu veriler sağlandığında ortamlar verileri eşitlemeye başlar. Ortamınız veri eşitlemeye hazır hale gelince tümleştirmeyi açabilirsiniz.

<sup>1</sup>Common Data Service'te mevcut olan İnsan Kaynakları varlıklarının listesi için bkz. [İnsan Kaynakları ve Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). Attract and Onboard için, tüm varlıklar Common Data Service'te kullanılabilir durumdadır.

### <a name="dmfdixf-entities"></a>DMF/DIXF varlıkları

Temelde Finance and Operations uygulamalarıyla aynı platformda oluşturulan İnsan Kaynakları, bazen Veri İçe/Dışa Aktarma Çerçevesi veya DIXF olarak da bilinen bir [Veri Yönetimi Çerçevesi (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json) ve İnsan Kaynakları ile veri içe/dışa aktarma için kullanılabilen bir veri kümesi sağlar. Common Data Service varlıkları İnsan Kaynakları için tercih edilen veri tümleştirme arabirimi olmakla birlikte, DMF varlıkları şöyle durumlarda yararlı olmaya devam edecektir:

- Common Data Service varlıkları henüz kullanılabilir değilse.

- Tümleştirme, yüksek performanslı toplu veri içe/dışa aktarma yetenekleri gerektiriyorsa.

DMF varlıkları şu anda İnsan Kaynakları verileri için en eksiksiz veri kapsamını sağlıyorsa.

DMF, gerçek zamanlı tümleştirmeler için uygun değildir (örneğin bir kullanıcı arabiriminde hemen kullanıcı geri bildirimi gerektiğinde) çünkü paket işlemleri zamanlanmış toplu işler olup, toplu iş hizmeti, yürütülecek işi seçmeden önce en az 1-2 dakika gecikecektir ve buna, içe/dışa aktarma işlemini tamamlamak için gereken süre de eklenecektir.

DMF, yüksek hacim gerektiğinde (günde binlerce zamanlanmış kayıt içe/dışa aktarma vb.) en iyi seçenek olabilir.

> [!NOTE]
> DMF, Attract and Onboard için kullanılamaz.

### <a name="dmf-package-rest-api"></a>DMF paket REST API'sı

DMF, veri paketlerini yönetmek için bir [REST API'sı](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) sağlar. Bu API, DMF ile programlı bir şekilde etkileşimde bulunarak şöyle eylemlere olanak sağlamak için kullanılabilir:

- Bir veri paketini içe aktarma.

- Bir veri paketini dışa aktarma.

- İçe/dışa aktarma işleminin durumunu denetleme.

DMF Paket REST API'sı İnsan Kaynakları'nda tam olarak desteklenir: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF, ek olarak, İnsan Kaynakları'nın Microsoft Azure SQL veritabanınıza veri aktarabilmesini sağlayan güçlü bir özellik sağlar (genellikle [Kendi Veritabanınızı Getirin](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) veya BYOD olarak bilinir). Bu büyük esneklik sağlar çünkü veriler kendi SQL veritabanınızdayken bir SQL veri deposuna bağlanabilen herhangi bir uygulamadan veya ara yazılımdan en iyi şekilde yararlanabilirsiniz.

BYOD genellikle salt okunur bir çözüm olarak düşünülmelidir. Azure SQL veritabanında istediğiniz her türlü veriyi (örneğin veri karmaları) yönetip depolayabilirsiniz ama Azure SQL veritabanında depolanan veriler yeniden İnsan Kaynakları'na eşitlenmez.

BYOD, bir [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) ardışık düzeni için veri kaynağı olarak raporlama çözümleri, veri tümleştirmeleri ve veri karmaları için uygundur.

> [!NOTE]
> BYOD, Attract and Onboard için kullanılamaz.

### <a name="odata-enabled-entities"></a>OData etkin varlıklar

Çoğu DMF varlığı İnsan Kaynakları veri hizmetine (OData) erişimi etkinleştirilmiş durumdadır. [Finance and Operations OData hizmeti](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) için sağlanan belgeler genellikle İnsan Kaynakları için de geçerlidir ancak kendi OData tarafından sağlanan varlıklarınızı oluşturma ile ilgili belgeler İnsan Kaynakları için geçerli değildir.

Common Data Service ve Common Data Service'in sağladığı OData uygulaması ([Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8)) üzerinden), İnsan Kaynakları veri hizmetine tercih edilmekle birlikte, İnsan Kaynakları veri hizmeti şu anda İnsan Kaynakları verileri için daha eksiksiz varlık kapsamına sahiptir.

### <a name="excel-add-in"></a>Excel Eklentisi

[Excel Eklentisi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) yüzeyin altındaki OData etkin varlıkların kullanılabilmesini sağlar. Bir son kullanıcının tanıdık Excel kullanıcı arabirimi yoluyla İnsan Kaynakları verilerini alması ve değiştirmesi için uygun bir yol sağlar.

Excel Eklentisi, iş etki alanı uzmanlarının özel verileri içe/dışa aktarmaları için uygundur. Programlı otomasyon gerektiren tekrarlı bir veri tümleştirmesi için, başka bir tümleştirme teknolojisi daha uygun olacaktır.

### <a name="data-integrator"></a>Veri Tümleştirici

Common Data Service yönetici deneyimi, Common Data Service ile veri tümleştirmeleri için kullanılabilen bir [Veri Tümleştirici hizmeti](https://docs.microsoft.com/powerapps/administrator/data-integrator) sağlar. Veri Tümleştirici, tümleştirme projelerini tanımlamak için kullanılabilir (bu projeler genellikle uygulama geliştiricilerinin belirli tümleştirmeler için özel olarak tasarladıkları ön tanımlı şablonlara dayanır). Tümleştirme projeleri yinelenen bir zaman planıyla otomatik olarak veya el ile çalıştırılmak üzere zamanlanabilir.

Veri Tümleştirici projeleri, Common Data Service toplu tümleştirmeleri için uygundur ve Dynamics 365 uygulamaları ailesi içindeki tümleştirmeler için mükemmel bir seçenek oluşturur. Örneğin Microsoft, İnsan Kaynakları'ndan alınan verileri Dynamics 365 Finance'e tümleştirmek için kullanılabilen özgün bir Veri Tümleştirici şablonu sağlamaktadır. Daha fazla bilgi için bkz. [Dynamics 365 Human Resources'dan Dynamics 365 Finance'e tümleştirme](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Veri Tümleştirici [Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query)'yi de destekler ([Gelişmiş sorgu özelliği](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering) aracılığıyla).
Zengin M formül dili dahil, güçlü, esnek veri filtreleme ve dönüştürme yeteneği sağlayan Power Query, Power BI raporları geliştirme deneyimi olanlar için büyük olasılıkla tanıdık gelecektir.

## <a name="deciding-on-an-integration-technology"></a>Bir tümleştirme teknolojisinde karar kılma

Bunca çeşitli tümleştirme teknolojileri mevcutken, kullanılacak tümleştirme yaklaşımında karar kılmak bazen bunaltıcı olabilir. Zamanla ve özellikle Common Data Service'teki veri kapsamı geliştikçe karar vermek kolaylaşacak, Common Data Service çoğu durumda tercih edilen veri arabirimi haline gelecektir. Ancak o zamana kadar, Common Data Service'in gereksinimlerinizi henüz karşılamadığını fark edebilirsiniz. Aşağıdaki tablo çeşitli tümleştirme teknolojisi seçeneklerinin bazı temel özelliklerini özetlemeye yardımcı olacaktır.

| Teknoloji/Araç/API    | Yinelenen tümleştirmeler                   | Zaman uyumlu/Zaman uyumsuz                    | API aracılığıyla programlı erişim        | Uygun veri hacimleri                                   | Veri kapsamı                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service varlıkları           | Evet, Veri Tümleştirici veya ara yazılım kullanarak | Zaman Uyumlu/Zaman Uyumsuz, Toplu (Veri Tümleştirici üzerinden) | Evet, Dynamics 365 Web API (OData) aracılığıyla | Kullanım durumuna göre değişir (etkileşimli kullanım için sayfalamayı destekler) | İyileştirme<sup>2</sup>                       |
| DMF varlıkları           | Evet, ara yazılım aracılığıyla zamanlanmış        | Zaman Uyumsuz, Toplu                                | Evet, DMF Paket REST API'sı         | Yüksek (yüz binlerce kayıt)                    | Yüksek                                |
| DMF Paket REST API'sı   | Evet, ara yazılım aracılığıyla zamanlanmış        | Zaman Uyumsuz, Toplu                                | Evet                                       | Yüksek (yüz binlerce kayıt)                    | API tüm DMF varlıklarını destekler       |
| BYOD                   | Evet, İnsan Kaynakları'nda yönetici tarafından zamanlanır        | Zaman Uyumsuz, Toplu                                | Hayır<sup>3</sup>                                    | Yüksek (yüz binlerce kayıt)                    | Tüm DMF varlıklarını destekler           |
| OData etkin varlıklar | Evet, ara yazılım kullanarak                    | Zaman Uyumlu                                        | Evet, İnsan Kaynakları Veri Hizmeti (OData) ile  | Kullanım durumuna göre değişir (etkileşimli kullanım için sayfalamayı destekler) | Yüksek                                |
| Excel Eklentisi           | Hayır                                       | Zaman Uyumlu                                        | Hayır                                        | Orta (on binlerce kayıt)                      | Tüm OData etkin varlıkları destekler |
| Veri Tümleştirici        | Evet, Veri Tümleştirici'de zamanlanır        | Zaman Uyumsuz, Toplu                                | Hayır                                        | Kullanım durumuna göre değişir                                       | Tüm Common Data Service varlıklarını destekler           |

<sup>2</sup>Microsoft, Common Data Service varlıkları için veri kapsamını artırmaya çok önem veriyor ve kapsam kullanılabilir hale gelince Common Data Service'in tercih edilen veri arabirimi olmasını öneriyor. Şu anda Common Data Service veri kapsamı DMF ve OData etkin varlıklara göre düşük.

<sup>3</sup>SQL veritabanına programlı olarak erişilebilir.

## <a name="summary"></a>Özet

İş verileriniz değerli bir varlıktır ama verileri belirli amaçlarınız için (raporlama, veri karmaları, özel uygulamalar vb.) kullanmak zorsa, değeri büyük ölçüde azalabilir. Dynamics 365 Human Resources, İnsan Kaynakları uygulamasının kullanıcı arabiriminin (UI) dışındaki verilerle çalışmak için çeşitli teknolojiler sağlayarak uygulamaların verilere erişmelerine olanak sağlar. Bu konu, kullanılabilen tümleştirme teknolojilerini ve bazı temel özelliklerini açıklamaktadır. Bu bilgiler, tümleştirme projeleriniz için hangi yaklaşımların kullanılacağı konusunda daha iyi kararlar almanıza yardımcı olacaktır.


---
title: Veri tümleştirme teknolojisi seçme
description: Bu makale, Human Resources tarafından yönetilen verilerle tümleştirme hakkında bilgi sağlar. Gereksinimlerinize en uygun teknolojilere karar vermenize yardımcı olacak farklı tümleştirme teknolojilerini açıklar.
author: andreabichsel
ms.date: 02/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d2978d680efa59b1ba9cfcd7f58655da0ff4107
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890112"
---
# <a name="choose-a-data-integration-technology"></a>Veri tümleştirme teknolojisi seçme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu makale, Dynamics 365 Human Resources tarafından yönetilen verilerle tümleştirme hakkında bilgi sağlar. Gereksinimlerinize en uygun teknolojilere karar vermenize yardımcı olacak farklı tümleştirme teknolojilerini açıklar.

## <a name="data-integration-background"></a>Veri tümleştirme arka planı

İş verileri şirketinizin benzersiz olmasını sağlayan temel varlıktır. İşletmenizin verileri çok değerlidir. İşletmenizde toplanan veriler arasındaki ilişkileri, kuruluşunuzda iş süreçlerini ve iş zekasını geliştirmek amacıyla kullanabilirsiniz. İş verilerinizi hangi sistemden gelirse gelsin kolay, güvenli ve kararlı bir şekilde sağlamak için çalışıyoruz.

Birden çok sistem arasında veri tümleştirme eskiden beri zor olmuştur.
Microsoft, veri tümleştirmeyi daha kolay hale getirmek için gereken adımları ve bu hedefin [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) ile gerçekleştirmesine yönelik büyük bir adım atıyor.

Human Resources Dataverse'ı, İnsan Kaynakları verileri için tercih edilen ortak arabirim yapıyor. Zamanla İnsan Kaynakları tarafından yönetilen en önemli verilerin tümünün Dataverse'te sunulacağını düşünüyoruz. Çoğu tümleştirme uygulaması için teknoloji seçeneği olarak Dataverse'i öneriyoruz.

Dataverse uygulamanızın gerektirdiği tüm verileri henüz içeremeyebilir. Ayrıca, proje zaman çizelgeniz için alternatif bir teknoloji gerekebileceğini anlıyoruz. Dataverse Tümleştirme gereksinimlerinizi karşılamıyorsa bize bildirin.

## <a name="integration-technologies"></a>Tümleştirme teknolojileri

Aşağıdaki bölümlerde İnsan Kaynakları ile kullanılabilecek farklı veri tümleştirme teknolojileri açıklanmaktadır.

### <a name="dataverse-tables"></a>Dataverse tabloları

Dataverse, İnsan Kaynakları için tercih edilen ortak veri arabirimidir. [Dynamics 365 Customer Engagement](/dynamics365/?panel=customer-engagement#pivot=business-apps) çözümleri tarafından kullanılan Dynamics 365 XRM platformundan oluşturuldu.

Dataverse veri tabloları için bir platform ve API sağlar. Human Resources'ı dağıttığınızda, bir Dataverse kurulumuna bağlanır. Human Resources verilerinin varlıkları bu Dataverse kurulumuna dağıtılır. Tablolar ve verileri, Dataverse kurulumuna bağlanabilen herhangi bir uygulama tarafından kullanılabilir. Human Resources, verileri Dataverse tablolarına ve bu tablolardan eşitler.

> [!NOTE]
> Human Resources varlıkları Dataverse tablolarına karşılık gelir. Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)

Tümleştirici uygulamalarınızın gerektirdiği veri tabloları Dataverse'te olduğunda, [Dataverse'ü ve desteklediği API'leri](/powerapps/?panel=developer#pivot=home) tamamen kullanabilirsiniz. Desteklenen API'lardan biri, Dataverse verilerine erişmek için OData uygulaması sağlayan [Dynamics 365 Web API](/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api)'dır.

Dataverse tabloları ve ilişkili API'leri; web uygulamalarından, web hizmetlerinden/API'lerinden ve OData akışlarına bağlanan diğer tüm uygulamalardan Human Resources verilerine erişmek için en iyi seçenektir.

> [!NOTE]
> Dataverse'i Human Resources için tercih edilen veri arabirimi yapma kararı henüz yeni olduğu için, tümleştirmenizde gereksinim duyduğunuz Human Resources veri varlıklarının henüz Dataverse'ta kullanıma hazır olmadığını görebilirsiniz.
> </br>
> Dataverse'ta mevcut olan Human Resources varlıklarının listesi için bkz. [Human Resources ve Dataverse](/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Tümleştirmeniz için gereken İnsan Kaynakları varlıkları henüz mevcut değilse, veri varlıklarının kullanılabilir hale gelmesini beklemeniz veya aşağıda açıklanan diğer tümleştirme teknolojilerinden birini kullanmanız gerekecektir.
> </br>
> Varsayılan olarak, Dataverse tümleştirmesi, sağlanan demo verilerini içermeyen yeni ortamlarda kapalıdır. Demo verilerini içeren yeni ortamlarda açıktır ve bu veriler sağlandığında ortamlar verileri eşitlemeye başlar. Ortamınız veri eşitlemeye hazır hale gelince tümleştirmeyi açabilirsiniz.

### <a name="dmfdixf-entities"></a>DMF/DIXF varlıkları

Temelde Finance and Operations uygulamalarıyla aynı platformda oluşturulan Human Resources, bir [Veri Yönetimi Çerçevesi (DMF)](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json) sağlar. DMF, Veri İçe Dışa Aktarma Çerçevesi (DIXF) olarak da bilinir. Human Resources, Human Resources verilerini içe aktarmak ve dışa aktarmak için kullanabileceğiniz bir veri varlıkları kümesi sağlar. Dataverse tabloları, Human Resources için tercih edilen veri tümleştirme arabirimi olsa da, DMF varlıkları aşağıdakiler gibi bazı durumlarda yararlıdır:

- Dataverse tabloları şu anda kullanılamıyor.

- Tümleştirme, yüksek performanslı toplu veri içe/dışa aktarma yetenekleri gerektiriyorsa.

> [!NOTE]
> Human Resources varlıkları Dataverse tablolarına karşılık gelir. Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)

DMF varlıkları şu anda Human Resources verileri için en eksiksiz veri kapsamını sağlamaktadır.

DMF, kullanıcı arabiriminde anında Kullanıcı geri bildirimi gerektiğinde olduğu gibi, gerçek zamanlı tümleştirmeler için uygun değildir. Paket işlemleri zamanlanmış toplu işlerdir ve toplu iş hizmeti işi yürütme için almadan ve içe/dışa aktarma işlemini tamamlamak için gerekli olan süre için en azından 1-2 dakikalık gecikme süresine sahiptir.

DMF, yüksek hacim gerektiğinde (günde binlerce zamanlanmış kayıt içe/dışa aktarma vb.) en iyi seçenek olabilir.

> [!NOTE]
> DMF, Attract and Onboard için kullanılamaz.

### <a name="dmf-package-rest-api"></a>DMF paket REST API'sı

DMF, veri paketlerini yönetmek için bir [REST API'sı](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) sağlar. Bu API, DMF ile programlı bir şekilde etkileşimde bulunarak şöyle eylemlere olanak sağlamak için kullanılabilir:

- Bir veri paketini içe aktarma.

- Bir veri paketini dışa aktarma.

- İçe/dışa aktarma işleminin durumunu denetleme.

DMF Paketi REST API'si Human Resources'da tam olarak desteklenir.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF, ek olarak, İnsan Kaynakları'nın Microsoft Azure SQL veritabanınıza veri aktarabilmesini sağlayan güçlü bir özellik sağlar ([Kendi Veritabanınızı Getirin](/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) veya BYOD olarak bilinir). Bu özellik yüksek esneklik sağlar. Veriler kendi SQL veritabanınızdayken bir SQL veri deposuna bağlanabilen herhangi bir uygulamadan veya ara yazılımdan en iyi şekilde yararlanabilirsiniz.

BYOD, esas olarak salt okunur bir çözümdür. Azure SQL veritabanında istediğiniz her türlü veriyi (örneğin veri karmaları) yönetip depolayabilirsiniz ama Azure SQL veritabanında depolanan veriler yeniden Human Resources'a eşitlenmez.

BYOD, bir [Azure Data Factory](/azure/data-factory/) ardışık düzeni için veri kaynağı olarak raporlama çözümleri, veri tümleştirmeleri ve veri karmaları için uygundur.

> [!NOTE]
> BYOD, Attract and Onboard için kullanılamaz.

### <a name="odata-enabled-entities"></a>OData etkin varlıklar

Çoğu DMF varlığı İnsan Kaynakları veri hizmetine (OData) erişimi etkinleştirilmiş durumdadır. [Finance and Operations OData hizmeti](/dynamics365/unified-operations/dev-itpro/data-entities/odata) için sağlanan belgeler, kendi OData tarafından sağlanan varlıklarınızı oluşturmak dışında Human Resources için geçerlidir.

Dataverse ve Dataverse'in sağladığı OData uygulaması ([Dynamics 365 Web API](/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8)) üzerinden), İnsan Kaynakları veri hizmetine tercih edilmekle birlikte, İnsan Kaynakları veri hizmeti şu anda İnsan Kaynakları verileri için daha eksiksiz varlık kapsamına sahiptir.

### <a name="excel-add-in"></a>Excel Eklentisi

[Excel Eklentisi](/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) yüzeyin altındaki OData etkin varlıkların kullanılabilmesini sağlar. Bir son kullanıcının tanıdık Excel kullanıcı arabirimi yoluyla İnsan Kaynakları verilerini alması ve değiştirmesi için uygun bir yol sağlar.

Excel Eklentisi, iş etki alanı uzmanlarının özel verileri içe/dışa aktarmaları için uygundur. Programlı otomasyon gerektiren tekrarlı bir veri tümleştirmesi için, başka bir tümleştirme teknolojisi daha uygun olacaktır.

### <a name="data-integrator"></a>Veri Tümleştirici

Dataverse'a veri tümleştirmek veya bu uygulamadan veri tümleştirmek için [Veri Tümleştirme hizmetini](/powerapps/administrator/data-integrator) kullanabilirsiniz . Veri Tümleştirici, tümleştirme projelerini tanımlamak için kullanılabilir (bu projeler genellikle uygulama geliştiricilerinin belirli tümleştirmeler için özel olarak tasarladıkları ön tanımlı şablonlara dayanır). Tümleştirme projelerini yinelenen bir zaman planıyla otomatik olarak veya el ile çalıştırılmak üzere zamanlayabilirsiniz.

Veri Tümleştirici projeleri Dataverse toplu iş tümleştirmeleri için uygundur. Dynamics 365 uygulama ailesi arasındaki Tümleştirmeler için harika bir seçimdir. Örneğin Microsoft, Human Resources'tan alınan verileri Dynamics 365 Finance'a tümleştirmek için kullanılabilen bir Veri Tümleştirici şablonu sağlamaktadır. Şablon hakkında daha fazla bilgiyi [Dynamics 365 Human Resources'tan Dynamics 365 Finance'a tümleştirme](hr-admin-integration-finance.md) bölümünde bulabilirsiniz.

### <a name="power-query"></a>Power Query

Veri Tümleştirici [Power Query](/power-query/power-query-what-is-power-query)'yi de destekler ([Gelişmiş Sorgu özelliği](/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering) aracılığıyla). Power Query zengin M formül dili dahil güçlü, esnek veri filtreleme ve dönüştürme işlemi sağlar. Power BI raporları geliştirdiyseniz, Power Query büyük olasılıkla tanıdık gelecektir.

## <a name="deciding-on-an-integration-technology"></a>Bir tümleştirme teknolojisinde karar kılma

Bunca çeşitli tümleştirme teknolojileri mevcutken, kullanılacak tümleştirme yaklaşımında karar kılmak bazen bunaltıcı olabilir. Dataverse'teki veri kapsamı geliştikçe karar vermek kolaylaşacak, Dataverse çoğu durumda tercih edilen veri arabirimi haline gelecektir. Ancak o zamana kadar, Dataverse'in gereksinimlerinizi henüz karşılamadığını fark edebilirsiniz. Aşağıdaki tablo çeşitli tümleştirme teknolojisi seçeneklerinin bazı temel özelliklerini özetler.

| Teknoloji/Araç/API    | Yinelenen tümleştirmeler                   | Zaman uyumlu/Zaman uyumsuz                    | API aracılığıyla programlı erişim        | Uygun veri hacimleri                                   | Veri kapsamı                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Dataverse tabloları           | Evet, Veri Tümleştirici veya ara yazılım kullanarak | Zaman Uyumlu/Zaman Uyumsuz, Toplu (Veri Tümleştirici üzerinden) | Evet, Dynamics 365 Web API (OData) aracılığıyla | Kullanım durumuna göre değişir (etkileşimli kullanım için sayfalamayı destekler) | İyileştirme<sup>2</sup>                       |
| DMF varlıkları           | Evet, ara yazılım aracılığıyla zamanlanmış        | Zaman Uyumsuz, Toplu                                | Evet, DMF Paket REST API'sı         | Yüksek (yüz binlerce kayıt)                    | Yüksek                                |
| DMF Paket REST API'sı   | Evet, ara yazılım aracılığıyla zamanlanmış        | Zaman Uyumsuz, Toplu                                | Evet                                       | Yüksek (yüz binlerce kayıt)                    | API tüm DMF varlıklarını destekler       |
| BYOD                   | Evet, İnsan Kaynakları'nda yönetici tarafından zamanlanır        | Zaman Uyumsuz, Toplu                                | Hayır<sup>3</sup>                                    | Yüksek (yüz binlerce kayıt)                    | Tüm DMF varlıklarını destekler           |
| OData etkin varlıklar | Evet, ara yazılım kullanarak                    | Zaman Uyumlu                                        | Evet, İnsan Kaynakları Veri Hizmeti (OData) ile  | Kullanım durumuna göre değişir (etkileşimli kullanım için sayfalamayı destekler) | Yüksek                                |
| Excel Eklentisi           | Hayır                                       | Zaman Uyumlu                                        | Hayır                                        | Orta (on binlerce kayıt)                      | Tüm OData etkin varlıkları destekler |
| Veri Tümleştirici        | Evet, Veri Tümleştirici'de zamanlanır        | Zaman Uyumsuz, Toplu                                | No                                        | Kullanım durumuna göre değişir                                       | Tüm Dataverse tablolarını destekler           |

<sup>2</sup>Microsoft, Dataverse tabloları için veri kapsamını artırmaya büyük yatırım yapmaktadır. Kapsam kullanılabilir olduğunda Dataverse kullanmanızı öneririz. Şu anda Dataverse veri kapsamı DMF ve OData etkin varlıklara göre düşüktür.

<sup>3</sup>SQL veritabanına programlı olarak erişilebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
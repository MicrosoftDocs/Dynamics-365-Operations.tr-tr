---
title: Canlı eşitleme sorunlarını giderme
description: Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 73a226d10c951179fd9f3bc2aed4a70efcc7f020
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466256"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Canlı eşitleme sorunlarını giderme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, Finance and Operations uygulamaları ve Microsoft Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konunun ele aldığı sorunlardan bazıları sistem yöneticisi rolü veya Azure Active Directory (Azure AD) kiracısı yönetici kimlik bilgileri gerektirebilir. Her bölümde, belirli bir rol veya belirli kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Canlı eşitleme, bir satır oluşturduğunuzda hata gösteriyor

Finance and Operations uygulamasında bir satır oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:

*\[{\\"hata\\":{\\"kod\\":\\"0x80072560\\",\\"mesaj\\":\\"Kullanıcı kurumun bir üyesi değil.\\"}}\], Uzak sunucu hata gönderdi: (403) Yasak."}}".*

Bu sorunu gidermek için, [sistem gereksinimleri ve önkoşulları](requirements-and-prerequisites.md) adımlarını izleyin. Bu adımları tamamlamak için Dataverse uygulamasında oluşturulan çift yazma uygulaması kullanıcılarının sistem yöneticisi rolüne sahip olması gerekir. Varsayılan sahip olan takımın sistem yöneticisi rolü de olmalıdır.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Tablo verilerini kaydetmeye çalıştığınızda canlı eşitleme bir hata gösteriyor

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Tablo verilerini bir Finance and Operations uygulamasında kaydetmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*Değişiklikler veritabanına kaydedilemiyor. İş birimi, hareketi kaydedemiyor. Veriler varlık uyglarına yazılamıyor. UnitOfMeasureEntity yazma işlemi hata iletisiyle başarısız oldu varlık uoms ile eşitlenemiyor.*

Sorunu gidermek için hem Finance and Operations hem de Dataverse uygulamasında önkoşul başvuru verilerinin bulunduğundan emin olun. Örneğin, bir müşteri kaydı belirli bir müşteri grubuna aitse müşteri grubu kaydının Dataverse uygulamasında mevcut olduğundan emin olun.

Veriler her iki tarafta da varsa ve sorunun verilerle ilgili olmadığını doğruladıysanız aşağıdaki adımları izleyin.

1. Excel eklentisini kullanarak **DualWriteProjectConfigurationEntity** varlığını açın. Eklentiyi kullanmak için Finance and Operations Excel eklentisinde tasarım modunu etkinleştirin ve bir çalışma sayfasına **DualWriteProjectConfigurationEntity** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
2. Çift yazma eşlemesinde ve projede sorunları olan kayıtları seçin ve silin. Her çift yazma eşlemesi için iki kayıt vardır.
3. Excel eklentisini kullanarak değişiklikleri yayımlayın. Bu adım, varlıktan ve temel tablolardan kayıtları sildiği için önemlidir.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Bir Finance and Operations uygulamada veri oluşturduğunuzda okuma veya yazma ayrıcalık hatalarını işleme

Finance and Operations uygulamalarından birinde veri oluşturduğunuzda bir "Hatalı İstek" hata iletisi alabilirsiniz.

![Hatalı istek hata iletisi örneği.](media/error_record_id_source.png)

Sorunu gidermek için eşlenen Dynamics 365 Sales veya Dynamics 365 Customer Service departmanının takımına doğru güvenlik rolünü atayarak eksik ayrıcalığı etkinleştirmelisiniz.

1. Finance and Operations uygulamada, veri tümleştirme bağlantısı kümesinde eşlenen iş birimini bulun.

    ![Organizasyon eşleme.](media/mapped_business_unit.png)

2. Customer Engagement uygulamasındaki ortamda oturum açın, **Ayar \> Güvenlik** öğesine gidin ve eşlenen departmanın takımını bulun.

    ![Eşlenen departmanın ekibi.](media/setting_security_page.png)

3. Düzenleme için takımın sayfasını açın ve ardından **Rolleri yönet**'i seçin.

    ![Rolleri Yönet düğmesi.](media/manage_team_roles.png)

4. **Takım Rollerini Yönet** iletişim kutusunda, ilgili tablolar için okuma/yazma ayrıcalığına sahip rolü atayın ve ardından **Tamam**'ı seçin.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>En son değiştirilen Dataverse ortamı olan ortamlarda eşitleme sorunlarını giderme

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Finance and Operations uygulamasında bir veri oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**CustCustomerV3Entity varlığı için yük oluşturulamıyor**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Geçersiz URI hatasıyla yük oluşturma başarısız oldu: URI boş."}\],"isErrorCountUpdated":true}*

Customer Engagement uygulamasındaki hata iletisi şu şekilde görünür:

> ISV kodundan beklenmeyen bir hata oluştu. (ErrorType = ClientError) Eklentiden beklenmeyen özel durum (Yürüt): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: varlık hesabı işlenemedi: (Bağlanan taraf belirli bir süre içinde doğru şekilde yanıt vermediği için bir bağlantı girişimi başarısız oldu veya bağlanan ana bilgisayar yanıt vermediği için bağlantı kurulamadı.

Bu hata, Finance and Operations uygulamasında veri oluşturmaya çalıştığınızda Dataverse ortamı yanlış bir şekilde sıfırlanırsa oluşur.

> [!IMPORTANT]
> Ortamları yeniden bağladıysanız risk azaltma adımlarına devam etmeden önce tüm varlık eşlemelerini durdurmanız gerekir.

Sorunu gidermek için hem Dataverse hem de Finance and Operations uygulamasındaki adımları tamamlamanız gerekir.

1. Finance and Operations uygulamasında şu adımları izleyin:

    1. Excel eklentisini kullanarak **DualWriteProjectConfigurationEntity** varlığını açın. Eklentiyi kullanmak için Finance and Operations Excel eklentisinde tasarım modunu etkinleştirin ve bir çalışma sayfasına **DualWriteProjectConfigurationEntity** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
    2. Çift yazma eşlemesinde ve projede sorunları olan kayıtları seçin ve silin. Her çift yazma eşlemesi için iki kayıt vardır.
    3. Excel eklentisini kullanarak değişiklikleri yayımlayın. Bu adım, varlıktan ve temel tablolardan kayıtları sildiği için önemlidir.
    4. Finance and Operations veya Dataverse ortamlarını yeniden bağladığınızda hataları önlemeye yardımcı olmak için çift yazma yapılandırmalarının kalmadığından emin olun.

2. Dataverse uygulamasında şu adımları izleyin:

    1. Dataverse ortamınızda oturum açın (örneğin, `https://*****.crm.dynamics.com/`).
    2. **Gelişmiş Ayarlar** \> **Gelişmiş Bul**'a gidin.
    3. **DualWrite Çalışma Zamanı Yapılandırması**'nı seçin.
    4. Görüntülenecek sütunu seçin.
    5. Yapılandırmaları görüntülemek için **Sonuçlar**'ı seçin.
    6. Tüm kurulumları silin.

3. Finance and Operations uygulamasında şu adımları izleyin:

    1. Excel eklentisini kullanarak **DualWriteProjectConfigurationEntity** varlığını açın. Eklentiyi kullanmak için Finance and Operations Excel eklentisinde tasarım modunu etkinleştirin ve bir çalışma sayfasına **DualWriteProjectConfigurationEntity** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
    2. Çift yazma eşlemesinde ve projede sorunları olan kayıtları seçin ve silin. Her çift yazma eşlemesi için iki kayıt vardır.
    3. Excel eklentisini kullanarak değişiklikleri yayımlayın. Bu adım, varlıktan ve temel tablolardan kayıtları sildiği için önemlidir.
    4. Finance and Operations veya Dataverse ortamlarını yeniden bağladığınızda hataları önlemeye yardımcı olmak için çift yazma yapılandırmalarının kalmadığından emin olun.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Tam veritabanı kopyalaması yaptıktan sonra aldığınız canlı eşitleme hatası

Bir sistemden diğerine tam veritabanı kopyalaması çalıştırdıktan ve ardından bir veritabanı işlemi çalıştırmayı denedikten sonra aşağıdaki hata iletisini alabilirsiniz:

*SecureConfig Kuruluşu (???), mevcut CRM Kuruluşu (???) ile eşleşmiyor.*

Bir sistemde kurulan çift yazma yapılandırmasının başka bir sistemde kullanılamadığından emin olmak için çift yazma çalışma zamanı eklentisi, hata iletisi gösterir.

Sorunu gidermek için veritabanını geri yükledikten sonra **msdyn_dualwriteruntimeconfig** tablosundaki tüm kayıtları silin. Daha fazla bilgi için bkz. [Çift yazma ortamlarının bağlantısını kaldırma ve yeniden bağlama](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Çift yazma eşlemelerinde hatalı sorgu filtresi söz diziminin neden olduğu canlı eşitleme sorunları

Çift yazma eşlemesi filtresinin sorgu ifadesi, söz dizimi açısından doğru olsa da beklendiği gibi çalışmayabilir. Filtre ifadesi, bir sorgu nesnesinin tek tek veri kaynaklarında değil bir varlık üzerindedir. Bu nedenle, oluşturulan SQL sorgusu beklenen sonuçları döndürmez.

Aşağıda bir örnek verilmiştir.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Üst varlıkları olmayan projelerin filtrelenmesini bekleyebilirsiniz. Ancak filtre, aşağıdaki örneğe benzeyen bir sorguya çevrildiği için çalışmaz.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Gerçek sonuç, `parentProject` alanının `null` olarak değerlendirilmesidir. Ancak `null`, boş dizeyle aynı özelliklere sahip değildir. Bu uyumsuzluk nedeniyle sorgu filtresi geçerli sonuçlar döndürmez.

Sorunu düzeltmek için şu adımları izleyin.

1. Uzantı modeline eklenebilen ve `null` öğesini boş dizeye dönüştüren mantıkla desteklenen bir hesaplanan sütun ekleyin.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Varsayılan sütun yerine yeni hesaplanan sütundaki filtreyi kullanın.

Filtreyi bir geliştirme ortamında değerlendirmek için aşağıdaki X++ kodunu kullanarak sonuçları doğrulayabilirsiniz. Bu kodu tek başına program olarak çalıştırın. Bu filtreleri, çift yazma eşlemelerinde kullanmadan önce bir varlık için geçerli olan farklı filtre türlerini değerlendirmek üzere kullanabilirsiniz. Sorgu, uyuşmazlıkları değerlendirmek için veritabanında çalıştırılabilir.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Finance and Operations uygulamalarından gelen veriler Dataverse ile eşitlenmiyor

Canlı eşitleme sırasında, Finance and Operations uygulamalarındaki verilerin yalnızca bir kısmının Dataverse ile eşitlenmesi veya verilerin hiç eşitlenmemesi sorunuyla karşılaşabilirsiniz.

> [!NOTE]
> Geliştirme sırasında bu sorunu gidermeniz gerekir.

Sorunu gidermeye başlamadan önce aşağıdaki önkoşulları inceleyin:

+ Özel değişikliklerinizin tek bir hareket kapsamında yazıldığından emin olun.
+ İş olayları ve çift yazma çerçevesi `doinsert()`, `doUpdate()` ve `recordset()` işlemlerini veya `skipBusinessEvents(true)` öğesinin işaretlendiği kayıtları işlemez. Kodunuz bu işlevlerin içindeyse çift yazma tetiklenmez.
+ İş olayları, eşlenen veri kaynağı için kaydedilmelidir. Bazı veri kaynakları bir dış birleşim kullanabilir ve Finance and Operations uygulamalarında salt okunur olarak işaretlenebilir. Bu veri kaynakları izlenmez.
+ Değişiklikler, yalnızca eşlenen alanlardalarsa tetiklenir. Eşlenmemiş alan değişiklikleri çift yazmayı tetiklemez.
+ Filtre değerlendirmelerinin geçerli bir sonuç sağladığından emin olun.

### <a name="troubleshooting-steps"></a>Sorun giderme adımları

1. Çift yazma yönetici sayfasındaki alan eşlemelerini inceleyin. Alan, Finance and Operations uygulamalarından Dataverse uygulamasına eşlenmemişse izlenmez. Örneğin, aşağıdaki şekilde gösterilen **Açıklama** alanı Dataverse uygulamasından izlenir ancak Finance and Operations uygulamalarından izlenmez. Finance and Operations uygulamalarının içindeki bu alanda yapılan hiçbir değişiklik izlenmez.

    ![İzlenen alan.](media/live-sync-troubleshooting-1.png)

2. Veri kaynağının iş olayları tanımında izlenip izlenmediğini belirleyin. Örneğin, aşağıdaki şekilde gösterilen **DefaultDimensionDAVs** tablosundaki ve temel tablolardaki hiçbir alan değişiklikler için izlenmez. Dış birleşim kullanan ve salt okunur olarak işaretlenen veri kaynakları izlenmez.

    ![İzlenmeyen alan.](media/live-sync-troubleshooting-2.png)

3. Aşağıdaki şekilde gösterildiği gibi eşlenen tablo alanlarının **BUSINESSEVENTSDEFINITION** tablosunda görünüp görünmeyeceğini belirleyin. Aradığınız alanı sorgu sonucunda bulamıyorsanız çift yazma tarafından tetiklenmez.

    ![Tabloda izlenen alan.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Örnek senaryo

Finance and Operations uygulamalarında, ilgili kişi kaydının adresinde bir güncelleştirme var ancak adres değişikliği Dataverse ile eşitlenmiyor. Bu senaryo, **BusinessEventsDefinition** tablosundaki hiçbir kaydın etkilenen tablo ve varlığın birleşimine sahip olmaması nedeniyle oluşur. Özellikle, **LogisticsPostalAddress** tablosu **smmContactpersonCDSV2Entity** varlığı için doğrudan veri kaynağı değildir. **smmContactpersonCDSV2Entity** varlığının veri kaynağı **smmContactPersonV2Entity** öğesidir ve **smmContactPersonV2Entity** öğesinin veri kaynağı **LogisticsPostalAddressBaseEntity** öğesidir. **LogisticsPostalAddress** tablosu, **LogisticsPostalAddressBaseEntity** için veri kaynağıdır.

Benzer bir durum, Finance and Operations uygulamalarında değiştirilmekte olan tablonun onu içeren varlıkla açık bir şekilde bağlantılı olmadığı durumlar gibi bazı standart olmayan modellerde ortaya çıkabilir. Örneğin, birincil adres verileri **smmContactPersonCDSV2Entity** varlığı üzerinde hesaplanır. Çift yazma çerçevesi, temel tablodaki bir değişikliğin varlıklarla nasıl eşlendiğini belirlemeye çalışır. Genellikle bu yaklaşım yeterlidir. Ancak, bazı durumlarda bağlantı o kadar karmaşıktır ki açık bir şekilde belirtmeniz gerekir. İlgili tablonun **RecId** öğesinin doğrudan varlık üzerinde kullanılabilir olduğundan emin olmalısınız. Ardından, tablodaki değişiklikleri izlemek için statik bir yöntem ekleyin.

Örneğin, **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()** yöntemini inceleyin. **CustCustomerV3entity** ve **VendVendorV2Entity** öğeleri bu durumu çözmeye yönelik olarak değiştirildi.

Sorunu düzeltmek için şu adımları izleyin.

1. **smmContactPersonV2Entity** varlığına bir **PrimaryPostalAddressRecId** alanı ekleyin. Bu alanı şirket içi yapın.

    ![Alan, smmContactPersonV2Entity varlığına eklendi.](media/Troubleshoot_live_sync_issue_1.png)

2. Aynı alanı **smmContactPersonCDSV2Entity** varlığına ekleyin.

    ![Alan, smmContactPersonCDSV2Entity varlığına eklendi.](media/Troubleshoot_live_sync_issue_2.png)

3. Aşağıdaki yöntemi **smmContactPersonCDSV2Entity** sınıfına ekleyin.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Veritabanını eşitleyin ve uygulamayı derleyin.
5. **smmContactPersonCDSV2Entity** varlığında oluşturulan tüm çift yazma eşlemelerini durdurun.
6. Eşlemeyi başlatın. **BusinessEventsDefinition** tablosunda **refentityname** değerinin **smmContactPersonCDSV2Entity** değerine eşit olduğu satır için **RefTableName** sütununu kullanarak izlemeye başladığınız yeni tabloyu (bu örnekte **LogisticsPostalAddress**) görmelisiniz.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Finance and Operations uygulamasından Dataverse uygulamasına aynı toplu iş içinde birden çok kaydın gönderildiği bir kayıt oluşturduğunuzda oluşan hata

Finance and Operations uygulaması, herhangi bir hareket için verileri toplu iş olarak oluşturur ve bunları toplu iş olarak Dataverse uygulamasına gönderir. Aynı hareketin bir parçası olarak iki kayıt oluşturulursa ve bunlar birbirlerine başvurursa Finance and Operations uygulamasında aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:

*aaa_fundingsources varlığına veri yazılamıyor. {PC00...} değerleriyle ebecsfs_contracts öğesi aranamıyor. {PC00...} değerleriyle aaa_fundingsources öğesi aranamıyor. aaa_fundingsources öğesine yazma işlemi hata iletisiyle başarısız oldu. Özel durum iletisi: Uzak sunucu bir hata verdi: (400) Hatalı İstek.*

Sorunu gidermek için Finance and Operations uygulamasında iki varlığın birbiriyle ilişkili olduğunu ve ilgili kayıtların aynı harekette işlendiğini belirtmek için varlık ilişkileri oluşturun.

## <a name="enable-verbose-logging-of-error-messages"></a>Hata iletilerinin ayrıntılı günlük kaydını etkinleştirme

Finance and Operations uygulamasında, Dataverse ortamıyla ilgili hatalarla karşılaşabilirsiniz. Hata iletisi, iletinin tam metnini veya diğer ilgili verileri içermeyebilir. Daha fazla bilgi almak için Finance and Operations uygulamalarındaki tüm proje yapılandırmalarındaki **DualWriteProjectConfigurationEntity** varlığında bulunan **IsDebugMode** bayrağını ayarlayarak ayrıntılı günlük kaydını etkinleştirebilirsiniz.

1. Excel eklentisini kullanarak **DualWriteProjectConfigurationEntity** varlığını açın. Eklentiyi kullanmak için Finance and Operations Excel eklentisinde tasarım modunu etkinleştirin ve bir çalışma sayfasına **DualWriteProjectConfigurationEntity** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
2. Projede **IsDebugMode** bayrağını **Evet** olarak ayarlayın.
3. Senaryoyu çalıştırın.
4. Ayrıntılı günlükler **DualWriteErrorLog** tablosunda bulunur. Tablo tarayıcısını kullanarak veri aramak için aşağıdaki URL'yi kullanın: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Hata ayıklama modunda daha fazla günlük yakalamak için [KB 4595434 (Çift yazma canlı eşitlemesinde yayılan boş değerler için düzeltme)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9) güncelleştirmesini yükleyin.

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Müşteri veya ilgili kişi için adres eklediğinizde oluşan hata

Finance and Operations uygulamalarında veya Dataverse uygulamasında bir müşteri veya ilgili kişi için adres eklemeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*msdyn_partypostaladresses varlığına veri yazılamıyor. DirPartyPostalAddressLocationCDSEntity öğesine yazma işlemi hata iletisiyle başarısız oldu İstek, BadRequest durum koduyla ve CDS hata koduyla başarısız oldu: 0x80040265 yanıt iletisi: Eklentide bir hata oluştu. Konum Kimliği öznitelik değerlerine sahip bir kayıt zaten var. Varlık anahtarı Konum Kimliği Anahtarı, bu öznitelik kümesinin benzersiz değerler içermesini gerektirir. Benzersiz değerler seçin ve tekrar deneyin.*

Sorunu gidermek için çift yazma düzenleme paketi sürümünü (2.2.2.60) yükleyin, böylece **Adres** tablosundaki anahtarlar, aşağıdaki tabloda gösterildiği gibi tanımlanır.

| Özellik | Değer |
|---|---|
| Görünen Ad | **Konum Anahtarı** |
| Kuruluş adı | **msdyn_locationkey** |
| Alanlar | **msdyn_locationid**, **parentid** |
| Çalıştırma Durumu | **Active** |
| Sistem işi | Boş |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Dataverse uygulamasında bir müşteri eklediğinizde oluşan hata

Dataverse uygulamasında bir müşteri eklemeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*"RecordError0":"Bilinmeyen özel durum ile Müşteriler V3 varlığı için yazma başarısız oldu - "Kuruluş" taraf türü için taraf kaydı bulunamadı"}.*

Dataverse uygulamasında bir müşteri oluşturulduğunda yeni bir parti numarası oluşturulur. Müşteri kaydı, tarafla birlikte Finance and Operations uygulamalarına eşitlenirse ancak farklı bir taraf numarasına sahip bir müşteri kaydı zaten varsa hata iletisi görüntülenir.

Sorunu gidermek için müşteriyi taraf araması yoluyla bulun. Müşteri yoksa yeni bir müşteri kaydı oluşturun. Müşteri varsa yeni müşteri kaydını oluşturmak için mevcut tarafı kullanın.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Dataverse uygulamasında yeni bir müşteri, satıcı veya ilgili kişi oluşturduğunuzda oluşan hata

Dataverse uygulamasında yeni bir müşteri, satıcı veya ilgili kişi oluşturmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*Bir tarafın türü "DirOrganization"dan "DirPerson"a güncelleştirilemez, bunun yerine mevcut tarafın silinmesi ve ardından eklenen yeni türle gerçekleştirilmesi gerekir.*

Dataverse uygulamasındaki **msdyn_party** tablosunda bir numara sırası bulunur. Dataverse uygulamasında bir hesap oluşturulduğunda yeni bir taraf oluşturulur (örneğin, **Kuruluş** türünde **Party-001**). Bu veriler Finance and Operations uygulamasına gönderilir. Dataverse ortamı sıfırlanırsa veya Finance and Operations ortamı farklı bir Dataverse ortamına bağlanırsa ve ardından Dataverse uygulamasında yeni bir ilgili kişi kaydı oluşturulursa **Party-001** ile başlayan yeni bir taraf değeri oluşturulur. Bu kez, oluşturulan parti kaydı **Kişi** türündeki **Party-001** olur. Bu veriler eşitlendiğinde **Kuruluş** türündeki **Party-001** taraf kaydı zaten mevcut olduğundan Finance and Operations uygulamaları önceki hata iletisini görüntüler.

Sorunu gidermek için Dataverse uygulamasındaki **msdyn_party** tablosunun **msdyn_partynumber** alanındaki otomatik numara sırasını farklı bir otomatik numara sırasıyla değiştirin.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Müşteri veya ilgili kişi eşlemeleriyle ilgili performans sorunu

**getEntityDataSourceToFieldMapping** yöntemini (**CustCustomerV3Entity** varlığındaki) ve **getEntityDataSourceToFieldMapping** yöntemini (**smmContactPersonCDSV2Entity** varlığındaki) özelleştirerek müşteriler ve ilgili kişiler için canlı eşitleme performansını az da olsa artırabilirsiniz. Bu özelleştirmeler, **BusinessEventsDefinition** tablosundaki kayıt sayısını azaltır. Kayıt sayısındaki bu azalma, oluşturulan olay sayısını da azaltır.

**CustCustomerV3Entity** varlığındaki **getEntityDataSourceToFieldMapping** yöntemi, müşterinin elektronik adresinin veya posta adresinin güncelleştirilmesinin iş olaylarını tetiklemesini ve böylece güncelleştirilen verilerin Dataverse uygulamasına gönderilmesini sağlar. Tüm alanları kullanmıyorsanız ve çift yazmada bilgiye ihtiyacınız yoksa yöntemdeki uygun satırları derleme dışında bırakın. Bu yöntemle eklenen her izlenen alan ve tablo, **BusinessEventsDefinition** tablosuna izlenen tablo ve izlenen varlığın birleşimi için bir kayıt ekler.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Benzer şekilde, **smmContactPersonCDSV2Entity** varlığındaki **getEntityDataSourceToFieldMapping** yöntemi, ilgili kişinin elektronik adresi veya posta adresindeki herhangi bir güncelleştirmenin iş olaylarını tetiklemesini ve böylece güncelleştirilen verilerin Dataverse uygulamasına gönderilmesini sağlar. Yöntemde, kullanmadığınız alanlar için satırları derleme dışında bırakabilirsiniz.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Yöntemleri güncelleştirdikten sonra şu adımları izleyin.

1. Veritabanını eşitleyin ve uygulamayı derleyin.
2. **smmContactPersonCDSV2Entity** ve **CustCustomerV3Entity** varlıklarındaki tüm çift yazma eşlemelerini durdurun.
3. Eşlemeleri başlatın. **smmContactPersonCDSV2Entity** ve **CustCustomerV3Entity** varlıklarında ve **BusinessEventsDefinition** tablosunda daha az kayıt görmelisiniz ve performans az da olsa artabilir.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

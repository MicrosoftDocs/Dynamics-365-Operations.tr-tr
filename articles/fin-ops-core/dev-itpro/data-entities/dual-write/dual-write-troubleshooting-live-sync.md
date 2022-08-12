---
title: Canlı eşitleme sorunlarını giderme
description: Bu makalede,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlanmaktadır.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 1211f7da15686f1c55a4c942f04c73d671e0ba6b
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111441"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Canlı eşitleme sorunlarını giderme

[!include [banner](../../includes/banner.md)]



Bu makalede, finans ve operasyon uygulamaları ile Microsoft Dataverse arasında çift yazma tümleştirmesi hakkında sorun giderme bilgileri sağlanmaktadır. Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu makalenin ele aldığı sorunlardan bazıları sistem yöneticisi rolü veya Azure Active Directory (Azure AD) kiracısı yönetici kimlik bilgileri gerektirebilir. Her bölümde, belirli bir rol veya belirli kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Canlı eşitleme, bir satır oluşturduğunuzda hata gösteriyor

Finans ve operasyon uygulamasında bir satır oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:

*\[{\\"hata\\":{\\"kod\\":\\"0x80072560\\",\\"mesaj\\":\\"Kullanıcı kurumun bir üyesi değil.\\"}}\], Uzak sunucu hata gönderdi: (403) Yasak."}}".*

Bu sorunu gidermek için, [sistem gereksinimleri ve önkoşulları](requirements-and-prerequisites.md) adımlarını izleyin. Bu adımları tamamlamak için Dataverse uygulamasında oluşturulan çift yazma uygulaması kullanıcılarının sistem yöneticisi rolüne sahip olması gerekir. Varsayılan sahip olan takımın sistem yöneticisi rolü de olmalıdır.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Tablo verilerini kaydetmeye çalıştığınızda canlı eşitleme bir hata gösteriyor

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Tablo verilerini bir finans ve operasyon uygulamasına kaydetmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*Değişiklikler veritabanına kaydedilemiyor. İş birimi, hareketi kaydedemiyor. Veriler varlık uyglarına yazılamıyor. UnitOfMeasureEntity yazma işlemi hata iletisiyle başarısız oldu varlık uoms ile eşitlenemiyor.*

Sorunu gidermek için ön koşul referans verilerinin hem finans ve operasyon uygulamasında hem de Dataverse'te yer aldığından emin olun. Örneğin, bir müşteri kaydı belirli bir müşteri grubuna aitse müşteri grubu kaydının Dataverse uygulamasında mevcut olduğundan emin olun.

Veriler her iki tarafta da varsa ve sorunun verilerle ilgili olmadığını doğruladıysanız aşağıdaki adımları izleyin.

1. Excel eklentisini kullanarak **DualWriteProjectConfigurationEntity** varlığını açın. Eklentiyi kullanmak için finans ve operasyon Excel eklentisinde tasarım modunu etkinleştirin ve sayfaya **DualWriteProjectConfigurationEntity** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
2. Çift yazma eşlemesinde ve projede sorunları olan kayıtları seçin ve silin. Her çift yazma eşlemesi için iki kayıt vardır.
3. Excel eklentisini kullanarak değişiklikleri yayımlayın. Bu adım, varlıktan ve temel tablolardan kayıtları sildiği için önemlidir.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Finans ve operasyon uygulamasında veri oluşturduğunuzda okuma veya yazma ayrıcalığı hatalarını işleme

Bir finans ve operasyon uygulamasında veri oluşturduğunuzda "Hatalı İstek" hata iletisi alabilirsiniz.

![Hatalı istek hata iletisi örneği.](media/error_record_id_source.png)

Sorunu gidermek için eşlenen Dynamics 365 Sales veya Dynamics 365 Customer Service departmanının takımına doğru güvenlik rolünü atayarak eksik ayrıcalığı etkinleştirmelisiniz.

1. Finans ve operasyon uygulamasında, Veri Tümleştirme bağlantı kümesinde eşlenen departmanı bulun.

    ![Organizasyon eşleme.](media/mapped_business_unit.png)

2. Customer Engagement uygulamasındaki ortamda oturum açın, **Ayar \> Güvenlik** öğesine gidin ve eşlenen departmanın takımını bulun.

    ![Eşlenen departmanın ekibi.](media/setting_security_page.png)

3. Düzenleme için takımın sayfasını açın ve ardından **Rolleri yönet**'i seçin.

    ![Rolleri Yönet düğmesi.](media/manage_team_roles.png)

4. **Takım Rollerini Yönet** iletişim kutusunda, ilgili tablolar için okuma/yazma ayrıcalığına sahip rolü atayın ve ardından **Tamam**'ı seçin.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>En son değiştirilen Dataverse ortamı olan ortamlarda eşitleme sorunlarını giderme

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Bir finans ve operasyon uygulamasında veri oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**CustCustomerV3Entity varlığı için yük oluşturulamıyor**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Geçersiz URI hatasıyla yük oluşturma başarısız oldu: URI boş."}\],"isErrorCountUpdated":true}*

Customer Engagement uygulamasındaki hata iletisi şu şekilde görünür:

> ISV kodundan beklenmeyen bir hata oluştu. (ErrorType = ClientError) Eklentiden beklenmeyen özel durum (Yürüt): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: varlık hesabı işlenemedi: (Bağlanan taraf belirli bir süre içinde doğru şekilde yanıt vermediği için bir bağlantı girişimi başarısız oldu veya bağlanan ana bilgisayar yanıt vermediği için bağlantı kurulamadı.

Bu hata, finans ve operasyon uygulamasında veri oluşturmaya çalıştığınızda Dataverse ortamı yanlış sıfırlanırsa oluşur.

> [!IMPORTANT]
> Ortamları yeniden bağladıysanız risk azaltma adımlarına devam etmeden önce tüm varlık eşlemelerini durdurmanız gerekir.

Sorunu gidermek için hem Dataverse hem de finans ve operasyon uygulamasındaki adımları tamamlamanız gerekir.

1. Finans ve operasyon uygulamasında şu adımları izleyin:

    1. Excel eklentisini kullanarak **DualWriteProjectConfigurationEntity** varlığını açın. Eklentiyi kullanmak için finans ve operasyon Excel eklentisinde tasarım modunu etkinleştirin ve sayfaya **DualWriteProjectConfigurationEntity** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
    2. Çift yazma eşlemesinde ve projede sorunları olan kayıtları seçin ve silin. Her çift yazma eşlemesi için iki kayıt vardır.
    3. Excel eklentisini kullanarak değişiklikleri yayımlayın. Bu adım, varlıktan ve temel tablolardan kayıtları sildiği için önemlidir.
    4. Finans ve operasyon veya Dataverse ortamlarını yeniden bağladığınızda hataları önlemeye yardımcı olmak için çift yazma yapılandırması kalmadığından emin olun.

2. Dataverse uygulamasında şu adımları izleyin:

    1. Dataverse ortamınızda oturum açın (örneğin, `https://*****.crm.dynamics.com/`).
    2. **Gelişmiş Ayarlar** \> **Gelişmiş Bul**'a gidin.
    3. **DualWrite Çalışma Zamanı Yapılandırması**'nı seçin.
    4. Görüntülenecek sütunu seçin.
    5. Yapılandırmaları görüntülemek için **Sonuçlar**'ı seçin.
    6. Tüm kurulumları silin.

3. Finans ve operasyon uygulamasında şu adımları izleyin:

    1. Excel eklentisini kullanarak **DualWriteProjectConfigurationEntity** varlığını açın. Eklentiyi kullanmak için finans ve operasyon Excel eklentisinde tasarım modunu etkinleştirin ve sayfaya **DualWriteProjectConfigurationEntity** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
    2. Çift yazma eşlemesinde ve projede sorunları olan kayıtları seçin ve silin. Her çift yazma eşlemesi için iki kayıt vardır.
    3. Excel eklentisini kullanarak değişiklikleri yayımlayın. Bu adım, varlıktan ve temel tablolardan kayıtları sildiği için önemlidir.
    4. Finans ve operasyon veya Dataverse ortamlarını yeniden bağladığınızda hataları önlemeye yardımcı olmak için çift yazma yapılandırması kalmadığından emin olun.

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

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Finans ve operasyon uygulamalarından gelen veriler Dataverse'e eşitlenmiyor

Canlı eşitleme sırasında, verilerin yalnızca bir kısmının finans ve operasyon uygulamalarından Dataverse'e eşitlenmesine veya verilerin hiç eşitlenmemesine neden olan bir sorunla karşılaşabilirsiniz.

> [!NOTE]
> Geliştirme sırasında bu sorunu gidermeniz gerekir.

Sorunu gidermeye başlamadan önce aşağıdaki önkoşulları inceleyin:

+ Özel değişikliklerinizin tek bir hareket kapsamında yazıldığından emin olun.
+ İş olayları ve çift yazma çerçevesi `doinsert()`, `doUpdate()` ve `recordset()` işlemlerini veya `skipBusinessEvents(true)` öğesinin işaretlendiği kayıtları işlemez. Kodunuz bu işlevlerin içindeyse çift yazma tetiklenmez.
+ İş olayları, eşlenen veri kaynağı için kaydedilmelidir. Bazı veri kaynakları dış birleşim kullanabilir ve yalnızca finans ve operasyon uygulamalarında okundu olarak işaretlenebilir. Bu veri kaynakları izlenmez.
+ Değişiklikler, yalnızca eşlenen alanlardalarsa tetiklenir. Eşlenmemiş alan değişiklikleri çift yazmayı tetiklemez.
+ Filtre değerlendirmelerinin geçerli bir sonuç sağladığından emin olun.

### <a name="troubleshooting-steps"></a>Sorun giderme adımları

1. Çift yazma yönetici sayfasındaki alan eşlemelerini inceleyin. Bir alan finans ve operasyon uygulamalarından Dataverse'e eşlenmemişse izlenmez. Örneğin, aşağıdaki çizimde, **Açıklama** alanı Dataverse'ten izlenir ancak finans ve operasyon uygulamalarından izlenmez. Finans ve operasyon uygulamalarında bu alanda yapılan hiçbir değişiklik izlenmeyecektir.

    ![İzlenen alan.](media/live-sync-troubleshooting-1.png)

2. Veri kaynağının iş olayları tanımında izlenip izlenmediğini belirleyin. Örneğin, aşağıdaki şekilde gösterilen **DefaultDimensionDAVs** tablosundaki ve temel tablolardaki hiçbir alan değişiklikler için izlenmez. Dış birleşim kullanan ve salt okunur olarak işaretlenen veri kaynakları izlenmez.

    ![İzlenmeyen alan.](media/live-sync-troubleshooting-2.png)

3. Aşağıdaki şekilde gösterildiği gibi eşlenen tablo alanlarının **BUSINESSEVENTSDEFINITION** tablosunda görünüp görünmeyeceğini belirleyin. Aradığınız alanı sorgu sonucunda bulamıyorsanız çift yazma tarafından tetiklenmez.

    ![Tabloda izlenen alan.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Örnek senaryo

Finans ve operasyon uygulamalarında, bir kişi kaydının adresinde bir güncelleştirme vardır ancak adres değişikliği Dataverse ile eşitlenmez. Bu senaryo, **BusinessEventsDefinition** tablosundaki hiçbir kaydın etkilenen tablo ve varlığın birleşimine sahip olmaması nedeniyle oluşur. Özellikle, **LogisticsPostalAddress** tablosu **smmContactpersonCDSV2Entity** varlığı için doğrudan veri kaynağı değildir. **smmContactpersonCDSV2Entity** varlığının veri kaynağı **smmContactPersonV2Entity** öğesidir ve **smmContactPersonV2Entity** öğesinin veri kaynağı **LogisticsPostalAddressBaseEntity** öğesidir. **LogisticsPostalAddress** tablosu, **LogisticsPostalAddressBaseEntity** için veri kaynağıdır.

Benzer bir durum, finans ve operasyon uygulamalarında değiştirilen tablonun açıkça onu içeren varlığa bağlı olmadığı durumlar gibi bazı standart dışı desenlerde de oluşabilir. Örneğin, birincil adres verileri **smmContactPersonCDSV2Entity** varlığı üzerinde hesaplanır. Çift yazma çerçevesi, temel tablodaki bir değişikliğin varlıklarla nasıl eşlendiğini belirlemeye çalışır. Genellikle bu yaklaşım yeterlidir. Ancak, bazı durumlarda bağlantı o kadar karmaşıktır ki açık bir şekilde belirtmeniz gerekir. İlgili tablonun **RecId** öğesinin doğrudan varlık üzerinde kullanılabilir olduğundan emin olmalısınız. Ardından, tablodaki değişiklikleri izlemek için statik bir yöntem ekleyin.

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

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Finans ve operasyon uygulamasından aynı toplu işlemdeki Dataverse'e birden çok kaydın gönderildiği bir kayıt oluşturduğunuzda hata oluştu

Herhangi bir işlem için, finans ve operasyon uygulaması bir toplu işlemde veri oluşturur ve bunu Dataverse'e toplu iş olarak gönderir. Aynı işlemin parçası olarak iki kayıt oluşturulursa ve birbirlerine başvuruyorlarsa finans ve operasyon uygulamasında aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:

*aaa_fundingsources varlığına veri yazılamıyor. {PC00...} değerleriyle ebecsfs_contracts öğesi aranamıyor. {PC00...} değerleriyle aaa_fundingsources öğesi aranamıyor. aaa_fundingsources öğesine yazma işlemi hata iletisiyle başarısız oldu. Özel durum iletisi: Uzak sunucu bir hata verdi: (400) Hatalı İstek.*

Sorunu gidermek için finans ve operasyon uygulamasında iki varlığın birbiriyle ilişkili olduğunu ve ilgili kayıtların aynı işlemde işlendiğini belirtmek için varlık ilişkileri oluşturun.

## <a name="enable-verbose-logging-of-error-messages"></a>Hata iletilerinin ayrıntılı günlük kaydını etkinleştirme

Finans ve operasyon uygulamasında, Dataverse ortamıyla ilgili hatalarla karşılaşabilirsiniz. Hata iletisi, iletinin tam metnini veya diğer ilgili verileri içermeyebilir. Daha fazla bilgi almak için finans ve operasyon uygulamalarındaki tüm proje yapılandırmalarında **DualWriteProjectConfigurationEntity** varlığında bulunan **IsDebugMode** bayrağını ayarlayarak ayrıntılı günlüğü etkinleştirebilirsiniz.

1. Excel eklentisini kullanarak **DualWriteProjectConfigurationEntity** varlığını açın. Eklentiyi kullanmak için finans ve operasyon Excel eklentisinde tasarım modunu etkinleştirin ve sayfaya **DualWriteProjectConfigurationEntity** öğesini ekleyin. Daha fazla bilgi için bkz. [Varlık verilerini Excel ile görüntüleme ve güncelleştirme](../../office-integration/use-excel-add-in.md).
2. Projede **IsDebugMode** bayrağını **Evet** olarak ayarlayın.
3. Senaryoyu çalıştırın.
4. Ayrıntılı günlükler **DualWriteErrorLog** tablosunda bulunur. Tablo tarayıcısını kullanarak veri aramak için aşağıdaki URL'yi kullanın: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Hata ayıklama modunda daha fazla günlük yakalamak için [BB 4595434 (Çift yazma canlı eşitlemesinde yayılan boş değerler için düzeltme)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9) güncelleştirmesini yükleyin.

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Müşteri veya ilgili kişi için adres eklediğinizde oluşan hata

Finans ve operasyon uygulamalarında veya Dataverse'te bir müşteri veya ilgili kişi için adres eklemeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

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

Dataverse uygulamasında bir müşteri oluşturulduğunda yeni bir parti numarası oluşturulur. Hata iletisi, müşteri kaydı karşı tarafla birlikte finans ve operasyon uygulamalarıyla eşitlendiğinde ancak zaten farklı bir taraf numarasına sahip bir müşteri kaydı olduğunda gösterilir.

Sorunu gidermek için müşteriyi taraf araması yoluyla bulun. Müşteri yoksa yeni bir müşteri kaydı oluşturun. Müşteri varsa yeni müşteri kaydını oluşturmak için mevcut tarafı kullanın.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Dataverse uygulamasında yeni bir müşteri, satıcı veya ilgili kişi oluşturduğunuzda oluşan hata

Dataverse uygulamasında yeni bir müşteri, satıcı veya ilgili kişi oluşturmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*Bir tarafın türü "DirOrganization"dan "DirPerson"a güncelleştirilemez, bunun yerine mevcut tarafın silinmesi ve ardından eklenen yeni türle gerçekleştirilmesi gerekir.*

Dataverse uygulamasındaki **msdyn_party** tablosunda bir numara sırası bulunur. Dataverse uygulamasında bir hesap oluşturulduğunda yeni bir taraf oluşturulur (örneğin, **Kuruluş** türünde **Party-001**). Bu veriler finans ve operasyon uygulamasına gönderilir. Dataverse ortamı sıfırlanırsa veya finans ve operasyon ortamı farklı bir Dataverse ortamına bağlanırsa ve sonra Dataverse'te yeni bir ilgili kişi kaydı oluşturulursa **Party-001** ile başlayan yeni bir taraf değeri oluşturulur. Bu kez, oluşturulan parti kaydı **Kişi** türündeki **Party-001** olur. Bu veriler eşitlendiğinde, **Kuruluş** türünde taraf kaydı **Party-001** zaten var olduğu için finans ve operasyon uygulamaları önceki hata iletisini gösterir.

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


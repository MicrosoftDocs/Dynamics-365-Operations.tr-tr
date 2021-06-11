---
title: Dataverse sanal tablo sorgularını iyileştirme
description: Dataverse sanal tablo sorgularının performansını en iyi duruma getirme ve sorunları giderme
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054920"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Dataverse sanal tablo sorgularını iyileştirme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Çıkış

### <a name="overview"></a>Genel bakış

Dynamics 365 Human Resources ile tümleştirme ve diğer veri bağlantılarını geliştirmek için Dataverse sanal tablolarını kullanırken, sanal tablolara yönelik sorgularda performans sorunlarıyla karşılaşabilirsiniz. Çeşitli istemciler veya arabirimler arasında yavaş sorgu yürütme gerçekleşebilir. Örneğin, aşağıdaki durumlarda sorunla karşılaşabilirsiniz:

- Dataverse Web API ile bir sanal tablo sorgularken
- Sanal tabloya karşı bir Power App oluştururken
- Sanal tabloda Power BI raporu oluştururken

Tüm bu arabirimlerin performans sorunu oluşturma olasılığı vardır.

Human Resources için Dataverse sanal tablo performansının yavaş olmasının bir nedeni, tablonun [gezinti özellikleriyle](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) ilgili sanal tablonun yabancı anahtar sütunlarıdır. Sanal bir tablo için gezinme özellikleri oluşturulduğunda, ilişkili sanal tablonun anahtar sütunu için anahtarın değerini temsil etmek üzere tabloya bir yabancı anahtar sütunu otomatik olarak eklenir. Örneğin, **mshr_hcmworkerbaseentity** varlığına **mshr_dirpersonentity** varlığından alınan yabanco anahtar özelliğiyle **_mshr_fk_person_id_value** sütunu eklenir. Bu yabancı anahtar sütunu değerlerinin tabloda tutulma şekli nedeniyle, değerlerin getirilmesi sanal tabloyla ilgili sorgu performansı üzerinde olumsuz etkiye sahip olabilir.

### <a name="potential-symptoms"></a>Olası belirtiler

Bu etkiyi örneğin Çalışan (**mshr_hcmworkerentity**) veya temel çalışan (**mshr_hcmworkerbaseentity**) varlığı için yapılan sorgularda görebilirsiniz. Performans sorunu bildiriminin kendisini birkaç farklı yolla görebilirsiniz:

- **Yavaş sorgu yürütme**: Sanal tabloya yönelik sorgu beklenen sonuçları döndürebilir ancak sorgu yürütmenin tamamlaması beklenenden uzun sürebilir.
- **Sorgu zaman aşımı**: Sorgu zaman aşımına uğrayabilir ve şu hatayı döndürebilir: "Finance and Operations'ı çağırmak için bir belirteç alındı ancak Finance and Operations InternalServerError türünde bir hata döndürdü."
- **Beklenmeyen hata**: Sorgu şu iletiyle birlikte 400 hata türünü döndürebilir: "Beklenmeyen bir hata oluştu."

  ![HcmWorkerBaseEntity üzerinde 400 hata türü](./media/HcmWorkerBaseEntityErrorType400.png)

- **Azaltma**: Sorgu sunucu kaynaklarını aşırı kullanabilir ve azaltmaya maruz olabilir. Bu durumda, sorgu şu hatayı döndürür: "Finance and Operations'ı çağırmak için bir belirteç alındı ancak Finance and Operations 429 türünde bir hata döndürdü." Human Resources'ta azaltma konusunda daha fazla bilgi için bkz. [Azaltmayla ilgili SSS](./hr-admin-integration-throttling-faq.md).

  ![HcmWorkerBaseEntity üzerinde 429 hata türü](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Çözünürlük

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Veri sorgunuz dahil edilen sütunların sayısını sınırlayın

Sanal tablolarla, sorgu performansını artırmak için en büyük potansiyeli olan yöntemlerden biri sorguda seçilen sütun sayısını sınırlandırmaktır. Sorgu performansını en iyi duruma getirmek için genel yöntem, sorgunuzdaki sütunları yalnızca gereksinim duyduğunuz özelliklerle sınırlandırmaktır. Bu özellikle, sanal tablolardaki yabancı anahtar sütunları için geçerlidir. Tümleştirmeniz veya raporunuz için yabancı anahtar sütunlarında bulunan değerlere gereksinim duymuyorsanız, sorguyu yabancı anahtar sütunlarını hariç tutarak yalnızca gereksinim duyduğunuz sütunları seçerek yapılandırın.

#### <a name="selecting-columns-in-an-odata-query"></a>OData sorgusunda sütun seçme

Dataverse Web API ile bir sanal tabloyu sorgularken, **$select** sistem sorgusu seçeneğini kullanarak sorguda bulunan sütunların sayısını sınırlayabilir ve sonuç döndürülmesi gereken sütunları tanımlayabilirsiniz. Performansı en üst düzeye çıkarmak için, yabancı anahtar sütunlarını (**_mshr_FK_** önekine sahip olan sütunlar) sorgunun dışında tutun.

Örneğin, **mshr_hcmworkerbaseentity** varlığı için aşağıdaki sorgu yalnızca **$select** sorgu seçeneği tümcesine dahil edilen sütunları içerecek ve yabancı anahtar değerleri dışarıda bırakılacaktır. Bu, tüm tablo sütunlarını içeren bir sorguya göre performans açısından önemli iyileşme sağlar.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Seçili sütun sayısını sınırlama önerisi, sorguyu ilgili sanal tablolara gezinti özellikleri üzerinden genişletmek için **$expand** sorgu seçeneği kullanılırken de geçerlidir. Örneğin, aşağıdaki sorgu **mshr_dirpersonentity** varlığından genişletilen sütunlarla birlikte **mshr_hcmworkerbaseentity** varlığındaki sütunları içerir. **$select** sorgu seçeneğinin aynı zamanda **$expand** sorgu seçeneği yan tümcesine dahil edildiğini unutmayın.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

**$expand** soru seçeneği yan tümcesinde **$select** sorgu seçeneğiyle veri alma yöntemini kullanırken, varlıklar arasındaki gezinme özelliği çok-bir ilişki olduğunda genellikle daha fazla performans artışı elde edersiniz. Bir-çok ilişkisini genişletirken sorgu yürütme süresinde aynı azalmayı göremezsiniz. Dataverse sanal tabloları için ilişki tanımı hakkında daha fazla bilgi edinmek için bkz. [Tablo ilişkileri](/powerapps/maker/data-platform/create-edit-entity-relationships).

Dataverse Web API'da **$select** ve **$expand** sistem sorgusunu kullanma hakkında daha fazla bilgi için bkz. [Sorguyla ilgili varlık kayıtlarını alma](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Power BI'da sütunları seçme

Dataverse sanal bir tablosu için Power BI raporu oluştururken yukarıda sözü edilen yavaş performans göstergelerinin herhangi biriyle karşılaşırsanız, rapor tablosunda yabancı anahtar sütunlarını seçili sütunların dışında bırakarak performansı artırabilirsiniz. Örneğin, **mshr_hcmworkerbaseentity** varlığına karşı bir rapor oluşturmak için Power BI Desktop kullanıyorsanız rapor sorgusuna eklemek istediğiniz sütunları seçmek için aşağıdaki adımları kullanabilirsiniz.

1. Power BI Desktop'ta eylem şeridindeki **Veri al** açılır listesinden **Daha fazla...** seçeneğini seçin.
2. **Veri Al** penceresinde, arama kutusuna **Common Data Service** yazıp **Common Data Service** bağlayıcısını ve **Bağlan**'ı seçin.
3. Common Data Service penceresinin **Sunucu URL**'si alanına, Dataverse ortamınızın kuruluş URI'sını girip **Tamam**'ı seçin.
  
   ![Dataverse ortamınız için URI girin](./media/PowerBIDataverseURLSetup.png)
  
4. Gezgin penceresinde, **Varlıklar** düğümünü genişletin.
5. Arama kutusuna **mshr_hcmworkerbaseentity** girin ve varlığı seçin.
6. **Verileri Dönüştür**'ü seçin.
7. Power Query Düzenleyici penceresinde, **Gelişmiş Düzenleyici**'yi seçin.
8. **Gelişmiş Düzenleyici** penceresinde, gerektiğinde diziye sütun ekleyerek veya kaldırarak sorguyu aşağıdaki gibi görünecek şekilde güncelleştirin.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Power Query Düzenleyicisi için Gelişmiş Düzenleyici'de sorguyu güncelleştirme](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. **Tamam**'ı seçin.

   > [!NOTE]
   > Güncelleştirmeden önce sorgudan 429 türünde bir hata aldıysanız, sorgunun başarıyla tamamlanması için sorguyu yenilemeden önce yeniden deneme süresinin dolmasını beklemeniz gerekebilir.

10. Power Query Düzenleyicisi eylem şeridinde **Kapat ve Uygula**'ya tıklayın.

Sanal tablodan seçilen sütunlarla Power BI raporunuzu oluşturmaya başlayabilirsiniz.

#### <a name="selecting-columns-in-power-apps"></a>Power Apps'de sütunları seçme

Dataverse Web API sorguları ve Power BI'ya benzer şekilde, uygulamanızdaki ilişkili tabloların sütunlarını hariç tutarak Dataverse sanal tablolarını temel alarak Power Apps için sorgu performansını artırabilirsiniz. Bir sayfaya ilgili bir tablodan alınan sütunlar eklendiyse verileri getirmek için oluşturulan istek URL'si ilgili tablonun yabancı anahtar özelliklerini içerecektir. Bu, yukarıdaki [OData Sorgusunda sütun seçme](#selecting-columns-in-power-apps) örneklerinde olduğu gibi, ek veri aramalarına neden olarak performansı azaltır.

Bu soruna bir çözüm bulmak için, ilgili tablolardan herhangi bir veri alanının Power App uygulamanızın herhangi bir veri formuna dahil edilmediğini doğrulayabilirsiniz.

1. Ağaç görünümü bölmesinde, ekran için veri formu seçin.
2. **Özellikler** bölmesinde, **Alanlar** özelliğinde **Düzenle**'yi seçin.
3. **Veri** bölmesinde, seçili alanların hiçbirinin veri kaynağının sanal tablosunun alanları olmadığını doğrulayın.

Örneğin, uygulamadaki bir sayfada bulunan veri alanlarından biri **ThisItem.Worker.Name** gibi (burada **Worker** ilgili tablodur) başka bir tabloya başvuruyorsa,veriler getirilirken performansın düşmesi olasılığı vardır.

Yalnızca gereksinim duyduğunuz sütunların Power App için veri almak üzere sorguya dahil edildiğinden emin olmak üzere [Power Apps İzleyicisi](/powerapps/maker/monitor-overview)'ni kullanabilirsiniz. Uygulamanız için seçtiğiniz sütunların verileri almak için en uygun sütunlar olmasını sağlamak amacıyla getRows işlemi için oluşturulan URL'yi görüntüleyebilirsiniz.

![getData işlemini analiz etmek için Power Apps İzleyicisi'ni kullanma](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Veri sorgusuna filtre uygulama

Sorgu yürütme performansını artırmak için başka bir yöntem de sorgu sonuçlarında döndürülen kayıtların sayısını sınırlandırmaktır. Bunu, yalnızca gereken kayıtları almanızı sağlamak üzere sonuçları filtreleyerek yapabilirsiniz.

Sorgu verilerini filtreleme hakkında daha fazla bilgi için bkz. [Sonuçları filtreleme](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).

### <a name="limiting-the-page-size-of-the-query"></a>Sorgunun sayfa boyutunu sınırlandırma

Büyük veri kümeleriyle çalışıyorsanız, veri sorgularına `odata.maxpagesize` tercih başlığını ekleyerek sorgu sonuçlarını birden çok sayfaya bölebilirsiniz.

Sayfalandırma hakkında daha fazla bilgi için bkz. [Bir sayfadaki döndürülecek varlıkların sayısını belirleme](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Ayrıca bkz.

- [Dataverse sanal tablolarını yapılandırma](hr-admin-integration-common-data-service-virtual-entities.md)
- [Human Resources sanal tablolarıyla ilgili SSS](hr-admin-virtual-entity-faq.md)
- [Azaltma ile ilgili SSS](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
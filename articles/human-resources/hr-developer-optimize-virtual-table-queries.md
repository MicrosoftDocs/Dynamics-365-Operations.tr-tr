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
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="79a51-103">Dataverse sanal tablo sorgularını iyileştirme</span><span class="sxs-lookup"><span data-stu-id="79a51-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="79a51-104">Çıkış</span><span class="sxs-lookup"><span data-stu-id="79a51-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="79a51-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="79a51-105">Overview</span></span>

<span data-ttu-id="79a51-106">Dynamics 365 Human Resources ile tümleştirme ve diğer veri bağlantılarını geliştirmek için Dataverse sanal tablolarını kullanırken, sanal tablolara yönelik sorgularda performans sorunlarıyla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="79a51-107">Çeşitli istemciler veya arabirimler arasında yavaş sorgu yürütme gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="79a51-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="79a51-108">Örneğin, aşağıdaki durumlarda sorunla karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="79a51-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="79a51-109">Dataverse Web API ile bir sanal tablo sorgularken</span><span class="sxs-lookup"><span data-stu-id="79a51-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="79a51-110">Sanal tabloya karşı bir Power App oluştururken</span><span class="sxs-lookup"><span data-stu-id="79a51-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="79a51-111">Sanal tabloda Power BI raporu oluştururken</span><span class="sxs-lookup"><span data-stu-id="79a51-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="79a51-112">Tüm bu arabirimlerin performans sorunu oluşturma olasılığı vardır.</span><span class="sxs-lookup"><span data-stu-id="79a51-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="79a51-113">Human Resources için Dataverse sanal tablo performansının yavaş olmasının bir nedeni, tablonun [gezinti özellikleriyle](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) ilgili sanal tablonun yabancı anahtar sütunlarıdır.</span><span class="sxs-lookup"><span data-stu-id="79a51-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="79a51-114">Sanal bir tablo için gezinme özellikleri oluşturulduğunda, ilişkili sanal tablonun anahtar sütunu için anahtarın değerini temsil etmek üzere tabloya bir yabancı anahtar sütunu otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="79a51-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="79a51-115">Örneğin, **mshr_hcmworkerbaseentity** varlığına **mshr_dirpersonentity** varlığından alınan yabanco anahtar özelliğiyle **_mshr_fk_person_id_value** sütunu eklenir.</span><span class="sxs-lookup"><span data-stu-id="79a51-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="79a51-116">Bu yabancı anahtar sütunu değerlerinin tabloda tutulma şekli nedeniyle, değerlerin getirilmesi sanal tabloyla ilgili sorgu performansı üzerinde olumsuz etkiye sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="79a51-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="79a51-117">Olası belirtiler</span><span class="sxs-lookup"><span data-stu-id="79a51-117">Potential symptoms</span></span>

<span data-ttu-id="79a51-118">Bu etkiyi örneğin Çalışan (**mshr_hcmworkerentity**) veya temel çalışan (**mshr_hcmworkerbaseentity**) varlığı için yapılan sorgularda görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="79a51-119">Performans sorunu bildiriminin kendisini birkaç farklı yolla görebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="79a51-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="79a51-120">**Yavaş sorgu yürütme**: Sanal tabloya yönelik sorgu beklenen sonuçları döndürebilir ancak sorgu yürütmenin tamamlaması beklenenden uzun sürebilir.</span><span class="sxs-lookup"><span data-stu-id="79a51-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="79a51-121">**Sorgu zaman aşımı**: Sorgu zaman aşımına uğrayabilir ve şu hatayı döndürebilir: "Finance and Operations'ı çağırmak için bir belirteç alındı ancak Finance and Operations InternalServerError türünde bir hata döndürdü."</span><span class="sxs-lookup"><span data-stu-id="79a51-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="79a51-122">**Beklenmeyen hata**: Sorgu şu iletiyle birlikte 400 hata türünü döndürebilir: "Beklenmeyen bir hata oluştu."</span><span class="sxs-lookup"><span data-stu-id="79a51-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![HcmWorkerBaseEntity üzerinde 400 hata türü](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="79a51-124">**Azaltma**: Sorgu sunucu kaynaklarını aşırı kullanabilir ve azaltmaya maruz olabilir.</span><span class="sxs-lookup"><span data-stu-id="79a51-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="79a51-125">Bu durumda, sorgu şu hatayı döndürür: "Finance and Operations'ı çağırmak için bir belirteç alındı ancak Finance and Operations 429 türünde bir hata döndürdü."</span><span class="sxs-lookup"><span data-stu-id="79a51-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="79a51-126">Human Resources'ta azaltma konusunda daha fazla bilgi için bkz. [Azaltmayla ilgili SSS](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="79a51-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![HcmWorkerBaseEntity üzerinde 429 hata türü](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="79a51-128">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="79a51-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="79a51-129">Veri sorgunuz dahil edilen sütunların sayısını sınırlayın</span><span class="sxs-lookup"><span data-stu-id="79a51-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="79a51-130">Sanal tablolarla, sorgu performansını artırmak için en büyük potansiyeli olan yöntemlerden biri sorguda seçilen sütun sayısını sınırlandırmaktır.</span><span class="sxs-lookup"><span data-stu-id="79a51-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="79a51-131">Sorgu performansını en iyi duruma getirmek için genel yöntem, sorgunuzdaki sütunları yalnızca gereksinim duyduğunuz özelliklerle sınırlandırmaktır.</span><span class="sxs-lookup"><span data-stu-id="79a51-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="79a51-132">Bu özellikle, sanal tablolardaki yabancı anahtar sütunları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="79a51-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="79a51-133">Tümleştirmeniz veya raporunuz için yabancı anahtar sütunlarında bulunan değerlere gereksinim duymuyorsanız, sorguyu yabancı anahtar sütunlarını hariç tutarak yalnızca gereksinim duyduğunuz sütunları seçerek yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="79a51-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="79a51-134">OData sorgusunda sütun seçme</span><span class="sxs-lookup"><span data-stu-id="79a51-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="79a51-135">Dataverse Web API ile bir sanal tabloyu sorgularken, **$select** sistem sorgusu seçeneğini kullanarak sorguda bulunan sütunların sayısını sınırlayabilir ve sonuç döndürülmesi gereken sütunları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="79a51-136">Performansı en üst düzeye çıkarmak için, yabancı anahtar sütunlarını (**_mshr_FK_** önekine sahip olan sütunlar) sorgunun dışında tutun.</span><span class="sxs-lookup"><span data-stu-id="79a51-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="79a51-137">Örneğin, **mshr_hcmworkerbaseentity** varlığı için aşağıdaki sorgu yalnızca **$select** sorgu seçeneği tümcesine dahil edilen sütunları içerecek ve yabancı anahtar değerleri dışarıda bırakılacaktır.</span><span class="sxs-lookup"><span data-stu-id="79a51-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="79a51-138">Bu, tüm tablo sütunlarını içeren bir sorguya göre performans açısından önemli iyileşme sağlar.</span><span class="sxs-lookup"><span data-stu-id="79a51-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="79a51-139">Seçili sütun sayısını sınırlama önerisi, sorguyu ilgili sanal tablolara gezinti özellikleri üzerinden genişletmek için **$expand** sorgu seçeneği kullanılırken de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="79a51-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="79a51-140">Örneğin, aşağıdaki sorgu **mshr_dirpersonentity** varlığından genişletilen sütunlarla birlikte **mshr_hcmworkerbaseentity** varlığındaki sütunları içerir.</span><span class="sxs-lookup"><span data-stu-id="79a51-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="79a51-141">**$select** sorgu seçeneğinin aynı zamanda **$expand** sorgu seçeneği yan tümcesine dahil edildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="79a51-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="79a51-142">**$expand** soru seçeneği yan tümcesinde **$select** sorgu seçeneğiyle veri alma yöntemini kullanırken, varlıklar arasındaki gezinme özelliği çok-bir ilişki olduğunda genellikle daha fazla performans artışı elde edersiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="79a51-143">Bir-çok ilişkisini genişletirken sorgu yürütme süresinde aynı azalmayı göremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="79a51-144">Dataverse sanal tabloları için ilişki tanımı hakkında daha fazla bilgi edinmek için bkz. [Tablo ilişkileri](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="79a51-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="79a51-145">Dataverse Web API'da **$select** ve **$expand** sistem sorgusunu kullanma hakkında daha fazla bilgi için bkz. [Sorguyla ilgili varlık kayıtlarını alma](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="79a51-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="79a51-146">Power BI'da sütunları seçme</span><span class="sxs-lookup"><span data-stu-id="79a51-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="79a51-147">Dataverse sanal bir tablosu için Power BI raporu oluştururken yukarıda sözü edilen yavaş performans göstergelerinin herhangi biriyle karşılaşırsanız, rapor tablosunda yabancı anahtar sütunlarını seçili sütunların dışında bırakarak performansı artırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="79a51-148">Örneğin, **mshr_hcmworkerbaseentity** varlığına karşı bir rapor oluşturmak için Power BI Desktop kullanıyorsanız rapor sorgusuna eklemek istediğiniz sütunları seçmek için aşağıdaki adımları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="79a51-149">Power BI Desktop'ta eylem şeridindeki **Veri al** açılır listesinden **Daha fazla...** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="79a51-150">**Veri Al** penceresinde, arama kutusuna **Common Data Service** yazıp **Common Data Service** bağlayıcısını ve **Bağlan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="79a51-151">Common Data Service penceresinin **Sunucu URL**'si alanına, Dataverse ortamınızın kuruluş URI'sını girip **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Dataverse ortamınız için URI girin](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="79a51-153">Gezgin penceresinde, **Varlıklar** düğümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="79a51-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="79a51-154">Arama kutusuna **mshr_hcmworkerbaseentity** girin ve varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="79a51-155">**Verileri Dönüştür**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="79a51-156">Power Query Düzenleyici penceresinde, **Gelişmiş Düzenleyici**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="79a51-157">**Gelişmiş Düzenleyici** penceresinde, gerektiğinde diziye sütun ekleyerek veya kaldırarak sorguyu aşağıdaki gibi görünecek şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="79a51-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

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

9. <span data-ttu-id="79a51-159">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="79a51-160">Güncelleştirmeden önce sorgudan 429 türünde bir hata aldıysanız, sorgunun başarıyla tamamlanması için sorguyu yenilemeden önce yeniden deneme süresinin dolmasını beklemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="79a51-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="79a51-161">Power Query Düzenleyicisi eylem şeridinde **Kapat ve Uygula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="79a51-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="79a51-162">Sanal tablodan seçilen sütunlarla Power BI raporunuzu oluşturmaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="79a51-163">Power Apps'de sütunları seçme</span><span class="sxs-lookup"><span data-stu-id="79a51-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="79a51-164">Dataverse Web API sorguları ve Power BI'ya benzer şekilde, uygulamanızdaki ilişkili tabloların sütunlarını hariç tutarak Dataverse sanal tablolarını temel alarak Power Apps için sorgu performansını artırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="79a51-165">Bir sayfaya ilgili bir tablodan alınan sütunlar eklendiyse verileri getirmek için oluşturulan istek URL'si ilgili tablonun yabancı anahtar özelliklerini içerecektir.</span><span class="sxs-lookup"><span data-stu-id="79a51-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="79a51-166">Bu, yukarıdaki [OData Sorgusunda sütun seçme](#selecting-columns-in-power-apps) örneklerinde olduğu gibi, ek veri aramalarına neden olarak performansı azaltır.</span><span class="sxs-lookup"><span data-stu-id="79a51-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="79a51-167">Bu soruna bir çözüm bulmak için, ilgili tablolardan herhangi bir veri alanının Power App uygulamanızın herhangi bir veri formuna dahil edilmediğini doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="79a51-168">Ağaç görünümü bölmesinde, ekran için veri formu seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="79a51-169">**Özellikler** bölmesinde, **Alanlar** özelliğinde **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="79a51-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="79a51-170">**Veri** bölmesinde, seçili alanların hiçbirinin veri kaynağının sanal tablosunun alanları olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="79a51-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="79a51-171">Örneğin, uygulamadaki bir sayfada bulunan veri alanlarından biri **ThisItem.Worker.Name** gibi (burada **Worker** ilgili tablodur) başka bir tabloya başvuruyorsa,veriler getirilirken performansın düşmesi olasılığı vardır.</span><span class="sxs-lookup"><span data-stu-id="79a51-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="79a51-172">Yalnızca gereksinim duyduğunuz sütunların Power App için veri almak üzere sorguya dahil edildiğinden emin olmak üzere [Power Apps İzleyicisi](/powerapps/maker/monitor-overview)'ni kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="79a51-173">Uygulamanız için seçtiğiniz sütunların verileri almak için en uygun sütunlar olmasını sağlamak amacıyla getRows işlemi için oluşturulan URL'yi görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![getData işlemini analiz etmek için Power Apps İzleyicisi'ni kullanma](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="79a51-175">Veri sorgusuna filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="79a51-175">Filtering the data query</span></span>

<span data-ttu-id="79a51-176">Sorgu yürütme performansını artırmak için başka bir yöntem de sorgu sonuçlarında döndürülen kayıtların sayısını sınırlandırmaktır.</span><span class="sxs-lookup"><span data-stu-id="79a51-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="79a51-177">Bunu, yalnızca gereken kayıtları almanızı sağlamak üzere sonuçları filtreleyerek yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="79a51-178">Sorgu verilerini filtreleme hakkında daha fazla bilgi için bkz. [Sonuçları filtreleme](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).</span><span class="sxs-lookup"><span data-stu-id="79a51-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="79a51-179">Sorgunun sayfa boyutunu sınırlandırma</span><span class="sxs-lookup"><span data-stu-id="79a51-179">Limiting the page size of the query</span></span>

<span data-ttu-id="79a51-180">Büyük veri kümeleriyle çalışıyorsanız, veri sorgularına `odata.maxpagesize` tercih başlığını ekleyerek sorgu sonuçlarını birden çok sayfaya bölebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79a51-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="79a51-181">Sayfalandırma hakkında daha fazla bilgi için bkz. [Bir sayfadaki döndürülecek varlıkların sayısını belirleme](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="79a51-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="79a51-182">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="79a51-182">See also</span></span>

- [<span data-ttu-id="79a51-183">Dataverse sanal tablolarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="79a51-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="79a51-184">Human Resources sanal tablolarıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="79a51-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="79a51-185">Azaltma ile ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="79a51-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
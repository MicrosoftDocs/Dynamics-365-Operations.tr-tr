---
title: Tarih ve Saat alanlarını anla
description: Microsoft Dynamics 365 Human Resources'ta tarih ve saat alanları kullanırken ne beklendiğinizi anlayın.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efda2b54f9228ac539e6ba2d18f85bf3ad15a6ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802443"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="493d3-103">Tarih ve Saat alanlarını anlama</span><span class="sxs-lookup"><span data-stu-id="493d3-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="493d3-104">**Tarih ve saat** alanları Dynamics 365 Human Resources içinde temel bir kavramdır.</span><span class="sxs-lookup"><span data-stu-id="493d3-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="493d3-105">Formlar, Dataverse ve dış kaynaklardaki **Tarih ve Saat** verileriyle nasıl çalışılacağını anlamak önemlidir.</span><span class="sxs-lookup"><span data-stu-id="493d3-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="493d3-106">Tarih ile Tarih ve saat alanı veri türleri arasındaki farkı anlama</span><span class="sxs-lookup"><span data-stu-id="493d3-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="493d3-107">**Tarih ve saat** alanları saat dilimi bilgilerini içerir, **Tarih** alanları ise içermez.</span><span class="sxs-lookup"><span data-stu-id="493d3-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="493d3-108">**Tarih** alanları aynı bilgileri herhangi bir konumda görüntüler.</span><span class="sxs-lookup"><span data-stu-id="493d3-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="493d3-109">**Tarih** alanına bir tarih girdiğinizde, İnsan Kaynakları, bu tarihi de veritabanına yazar.</span><span class="sxs-lookup"><span data-stu-id="493d3-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="493d3-110">Bir **tarih ve saat** alanındaki verileri görüntülerken, İnsan Kaynakları tarih ve saat, **Kullanıcı seçenekleri** formunda (**Ortak > Kurulum > Kullanıcı seçenekleri**) ayarlanan saat dilimine göre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="493d3-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="493d3-111">Alana girdiğiniz tarih ve saat bilgileri veritabanına yazılan bilgilerle aynı olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="493d3-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="493d3-112">[![Kullanıcı seçenekleri formu](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="493d3-113">Formlardaki Tarih ve Saat alanlarını anlama</span><span class="sxs-lookup"><span data-stu-id="493d3-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="493d3-114">Kullanıcının saat dilimi Eşgüdümlü Evrensel Saat (UTC) olarak ayarlanmazsa ekranda görüntülenen **Tarih ve Saat** verileri veritabanında depolanan verilerle aynı değildir.</span><span class="sxs-lookup"><span data-stu-id="493d3-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="493d3-115">**Tarih ve saat** alanlarındaki veriler her zaman UTC olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="493d3-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="493d3-116">[![Çalışan formu UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="493d3-117">Veritabanında Tarih ve Saat alanlarını anlama</span><span class="sxs-lookup"><span data-stu-id="493d3-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="493d3-118">Human Resources veritabanına bir **Tarih ve Saat** değeri yazdığında, verileri UTC'ye göre depolar.</span><span class="sxs-lookup"><span data-stu-id="493d3-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="493d3-119">Bu, kullanıcıların Kullanıcı seçeneklerinde tanımlanan saat dilimine göre herhangi bir **tarih ve saat** verisini görmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="493d3-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="493d3-120">Yukarıdaki örnekte başlangıç zamanı zamanda bir noktadır, belirli bir tarihi değil.</span><span class="sxs-lookup"><span data-stu-id="493d3-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="493d3-121">Oturum açan kullanıcının saat dilimi GMT +12:00'den GMT UTC'ye değiştirildiğinde aynı kayıt 01/05/2019 12:00:00 yerine 30/04/2019 12:00:00'yi gösterir.</span><span class="sxs-lookup"><span data-stu-id="493d3-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="493d3-122">Aşağıdaki örnekte, çalışan 000724 istihdamı saat diliminden bağımsız olarak aynı anda etkin olur.</span><span class="sxs-lookup"><span data-stu-id="493d3-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="493d3-123">Çalışan GMT saat diliminde 30/04/2019 tarihinde etkin olacak ve GMT + 12:00 saat dilimindeki 05/01/2019 ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="493d3-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="493d3-124">Her ikisi de belirli bir tarih değil, zaman içinde aynı noktaya başvuruda bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="493d3-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="493d3-125">[![Çalışan formu GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="493d3-126">Veri yönetimi çerçevesi, Excel, Dataverse ve Power BI'da Tarih ve Saat verileri</span><span class="sxs-lookup"><span data-stu-id="493d3-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="493d3-127">Veri yönetimi çerçevesi, Excel eklentisi, Dataverse ve Power BI raporlama, verilerle doğrudan veritabanı düzeyinde etkileşimde bulunmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="493d3-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="493d3-128">**Tarih ve Saat** verilerini kullanıcının saat dilimine ayarlayan bir istemci olmadığından, tüm **Tarih ve Saat** değerleri UTC'ye göredir ve bu da veri girerken veya görüntülerken bazı yanlış varsayımlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="493d3-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="493d3-129">DMF, Excel veya Dataverse aracılığıyla gönderilen **Tarih ve Saat** verilerinin veritabanı tarafından UTC'ye göre olduğu varsayılır.</span><span class="sxs-lookup"><span data-stu-id="493d3-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="493d3-130">Verileri görüntüleyen kullanıcının kullanıcı saat dilimi UTC olarak ayarlanmadığından, bu durum, gönderilen **tarih ve saat** değerinin beklendiği gibi görüntülenmediği durumlarda bazı karışıklıklara neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="493d3-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="493d3-131">Veriler dışa aktarıldığında aynı şey ters yönde de gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="493d3-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="493d3-132">Dışarı aktarılan DMF varlığındaki **Tarih ve Saat** verileri Dynamics istemcisinde görüntülenenden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="493d3-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="493d3-133">Verileri görüntülemek veya yazmak için DMF gibi dış kaynakları kullanırken, **Tarih ve Saat** değerlerinin, kullanıcının bilgisayarının saat dilimine veya geçerli kullanıcı saat dilimi ayarlarına bakılmaksızın varsayılan olarak UTC'ye göre olduğunun kabul edildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="493d3-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="493d3-134">Farklı ürün alanlarında görüntülenen aynı kayda örnekler</span><span class="sxs-lookup"><span data-stu-id="493d3-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="493d3-135">**Kullanıcı saat dilimi UTC olarak ayarlanan İnsan Kaynakları**</span><span class="sxs-lookup"><span data-stu-id="493d3-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="493d3-136">[![Çalışan formu UTC olarak ayarlandı](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="493d3-137">**Kullanıcı saat dilimi GMT+12:00 olarak ayarlanan İnsan Kaynakları**</span><span class="sxs-lookup"><span data-stu-id="493d3-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="493d3-138">[![Çalışan formu GMT olarak ayarlandı](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="493d3-139">**OData aracılığıyla Excel**</span><span class="sxs-lookup"><span data-stu-id="493d3-139">**Excel Via OData**</span></span>

<span data-ttu-id="493d3-140">[![OData aracılığıyla Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="493d3-141">**DMF Aşamalandırma**</span><span class="sxs-lookup"><span data-stu-id="493d3-141">**DMF Staging**</span></span>

<span data-ttu-id="493d3-142">[![DMF Aşamalandırma](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="493d3-143">**DMF dışa aktarma**</span><span class="sxs-lookup"><span data-stu-id="493d3-143">**DMF Export**</span></span>

<span data-ttu-id="493d3-144">[![DMF Dışarı Aktarma](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="493d3-145">**Dataverse İle Excel**</span><span class="sxs-lookup"><span data-stu-id="493d3-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="493d3-146">[![Dataverse İle Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="493d3-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="493d3-147">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="493d3-147">See also</span></span>

[<span data-ttu-id="493d3-148">Tarih ve saat verileri</span><span class="sxs-lookup"><span data-stu-id="493d3-148">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="493d3-149">Kullanıcının tercih ettiği saat dilimleri</span><span class="sxs-lookup"><span data-stu-id="493d3-149">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
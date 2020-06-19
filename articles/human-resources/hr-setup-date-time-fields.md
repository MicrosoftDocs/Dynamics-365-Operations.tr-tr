---
title: Tarih ve Saat alanlarını anla
description: Microsoft Dynamics 365 Human Resources'ta tarih ve saat alanları kullanırken ne beklendiğinizi anlayın. Dış kaynak, İnsan Kaynakları veya Common Data Service formunda tarih ve saat verileriyle etkileşim kurarken bekleyeceklerinizle ilgili açıklık elde edin.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be1e28d0b842184ce3c4f7bd9748f5e76ac67489
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430107"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="46da7-104">Tarih ve Saat alanlarını anla</span><span class="sxs-lookup"><span data-stu-id="46da7-104">Understand Date and Time fields</span></span>

<span data-ttu-id="46da7-105">**Tarih ve saat** alanları Dynamics 365 Human Resources içinde temel bir kavramdır.</span><span class="sxs-lookup"><span data-stu-id="46da7-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="46da7-106">Bir Dynamics 365 Human Resources formları, Common Data Service ve dış kaynakta **tarih ve saat** verileriyle nasıl çalışacağının anlaşılması önemlidir.</span><span class="sxs-lookup"><span data-stu-id="46da7-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="46da7-107">Tarih ile Tarih ve saat alanı veri türleri arasındaki farkı anlama</span><span class="sxs-lookup"><span data-stu-id="46da7-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="46da7-108">**Tarih ve saat** alanları saat dilimi bilgilerini içerir, **Tarih** alanları ise içermez.</span><span class="sxs-lookup"><span data-stu-id="46da7-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="46da7-109">**Tarih** alanları aynı bilgileri herhangi bir konumda görüntüler.</span><span class="sxs-lookup"><span data-stu-id="46da7-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="46da7-110">**Tarih** alanına bir tarih girdiğinizde, İnsan Kaynakları, bu tarihi de veritabanına yazar.</span><span class="sxs-lookup"><span data-stu-id="46da7-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="46da7-111">Bir **tarih ve saat** alanındaki verileri görüntülerken, İnsan Kaynakları tarih ve saat, **Kullanıcı seçenekleri** formunda (**Ortak > Kurulum > Kullanıcı seçenekleri**) ayarlanan saat dilimine göre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="46da7-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="46da7-112">Alana girdiğiniz tarih ve saat bilgileri veritabanına yazılan bilgilerle aynı olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="46da7-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="46da7-113">[![Kullanıcı seçenekleri formu](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="46da7-114">Formlardaki Tarih ve Saat alanlarını anlama</span><span class="sxs-lookup"><span data-stu-id="46da7-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="46da7-115">**Tarih ve saat** alanına veri girerken, kullanıcının saat dilimi Eşgüdümlü Evrensel Saat'e (UTC) ayarlanmamışsa, ekranda görüntülenen veriler veritabanında depolanan verilerle aynı değildir.</span><span class="sxs-lookup"><span data-stu-id="46da7-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="46da7-116">**Tarih ve saat** alanlarındaki veriler her zaman UTC olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="46da7-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="46da7-117">[![Çalışan formu](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="46da7-118">Veritabanında Tarih ve Saat alanlarını anlama</span><span class="sxs-lookup"><span data-stu-id="46da7-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="46da7-119">İnsan Kaynakları **Tarih ve saat** değerini veritabanına yazdığında verileri UTC'de depolar.</span><span class="sxs-lookup"><span data-stu-id="46da7-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="46da7-120">Bu, kullanıcıların Kullanıcı seçeneklerinde tanımlanan saat dilimine göre herhangi bir **tarih ve saat** verisini görmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="46da7-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="46da7-121">Yukarıdaki örnekte başlangıç zamanı zamanda bir noktadır, belirli bir tarihi değil.</span><span class="sxs-lookup"><span data-stu-id="46da7-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="46da7-122">Oturum açmış olan kullanıcının saat dilimini GMT + 12:00'den GMT UTC'ye değiştirerek, yeni oluşturulan kayıt 01/05/2019 12:00:00 yerine 30/04/2019 12:00:00 gösterir.</span><span class="sxs-lookup"><span data-stu-id="46da7-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="46da7-123">Aşağıdaki örnekte, çalışan 000724 istihdamı saat diliminden bağımsız olarak aynı anda etkin olur.</span><span class="sxs-lookup"><span data-stu-id="46da7-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="46da7-124">Çalışan GMT saat diliminde 30/04/2019 tarihinde etkin olacak ve GMT + 12:00 saat dilimindeki 05/01/2019 ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="46da7-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="46da7-125">Her ikisi de belirli bir tarih değil, zaman içinde aynı noktaya başvuruda bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="46da7-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="46da7-126">[![Çalışan formu](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="46da7-127">Veri yönetimi çerçevesi, Excel, Common Data Service ve Power BI'da Tarih ve Saat verileri</span><span class="sxs-lookup"><span data-stu-id="46da7-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="46da7-128">Veri yönetimi çerçevesi, Excel eklentisi, Common Data Service ve Power BI raporlama, verilerle doğrudan veritabanı düzeyinde etkileşimde bulunmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="46da7-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="46da7-129">**Tarih ve saat** verilerini kullanıcının saat dilimine göre ayarlayabileceği bir istemci olmadığından, tüm **tarih ve saat** değerleri UTC'de olup verileri girerken veya görüntülerken bazı yanlış varsayımlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="46da7-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="46da7-130">DMF, Excel veya Common Data Service ile gönderilen **tarih ve saat** verilerinin veritabanı tarafından UTC'de olduğu varsayılır.</span><span class="sxs-lookup"><span data-stu-id="46da7-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="46da7-131">Verileri görüntüleyen kullanıcının kullanıcı saat dilimi UTC olarak ayarlanmadığından, bu durum, gönderilen **tarih ve saat** değerinin beklendiği gibi görüntülenmediği durumlarda bazı karışıklıklara neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="46da7-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="46da7-132">Veriler dışa aktarıldığında aynı şey ters yönde de gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="46da7-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="46da7-133">Dışa aktarılan DMF varlığındaki **tarih ve saat** verileri farklı olabilir ve böylece Dynamics istemcisinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="46da7-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="46da7-134">Verileri görüntülemek veya yazmak için DMF gibi harici kaynaklar kullanırken, kullanıcının bilgisayarının saat dilimi veya geçerli kullanıcı zaman dilimi ayarları ne olursa olsun, **Tarih ve Saat** değerlerinin UTC'de varsayılan olarak değerlendirildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="46da7-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="46da7-135">Farklı ürün alanlarında görüntülenen aynı kayda örnekler</span><span class="sxs-lookup"><span data-stu-id="46da7-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="46da7-136">**Kullanıcı saat dilimi UTC olarak ayarlanan İnsan Kaynakları**</span><span class="sxs-lookup"><span data-stu-id="46da7-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="46da7-137">[![Çalışan formu](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="46da7-138">**Kullanıcı saat dilimi GMT+12:00 olarak ayarlanan İnsan Kaynakları**</span><span class="sxs-lookup"><span data-stu-id="46da7-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="46da7-139">[![Çalışan formu](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="46da7-140">**OData aracılığıyla Excel**</span><span class="sxs-lookup"><span data-stu-id="46da7-140">**Excel Via OData**</span></span>

<span data-ttu-id="46da7-141">[![OData aracılığıyla Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="46da7-142">**DMF Aşamalandırma**</span><span class="sxs-lookup"><span data-stu-id="46da7-142">**DMF Staging**</span></span>

<span data-ttu-id="46da7-143">[![DMF Aşamalandırma](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="46da7-144">**DMF dışa aktarma**</span><span class="sxs-lookup"><span data-stu-id="46da7-144">**DMF Export**</span></span>

<span data-ttu-id="46da7-145">[![DMF Aşamalandırma](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="46da7-146">**Common Data Service İle Excel**</span><span class="sxs-lookup"><span data-stu-id="46da7-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="46da7-147">[![Common Data Service İle Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="46da7-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="46da7-148">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="46da7-148">See also</span></span>

[<span data-ttu-id="46da7-149">Tarih ve saat verileri</span><span class="sxs-lookup"><span data-stu-id="46da7-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="46da7-150">Kullanıcının tercih ettiği saat dilimleri</span><span class="sxs-lookup"><span data-stu-id="46da7-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 

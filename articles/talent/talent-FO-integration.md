---
title: Dynamics 365 Talent ile Dynamics 365 Finance tümleştirmesi SSS
description: Bu konu altında, bir Talent ve Finance tümleştirmesinde hangi verilerin eşitleneceği açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251027"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="e36d7-103">Dynamics 365 Talent ile Dynamics 365 Finance tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="e36d7-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e36d7-104">Bu konu, hangi verilerin Dynamics 365 Talent, Dynamics 365 Finance ile tümleştirildiğinde eşitleneceğine dair sıkça sorulan soruları yanıtlar.</span><span class="sxs-lookup"><span data-stu-id="e36d7-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="e36d7-105">Tüm veriler mi eşitlenir yoksa yalnızca bazı veri varlıkları mı?</span><span class="sxs-lookup"><span data-stu-id="e36d7-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="e36d7-106">Core HR için, bir veri alt kümesi eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="e36d7-107">Tüm varlıkların listesi için bkz. [Dynamics 365 Talent'tan Dynamics 365 Finance tümleştirmesi](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="e36d7-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="e36d7-108">Attract ve Onboard için tüm veri Common Data Service için yereldir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="e36d7-109">Yeni bir eşlemeyi şablonları kullanmadan oluşturabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="e36d7-110">Şablonları, başlangıç noktasıdır.</span><span class="sxs-lookup"><span data-stu-id="e36d7-110">Templates are the starting point.</span></span> <span data-ttu-id="e36d7-111">Kendi şablonunuzu oluşturabilirsiniz, ancak şablon bir tümleştirme projesi oluşturma sırasında her zaman gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="e36d7-112">Veri tümleştirme (DI) şablonları ve projeleri hakkında daha fazla bilgi için bkz. [Common Data Service için veri tümleştirme](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="e36d7-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="e36d7-113">Talent ve Finance arasında aktarmak üzere mali boyutlar eşleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-113">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="e36d7-114">Mali boyutlar şu anda Common Data Service içinde mevcut değildir ve bunu sonucunda varsayılan şablonun parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="e36d7-115">Bu varlık planlanmıştır, ancak şu anda zaman çizelgesi mevcut değildir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="e36d7-116">Finance'te bulunan ancak Talent'ta bulunmayan veriler için, Talent'taki **Bağlantıları yapılandır**'ı kullanarak iki sistemi birbirine bağlayın.</span><span class="sxs-lookup"><span data-stu-id="e36d7-116">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="e36d7-117">Talent ve Finance arasındaki bağlantıları yapılandırma hakkında daha fazla bilgi için bkz. [Dynamics 365 Talent: Core HR'daki yenilikler veya değişiklikler (31 Ekim 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="e36d7-117">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![Mali boyutları eşle](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="e36d7-119">Bazı durumlarda çalışanları içe aktardığım zaman, Finance'te devre dışı çalışanlar haline geliyorlar.</span><span class="sxs-lookup"><span data-stu-id="e36d7-119">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="e36d7-120">Neden?</span><span class="sxs-lookup"><span data-stu-id="e36d7-120">Why?</span></span>

<span data-ttu-id="e36d7-121">Çalışanların Talent içinde etkin bir çalışma ayrıntısı kaydı yoksa bu hatayı alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e36d7-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="e36d7-122">Bunu çözümlemek için **Personel Yönetimi \> Çalışanlar \> Çalışma Geçmişi \> Veri Yöneticisi**'ne gidin ve etkin bir çalışan ayrıntı kaydı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e36d7-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="e36d7-123">Yalnızca bir alan alt kümesine eşleşmeyi seçersem, eşleştirilmemiş alanlara yapılan değişiklikler bir eşitleme tetikler mi?</span><span class="sxs-lookup"><span data-stu-id="e36d7-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="e36d7-124">Veri eşitleme yürütme planını izler.</span><span class="sxs-lookup"><span data-stu-id="e36d7-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="e36d7-125">Tümleştirme, alanın tümleştirme eşleştirmesinin parçası olup olmadığından bağımsız olarak kayıttaki herhangi bir alan değişirse kaydı çekecektir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="e36d7-126">Yalnızca etkin alt değişiklikleri ve işten çıkarılan kayıtların nasıl gönderebilirim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="e36d7-127">"Gelişmiş sorgu" kullanarak, kaynak verisini hedefe aktarmadan önce filtreleyebilir ve şekillendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e36d7-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Etkin çalışan gelişmiş sorgusu](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="e36d7-129">Belirli bir varlık için hangi alanların Finance'e gönderileceğini belirtebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-129">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="e36d7-130">Alanlar tümleştirme görevinden eklenebilir veya çıkartılabilir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="e36d7-131">Common Data Service varlığı içinde mevcut olan tüm veri alanları Core HR'dan doldurulmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="e36d7-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="e36d7-132">Ek veriler PowerApps ile doldurulabilir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-132">Additional data can be populated via PowerApps.</span></span>

![Bir tümleştirme görevinden alanları ekleyin veya çıkartın](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="e36d7-134">Tümleştirmeyi bir toplu iş olarak ayarlıyorum, ancak hedef sisteme Talent bağlantıyı kaybetti.</span><span class="sxs-lookup"><span data-stu-id="e36d7-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="e36d7-135">Aynı değişiklik kümesini hedef sisteme nasıl gönderebilirim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="e36d7-136">Özel durum işleme için özel bir kurulum gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="e36d7-137">Veri Tümleştirme, kaynak ve hedefte gerçekleşen hatları yakalar ve raporlar ve el ile yeniden denemelere izin verecektir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="e36d7-138">Ancak, el ile veri düzeltmeye izin vermez.</span><span class="sxs-lookup"><span data-stu-id="e36d7-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="e36d7-139">Veri güncelleştirmeleri gerekliyse, kaynak veya hedefte gerçekleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="e36d7-140">Çift yönlü tümleştirme ayarlayabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="e36d7-141">Hayır, tümleştirme şu anda yalnızca tek yönlüdür (Talent'tan Finance and Operations'a).</span><span class="sxs-lookup"><span data-stu-id="e36d7-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="e36d7-142">Bununla birlikte, Talent'tan Finance'e veri göndermek için bir varsayılan şablon vardır.</span><span class="sxs-lookup"><span data-stu-id="e36d7-142">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="e36d7-143">Tümleştirmemin bir parçası olarak kayıt silinmesine izin verebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="e36d7-144">Hayır, Veri Tümleştirici, silinen kayıtları veri aktarımı için yakalamayacaktır.</span><span class="sxs-lookup"><span data-stu-id="e36d7-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="e36d7-145">Yalnızca veri oluşturma ve güncelleştirme (UPSERT) şu anda dahildir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="e36d7-146">Hatalı yürütmeyi yeniden çalıştırabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="e36d7-147">Bu durumda, tam dosya mı gönderir yalnızca değişiklikleri mi?</span><span class="sxs-lookup"><span data-stu-id="e36d7-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="e36d7-148">Veri Tümleştiricinin ilk çalıştırılması her zaman tam çalıştırmadır.</span><span class="sxs-lookup"><span data-stu-id="e36d7-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="e36d7-149">Sonraki yürütmeler değişiklik izlemeye dayanır.</span><span class="sxs-lookup"><span data-stu-id="e36d7-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="e36d7-150">Bir hatalı çalışma yürütülürse, yürütme kapsamdaki kayıtları çıkartır ve Common Data Service'ten en güncel değişiklikleri gönderir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="e36d7-151">Proje kaydettiğimde, "Proje eşleme hatalarına sahip" hatasını alıyorum.</span><span class="sxs-lookup"><span data-stu-id="e36d7-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="e36d7-152">Ne yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="e36d7-152">What do I do?</span></span>

<span data-ttu-id="e36d7-153">Tümleştirme anahtarlarınızı kurulumunu denetleyin, kurulum için gerekli değişiklikleri yapın ve sonra varlıkları projedeki yenileyin.</span><span class="sxs-lookup"><span data-stu-id="e36d7-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="e36d7-154">Varsayılan şablon kullanıldığında, tümleştirme anahtarları otomatik olarak alınacak.</span><span class="sxs-lookup"><span data-stu-id="e36d7-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="e36d7-155">Varolan şablona yeni görevler eklendiğinde bu sorun ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="e36d7-156">Çalışanların işe sahip olduğu N sayıda tüzel varlığa sahipsem, bunların her biri için eşleşme oluşturmam gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="e36d7-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="e36d7-157">Evet, Finance'teki her bir tüzel kişilik için, veri tümleştirmede ayrı bir tümleştirme projesine gereksiniminiz olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e36d7-157">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="e36d7-158">Microsoft tarafından sağlanan varsayılan şablonun parçası olmayan verileri aktarmak gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="e36d7-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="e36d7-159">Bunu yapabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-159">Can I do this?</span></span>

<span data-ttu-id="e36d7-160">Evet, varolan şablondan alanlar kaldırılabilir veya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="e36d7-161">Şablon diğer Common Data Service varlıkları için ek verileri dahil etmek üzere değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="e36d7-162">Varlığın, şablona dahil edilmesi için Common Data Service içinde olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="e36d7-163">Kısa süre önce Finance ve Talent ortamları oluşturdum ve "Veri değeri tutarlılık kısıtlamalarını ihlal ediyor" hatasını alıyorum.</span><span class="sxs-lookup"><span data-stu-id="e36d7-163">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="e36d7-164">Neden?</span><span class="sxs-lookup"><span data-stu-id="e36d7-164">Why?</span></span>

<span data-ttu-id="e36d7-165">Bu hatanın nedenleri arasında şunlar olabilir:</span><span class="sxs-lookup"><span data-stu-id="e36d7-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="e36d7-166">Veri aktarma, kaynakta (Common Data Service) yinelenen kayıtların ayıklanmasıyla sonuçlandı.</span><span class="sxs-lookup"><span data-stu-id="e36d7-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="e36d7-167">Veri aktarımı, Finance and Operations'ta ihtiyaç duyulan alanlar için boş değerlere sahip.</span><span class="sxs-lookup"><span data-stu-id="e36d7-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="e36d7-168">Verinin Common Data Service içindeki olduğundan ve Finance and Operations gereksinimlerini karşıladığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="e36d7-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="e36d7-169">Yürütme hataları varsa ve Çalışan kimliği eşitlenmediyse, hatalı çalışan kaydına sahip geçmiş işi nasıl bulabilirim?</span><span class="sxs-lookup"><span data-stu-id="e36d7-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="e36d7-170">Veri Tümleştirici, Finance'te birden fazla proje oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e36d7-170">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="e36d7-171">Veri Tümleştirici görevi ve Finance projesi arasındaki ilişki bire bir ilişkidir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-171">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="e36d7-172">Veri Tümleştirici yürütme geçmişinden zamanı takip edin ve Finance'te dizin -1 olan projeyi arayın.</span><span class="sxs-lookup"><span data-stu-id="e36d7-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="e36d7-173">Görev numarası Veri Tümleştirici'de 9 ise, Finance'teki dizin 8'dir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-173">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="e36d7-174">Veri Tümleştiricisinden görev dizinini yakalayın (bu örnekte "9"dur).</span><span class="sxs-lookup"><span data-stu-id="e36d7-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Veri Tümleştiricisinden görev dizinini yakalayın.](media/CaptureTaskIndex.png)

2. <span data-ttu-id="e36d7-176">Projenin yürütme zamanını izleyin.</span><span class="sxs-lookup"><span data-stu-id="e36d7-176">Track the execution time of the project.</span></span>

![Projenin yürütme zamanını izleyin](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="e36d7-178">Finance'te - 1 dizini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e36d7-178">In Finance, identify index - 1.</span></span> <span data-ttu-id="e36d7-179">Bu örnekte, sonek "8"e sahip olan ve yürütme zamanı dizin "0" projesi olan proje, Adım 2'deki yürütme zamanı ile eşleşiyor.</span><span class="sxs-lookup"><span data-stu-id="e36d7-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Dizini tanımlayın](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="e36d7-181">Talent ve Finance'i tümleştirdikten sonra Talent verilerimi Finance'te görmüyorum.</span><span class="sxs-lookup"><span data-stu-id="e36d7-181">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="e36d7-182">Ne yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="e36d7-182">What do I do?</span></span>

<span data-ttu-id="e36d7-183">Finance'e tümleştirme iki adımlı bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-183">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="e36d7-184">Öncelikle, Talent verisinin güncelleştirilmiş ve Common Data Service içinde kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e36d7-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="e36d7-185">Bu neredeyse gerçek zamanlı bir eşitlemedir ve PowerApps içinde veri girişleri içindeki veriye bakarak doğrulanabilir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Common Data Service içindeki veri](media/DataInCDS.png)

<span data-ttu-id="e36d7-187">Veri Common Data Service'te beklendiği gibi görüntülenmiyorsa, varlığın tümleştirme ile desteklendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="e36d7-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="e36d7-188">Common Data Service içine ek veri dahil etmek için Microsoft tarafından bir değişiklik gerekir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="e36d7-189">Varlık destekleniyorsa ve veri Common Data Service içinde kullanılabilirse, Veri Tümleştiricisi içinde eşleştirmenin doğru olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e36d7-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="e36d7-190">Tümleştirme eşleştirmesi doğru gözüküyorsa, veri yönetimi işlerini başarıyla çalıştırıldığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e36d7-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="e36d7-191">Toplu işlerin yürütülmesinde hatalar ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="e36d7-192">Veri Yönetimi hakkında daha fazla bilgi için bkz. [Veri yönetimi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e36d7-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="e36d7-193">Çalışanlarımın adresleri Finance'e aktardıktan sonra doğru görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="e36d7-193">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="e36d7-194">Ne yapmalıyım?</span><span class="sxs-lookup"><span data-stu-id="e36d7-194">What should I do?</span></span>

<span data-ttu-id="e36d7-195">**Konum Kodu** için numara serisi, Talent'ta ve Finance'te aynı düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="e36d7-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="e36d7-196">Numara serisinin her iki tarafta da benzersiz olması gerekir, bu sayede veriyi Common Data Service'ten Finance and Operations'a tümleştirirken adres çakışmaları gerçekleşmez.</span><span class="sxs-lookup"><span data-stu-id="e36d7-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="e36d7-197">Talent tümleştirmesi sırasında, numara serilerinin Talent'ta ve Finance'te içinde aynı olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e36d7-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="e36d7-198">Tüm numara serilerinin, verinin her iki sistemde de tutulabildiği yerlerde aynı olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e36d7-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="e36d7-199">Bağlantımı kümesi oluştururken, Bağlantı açılır listesinde bağlantıyı göremiyorum.</span><span class="sxs-lookup"><span data-stu-id="e36d7-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="e36d7-200">Ne yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="e36d7-200">What do I do?</span></span>

<span data-ttu-id="e36d7-201">Bağlantılarınızı oluştururken Dynamics 365 Finance'i ve Common Data Service'i seçtiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="e36d7-201">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="e36d7-202">Çalışmaları eşitlerken “CompanyInfo_FK mevcut değil" veya “Değer 12/31/2154 11:59:59 pm', 'Çalışma sonlanma tarihi' ilgili 'Çalışma' tablosunda bulunamadı.” hatasını alıyorum. Ne yapmalıyım?</span><span class="sxs-lookup"><span data-stu-id="e36d7-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="e36d7-203">Doğru tüzel varlıkları eşlediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="e36d7-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="e36d7-204">Tüzel varlık eşitleme, varsayılan şablonun parçası değildir, bu nedenle Talent ve Common Data Service bulunan her bir tüzel varlığın Finance'te de mevcut olması beklenir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="e36d7-205">İlişkili Bağlantı Kümesi için doğru tüzel varlıkları seçtiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="e36d7-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="e36d7-206">Projemi ayarladıktan sonra Finance için alan eşleşmesi boş görünüyor.</span><span class="sxs-lookup"><span data-stu-id="e36d7-206">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="e36d7-207">Ne yapmalıyım?</span><span class="sxs-lookup"><span data-stu-id="e36d7-207">What should I do?</span></span>

<span data-ttu-id="e36d7-208">Finance'te veri varlıklarını **Veri yönetimi \> Çerçeve Parametreleri \> Varlık ayarları \> Varlık listesini yenile**'ye giderek yenileyin.</span><span class="sxs-lookup"><span data-stu-id="e36d7-208">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="e36d7-209">Bunun tamamlanması birkaç dakika sürer ve daha sonra bu eşleşmeleri görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e36d7-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="e36d7-210">Yeni proje oluşturulduğunda bu sorun oluşur.</span><span class="sxs-lookup"><span data-stu-id="e36d7-210">This issue occurs when new projects are created.</span></span>

![Eksik alan eşlemeleri](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="e36d7-212">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e36d7-212">Additional resources</span></span>

- <span data-ttu-id="e36d7-213">Veri Tümleştirici (DI):</span><span class="sxs-lookup"><span data-stu-id="e36d7-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="e36d7-214">Veriyi Common Data Service içine tümleştir</span><span class="sxs-lookup"><span data-stu-id="e36d7-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="e36d7-215">Veri Tümleştirici hata yönetimi ve sorun giderme</span><span class="sxs-lookup"><span data-stu-id="e36d7-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="e36d7-216">PowerApps, Microsoft Flow ve Common Data Service'te sistemin oluşturduğu günlükler için DSR taleplerine yanıt verme</span><span class="sxs-lookup"><span data-stu-id="e36d7-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="e36d7-217">Veri Yönetimi:</span><span class="sxs-lookup"><span data-stu-id="e36d7-217">Data Management:</span></span>

  - [<span data-ttu-id="e36d7-218">Veri yönetimi</span><span class="sxs-lookup"><span data-stu-id="e36d7-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)

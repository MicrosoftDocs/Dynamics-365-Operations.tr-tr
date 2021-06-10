---
title: Finans ile tümleştirme SSS
description: Bu konu altında, bir İnsan Kaynakları ve Finance tümleştirmesinde hangi verilerin eşitleneceği açıklanmaktadır.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2ac28a1bd09cf68c711295116fb007bdfab2070
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053407"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="6cb9f-103">Finans ile tümleştirme SSS</span><span class="sxs-lookup"><span data-stu-id="6cb9f-103">Integration with Finance FAQ</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6cb9f-104">Bu konu, hangi verilerin Dynamics 365 Human Resources, Dynamics 365 Finance ile tümleştirildiğinde eşitleneceğine dair sıkça sorulan soruları yanıtlar.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a><span data-ttu-id="6cb9f-105">Power Apps uygulamasında Dynamics 365 Talent uygulama kullanıcısını düzenleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-105">Can I edit the Dynamics 365 Talent application user in Power Apps?</span></span>

<span data-ttu-id="6cb9f-106">Hayır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-106">No.</span></span> <span data-ttu-id="6cb9f-107">Eğer Human Resources uygulama kullanıcısını düzenlerseniz, Human Resources ve Dataverse arasındaki bütünleşme başarısız olabilir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-107">If you edit the Human Resources application user, the integration between Human Resources and Dataverse might fail.</span></span> <span data-ttu-id="6cb9f-108">Aşağıdaki tabloda, Talent uygulama kullanıcısı için varsayılan ayarlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-108">The following table shows the default settings for the Talent application user.</span></span>

| <span data-ttu-id="6cb9f-109">Tam Ad</span><span class="sxs-lookup"><span data-stu-id="6cb9f-109">Full Name</span></span> | <span data-ttu-id="6cb9f-110">Başvuru kodu</span><span class="sxs-lookup"><span data-stu-id="6cb9f-110">Application ID</span></span> | <span data-ttu-id="6cb9f-111">Azure AD Nesne kodu</span><span class="sxs-lookup"><span data-stu-id="6cb9f-111">Azure AD Object ID</span></span> | <span data-ttu-id="6cb9f-112">Başvuru kodu URI</span><span class="sxs-lookup"><span data-stu-id="6cb9f-112">Application ID URI</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="6cb9f-113">Dynamics365 for Talent</span><span class="sxs-lookup"><span data-stu-id="6cb9f-113">Dynamics365 for Talent</span></span> | <span data-ttu-id="6cb9f-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="6cb9f-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> | <span data-ttu-id="6cb9f-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span><span class="sxs-lookup"><span data-stu-id="6cb9f-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span></span> | <span data-ttu-id="6cb9f-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="6cb9f-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> |

![Talent uygulama kullanıcısı için varsayılan ayarlar](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="6cb9f-118">Tüm veriler mi eşitlenir yoksa yalnızca bazı veri varlıkları mı?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-118">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="6cb9f-119">Bir veri alt kümesi eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-119">A subset of the data is synchronized.</span></span> <span data-ttu-id="6cb9f-120">Tüm varlıkların listesi için bkz. [Dynamics 365 Finance tümleştirmesi](hr-admin-integration-finance.md).</span><span class="sxs-lookup"><span data-stu-id="6cb9f-120">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a><span data-ttu-id="6cb9f-121">Dataverse'e eşitlenen verileri neden göremiyorum?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-121">Why don't I see any data synced to Dataverse?</span></span>

<span data-ttu-id="6cb9f-122">Varsayılan olarak, Dataverse tümleştirmesi sağlanan demo verileri içermeyen yeni ortamlarda kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-122">By default, the Dataverse integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="6cb9f-123">Varsayılan olarak, demo verileri içeren yeni ortamlarda açıktır ve ortam sağlandığında veri eşitlemesi başlar.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-123">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="6cb9f-124">Ortamınız veri eşitlemeye hazır olduktan sonra tümleştirmeyi açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-124">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="6cb9f-125">Daha fazla bilgi için bkz. [Dataverse tümleştirmesini yapılandırma](hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="6cb9f-125">For more information, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="6cb9f-126">Yeni bir eşlemeyi şablonları kullanmadan oluşturabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-126">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="6cb9f-127">Şablonları, başlangıç noktasıdır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-127">Templates are the starting point.</span></span> <span data-ttu-id="6cb9f-128">Kendi şablonunuzu oluşturabilirsiniz, ancak şablon bir tümleştirme projesi oluşturma sırasında her zaman gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-128">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="6cb9f-129">Veri tümleştirme (DI) şablonları ve projeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse için veri tümleştirme](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="6cb9f-129">For more information about data integrator (DI), templates, and projects, see [Integrate data into Microsoft Dataverse](/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="6cb9f-130">İnsan Kaynakları ve Finance arasında aktarmak üzere mali boyutlar eşleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-130">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="6cb9f-131">Mali boyutlar şu anda Dataverse içinde mevcut değildir ve bunu sonucunda varsayılan şablonun parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-131">Financial dimensions aren’t currently in Dataverse and as a result aren’t part of the default template.</span></span> <span data-ttu-id="6cb9f-132">Bu varlık planlanmıştır, ancak şu anda zaman çizelgesi mevcut değildir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-132">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="6cb9f-133">Finance içinde bulunan ancak Human Resources içinde bulunmayan veri için iki sistemi birbirine Human Resources için **Bağlantıları yapılandır**'ı kullanarak bağlayın.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-133">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![Mali boyutları eşle](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="6cb9f-135">Bazı durumlarda çalışanları içe aktardığım zaman, Finance'te devre dışı çalışanlar haline geliyorlar.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-135">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="6cb9f-136">Neden?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-136">Why?</span></span>

<span data-ttu-id="6cb9f-137">Çalışanların İnsan Kaynakları içinde etkin bir çalışma ayrıntısı kaydı yoksa bu hatayı alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-137">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="6cb9f-138">Bunu çözümlemek için **Personel Yönetimi \> Çalışanlar \> Çalışma Geçmişi \> Veri Yöneticisi**'ne gidin ve etkin bir çalışan ayrıntı kaydı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-138">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="6cb9f-139">Yalnızca bir alan alt kümesine eşleşmeyi seçersem, eşleştirilmemiş alanlara yapılan değişiklikler bir eşitleme tetikler mi?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-139">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="6cb9f-140">Veri eşitleme yürütme planını izler.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-140">Data sync follows the execution schedule.</span></span> <span data-ttu-id="6cb9f-141">Tümleştirme, alanın tümleştirme eşleştirmesinin parçası olup olmadığından bağımsız olarak kayıttaki herhangi bir alan değişirse kaydı çekecektir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-141">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="6cb9f-142">Yalnızca etkin alt değişiklikleri ve işten çıkarılan kayıtların nasıl gönderebilirim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-142">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="6cb9f-143">"Gelişmiş sorgu" kullanarak, kaynak verisini hedefe aktarmadan önce filtreleyebilir ve şekillendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-143">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Etkin çalışan gelişmiş sorgusu](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="6cb9f-145">Belirli bir varlık için hangi alanların Finance'e gönderileceğini belirtebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-145">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="6cb9f-146">Alanlar tümleştirme görevinden eklenebilir veya çıkartılabilir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-146">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="6cb9f-147">Dataverse tablosu içinde mevcut olan tüm veri alanlarıİnsan Kaynakları'ndan doldurulmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-147">Not all data fields that exist on the Dataverse table will be populated from Human Resources.</span></span>
<span data-ttu-id="6cb9f-148">Ek veriler Power Apps ile doldurulabilir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-148">Additional data can be populated via Power Apps.</span></span>

![Bir tümleştirme görevinden alanları ekleyin veya çıkartın](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="6cb9f-150">Tümleştirmeyi bir toplu iş olarak ayarlıyorum, ancak hedef sisteme İnsan Kaynakları bağlantıyı kaybetti.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-150">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="6cb9f-151">Aynı değişiklik kümesini hedef sisteme nasıl gönderebilirim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-151">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="6cb9f-152">Özel durum işleme için özel bir kurulum gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-152">No special setup is required for exception handling.</span></span> <span data-ttu-id="6cb9f-153">Veri Tümleştirme, kaynak ve hedefte gerçekleşen hatları yakalar ve raporlar ve el ile yeniden denemelere izin verecektir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-153">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="6cb9f-154">Ancak, el ile veri düzeltmeye izin vermez.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-154">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="6cb9f-155">Veri güncelleştirmeleri gerekliyse, kaynak veya hedefte gerçekleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-155">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="6cb9f-156">Çift yönlü tümleştirme ayarlayabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-156">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="6cb9f-157">Hayır, tümleştirme Şu anda tek yönlü (Finance and Operations'tan İnsan Kaynakları).</span><span class="sxs-lookup"><span data-stu-id="6cb9f-157">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="6cb9f-158">Bununla birlikte, İnsan Kaynakları'ndan Finance'e veri göndermek için bir varsayılan şablon vardır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-158">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="6cb9f-159">Tümleştirmemin bir parçası olarak kayıt silinmesine izin verebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-159">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="6cb9f-160">Hayır, Veri Tümleştirici, silinen kayıtları veri aktarımı için yakalamayacaktır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-160">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="6cb9f-161">Yalnızca veri oluşturma ve güncelleştirme (UPSERT) şu anda dahildir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-161">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="6cb9f-162">Hatalı yürütmeyi yeniden çalıştırabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-162">Can I rerun the errored execution?</span></span> <span data-ttu-id="6cb9f-163">Bu durumda, tam dosya mı gönderir yalnızca değişiklikleri mi?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-163">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="6cb9f-164">Veri Tümleştiricinin ilk çalıştırılması her zaman tam çalıştırmadır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-164">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="6cb9f-165">Sonraki yürütmeler değişiklik izlemeye dayanır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-165">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="6cb9f-166">Bir hatalı çalışma yürütülürse, yürütme kapsamdaki kayıtları çıkartır ve Dataverse'ten en güncel değişiklikleri gönderir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-166">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Dataverse.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="6cb9f-167">Proje kaydettiğimde, "Proje eşleme hatalarına sahip" hatasını alıyorum.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-167">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="6cb9f-168">Ne yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-168">What do I do?</span></span>

<span data-ttu-id="6cb9f-169">Tümleştirme anahtarlarınızı kurulumunu denetleyin, kurulum için gerekli değişiklikleri yapın ve sonra varlıkları projedeki yenileyin.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-169">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="6cb9f-170">Varsayılan şablon kullanıldığında, tümleştirme anahtarları otomatik olarak alınacak.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-170">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="6cb9f-171">Var olan şablona yeni görevler eklendiğinde bu sorun ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-171">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="6cb9f-172">Çalışanların işe sahip olduğu N sayıda tüzel varlığa sahipsem, bunların her biri için eşleşme oluşturmam gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-172">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="6cb9f-173">Evet, Finance'teki her bir tüzel kişilik için, veri tümleştirmede ayrı bir tümleştirme projesine gereksiniminiz olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-173">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="6cb9f-174">Microsoft tarafından sağlanan varsayılan şablonun parçası olmayan verileri aktarmak gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-174">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="6cb9f-175">Bunu yapabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-175">Can I do this?</span></span>

<span data-ttu-id="6cb9f-176">Evet, var olan şablondan alanlar kaldırılabilir veya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-176">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="6cb9f-177">Şablon diğer Dataverse tabloları için ek verileri dahil etmek üzere değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-177">The template can be modified to include additional data from other Dataverse tables.</span></span> <span data-ttu-id="6cb9f-178">Varlığın, şablona dahil edilmesi için Dataverse içinde olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-178">The entity must be in Dataverse for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="6cb9f-179">Kısa süre önce Finance ve İnsan Kaynakları ortamları oluşturdum ve "Veri değeri tutarlılık kısıtlamalarını ihlal ediyor" hatasını alıyorum.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-179">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="6cb9f-180">Neden?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-180">Why?</span></span>

<span data-ttu-id="6cb9f-181">Bu hatanın nedenleri arasında şunlar olabilir:</span><span class="sxs-lookup"><span data-stu-id="6cb9f-181">Reasons for this error can include:</span></span>

- <span data-ttu-id="6cb9f-182">Veri aktarma, kaynakta (Dataverse) yinelenen kayıtların ayıklanmasıyla sonuçlandı.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-182">The data transfer resulted in duplicate records extraction at the source (Dataverse).</span></span>

- <span data-ttu-id="6cb9f-183">Veri aktarımı, Finance and Operations'ta ihtiyaç duyulan alanlar için boş değerlere sahip.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-183">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="6cb9f-184">Verinin Dataverse içindeki olduğundan ve Finance and Operations gereksinimlerini karşıladığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-184">Verify the data that is in Dataverse and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="6cb9f-185">Yürütme hataları varsa ve Çalışan kimliği eşitlenmediyse, hatalı çalışan kaydına sahip geçmiş işi nasıl bulabilirim?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-185">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="6cb9f-186">Veri Tümleştirici, Finance'te birden fazla proje oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-186">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="6cb9f-187">Veri Tümleştirici görevi ve Finance projesi arasındaki ilişki bire bir ilişkidir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-187">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="6cb9f-188">Veri Tümleştirici yürütme geçmişinden zamanı takip edin ve Finance'te dizin -1 olan projeyi arayın.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-188">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="6cb9f-189">Görev numarası Veri Tümleştirici'de 9 ise, Finance'teki dizin 8'dir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-189">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="6cb9f-190">Veri Tümleştiricisinden görev dizinini yakalayın (bu örnekte "9"dur).</span><span class="sxs-lookup"><span data-stu-id="6cb9f-190">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![Veri Tümleştiricisinden görev dizinini yakalayın.](media/CaptureTaskIndex.png)

2. <span data-ttu-id="6cb9f-192">Projenin yürütme zamanını izleyin.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-192">Track the execution time of the project.</span></span>

    ![Projenin yürütme zamanını izleyin](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="6cb9f-194">Finance'te - 1 dizini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-194">In Finance, identify index - 1.</span></span> <span data-ttu-id="6cb9f-195">Bu örnekte, sonek "8"e sahip olan ve yürütme zamanı dizin "0" projesi olan proje, Adım 2'deki yürütme zamanı ile eşleşiyor.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-195">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![Dizini tanımlayın](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="6cb9f-197">İnsan Kaynakları ve finans'yı tümleştirdikten sonra, İnsan Kaynakları verilerimi finans içinde görmüyorum.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-197">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="6cb9f-198">Ne yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-198">What do I do?</span></span>

<span data-ttu-id="6cb9f-199">Finance'e tümleştirme iki adımlı bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-199">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="6cb9f-200">Öncelikle, İnsan Kaynakları verisinin güncelleştirilmiş ve Dataverse içinde kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-200">First, verify that the Human Resources data is updated and available in Dataverse.</span></span> <span data-ttu-id="6cb9f-201">Bu neredeyse gerçek zamanlı bir eşitlemedir ve Power Apps içinde veri tabloları içindeki veriye bakarak doğrulanabilir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-201">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data tables.</span></span>

![Dataverse içindeki veri](media/DataInCDS.png)

<span data-ttu-id="6cb9f-203">Veri Dataverse'te beklendiği gibi görüntülenmiyorsa, varlığın tümleştirme ile desteklendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-203">If the data is not appearing as expected in Dataverse, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="6cb9f-204">Dataverse içine ek veri dahil etmek için Microsoft tarafından bir değişiklik gerekir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-204">To include additional data in Dataverse, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="6cb9f-205">Varlık destekleniyorsa ve veri Dataverse içinde kullanılabilirse, Veri Tümleştiricisi içinde eşleştirmenin doğru olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-205">If the entity is supported and the data is available in Dataverse, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="6cb9f-206">Tümleştirme eşleştirmesi doğru gözüküyorsa, veri yönetimi işlerini başarıyla çalıştırıldığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-206">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="6cb9f-207">Toplu işlerin yürütülmesinde hatalar ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-207">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="6cb9f-208">Veri Yönetimi hakkında daha fazla bilgi için bkz. [Veri yönetimi](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="6cb9f-208">For more information about Data Management, see [Data management](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="6cb9f-209">Çalışanlarımın adresleri Finance'e aktardıktan sonra doğru görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-209">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="6cb9f-210">Ne yapmalıyım?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-210">What should I do?</span></span>

<span data-ttu-id="6cb9f-211">**Konum Kodu** için numara serisi, İnsan Kaynakları'ta ve Finance'te aynı düzeni kullanır.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-211">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="6cb9f-212">Numara serisinin her iki tarafta da benzersiz olması gerekir, bu sayede veriyi Dataverse'ten Finance and Operations'a tümleştirirken adres çakışmaları gerçekleşmez.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-212">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Dataverse to Finance and Operations.</span></span>

<span data-ttu-id="6cb9f-213">İnsan Kaynakları tümleştirmesi sırasında, numara serilerinin İnsan Kaynakları ve Finance içinde aynı olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-213">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="6cb9f-214">Tüm numara serilerinin, verinin her iki sistemde de tutulabildiği yerlerde aynı olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-214">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="6cb9f-215">Bağlantımı kümesi oluştururken, Bağlantı açılır listesinde bağlantıyı göremiyorum.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-215">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="6cb9f-216">Ne yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-216">What do I do?</span></span>

<span data-ttu-id="6cb9f-217">Bağlantılarınızı oluştururken Dynamics 365 Finance'i ve Dataverse'i seçtiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-217">Make sure when creating your connections, you choose Dynamics 365 Finance and Dataverse.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="6cb9f-218">Çalışmaları eşitlerken “CompanyInfo_FK mevcut değil" veya “Değer 12/31/2154 11:59:59 pm', 'Çalışma sonlanma tarihi' ilgili 'Çalışma' tablosunda bulunamadı.” hatasını alıyorum. Ne yapmalıyım?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-218">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="6cb9f-219">Doğru tüzel varlıkları eşlediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-219">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="6cb9f-220">Tüzel varlık eşitleme, varsayılan şablonun parçası değildir, bu nedenle İnsan Kaynakları ve Dataverse bulunan her bir tüzel varlığın Finance'te de mevcut olması beklenir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-220">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Dataverse is also present in Finance.</span></span>
<span data-ttu-id="6cb9f-221">İlişkili Bağlantı Kümesi için doğru tüzel varlıkları seçtiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-221">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="6cb9f-222">Projemi ayarladıktan sonra Finance için alan eşleşmesi boş görünüyor.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-222">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="6cb9f-223">Ne yapmalıyım?</span><span class="sxs-lookup"><span data-stu-id="6cb9f-223">What should I do?</span></span>

<span data-ttu-id="6cb9f-224">Finance'te veri varlıklarını **Veri yönetimi \> Çerçeve Parametreleri \> Varlık ayarları \> Varlık listesini yenile**'ye giderek yenileyin.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-224">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="6cb9f-225">Bunun tamamlanması birkaç dakika sürer ve daha sonra bu eşleşmeleri görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-225">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="6cb9f-226">Yeni proje oluşturulduğunda bu sorun oluşur.</span><span class="sxs-lookup"><span data-stu-id="6cb9f-226">This issue occurs when new projects are created.</span></span>

![Eksik alan eşlemeleri](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="6cb9f-228">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6cb9f-228">Additional resources</span></span>

- <span data-ttu-id="6cb9f-229">Veri Tümleştirici (DI):</span><span class="sxs-lookup"><span data-stu-id="6cb9f-229">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="6cb9f-230">Veriyi Microsoft Dataverse içine tümleştir</span><span class="sxs-lookup"><span data-stu-id="6cb9f-230">Integrate data into Microsoft Dataverse</span></span>](/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="6cb9f-231">Veri Tümleştirici hata yönetimi ve sorun giderme</span><span class="sxs-lookup"><span data-stu-id="6cb9f-231">Data Integrator error management and troubleshooting</span></span>](/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="6cb9f-232">Power Apps, Microsoft Power Automate ve Dataverse'te sistem tarafından oluşturulan günlükler için DSR taleplerine yanıt verme</span><span class="sxs-lookup"><span data-stu-id="6cb9f-232">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Dataverse</span></span>](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="6cb9f-233">Veri Yönetimi:</span><span class="sxs-lookup"><span data-stu-id="6cb9f-233">Data Management:</span></span>

  - [<span data-ttu-id="6cb9f-234">Veri yönetimi</span><span class="sxs-lookup"><span data-stu-id="6cb9f-234">Data management</span></span>](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
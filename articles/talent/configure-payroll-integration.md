---
title: "Talent ile Dayforce arasında bordro tümleştirmesini yapılandırma"
description: "Bu konuda, bir ödeme işlemini işlemek üzere Microsoft Dynamics 365 for Talent ile Ceridian Dayforce arasındaki tümleştirmeyi nasıl yapılandıracağınız açıklanmaktadır."
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="4bb29-103">Talent ile Dayforce arasında bordro tümleştirmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4bb29-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4bb29-104">Microsoft Dynamics 365 for Talent ile Ceridian Dayforce arasındaki tümleştirme, bu konuda açıklanan çeşitli yapılandırma adımlarına dayanır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="4bb29-105">Ödeme işlemini işlemeden önce tümleştirmeyi hem Talent hem de Dayforce'ta yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="4bb29-106">Ödeme işlemlerini tamamlamak için Dayforce gibi bir hizmet kullandığınızda tümleştirmeyi Talent'ta etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="4bb29-107">Tümleştirme için Talent'tan özel veriler gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="4bb29-108">Bu nedenle, Dayforce ile eşlenmiş verilerin Talent'ta tümleştirmeyi destekleyecek şekilde yapılandırıldığını doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="4bb29-109">Tümleştirme, aşağıdaki geniş veri kategorilerini kullanır:</span><span class="sxs-lookup"><span data-stu-id="4bb29-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="4bb29-110">İnsan kaynakları verileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-110">Human resources data</span></span>
- <span data-ttu-id="4bb29-111">Ücret verileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-111">Compensation data</span></span>
- <span data-ttu-id="4bb29-112">Ödeme döngüleri, ödeme dönemleri ve kazanç kodları gibi bordro verileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="4bb29-113">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-113">Worker data</span></span>

<span data-ttu-id="4bb29-114">Bu konuda, tümleştirmeyi etkinleştirmek için izlemeniz gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="4bb29-115">Ayrıca veri türleri ve tümleştirmenin gerektirdiği yapılandırma ayrıntıları da açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="4bb29-116">Tümleştirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4bb29-116">Enable the integration</span></span>

<span data-ttu-id="4bb29-117">Talent'ta yapılandırmayı açmanız ve Dayforce'a bağlanmak için yapılandırma bilgilerini girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="4bb29-118">Microsoft Dynamics 365 for Finance and Operations'a aktarılmak üzere oluşturulan genel muhasebe hareketini istiyorsanız ayrıca bir Microsoft Azure depolama hesabı oluşturmanız ve Finance and Operations'ta Azure Depolama bağlantı dizesini de girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="4bb29-119">Talent'ta tümleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4bb29-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="4bb29-120">**Sistem yönetimi** sayfasında **Tümleştirme yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4bb29-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="4bb29-121">Güvenli Dosya Aktarım Protokolü (FTP) uç noktasını ve güvenli FTP klasörü yolunu girin.</span><span class="sxs-lookup"><span data-stu-id="4bb29-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="4bb29-122">Güvenli FTP uç noktasına ve klasör yoluna erişecek kullanıcının kullanıcı adını ve parolasını girin.</span><span class="sxs-lookup"><span data-stu-id="4bb29-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="4bb29-123">Bağlantıyı gerektiği gibi test edin ve **Bordro tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4bb29-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="4bb29-124">Tümleştirme açıldığında veri dışa aktarma paketi ve dosyalar oluşturulur ve sıklık ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="4bb29-125">Bu sıklığı ihtiyaç duyduğunuz şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bb29-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="4bb29-126">Azure depolama hesapları ve Azure Depolama bağlantı dizeleri hakkında daha fazla bilgi için aşağıdaki Azure konularına bakın:</span><span class="sxs-lookup"><span data-stu-id="4bb29-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="4bb29-127">Azure depolama hesapları hakkında</span><span class="sxs-lookup"><span data-stu-id="4bb29-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="4bb29-128">Azure Depolama bağlantı dizelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4bb29-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="4bb29-129">Verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4bb29-129">Configure your data</span></span> 

<span data-ttu-id="4bb29-130">Bordro işlemek için Talent'ta insan kaynağı verilerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="4bb29-131">Kazanç ve ücret bilgileriyle birlikte işler ve pozisyonlar gibi kurumsal verileri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="4bb29-132">Bu bilgiler personel ödemesi oluşturmak için gerekli olan istihdam, ödeme ve kesinti bilgilerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="4bb29-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="4bb29-133">İnsan kaynağı verileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="4bb29-134">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="4bb29-134">Benefits</span></span> 

<span data-ttu-id="4bb29-135">İnsan kaynakları, bir kuruluşun çalışanları için sunduğu veya işlediği kazançları, kesintileri ve çalışan ücret planlarını ayarlamak ve bunları yönetmek için kullanılan araçları sağlar.</span><span class="sxs-lookup"><span data-stu-id="4bb29-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="4bb29-136">Kazançları oluştururken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="4bb29-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="4bb29-137">Kazanç planları</span><span class="sxs-lookup"><span data-stu-id="4bb29-137">Benefit plans</span></span>

- <span data-ttu-id="4bb29-138">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-138">Plan (required)</span></span>
- <span data-ttu-id="4bb29-139">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-139">Type (required)</span></span>
- <span data-ttu-id="4bb29-140">Bordro etkisi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-140">Payroll impact (required)</span></span>
- <span data-ttu-id="4bb29-141">Borçları kurtar</span><span class="sxs-lookup"><span data-stu-id="4bb29-141">Recover arrears</span></span>
- <span data-ttu-id="4bb29-142">Kesinti yöntemi</span><span class="sxs-lookup"><span data-stu-id="4bb29-142">Deduction method</span></span>
- <span data-ttu-id="4bb29-143">Kesinti önceliği</span><span class="sxs-lookup"><span data-stu-id="4bb29-143">Deduction priority</span></span>
- <span data-ttu-id="4bb29-144">Dönemi sınırla</span><span class="sxs-lookup"><span data-stu-id="4bb29-144">Limit period</span></span>
- <span data-ttu-id="4bb29-145">Sınır tutar</span><span class="sxs-lookup"><span data-stu-id="4bb29-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="4bb29-146">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="4bb29-146">Benefits</span></span>

- <span data-ttu-id="4bb29-147">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-147">Plan (required)</span></span>
- <span data-ttu-id="4bb29-148">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-148">Type (required)</span></span>
- <span data-ttu-id="4bb29-149">Seçenek (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-149">Option (required)</span></span>
- <span data-ttu-id="4bb29-150">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-150">Benefit ID (required)</span></span>
- <span data-ttu-id="4bb29-151">Sıklık</span><span class="sxs-lookup"><span data-stu-id="4bb29-151">Frequency</span></span>
- <span data-ttu-id="4bb29-152">Temel</span><span class="sxs-lookup"><span data-stu-id="4bb29-152">Basis</span></span>
- <span data-ttu-id="4bb29-153">Tutar veya oran</span><span class="sxs-lookup"><span data-stu-id="4bb29-153">Amount or rate</span></span>
- <span data-ttu-id="4bb29-154">Kazanç kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="4bb29-155">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="4bb29-155">Supported frequencies</span></span> 

- <span data-ttu-id="4bb29-156">Haftalık</span><span class="sxs-lookup"><span data-stu-id="4bb29-156">Weekly</span></span>
- <span data-ttu-id="4bb29-157">İki haftada bir</span><span class="sxs-lookup"><span data-stu-id="4bb29-157">Bi-weekly</span></span>
- <span data-ttu-id="4bb29-158">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="4bb29-158">Semi-monthly</span></span>
- <span data-ttu-id="4bb29-159">Aylık</span><span class="sxs-lookup"><span data-stu-id="4bb29-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="4bb29-160">Desteklenen tabanlar</span><span class="sxs-lookup"><span data-stu-id="4bb29-160">Supported bases</span></span> 

- <span data-ttu-id="4bb29-161">Sabit tutar</span><span class="sxs-lookup"><span data-stu-id="4bb29-161">Fixed amount</span></span>
- <span data-ttu-id="4bb29-162">Kazançların yüzdesi</span><span class="sxs-lookup"><span data-stu-id="4bb29-162">Percent of earnings</span></span>
- <span data-ttu-id="4bb29-163">Üretime yönelik saatler</span><span class="sxs-lookup"><span data-stu-id="4bb29-163">Productive hours</span></span>

<span data-ttu-id="4bb29-164">Dayforce, kazanç planında tanımlanan bordro etkisine göre aşağıdaki kesintileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bb29-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="4bb29-165">Talent'ta seçim</span><span class="sxs-lookup"><span data-stu-id="4bb29-165">Selection in Talent</span></span>        | <span data-ttu-id="4bb29-166">Dayforce'ta sonuç</span><span class="sxs-lookup"><span data-stu-id="4bb29-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="4bb29-167">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="4bb29-167">None</span></span>                       | <span data-ttu-id="4bb29-168">Kesinti oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="4bb29-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="4bb29-169">Yalnızca kesinti</span><span class="sxs-lookup"><span data-stu-id="4bb29-169">Deduction only</span></span>             | <span data-ttu-id="4bb29-170">Personel kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4bb29-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="4bb29-171">Yalnızca katkı</span><span class="sxs-lookup"><span data-stu-id="4bb29-171">Contribution only</span></span>          | <span data-ttu-id="4bb29-172">İşveren kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4bb29-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="4bb29-173">Kesinti ve katkı</span><span class="sxs-lookup"><span data-stu-id="4bb29-173">Deduction and contribution</span></span> | <span data-ttu-id="4bb29-174">Personel ve işveren kesintileri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4bb29-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="4bb29-175">Kazanç programı tanımlama ve yönetme hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="4bb29-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="4bb29-176">Personel kazançları programı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bb29-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="4bb29-177">Yeni kazanç oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bb29-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="4bb29-178">Kazanç uygunluk kurallarını ve ilkelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="4bb29-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="4bb29-179">Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma</span><span class="sxs-lookup"><span data-stu-id="4bb29-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="4bb29-180">Ücret</span><span class="sxs-lookup"><span data-stu-id="4bb29-180">Compensation</span></span> 

<span data-ttu-id="4bb29-181">Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="4bb29-182">Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="4bb29-183">İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="4bb29-184">Dayforce personelin saatlik veya yıllık ücretlerini hesaplamak için ücret bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="4bb29-185">Sabit ücret planları ve ödeme oranı dönüştürmeleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="4bb29-186">Personelin bir sabit ücret planıyla ilişkilendirilmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="4bb29-187">Ücret planları hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="4bb29-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="4bb29-188">Sabit ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bb29-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="4bb29-189">Değişken ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bb29-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="4bb29-190">Maaş/ücret yapısı ve planları geliştirme</span><span class="sxs-lookup"><span data-stu-id="4bb29-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="4bb29-191">İşlem ücreti</span><span class="sxs-lookup"><span data-stu-id="4bb29-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="4bb29-192">Ücret işlemini tanımlama ve sonuçları hesaplama</span><span class="sxs-lookup"><span data-stu-id="4bb29-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="4bb29-193">Personeli sabit ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="4bb29-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="4bb29-194">Personeli değişken ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="4bb29-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="4bb29-195">İşler</span><span class="sxs-lookup"><span data-stu-id="4bb29-195">Jobs</span></span> 

<span data-ttu-id="4bb29-196">Bir iş, işi gerçekleştiren kişiden beklenen görev ve sorumlulukların toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="4bb29-197">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="4bb29-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="4bb29-198">İşin bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4bb29-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="4bb29-199">Yeni işler tanımlama</span><span class="sxs-lookup"><span data-stu-id="4bb29-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="4bb29-200">Pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="4bb29-200">Positions</span></span>

<span data-ttu-id="4bb29-201">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="4bb29-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="4bb29-202">Örneğin, "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş pozisyonlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="4bb29-203">Bir pozisyon, bir departmanda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4bb29-203">A position exists in a department.</span></span> <span data-ttu-id="4bb29-204">Her pozisyonla yalnızca bir çalışan ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="4bb29-205">Pozisyonları ayarlarken aşağıdaki verileri ve yapılandırmayı göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="4bb29-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="4bb29-206">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-206">Position (required)</span></span>
- <span data-ttu-id="4bb29-207">Açıklama (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-207">Description (required)</span></span>
- <span data-ttu-id="4bb29-208">İş (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-208">Job (required)</span></span>
- <span data-ttu-id="4bb29-209">Departman (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-209">Department (required)</span></span>
- <span data-ttu-id="4bb29-210">Pozisyon türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-210">Position type (required)</span></span>
- <span data-ttu-id="4bb29-211">Tam zamanlı eşdeğeri</span><span class="sxs-lookup"><span data-stu-id="4bb29-211">Full-time equivalent</span></span>
- <span data-ttu-id="4bb29-212">Yıllık mesai saatleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="4bb29-213">Tüzel kişilik tarafından ödenen (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="4bb29-214">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-214">Pay cycle (required)</span></span>
- <span data-ttu-id="4bb29-215">Varsayılan mali boyut – Maliyet merkezi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="4bb29-216">Çalışan ataması: Çalışan, atama başlangıç tarihi, atama bitiş tarihi, neden kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="4bb29-217">Aynı departmanda birden fazla pozisyon aynı işle ilişkilendirilmişse bunlar Dayforce'ta tek bir pozisyonda konsolide edilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="4bb29-218">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="4bb29-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="4bb29-219">Departmanlar, işler ve pozisyonları kullanarak iş gücünüzü düzenleme</span><span class="sxs-lookup"><span data-stu-id="4bb29-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="4bb29-220">Pozisyonları ayarlama</span><span class="sxs-lookup"><span data-stu-id="4bb29-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="4bb29-221">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="4bb29-221">Departments</span></span>

<span data-ttu-id="4bb29-222">Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="4bb29-223">Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur.</span><span class="sxs-lookup"><span data-stu-id="4bb29-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="4bb29-224">İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bb29-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="4bb29-225">Departmanların kâr ve zarar sorumluluğu olabilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="4bb29-226">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="4bb29-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="4bb29-227">Departman oluşturma ve departman hiyerarşisi ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="4bb29-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="4bb29-228">Yeni departmanlar tanımlama</span><span class="sxs-lookup"><span data-stu-id="4bb29-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="4bb29-229">Ödeme döngüleri ve ödeme dönemleri</span><span class="sxs-lookup"><span data-stu-id="4bb29-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="4bb29-230">Ödeme döngüsü, bordronun ne sıklıkta çalıştırıldığını ve çalışanlara ödeme yapılan belirli günleri belirler.</span><span class="sxs-lookup"><span data-stu-id="4bb29-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="4bb29-231">Örneğin, bir ödeme döngüsü aylık olabilir ve personele ayın son günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="4bb29-232">Alternatif olarak, bir ödeme döngüsü haftalık olabilir ve personele ödeme döneminin bitişinden sonraki Salı günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="4bb29-233">Ödeme döngüleri, bu pozisyonlardaki çalışanlara ne zaman ödeme yapıldığını kontrol etmek için pozisyonlara atanır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="4bb29-234">Ödeme döngülerini oluşturduktan sonra her döngü için ödeme dönemleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bb29-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="4bb29-235">Her ödeme dönemi, sağladığınız bilgilere göre varsayılan bir ödeme tarihi içerir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="4bb29-236">Ancak ödeme döneminin bir tatil gününe denk gelmesi gibi istisnalara izin vermek için ödeme döneminde varsayılan ödeme tarihini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bb29-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="4bb29-237">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="4bb29-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="4bb29-238">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-238">Pay cycle (required)</span></span>
- <span data-ttu-id="4bb29-239">Ödeme döngüsü sıklığı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="4bb29-240">Dönem başlangıç tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="4bb29-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="4bb29-241">Varsayılan ödeme tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="4bb29-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="4bb29-242">Bu bilgiler ödeme grupları olarak Dayforce ile tümleştirilir ve her ödeme döngüsü için ülke veya bölgeye göre ayrılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="4bb29-243">Tümleştirmeden önce en az bir ödeme dönemi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="4bb29-244">Dayforce, ilk ödeme döneminin başlangıç tarihine ve Talent'ta ayarlanan varsayılan ödeme tarihine bağlı olarak ödeme grubu takvimlerini ve ödeme tarihlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bb29-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="4bb29-245">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="4bb29-245">Earning codes</span></span>

<span data-ttu-id="4bb29-246">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4bb29-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="4bb29-247">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametrelere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="4bb29-248">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="4bb29-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="4bb29-249">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-249">Earning Code (required)</span></span>
- <span data-ttu-id="4bb29-250">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bb29-250">Description</span></span>
- <span data-ttu-id="4bb29-251">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="4bb29-251">Unit of measure</span></span>
- <span data-ttu-id="4bb29-252">Üretken</span><span class="sxs-lookup"><span data-stu-id="4bb29-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="4bb29-253">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-253">Worker data</span></span>

<span data-ttu-id="4bb29-254">Sahip olduğunuz çeşitli çalışan türlerine ilişkin kayıtlar, insan kaynaklarınız ve bordro sistemleriniz için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="4bb29-255">Girdiğiniz bilgiler çalışanları ve kişisel bilgileri izlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="4bb29-256">Çalışanlar hakkında aşağıdaki bilgileri koruyabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4bb29-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="4bb29-257">**Temel**: İletişim bilgileri, demografik bilgiler, kimlik bilgileri, aile bilgileri, askerlik hizmeti durumu, göçmenlik bilgileri ile kişisel ve acil durum iletişim kişileri gibi temel bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="4bb29-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="4bb29-258">**İstihdam**: Şirket veya kuruluş ilişkisi, pozisyon ataması, başlangıç ve bitiş tarihleri, iş uygunluğu, istihdam koşulları, emeklilik, tatil ve tayin bilgileri gibi bir çalışanın istihdamıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="4bb29-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="4bb29-259">**İzin ve devamsızlık**: Çalışma takvimleri, devamsızlık işlemleri ve devamsızlık ayarı gibi bir çalışanın devamsızlığıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="4bb29-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="4bb29-260">**Ücret ve bordro**: Plan kaydı, ödüller, performans, komisyon, vergi bilgileri, emeklilik ve maaş kesintileri gibi bir çalışanın ücret planlarıyla ilgili bilgileri ve bordro bilgilerini tutun.</span><span class="sxs-lookup"><span data-stu-id="4bb29-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="4bb29-261">Çalışan bilgilerini girerken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="4bb29-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="4bb29-262">Genel bilgiler</span><span class="sxs-lookup"><span data-stu-id="4bb29-262">General information</span></span>

- <span data-ttu-id="4bb29-263">Personel numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-263">Personnel number (required)</span></span>
- <span data-ttu-id="4bb29-264">Ad (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-264">First name (required)</span></span>
- <span data-ttu-id="4bb29-265">Soyadı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-265">Last name (required)</span></span>
- <span data-ttu-id="4bb29-266">İkinci adı</span><span class="sxs-lookup"><span data-stu-id="4bb29-266">Middle name</span></span>
- <span data-ttu-id="4bb29-267">Kıdem tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-267">Seniority date</span></span>
- <span data-ttu-id="4bb29-268">Bilinen hali</span><span class="sxs-lookup"><span data-stu-id="4bb29-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="4bb29-269">Kişisel bilgiler</span><span class="sxs-lookup"><span data-stu-id="4bb29-269">Personal information</span></span>

- <span data-ttu-id="4bb29-270">Medeni durum (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-270">Marital status (required)</span></span>
- <span data-ttu-id="4bb29-271">Doğum tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-271">Birth date (required)</span></span>
- <span data-ttu-id="4bb29-272">Cinsiyet (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-272">Gender (required)</span></span>
- <span data-ttu-id="4bb29-273">Engelli kişi</span><span class="sxs-lookup"><span data-stu-id="4bb29-273">Person with disabilities</span></span>
- <span data-ttu-id="4bb29-274">Uyruğu ülkesi bölgesi (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="4bb29-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="4bb29-275">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-275">Address information</span></span>

- <span data-ttu-id="4bb29-276">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-276">Primary (required)</span></span>
- <span data-ttu-id="4bb29-277">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-277">Country/region (required)</span></span>
- <span data-ttu-id="4bb29-278">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-278">Postal code (required)</span></span>
- <span data-ttu-id="4bb29-279">Cadde Numarası (gerekli) (Yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="4bb29-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="4bb29-280">Bina Tamamlayıcı (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="4bb29-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="4bb29-281">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-281">City (required)</span></span>
- <span data-ttu-id="4bb29-282">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-282">State (required)</span></span>
- <span data-ttu-id="4bb29-283">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="4bb29-284">İletişim bilgileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-284">Contact information</span></span> 

- <span data-ttu-id="4bb29-285">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-285">Primary (required)</span></span>
- <span data-ttu-id="4bb29-286">İlgili kişi numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-286">Contact number (required)</span></span>
- <span data-ttu-id="4bb29-287">Dahili</span><span class="sxs-lookup"><span data-stu-id="4bb29-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="4bb29-288">Bordro bilgileri ve kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="4bb29-288">Payroll information and earning codes</span></span>

<span data-ttu-id="4bb29-289">Personele belirli bir ödeme sıklığında özel kazançlar atanabilir ve çalışanlar, tercih edilen bir ödeme yöntemine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="4bb29-290">Bu tercihlerin ve ayarların kullanıldığının sağlanmasına yardımcı olmak için Dayforce'ta aşağıdaki alanlar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="4bb29-291">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="4bb29-291">Earning codes</span></span>

- <span data-ttu-id="4bb29-292">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-292">Position (required)</span></span>
- <span data-ttu-id="4bb29-293">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-293">Earning Code (required)</span></span>
- <span data-ttu-id="4bb29-294">Sıklık (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-294">Frequency (required)</span></span>
- <span data-ttu-id="4bb29-295">Tutar (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="4bb29-296">Bordro bilgileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-296">Payroll information</span></span>

- <span data-ttu-id="4bb29-297">Ödeme Yöntemi</span><span class="sxs-lookup"><span data-stu-id="4bb29-297">Payment Method</span></span>
- <span data-ttu-id="4bb29-298">Ekonomik Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-298">Economic Region (required)</span></span>
- <span data-ttu-id="4bb29-299">Personel Kazanç Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-299">Employee Benefits ID</span></span>
- <span data-ttu-id="4bb29-300">Ulusal Kimlik Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-300">National ID Number (required)</span></span>
- <span data-ttu-id="4bb29-301">Askerlik Hizmet Numarası</span><span class="sxs-lookup"><span data-stu-id="4bb29-301">Military Service Number</span></span>
- <span data-ttu-id="4bb29-302">Vardiya Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-302">Shift ID (required)</span></span>
- <span data-ttu-id="4bb29-303">Vergi Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-303">Tax Number (required)</span></span>
- <span data-ttu-id="4bb29-304">Sendika Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-304">Union ID (required)</span></span>
- <span data-ttu-id="4bb29-305">İş Günü Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-305">Work Day ID (required)</span></span>
- <span data-ttu-id="4bb29-306">Çalışma İzni Numarası</span><span class="sxs-lookup"><span data-stu-id="4bb29-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="4bb29-307">Meksika'da ödeme yöntemleri olarak **Nakit**, **Çek** (şirketin fiziksel çeki) ve **Elektronik Ödeme** desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="4bb29-308">Hiçbir ödeme yöntemi belirtilmemişse varsayılan olarak **Çek** kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="4bb29-309">İstihdam ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="4bb29-309">Employment details</span></span>

<span data-ttu-id="4bb29-310">İstihdam ayrıntıları geçmişi, personelin Dayforce'ta işe alma, işten çıkarma ve yeniden işe alma durumlarını oluşturmada temel bilgi olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="4bb29-311">Dayforce, bir defada yalnızca bir etkin istihdam kaydını destekler.</span><span class="sxs-lookup"><span data-stu-id="4bb29-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="4bb29-312">İşe başlama tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-312">Employment start date (required)</span></span>
- <span data-ttu-id="4bb29-313">İş bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-313">Employment end date</span></span>
- <span data-ttu-id="4bb29-314">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-314">Start date</span></span>
- <span data-ttu-id="4bb29-315">Ayarlanan başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-315">Adjusted start date</span></span>
- <span data-ttu-id="4bb29-316">İşten çıkarma tarihi (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="4bb29-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="4bb29-317">İşten çıkarma nedeni (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="4bb29-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="4bb29-318">Personelin önemli tarihleri aşağıdaki bilgiler kullanılarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="4bb29-319">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-319">Talent</span></span>                | <span data-ttu-id="4bb29-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb29-321">En son işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-321">Most recent hire date</span></span> | <span data-ttu-id="4bb29-322">Geçerli sonlandırılmamış işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="4bb29-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="4bb29-323">İşten çıkarma tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-323">Termination date</span></span>      | <span data-ttu-id="4bb29-324">Geçerli sonlandırılmamış işten çıkış tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="4bb29-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="4bb29-325">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-325">Start date</span></span>            | <span data-ttu-id="4bb29-326">Ayarlanan başlama tarihi, başlama tarihi veya geçerli etkin olmayan işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="4bb29-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="4bb29-327">Orijinal işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-327">Original hire date</span></span>    | <span data-ttu-id="4bb29-328">En erken işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="4bb29-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="4bb29-329">Ücret</span><span class="sxs-lookup"><span data-stu-id="4bb29-329">Compensation</span></span>

<span data-ttu-id="4bb29-330">Bir istihdam dönemi boyunca her personelin birincil pozisyonu ile sabit ücret planı ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="4bb29-331">Bu dönem personelin işe alındığı (veya işe başlama tarihi) tarihte başlar ve işten çıkış tarihine kadar devam eder.</span><span class="sxs-lookup"><span data-stu-id="4bb29-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="4bb29-332">Yürürlük Tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-332">Effective Date (required)</span></span>
- <span data-ttu-id="4bb29-333">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-333">Expiration date</span></span>
- <span data-ttu-id="4bb29-334">Ödeme Oranı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-334">Pay Rate (required)</span></span>
- <span data-ttu-id="4bb29-335">Ödeme Oranı Dönüştürmeleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="4bb29-336">Yıllık eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="4bb29-337">Saatlik eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="4bb29-338">Saatlik personelin birden fazla pozisyonu varsa birincil pozisyonun sabit ücreti, personel düzeyinde taban oranı/maaş olarak Dayforce'ta içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="4bb29-339">Birincil olmayan pozisyonlar için saatlik oran Dayforce'ta ilgili pozisyona kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="4bb29-340">Maaşlı personelin birden fazla pozisyonu varsa tüm etkin pozisyonlar için kümülatif saat oranı ve yıllık maaş oluşturulur ve personel düzeyinde taban oranı/maaş olarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="4bb29-341">Kimlik numaraları</span><span class="sxs-lookup"><span data-stu-id="4bb29-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="4bb29-342">Sosyal Güvenlik Kimlik Tanımlayıcı</span><span class="sxs-lookup"><span data-stu-id="4bb29-342">Social Security identifier</span></span> 

<span data-ttu-id="4bb29-343">Her personelin bir birincil kimlik tanımlayıcısı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="4bb29-344">Bu kimlik tanımlayıcı **SSK** kimlik türünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="4bb29-345">Dayforce'ta bu, personelin işe alınması için gereken Sosyal Güvenlik kimlik tanımlayıcı olarak otomatik türetilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="4bb29-346">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-346">Primary (required)</span></span>
- <span data-ttu-id="4bb29-347">Kimlik Türü = "SSN"</span><span class="sxs-lookup"><span data-stu-id="4bb29-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="4bb29-348">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="4bb29-348">Issued Date</span></span>
- <span data-ttu-id="4bb29-349">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-349">Expiration Date</span></span>

<span data-ttu-id="4bb29-350">Personel, **SSN** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="4bb29-351">Ancak numaranın etkin veya süresinin dolmuş olup olmadığına bakılmaksızın yalnızca **Birincil** olarak işaretlenen kayıt Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="4bb29-352">Banka hesapları ve tahsilatlar</span><span class="sxs-lookup"><span data-stu-id="4bb29-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="4bb29-353">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel için geçerli banka hesap bilgileri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="4bb29-354">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-354">Talent</span></span>                         | <span data-ttu-id="4bb29-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb29-356">Banka hesap numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="4bb29-357">SWIFT kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-357">SWIFT code (required)</span></span>          | <span data-ttu-id="4bb29-358">Meksika'da bordro işlemleri için **Banka Kodu** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="4bb29-359">Şube numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="4bb29-360">Banka hesabı türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-360">Bank account type (required)</span></span>   | <span data-ttu-id="4bb29-361">Meksika'da bordro işlemleri için **Hesap türü** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="4bb29-362">Desteklenen değerler **Cari** ve **Bordro**'yu içerir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="4bb29-363">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel, birincil adresi Meksika'da olan ve bir Meksika bankasındaki geçerli bir banka hesabıyla ilişkilendirilmiş tüzel kişilik altında bulunan bir bakiye hesabına bağlantı sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="4bb29-364">Bakiye hesabı olmayan diğer hesaplar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="4bb29-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="4bb29-365">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="4bb29-365">Address information</span></span>

<span data-ttu-id="4bb29-366">Her personelin bir birincil konumu olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-366">Every employee must have one primary location.</span></span> <span data-ttu-id="4bb29-367">Dayforce'ta bu konum, personelin vergiye esas birincil ikamet yerini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="4bb29-368">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-368">Primary (required)</span></span>
- <span data-ttu-id="4bb29-369">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-369">Country/region (required)</span></span>
- <span data-ttu-id="4bb29-370">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="4bb29-371">Cadde (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-371">Street (required)</span></span>
- <span data-ttu-id="4bb29-372">Cadde Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-372">Street Number (required)</span></span>
- <span data-ttu-id="4bb29-373">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="4bb29-373">Building Complement</span></span>
- <span data-ttu-id="4bb29-374">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-374">City (required)</span></span>
- <span data-ttu-id="4bb29-375">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-375">State (required)</span></span>
- <span data-ttu-id="4bb29-376">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="4bb29-377">Amerika Birleşik Devletleri ve Kanada’da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4bb29-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="4bb29-378">Amerika Birleşik Devletleri ve Kanada’daki personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="4bb29-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="4bb29-379">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-379">Departments are required on positions.</span></span>
- <span data-ttu-id="4bb29-380">Maliyet merkezleri mali boyut olarak ayarlanmalı ve varsayılan mali boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="4bb29-381">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="4bb29-381">Job types</span></span>

<span data-ttu-id="4bb29-382">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="4bb29-383">Amerika Birleşik Devletleri ve Kanada'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="4bb29-384">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="4bb29-385">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="4bb29-386">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="4bb29-387">İş türü</span><span class="sxs-lookup"><span data-stu-id="4bb29-387">Job type</span></span>   | <span data-ttu-id="4bb29-388">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bb29-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="4bb29-389">Saatlik</span><span class="sxs-lookup"><span data-stu-id="4bb29-389">Hourly</span></span>     | <span data-ttu-id="4bb29-390">Saatlik</span><span class="sxs-lookup"><span data-stu-id="4bb29-390">Hourly</span></span>      |
| <span data-ttu-id="4bb29-391">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="4bb29-391">Salaried</span></span>   | <span data-ttu-id="4bb29-392">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="4bb29-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="4bb29-393">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="4bb29-393">Position types</span></span> 

<span data-ttu-id="4bb29-394">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="4bb29-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="4bb29-395">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="4bb29-396">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="4bb29-397">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="4bb29-397">Position type</span></span>   | <span data-ttu-id="4bb29-398">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bb29-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="4bb29-399">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="4bb29-399">Full-time</span></span>       | <span data-ttu-id="4bb29-400">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="4bb29-400">Full time employee</span></span> |
| <span data-ttu-id="4bb29-401">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="4bb29-401">Part-time</span></span>       | <span data-ttu-id="4bb29-402">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="4bb29-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="4bb29-403">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="4bb29-403">Reason codes</span></span>

<span data-ttu-id="4bb29-404">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="4bb29-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="4bb29-405">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="4bb29-406">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="4bb29-407">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-407">Reason code</span></span>    | <span data-ttu-id="4bb29-408">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bb29-408">Description</span></span>      | <span data-ttu-id="4bb29-409">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="4bb29-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="4bb29-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="4bb29-410">RESIGNATION</span></span>    | <span data-ttu-id="4bb29-411">İstifa</span><span class="sxs-lookup"><span data-stu-id="4bb29-411">Resignation</span></span>      | <span data-ttu-id="4bb29-412">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-412">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="4bb29-413">TERMINATION</span></span>    | <span data-ttu-id="4bb29-414">Bitiş</span><span class="sxs-lookup"><span data-stu-id="4bb29-414">Termination</span></span>      | <span data-ttu-id="4bb29-415">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-415">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="4bb29-416">RETIREMENT</span></span>     | <span data-ttu-id="4bb29-417">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="4bb29-417">Retirement</span></span>       | <span data-ttu-id="4bb29-418">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-418">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-419">OTHER</span><span class="sxs-lookup"><span data-stu-id="4bb29-419">OTHER</span></span>          | <span data-ttu-id="4bb29-420">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="4bb29-420">Other Reasons</span></span>    | <span data-ttu-id="4bb29-421">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-421">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="4bb29-422">DEATH</span></span>          | <span data-ttu-id="4bb29-423">Ölüm</span><span class="sxs-lookup"><span data-stu-id="4bb29-423">Death</span></span>            | <span data-ttu-id="4bb29-424">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-424">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="4bb29-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="4bb29-426">İzin</span><span class="sxs-lookup"><span data-stu-id="4bb29-426">Leave of Absence</span></span> | <span data-ttu-id="4bb29-427">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-427">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="4bb29-428">CONTRACTEND</span></span>    | <span data-ttu-id="4bb29-429">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="4bb29-429">End of Contract</span></span>  | <span data-ttu-id="4bb29-430">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-430">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="4bb29-431">SALARYCHANGE</span></span>   | <span data-ttu-id="4bb29-432">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="4bb29-432">Change of Salary</span></span> | <span data-ttu-id="4bb29-433">Ücret</span><span class="sxs-lookup"><span data-stu-id="4bb29-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="4bb29-434">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="4bb29-434">Marital status</span></span>

<span data-ttu-id="4bb29-435">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="4bb29-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="4bb29-436">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="4bb29-437">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-437">Talent</span></span>                 | <span data-ttu-id="4bb29-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="4bb29-439">Evli</span><span class="sxs-lookup"><span data-stu-id="4bb29-439">Married</span></span>                | <span data-ttu-id="4bb29-440">Evli</span><span class="sxs-lookup"><span data-stu-id="4bb29-440">Married</span></span>              |
| <span data-ttu-id="4bb29-441">Tekli</span><span class="sxs-lookup"><span data-stu-id="4bb29-441">Single</span></span>                 | <span data-ttu-id="4bb29-442">Tekli</span><span class="sxs-lookup"><span data-stu-id="4bb29-442">Single</span></span>               |
| <span data-ttu-id="4bb29-443">Dul</span><span class="sxs-lookup"><span data-stu-id="4bb29-443">Widowed</span></span>                | <span data-ttu-id="4bb29-444">Dul</span><span class="sxs-lookup"><span data-stu-id="4bb29-444">Widowed</span></span>              |
| <span data-ttu-id="4bb29-445">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="4bb29-445">Divorced</span></span>               | <span data-ttu-id="4bb29-446">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="4bb29-446">Divorced</span></span>             |
| <span data-ttu-id="4bb29-447">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="4bb29-447">Registered Partnership</span></span> | <span data-ttu-id="4bb29-448">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="4bb29-448">Domestic Partnership</span></span> |
| <span data-ttu-id="4bb29-449">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="4bb29-449">None</span></span>                   | <span data-ttu-id="4bb29-450">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="4bb29-450">None</span></span>                 |
| <span data-ttu-id="4bb29-451">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="4bb29-451">Cohabiting</span></span>             | <span data-ttu-id="4bb29-452">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="4bb29-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="4bb29-453">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="4bb29-453">Gender</span></span>

<span data-ttu-id="4bb29-454">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="4bb29-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="4bb29-455">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="4bb29-456">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-456">Talent</span></span>       | <span data-ttu-id="4bb29-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="4bb29-458">Erkek</span><span class="sxs-lookup"><span data-stu-id="4bb29-458">Male</span></span>         | <span data-ttu-id="4bb29-459">Erkek</span><span class="sxs-lookup"><span data-stu-id="4bb29-459">Male</span></span>            |
| <span data-ttu-id="4bb29-460">Kadın</span><span class="sxs-lookup"><span data-stu-id="4bb29-460">Female</span></span>       | <span data-ttu-id="4bb29-461">Kadın</span><span class="sxs-lookup"><span data-stu-id="4bb29-461">Female</span></span>          |
| <span data-ttu-id="4bb29-462">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="4bb29-462">Non-specific</span></span> | <span data-ttu-id="4bb29-463">*Desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="4bb29-464">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="4bb29-464">Earning codes</span></span>

<span data-ttu-id="4bb29-465">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4bb29-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="4bb29-466">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="4bb29-467">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="4bb29-468">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="4bb29-468">Supported frequencies</span></span>

- <span data-ttu-id="4bb29-469">Tümü</span><span class="sxs-lookup"><span data-stu-id="4bb29-469">All</span></span>
- <span data-ttu-id="4bb29-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="4bb29-470">EVERYPAY</span></span>
- <span data-ttu-id="4bb29-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="4bb29-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="4bb29-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="4bb29-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="4bb29-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="4bb29-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="4bb29-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-474">1OFMTH</span></span>
- <span data-ttu-id="4bb29-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-475">LASTOFMTH</span></span>
- <span data-ttu-id="4bb29-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-476">2OFMTH</span></span>
- <span data-ttu-id="4bb29-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-477">3OFMTH</span></span>
- <span data-ttu-id="4bb29-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-478">4OFMTH</span></span>
- <span data-ttu-id="4bb29-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-479">5OFMTH</span></span>
- <span data-ttu-id="4bb29-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-480">1N2OFMTH</span></span>
- <span data-ttu-id="4bb29-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-481">3N4OFMTH</span></span>
- <span data-ttu-id="4bb29-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-482">1N3OFMTH</span></span>
- <span data-ttu-id="4bb29-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-483">1N4OFMTH</span></span>
- <span data-ttu-id="4bb29-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-484">2N3OFMTH</span></span>
- <span data-ttu-id="4bb29-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-485">2N4OFMTH</span></span>
- <span data-ttu-id="4bb29-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="4bb29-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="4bb29-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="4bb29-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="4bb29-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="4bb29-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="4bb29-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="4bb29-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="4bb29-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="4bb29-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="4bb29-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="4bb29-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="4bb29-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="4bb29-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="4bb29-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="4bb29-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="4bb29-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="4bb29-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="4bb29-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="4bb29-498">Adresler</span><span class="sxs-lookup"><span data-stu-id="4bb29-498">Addresses</span></span>

<span data-ttu-id="4bb29-499">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="4bb29-500">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="4bb29-501">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-501">Talent</span></span>          | <span data-ttu-id="4bb29-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="4bb29-503">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="4bb29-503">Country/Region</span></span>  | <span data-ttu-id="4bb29-504">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-504">Country Code</span></span>          |
| <span data-ttu-id="4bb29-505">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-505">Zip/Postal Code</span></span> | <span data-ttu-id="4bb29-506">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-506">Postal Code</span></span>           |
| <span data-ttu-id="4bb29-507">İl</span><span class="sxs-lookup"><span data-stu-id="4bb29-507">State</span></span>           | <span data-ttu-id="4bb29-508">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-508">State Code</span></span>            |
| <span data-ttu-id="4bb29-509">Şehir</span><span class="sxs-lookup"><span data-stu-id="4bb29-509">City</span></span>            | <span data-ttu-id="4bb29-510">Şehir</span><span class="sxs-lookup"><span data-stu-id="4bb29-510">City</span></span>                  |
| <span data-ttu-id="4bb29-511">İlçe</span><span class="sxs-lookup"><span data-stu-id="4bb29-511">County</span></span>          | <span data-ttu-id="4bb29-512">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="4bb29-512">County (Municipality)</span></span> |
| <span data-ttu-id="4bb29-513">Sokak</span><span class="sxs-lookup"><span data-stu-id="4bb29-513">Street</span></span>          | <span data-ttu-id="4bb29-514">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="4bb29-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="4bb29-515">Vergi bölgeleri</span><span class="sxs-lookup"><span data-stu-id="4bb29-515">Tax regions</span></span>

<span data-ttu-id="4bb29-516">Vergi bölgeleri, bordro oluşturma sırasında uygulanması gereken uygun vergiyi belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="4bb29-517">Vergi bölgeleri, Dayforce'a konum adresleri olarak eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="4bb29-518">Varsayılan vergi bölgesi, çalışanın etkin konumuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="4bb29-519">Vergi bölgesi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-519">Tax region (required)</span></span>
- <span data-ttu-id="4bb29-520">Ülke/Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-520">Country/Region (required)</span></span>
- <span data-ttu-id="4bb29-521">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-521">State (required)</span></span>
- <span data-ttu-id="4bb29-522">İlçe</span><span class="sxs-lookup"><span data-stu-id="4bb29-522">County</span></span> 
- <span data-ttu-id="4bb29-523">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="4bb29-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="4bb29-524">Meksika'da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4bb29-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="4bb29-525">Meksika'da personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="4bb29-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="4bb29-526">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-526">Departments are required on positions.</span></span>
- <span data-ttu-id="4bb29-527">Maliyet merkezleri mali boyut olarak ayarlanmalı ve Varsayılan Mali Boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="4bb29-528">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="4bb29-528">Job types</span></span>

<span data-ttu-id="4bb29-529">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="4bb29-530">Meksika'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="4bb29-531">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="4bb29-532">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="4bb29-533">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="4bb29-534">İş türü</span><span class="sxs-lookup"><span data-stu-id="4bb29-534">Job type</span></span>   | <span data-ttu-id="4bb29-535">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bb29-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="4bb29-536">Saatlik</span><span class="sxs-lookup"><span data-stu-id="4bb29-536">Hourly</span></span>     | <span data-ttu-id="4bb29-537">MX Saatlik</span><span class="sxs-lookup"><span data-stu-id="4bb29-537">MX Hourly</span></span>   |
| <span data-ttu-id="4bb29-538">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="4bb29-538">Salaried</span></span>   | <span data-ttu-id="4bb29-539">MX Maaşlı</span><span class="sxs-lookup"><span data-stu-id="4bb29-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="4bb29-540">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="4bb29-540">Position types</span></span> 

<span data-ttu-id="4bb29-541">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="4bb29-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="4bb29-542">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="4bb29-543">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="4bb29-544">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="4bb29-544">Position type</span></span>   | <span data-ttu-id="4bb29-545">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bb29-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="4bb29-546">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="4bb29-546">Full-time</span></span>       | <span data-ttu-id="4bb29-547">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="4bb29-547">Full time employee</span></span> |
| <span data-ttu-id="4bb29-548">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="4bb29-548">Part-time</span></span>       | <span data-ttu-id="4bb29-549">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="4bb29-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="4bb29-550">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="4bb29-550">Reason codes</span></span>

<span data-ttu-id="4bb29-551">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="4bb29-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="4bb29-552">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="4bb29-553">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="4bb29-554">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-554">Reason code</span></span>            | <span data-ttu-id="4bb29-555">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bb29-555">Description</span></span>                    | <span data-ttu-id="4bb29-556">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="4bb29-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="4bb29-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="4bb29-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="4bb29-558">İlk bordrodan önce ayrılma</span><span class="sxs-lookup"><span data-stu-id="4bb29-558">Departure before first payroll</span></span> | <span data-ttu-id="4bb29-559">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-559">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="4bb29-560">RESIGNATION</span></span>            | <span data-ttu-id="4bb29-561">İstifa</span><span class="sxs-lookup"><span data-stu-id="4bb29-561">Resignation</span></span>                    | <span data-ttu-id="4bb29-562">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-562">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="4bb29-563">PENSION</span></span>                | <span data-ttu-id="4bb29-564">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="4bb29-564">Pension</span></span>                        | <span data-ttu-id="4bb29-565">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-565">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="4bb29-566">TERMINATION</span></span>            | <span data-ttu-id="4bb29-567">Bitiş</span><span class="sxs-lookup"><span data-stu-id="4bb29-567">Termination</span></span>                    | <span data-ttu-id="4bb29-568">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-568">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="4bb29-569">RETIREMENT</span></span>             | <span data-ttu-id="4bb29-570">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="4bb29-570">Retirement</span></span>                     | <span data-ttu-id="4bb29-571">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-571">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="4bb29-572">ABSENTEE</span></span>               | <span data-ttu-id="4bb29-573">Devamsızlık</span><span class="sxs-lookup"><span data-stu-id="4bb29-573">Absentee</span></span>                       | <span data-ttu-id="4bb29-574">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-574">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-575">OTHER</span><span class="sxs-lookup"><span data-stu-id="4bb29-575">OTHER</span></span>                  | <span data-ttu-id="4bb29-576">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="4bb29-576">Other Reasons</span></span>                  | <span data-ttu-id="4bb29-577">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-577">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="4bb29-578">CLOSURE</span></span>                | <span data-ttu-id="4bb29-579">İşletmenin Kapanması</span><span class="sxs-lookup"><span data-stu-id="4bb29-579">Business Closure</span></span>               | <span data-ttu-id="4bb29-580">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-580">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="4bb29-581">DEATH</span></span>                  | <span data-ttu-id="4bb29-582">Ölüm</span><span class="sxs-lookup"><span data-stu-id="4bb29-582">Death</span></span>                          | <span data-ttu-id="4bb29-583">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-583">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="4bb29-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="4bb29-585">İzin</span><span class="sxs-lookup"><span data-stu-id="4bb29-585">Leave of Absence</span></span>               | <span data-ttu-id="4bb29-586">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-586">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="4bb29-587">CONTRACTEND</span></span>            | <span data-ttu-id="4bb29-588">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="4bb29-588">End of Contract</span></span>                | <span data-ttu-id="4bb29-589">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="4bb29-589">Terminate worker</span></span>     |
| <span data-ttu-id="4bb29-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="4bb29-590">SALARYCHANGE</span></span>           | <span data-ttu-id="4bb29-591">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="4bb29-591">Change of Salary</span></span>               | <span data-ttu-id="4bb29-592">Ücret</span><span class="sxs-lookup"><span data-stu-id="4bb29-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="4bb29-593">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="4bb29-593">Terms of employment</span></span>

<span data-ttu-id="4bb29-594">İstihdam koşulları, istihdam koşullarının kategorilerini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="4bb29-595">Koşullar, istihdam göstergesi değerleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="4bb29-596">Aşağıdaki istihdam koşulları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="4bb29-597">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="4bb29-597">Terms of employment</span></span>   | <span data-ttu-id="4bb29-598">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bb29-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="4bb29-599">Normal</span><span class="sxs-lookup"><span data-stu-id="4bb29-599">Regular</span></span>               | <span data-ttu-id="4bb29-600">Normal</span><span class="sxs-lookup"><span data-stu-id="4bb29-600">Regular</span></span>     |
| <span data-ttu-id="4bb29-601">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="4bb29-601">Direct</span></span>                | <span data-ttu-id="4bb29-602">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="4bb29-602">Direct</span></span>      |
| <span data-ttu-id="4bb29-603">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="4bb29-603">Internship</span></span>            | <span data-ttu-id="4bb29-604">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="4bb29-604">Internship</span></span>  |
| <span data-ttu-id="4bb29-605">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="4bb29-605">Permanent</span></span>             | <span data-ttu-id="4bb29-606">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="4bb29-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="4bb29-607">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="4bb29-607">Marital status</span></span>

<span data-ttu-id="4bb29-608">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="4bb29-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="4bb29-609">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="4bb29-610">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-610">Talent</span></span>                 | <span data-ttu-id="4bb29-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="4bb29-612">Evli</span><span class="sxs-lookup"><span data-stu-id="4bb29-612">Married</span></span>                | <span data-ttu-id="4bb29-613">Evli</span><span class="sxs-lookup"><span data-stu-id="4bb29-613">Married</span></span>                   |
| <span data-ttu-id="4bb29-614">Tekli</span><span class="sxs-lookup"><span data-stu-id="4bb29-614">Single</span></span>                 | <span data-ttu-id="4bb29-615">Tekli</span><span class="sxs-lookup"><span data-stu-id="4bb29-615">Single</span></span>                    |
| <span data-ttu-id="4bb29-616">Dul</span><span class="sxs-lookup"><span data-stu-id="4bb29-616">Widowed</span></span>                | <span data-ttu-id="4bb29-617">Dul</span><span class="sxs-lookup"><span data-stu-id="4bb29-617">Widowed</span></span>                   |
| <span data-ttu-id="4bb29-618">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="4bb29-618">Divorced</span></span>               | <span data-ttu-id="4bb29-619">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="4bb29-619">Divorced</span></span>                  |
| <span data-ttu-id="4bb29-620">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="4bb29-620">Registered Partnership</span></span> | <span data-ttu-id="4bb29-621">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="4bb29-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="4bb29-622">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="4bb29-622">None</span></span>                   | <span data-ttu-id="4bb29-623">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="4bb29-624">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="4bb29-624">Cohabiting</span></span>             | <span data-ttu-id="4bb29-625">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="4bb29-626">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="4bb29-626">Gender</span></span>

<span data-ttu-id="4bb29-627">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="4bb29-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="4bb29-628">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="4bb29-629">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-629">Talent</span></span>       | <span data-ttu-id="4bb29-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="4bb29-631">Erkek</span><span class="sxs-lookup"><span data-stu-id="4bb29-631">Male</span></span>         | <span data-ttu-id="4bb29-632">Erkek</span><span class="sxs-lookup"><span data-stu-id="4bb29-632">Male</span></span>                      |
| <span data-ttu-id="4bb29-633">Kadın</span><span class="sxs-lookup"><span data-stu-id="4bb29-633">Female</span></span>       | <span data-ttu-id="4bb29-634">Kadın</span><span class="sxs-lookup"><span data-stu-id="4bb29-634">Female</span></span>                    |
| <span data-ttu-id="4bb29-635">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="4bb29-635">Non-specific</span></span> | <span data-ttu-id="4bb29-636">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="4bb29-637">Ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="4bb29-637">Payment method</span></span>

<span data-ttu-id="4bb29-638">Ödeme yöntemleri, personele ve şirkete çalışanlara nasıl ödeme yapılacağını tanımlamak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="4bb29-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="4bb29-639">Ödeme yöntemleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="4bb29-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="4bb29-640">Aşağıdaki tabloda ödeme yöntemlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="4bb29-641">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-641">Talent</span></span>             | <span data-ttu-id="4bb29-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="4bb29-643">Nakit</span><span class="sxs-lookup"><span data-stu-id="4bb29-643">Cash</span></span>               | <span data-ttu-id="4bb29-644">Nakit</span><span class="sxs-lookup"><span data-stu-id="4bb29-644">Cash</span></span>                      |
| <span data-ttu-id="4bb29-645">Elektronik Ödeme</span><span class="sxs-lookup"><span data-stu-id="4bb29-645">Electronic Payment</span></span> | <span data-ttu-id="4bb29-646">Transfer et</span><span class="sxs-lookup"><span data-stu-id="4bb29-646">Transfer</span></span>                  |
| <span data-ttu-id="4bb29-647">Denetle</span><span class="sxs-lookup"><span data-stu-id="4bb29-647">Check</span></span>              | <span data-ttu-id="4bb29-648">Çek</span><span class="sxs-lookup"><span data-stu-id="4bb29-648">Cheque</span></span>                    |
| <span data-ttu-id="4bb29-649">Banka Ödeme Emri</span><span class="sxs-lookup"><span data-stu-id="4bb29-649">Bank Draft</span></span>         | <span data-ttu-id="4bb29-650">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="4bb29-651">Diğer</span><span class="sxs-lookup"><span data-stu-id="4bb29-651">Other</span></span>              | <span data-ttu-id="4bb29-652">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="4bb29-653">Banka hesabı türü</span><span class="sxs-lookup"><span data-stu-id="4bb29-653">Bank account type</span></span>

<span data-ttu-id="4bb29-654">Banka hesap türleri, personele elektronik ödeme yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="4bb29-655">Banka hesap türleri, transfer hesabı bilgileri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="4bb29-656">Banka hesap türleri, uygunsa tümleştirme işleminden sonra kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="4bb29-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="4bb29-657">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-657">Talent</span></span>            | <span data-ttu-id="4bb29-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="4bb29-659">Cari Hesap</span><span class="sxs-lookup"><span data-stu-id="4bb29-659">Checking Account</span></span>  | <span data-ttu-id="4bb29-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="4bb29-660">CheckingAccount</span></span>           |
| <span data-ttu-id="4bb29-661">Bordro Hesabı</span><span class="sxs-lookup"><span data-stu-id="4bb29-661">Payroll Account</span></span>   | <span data-ttu-id="4bb29-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="4bb29-662">PayrollAccount</span></span>            |
| <span data-ttu-id="4bb29-663">Tasarruf Hesabı</span><span class="sxs-lookup"><span data-stu-id="4bb29-663">Savings Account</span></span>   | <span data-ttu-id="4bb29-664">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="4bb29-665">BankGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="4bb29-665">BankGirot account</span></span> | <span data-ttu-id="4bb29-666">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="4bb29-667">PlusGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="4bb29-667">PlusGirot account</span></span> | <span data-ttu-id="4bb29-668">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="4bb29-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="4bb29-669">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="4bb29-669">Earning codes</span></span>

<span data-ttu-id="4bb29-670">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4bb29-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="4bb29-671">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="4bb29-672">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4bb29-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="4bb29-673">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="4bb29-673">Supported frequencies</span></span>

- <span data-ttu-id="4bb29-674">Tümü</span><span class="sxs-lookup"><span data-stu-id="4bb29-674">All</span></span>
- <span data-ttu-id="4bb29-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="4bb29-675">EVERYPAY</span></span>
- <span data-ttu-id="4bb29-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="4bb29-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="4bb29-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="4bb29-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="4bb29-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="4bb29-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="4bb29-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-679">1OFMTH</span></span>
- <span data-ttu-id="4bb29-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-680">LASTOFMTH</span></span>
- <span data-ttu-id="4bb29-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-681">2OFMTH</span></span>
- <span data-ttu-id="4bb29-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-682">3OFMTH</span></span>
- <span data-ttu-id="4bb29-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-683">4OFMTH</span></span>
- <span data-ttu-id="4bb29-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-684">5OFMTH</span></span>
- <span data-ttu-id="4bb29-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-685">1N2OFMTH</span></span>
- <span data-ttu-id="4bb29-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-686">3N4OFMTH</span></span>
- <span data-ttu-id="4bb29-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-687">1N3OFMTH</span></span>
- <span data-ttu-id="4bb29-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-688">1N4OFMTH</span></span>
- <span data-ttu-id="4bb29-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-689">2N3OFMTH</span></span>
- <span data-ttu-id="4bb29-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-690">2N4OFMTH</span></span>
- <span data-ttu-id="4bb29-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="4bb29-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="4bb29-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="4bb29-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="4bb29-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="4bb29-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="4bb29-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="4bb29-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="4bb29-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="4bb29-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="4bb29-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="4bb29-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="4bb29-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="4bb29-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="4bb29-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="4bb29-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="4bb29-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="4bb29-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="4bb29-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="4bb29-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="4bb29-703">Adresler</span><span class="sxs-lookup"><span data-stu-id="4bb29-703">Addresses</span></span>

<span data-ttu-id="4bb29-704">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="4bb29-705">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="4bb29-706">Talent</span><span class="sxs-lookup"><span data-stu-id="4bb29-706">Talent</span></span>              | <span data-ttu-id="4bb29-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="4bb29-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="4bb29-708">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="4bb29-708">Country/Region</span></span>      | <span data-ttu-id="4bb29-709">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-709">Country Code</span></span>          |
| <span data-ttu-id="4bb29-710">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-710">Zip/Postal Code</span></span>     | <span data-ttu-id="4bb29-711">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-711">Postal Code</span></span>           |
| <span data-ttu-id="4bb29-712">İl</span><span class="sxs-lookup"><span data-stu-id="4bb29-712">State</span></span>               | <span data-ttu-id="4bb29-713">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="4bb29-713">State Code</span></span>            |
| <span data-ttu-id="4bb29-714">Şehir</span><span class="sxs-lookup"><span data-stu-id="4bb29-714">City</span></span>                | <span data-ttu-id="4bb29-715">Şehir</span><span class="sxs-lookup"><span data-stu-id="4bb29-715">City</span></span>                  |
| <span data-ttu-id="4bb29-716">İlçe</span><span class="sxs-lookup"><span data-stu-id="4bb29-716">County</span></span>              | <span data-ttu-id="4bb29-717">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="4bb29-717">County (Municipality)</span></span> |
| <span data-ttu-id="4bb29-718">Sokak</span><span class="sxs-lookup"><span data-stu-id="4bb29-718">Street</span></span>              | <span data-ttu-id="4bb29-719">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="4bb29-719">Address Line 1</span></span>        |
| <span data-ttu-id="4bb29-720">Cadde Numarası</span><span class="sxs-lookup"><span data-stu-id="4bb29-720">Street Number</span></span>       | <span data-ttu-id="4bb29-721">Adres Satırı 2</span><span class="sxs-lookup"><span data-stu-id="4bb29-721">Address Line 2</span></span>        |
| <span data-ttu-id="4bb29-722">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="4bb29-722">Building Complement</span></span> | <span data-ttu-id="4bb29-723">Adres Satırı 5</span><span class="sxs-lookup"><span data-stu-id="4bb29-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="4bb29-724">Pasaport numarası</span><span class="sxs-lookup"><span data-stu-id="4bb29-724">Passport number</span></span>

<span data-ttu-id="4bb29-725">Personel pasaport bilgilerini bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-725">Employees can declare passport information.</span></span> <span data-ttu-id="4bb29-726">Bu bilgiler, **Pasaport** kimlik türünü içerir ve Meksika'ya özel personel bilgilerinin bir parçası olarak Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="4bb29-727">Kimlik Türü = "Pasaport"</span><span class="sxs-lookup"><span data-stu-id="4bb29-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="4bb29-728">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="4bb29-728">Issued Date</span></span>
- <span data-ttu-id="4bb29-729">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="4bb29-729">Expiration Date</span></span>

<span data-ttu-id="4bb29-730">Personel, **Pasaport** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="4bb29-731">Ancak yalnızca geçerli etkin pasaport girişi Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="4bb29-732">Tüm pasaport girişlerinin süresi dolmuşsa en son verilen pasaport Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4bb29-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>


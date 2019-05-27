---
title: Talent ile Dayforce arasında bordro tümleştirmesini yapılandırma
description: Bu konuda, bir ödeme işlemini işlemek üzere Microsoft Dynamics 365 for Talent ile Ceridian Dayforce arasındaki tümleştirmeyi nasıl yapılandıracağınız açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519266"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="1db32-103">Talent ve Dayforce arasında bordro tümleştirmeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1db32-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1db32-104">Microsoft Dynamics 365 for Talent ile Ceridian Dayforce arasındaki tümleştirme, bu konuda açıklanan çeşitli yapılandırma adımlarına dayanır.</span><span class="sxs-lookup"><span data-stu-id="1db32-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="1db32-105">Ödeme işlemini işlemeden önce tümleştirmeyi hem Talent hem de Dayforce'ta yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="1db32-106">Ödeme işlemlerini tamamlamak için Dayforce gibi bir hizmet kullandığınızda tümleştirmeyi Talent'ta etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="1db32-107">Tümleştirme için Talent'tan özel veriler gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="1db32-108">Bu nedenle, Dayforce ile eşlenmiş verilerin Talent'ta tümleştirmeyi destekleyecek şekilde yapılandırıldığını doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="1db32-109">Tümleştirme, aşağıdaki geniş veri kategorilerini kullanır:</span><span class="sxs-lookup"><span data-stu-id="1db32-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="1db32-110">İnsan kaynakları verileri</span><span class="sxs-lookup"><span data-stu-id="1db32-110">Human resources data</span></span>
- <span data-ttu-id="1db32-111">Ücret verileri</span><span class="sxs-lookup"><span data-stu-id="1db32-111">Compensation data</span></span>
- <span data-ttu-id="1db32-112">Ödeme döngüleri, ödeme dönemleri ve kazanç kodları gibi bordro verileri</span><span class="sxs-lookup"><span data-stu-id="1db32-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="1db32-113">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="1db32-113">Worker data</span></span>

<span data-ttu-id="1db32-114">Bu konuda, tümleştirmeyi etkinleştirmek için izlemeniz gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1db32-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="1db32-115">Ayrıca veri türleri ve tümleştirmenin gerektirdiği yapılandırma ayrıntıları da açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1db32-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="1db32-116">Tümleştirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1db32-116">Enable the integration</span></span>

<span data-ttu-id="1db32-117">Talent'ta yapılandırmayı açmanız ve Dayforce'a bağlanmak için yapılandırma bilgilerini girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="1db32-118">Microsoft Dynamics 365 for Finance and Operations'a aktarılmak üzere oluşturulan genel muhasebe hareketini istiyorsanız ayrıca bir Microsoft Azure depolama hesabı oluşturmanız ve Finance and Operations'ta Azure Depolama bağlantı dizesini de girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="1db32-119">Talent'ta tümleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1db32-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="1db32-120">**Sistem yönetimi** sayfasında **Tümleştirme yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1db32-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="1db32-121">Güvenli Dosya Aktarım Protokolü (FTP) uç noktasını ve güvenli FTP klasörü yolunu girin.</span><span class="sxs-lookup"><span data-stu-id="1db32-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="1db32-122">Güvenli FTP uç noktasına ve klasör yoluna erişecek kullanıcının kullanıcı adını ve parolasını girin.</span><span class="sxs-lookup"><span data-stu-id="1db32-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="1db32-123">Bağlantıyı gerektiği gibi test edin ve **Bordro tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1db32-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="1db32-124">Tümleştirme açıldığında veri dışa aktarma paketi ve dosyalar oluşturulur ve sıklık ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1db32-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="1db32-125">Bu sıklığı ihtiyaç duyduğunuz şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1db32-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="1db32-126">Azure depolama hesapları ve Azure Depolama bağlantı dizeleri hakkında daha fazla bilgi için aşağıdaki Azure konularına bakın:</span><span class="sxs-lookup"><span data-stu-id="1db32-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="1db32-127">Azure depolama hesapları hakkında</span><span class="sxs-lookup"><span data-stu-id="1db32-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="1db32-128">Azure Depolama bağlantı dizelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1db32-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="1db32-129">Verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1db32-129">Configure your data</span></span> 

<span data-ttu-id="1db32-130">Bordro işlemek için Talent'ta insan kaynağı verilerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="1db32-131">Kazanç ve ücret bilgileriyle birlikte işler ve pozisyonlar gibi kurumsal verileri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="1db32-132">Bu bilgiler personel ödemesi oluşturmak için gerekli olan istihdam, ödeme ve kesinti bilgilerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="1db32-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="1db32-133">İnsan kaynağı verileri</span><span class="sxs-lookup"><span data-stu-id="1db32-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="1db32-134">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="1db32-134">Benefits</span></span> 

<span data-ttu-id="1db32-135">İnsan kaynakları, bir kuruluşun çalışanları için sunduğu veya işlediği kazançları, kesintileri ve çalışan ücret planlarını ayarlamak ve bunları yönetmek için kullanılan araçları sağlar.</span><span class="sxs-lookup"><span data-stu-id="1db32-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="1db32-136">Kazançları oluştururken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="1db32-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="1db32-137">Kazanç planları</span><span class="sxs-lookup"><span data-stu-id="1db32-137">Benefit plans</span></span>

- <span data-ttu-id="1db32-138">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-138">Plan (required)</span></span>
- <span data-ttu-id="1db32-139">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-139">Type (required)</span></span>
- <span data-ttu-id="1db32-140">Bordro etkisi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-140">Payroll impact (required)</span></span>
- <span data-ttu-id="1db32-141">Borçları kurtar</span><span class="sxs-lookup"><span data-stu-id="1db32-141">Recover arrears</span></span>
- <span data-ttu-id="1db32-142">Kesinti yöntemi</span><span class="sxs-lookup"><span data-stu-id="1db32-142">Deduction method</span></span>
- <span data-ttu-id="1db32-143">Kesinti önceliği</span><span class="sxs-lookup"><span data-stu-id="1db32-143">Deduction priority</span></span>
- <span data-ttu-id="1db32-144">Dönemi sınırla</span><span class="sxs-lookup"><span data-stu-id="1db32-144">Limit period</span></span>
- <span data-ttu-id="1db32-145">Sınır tutar</span><span class="sxs-lookup"><span data-stu-id="1db32-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="1db32-146">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="1db32-146">Benefits</span></span>

- <span data-ttu-id="1db32-147">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-147">Plan (required)</span></span>
- <span data-ttu-id="1db32-148">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-148">Type (required)</span></span>
- <span data-ttu-id="1db32-149">Seçenek (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-149">Option (required)</span></span>
- <span data-ttu-id="1db32-150">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-150">Benefit ID (required)</span></span>
- <span data-ttu-id="1db32-151">Sıklık</span><span class="sxs-lookup"><span data-stu-id="1db32-151">Frequency</span></span>
- <span data-ttu-id="1db32-152">Temel</span><span class="sxs-lookup"><span data-stu-id="1db32-152">Basis</span></span>
- <span data-ttu-id="1db32-153">Tutar veya oran</span><span class="sxs-lookup"><span data-stu-id="1db32-153">Amount or rate</span></span>
- <span data-ttu-id="1db32-154">Kazanç kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="1db32-155">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="1db32-155">Supported frequencies</span></span> 

- <span data-ttu-id="1db32-156">Haftalık</span><span class="sxs-lookup"><span data-stu-id="1db32-156">Weekly</span></span>
- <span data-ttu-id="1db32-157">İki haftada bir</span><span class="sxs-lookup"><span data-stu-id="1db32-157">Bi-weekly</span></span>
- <span data-ttu-id="1db32-158">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="1db32-158">Semi-monthly</span></span>
- <span data-ttu-id="1db32-159">Aylık</span><span class="sxs-lookup"><span data-stu-id="1db32-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="1db32-160">Desteklenen tabanlar</span><span class="sxs-lookup"><span data-stu-id="1db32-160">Supported bases</span></span> 

- <span data-ttu-id="1db32-161">Sabit tutar</span><span class="sxs-lookup"><span data-stu-id="1db32-161">Fixed amount</span></span>
- <span data-ttu-id="1db32-162">Kazançların yüzdesi</span><span class="sxs-lookup"><span data-stu-id="1db32-162">Percent of earnings</span></span>
- <span data-ttu-id="1db32-163">Üretime yönelik saatler</span><span class="sxs-lookup"><span data-stu-id="1db32-163">Productive hours</span></span>

<span data-ttu-id="1db32-164">Dayforce, kazanç planında tanımlanan bordro etkisine göre aşağıdaki kesintileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1db32-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="1db32-165">Talent'ta seçim</span><span class="sxs-lookup"><span data-stu-id="1db32-165">Selection in Talent</span></span>        | <span data-ttu-id="1db32-166">Dayforce'ta sonuç</span><span class="sxs-lookup"><span data-stu-id="1db32-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="1db32-167">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="1db32-167">None</span></span>                       | <span data-ttu-id="1db32-168">Kesinti oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="1db32-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="1db32-169">Yalnızca kesinti</span><span class="sxs-lookup"><span data-stu-id="1db32-169">Deduction only</span></span>             | <span data-ttu-id="1db32-170">Personel kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1db32-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="1db32-171">Yalnızca katkı</span><span class="sxs-lookup"><span data-stu-id="1db32-171">Contribution only</span></span>          | <span data-ttu-id="1db32-172">İşveren kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1db32-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="1db32-173">Kesinti ve katkı</span><span class="sxs-lookup"><span data-stu-id="1db32-173">Deduction and contribution</span></span> | <span data-ttu-id="1db32-174">Personel ve işveren kesintileri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1db32-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="1db32-175">Kazanç programı tanımlama ve yönetme hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="1db32-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="1db32-176">Personel kazançları programı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1db32-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="1db32-177">Yeni kazanç oluşturma</span><span class="sxs-lookup"><span data-stu-id="1db32-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="1db32-178">Kazanç uygunluk kurallarını ve ilkelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="1db32-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="1db32-179">Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma</span><span class="sxs-lookup"><span data-stu-id="1db32-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="1db32-180">Ücret</span><span class="sxs-lookup"><span data-stu-id="1db32-180">Compensation</span></span> 

<span data-ttu-id="1db32-181">Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="1db32-182">Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="1db32-183">İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="1db32-184">Dayforce personelin saatlik veya yıllık ücretlerini hesaplamak için ücret bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1db32-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="1db32-185">Sabit ücret planları ve ödeme oranı dönüştürmeleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="1db32-186">Personelin bir sabit ücret planıyla ilişkilendirilmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="1db32-187">Ücret planları hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="1db32-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="1db32-188">Sabit ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="1db32-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="1db32-189">Değişken ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="1db32-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="1db32-190">Maaş/ücret yapısı ve planları geliştirme</span><span class="sxs-lookup"><span data-stu-id="1db32-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="1db32-191">İşlem ücreti</span><span class="sxs-lookup"><span data-stu-id="1db32-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="1db32-192">Ücret işlemini tanımlama ve sonuçları hesaplama</span><span class="sxs-lookup"><span data-stu-id="1db32-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="1db32-193">Personeli sabit ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="1db32-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="1db32-194">Personeli değişken ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="1db32-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="1db32-195">İşler</span><span class="sxs-lookup"><span data-stu-id="1db32-195">Jobs</span></span> 

<span data-ttu-id="1db32-196">Bir iş, işi gerçekleştiren kişiden beklenen görev ve sorumlulukların toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="1db32-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="1db32-197">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="1db32-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="1db32-198">İşin bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1db32-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="1db32-199">Yeni işler tanımlama</span><span class="sxs-lookup"><span data-stu-id="1db32-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="1db32-200">Pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="1db32-200">Positions</span></span>

<span data-ttu-id="1db32-201">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="1db32-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="1db32-202">Örneğin, "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş pozisyonlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="1db32-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="1db32-203">Bir pozisyon, bir departmanda bulunur.</span><span class="sxs-lookup"><span data-stu-id="1db32-203">A position exists in a department.</span></span> <span data-ttu-id="1db32-204">Her pozisyonla yalnızca bir çalışan ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="1db32-205">Pozisyonları ayarlarken aşağıdaki verileri ve yapılandırmayı göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="1db32-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="1db32-206">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-206">Position (required)</span></span>
- <span data-ttu-id="1db32-207">Açıklama (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-207">Description (required)</span></span>
- <span data-ttu-id="1db32-208">İş (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-208">Job (required)</span></span>
- <span data-ttu-id="1db32-209">Departman (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-209">Department (required)</span></span>
- <span data-ttu-id="1db32-210">Pozisyon türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-210">Position type (required)</span></span>
- <span data-ttu-id="1db32-211">Tam zamanlı eşdeğeri</span><span class="sxs-lookup"><span data-stu-id="1db32-211">Full-time equivalent</span></span>
- <span data-ttu-id="1db32-212">Yıllık mesai saatleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="1db32-213">Tüzel kişilik tarafından ödenen (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="1db32-214">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-214">Pay cycle (required)</span></span>
- <span data-ttu-id="1db32-215">Varsayılan mali boyut – Maliyet merkezi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="1db32-216">Çalışan ataması: Çalışan, atama başlangıç tarihi, atama bitiş tarihi, neden kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="1db32-217">Aynı departmanda birden fazla pozisyon aynı işle ilişkilendirilmişse bunlar Dayforce'ta tek bir pozisyonda konsolide edilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="1db32-218">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="1db32-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="1db32-219">Departmanlar, işler ve pozisyonları kullanarak iş gücünüzü düzenleme</span><span class="sxs-lookup"><span data-stu-id="1db32-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="1db32-220">Pozisyonları ayarlama</span><span class="sxs-lookup"><span data-stu-id="1db32-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="1db32-221">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="1db32-221">Departments</span></span>

<span data-ttu-id="1db32-222">Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir.</span><span class="sxs-lookup"><span data-stu-id="1db32-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="1db32-223">Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur.</span><span class="sxs-lookup"><span data-stu-id="1db32-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="1db32-224">İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1db32-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="1db32-225">Departmanların kâr ve zarar sorumluluğu olabilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="1db32-226">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="1db32-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="1db32-227">Departman oluşturma ve departman hiyerarşisi ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="1db32-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="1db32-228">Yeni departmanlar tanımlama</span><span class="sxs-lookup"><span data-stu-id="1db32-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="1db32-229">Ödeme döngüleri ve ödeme dönemleri</span><span class="sxs-lookup"><span data-stu-id="1db32-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="1db32-230">Ödeme döngüsü, bordronun ne sıklıkta çalıştırıldığını ve çalışanlara ödeme yapılan belirli günleri belirler.</span><span class="sxs-lookup"><span data-stu-id="1db32-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="1db32-231">Örneğin, bir ödeme döngüsü aylık olabilir ve personele ayın son günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="1db32-232">Alternatif olarak, bir ödeme döngüsü haftalık olabilir ve personele ödeme döneminin bitişinden sonraki Salı günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="1db32-233">Ödeme döngüleri, bu pozisyonlardaki çalışanlara ne zaman ödeme yapıldığını kontrol etmek için pozisyonlara atanır.</span><span class="sxs-lookup"><span data-stu-id="1db32-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="1db32-234">Ödeme döngülerini oluşturduktan sonra her döngü için ödeme dönemleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1db32-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="1db32-235">Her ödeme dönemi, sağladığınız bilgilere göre varsayılan bir ödeme tarihi içerir.</span><span class="sxs-lookup"><span data-stu-id="1db32-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="1db32-236">Ancak ödeme döneminin bir tatil gününe denk gelmesi gibi istisnalara izin vermek için ödeme döneminde varsayılan ödeme tarihini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1db32-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="1db32-237">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="1db32-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="1db32-238">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-238">Pay cycle (required)</span></span>
- <span data-ttu-id="1db32-239">Ödeme döngüsü sıklığı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="1db32-240">Dönem başlangıç tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="1db32-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="1db32-241">Varsayılan ödeme tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="1db32-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="1db32-242">Bu bilgiler ödeme grupları olarak Dayforce ile tümleştirilir ve her ödeme döngüsü için ülke veya bölgeye göre ayrılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="1db32-243">Tümleştirmeden önce en az bir ödeme dönemi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1db32-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="1db32-244">Dayforce, ilk ödeme döneminin başlangıç tarihine ve Talent'ta ayarlanan varsayılan ödeme tarihine bağlı olarak ödeme grubu takvimlerini ve ödeme tarihlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1db32-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="1db32-245">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="1db32-245">Earning codes</span></span>

<span data-ttu-id="1db32-246">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1db32-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1db32-247">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametrelere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="1db32-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="1db32-248">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="1db32-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="1db32-249">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-249">Earning Code (required)</span></span>
- <span data-ttu-id="1db32-250">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db32-250">Description</span></span>
- <span data-ttu-id="1db32-251">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="1db32-251">Unit of measure</span></span>
- <span data-ttu-id="1db32-252">Üretken</span><span class="sxs-lookup"><span data-stu-id="1db32-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="1db32-253">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="1db32-253">Worker data</span></span>

<span data-ttu-id="1db32-254">Sahip olduğunuz çeşitli çalışan türlerine ilişkin kayıtlar, insan kaynaklarınız ve bordro sistemleriniz için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="1db32-255">Girdiğiniz bilgiler çalışanları ve kişisel bilgileri izlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="1db32-256">Çalışanlar hakkında aşağıdaki bilgileri koruyabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="1db32-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="1db32-257">**Temel**: İletişim bilgileri, demografik bilgiler, kimlik bilgileri, aile bilgileri, askerlik hizmeti durumu, göçmenlik bilgileri ile kişisel ve acil durum iletişim kişileri gibi temel bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="1db32-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="1db32-258">**İstihdam**: Şirket veya kuruluş ilişkisi, pozisyon ataması, başlangıç ve bitiş tarihleri, iş uygunluğu, istihdam koşulları, emeklilik, tatil ve tayin bilgileri gibi bir çalışanın istihdamıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="1db32-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="1db32-259">**İzin ve devamsızlık**: Çalışma takvimleri, devamsızlık işlemleri ve devamsızlık ayarı gibi bir çalışanın devamsızlığıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="1db32-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="1db32-260">**Ücret ve bordro**: Plan kaydı, ödüller, performans, komisyon, vergi bilgileri, emeklilik ve maaş kesintileri gibi bir çalışanın ücret planlarıyla ilgili bilgileri ve bordro bilgilerini tutun.</span><span class="sxs-lookup"><span data-stu-id="1db32-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="1db32-261">Çalışan bilgilerini girerken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="1db32-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="1db32-262">Genel bilgiler</span><span class="sxs-lookup"><span data-stu-id="1db32-262">General information</span></span>

- <span data-ttu-id="1db32-263">Personel numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-263">Personnel number (required)</span></span>
- <span data-ttu-id="1db32-264">Ad (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-264">First name (required)</span></span>
- <span data-ttu-id="1db32-265">Soyadı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-265">Last name (required)</span></span>
- <span data-ttu-id="1db32-266">İkinci adı</span><span class="sxs-lookup"><span data-stu-id="1db32-266">Middle name</span></span>
- <span data-ttu-id="1db32-267">Kıdem tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-267">Seniority date</span></span>
- <span data-ttu-id="1db32-268">Bilinen hali</span><span class="sxs-lookup"><span data-stu-id="1db32-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="1db32-269">Kişisel bilgiler</span><span class="sxs-lookup"><span data-stu-id="1db32-269">Personal information</span></span>

- <span data-ttu-id="1db32-270">Medeni durum (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-270">Marital status (required)</span></span>
- <span data-ttu-id="1db32-271">Doğum tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-271">Birth date (required)</span></span>
- <span data-ttu-id="1db32-272">Cinsiyet (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-272">Gender (required)</span></span>
- <span data-ttu-id="1db32-273">Engelli kişi</span><span class="sxs-lookup"><span data-stu-id="1db32-273">Person with disabilities</span></span>
- <span data-ttu-id="1db32-274">Uyruğu ülkesi bölgesi (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="1db32-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="1db32-275">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="1db32-275">Address information</span></span>

- <span data-ttu-id="1db32-276">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-276">Primary (required)</span></span>
- <span data-ttu-id="1db32-277">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-277">Country/region (required)</span></span>
- <span data-ttu-id="1db32-278">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-278">Postal code (required)</span></span>
- <span data-ttu-id="1db32-279">Cadde Numarası (gerekli) (Yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="1db32-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="1db32-280">Bina Tamamlayıcı (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="1db32-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="1db32-281">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-281">City (required)</span></span>
- <span data-ttu-id="1db32-282">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-282">State (required)</span></span>
- <span data-ttu-id="1db32-283">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="1db32-284">İletişim bilgileri</span><span class="sxs-lookup"><span data-stu-id="1db32-284">Contact information</span></span> 

- <span data-ttu-id="1db32-285">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-285">Primary (required)</span></span>
- <span data-ttu-id="1db32-286">İlgili kişi numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-286">Contact number (required)</span></span>
- <span data-ttu-id="1db32-287">Dahili</span><span class="sxs-lookup"><span data-stu-id="1db32-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="1db32-288">Bordro bilgileri ve kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="1db32-288">Payroll information and earning codes</span></span>

<span data-ttu-id="1db32-289">Personele belirli bir ödeme sıklığında özel kazançlar atanabilir ve çalışanlar, tercih edilen bir ödeme yöntemine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="1db32-290">Bu tercihlerin ve ayarların kullanıldığının sağlanmasına yardımcı olmak için Dayforce'ta aşağıdaki alanlar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="1db32-291">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="1db32-291">Earning codes</span></span>

- <span data-ttu-id="1db32-292">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-292">Position (required)</span></span>
- <span data-ttu-id="1db32-293">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-293">Earning Code (required)</span></span>
- <span data-ttu-id="1db32-294">Sıklık (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-294">Frequency (required)</span></span>
- <span data-ttu-id="1db32-295">Tutar (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="1db32-296">Bordro bilgileri</span><span class="sxs-lookup"><span data-stu-id="1db32-296">Payroll information</span></span>

- <span data-ttu-id="1db32-297">Ödeme Yöntemi</span><span class="sxs-lookup"><span data-stu-id="1db32-297">Payment Method</span></span>
- <span data-ttu-id="1db32-298">Ekonomik Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-298">Economic Region (required)</span></span>
- <span data-ttu-id="1db32-299">Personel Kazanç Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-299">Employee Benefits ID</span></span>
- <span data-ttu-id="1db32-300">Ulusal Kimlik Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-300">National ID Number (required)</span></span>
- <span data-ttu-id="1db32-301">Askerlik Hizmet Numarası</span><span class="sxs-lookup"><span data-stu-id="1db32-301">Military Service Number</span></span>
- <span data-ttu-id="1db32-302">Vardiya Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-302">Shift ID (required)</span></span>
- <span data-ttu-id="1db32-303">Vergi Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-303">Tax Number (required)</span></span>
- <span data-ttu-id="1db32-304">Sendika Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-304">Union ID (required)</span></span>
- <span data-ttu-id="1db32-305">İş Günü Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-305">Work Day ID (required)</span></span>
- <span data-ttu-id="1db32-306">Çalışma İzni Numarası</span><span class="sxs-lookup"><span data-stu-id="1db32-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="1db32-307">Meksika'da ödeme yöntemleri olarak **Nakit**, **Çek** (şirketin fiziksel çeki) ve **Elektronik Ödeme** desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="1db32-308">Hiçbir ödeme yöntemi belirtilmemişse varsayılan olarak **Çek** kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="1db32-309">İstihdam ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="1db32-309">Employment details</span></span>

<span data-ttu-id="1db32-310">İstihdam ayrıntıları geçmişi, personelin Dayforce'ta işe alma, işten çıkarma ve yeniden işe alma durumlarını oluşturmada temel bilgi olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="1db32-311">Dayforce, bir defada yalnızca bir etkin istihdam kaydını destekler.</span><span class="sxs-lookup"><span data-stu-id="1db32-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="1db32-312">İşe başlama tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-312">Employment start date (required)</span></span>
- <span data-ttu-id="1db32-313">İş bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-313">Employment end date</span></span>
- <span data-ttu-id="1db32-314">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-314">Start date</span></span>
- <span data-ttu-id="1db32-315">Ayarlanan başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-315">Adjusted start date</span></span>
- <span data-ttu-id="1db32-316">İşten çıkarma tarihi (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="1db32-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="1db32-317">İşten çıkarma nedeni (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="1db32-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="1db32-318">Personelin önemli tarihleri aşağıdaki bilgiler kullanılarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="1db32-319">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-319">Talent</span></span>                | <span data-ttu-id="1db32-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1db32-321">En son işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-321">Most recent hire date</span></span> | <span data-ttu-id="1db32-322">Geçerli sonlandırılmamış işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="1db32-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="1db32-323">İşten çıkarma tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-323">Termination date</span></span>      | <span data-ttu-id="1db32-324">Geçerli sonlandırılmamış işten çıkış tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="1db32-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="1db32-325">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-325">Start date</span></span>            | <span data-ttu-id="1db32-326">Ayarlanan başlama tarihi, başlama tarihi veya geçerli etkin olmayan işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="1db32-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="1db32-327">Orijinal işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-327">Original hire date</span></span>    | <span data-ttu-id="1db32-328">En erken işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="1db32-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="1db32-329">Ücret</span><span class="sxs-lookup"><span data-stu-id="1db32-329">Compensation</span></span>

<span data-ttu-id="1db32-330">Bir istihdam dönemi boyunca her personelin birincil pozisyonu ile sabit ücret planı ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="1db32-331">Bu dönem personelin işe alındığı (veya işe başlama tarihi) tarihte başlar ve işten çıkış tarihine kadar devam eder.</span><span class="sxs-lookup"><span data-stu-id="1db32-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="1db32-332">Yürürlük Tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-332">Effective Date (required)</span></span>
- <span data-ttu-id="1db32-333">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-333">Expiration date</span></span>
- <span data-ttu-id="1db32-334">Ödeme Oranı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-334">Pay Rate (required)</span></span>
- <span data-ttu-id="1db32-335">Ödeme Oranı Dönüştürmeleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="1db32-336">Yıllık eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="1db32-337">Saatlik eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="1db32-338">Saatlik personelin birden fazla pozisyonu varsa birincil pozisyonun sabit ücreti, personel düzeyinde taban oranı/maaş olarak Dayforce'ta içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="1db32-339">Birincil olmayan pozisyonlar için saatlik oran Dayforce'ta ilgili pozisyona kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="1db32-340">Maaşlı personelin birden fazla pozisyonu varsa tüm etkin pozisyonlar için kümülatif saat oranı ve yıllık maaş oluşturulur ve personel düzeyinde taban oranı/maaş olarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="1db32-341">Kimlik numaraları</span><span class="sxs-lookup"><span data-stu-id="1db32-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="1db32-342">Sosyal Güvenlik Kimlik Tanımlayıcı</span><span class="sxs-lookup"><span data-stu-id="1db32-342">Social Security identifier</span></span> 

<span data-ttu-id="1db32-343">Her personelin bir birincil kimlik tanımlayıcısı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="1db32-344">Bu kimlik tanımlayıcı **SSK** kimlik türünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1db32-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="1db32-345">Dayforce'ta bu, personelin işe alınması için gereken Sosyal Güvenlik kimlik tanımlayıcı olarak otomatik türetilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="1db32-346">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-346">Primary (required)</span></span>
- <span data-ttu-id="1db32-347">Kimlik Türü = "SSN"</span><span class="sxs-lookup"><span data-stu-id="1db32-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="1db32-348">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="1db32-348">Issued Date</span></span>
- <span data-ttu-id="1db32-349">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-349">Expiration Date</span></span>

<span data-ttu-id="1db32-350">Personel, **SSN** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="1db32-351">Ancak numaranın etkin veya süresinin dolmuş olup olmadığına bakılmaksızın yalnızca **Birincil** olarak işaretlenen kayıt Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="1db32-352">Banka hesapları ve tahsilatlar</span><span class="sxs-lookup"><span data-stu-id="1db32-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="1db32-353">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel için geçerli banka hesap bilgileri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="1db32-354">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-354">Talent</span></span>                         | <span data-ttu-id="1db32-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1db32-356">Banka hesap numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="1db32-357">SWIFT kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-357">SWIFT code (required)</span></span>          | <span data-ttu-id="1db32-358">Meksika'da bordro işlemleri için **Banka Kodu** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="1db32-359">Şube numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="1db32-360">Banka hesabı türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-360">Bank account type (required)</span></span>   | <span data-ttu-id="1db32-361">Meksika'da bordro işlemleri için **Hesap türü** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="1db32-362">Desteklenen değerler **Cari** ve **Bordro**'yu içerir.</span><span class="sxs-lookup"><span data-stu-id="1db32-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="1db32-363">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel, birincil adresi Meksika'da olan ve bir Meksika bankasındaki geçerli bir banka hesabıyla ilişkilendirilmiş tüzel kişilik altında bulunan bir bakiye hesabına bağlantı sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="1db32-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="1db32-364">Bakiye hesabı olmayan diğer hesaplar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="1db32-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="1db32-365">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="1db32-365">Address information</span></span>

<span data-ttu-id="1db32-366">Her personelin bir birincil konumu olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-366">Every employee must have one primary location.</span></span> <span data-ttu-id="1db32-367">Dayforce'ta bu konum, personelin vergiye esas birincil ikamet yerini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="1db32-368">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-368">Primary (required)</span></span>
- <span data-ttu-id="1db32-369">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-369">Country/region (required)</span></span>
- <span data-ttu-id="1db32-370">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="1db32-371">Cadde (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-371">Street (required)</span></span>
- <span data-ttu-id="1db32-372">Cadde Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-372">Street Number (required)</span></span>
- <span data-ttu-id="1db32-373">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="1db32-373">Building Complement</span></span>
- <span data-ttu-id="1db32-374">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-374">City (required)</span></span>
- <span data-ttu-id="1db32-375">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-375">State (required)</span></span>
- <span data-ttu-id="1db32-376">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="1db32-377">Amerika Birleşik Devletleri ve Kanada’da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1db32-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="1db32-378">Amerika Birleşik Devletleri ve Kanada’daki personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="1db32-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="1db32-379">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-379">Departments are required on positions.</span></span>
- <span data-ttu-id="1db32-380">Maliyet merkezleri mali boyut olarak ayarlanmalı ve varsayılan mali boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1db32-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="1db32-381">Departman gerektiren Pozisyonlar için Talent gerektirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1db32-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="1db32-382">Bunu yapmak için **İnsan Kaynakları Paylaşılan Pozisyonlar > Pozisyonlar > Pozisyonlarda departmanlar gerektir**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1db32-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="1db32-383">Bu ayarın tümleştirme için zorunlu olmasını öneririz.</span><span class="sxs-lookup"><span data-stu-id="1db32-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="1db32-384">İş türleri</span><span class="sxs-lookup"><span data-stu-id="1db32-384">Job types</span></span>

<span data-ttu-id="1db32-385">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="1db32-386">Amerika Birleşik Devletleri ve Kanada'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="1db32-387">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="1db32-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="1db32-388">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="1db32-389">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="1db32-390">İş türü</span><span class="sxs-lookup"><span data-stu-id="1db32-390">Job type</span></span>   | <span data-ttu-id="1db32-391">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db32-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="1db32-392">Saatlik</span><span class="sxs-lookup"><span data-stu-id="1db32-392">Hourly</span></span>     | <span data-ttu-id="1db32-393">Saatlik</span><span class="sxs-lookup"><span data-stu-id="1db32-393">Hourly</span></span>      |
| <span data-ttu-id="1db32-394">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="1db32-394">Salaried</span></span>   | <span data-ttu-id="1db32-395">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="1db32-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="1db32-396">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="1db32-396">Position types</span></span> 

<span data-ttu-id="1db32-397">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="1db32-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="1db32-398">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="1db32-399">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="1db32-400">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="1db32-400">Position type</span></span>   | <span data-ttu-id="1db32-401">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db32-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="1db32-402">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="1db32-402">Full-time</span></span>       | <span data-ttu-id="1db32-403">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="1db32-403">Full time employee</span></span> |
| <span data-ttu-id="1db32-404">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="1db32-404">Part-time</span></span>       | <span data-ttu-id="1db32-405">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="1db32-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="1db32-406">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="1db32-406">Reason codes</span></span>

<span data-ttu-id="1db32-407">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="1db32-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="1db32-408">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="1db32-409">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="1db32-410">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-410">Reason code</span></span>    | <span data-ttu-id="1db32-411">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db32-411">Description</span></span>      | <span data-ttu-id="1db32-412">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="1db32-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="1db32-413">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="1db32-413">RESIGNATION</span></span>    | <span data-ttu-id="1db32-414">İstifa</span><span class="sxs-lookup"><span data-stu-id="1db32-414">Resignation</span></span>      | <span data-ttu-id="1db32-415">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-415">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-416">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="1db32-416">TERMINATION</span></span>    | <span data-ttu-id="1db32-417">Bitiş</span><span class="sxs-lookup"><span data-stu-id="1db32-417">Termination</span></span>      | <span data-ttu-id="1db32-418">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-418">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-419">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="1db32-419">RETIREMENT</span></span>     | <span data-ttu-id="1db32-420">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="1db32-420">Retirement</span></span>       | <span data-ttu-id="1db32-421">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-421">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-422">OTHER</span><span class="sxs-lookup"><span data-stu-id="1db32-422">OTHER</span></span>          | <span data-ttu-id="1db32-423">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="1db32-423">Other Reasons</span></span>    | <span data-ttu-id="1db32-424">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-424">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-425">DEATH</span><span class="sxs-lookup"><span data-stu-id="1db32-425">DEATH</span></span>          | <span data-ttu-id="1db32-426">Ölüm</span><span class="sxs-lookup"><span data-stu-id="1db32-426">Death</span></span>            | <span data-ttu-id="1db32-427">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-427">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="1db32-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="1db32-429">İzin</span><span class="sxs-lookup"><span data-stu-id="1db32-429">Leave of Absence</span></span> | <span data-ttu-id="1db32-430">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-430">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="1db32-431">CONTRACTEND</span></span>    | <span data-ttu-id="1db32-432">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="1db32-432">End of Contract</span></span>  | <span data-ttu-id="1db32-433">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-433">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="1db32-434">SALARYCHANGE</span></span>   | <span data-ttu-id="1db32-435">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="1db32-435">Change of Salary</span></span> | <span data-ttu-id="1db32-436">Ücret</span><span class="sxs-lookup"><span data-stu-id="1db32-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="1db32-437">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="1db32-437">Marital status</span></span>

<span data-ttu-id="1db32-438">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="1db32-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1db32-439">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1db32-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="1db32-440">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-440">Talent</span></span>                 | <span data-ttu-id="1db32-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="1db32-442">Evli</span><span class="sxs-lookup"><span data-stu-id="1db32-442">Married</span></span>                | <span data-ttu-id="1db32-443">Evli</span><span class="sxs-lookup"><span data-stu-id="1db32-443">Married</span></span>              |
| <span data-ttu-id="1db32-444">Tekli</span><span class="sxs-lookup"><span data-stu-id="1db32-444">Single</span></span>                 | <span data-ttu-id="1db32-445">Tekli</span><span class="sxs-lookup"><span data-stu-id="1db32-445">Single</span></span>               |
| <span data-ttu-id="1db32-446">Dul</span><span class="sxs-lookup"><span data-stu-id="1db32-446">Widowed</span></span>                | <span data-ttu-id="1db32-447">Dul</span><span class="sxs-lookup"><span data-stu-id="1db32-447">Widowed</span></span>              |
| <span data-ttu-id="1db32-448">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="1db32-448">Divorced</span></span>               | <span data-ttu-id="1db32-449">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="1db32-449">Divorced</span></span>             |
| <span data-ttu-id="1db32-450">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="1db32-450">Registered Partnership</span></span> | <span data-ttu-id="1db32-451">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="1db32-451">Domestic Partnership</span></span> |
| <span data-ttu-id="1db32-452">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="1db32-452">None</span></span>                   | <span data-ttu-id="1db32-453">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="1db32-453">None</span></span>                 |
| <span data-ttu-id="1db32-454">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="1db32-454">Cohabiting</span></span>             | <span data-ttu-id="1db32-455">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="1db32-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="1db32-456">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="1db32-456">Gender</span></span>

<span data-ttu-id="1db32-457">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="1db32-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1db32-458">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1db32-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="1db32-459">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-459">Talent</span></span>       | <span data-ttu-id="1db32-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="1db32-461">Erkek</span><span class="sxs-lookup"><span data-stu-id="1db32-461">Male</span></span>         | <span data-ttu-id="1db32-462">Erkek</span><span class="sxs-lookup"><span data-stu-id="1db32-462">Male</span></span>            |
| <span data-ttu-id="1db32-463">Kadın</span><span class="sxs-lookup"><span data-stu-id="1db32-463">Female</span></span>       | <span data-ttu-id="1db32-464">Kadın</span><span class="sxs-lookup"><span data-stu-id="1db32-464">Female</span></span>          |
| <span data-ttu-id="1db32-465">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="1db32-465">Non-specific</span></span> | <span data-ttu-id="1db32-466">*Desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="1db32-467">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="1db32-467">Earning codes</span></span>

<span data-ttu-id="1db32-468">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1db32-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1db32-469">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="1db32-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="1db32-470">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="1db32-471">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="1db32-471">Supported frequencies</span></span>

- <span data-ttu-id="1db32-472">Tümü</span><span class="sxs-lookup"><span data-stu-id="1db32-472">All</span></span>
- <span data-ttu-id="1db32-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="1db32-473">EVERYPAY</span></span>
- <span data-ttu-id="1db32-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="1db32-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="1db32-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="1db32-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="1db32-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="1db32-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="1db32-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-477">1OFMTH</span></span>
- <span data-ttu-id="1db32-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-478">LASTOFMTH</span></span>
- <span data-ttu-id="1db32-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-479">2OFMTH</span></span>
- <span data-ttu-id="1db32-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-480">3OFMTH</span></span>
- <span data-ttu-id="1db32-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-481">4OFMTH</span></span>
- <span data-ttu-id="1db32-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-482">5OFMTH</span></span>
- <span data-ttu-id="1db32-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-483">1N2OFMTH</span></span>
- <span data-ttu-id="1db32-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-484">3N4OFMTH</span></span>
- <span data-ttu-id="1db32-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-485">1N3OFMTH</span></span>
- <span data-ttu-id="1db32-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-486">1N4OFMTH</span></span>
- <span data-ttu-id="1db32-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-487">2N3OFMTH</span></span>
- <span data-ttu-id="1db32-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-488">2N4OFMTH</span></span>
- <span data-ttu-id="1db32-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="1db32-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="1db32-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="1db32-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="1db32-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="1db32-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="1db32-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="1db32-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="1db32-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="1db32-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="1db32-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="1db32-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="1db32-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="1db32-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="1db32-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="1db32-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1db32-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="1db32-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1db32-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="1db32-501">Adresler</span><span class="sxs-lookup"><span data-stu-id="1db32-501">Addresses</span></span>

<span data-ttu-id="1db32-502">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="1db32-503">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="1db32-504">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-504">Talent</span></span>          | <span data-ttu-id="1db32-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="1db32-506">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="1db32-506">Country/Region</span></span>  | <span data-ttu-id="1db32-507">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-507">Country Code</span></span>          |
| <span data-ttu-id="1db32-508">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-508">Zip/Postal Code</span></span> | <span data-ttu-id="1db32-509">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-509">Postal Code</span></span>           |
| <span data-ttu-id="1db32-510">İl</span><span class="sxs-lookup"><span data-stu-id="1db32-510">State</span></span>           | <span data-ttu-id="1db32-511">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-511">State Code</span></span>            |
| <span data-ttu-id="1db32-512">Şehir</span><span class="sxs-lookup"><span data-stu-id="1db32-512">City</span></span>            | <span data-ttu-id="1db32-513">Şehir</span><span class="sxs-lookup"><span data-stu-id="1db32-513">City</span></span>                  |
| <span data-ttu-id="1db32-514">İlçe</span><span class="sxs-lookup"><span data-stu-id="1db32-514">County</span></span>          | <span data-ttu-id="1db32-515">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="1db32-515">County (Municipality)</span></span> |
| <span data-ttu-id="1db32-516">Sokak</span><span class="sxs-lookup"><span data-stu-id="1db32-516">Street</span></span>          | <span data-ttu-id="1db32-517">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="1db32-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="1db32-518">Vergi bölgeleri</span><span class="sxs-lookup"><span data-stu-id="1db32-518">Tax regions</span></span>

<span data-ttu-id="1db32-519">Vergi bölgeleri, bordro oluşturma sırasında uygulanması gereken uygun vergiyi belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="1db32-520">Vergi bölgeleri, Dayforce'a konum adresleri olarak eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="1db32-521">Varsayılan vergi bölgesi, çalışanın etkin konumuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="1db32-522">Vergi bölgesi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-522">Tax region (required)</span></span>
- <span data-ttu-id="1db32-523">Ülke/Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-523">Country/Region (required)</span></span>
- <span data-ttu-id="1db32-524">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-524">State (required)</span></span>
- <span data-ttu-id="1db32-525">İlçe</span><span class="sxs-lookup"><span data-stu-id="1db32-525">County</span></span> 
- <span data-ttu-id="1db32-526">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="1db32-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="1db32-527">Meksika'da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1db32-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="1db32-528">Meksika'da personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="1db32-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="1db32-529">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-529">Departments are required on positions.</span></span>
- <span data-ttu-id="1db32-530">Maliyet merkezleri mali boyut olarak ayarlanmalı ve Varsayılan Mali Boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1db32-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="1db32-531">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="1db32-531">Job types</span></span>

<span data-ttu-id="1db32-532">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="1db32-533">Meksika'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="1db32-534">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="1db32-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="1db32-535">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="1db32-536">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="1db32-537">İş türü</span><span class="sxs-lookup"><span data-stu-id="1db32-537">Job type</span></span>   | <span data-ttu-id="1db32-538">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db32-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="1db32-539">Saatlik</span><span class="sxs-lookup"><span data-stu-id="1db32-539">Hourly</span></span>     | <span data-ttu-id="1db32-540">MX Saatlik</span><span class="sxs-lookup"><span data-stu-id="1db32-540">MX Hourly</span></span>   |
| <span data-ttu-id="1db32-541">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="1db32-541">Salaried</span></span>   | <span data-ttu-id="1db32-542">MX Maaşlı</span><span class="sxs-lookup"><span data-stu-id="1db32-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="1db32-543">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="1db32-543">Position types</span></span> 

<span data-ttu-id="1db32-544">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="1db32-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="1db32-545">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="1db32-546">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="1db32-547">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="1db32-547">Position type</span></span>   | <span data-ttu-id="1db32-548">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db32-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="1db32-549">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="1db32-549">Full-time</span></span>       | <span data-ttu-id="1db32-550">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="1db32-550">Full time employee</span></span> |
| <span data-ttu-id="1db32-551">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="1db32-551">Part-time</span></span>       | <span data-ttu-id="1db32-552">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="1db32-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="1db32-553">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="1db32-553">Reason codes</span></span>

<span data-ttu-id="1db32-554">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="1db32-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="1db32-555">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="1db32-556">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="1db32-557">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-557">Reason code</span></span>            | <span data-ttu-id="1db32-558">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db32-558">Description</span></span>                    | <span data-ttu-id="1db32-559">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="1db32-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="1db32-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="1db32-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="1db32-561">İlk bordrodan önce ayrılma</span><span class="sxs-lookup"><span data-stu-id="1db32-561">Departure before first payroll</span></span> | <span data-ttu-id="1db32-562">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-562">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-563">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="1db32-563">RESIGNATION</span></span>            | <span data-ttu-id="1db32-564">İstifa</span><span class="sxs-lookup"><span data-stu-id="1db32-564">Resignation</span></span>                    | <span data-ttu-id="1db32-565">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-565">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="1db32-566">PENSION</span></span>                | <span data-ttu-id="1db32-567">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="1db32-567">Pension</span></span>                        | <span data-ttu-id="1db32-568">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-568">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-569">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="1db32-569">TERMINATION</span></span>            | <span data-ttu-id="1db32-570">Bitiş</span><span class="sxs-lookup"><span data-stu-id="1db32-570">Termination</span></span>                    | <span data-ttu-id="1db32-571">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-571">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-572">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="1db32-572">RETIREMENT</span></span>             | <span data-ttu-id="1db32-573">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="1db32-573">Retirement</span></span>                     | <span data-ttu-id="1db32-574">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-574">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="1db32-575">ABSENTEE</span></span>               | <span data-ttu-id="1db32-576">Devamsızlık</span><span class="sxs-lookup"><span data-stu-id="1db32-576">Absentee</span></span>                       | <span data-ttu-id="1db32-577">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-577">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-578">OTHER</span><span class="sxs-lookup"><span data-stu-id="1db32-578">OTHER</span></span>                  | <span data-ttu-id="1db32-579">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="1db32-579">Other Reasons</span></span>                  | <span data-ttu-id="1db32-580">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-580">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-581">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="1db32-581">CLOSURE</span></span>                | <span data-ttu-id="1db32-582">İşletmenin Kapanması</span><span class="sxs-lookup"><span data-stu-id="1db32-582">Business Closure</span></span>               | <span data-ttu-id="1db32-583">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-583">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-584">DEATH</span><span class="sxs-lookup"><span data-stu-id="1db32-584">DEATH</span></span>                  | <span data-ttu-id="1db32-585">Ölüm</span><span class="sxs-lookup"><span data-stu-id="1db32-585">Death</span></span>                          | <span data-ttu-id="1db32-586">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-586">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="1db32-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="1db32-588">İzin</span><span class="sxs-lookup"><span data-stu-id="1db32-588">Leave of Absence</span></span>               | <span data-ttu-id="1db32-589">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-589">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="1db32-590">CONTRACTEND</span></span>            | <span data-ttu-id="1db32-591">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="1db32-591">End of Contract</span></span>                | <span data-ttu-id="1db32-592">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="1db32-592">Terminate worker</span></span>     |
| <span data-ttu-id="1db32-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="1db32-593">SALARYCHANGE</span></span>           | <span data-ttu-id="1db32-594">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="1db32-594">Change of Salary</span></span>               | <span data-ttu-id="1db32-595">Ücret</span><span class="sxs-lookup"><span data-stu-id="1db32-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="1db32-596">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="1db32-596">Terms of employment</span></span>

<span data-ttu-id="1db32-597">İstihdam koşulları, istihdam koşullarının kategorilerini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="1db32-598">Koşullar, istihdam göstergesi değerleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="1db32-599">Aşağıdaki istihdam koşulları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="1db32-600">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="1db32-600">Terms of employment</span></span>   | <span data-ttu-id="1db32-601">Tanım</span><span class="sxs-lookup"><span data-stu-id="1db32-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="1db32-602">Normal</span><span class="sxs-lookup"><span data-stu-id="1db32-602">Regular</span></span>               | <span data-ttu-id="1db32-603">Normal</span><span class="sxs-lookup"><span data-stu-id="1db32-603">Regular</span></span>     |
| <span data-ttu-id="1db32-604">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="1db32-604">Direct</span></span>                | <span data-ttu-id="1db32-605">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="1db32-605">Direct</span></span>      |
| <span data-ttu-id="1db32-606">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="1db32-606">Internship</span></span>            | <span data-ttu-id="1db32-607">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="1db32-607">Internship</span></span>  |
| <span data-ttu-id="1db32-608">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="1db32-608">Permanent</span></span>             | <span data-ttu-id="1db32-609">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="1db32-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="1db32-610">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="1db32-610">Marital status</span></span>

<span data-ttu-id="1db32-611">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="1db32-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1db32-612">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1db32-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="1db32-613">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-613">Talent</span></span>                 | <span data-ttu-id="1db32-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="1db32-615">Evli</span><span class="sxs-lookup"><span data-stu-id="1db32-615">Married</span></span>                | <span data-ttu-id="1db32-616">Evli</span><span class="sxs-lookup"><span data-stu-id="1db32-616">Married</span></span>                   |
| <span data-ttu-id="1db32-617">Tekli</span><span class="sxs-lookup"><span data-stu-id="1db32-617">Single</span></span>                 | <span data-ttu-id="1db32-618">Tekli</span><span class="sxs-lookup"><span data-stu-id="1db32-618">Single</span></span>                    |
| <span data-ttu-id="1db32-619">Dul</span><span class="sxs-lookup"><span data-stu-id="1db32-619">Widowed</span></span>                | <span data-ttu-id="1db32-620">Dul</span><span class="sxs-lookup"><span data-stu-id="1db32-620">Widowed</span></span>                   |
| <span data-ttu-id="1db32-621">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="1db32-621">Divorced</span></span>               | <span data-ttu-id="1db32-622">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="1db32-622">Divorced</span></span>                  |
| <span data-ttu-id="1db32-623">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="1db32-623">Registered Partnership</span></span> | <span data-ttu-id="1db32-624">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="1db32-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="1db32-625">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="1db32-625">None</span></span>                   | <span data-ttu-id="1db32-626">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1db32-627">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="1db32-627">Cohabiting</span></span>             | <span data-ttu-id="1db32-628">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="1db32-629">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="1db32-629">Gender</span></span>

<span data-ttu-id="1db32-630">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="1db32-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1db32-631">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1db32-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="1db32-632">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-632">Talent</span></span>       | <span data-ttu-id="1db32-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="1db32-634">Erkek</span><span class="sxs-lookup"><span data-stu-id="1db32-634">Male</span></span>         | <span data-ttu-id="1db32-635">Erkek</span><span class="sxs-lookup"><span data-stu-id="1db32-635">Male</span></span>                      |
| <span data-ttu-id="1db32-636">Kadın</span><span class="sxs-lookup"><span data-stu-id="1db32-636">Female</span></span>       | <span data-ttu-id="1db32-637">Kadın</span><span class="sxs-lookup"><span data-stu-id="1db32-637">Female</span></span>                    |
| <span data-ttu-id="1db32-638">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="1db32-638">Non-specific</span></span> | <span data-ttu-id="1db32-639">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="1db32-640">Ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="1db32-640">Payment method</span></span>

<span data-ttu-id="1db32-641">Ödeme yöntemleri, personele ve şirkete çalışanlara nasıl ödeme yapılacağını tanımlamak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="1db32-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="1db32-642">Ödeme yöntemleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="1db32-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="1db32-643">Aşağıdaki tabloda ödeme yöntemlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1db32-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="1db32-644">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-644">Talent</span></span>             | <span data-ttu-id="1db32-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="1db32-646">Nakit</span><span class="sxs-lookup"><span data-stu-id="1db32-646">Cash</span></span>               | <span data-ttu-id="1db32-647">Nakit</span><span class="sxs-lookup"><span data-stu-id="1db32-647">Cash</span></span>                      |
| <span data-ttu-id="1db32-648">Elektronik Ödeme</span><span class="sxs-lookup"><span data-stu-id="1db32-648">Electronic Payment</span></span> | <span data-ttu-id="1db32-649">Transfer et</span><span class="sxs-lookup"><span data-stu-id="1db32-649">Transfer</span></span>                  |
| <span data-ttu-id="1db32-650">Denetle</span><span class="sxs-lookup"><span data-stu-id="1db32-650">Check</span></span>              | <span data-ttu-id="1db32-651">Çek</span><span class="sxs-lookup"><span data-stu-id="1db32-651">Cheque</span></span>                    |
| <span data-ttu-id="1db32-652">Banka Ödeme Emri</span><span class="sxs-lookup"><span data-stu-id="1db32-652">Bank Draft</span></span>         | <span data-ttu-id="1db32-653">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1db32-654">Diğer</span><span class="sxs-lookup"><span data-stu-id="1db32-654">Other</span></span>              | <span data-ttu-id="1db32-655">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="1db32-656">Banka hesabı türü</span><span class="sxs-lookup"><span data-stu-id="1db32-656">Bank account type</span></span>

<span data-ttu-id="1db32-657">Banka hesap türleri, personele elektronik ödeme yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="1db32-658">Banka hesap türleri, transfer hesabı bilgileri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="1db32-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="1db32-659">Banka hesap türleri, uygunsa tümleştirme işleminden sonra kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="1db32-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="1db32-660">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-660">Talent</span></span>            | <span data-ttu-id="1db32-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="1db32-662">Cari Hesap</span><span class="sxs-lookup"><span data-stu-id="1db32-662">Checking Account</span></span>  | <span data-ttu-id="1db32-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="1db32-663">CheckingAccount</span></span>           |
| <span data-ttu-id="1db32-664">Bordro Hesabı</span><span class="sxs-lookup"><span data-stu-id="1db32-664">Payroll Account</span></span>   | <span data-ttu-id="1db32-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="1db32-665">PayrollAccount</span></span>            |
| <span data-ttu-id="1db32-666">Tasarruf Hesabı</span><span class="sxs-lookup"><span data-stu-id="1db32-666">Savings Account</span></span>   | <span data-ttu-id="1db32-667">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1db32-668">BankGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="1db32-668">BankGirot account</span></span> | <span data-ttu-id="1db32-669">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="1db32-670">PlusGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="1db32-670">PlusGirot account</span></span> | <span data-ttu-id="1db32-671">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="1db32-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="1db32-672">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="1db32-672">Earning codes</span></span>

<span data-ttu-id="1db32-673">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1db32-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="1db32-674">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="1db32-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="1db32-675">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1db32-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="1db32-676">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="1db32-676">Supported frequencies</span></span>

- <span data-ttu-id="1db32-677">Tümü</span><span class="sxs-lookup"><span data-stu-id="1db32-677">All</span></span>
- <span data-ttu-id="1db32-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="1db32-678">EVERYPAY</span></span>
- <span data-ttu-id="1db32-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="1db32-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="1db32-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="1db32-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="1db32-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="1db32-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="1db32-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-682">1OFMTH</span></span>
- <span data-ttu-id="1db32-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-683">LASTOFMTH</span></span>
- <span data-ttu-id="1db32-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-684">2OFMTH</span></span>
- <span data-ttu-id="1db32-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-685">3OFMTH</span></span>
- <span data-ttu-id="1db32-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-686">4OFMTH</span></span>
- <span data-ttu-id="1db32-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-687">5OFMTH</span></span>
- <span data-ttu-id="1db32-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-688">1N2OFMTH</span></span>
- <span data-ttu-id="1db32-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-689">3N4OFMTH</span></span>
- <span data-ttu-id="1db32-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-690">1N3OFMTH</span></span>
- <span data-ttu-id="1db32-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-691">1N4OFMTH</span></span>
- <span data-ttu-id="1db32-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-692">2N3OFMTH</span></span>
- <span data-ttu-id="1db32-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-693">2N4OFMTH</span></span>
- <span data-ttu-id="1db32-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="1db32-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="1db32-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="1db32-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="1db32-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="1db32-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="1db32-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="1db32-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="1db32-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="1db32-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="1db32-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="1db32-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="1db32-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="1db32-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="1db32-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="1db32-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="1db32-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1db32-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="1db32-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="1db32-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="1db32-706">Adresler</span><span class="sxs-lookup"><span data-stu-id="1db32-706">Addresses</span></span>

<span data-ttu-id="1db32-707">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="1db32-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="1db32-708">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1db32-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="1db32-709">Talent</span><span class="sxs-lookup"><span data-stu-id="1db32-709">Talent</span></span>              | <span data-ttu-id="1db32-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="1db32-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="1db32-711">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="1db32-711">Country/Region</span></span>      | <span data-ttu-id="1db32-712">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-712">Country Code</span></span>          |
| <span data-ttu-id="1db32-713">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-713">Zip/Postal Code</span></span>     | <span data-ttu-id="1db32-714">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-714">Postal Code</span></span>           |
| <span data-ttu-id="1db32-715">İl</span><span class="sxs-lookup"><span data-stu-id="1db32-715">State</span></span>               | <span data-ttu-id="1db32-716">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="1db32-716">State Code</span></span>            |
| <span data-ttu-id="1db32-717">Şehir</span><span class="sxs-lookup"><span data-stu-id="1db32-717">City</span></span>                | <span data-ttu-id="1db32-718">Şehir</span><span class="sxs-lookup"><span data-stu-id="1db32-718">City</span></span>                  |
| <span data-ttu-id="1db32-719">İlçe</span><span class="sxs-lookup"><span data-stu-id="1db32-719">County</span></span>              | <span data-ttu-id="1db32-720">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="1db32-720">County (Municipality)</span></span> |
| <span data-ttu-id="1db32-721">Sokak</span><span class="sxs-lookup"><span data-stu-id="1db32-721">Street</span></span>              | <span data-ttu-id="1db32-722">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="1db32-722">Address Line 1</span></span>        |
| <span data-ttu-id="1db32-723">Cadde Numarası</span><span class="sxs-lookup"><span data-stu-id="1db32-723">Street Number</span></span>       | <span data-ttu-id="1db32-724">Adres Satırı 2</span><span class="sxs-lookup"><span data-stu-id="1db32-724">Address Line 2</span></span>        |
| <span data-ttu-id="1db32-725">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="1db32-725">Building Complement</span></span> | <span data-ttu-id="1db32-726">Adres Satırı 5</span><span class="sxs-lookup"><span data-stu-id="1db32-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="1db32-727">Pasaport numarası</span><span class="sxs-lookup"><span data-stu-id="1db32-727">Passport number</span></span>

<span data-ttu-id="1db32-728">Personel pasaport bilgilerini bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-728">Employees can declare passport information.</span></span> <span data-ttu-id="1db32-729">Bu bilgiler, **Pasaport** kimlik türünü içerir ve Meksika'ya özel personel bilgilerinin bir parçası olarak Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="1db32-730">Kimlik Türü = "Pasaport"</span><span class="sxs-lookup"><span data-stu-id="1db32-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="1db32-731">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="1db32-731">Issued Date</span></span>
- <span data-ttu-id="1db32-732">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="1db32-732">Expiration Date</span></span>

<span data-ttu-id="1db32-733">Personel, **Pasaport** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="1db32-734">Ancak yalnızca geçerli etkin pasaport girişi Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="1db32-735">Tüm pasaport girişlerinin süresi dolmuşsa en son verilen pasaport Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1db32-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

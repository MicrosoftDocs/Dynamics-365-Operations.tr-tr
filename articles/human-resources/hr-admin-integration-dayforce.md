---
title: Dayforce ile tümleştirme yapılandırma
description: Microsoft Dynamics 365 Human Resources ile Ceridian Dayforce arasındaki tümleştirme, bu makalede açıklanan çeşitli yapılandırma adımlarına dayanır. Ödeme işlemini işlemeden önce tümleştirmeyi hem Human Resources'ta hem de Dayforce'ta yapılandırmanız gerekir.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051509"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="d818c-104">Dayforce ile tümleştirme yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d818c-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d818c-105">Microsoft Dynamics 365 Human Resources ile Ceridian Dayforce arasındaki tümleştirme, bu makalede açıklanan çeşitli yapılandırma adımlarına dayanır.</span><span class="sxs-lookup"><span data-stu-id="d818c-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="d818c-106">Ödeme işlemini işlemeden önce tümleştirmeyi hem Human Resources'ta hem de Dayforce'ta yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="d818c-107">Ödeme işlemlerini tamamlamak için Dayforce gibi bir hizmet kullandığınızda tümleştirmeyi Human Resources'ta etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="d818c-108">Tümleştirme için Human Resources'tan özel veriler gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="d818c-109">Bu nedenle, Dayforce ile eşlenmiş verilerin Human Resources'ta tümleştirmeyi destekleyecek şekilde yapılandırıldığını doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="d818c-110">Tümleştirme, aşağıdaki geniş veri kategorilerini kullanır:</span><span class="sxs-lookup"><span data-stu-id="d818c-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="d818c-111">İnsan kaynakları verileri</span><span class="sxs-lookup"><span data-stu-id="d818c-111">Human resources data</span></span>
- <span data-ttu-id="d818c-112">Ücret verileri</span><span class="sxs-lookup"><span data-stu-id="d818c-112">Compensation data</span></span>
- <span data-ttu-id="d818c-113">Ödeme döngüleri, ödeme dönemleri ve kazanç kodları gibi bordro verileri</span><span class="sxs-lookup"><span data-stu-id="d818c-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="d818c-114">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="d818c-114">Worker data</span></span>

<span data-ttu-id="d818c-115">Bu makalede, tümleştirmeyi etkinleştirmek için izlemeniz gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d818c-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="d818c-116">Ayrıca veri türleri ve tümleştirmenin gerektirdiği yapılandırma ayrıntıları da açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d818c-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="d818c-117">Tümleştirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d818c-117">Enable the integration</span></span>

<span data-ttu-id="d818c-118">Human Resources'ta yapılandırmayı açmanız ve Dayforce'a bağlanmak için yapılandırma bilgilerini girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="d818c-119">Microsoft Dynamics 365 Finance'a aktarılmak üzere oluşturulan genel muhasebe hareketini istiyorsanız ayrıca bir Microsoft Azure depolama hesabı oluşturmanız ve Finance'ta Azure Depolama bağlantı dizesini de girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="d818c-120">Human Resources'ta tümleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d818c-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="d818c-121">**Sistem yönetimi** sayfasında **Tümleştirme yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d818c-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="d818c-122">Güvenli Dosya Aktarım Protokolü (FTP) uç noktasını ve güvenli FTP klasörü yolunu girin.</span><span class="sxs-lookup"><span data-stu-id="d818c-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="d818c-123">Güvenli FTP uç noktasına ve klasör yoluna erişecek kullanıcının kullanıcı adını ve parolasını girin.</span><span class="sxs-lookup"><span data-stu-id="d818c-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="d818c-124">Bağlantıyı gerektiği gibi test edin ve **Bordro tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d818c-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="d818c-125">Tümleştirme açıldığında veri dışa aktarma paketi ve dosyalar oluşturulur ve sıklık ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d818c-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="d818c-126">Bu sıklığı ihtiyaç duyduğunuz şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d818c-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="d818c-127">Azure depolama hesapları ve Azure Depolama bağlantı dizeleri hakkında daha fazla bilgi için aşağıdaki Azure makalelerine bakın:</span><span class="sxs-lookup"><span data-stu-id="d818c-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="d818c-128">Azure depolama hesapları hakkında</span><span class="sxs-lookup"><span data-stu-id="d818c-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="d818c-129">Azure Depolama bağlantı dizelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d818c-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="d818c-130">Bordro tümleştirmesinin etkinleştirilmesinin teknik ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="d818c-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="d818c-131">Bordro tümleştirmesinin açılmasının iki temel etkisi vardır:</span><span class="sxs-lookup"><span data-stu-id="d818c-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="d818c-132">"Bordro tümleştirmesini dışa aktar" adlı dışa veri aktarma projesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d818c-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="d818c-133">Bu proje, bordro tümleştirmesi için gerekli olan varlıkları ve alanları içerir.</span><span class="sxs-lookup"><span data-stu-id="d818c-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="d818c-134">Projeyi incelemek için **Sistem yönetimi**'ne gidin, **Veri yönetimi** kutucuğunu seçin ve ardından projeler listesinden veri projesini açın.</span><span class="sxs-lookup"><span data-stu-id="d818c-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="d818c-135">Bu toplu iş, veri dışa aktarma projesini yürütür, sonuçta elde edilen veri paketini şifreler ve veri paketi dosyasını **Tümleştirme Yapılandırması** ekranında yapılandırılan SFTP son noktasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="d818c-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="d818c-136">SFTP son noktasına aktarılan veri paketi, pakette benzersiz bir anahtar kullanılarak şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="d818c-137">Anahtar yalnızca Ceridian tarafından erişilebilen bir Azure Key Vault'ta yer alır.</span><span class="sxs-lookup"><span data-stu-id="d818c-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="d818c-138">Veri paketi içeriğinin şifresini çözmek ve içeriği incelemek mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="d818c-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="d818c-139">Veri paketinin içeriğini incelemeniz gerekiyorsa "Bordro tümleştirmesini dışa aktar" veri projesini el ile dışa aktarmanız, indirmeniz ve sonra açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="d818c-140">El ile dışa aktarmada şifreleme uygulanmaz veya paket transfer edilmez.</span><span class="sxs-lookup"><span data-stu-id="d818c-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="d818c-141">Tümleştirme dosyalarının Dynamics 365 Human Resources UAT veya Korumalı alan ortamından bir Ceridian Dayforce Test ortamına gönderildiği durumlarda şu anahtar kasası URL'sini kullanabilirsiniz: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="d818c-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="d818c-142">Verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d818c-142">Configure your data</span></span> 

<span data-ttu-id="d818c-143">Bordro işlemek için Human Resources'ta insan kaynağı verilerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="d818c-144">Kazanç ve ücret bilgileriyle birlikte işler ve pozisyonlar gibi kurumsal verileri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="d818c-145">Bu bilgiler personel ödemesi oluşturmak için gerekli olan istihdam, ödeme ve kesinti bilgilerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d818c-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="d818c-146">İnsan kaynağı verileri</span><span class="sxs-lookup"><span data-stu-id="d818c-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="d818c-147">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="d818c-147">Benefits</span></span> 

<span data-ttu-id="d818c-148">İnsan kaynakları, bir kuruluşun çalışanları için sunduğu veya işlediği kazançları, kesintileri ve çalışan ücret planlarını ayarlamak ve bunları yönetmek için kullanılan araçları sağlar.</span><span class="sxs-lookup"><span data-stu-id="d818c-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="d818c-149">Kazançları oluştururken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="d818c-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="d818c-150">Kazanç planları</span><span class="sxs-lookup"><span data-stu-id="d818c-150">Benefit plans</span></span>

- <span data-ttu-id="d818c-151">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-151">Plan (required)</span></span>
- <span data-ttu-id="d818c-152">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-152">Type (required)</span></span>
- <span data-ttu-id="d818c-153">Bordro etkisi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-153">Payroll impact (required)</span></span>
- <span data-ttu-id="d818c-154">Borçları kurtar</span><span class="sxs-lookup"><span data-stu-id="d818c-154">Recover arrears</span></span>
- <span data-ttu-id="d818c-155">Kesinti yöntemi</span><span class="sxs-lookup"><span data-stu-id="d818c-155">Deduction method</span></span>
- <span data-ttu-id="d818c-156">Kesinti önceliği</span><span class="sxs-lookup"><span data-stu-id="d818c-156">Deduction priority</span></span>
- <span data-ttu-id="d818c-157">Dönemi sınırla</span><span class="sxs-lookup"><span data-stu-id="d818c-157">Limit period</span></span>
- <span data-ttu-id="d818c-158">Sınır tutar</span><span class="sxs-lookup"><span data-stu-id="d818c-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="d818c-159">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="d818c-159">Benefits</span></span>

- <span data-ttu-id="d818c-160">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-160">Plan (required)</span></span>
- <span data-ttu-id="d818c-161">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-161">Type (required)</span></span>
- <span data-ttu-id="d818c-162">Seçenek (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-162">Option (required)</span></span>
- <span data-ttu-id="d818c-163">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-163">Benefit ID (required)</span></span>
- <span data-ttu-id="d818c-164">Sıklık</span><span class="sxs-lookup"><span data-stu-id="d818c-164">Frequency</span></span>
- <span data-ttu-id="d818c-165">Temel</span><span class="sxs-lookup"><span data-stu-id="d818c-165">Basis</span></span>
- <span data-ttu-id="d818c-166">Tutar veya oran</span><span class="sxs-lookup"><span data-stu-id="d818c-166">Amount or rate</span></span>
- <span data-ttu-id="d818c-167">Kazanç kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="d818c-168">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="d818c-168">Supported frequencies</span></span> 

- <span data-ttu-id="d818c-169">Haftalık</span><span class="sxs-lookup"><span data-stu-id="d818c-169">Weekly</span></span>
- <span data-ttu-id="d818c-170">İki haftada bir</span><span class="sxs-lookup"><span data-stu-id="d818c-170">Bi-weekly</span></span>
- <span data-ttu-id="d818c-171">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="d818c-171">Semi-monthly</span></span>
- <span data-ttu-id="d818c-172">Aylık</span><span class="sxs-lookup"><span data-stu-id="d818c-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="d818c-173">Desteklenen tabanlar</span><span class="sxs-lookup"><span data-stu-id="d818c-173">Supported bases</span></span> 

- <span data-ttu-id="d818c-174">Sabit tutar</span><span class="sxs-lookup"><span data-stu-id="d818c-174">Fixed amount</span></span>
- <span data-ttu-id="d818c-175">Kazançların yüzdesi</span><span class="sxs-lookup"><span data-stu-id="d818c-175">Percent of earnings</span></span>
- <span data-ttu-id="d818c-176">Üretime yönelik saatler</span><span class="sxs-lookup"><span data-stu-id="d818c-176">Productive hours</span></span>

<span data-ttu-id="d818c-177">Dayforce, kazanç planında tanımlanan bordro etkisine göre aşağıdaki kesintileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d818c-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="d818c-178">Human Resources'ta seçim</span><span class="sxs-lookup"><span data-stu-id="d818c-178">Selection in Human Resources</span></span>        | <span data-ttu-id="d818c-179">Dayforce'ta sonuç</span><span class="sxs-lookup"><span data-stu-id="d818c-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d818c-180">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="d818c-180">None</span></span>                       | <span data-ttu-id="d818c-181">Kesinti oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="d818c-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="d818c-182">Yalnızca kesinti</span><span class="sxs-lookup"><span data-stu-id="d818c-182">Deduction only</span></span>             | <span data-ttu-id="d818c-183">Personel kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d818c-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="d818c-184">Yalnızca katkı</span><span class="sxs-lookup"><span data-stu-id="d818c-184">Contribution only</span></span>          | <span data-ttu-id="d818c-185">İşveren kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d818c-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="d818c-186">Kesinti ve katkı</span><span class="sxs-lookup"><span data-stu-id="d818c-186">Deduction and contribution</span></span> | <span data-ttu-id="d818c-187">Personel ve işveren kesintileri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d818c-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="d818c-188">Kazanç programı tanımlama ve yönetme hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="d818c-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="d818c-189">Personel kazançları programı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d818c-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="d818c-190">Yeni kazanç oluştur</span><span class="sxs-lookup"><span data-stu-id="d818c-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="d818c-191">Kazanç uygunluk kurallarını ve ilkelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="d818c-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="d818c-192">Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma</span><span class="sxs-lookup"><span data-stu-id="d818c-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="d818c-193">Ücret</span><span class="sxs-lookup"><span data-stu-id="d818c-193">Compensation</span></span> 

<span data-ttu-id="d818c-194">Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d818c-195">Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d818c-196">İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="d818c-197">Dayforce personelin saatlik veya yıllık ücretlerini hesaplamak için ücret bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d818c-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="d818c-198">Sabit ücret planları ve ödeme oranı dönüştürmeleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="d818c-199">Personelin bir sabit ücret planıyla ilişkilendirilmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="d818c-200">Ücret planları hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="d818c-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="d818c-201">Sabit ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="d818c-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="d818c-202">Değişken ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="d818c-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="d818c-203">Maaş/ücret yapısı ve planları geliştirme</span><span class="sxs-lookup"><span data-stu-id="d818c-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="d818c-204">İşlem ücreti</span><span class="sxs-lookup"><span data-stu-id="d818c-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="d818c-205">Ücret işlemini tanımlama ve sonuçları hesaplama</span><span class="sxs-lookup"><span data-stu-id="d818c-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="d818c-206">Personeli sabit ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="d818c-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="d818c-207">Personeli değişken ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="d818c-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="d818c-208">İşler</span><span class="sxs-lookup"><span data-stu-id="d818c-208">Jobs</span></span> 

<span data-ttu-id="d818c-209">Bir iş, işi gerçekleştiren kişiden beklenen görev ve sorumlulukların toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="d818c-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d818c-210">Daha fazla bilgi edinmek için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="d818c-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d818c-211">İşin bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="d818c-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="d818c-212">Yeni işler tanımlama</span><span class="sxs-lookup"><span data-stu-id="d818c-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="d818c-213">Pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="d818c-213">Positions</span></span>

<span data-ttu-id="d818c-214">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="d818c-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="d818c-215">Örneğin, "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş pozisyonlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="d818c-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="d818c-216">Bir pozisyon, bir departmanda bulunur.</span><span class="sxs-lookup"><span data-stu-id="d818c-216">A position exists in a department.</span></span> <span data-ttu-id="d818c-217">Her pozisyonla yalnızca bir çalışan ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="d818c-218">Pozisyonları ayarlarken aşağıdaki verileri ve yapılandırmayı göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="d818c-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="d818c-219">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-219">Position (required)</span></span>
- <span data-ttu-id="d818c-220">Açıklama (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-220">Description (required)</span></span>
- <span data-ttu-id="d818c-221">İş (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-221">Job (required)</span></span>
- <span data-ttu-id="d818c-222">Departman (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-222">Department (required)</span></span>
- <span data-ttu-id="d818c-223">Pozisyon türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-223">Position type (required)</span></span>
- <span data-ttu-id="d818c-224">Tam zamanlı eşdeğeri</span><span class="sxs-lookup"><span data-stu-id="d818c-224">Full-time equivalent</span></span>
- <span data-ttu-id="d818c-225">Yıllık mesai saatleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="d818c-226">Tüzel kişilik tarafından ödenen (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="d818c-227">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-227">Pay cycle (required)</span></span>
- <span data-ttu-id="d818c-228">Varsayılan mali boyut – Maliyet merkezi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="d818c-229">Çalışan ataması: Çalışan, atama başlangıç tarihi, atama bitiş tarihi, neden kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="d818c-230">Aynı departmanda birden fazla pozisyon aynı işle ilişkilendirilmişse bunlar Dayforce'ta tek bir pozisyonda konsolide edilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="d818c-231">Daha fazla bilgi edinmek için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="d818c-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d818c-232">Departmanlar, işler ve pozisyonları kullanarak iş gücünüzü düzenleme</span><span class="sxs-lookup"><span data-stu-id="d818c-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="d818c-233">Pozisyonları ayarlama</span><span class="sxs-lookup"><span data-stu-id="d818c-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="d818c-234">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="d818c-234">Departments</span></span>

<span data-ttu-id="d818c-235">Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir.</span><span class="sxs-lookup"><span data-stu-id="d818c-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d818c-236">Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur.</span><span class="sxs-lookup"><span data-stu-id="d818c-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d818c-237">İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d818c-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d818c-238">Departmanların kâr ve zarar sorumluluğu olabilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d818c-239">Daha fazla bilgi edinmek için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="d818c-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d818c-240">Departman oluşturma ve departman hiyerarşisi ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="d818c-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="d818c-241">Yeni departmanlar tanımlama</span><span class="sxs-lookup"><span data-stu-id="d818c-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="d818c-242">Ödeme döngüleri ve ödeme dönemleri</span><span class="sxs-lookup"><span data-stu-id="d818c-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="d818c-243">Ödeme döngüsü, bordronun ne sıklıkta çalıştırıldığını ve çalışanlara ödeme yapılan belirli günleri belirler.</span><span class="sxs-lookup"><span data-stu-id="d818c-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="d818c-244">Örneğin, bir ödeme döngüsü aylık olabilir ve personele ayın son günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="d818c-245">Alternatif olarak, bir ödeme döngüsü haftalık olabilir ve personele ödeme döneminin bitişinden sonraki Salı günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="d818c-246">Ödeme döngüleri, bu pozisyonlardaki çalışanlara ne zaman ödeme yapıldığını kontrol etmek için pozisyonlara atanır.</span><span class="sxs-lookup"><span data-stu-id="d818c-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="d818c-247">Ödeme döngülerini oluşturduktan sonra her döngü için ödeme dönemleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d818c-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="d818c-248">Her ödeme dönemi, sağladığınız bilgilere göre varsayılan bir ödeme tarihi içerir.</span><span class="sxs-lookup"><span data-stu-id="d818c-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="d818c-249">Ancak ödeme döneminin bir tatil gününe denk gelmesi gibi istisnalara izin vermek için ödeme döneminde varsayılan ödeme tarihini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d818c-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="d818c-250">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="d818c-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d818c-251">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-251">Pay cycle (required)</span></span>
- <span data-ttu-id="d818c-252">Ödeme döngüsü sıklığı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="d818c-253">Dönem başlangıç tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="d818c-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="d818c-254">Varsayılan ödeme tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="d818c-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="d818c-255">Bu bilgiler ödeme grupları olarak Dayforce ile tümleştirilir ve her ödeme döngüsü için ülke veya bölgeye göre ayrılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="d818c-256">Tümleştirmeden önce en az bir ödeme dönemi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d818c-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="d818c-257">Dayforce, ilk ödeme döneminin başlangıç tarihine ve Human Resources'ta ayarlanan varsayılan ödeme tarihine bağlı olarak ödeme grubu takvimlerini ve ödeme tarihlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d818c-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="d818c-258">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="d818c-258">Earning codes</span></span>

<span data-ttu-id="d818c-259">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d818c-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d818c-260">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametrelere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="d818c-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="d818c-261">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="d818c-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d818c-262">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-262">Earning Code (required)</span></span>
- <span data-ttu-id="d818c-263">Tanım</span><span class="sxs-lookup"><span data-stu-id="d818c-263">Description</span></span>
- <span data-ttu-id="d818c-264">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="d818c-264">Unit of measure</span></span>
- <span data-ttu-id="d818c-265">Üretken</span><span class="sxs-lookup"><span data-stu-id="d818c-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="d818c-266">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="d818c-266">Worker data</span></span>

<span data-ttu-id="d818c-267">Sahip olduğunuz çeşitli çalışan türlerine ilişkin kayıtlar, insan kaynaklarınız ve bordro sistemleriniz için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="d818c-268">Girdiğiniz bilgiler çalışanları ve kişisel bilgileri izlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="d818c-269">Çalışanlar hakkında aşağıdaki bilgileri koruyabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d818c-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="d818c-270">**Temel**: İletişim bilgileri, demografik bilgiler, kimlik bilgileri, aile bilgileri, askerlik hizmeti durumu, göçmenlik bilgileri ile kişisel ve acil durum iletişim kişileri gibi temel bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="d818c-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="d818c-271">**İstihdam**: Şirket veya kuruluş ilişkisi, pozisyon ataması, başlangıç ve bitiş tarihleri, iş uygunluğu, istihdam koşulları, emeklilik, tatil ve tayin bilgileri gibi bir çalışanın istihdamıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="d818c-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="d818c-272">**İzin ve devamsızlık**: Çalışma takvimleri, devamsızlık işlemleri ve devamsızlık ayarı gibi bir çalışanın devamsızlığıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="d818c-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="d818c-273">**Ücret ve bordro**: Plan kaydı, ödüller, performans, komisyon, vergi bilgileri, emeklilik ve maaş kesintileri gibi bir çalışanın ücret planlarıyla ilgili bilgileri ve bordro bilgilerini tutun.</span><span class="sxs-lookup"><span data-stu-id="d818c-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="d818c-274">Çalışan bilgilerini girerken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="d818c-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="d818c-275">Genel bilgiler</span><span class="sxs-lookup"><span data-stu-id="d818c-275">General information</span></span>

- <span data-ttu-id="d818c-276">Personel numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-276">Personnel number (required)</span></span>
- <span data-ttu-id="d818c-277">Ad (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-277">First name (required)</span></span>
- <span data-ttu-id="d818c-278">Soyadı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-278">Last name (required)</span></span>
- <span data-ttu-id="d818c-279">İkinci adı</span><span class="sxs-lookup"><span data-stu-id="d818c-279">Middle name</span></span>
- <span data-ttu-id="d818c-280">Kıdem tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-280">Seniority date</span></span>
- <span data-ttu-id="d818c-281">Bilinen hali</span><span class="sxs-lookup"><span data-stu-id="d818c-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="d818c-282">Kişisel bilgiler</span><span class="sxs-lookup"><span data-stu-id="d818c-282">Personal information</span></span>

- <span data-ttu-id="d818c-283">Medeni durum (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-283">Marital status (required)</span></span>
- <span data-ttu-id="d818c-284">Doğum tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-284">Birth date (required)</span></span>
- <span data-ttu-id="d818c-285">Cinsiyet (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-285">Gender (required)</span></span>
- <span data-ttu-id="d818c-286">Engelli kişi</span><span class="sxs-lookup"><span data-stu-id="d818c-286">Person with disabilities</span></span>
- <span data-ttu-id="d818c-287">Uyruğu ülkesi bölgesi (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="d818c-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="d818c-288">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="d818c-288">Address information</span></span>

- <span data-ttu-id="d818c-289">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-289">Primary (required)</span></span>
- <span data-ttu-id="d818c-290">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-290">Country/region (required)</span></span>
- <span data-ttu-id="d818c-291">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-291">Postal code (required)</span></span>
- <span data-ttu-id="d818c-292">Cadde Numarası (gerekli) (Yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="d818c-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="d818c-293">Bina Tamamlayıcı (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="d818c-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="d818c-294">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-294">City (required)</span></span>
- <span data-ttu-id="d818c-295">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-295">State (required)</span></span>
- <span data-ttu-id="d818c-296">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="d818c-297">İletişim bilgileri</span><span class="sxs-lookup"><span data-stu-id="d818c-297">Contact information</span></span> 

- <span data-ttu-id="d818c-298">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-298">Primary (required)</span></span>
- <span data-ttu-id="d818c-299">İlgili kişi numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-299">Contact number (required)</span></span>
- <span data-ttu-id="d818c-300">Dahili</span><span class="sxs-lookup"><span data-stu-id="d818c-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="d818c-301">Bordro bilgileri ve kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="d818c-301">Payroll information and earning codes</span></span>

<span data-ttu-id="d818c-302">Personele belirli bir ödeme sıklığında özel kazançlar atanabilir ve çalışanlar, tercih edilen bir ödeme yöntemine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="d818c-303">Bu tercihlerin ve ayarların kullanıldığının sağlanmasına yardımcı olmak için Dayforce'ta aşağıdaki alanlar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="d818c-304">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="d818c-304">Earning codes</span></span>

- <span data-ttu-id="d818c-305">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-305">Position (required)</span></span>
- <span data-ttu-id="d818c-306">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-306">Earning Code (required)</span></span>
- <span data-ttu-id="d818c-307">Sıklık (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-307">Frequency (required)</span></span>
- <span data-ttu-id="d818c-308">Tutar (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="d818c-309">Bordro bilgileri</span><span class="sxs-lookup"><span data-stu-id="d818c-309">Payroll information</span></span>

- <span data-ttu-id="d818c-310">Ödeme Yöntemi</span><span class="sxs-lookup"><span data-stu-id="d818c-310">Payment Method</span></span>
- <span data-ttu-id="d818c-311">Ekonomik Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-311">Economic Region (required)</span></span>
- <span data-ttu-id="d818c-312">Personel Kazanç Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-312">Employee Benefits ID</span></span>
- <span data-ttu-id="d818c-313">Ulusal Kimlik Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-313">National ID Number (required)</span></span>
- <span data-ttu-id="d818c-314">Askerlik Hizmet Numarası</span><span class="sxs-lookup"><span data-stu-id="d818c-314">Military Service Number</span></span>
- <span data-ttu-id="d818c-315">Vardiya Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-315">Shift ID (required)</span></span>
- <span data-ttu-id="d818c-316">Vergi Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-316">Tax Number (required)</span></span>
- <span data-ttu-id="d818c-317">Sendika Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-317">Union ID (required)</span></span>
- <span data-ttu-id="d818c-318">İş Günü Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-318">Work Day ID (required)</span></span>
- <span data-ttu-id="d818c-319">Çalışma İzni Numarası</span><span class="sxs-lookup"><span data-stu-id="d818c-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="d818c-320">Meksika'da ödeme yöntemleri olarak **Nakit**, **Çek** (şirketin fiziksel çeki) ve **Elektronik Ödeme** desteklenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="d818c-321">Hiçbir ödeme yöntemi belirtilmemişse varsayılan olarak **Çek** kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="d818c-322">İstihdam ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="d818c-322">Employment details</span></span>

<span data-ttu-id="d818c-323">İstihdam ayrıntıları geçmişi, personelin Dayforce'ta işe alma, işten çıkarma ve yeniden işe alma durumlarını oluşturmada temel bilgi olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="d818c-324">Dayforce, bir defada yalnızca bir etkin istihdam kaydını destekler.</span><span class="sxs-lookup"><span data-stu-id="d818c-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="d818c-325">İşe başlama tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-325">Employment start date (required)</span></span>
- <span data-ttu-id="d818c-326">İş bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-326">Employment end date</span></span>
- <span data-ttu-id="d818c-327">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-327">Start date</span></span>
- <span data-ttu-id="d818c-328">Ayarlanan başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-328">Adjusted start date</span></span>
- <span data-ttu-id="d818c-329">İşten çıkarma tarihi (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="d818c-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="d818c-330">İşten çıkarma nedeni (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="d818c-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="d818c-331">Personelin önemli tarihleri aşağıdaki bilgiler kullanılarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="d818c-332">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-332">Human Resources</span></span>                | <span data-ttu-id="d818c-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d818c-334">En son işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-334">Most recent hire date</span></span> | <span data-ttu-id="d818c-335">Geçerli sonlandırılmamış işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="d818c-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d818c-336">İşten çıkarma tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-336">Termination date</span></span>      | <span data-ttu-id="d818c-337">Geçerli sonlandırılmamış işten çıkış tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="d818c-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d818c-338">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-338">Start date</span></span>            | <span data-ttu-id="d818c-339">Ayarlanan başlama tarihi, başlama tarihi veya geçerli etkin olmayan işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="d818c-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="d818c-340">Orijinal işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-340">Original hire date</span></span>    | <span data-ttu-id="d818c-341">En erken işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="d818c-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="d818c-342">Ücret</span><span class="sxs-lookup"><span data-stu-id="d818c-342">Compensation</span></span>

<span data-ttu-id="d818c-343">Bir istihdam dönemi boyunca her personelin birincil pozisyonu ile sabit ücret planı ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="d818c-344">Bu dönem personelin işe alındığı (veya işe başlama tarihi) tarihte başlar ve işten çıkış tarihine kadar devam eder.</span><span class="sxs-lookup"><span data-stu-id="d818c-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="d818c-345">Yürürlük Tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-345">Effective Date (required)</span></span>
- <span data-ttu-id="d818c-346">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-346">Expiration date</span></span>
- <span data-ttu-id="d818c-347">Ödeme Oranı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-347">Pay Rate (required)</span></span>
- <span data-ttu-id="d818c-348">Ödeme Oranı Dönüştürmeleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="d818c-349">Yıllık eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="d818c-350">Saatlik eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="d818c-351">Saatlik personelin birden fazla pozisyonu varsa birincil pozisyonun sabit ücreti, personel düzeyinde taban oranı/maaş olarak Dayforce'ta içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="d818c-352">Birincil olmayan pozisyonlar için saatlik oran Dayforce'ta ilgili pozisyona kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="d818c-353">Maaşlı personelin birden fazla pozisyonu varsa tüm etkin pozisyonlar için kümülatif saat oranı ve yıllık maaş oluşturulur ve personel düzeyinde taban oranı/maaş olarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="d818c-354">Kimlik numaraları</span><span class="sxs-lookup"><span data-stu-id="d818c-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="d818c-355">Sosyal Güvenlik Kimlik Tanımlayıcı</span><span class="sxs-lookup"><span data-stu-id="d818c-355">Social Security identifier</span></span> 

<span data-ttu-id="d818c-356">Her personelin bir birincil kimlik tanımlayıcısı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="d818c-357">Bu kimlik tanımlayıcı **SSK** kimlik türünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d818c-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="d818c-358">Dayforce'ta bu, personelin işe alınması için gereken Sosyal Güvenlik kimlik tanımlayıcı olarak otomatik türetilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="d818c-359">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-359">Primary (required)</span></span>
- <span data-ttu-id="d818c-360">Kimlik Türü = "SSN"</span><span class="sxs-lookup"><span data-stu-id="d818c-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="d818c-361">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="d818c-361">Issued Date</span></span>
- <span data-ttu-id="d818c-362">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-362">Expiration Date</span></span>

<span data-ttu-id="d818c-363">Personel, **SSN** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="d818c-364">Ancak numaranın etkin veya süresinin dolmuş olup olmadığına bakılmaksızın yalnızca **Birincil** olarak işaretlenen kayıt Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="d818c-365">Banka hesapları ve tahsilatlar</span><span class="sxs-lookup"><span data-stu-id="d818c-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="d818c-366">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel için geçerli banka hesap bilgileri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="d818c-367">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-367">Human Resources</span></span>                         | <span data-ttu-id="d818c-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d818c-369">Banka hesap numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="d818c-370">SWIFT kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-370">SWIFT code (required)</span></span>          | <span data-ttu-id="d818c-371">Meksika'da bordro işlemleri için **Banka Kodu** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="d818c-372">Şube numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="d818c-373">Banka hesabı türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-373">Bank account type (required)</span></span>   | <span data-ttu-id="d818c-374">Meksika'da bordro işlemleri için **Hesap türü** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="d818c-375">Desteklenen değerler **Cari** ve **Bordro**'yu içerir.</span><span class="sxs-lookup"><span data-stu-id="d818c-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="d818c-376">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel, birincil adresi Meksika'da olan ve bir Meksika bankasındaki geçerli bir banka hesabıyla ilişkilendirilmiş tüzel kişilik altında bulunan bir bakiye hesabına bağlantı sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="d818c-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="d818c-377">Bakiye hesabı olmayan diğer hesaplar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="d818c-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="d818c-378">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="d818c-378">Address information</span></span>

<span data-ttu-id="d818c-379">Her personelin bir birincil konumu olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-379">Every employee must have one primary location.</span></span> <span data-ttu-id="d818c-380">Dayforce'ta bu konum, personelin vergiye esas birincil ikamet yerini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="d818c-381">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-381">Primary (required)</span></span>
- <span data-ttu-id="d818c-382">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-382">Country/region (required)</span></span>
- <span data-ttu-id="d818c-383">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="d818c-384">Cadde (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-384">Street (required)</span></span>
- <span data-ttu-id="d818c-385">Cadde Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-385">Street Number (required)</span></span>
- <span data-ttu-id="d818c-386">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="d818c-386">Building Complement</span></span>
- <span data-ttu-id="d818c-387">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-387">City (required)</span></span>
- <span data-ttu-id="d818c-388">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-388">State (required)</span></span>
- <span data-ttu-id="d818c-389">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="d818c-390">Amerika Birleşik Devletleri ve Kanada’da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d818c-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="d818c-391">Amerika Birleşik Devletleri ve Kanada’daki personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="d818c-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="d818c-392">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-392">Departments are required on positions.</span></span>
- <span data-ttu-id="d818c-393">Maliyet merkezleri mali boyut olarak ayarlanmalı ve varsayılan mali boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d818c-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="d818c-394">Human Resources'ı Pozisyonların bir Departman belirtmesini zorunlu kılacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d818c-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="d818c-395">Bunu yapmak için **İnsan Kaynakları Paylaşılan Pozisyonlar > Pozisyonlar > Pozisyonlarda departmanlar gerektir**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d818c-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="d818c-396">Bu ayarın tümleştirme için zorunlu olmasını öneririz.</span><span class="sxs-lookup"><span data-stu-id="d818c-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="d818c-397">İş türleri</span><span class="sxs-lookup"><span data-stu-id="d818c-397">Job types</span></span>

<span data-ttu-id="d818c-398">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d818c-399">Amerika Birleşik Devletleri ve Kanada'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="d818c-400">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="d818c-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d818c-401">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d818c-402">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d818c-403">İş türü</span><span class="sxs-lookup"><span data-stu-id="d818c-403">Job type</span></span>   | <span data-ttu-id="d818c-404">Tanım</span><span class="sxs-lookup"><span data-stu-id="d818c-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d818c-405">Saatlik</span><span class="sxs-lookup"><span data-stu-id="d818c-405">Hourly</span></span>     | <span data-ttu-id="d818c-406">Saatlik</span><span class="sxs-lookup"><span data-stu-id="d818c-406">Hourly</span></span>      |
| <span data-ttu-id="d818c-407">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="d818c-407">Salaried</span></span>   | <span data-ttu-id="d818c-408">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="d818c-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="d818c-409">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="d818c-409">Position types</span></span> 

<span data-ttu-id="d818c-410">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="d818c-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d818c-411">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d818c-412">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d818c-413">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="d818c-413">Position type</span></span>   | <span data-ttu-id="d818c-414">Tanım</span><span class="sxs-lookup"><span data-stu-id="d818c-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d818c-415">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="d818c-415">Full-time</span></span>       | <span data-ttu-id="d818c-416">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="d818c-416">Full time employee</span></span> |
| <span data-ttu-id="d818c-417">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="d818c-417">Part-time</span></span>       | <span data-ttu-id="d818c-418">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="d818c-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d818c-419">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="d818c-419">Reason codes</span></span>

<span data-ttu-id="d818c-420">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="d818c-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d818c-421">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d818c-422">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d818c-423">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-423">Reason code</span></span>    | <span data-ttu-id="d818c-424">Tanım</span><span class="sxs-lookup"><span data-stu-id="d818c-424">Description</span></span>      | <span data-ttu-id="d818c-425">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="d818c-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="d818c-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d818c-426">RESIGNATION</span></span>    | <span data-ttu-id="d818c-427">İstifa</span><span class="sxs-lookup"><span data-stu-id="d818c-427">Resignation</span></span>      | <span data-ttu-id="d818c-428">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-428">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d818c-429">TERMINATION</span></span>    | <span data-ttu-id="d818c-430">Bitiş</span><span class="sxs-lookup"><span data-stu-id="d818c-430">Termination</span></span>      | <span data-ttu-id="d818c-431">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-431">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d818c-432">RETIREMENT</span></span>     | <span data-ttu-id="d818c-433">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="d818c-433">Retirement</span></span>       | <span data-ttu-id="d818c-434">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-434">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-435">OTHER</span><span class="sxs-lookup"><span data-stu-id="d818c-435">OTHER</span></span>          | <span data-ttu-id="d818c-436">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="d818c-436">Other Reasons</span></span>    | <span data-ttu-id="d818c-437">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-437">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="d818c-438">DEATH</span></span>          | <span data-ttu-id="d818c-439">Ölüm</span><span class="sxs-lookup"><span data-stu-id="d818c-439">Death</span></span>            | <span data-ttu-id="d818c-440">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-440">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d818c-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="d818c-442">İzin</span><span class="sxs-lookup"><span data-stu-id="d818c-442">Leave of Absence</span></span> | <span data-ttu-id="d818c-443">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-443">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d818c-444">CONTRACTEND</span></span>    | <span data-ttu-id="d818c-445">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="d818c-445">End of Contract</span></span>  | <span data-ttu-id="d818c-446">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-446">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d818c-447">SALARYCHANGE</span></span>   | <span data-ttu-id="d818c-448">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="d818c-448">Change of Salary</span></span> | <span data-ttu-id="d818c-449">Ücret</span><span class="sxs-lookup"><span data-stu-id="d818c-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="d818c-450">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="d818c-450">Marital status</span></span>

<span data-ttu-id="d818c-451">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="d818c-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d818c-452">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d818c-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d818c-453">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-453">Human Resources</span></span>                 | <span data-ttu-id="d818c-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="d818c-455">Evli</span><span class="sxs-lookup"><span data-stu-id="d818c-455">Married</span></span>                | <span data-ttu-id="d818c-456">Evli</span><span class="sxs-lookup"><span data-stu-id="d818c-456">Married</span></span>              |
| <span data-ttu-id="d818c-457">Tekli</span><span class="sxs-lookup"><span data-stu-id="d818c-457">Single</span></span>                 | <span data-ttu-id="d818c-458">Tekli</span><span class="sxs-lookup"><span data-stu-id="d818c-458">Single</span></span>               |
| <span data-ttu-id="d818c-459">Dul</span><span class="sxs-lookup"><span data-stu-id="d818c-459">Widowed</span></span>                | <span data-ttu-id="d818c-460">Dul</span><span class="sxs-lookup"><span data-stu-id="d818c-460">Widowed</span></span>              |
| <span data-ttu-id="d818c-461">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="d818c-461">Divorced</span></span>               | <span data-ttu-id="d818c-462">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="d818c-462">Divorced</span></span>             |
| <span data-ttu-id="d818c-463">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="d818c-463">Registered Partnership</span></span> | <span data-ttu-id="d818c-464">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="d818c-464">Domestic Partnership</span></span> |
| <span data-ttu-id="d818c-465">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="d818c-465">None</span></span>                   | <span data-ttu-id="d818c-466">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="d818c-466">None</span></span>                 |
| <span data-ttu-id="d818c-467">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="d818c-467">Cohabiting</span></span>             | <span data-ttu-id="d818c-468">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="d818c-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="d818c-469">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="d818c-469">Gender</span></span>

<span data-ttu-id="d818c-470">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="d818c-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d818c-471">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d818c-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d818c-472">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-472">Human Resources</span></span>       | <span data-ttu-id="d818c-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="d818c-474">Erkek</span><span class="sxs-lookup"><span data-stu-id="d818c-474">Male</span></span>         | <span data-ttu-id="d818c-475">Erkek</span><span class="sxs-lookup"><span data-stu-id="d818c-475">Male</span></span>            |
| <span data-ttu-id="d818c-476">Kadın</span><span class="sxs-lookup"><span data-stu-id="d818c-476">Female</span></span>       | <span data-ttu-id="d818c-477">Kadın</span><span class="sxs-lookup"><span data-stu-id="d818c-477">Female</span></span>          |
| <span data-ttu-id="d818c-478">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="d818c-478">Non-specific</span></span> | <span data-ttu-id="d818c-479">*Desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d818c-480">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="d818c-480">Earning codes</span></span>

<span data-ttu-id="d818c-481">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d818c-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d818c-482">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="d818c-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d818c-483">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d818c-484">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="d818c-484">Supported frequencies</span></span>

- <span data-ttu-id="d818c-485">Tümü</span><span class="sxs-lookup"><span data-stu-id="d818c-485">All</span></span>
- <span data-ttu-id="d818c-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d818c-486">EVERYPAY</span></span>
- <span data-ttu-id="d818c-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d818c-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d818c-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d818c-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d818c-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d818c-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d818c-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-490">1OFMTH</span></span>
- <span data-ttu-id="d818c-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-491">LASTOFMTH</span></span>
- <span data-ttu-id="d818c-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-492">2OFMTH</span></span>
- <span data-ttu-id="d818c-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-493">3OFMTH</span></span>
- <span data-ttu-id="d818c-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-494">4OFMTH</span></span>
- <span data-ttu-id="d818c-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-495">5OFMTH</span></span>
- <span data-ttu-id="d818c-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-496">1N2OFMTH</span></span>
- <span data-ttu-id="d818c-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-497">3N4OFMTH</span></span>
- <span data-ttu-id="d818c-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-498">1N3OFMTH</span></span>
- <span data-ttu-id="d818c-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-499">1N4OFMTH</span></span>
- <span data-ttu-id="d818c-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-500">2N3OFMTH</span></span>
- <span data-ttu-id="d818c-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-501">2N4OFMTH</span></span>
- <span data-ttu-id="d818c-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="d818c-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="d818c-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="d818c-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="d818c-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d818c-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d818c-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d818c-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d818c-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d818c-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d818c-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d818c-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d818c-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d818c-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d818c-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d818c-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d818c-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d818c-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d818c-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d818c-514">Adresler</span><span class="sxs-lookup"><span data-stu-id="d818c-514">Addresses</span></span>

<span data-ttu-id="d818c-515">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d818c-516">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d818c-517">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-517">Human Resources</span></span>          | <span data-ttu-id="d818c-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="d818c-519">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="d818c-519">Country/Region</span></span>  | <span data-ttu-id="d818c-520">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-520">Country Code</span></span>          |
| <span data-ttu-id="d818c-521">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-521">Zip/Postal Code</span></span> | <span data-ttu-id="d818c-522">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-522">Postal Code</span></span>           |
| <span data-ttu-id="d818c-523">İl</span><span class="sxs-lookup"><span data-stu-id="d818c-523">State</span></span>           | <span data-ttu-id="d818c-524">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-524">State Code</span></span>            |
| <span data-ttu-id="d818c-525">Şehir</span><span class="sxs-lookup"><span data-stu-id="d818c-525">City</span></span>            | <span data-ttu-id="d818c-526">Şehir</span><span class="sxs-lookup"><span data-stu-id="d818c-526">City</span></span>                  |
| <span data-ttu-id="d818c-527">İlçe</span><span class="sxs-lookup"><span data-stu-id="d818c-527">County</span></span>          | <span data-ttu-id="d818c-528">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="d818c-528">County (Municipality)</span></span> |
| <span data-ttu-id="d818c-529">Sokak</span><span class="sxs-lookup"><span data-stu-id="d818c-529">Street</span></span>          | <span data-ttu-id="d818c-530">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="d818c-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="d818c-531">Vergi bölgeleri</span><span class="sxs-lookup"><span data-stu-id="d818c-531">Tax regions</span></span>

<span data-ttu-id="d818c-532">Vergi bölgeleri, bordro oluşturma sırasında uygulanması gereken uygun vergiyi belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="d818c-533">Vergi bölgeleri, Dayforce'a konum adresleri olarak eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="d818c-534">Varsayılan vergi bölgesi, çalışanın etkin konumuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="d818c-535">Vergi bölgesi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-535">Tax region (required)</span></span>
- <span data-ttu-id="d818c-536">Ülke/Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-536">Country/Region (required)</span></span>
- <span data-ttu-id="d818c-537">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-537">State (required)</span></span>
- <span data-ttu-id="d818c-538">İlçe</span><span class="sxs-lookup"><span data-stu-id="d818c-538">County</span></span> 
- <span data-ttu-id="d818c-539">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="d818c-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="d818c-540">Meksika'da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d818c-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="d818c-541">Meksika'da personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="d818c-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="d818c-542">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-542">Departments are required on positions.</span></span>
- <span data-ttu-id="d818c-543">Maliyet merkezleri mali boyut olarak ayarlanmalı ve Varsayılan Mali Boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d818c-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="d818c-544">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="d818c-544">Job types</span></span>

<span data-ttu-id="d818c-545">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d818c-546">Meksika'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="d818c-547">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="d818c-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d818c-548">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d818c-549">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d818c-550">İş türü</span><span class="sxs-lookup"><span data-stu-id="d818c-550">Job type</span></span>   | <span data-ttu-id="d818c-551">Tanım</span><span class="sxs-lookup"><span data-stu-id="d818c-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d818c-552">Saatlik</span><span class="sxs-lookup"><span data-stu-id="d818c-552">Hourly</span></span>     | <span data-ttu-id="d818c-553">MX Saatlik</span><span class="sxs-lookup"><span data-stu-id="d818c-553">MX Hourly</span></span>   |
| <span data-ttu-id="d818c-554">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="d818c-554">Salaried</span></span>   | <span data-ttu-id="d818c-555">MX Maaşlı</span><span class="sxs-lookup"><span data-stu-id="d818c-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="d818c-556">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="d818c-556">Position types</span></span> 

<span data-ttu-id="d818c-557">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="d818c-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d818c-558">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d818c-559">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d818c-560">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="d818c-560">Position type</span></span>   | <span data-ttu-id="d818c-561">Tanım</span><span class="sxs-lookup"><span data-stu-id="d818c-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d818c-562">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="d818c-562">Full-time</span></span>       | <span data-ttu-id="d818c-563">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="d818c-563">Full time employee</span></span> |
| <span data-ttu-id="d818c-564">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="d818c-564">Part-time</span></span>       | <span data-ttu-id="d818c-565">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="d818c-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d818c-566">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="d818c-566">Reason codes</span></span>

<span data-ttu-id="d818c-567">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="d818c-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d818c-568">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d818c-569">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d818c-570">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-570">Reason code</span></span>            | <span data-ttu-id="d818c-571">Tanım</span><span class="sxs-lookup"><span data-stu-id="d818c-571">Description</span></span>                    | <span data-ttu-id="d818c-572">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="d818c-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="d818c-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="d818c-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="d818c-574">İlk bordrodan önce ayrılma</span><span class="sxs-lookup"><span data-stu-id="d818c-574">Departure before first payroll</span></span> | <span data-ttu-id="d818c-575">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-575">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d818c-576">RESIGNATION</span></span>            | <span data-ttu-id="d818c-577">İstifa</span><span class="sxs-lookup"><span data-stu-id="d818c-577">Resignation</span></span>                    | <span data-ttu-id="d818c-578">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-578">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="d818c-579">PENSION</span></span>                | <span data-ttu-id="d818c-580">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="d818c-580">Pension</span></span>                        | <span data-ttu-id="d818c-581">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-581">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d818c-582">TERMINATION</span></span>            | <span data-ttu-id="d818c-583">Bitiş</span><span class="sxs-lookup"><span data-stu-id="d818c-583">Termination</span></span>                    | <span data-ttu-id="d818c-584">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-584">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d818c-585">RETIREMENT</span></span>             | <span data-ttu-id="d818c-586">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="d818c-586">Retirement</span></span>                     | <span data-ttu-id="d818c-587">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-587">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="d818c-588">ABSENTEE</span></span>               | <span data-ttu-id="d818c-589">Devamsızlık</span><span class="sxs-lookup"><span data-stu-id="d818c-589">Absentee</span></span>                       | <span data-ttu-id="d818c-590">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-590">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-591">OTHER</span><span class="sxs-lookup"><span data-stu-id="d818c-591">OTHER</span></span>                  | <span data-ttu-id="d818c-592">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="d818c-592">Other Reasons</span></span>                  | <span data-ttu-id="d818c-593">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-593">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="d818c-594">CLOSURE</span></span>                | <span data-ttu-id="d818c-595">İşletmenin Kapanması</span><span class="sxs-lookup"><span data-stu-id="d818c-595">Business Closure</span></span>               | <span data-ttu-id="d818c-596">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-596">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="d818c-597">DEATH</span></span>                  | <span data-ttu-id="d818c-598">Ölüm</span><span class="sxs-lookup"><span data-stu-id="d818c-598">Death</span></span>                          | <span data-ttu-id="d818c-599">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-599">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d818c-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="d818c-601">İzin</span><span class="sxs-lookup"><span data-stu-id="d818c-601">Leave of Absence</span></span>               | <span data-ttu-id="d818c-602">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-602">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d818c-603">CONTRACTEND</span></span>            | <span data-ttu-id="d818c-604">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="d818c-604">End of Contract</span></span>                | <span data-ttu-id="d818c-605">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="d818c-605">Terminate worker</span></span>     |
| <span data-ttu-id="d818c-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d818c-606">SALARYCHANGE</span></span>           | <span data-ttu-id="d818c-607">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="d818c-607">Change of Salary</span></span>               | <span data-ttu-id="d818c-608">Ücret</span><span class="sxs-lookup"><span data-stu-id="d818c-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="d818c-609">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="d818c-609">Terms of employment</span></span>

<span data-ttu-id="d818c-610">İstihdam koşulları, istihdam koşullarının kategorilerini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="d818c-611">Koşullar, istihdam göstergesi değerleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="d818c-612">Aşağıdaki istihdam koşulları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="d818c-613">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="d818c-613">Terms of employment</span></span>   | <span data-ttu-id="d818c-614">Tanım</span><span class="sxs-lookup"><span data-stu-id="d818c-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d818c-615">Normal</span><span class="sxs-lookup"><span data-stu-id="d818c-615">Regular</span></span>               | <span data-ttu-id="d818c-616">Normal</span><span class="sxs-lookup"><span data-stu-id="d818c-616">Regular</span></span>     |
| <span data-ttu-id="d818c-617">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="d818c-617">Direct</span></span>                | <span data-ttu-id="d818c-618">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="d818c-618">Direct</span></span>      |
| <span data-ttu-id="d818c-619">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="d818c-619">Internship</span></span>            | <span data-ttu-id="d818c-620">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="d818c-620">Internship</span></span>  |
| <span data-ttu-id="d818c-621">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="d818c-621">Permanent</span></span>             | <span data-ttu-id="d818c-622">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="d818c-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="d818c-623">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="d818c-623">Marital status</span></span>

<span data-ttu-id="d818c-624">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="d818c-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d818c-625">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d818c-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d818c-626">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-626">Human Resources</span></span>                 | <span data-ttu-id="d818c-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="d818c-628">Evli</span><span class="sxs-lookup"><span data-stu-id="d818c-628">Married</span></span>                | <span data-ttu-id="d818c-629">Evli</span><span class="sxs-lookup"><span data-stu-id="d818c-629">Married</span></span>                   |
| <span data-ttu-id="d818c-630">Tekli</span><span class="sxs-lookup"><span data-stu-id="d818c-630">Single</span></span>                 | <span data-ttu-id="d818c-631">Tekli</span><span class="sxs-lookup"><span data-stu-id="d818c-631">Single</span></span>                    |
| <span data-ttu-id="d818c-632">Dul</span><span class="sxs-lookup"><span data-stu-id="d818c-632">Widowed</span></span>                | <span data-ttu-id="d818c-633">Dul</span><span class="sxs-lookup"><span data-stu-id="d818c-633">Widowed</span></span>                   |
| <span data-ttu-id="d818c-634">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="d818c-634">Divorced</span></span>               | <span data-ttu-id="d818c-635">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="d818c-635">Divorced</span></span>                  |
| <span data-ttu-id="d818c-636">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="d818c-636">Registered Partnership</span></span> | <span data-ttu-id="d818c-637">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="d818c-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="d818c-638">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="d818c-638">None</span></span>                   | <span data-ttu-id="d818c-639">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d818c-640">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="d818c-640">Cohabiting</span></span>             | <span data-ttu-id="d818c-641">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="d818c-642">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="d818c-642">Gender</span></span>

<span data-ttu-id="d818c-643">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="d818c-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d818c-644">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d818c-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d818c-645">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-645">Human Resources</span></span>       | <span data-ttu-id="d818c-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="d818c-647">Erkek</span><span class="sxs-lookup"><span data-stu-id="d818c-647">Male</span></span>         | <span data-ttu-id="d818c-648">Erkek</span><span class="sxs-lookup"><span data-stu-id="d818c-648">Male</span></span>                      |
| <span data-ttu-id="d818c-649">Kadın</span><span class="sxs-lookup"><span data-stu-id="d818c-649">Female</span></span>       | <span data-ttu-id="d818c-650">Kadın</span><span class="sxs-lookup"><span data-stu-id="d818c-650">Female</span></span>                    |
| <span data-ttu-id="d818c-651">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="d818c-651">Non-specific</span></span> | <span data-ttu-id="d818c-652">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="d818c-653">Ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="d818c-653">Payment method</span></span>

<span data-ttu-id="d818c-654">Ödeme yöntemleri, personele ve şirkete çalışanlara nasıl ödeme yapılacağını tanımlamak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="d818c-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="d818c-655">Ödeme yöntemleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="d818c-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d818c-656">Aşağıdaki tabloda ödeme yöntemlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d818c-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="d818c-657">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-657">Human Resources</span></span>             | <span data-ttu-id="d818c-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="d818c-659">Nakit</span><span class="sxs-lookup"><span data-stu-id="d818c-659">Cash</span></span>               | <span data-ttu-id="d818c-660">Nakit</span><span class="sxs-lookup"><span data-stu-id="d818c-660">Cash</span></span>                      |
| <span data-ttu-id="d818c-661">Elektronik Ödeme</span><span class="sxs-lookup"><span data-stu-id="d818c-661">Electronic Payment</span></span> | <span data-ttu-id="d818c-662">Transfer et</span><span class="sxs-lookup"><span data-stu-id="d818c-662">Transfer</span></span>                  |
| <span data-ttu-id="d818c-663">Denetle</span><span class="sxs-lookup"><span data-stu-id="d818c-663">Check</span></span>              | <span data-ttu-id="d818c-664">Çek</span><span class="sxs-lookup"><span data-stu-id="d818c-664">Cheque</span></span>                    |
| <span data-ttu-id="d818c-665">Banka Ödeme Emri</span><span class="sxs-lookup"><span data-stu-id="d818c-665">Bank Draft</span></span>         | <span data-ttu-id="d818c-666">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d818c-667">Diğer</span><span class="sxs-lookup"><span data-stu-id="d818c-667">Other</span></span>              | <span data-ttu-id="d818c-668">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="d818c-669">Banka hesabı türü</span><span class="sxs-lookup"><span data-stu-id="d818c-669">Bank account type</span></span>

<span data-ttu-id="d818c-670">Banka hesap türleri, personele elektronik ödeme yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="d818c-671">Banka hesap türleri, transfer hesabı bilgileri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="d818c-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="d818c-672">Banka hesap türleri, uygunsa tümleştirme işleminden sonra kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="d818c-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="d818c-673">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-673">Human Resources</span></span>            | <span data-ttu-id="d818c-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="d818c-675">Cari Hesap</span><span class="sxs-lookup"><span data-stu-id="d818c-675">Checking Account</span></span>  | <span data-ttu-id="d818c-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="d818c-676">CheckingAccount</span></span>           |
| <span data-ttu-id="d818c-677">Bordro Hesabı</span><span class="sxs-lookup"><span data-stu-id="d818c-677">Payroll Account</span></span>   | <span data-ttu-id="d818c-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="d818c-678">PayrollAccount</span></span>            |
| <span data-ttu-id="d818c-679">Tasarruf Hesabı</span><span class="sxs-lookup"><span data-stu-id="d818c-679">Savings Account</span></span>   | <span data-ttu-id="d818c-680">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d818c-681">BankGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="d818c-681">BankGirot account</span></span> | <span data-ttu-id="d818c-682">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d818c-683">PlusGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="d818c-683">PlusGirot account</span></span> | <span data-ttu-id="d818c-684">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="d818c-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d818c-685">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="d818c-685">Earning codes</span></span>

<span data-ttu-id="d818c-686">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d818c-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d818c-687">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="d818c-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d818c-688">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d818c-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d818c-689">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="d818c-689">Supported frequencies</span></span>

- <span data-ttu-id="d818c-690">Tümü</span><span class="sxs-lookup"><span data-stu-id="d818c-690">All</span></span>
- <span data-ttu-id="d818c-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d818c-691">EVERYPAY</span></span>
- <span data-ttu-id="d818c-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d818c-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d818c-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d818c-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d818c-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d818c-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d818c-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-695">1OFMTH</span></span>
- <span data-ttu-id="d818c-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-696">LASTOFMTH</span></span>
- <span data-ttu-id="d818c-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-697">2OFMTH</span></span>
- <span data-ttu-id="d818c-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-698">3OFMTH</span></span>
- <span data-ttu-id="d818c-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-699">4OFMTH</span></span>
- <span data-ttu-id="d818c-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-700">5OFMTH</span></span>
- <span data-ttu-id="d818c-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-701">1N2OFMTH</span></span>
- <span data-ttu-id="d818c-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-702">3N4OFMTH</span></span>
- <span data-ttu-id="d818c-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-703">1N3OFMTH</span></span>
- <span data-ttu-id="d818c-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-704">1N4OFMTH</span></span>
- <span data-ttu-id="d818c-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-705">2N3OFMTH</span></span>
- <span data-ttu-id="d818c-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-706">2N4OFMTH</span></span>
- <span data-ttu-id="d818c-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="d818c-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="d818c-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="d818c-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="d818c-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d818c-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d818c-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d818c-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d818c-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d818c-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d818c-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d818c-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d818c-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d818c-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d818c-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d818c-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d818c-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d818c-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d818c-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d818c-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d818c-719">Adresler</span><span class="sxs-lookup"><span data-stu-id="d818c-719">Addresses</span></span>

<span data-ttu-id="d818c-720">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="d818c-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d818c-721">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d818c-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d818c-722">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="d818c-722">Human Resources</span></span>              | <span data-ttu-id="d818c-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d818c-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="d818c-724">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="d818c-724">Country/Region</span></span>      | <span data-ttu-id="d818c-725">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-725">Country Code</span></span>          |
| <span data-ttu-id="d818c-726">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-726">Zip/Postal Code</span></span>     | <span data-ttu-id="d818c-727">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-727">Postal Code</span></span>           |
| <span data-ttu-id="d818c-728">İl</span><span class="sxs-lookup"><span data-stu-id="d818c-728">State</span></span>               | <span data-ttu-id="d818c-729">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="d818c-729">State Code</span></span>            |
| <span data-ttu-id="d818c-730">Şehir</span><span class="sxs-lookup"><span data-stu-id="d818c-730">City</span></span>                | <span data-ttu-id="d818c-731">Şehir</span><span class="sxs-lookup"><span data-stu-id="d818c-731">City</span></span>                  |
| <span data-ttu-id="d818c-732">İlçe</span><span class="sxs-lookup"><span data-stu-id="d818c-732">County</span></span>              | <span data-ttu-id="d818c-733">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="d818c-733">County (Municipality)</span></span> |
| <span data-ttu-id="d818c-734">Sokak</span><span class="sxs-lookup"><span data-stu-id="d818c-734">Street</span></span>              | <span data-ttu-id="d818c-735">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="d818c-735">Address Line 1</span></span>        |
| <span data-ttu-id="d818c-736">Cadde Numarası</span><span class="sxs-lookup"><span data-stu-id="d818c-736">Street Number</span></span>       | <span data-ttu-id="d818c-737">Adres Satırı 2</span><span class="sxs-lookup"><span data-stu-id="d818c-737">Address Line 2</span></span>        |
| <span data-ttu-id="d818c-738">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="d818c-738">Building Complement</span></span> | <span data-ttu-id="d818c-739">Adres Satırı 5</span><span class="sxs-lookup"><span data-stu-id="d818c-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="d818c-740">Pasaport numarası</span><span class="sxs-lookup"><span data-stu-id="d818c-740">Passport number</span></span>

<span data-ttu-id="d818c-741">Personel pasaport bilgilerini bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-741">Employees can declare passport information.</span></span> <span data-ttu-id="d818c-742">Bu bilgiler, **Pasaport** kimlik türünü içerir ve Meksika'ya özel personel bilgilerinin bir parçası olarak Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="d818c-743">Kimlik Türü = "Pasaport"</span><span class="sxs-lookup"><span data-stu-id="d818c-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="d818c-744">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="d818c-744">Issued Date</span></span>
- <span data-ttu-id="d818c-745">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="d818c-745">Expiration Date</span></span>

<span data-ttu-id="d818c-746">Personel, **Pasaport** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="d818c-747">Ancak yalnızca geçerli etkin pasaport girişi Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="d818c-748">Tüm pasaport girişlerinin süresi dolmuşsa en son verilen pasaport Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d818c-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
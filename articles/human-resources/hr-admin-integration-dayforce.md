---
title: Dayforce ile tümleştirme yapılandırma
description: Microsoft Dynamics 365 Human Resources ile Ceridian Dayforce arasındaki tümleştirme, bu makalede açıklanan çeşitli yapılandırma adımlarına dayanır. Ödeme işlemini işlemeden önce tümleştirmeyi hem Human Resources'ta hem de Dayforce'ta yapılandırmanız gerekir.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c66ec772ea66732e042f50081f04a6569852f211
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420861"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="30a7f-104">Dayforce ile tümleştirme yapılandırma</span><span class="sxs-lookup"><span data-stu-id="30a7f-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="30a7f-105">Microsoft Dynamics 365 Human Resources ile Ceridian Dayforce arasındaki tümleştirme, bu makalede açıklanan çeşitli yapılandırma adımlarına dayanır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="30a7f-106">Ödeme işlemini işlemeden önce tümleştirmeyi hem Human Resources'ta hem de Dayforce'ta yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="30a7f-107">Ödeme işlemlerini tamamlamak için Dayforce gibi bir hizmet kullandığınızda tümleştirmeyi Human Resources'ta etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="30a7f-108">Tümleştirme için Human Resources'tan özel veriler gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="30a7f-109">Bu nedenle, Dayforce ile eşlenmiş verilerin Human Resources'ta tümleştirmeyi destekleyecek şekilde yapılandırıldığını doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="30a7f-110">Tümleştirme, aşağıdaki geniş veri kategorilerini kullanır:</span><span class="sxs-lookup"><span data-stu-id="30a7f-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="30a7f-111">İnsan kaynakları verileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-111">Human resources data</span></span>
- <span data-ttu-id="30a7f-112">Ücret verileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-112">Compensation data</span></span>
- <span data-ttu-id="30a7f-113">Ödeme döngüleri, ödeme dönemleri ve kazanç kodları gibi bordro verileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="30a7f-114">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-114">Worker data</span></span>

<span data-ttu-id="30a7f-115">Bu makalede, tümleştirmeyi etkinleştirmek için izlemeniz gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="30a7f-116">Ayrıca veri türleri ve tümleştirmenin gerektirdiği yapılandırma ayrıntıları da açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="30a7f-117">Tümleştirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="30a7f-117">Enable the integration</span></span>

<span data-ttu-id="30a7f-118">Human Resources'ta yapılandırmayı açmanız ve Dayforce'a bağlanmak için yapılandırma bilgilerini girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="30a7f-119">Microsoft Dynamics 365 Finance'a aktarılmak üzere oluşturulan genel muhasebe hareketini istiyorsanız ayrıca bir Microsoft Azure depolama hesabı oluşturmanız ve Finance'ta Azure Depolama bağlantı dizesini de girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="30a7f-120">Human Resources'ta tümleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30a7f-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="30a7f-121">**Sistem yönetimi** sayfasında **Tümleştirme yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="30a7f-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="30a7f-122">Güvenli Dosya Aktarım Protokolü (FTP) uç noktasını ve güvenli FTP klasörü yolunu girin.</span><span class="sxs-lookup"><span data-stu-id="30a7f-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="30a7f-123">Güvenli FTP uç noktasına ve klasör yoluna erişecek kullanıcının kullanıcı adını ve parolasını girin.</span><span class="sxs-lookup"><span data-stu-id="30a7f-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="30a7f-124">Bağlantıyı gerektiği gibi test edin ve **Bordro tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="30a7f-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="30a7f-125">Tümleştirme açıldığında veri dışa aktarma paketi ve dosyalar oluşturulur ve sıklık ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="30a7f-126">Bu sıklığı ihtiyaç duyduğunuz şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30a7f-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="30a7f-127">Azure depolama hesapları ve Azure Depolama bağlantı dizeleri hakkında daha fazla bilgi için aşağıdaki Azure makalelerine bakın:</span><span class="sxs-lookup"><span data-stu-id="30a7f-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="30a7f-128">Azure depolama hesapları hakkında</span><span class="sxs-lookup"><span data-stu-id="30a7f-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="30a7f-129">Azure Depolama bağlantı dizelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="30a7f-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="30a7f-130">Bordro tümleştirmesinin etkinleştirilmesinin teknik ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="30a7f-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="30a7f-131">Bordro tümleştirmesinin açılmasının iki temel etkisi vardır:</span><span class="sxs-lookup"><span data-stu-id="30a7f-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="30a7f-132">"Bordro tümleştirmesini dışa aktar" adlı dışa veri aktarma projesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="30a7f-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="30a7f-133">Bu proje, bordro tümleştirmesi için gerekli olan varlıkları ve alanları içerir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="30a7f-134">Projeyi incelemek için **Sistem yönetimi**'ne gidin, **Veri yönetimi** kutucuğunu seçin ve ardından projeler listesinden veri projesini açın.</span><span class="sxs-lookup"><span data-stu-id="30a7f-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="30a7f-135">Bu toplu iş, veri dışa aktarma projesini yürütür, sonuçta elde edilen veri paketini şifreler ve veri paketi dosyasını **Tümleştirme Yapılandırması** ekranında yapılandırılan SFTP son noktasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="30a7f-136">SFTP son noktasına aktarılan veri paketi, pakette benzersiz bir anahtar kullanılarak şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="30a7f-137">Anahtar yalnızca Ceridian tarafından erişilebilen bir Azure Key Vault'ta yer alır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="30a7f-138">Veri paketi içeriğinin şifresini çözmek ve içeriği incelemek mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="30a7f-139">Veri paketinin içeriğini incelemeniz gerekiyorsa "Bordro tümleştirmesini dışa aktar" veri projesini el ile dışa aktarmanız, indirmeniz ve sonra açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="30a7f-140">El ile dışa aktarmada şifreleme uygulanmaz veya paket transfer edilmez.</span><span class="sxs-lookup"><span data-stu-id="30a7f-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="30a7f-141">Verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="30a7f-141">Configure your data</span></span> 

<span data-ttu-id="30a7f-142">Bordro işlemek için Human Resources'ta insan kaynağı verilerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="30a7f-143">Kazanç ve ücret bilgileriyle birlikte işler ve pozisyonlar gibi kurumsal verileri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="30a7f-144">Bu bilgiler personel ödemesi oluşturmak için gerekli olan istihdam, ödeme ve kesinti bilgilerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="30a7f-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="30a7f-145">İnsan kaynağı verileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="30a7f-146">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="30a7f-146">Benefits</span></span> 

<span data-ttu-id="30a7f-147">İnsan kaynakları, bir kuruluşun çalışanları için sunduğu veya işlediği kazançları, kesintileri ve çalışan ücret planlarını ayarlamak ve bunları yönetmek için kullanılan araçları sağlar.</span><span class="sxs-lookup"><span data-stu-id="30a7f-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="30a7f-148">Kazançları oluştururken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="30a7f-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="30a7f-149">Kazanç planları</span><span class="sxs-lookup"><span data-stu-id="30a7f-149">Benefit plans</span></span>

- <span data-ttu-id="30a7f-150">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-150">Plan (required)</span></span>
- <span data-ttu-id="30a7f-151">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-151">Type (required)</span></span>
- <span data-ttu-id="30a7f-152">Bordro etkisi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-152">Payroll impact (required)</span></span>
- <span data-ttu-id="30a7f-153">Borçları kurtar</span><span class="sxs-lookup"><span data-stu-id="30a7f-153">Recover arrears</span></span>
- <span data-ttu-id="30a7f-154">Kesinti yöntemi</span><span class="sxs-lookup"><span data-stu-id="30a7f-154">Deduction method</span></span>
- <span data-ttu-id="30a7f-155">Kesinti önceliği</span><span class="sxs-lookup"><span data-stu-id="30a7f-155">Deduction priority</span></span>
- <span data-ttu-id="30a7f-156">Dönemi sınırla</span><span class="sxs-lookup"><span data-stu-id="30a7f-156">Limit period</span></span>
- <span data-ttu-id="30a7f-157">Sınır tutar</span><span class="sxs-lookup"><span data-stu-id="30a7f-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="30a7f-158">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="30a7f-158">Benefits</span></span>

- <span data-ttu-id="30a7f-159">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-159">Plan (required)</span></span>
- <span data-ttu-id="30a7f-160">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-160">Type (required)</span></span>
- <span data-ttu-id="30a7f-161">Seçenek (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-161">Option (required)</span></span>
- <span data-ttu-id="30a7f-162">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-162">Benefit ID (required)</span></span>
- <span data-ttu-id="30a7f-163">Sıklık</span><span class="sxs-lookup"><span data-stu-id="30a7f-163">Frequency</span></span>
- <span data-ttu-id="30a7f-164">Temel</span><span class="sxs-lookup"><span data-stu-id="30a7f-164">Basis</span></span>
- <span data-ttu-id="30a7f-165">Tutar veya oran</span><span class="sxs-lookup"><span data-stu-id="30a7f-165">Amount or rate</span></span>
- <span data-ttu-id="30a7f-166">Kazanç kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="30a7f-167">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="30a7f-167">Supported frequencies</span></span> 

- <span data-ttu-id="30a7f-168">Haftalık</span><span class="sxs-lookup"><span data-stu-id="30a7f-168">Weekly</span></span>
- <span data-ttu-id="30a7f-169">İki haftada bir</span><span class="sxs-lookup"><span data-stu-id="30a7f-169">Bi-weekly</span></span>
- <span data-ttu-id="30a7f-170">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="30a7f-170">Semi-monthly</span></span>
- <span data-ttu-id="30a7f-171">Aylık</span><span class="sxs-lookup"><span data-stu-id="30a7f-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="30a7f-172">Desteklenen tabanlar</span><span class="sxs-lookup"><span data-stu-id="30a7f-172">Supported bases</span></span> 

- <span data-ttu-id="30a7f-173">Sabit tutar</span><span class="sxs-lookup"><span data-stu-id="30a7f-173">Fixed amount</span></span>
- <span data-ttu-id="30a7f-174">Kazançların yüzdesi</span><span class="sxs-lookup"><span data-stu-id="30a7f-174">Percent of earnings</span></span>
- <span data-ttu-id="30a7f-175">Üretime yönelik saatler</span><span class="sxs-lookup"><span data-stu-id="30a7f-175">Productive hours</span></span>

<span data-ttu-id="30a7f-176">Dayforce, kazanç planında tanımlanan bordro etkisine göre aşağıdaki kesintileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30a7f-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="30a7f-177">Human Resources'ta seçim</span><span class="sxs-lookup"><span data-stu-id="30a7f-177">Selection in Human Resources</span></span>        | <span data-ttu-id="30a7f-178">Dayforce'ta sonuç</span><span class="sxs-lookup"><span data-stu-id="30a7f-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="30a7f-179">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="30a7f-179">None</span></span>                       | <span data-ttu-id="30a7f-180">Kesinti oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="30a7f-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="30a7f-181">Yalnızca kesinti</span><span class="sxs-lookup"><span data-stu-id="30a7f-181">Deduction only</span></span>             | <span data-ttu-id="30a7f-182">Personel kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="30a7f-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="30a7f-183">Yalnızca katkı</span><span class="sxs-lookup"><span data-stu-id="30a7f-183">Contribution only</span></span>          | <span data-ttu-id="30a7f-184">İşveren kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="30a7f-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="30a7f-185">Kesinti ve katkı</span><span class="sxs-lookup"><span data-stu-id="30a7f-185">Deduction and contribution</span></span> | <span data-ttu-id="30a7f-186">Personel ve işveren kesintileri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="30a7f-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="30a7f-187">Kazanç programı tanımlama ve yönetme hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="30a7f-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="30a7f-188">Personel kazançları programı oluşturma</span><span class="sxs-lookup"><span data-stu-id="30a7f-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="30a7f-189">Yeni kazanç oluştur</span><span class="sxs-lookup"><span data-stu-id="30a7f-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="30a7f-190">Kazanç uygunluk kurallarını ve ilkelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="30a7f-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="30a7f-191">Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma</span><span class="sxs-lookup"><span data-stu-id="30a7f-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="30a7f-192">Ücret</span><span class="sxs-lookup"><span data-stu-id="30a7f-192">Compensation</span></span> 

<span data-ttu-id="30a7f-193">Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="30a7f-194">Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="30a7f-195">İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="30a7f-196">Dayforce personelin saatlik veya yıllık ücretlerini hesaplamak için ücret bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="30a7f-197">Sabit ücret planları ve ödeme oranı dönüştürmeleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="30a7f-198">Personelin bir sabit ücret planıyla ilişkilendirilmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="30a7f-199">Ücret planları hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="30a7f-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="30a7f-200">Sabit ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="30a7f-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="30a7f-201">Değişken ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="30a7f-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="30a7f-202">Maaş/ücret yapısı ve planları geliştirme</span><span class="sxs-lookup"><span data-stu-id="30a7f-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="30a7f-203">İşlem ücreti</span><span class="sxs-lookup"><span data-stu-id="30a7f-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="30a7f-204">Ücret işlemini tanımlama ve sonuçları hesaplama</span><span class="sxs-lookup"><span data-stu-id="30a7f-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="30a7f-205">Personeli sabit ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="30a7f-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="30a7f-206">Personeli değişken ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="30a7f-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="30a7f-207">İşler</span><span class="sxs-lookup"><span data-stu-id="30a7f-207">Jobs</span></span> 

<span data-ttu-id="30a7f-208">Bir iş, işi gerçekleştiren kişiden beklenen görev ve sorumlulukların toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="30a7f-209">Daha fazla bilgi edinmek için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="30a7f-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="30a7f-210">İşin bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="30a7f-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="30a7f-211">Yeni işler tanımlama</span><span class="sxs-lookup"><span data-stu-id="30a7f-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="30a7f-212">Pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="30a7f-212">Positions</span></span>

<span data-ttu-id="30a7f-213">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="30a7f-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="30a7f-214">Örneğin, "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş pozisyonlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="30a7f-215">Bir pozisyon, bir departmanda bulunur.</span><span class="sxs-lookup"><span data-stu-id="30a7f-215">A position exists in a department.</span></span> <span data-ttu-id="30a7f-216">Her pozisyonla yalnızca bir çalışan ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="30a7f-217">Pozisyonları ayarlarken aşağıdaki verileri ve yapılandırmayı göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="30a7f-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="30a7f-218">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-218">Position (required)</span></span>
- <span data-ttu-id="30a7f-219">Açıklama (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-219">Description (required)</span></span>
- <span data-ttu-id="30a7f-220">İş (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-220">Job (required)</span></span>
- <span data-ttu-id="30a7f-221">Departman (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-221">Department (required)</span></span>
- <span data-ttu-id="30a7f-222">Pozisyon türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-222">Position type (required)</span></span>
- <span data-ttu-id="30a7f-223">Tam zamanlı eşdeğeri</span><span class="sxs-lookup"><span data-stu-id="30a7f-223">Full-time equivalent</span></span>
- <span data-ttu-id="30a7f-224">Yıllık mesai saatleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="30a7f-225">Tüzel kişilik tarafından ödenen (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="30a7f-226">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-226">Pay cycle (required)</span></span>
- <span data-ttu-id="30a7f-227">Varsayılan mali boyut – Maliyet merkezi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="30a7f-228">Çalışan ataması: Çalışan, atama başlangıç tarihi, atama bitiş tarihi, neden kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="30a7f-229">Aynı departmanda birden fazla pozisyon aynı işle ilişkilendirilmişse bunlar Dayforce'ta tek bir pozisyonda konsolide edilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="30a7f-230">Daha fazla bilgi edinmek için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="30a7f-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="30a7f-231">Departmanlar, işler ve pozisyonları kullanarak iş gücünüzü düzenleme</span><span class="sxs-lookup"><span data-stu-id="30a7f-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="30a7f-232">Pozisyonları ayarlama</span><span class="sxs-lookup"><span data-stu-id="30a7f-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="30a7f-233">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="30a7f-233">Departments</span></span>

<span data-ttu-id="30a7f-234">Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="30a7f-235">Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur.</span><span class="sxs-lookup"><span data-stu-id="30a7f-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="30a7f-236">İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30a7f-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="30a7f-237">Departmanların kâr ve zarar sorumluluğu olabilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="30a7f-238">Daha fazla bilgi edinmek için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="30a7f-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="30a7f-239">Departman oluşturma ve departman hiyerarşisi ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="30a7f-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="30a7f-240">Yeni departmanlar tanımlama</span><span class="sxs-lookup"><span data-stu-id="30a7f-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="30a7f-241">Ödeme döngüleri ve ödeme dönemleri</span><span class="sxs-lookup"><span data-stu-id="30a7f-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="30a7f-242">Ödeme döngüsü, bordronun ne sıklıkta çalıştırıldığını ve çalışanlara ödeme yapılan belirli günleri belirler.</span><span class="sxs-lookup"><span data-stu-id="30a7f-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="30a7f-243">Örneğin, bir ödeme döngüsü aylık olabilir ve personele ayın son günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="30a7f-244">Alternatif olarak, bir ödeme döngüsü haftalık olabilir ve personele ödeme döneminin bitişinden sonraki Salı günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="30a7f-245">Ödeme döngüleri, bu pozisyonlardaki çalışanlara ne zaman ödeme yapıldığını kontrol etmek için pozisyonlara atanır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="30a7f-246">Ödeme döngülerini oluşturduktan sonra her döngü için ödeme dönemleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30a7f-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="30a7f-247">Her ödeme dönemi, sağladığınız bilgilere göre varsayılan bir ödeme tarihi içerir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="30a7f-248">Ancak ödeme döneminin bir tatil gününe denk gelmesi gibi istisnalara izin vermek için ödeme döneminde varsayılan ödeme tarihini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30a7f-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="30a7f-249">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="30a7f-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="30a7f-250">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-250">Pay cycle (required)</span></span>
- <span data-ttu-id="30a7f-251">Ödeme döngüsü sıklığı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="30a7f-252">Dönem başlangıç tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="30a7f-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="30a7f-253">Varsayılan ödeme tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="30a7f-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="30a7f-254">Bu bilgiler ödeme grupları olarak Dayforce ile tümleştirilir ve her ödeme döngüsü için ülke veya bölgeye göre ayrılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="30a7f-255">Tümleştirmeden önce en az bir ödeme dönemi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="30a7f-256">Dayforce, ilk ödeme döneminin başlangıç tarihine ve Human Resources'ta ayarlanan varsayılan ödeme tarihine bağlı olarak ödeme grubu takvimlerini ve ödeme tarihlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30a7f-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="30a7f-257">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="30a7f-257">Earning codes</span></span>

<span data-ttu-id="30a7f-258">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="30a7f-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="30a7f-259">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametrelere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="30a7f-260">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="30a7f-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="30a7f-261">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-261">Earning Code (required)</span></span>
- <span data-ttu-id="30a7f-262">Tanım</span><span class="sxs-lookup"><span data-stu-id="30a7f-262">Description</span></span>
- <span data-ttu-id="30a7f-263">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="30a7f-263">Unit of measure</span></span>
- <span data-ttu-id="30a7f-264">Üretken</span><span class="sxs-lookup"><span data-stu-id="30a7f-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="30a7f-265">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-265">Worker data</span></span>

<span data-ttu-id="30a7f-266">Sahip olduğunuz çeşitli çalışan türlerine ilişkin kayıtlar, insan kaynaklarınız ve bordro sistemleriniz için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="30a7f-267">Girdiğiniz bilgiler çalışanları ve kişisel bilgileri izlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="30a7f-268">Çalışanlar hakkında aşağıdaki bilgileri koruyabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="30a7f-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="30a7f-269">**Temel**: İletişim bilgileri, demografik bilgiler, kimlik bilgileri, aile bilgileri, askerlik hizmeti durumu, göçmenlik bilgileri ile kişisel ve acil durum iletişim kişileri gibi temel bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="30a7f-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="30a7f-270">**İstihdam**: Şirket veya kuruluş ilişkisi, pozisyon ataması, başlangıç ve bitiş tarihleri, iş uygunluğu, istihdam koşulları, emeklilik, tatil ve tayin bilgileri gibi bir çalışanın istihdamıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="30a7f-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="30a7f-271">**İzin ve devamsızlık**: Çalışma takvimleri, devamsızlık işlemleri ve devamsızlık ayarı gibi bir çalışanın devamsızlığıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="30a7f-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="30a7f-272">**Ücret ve bordro**: Plan kaydı, ödüller, performans, komisyon, vergi bilgileri, emeklilik ve maaş kesintileri gibi bir çalışanın ücret planlarıyla ilgili bilgileri ve bordro bilgilerini tutun.</span><span class="sxs-lookup"><span data-stu-id="30a7f-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="30a7f-273">Çalışan bilgilerini girerken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="30a7f-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="30a7f-274">Genel bilgiler</span><span class="sxs-lookup"><span data-stu-id="30a7f-274">General information</span></span>

- <span data-ttu-id="30a7f-275">Personel numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-275">Personnel number (required)</span></span>
- <span data-ttu-id="30a7f-276">Ad (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-276">First name (required)</span></span>
- <span data-ttu-id="30a7f-277">Soyadı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-277">Last name (required)</span></span>
- <span data-ttu-id="30a7f-278">İkinci adı</span><span class="sxs-lookup"><span data-stu-id="30a7f-278">Middle name</span></span>
- <span data-ttu-id="30a7f-279">Kıdem tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-279">Seniority date</span></span>
- <span data-ttu-id="30a7f-280">Bilinen hali</span><span class="sxs-lookup"><span data-stu-id="30a7f-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="30a7f-281">Kişisel bilgiler</span><span class="sxs-lookup"><span data-stu-id="30a7f-281">Personal information</span></span>

- <span data-ttu-id="30a7f-282">Medeni durum (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-282">Marital status (required)</span></span>
- <span data-ttu-id="30a7f-283">Doğum tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-283">Birth date (required)</span></span>
- <span data-ttu-id="30a7f-284">Cinsiyet (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-284">Gender (required)</span></span>
- <span data-ttu-id="30a7f-285">Engelli kişi</span><span class="sxs-lookup"><span data-stu-id="30a7f-285">Person with disabilities</span></span>
- <span data-ttu-id="30a7f-286">Uyruğu ülkesi bölgesi (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="30a7f-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="30a7f-287">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-287">Address information</span></span>

- <span data-ttu-id="30a7f-288">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-288">Primary (required)</span></span>
- <span data-ttu-id="30a7f-289">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-289">Country/region (required)</span></span>
- <span data-ttu-id="30a7f-290">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-290">Postal code (required)</span></span>
- <span data-ttu-id="30a7f-291">Cadde Numarası (gerekli) (Yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="30a7f-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="30a7f-292">Bina Tamamlayıcı (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="30a7f-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="30a7f-293">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-293">City (required)</span></span>
- <span data-ttu-id="30a7f-294">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-294">State (required)</span></span>
- <span data-ttu-id="30a7f-295">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="30a7f-296">İletişim bilgileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-296">Contact information</span></span> 

- <span data-ttu-id="30a7f-297">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-297">Primary (required)</span></span>
- <span data-ttu-id="30a7f-298">İlgili kişi numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-298">Contact number (required)</span></span>
- <span data-ttu-id="30a7f-299">Dahili</span><span class="sxs-lookup"><span data-stu-id="30a7f-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="30a7f-300">Bordro bilgileri ve kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="30a7f-300">Payroll information and earning codes</span></span>

<span data-ttu-id="30a7f-301">Personele belirli bir ödeme sıklığında özel kazançlar atanabilir ve çalışanlar, tercih edilen bir ödeme yöntemine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="30a7f-302">Bu tercihlerin ve ayarların kullanıldığının sağlanmasına yardımcı olmak için Dayforce'ta aşağıdaki alanlar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="30a7f-303">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="30a7f-303">Earning codes</span></span>

- <span data-ttu-id="30a7f-304">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-304">Position (required)</span></span>
- <span data-ttu-id="30a7f-305">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-305">Earning Code (required)</span></span>
- <span data-ttu-id="30a7f-306">Sıklık (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-306">Frequency (required)</span></span>
- <span data-ttu-id="30a7f-307">Tutar (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="30a7f-308">Bordro bilgileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-308">Payroll information</span></span>

- <span data-ttu-id="30a7f-309">Ödeme Yöntemi</span><span class="sxs-lookup"><span data-stu-id="30a7f-309">Payment Method</span></span>
- <span data-ttu-id="30a7f-310">Ekonomik Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-310">Economic Region (required)</span></span>
- <span data-ttu-id="30a7f-311">Personel Kazanç Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-311">Employee Benefits ID</span></span>
- <span data-ttu-id="30a7f-312">Ulusal Kimlik Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-312">National ID Number (required)</span></span>
- <span data-ttu-id="30a7f-313">Askerlik Hizmet Numarası</span><span class="sxs-lookup"><span data-stu-id="30a7f-313">Military Service Number</span></span>
- <span data-ttu-id="30a7f-314">Vardiya Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-314">Shift ID (required)</span></span>
- <span data-ttu-id="30a7f-315">Vergi Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-315">Tax Number (required)</span></span>
- <span data-ttu-id="30a7f-316">Sendika Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-316">Union ID (required)</span></span>
- <span data-ttu-id="30a7f-317">İş Günü Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-317">Work Day ID (required)</span></span>
- <span data-ttu-id="30a7f-318">Çalışma İzni Numarası</span><span class="sxs-lookup"><span data-stu-id="30a7f-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="30a7f-319">Meksika'da ödeme yöntemleri olarak **Nakit**, **Çek** (şirketin fiziksel çeki) ve **Elektronik Ödeme** desteklenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="30a7f-320">Hiçbir ödeme yöntemi belirtilmemişse varsayılan olarak **Çek** kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="30a7f-321">İstihdam ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="30a7f-321">Employment details</span></span>

<span data-ttu-id="30a7f-322">İstihdam ayrıntıları geçmişi, personelin Dayforce'ta işe alma, işten çıkarma ve yeniden işe alma durumlarını oluşturmada temel bilgi olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="30a7f-323">Dayforce, bir defada yalnızca bir etkin istihdam kaydını destekler.</span><span class="sxs-lookup"><span data-stu-id="30a7f-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="30a7f-324">İşe başlama tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-324">Employment start date (required)</span></span>
- <span data-ttu-id="30a7f-325">İş bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-325">Employment end date</span></span>
- <span data-ttu-id="30a7f-326">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-326">Start date</span></span>
- <span data-ttu-id="30a7f-327">Ayarlanan başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-327">Adjusted start date</span></span>
- <span data-ttu-id="30a7f-328">İşten çıkarma tarihi (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="30a7f-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="30a7f-329">İşten çıkarma nedeni (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="30a7f-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="30a7f-330">Personelin önemli tarihleri aşağıdaki bilgiler kullanılarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="30a7f-331">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-331">Human Resources</span></span>                | <span data-ttu-id="30a7f-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a7f-333">En son işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-333">Most recent hire date</span></span> | <span data-ttu-id="30a7f-334">Geçerli sonlandırılmamış işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="30a7f-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="30a7f-335">İşten çıkarma tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-335">Termination date</span></span>      | <span data-ttu-id="30a7f-336">Geçerli sonlandırılmamış işten çıkış tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="30a7f-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="30a7f-337">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-337">Start date</span></span>            | <span data-ttu-id="30a7f-338">Ayarlanan başlama tarihi, başlama tarihi veya geçerli etkin olmayan işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="30a7f-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="30a7f-339">Orijinal işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-339">Original hire date</span></span>    | <span data-ttu-id="30a7f-340">En erken işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="30a7f-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="30a7f-341">Ücret</span><span class="sxs-lookup"><span data-stu-id="30a7f-341">Compensation</span></span>

<span data-ttu-id="30a7f-342">Bir istihdam dönemi boyunca her personelin birincil pozisyonu ile sabit ücret planı ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="30a7f-343">Bu dönem personelin işe alındığı (veya işe başlama tarihi) tarihte başlar ve işten çıkış tarihine kadar devam eder.</span><span class="sxs-lookup"><span data-stu-id="30a7f-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="30a7f-344">Yürürlük Tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-344">Effective Date (required)</span></span>
- <span data-ttu-id="30a7f-345">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-345">Expiration date</span></span>
- <span data-ttu-id="30a7f-346">Ödeme Oranı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-346">Pay Rate (required)</span></span>
- <span data-ttu-id="30a7f-347">Ödeme Oranı Dönüştürmeleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="30a7f-348">Yıllık eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="30a7f-349">Saatlik eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="30a7f-350">Saatlik personelin birden fazla pozisyonu varsa birincil pozisyonun sabit ücreti, personel düzeyinde taban oranı/maaş olarak Dayforce'ta içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="30a7f-351">Birincil olmayan pozisyonlar için saatlik oran Dayforce'ta ilgili pozisyona kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="30a7f-352">Maaşlı personelin birden fazla pozisyonu varsa tüm etkin pozisyonlar için kümülatif saat oranı ve yıllık maaş oluşturulur ve personel düzeyinde taban oranı/maaş olarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="30a7f-353">Kimlik numaraları</span><span class="sxs-lookup"><span data-stu-id="30a7f-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="30a7f-354">Sosyal Güvenlik Kimlik Tanımlayıcı</span><span class="sxs-lookup"><span data-stu-id="30a7f-354">Social Security identifier</span></span> 

<span data-ttu-id="30a7f-355">Her personelin bir birincil kimlik tanımlayıcısı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="30a7f-356">Bu kimlik tanımlayıcı **SSK** kimlik türünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="30a7f-357">Dayforce'ta bu, personelin işe alınması için gereken Sosyal Güvenlik kimlik tanımlayıcı olarak otomatik türetilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="30a7f-358">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-358">Primary (required)</span></span>
- <span data-ttu-id="30a7f-359">Kimlik Türü = "SSN"</span><span class="sxs-lookup"><span data-stu-id="30a7f-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="30a7f-360">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="30a7f-360">Issued Date</span></span>
- <span data-ttu-id="30a7f-361">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-361">Expiration Date</span></span>

<span data-ttu-id="30a7f-362">Personel, **SSN** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="30a7f-363">Ancak numaranın etkin veya süresinin dolmuş olup olmadığına bakılmaksızın yalnızca **Birincil** olarak işaretlenen kayıt Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="30a7f-364">Banka hesapları ve tahsilatlar</span><span class="sxs-lookup"><span data-stu-id="30a7f-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="30a7f-365">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel için geçerli banka hesap bilgileri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="30a7f-366">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-366">Human Resources</span></span>                         | <span data-ttu-id="30a7f-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a7f-368">Banka hesap numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="30a7f-369">SWIFT kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-369">SWIFT code (required)</span></span>          | <span data-ttu-id="30a7f-370">Meksika'da bordro işlemleri için **Banka Kodu** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="30a7f-371">Şube numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="30a7f-372">Banka hesabı türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-372">Bank account type (required)</span></span>   | <span data-ttu-id="30a7f-373">Meksika'da bordro işlemleri için **Hesap türü** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="30a7f-374">Desteklenen değerler **Cari** ve **Bordro**'yu içerir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="30a7f-375">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel, birincil adresi Meksika'da olan ve bir Meksika bankasındaki geçerli bir banka hesabıyla ilişkilendirilmiş tüzel kişilik altında bulunan bir bakiye hesabına bağlantı sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="30a7f-376">Bakiye hesabı olmayan diğer hesaplar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="30a7f-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="30a7f-377">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="30a7f-377">Address information</span></span>

<span data-ttu-id="30a7f-378">Her personelin bir birincil konumu olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-378">Every employee must have one primary location.</span></span> <span data-ttu-id="30a7f-379">Dayforce'ta bu konum, personelin vergiye esas birincil ikamet yerini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="30a7f-380">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-380">Primary (required)</span></span>
- <span data-ttu-id="30a7f-381">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-381">Country/region (required)</span></span>
- <span data-ttu-id="30a7f-382">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="30a7f-383">Cadde (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-383">Street (required)</span></span>
- <span data-ttu-id="30a7f-384">Cadde Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-384">Street Number (required)</span></span>
- <span data-ttu-id="30a7f-385">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="30a7f-385">Building Complement</span></span>
- <span data-ttu-id="30a7f-386">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-386">City (required)</span></span>
- <span data-ttu-id="30a7f-387">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-387">State (required)</span></span>
- <span data-ttu-id="30a7f-388">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="30a7f-389">Amerika Birleşik Devletleri ve Kanada’da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="30a7f-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="30a7f-390">Amerika Birleşik Devletleri ve Kanada’daki personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="30a7f-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="30a7f-391">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-391">Departments are required on positions.</span></span>
- <span data-ttu-id="30a7f-392">Maliyet merkezleri mali boyut olarak ayarlanmalı ve varsayılan mali boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="30a7f-393">Human Resources'ı Pozisyonların bir Departman belirtmesini zorunlu kılacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30a7f-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="30a7f-394">Bunu yapmak için **İnsan Kaynakları Paylaşılan Pozisyonlar > Pozisyonlar > Pozisyonlarda departmanlar gerektir**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="30a7f-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="30a7f-395">Bu ayarın tümleştirme için zorunlu olmasını öneririz.</span><span class="sxs-lookup"><span data-stu-id="30a7f-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="30a7f-396">İş türleri</span><span class="sxs-lookup"><span data-stu-id="30a7f-396">Job types</span></span>

<span data-ttu-id="30a7f-397">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="30a7f-398">Amerika Birleşik Devletleri ve Kanada'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="30a7f-399">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="30a7f-400">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="30a7f-401">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="30a7f-402">İş türü</span><span class="sxs-lookup"><span data-stu-id="30a7f-402">Job type</span></span>   | <span data-ttu-id="30a7f-403">Tanım</span><span class="sxs-lookup"><span data-stu-id="30a7f-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="30a7f-404">Saatlik</span><span class="sxs-lookup"><span data-stu-id="30a7f-404">Hourly</span></span>     | <span data-ttu-id="30a7f-405">Saatlik</span><span class="sxs-lookup"><span data-stu-id="30a7f-405">Hourly</span></span>      |
| <span data-ttu-id="30a7f-406">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="30a7f-406">Salaried</span></span>   | <span data-ttu-id="30a7f-407">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="30a7f-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="30a7f-408">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="30a7f-408">Position types</span></span> 

<span data-ttu-id="30a7f-409">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="30a7f-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="30a7f-410">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="30a7f-411">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="30a7f-412">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="30a7f-412">Position type</span></span>   | <span data-ttu-id="30a7f-413">Tanım</span><span class="sxs-lookup"><span data-stu-id="30a7f-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="30a7f-414">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="30a7f-414">Full-time</span></span>       | <span data-ttu-id="30a7f-415">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="30a7f-415">Full time employee</span></span> |
| <span data-ttu-id="30a7f-416">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="30a7f-416">Part-time</span></span>       | <span data-ttu-id="30a7f-417">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="30a7f-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="30a7f-418">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="30a7f-418">Reason codes</span></span>

<span data-ttu-id="30a7f-419">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="30a7f-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="30a7f-420">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="30a7f-421">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="30a7f-422">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-422">Reason code</span></span>    | <span data-ttu-id="30a7f-423">Tanım</span><span class="sxs-lookup"><span data-stu-id="30a7f-423">Description</span></span>      | <span data-ttu-id="30a7f-424">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="30a7f-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="30a7f-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="30a7f-425">RESIGNATION</span></span>    | <span data-ttu-id="30a7f-426">İstifa</span><span class="sxs-lookup"><span data-stu-id="30a7f-426">Resignation</span></span>      | <span data-ttu-id="30a7f-427">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-427">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="30a7f-428">TERMINATION</span></span>    | <span data-ttu-id="30a7f-429">Bitiş</span><span class="sxs-lookup"><span data-stu-id="30a7f-429">Termination</span></span>      | <span data-ttu-id="30a7f-430">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-430">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="30a7f-431">RETIREMENT</span></span>     | <span data-ttu-id="30a7f-432">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="30a7f-432">Retirement</span></span>       | <span data-ttu-id="30a7f-433">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-433">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-434">OTHER</span><span class="sxs-lookup"><span data-stu-id="30a7f-434">OTHER</span></span>          | <span data-ttu-id="30a7f-435">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="30a7f-435">Other Reasons</span></span>    | <span data-ttu-id="30a7f-436">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-436">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="30a7f-437">DEATH</span></span>          | <span data-ttu-id="30a7f-438">Ölüm</span><span class="sxs-lookup"><span data-stu-id="30a7f-438">Death</span></span>            | <span data-ttu-id="30a7f-439">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-439">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="30a7f-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="30a7f-441">İzin</span><span class="sxs-lookup"><span data-stu-id="30a7f-441">Leave of Absence</span></span> | <span data-ttu-id="30a7f-442">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-442">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="30a7f-443">CONTRACTEND</span></span>    | <span data-ttu-id="30a7f-444">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="30a7f-444">End of Contract</span></span>  | <span data-ttu-id="30a7f-445">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-445">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="30a7f-446">SALARYCHANGE</span></span>   | <span data-ttu-id="30a7f-447">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="30a7f-447">Change of Salary</span></span> | <span data-ttu-id="30a7f-448">Ücret</span><span class="sxs-lookup"><span data-stu-id="30a7f-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="30a7f-449">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="30a7f-449">Marital status</span></span>

<span data-ttu-id="30a7f-450">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="30a7f-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="30a7f-451">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="30a7f-452">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-452">Human Resources</span></span>                 | <span data-ttu-id="30a7f-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="30a7f-454">Evli</span><span class="sxs-lookup"><span data-stu-id="30a7f-454">Married</span></span>                | <span data-ttu-id="30a7f-455">Evli</span><span class="sxs-lookup"><span data-stu-id="30a7f-455">Married</span></span>              |
| <span data-ttu-id="30a7f-456">Tekli</span><span class="sxs-lookup"><span data-stu-id="30a7f-456">Single</span></span>                 | <span data-ttu-id="30a7f-457">Tekli</span><span class="sxs-lookup"><span data-stu-id="30a7f-457">Single</span></span>               |
| <span data-ttu-id="30a7f-458">Dul</span><span class="sxs-lookup"><span data-stu-id="30a7f-458">Widowed</span></span>                | <span data-ttu-id="30a7f-459">Dul</span><span class="sxs-lookup"><span data-stu-id="30a7f-459">Widowed</span></span>              |
| <span data-ttu-id="30a7f-460">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="30a7f-460">Divorced</span></span>               | <span data-ttu-id="30a7f-461">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="30a7f-461">Divorced</span></span>             |
| <span data-ttu-id="30a7f-462">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="30a7f-462">Registered Partnership</span></span> | <span data-ttu-id="30a7f-463">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="30a7f-463">Domestic Partnership</span></span> |
| <span data-ttu-id="30a7f-464">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="30a7f-464">None</span></span>                   | <span data-ttu-id="30a7f-465">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="30a7f-465">None</span></span>                 |
| <span data-ttu-id="30a7f-466">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="30a7f-466">Cohabiting</span></span>             | <span data-ttu-id="30a7f-467">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="30a7f-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="30a7f-468">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="30a7f-468">Gender</span></span>

<span data-ttu-id="30a7f-469">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="30a7f-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="30a7f-470">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="30a7f-471">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-471">Human Resources</span></span>       | <span data-ttu-id="30a7f-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="30a7f-473">Erkek</span><span class="sxs-lookup"><span data-stu-id="30a7f-473">Male</span></span>         | <span data-ttu-id="30a7f-474">Erkek</span><span class="sxs-lookup"><span data-stu-id="30a7f-474">Male</span></span>            |
| <span data-ttu-id="30a7f-475">Kadın</span><span class="sxs-lookup"><span data-stu-id="30a7f-475">Female</span></span>       | <span data-ttu-id="30a7f-476">Kadın</span><span class="sxs-lookup"><span data-stu-id="30a7f-476">Female</span></span>          |
| <span data-ttu-id="30a7f-477">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="30a7f-477">Non-specific</span></span> | <span data-ttu-id="30a7f-478">*Desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="30a7f-479">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="30a7f-479">Earning codes</span></span>

<span data-ttu-id="30a7f-480">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="30a7f-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="30a7f-481">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="30a7f-482">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="30a7f-483">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="30a7f-483">Supported frequencies</span></span>

- <span data-ttu-id="30a7f-484">Tümü</span><span class="sxs-lookup"><span data-stu-id="30a7f-484">All</span></span>
- <span data-ttu-id="30a7f-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="30a7f-485">EVERYPAY</span></span>
- <span data-ttu-id="30a7f-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="30a7f-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="30a7f-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="30a7f-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="30a7f-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="30a7f-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="30a7f-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-489">1OFMTH</span></span>
- <span data-ttu-id="30a7f-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-490">LASTOFMTH</span></span>
- <span data-ttu-id="30a7f-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-491">2OFMTH</span></span>
- <span data-ttu-id="30a7f-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-492">3OFMTH</span></span>
- <span data-ttu-id="30a7f-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-493">4OFMTH</span></span>
- <span data-ttu-id="30a7f-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-494">5OFMTH</span></span>
- <span data-ttu-id="30a7f-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-495">1N2OFMTH</span></span>
- <span data-ttu-id="30a7f-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-496">3N4OFMTH</span></span>
- <span data-ttu-id="30a7f-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-497">1N3OFMTH</span></span>
- <span data-ttu-id="30a7f-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-498">1N4OFMTH</span></span>
- <span data-ttu-id="30a7f-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-499">2N3OFMTH</span></span>
- <span data-ttu-id="30a7f-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-500">2N4OFMTH</span></span>
- <span data-ttu-id="30a7f-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="30a7f-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="30a7f-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="30a7f-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="30a7f-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="30a7f-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="30a7f-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="30a7f-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="30a7f-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="30a7f-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="30a7f-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="30a7f-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="30a7f-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="30a7f-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="30a7f-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="30a7f-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="30a7f-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="30a7f-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="30a7f-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="30a7f-513">Adresler</span><span class="sxs-lookup"><span data-stu-id="30a7f-513">Addresses</span></span>

<span data-ttu-id="30a7f-514">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="30a7f-515">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="30a7f-516">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-516">Human Resources</span></span>          | <span data-ttu-id="30a7f-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="30a7f-518">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="30a7f-518">Country/Region</span></span>  | <span data-ttu-id="30a7f-519">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-519">Country Code</span></span>          |
| <span data-ttu-id="30a7f-520">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-520">Zip/Postal Code</span></span> | <span data-ttu-id="30a7f-521">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-521">Postal Code</span></span>           |
| <span data-ttu-id="30a7f-522">İl</span><span class="sxs-lookup"><span data-stu-id="30a7f-522">State</span></span>           | <span data-ttu-id="30a7f-523">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-523">State Code</span></span>            |
| <span data-ttu-id="30a7f-524">Şehir</span><span class="sxs-lookup"><span data-stu-id="30a7f-524">City</span></span>            | <span data-ttu-id="30a7f-525">Şehir</span><span class="sxs-lookup"><span data-stu-id="30a7f-525">City</span></span>                  |
| <span data-ttu-id="30a7f-526">İlçe</span><span class="sxs-lookup"><span data-stu-id="30a7f-526">County</span></span>          | <span data-ttu-id="30a7f-527">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="30a7f-527">County (Municipality)</span></span> |
| <span data-ttu-id="30a7f-528">Sokak</span><span class="sxs-lookup"><span data-stu-id="30a7f-528">Street</span></span>          | <span data-ttu-id="30a7f-529">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="30a7f-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="30a7f-530">Vergi bölgeleri</span><span class="sxs-lookup"><span data-stu-id="30a7f-530">Tax regions</span></span>

<span data-ttu-id="30a7f-531">Vergi bölgeleri, bordro oluşturma sırasında uygulanması gereken uygun vergiyi belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="30a7f-532">Vergi bölgeleri, Dayforce'a konum adresleri olarak eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="30a7f-533">Varsayılan vergi bölgesi, çalışanın etkin konumuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="30a7f-534">Vergi bölgesi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-534">Tax region (required)</span></span>
- <span data-ttu-id="30a7f-535">Ülke/Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-535">Country/Region (required)</span></span>
- <span data-ttu-id="30a7f-536">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-536">State (required)</span></span>
- <span data-ttu-id="30a7f-537">İlçe</span><span class="sxs-lookup"><span data-stu-id="30a7f-537">County</span></span> 
- <span data-ttu-id="30a7f-538">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="30a7f-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="30a7f-539">Meksika'da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="30a7f-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="30a7f-540">Meksika'da personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="30a7f-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="30a7f-541">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-541">Departments are required on positions.</span></span>
- <span data-ttu-id="30a7f-542">Maliyet merkezleri mali boyut olarak ayarlanmalı ve Varsayılan Mali Boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="30a7f-543">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="30a7f-543">Job types</span></span>

<span data-ttu-id="30a7f-544">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="30a7f-545">Meksika'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="30a7f-546">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="30a7f-547">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="30a7f-548">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="30a7f-549">İş türü</span><span class="sxs-lookup"><span data-stu-id="30a7f-549">Job type</span></span>   | <span data-ttu-id="30a7f-550">Tanım</span><span class="sxs-lookup"><span data-stu-id="30a7f-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="30a7f-551">Saatlik</span><span class="sxs-lookup"><span data-stu-id="30a7f-551">Hourly</span></span>     | <span data-ttu-id="30a7f-552">MX Saatlik</span><span class="sxs-lookup"><span data-stu-id="30a7f-552">MX Hourly</span></span>   |
| <span data-ttu-id="30a7f-553">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="30a7f-553">Salaried</span></span>   | <span data-ttu-id="30a7f-554">MX Maaşlı</span><span class="sxs-lookup"><span data-stu-id="30a7f-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="30a7f-555">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="30a7f-555">Position types</span></span> 

<span data-ttu-id="30a7f-556">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="30a7f-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="30a7f-557">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="30a7f-558">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="30a7f-559">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="30a7f-559">Position type</span></span>   | <span data-ttu-id="30a7f-560">Tanım</span><span class="sxs-lookup"><span data-stu-id="30a7f-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="30a7f-561">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="30a7f-561">Full-time</span></span>       | <span data-ttu-id="30a7f-562">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="30a7f-562">Full time employee</span></span> |
| <span data-ttu-id="30a7f-563">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="30a7f-563">Part-time</span></span>       | <span data-ttu-id="30a7f-564">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="30a7f-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="30a7f-565">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="30a7f-565">Reason codes</span></span>

<span data-ttu-id="30a7f-566">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="30a7f-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="30a7f-567">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="30a7f-568">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="30a7f-569">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-569">Reason code</span></span>            | <span data-ttu-id="30a7f-570">Tanım</span><span class="sxs-lookup"><span data-stu-id="30a7f-570">Description</span></span>                    | <span data-ttu-id="30a7f-571">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="30a7f-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="30a7f-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="30a7f-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="30a7f-573">İlk bordrodan önce ayrılma</span><span class="sxs-lookup"><span data-stu-id="30a7f-573">Departure before first payroll</span></span> | <span data-ttu-id="30a7f-574">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-574">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="30a7f-575">RESIGNATION</span></span>            | <span data-ttu-id="30a7f-576">İstifa</span><span class="sxs-lookup"><span data-stu-id="30a7f-576">Resignation</span></span>                    | <span data-ttu-id="30a7f-577">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-577">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="30a7f-578">PENSION</span></span>                | <span data-ttu-id="30a7f-579">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="30a7f-579">Pension</span></span>                        | <span data-ttu-id="30a7f-580">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-580">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="30a7f-581">TERMINATION</span></span>            | <span data-ttu-id="30a7f-582">Bitiş</span><span class="sxs-lookup"><span data-stu-id="30a7f-582">Termination</span></span>                    | <span data-ttu-id="30a7f-583">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-583">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="30a7f-584">RETIREMENT</span></span>             | <span data-ttu-id="30a7f-585">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="30a7f-585">Retirement</span></span>                     | <span data-ttu-id="30a7f-586">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-586">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="30a7f-587">ABSENTEE</span></span>               | <span data-ttu-id="30a7f-588">Devamsızlık</span><span class="sxs-lookup"><span data-stu-id="30a7f-588">Absentee</span></span>                       | <span data-ttu-id="30a7f-589">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-589">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-590">OTHER</span><span class="sxs-lookup"><span data-stu-id="30a7f-590">OTHER</span></span>                  | <span data-ttu-id="30a7f-591">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="30a7f-591">Other Reasons</span></span>                  | <span data-ttu-id="30a7f-592">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-592">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="30a7f-593">CLOSURE</span></span>                | <span data-ttu-id="30a7f-594">İşletmenin Kapanması</span><span class="sxs-lookup"><span data-stu-id="30a7f-594">Business Closure</span></span>               | <span data-ttu-id="30a7f-595">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-595">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="30a7f-596">DEATH</span></span>                  | <span data-ttu-id="30a7f-597">Ölüm</span><span class="sxs-lookup"><span data-stu-id="30a7f-597">Death</span></span>                          | <span data-ttu-id="30a7f-598">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-598">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="30a7f-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="30a7f-600">İzin</span><span class="sxs-lookup"><span data-stu-id="30a7f-600">Leave of Absence</span></span>               | <span data-ttu-id="30a7f-601">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-601">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="30a7f-602">CONTRACTEND</span></span>            | <span data-ttu-id="30a7f-603">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="30a7f-603">End of Contract</span></span>                | <span data-ttu-id="30a7f-604">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="30a7f-604">Terminate worker</span></span>     |
| <span data-ttu-id="30a7f-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="30a7f-605">SALARYCHANGE</span></span>           | <span data-ttu-id="30a7f-606">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="30a7f-606">Change of Salary</span></span>               | <span data-ttu-id="30a7f-607">Ücret</span><span class="sxs-lookup"><span data-stu-id="30a7f-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="30a7f-608">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="30a7f-608">Terms of employment</span></span>

<span data-ttu-id="30a7f-609">İstihdam koşulları, istihdam koşullarının kategorilerini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="30a7f-610">Koşullar, istihdam göstergesi değerleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="30a7f-611">Aşağıdaki istihdam koşulları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="30a7f-612">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="30a7f-612">Terms of employment</span></span>   | <span data-ttu-id="30a7f-613">Tanım</span><span class="sxs-lookup"><span data-stu-id="30a7f-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="30a7f-614">Normal</span><span class="sxs-lookup"><span data-stu-id="30a7f-614">Regular</span></span>               | <span data-ttu-id="30a7f-615">Normal</span><span class="sxs-lookup"><span data-stu-id="30a7f-615">Regular</span></span>     |
| <span data-ttu-id="30a7f-616">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="30a7f-616">Direct</span></span>                | <span data-ttu-id="30a7f-617">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="30a7f-617">Direct</span></span>      |
| <span data-ttu-id="30a7f-618">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="30a7f-618">Internship</span></span>            | <span data-ttu-id="30a7f-619">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="30a7f-619">Internship</span></span>  |
| <span data-ttu-id="30a7f-620">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="30a7f-620">Permanent</span></span>             | <span data-ttu-id="30a7f-621">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="30a7f-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="30a7f-622">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="30a7f-622">Marital status</span></span>

<span data-ttu-id="30a7f-623">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="30a7f-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="30a7f-624">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="30a7f-625">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-625">Human Resources</span></span>                 | <span data-ttu-id="30a7f-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="30a7f-627">Evli</span><span class="sxs-lookup"><span data-stu-id="30a7f-627">Married</span></span>                | <span data-ttu-id="30a7f-628">Evli</span><span class="sxs-lookup"><span data-stu-id="30a7f-628">Married</span></span>                   |
| <span data-ttu-id="30a7f-629">Tekli</span><span class="sxs-lookup"><span data-stu-id="30a7f-629">Single</span></span>                 | <span data-ttu-id="30a7f-630">Tekli</span><span class="sxs-lookup"><span data-stu-id="30a7f-630">Single</span></span>                    |
| <span data-ttu-id="30a7f-631">Dul</span><span class="sxs-lookup"><span data-stu-id="30a7f-631">Widowed</span></span>                | <span data-ttu-id="30a7f-632">Dul</span><span class="sxs-lookup"><span data-stu-id="30a7f-632">Widowed</span></span>                   |
| <span data-ttu-id="30a7f-633">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="30a7f-633">Divorced</span></span>               | <span data-ttu-id="30a7f-634">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="30a7f-634">Divorced</span></span>                  |
| <span data-ttu-id="30a7f-635">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="30a7f-635">Registered Partnership</span></span> | <span data-ttu-id="30a7f-636">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="30a7f-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="30a7f-637">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="30a7f-637">None</span></span>                   | <span data-ttu-id="30a7f-638">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="30a7f-639">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="30a7f-639">Cohabiting</span></span>             | <span data-ttu-id="30a7f-640">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="30a7f-641">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="30a7f-641">Gender</span></span>

<span data-ttu-id="30a7f-642">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="30a7f-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="30a7f-643">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="30a7f-644">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-644">Human Resources</span></span>       | <span data-ttu-id="30a7f-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="30a7f-646">Erkek</span><span class="sxs-lookup"><span data-stu-id="30a7f-646">Male</span></span>         | <span data-ttu-id="30a7f-647">Erkek</span><span class="sxs-lookup"><span data-stu-id="30a7f-647">Male</span></span>                      |
| <span data-ttu-id="30a7f-648">Kadın</span><span class="sxs-lookup"><span data-stu-id="30a7f-648">Female</span></span>       | <span data-ttu-id="30a7f-649">Kadın</span><span class="sxs-lookup"><span data-stu-id="30a7f-649">Female</span></span>                    |
| <span data-ttu-id="30a7f-650">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="30a7f-650">Non-specific</span></span> | <span data-ttu-id="30a7f-651">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="30a7f-652">Ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="30a7f-652">Payment method</span></span>

<span data-ttu-id="30a7f-653">Ödeme yöntemleri, personele ve şirkete çalışanlara nasıl ödeme yapılacağını tanımlamak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="30a7f-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="30a7f-654">Ödeme yöntemleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="30a7f-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="30a7f-655">Aşağıdaki tabloda ödeme yöntemlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="30a7f-656">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-656">Human Resources</span></span>             | <span data-ttu-id="30a7f-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="30a7f-658">Nakit</span><span class="sxs-lookup"><span data-stu-id="30a7f-658">Cash</span></span>               | <span data-ttu-id="30a7f-659">Nakit</span><span class="sxs-lookup"><span data-stu-id="30a7f-659">Cash</span></span>                      |
| <span data-ttu-id="30a7f-660">Elektronik Ödeme</span><span class="sxs-lookup"><span data-stu-id="30a7f-660">Electronic Payment</span></span> | <span data-ttu-id="30a7f-661">Transfer et</span><span class="sxs-lookup"><span data-stu-id="30a7f-661">Transfer</span></span>                  |
| <span data-ttu-id="30a7f-662">Denetle</span><span class="sxs-lookup"><span data-stu-id="30a7f-662">Check</span></span>              | <span data-ttu-id="30a7f-663">Çek</span><span class="sxs-lookup"><span data-stu-id="30a7f-663">Cheque</span></span>                    |
| <span data-ttu-id="30a7f-664">Banka Ödeme Emri</span><span class="sxs-lookup"><span data-stu-id="30a7f-664">Bank Draft</span></span>         | <span data-ttu-id="30a7f-665">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="30a7f-666">Diğer</span><span class="sxs-lookup"><span data-stu-id="30a7f-666">Other</span></span>              | <span data-ttu-id="30a7f-667">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="30a7f-668">Banka hesabı türü</span><span class="sxs-lookup"><span data-stu-id="30a7f-668">Bank account type</span></span>

<span data-ttu-id="30a7f-669">Banka hesap türleri, personele elektronik ödeme yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="30a7f-670">Banka hesap türleri, transfer hesabı bilgileri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="30a7f-671">Banka hesap türleri, uygunsa tümleştirme işleminden sonra kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="30a7f-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="30a7f-672">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-672">Human Resources</span></span>            | <span data-ttu-id="30a7f-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="30a7f-674">Cari Hesap</span><span class="sxs-lookup"><span data-stu-id="30a7f-674">Checking Account</span></span>  | <span data-ttu-id="30a7f-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="30a7f-675">CheckingAccount</span></span>           |
| <span data-ttu-id="30a7f-676">Bordro Hesabı</span><span class="sxs-lookup"><span data-stu-id="30a7f-676">Payroll Account</span></span>   | <span data-ttu-id="30a7f-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="30a7f-677">PayrollAccount</span></span>            |
| <span data-ttu-id="30a7f-678">Tasarruf Hesabı</span><span class="sxs-lookup"><span data-stu-id="30a7f-678">Savings Account</span></span>   | <span data-ttu-id="30a7f-679">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="30a7f-680">BankGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="30a7f-680">BankGirot account</span></span> | <span data-ttu-id="30a7f-681">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="30a7f-682">PlusGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="30a7f-682">PlusGirot account</span></span> | <span data-ttu-id="30a7f-683">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="30a7f-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="30a7f-684">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="30a7f-684">Earning codes</span></span>

<span data-ttu-id="30a7f-685">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="30a7f-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="30a7f-686">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="30a7f-687">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30a7f-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="30a7f-688">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="30a7f-688">Supported frequencies</span></span>

- <span data-ttu-id="30a7f-689">Tümü</span><span class="sxs-lookup"><span data-stu-id="30a7f-689">All</span></span>
- <span data-ttu-id="30a7f-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="30a7f-690">EVERYPAY</span></span>
- <span data-ttu-id="30a7f-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="30a7f-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="30a7f-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="30a7f-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="30a7f-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="30a7f-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="30a7f-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-694">1OFMTH</span></span>
- <span data-ttu-id="30a7f-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-695">LASTOFMTH</span></span>
- <span data-ttu-id="30a7f-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-696">2OFMTH</span></span>
- <span data-ttu-id="30a7f-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-697">3OFMTH</span></span>
- <span data-ttu-id="30a7f-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-698">4OFMTH</span></span>
- <span data-ttu-id="30a7f-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-699">5OFMTH</span></span>
- <span data-ttu-id="30a7f-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-700">1N2OFMTH</span></span>
- <span data-ttu-id="30a7f-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-701">3N4OFMTH</span></span>
- <span data-ttu-id="30a7f-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-702">1N3OFMTH</span></span>
- <span data-ttu-id="30a7f-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-703">1N4OFMTH</span></span>
- <span data-ttu-id="30a7f-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-704">2N3OFMTH</span></span>
- <span data-ttu-id="30a7f-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-705">2N4OFMTH</span></span>
- <span data-ttu-id="30a7f-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="30a7f-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="30a7f-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="30a7f-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="30a7f-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="30a7f-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="30a7f-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="30a7f-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="30a7f-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="30a7f-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="30a7f-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="30a7f-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="30a7f-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="30a7f-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="30a7f-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="30a7f-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="30a7f-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="30a7f-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="30a7f-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="30a7f-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="30a7f-718">Adresler</span><span class="sxs-lookup"><span data-stu-id="30a7f-718">Addresses</span></span>

<span data-ttu-id="30a7f-719">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="30a7f-720">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="30a7f-721">İnsan Kaynakları</span><span class="sxs-lookup"><span data-stu-id="30a7f-721">Human Resources</span></span>              | <span data-ttu-id="30a7f-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="30a7f-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="30a7f-723">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="30a7f-723">Country/Region</span></span>      | <span data-ttu-id="30a7f-724">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-724">Country Code</span></span>          |
| <span data-ttu-id="30a7f-725">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-725">Zip/Postal Code</span></span>     | <span data-ttu-id="30a7f-726">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-726">Postal Code</span></span>           |
| <span data-ttu-id="30a7f-727">İl</span><span class="sxs-lookup"><span data-stu-id="30a7f-727">State</span></span>               | <span data-ttu-id="30a7f-728">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="30a7f-728">State Code</span></span>            |
| <span data-ttu-id="30a7f-729">Şehir</span><span class="sxs-lookup"><span data-stu-id="30a7f-729">City</span></span>                | <span data-ttu-id="30a7f-730">Şehir</span><span class="sxs-lookup"><span data-stu-id="30a7f-730">City</span></span>                  |
| <span data-ttu-id="30a7f-731">İlçe</span><span class="sxs-lookup"><span data-stu-id="30a7f-731">County</span></span>              | <span data-ttu-id="30a7f-732">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="30a7f-732">County (Municipality)</span></span> |
| <span data-ttu-id="30a7f-733">Sokak</span><span class="sxs-lookup"><span data-stu-id="30a7f-733">Street</span></span>              | <span data-ttu-id="30a7f-734">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="30a7f-734">Address Line 1</span></span>        |
| <span data-ttu-id="30a7f-735">Cadde Numarası</span><span class="sxs-lookup"><span data-stu-id="30a7f-735">Street Number</span></span>       | <span data-ttu-id="30a7f-736">Adres Satırı 2</span><span class="sxs-lookup"><span data-stu-id="30a7f-736">Address Line 2</span></span>        |
| <span data-ttu-id="30a7f-737">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="30a7f-737">Building Complement</span></span> | <span data-ttu-id="30a7f-738">Adres Satırı 5</span><span class="sxs-lookup"><span data-stu-id="30a7f-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="30a7f-739">Pasaport numarası</span><span class="sxs-lookup"><span data-stu-id="30a7f-739">Passport number</span></span>

<span data-ttu-id="30a7f-740">Personel pasaport bilgilerini bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-740">Employees can declare passport information.</span></span> <span data-ttu-id="30a7f-741">Bu bilgiler, **Pasaport** kimlik türünü içerir ve Meksika'ya özel personel bilgilerinin bir parçası olarak Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="30a7f-742">Kimlik Türü = "Pasaport"</span><span class="sxs-lookup"><span data-stu-id="30a7f-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="30a7f-743">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="30a7f-743">Issued Date</span></span>
- <span data-ttu-id="30a7f-744">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="30a7f-744">Expiration Date</span></span>

<span data-ttu-id="30a7f-745">Personel, **Pasaport** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="30a7f-746">Ancak yalnızca geçerli etkin pasaport girişi Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="30a7f-747">Tüm pasaport girişlerinin süresi dolmuşsa en son verilen pasaport Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="30a7f-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>


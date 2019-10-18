---
title: Talent ile Dayforce arasında bordro tümleştirmesini yapılandırma
description: Bu konuda, bir ödeme işlemini işlemek üzere Microsoft Dynamics 365 Talent ile Ceridian Dayforce arasındaki tümleştirmeyi nasıl yapılandıracağınız açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: ec1d14cb14ab709dfc1bead4be0785904efcce4e
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251051"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="fe65f-103">Talent ve Dayforce arasında bordro tümleştirmeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fe65f-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe65f-104">Microsoft Dynamics 365 Talent ile Ceridian Dayforce arasındaki tümleştirme, bu konuda açıklanan çeşitli yapılandırma adımlarına dayanır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="fe65f-105">Ödeme işlemini işlemeden önce tümleştirmeyi hem Talent hem de Dayforce'ta yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="fe65f-106">Ödeme işlemlerini tamamlamak için Dayforce gibi bir hizmet kullandığınızda tümleştirmeyi Talent'ta etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="fe65f-107">Tümleştirme için Talent'tan özel veriler gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="fe65f-108">Bu nedenle, Dayforce ile eşlenmiş verilerin Talent'ta tümleştirmeyi destekleyecek şekilde yapılandırıldığını doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="fe65f-109">Tümleştirme, aşağıdaki geniş veri kategorilerini kullanır:</span><span class="sxs-lookup"><span data-stu-id="fe65f-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="fe65f-110">İnsan kaynakları verileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-110">Human resources data</span></span>
- <span data-ttu-id="fe65f-111">Ücret verileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-111">Compensation data</span></span>
- <span data-ttu-id="fe65f-112">Ödeme döngüleri, ödeme dönemleri ve kazanç kodları gibi bordro verileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="fe65f-113">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-113">Worker data</span></span>

<span data-ttu-id="fe65f-114">Bu konuda, tümleştirmeyi etkinleştirmek için izlemeniz gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="fe65f-115">Ayrıca veri türleri ve tümleştirmenin gerektirdiği yapılandırma ayrıntıları da açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="fe65f-116">Tümleştirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="fe65f-116">Enable the integration</span></span>

<span data-ttu-id="fe65f-117">Talent'ta yapılandırmayı açmanız ve Dayforce'a bağlanmak için yapılandırma bilgilerini girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="fe65f-118">Microsoft Dynamics 365 Finance'a aktarılmak üzere oluşturulan genel muhasebe hareketini istiyorsanız ayrıca bir Microsoft Azure depolama hesabı oluşturmanız ve Finance'ta Azure Depolama bağlantı dizesini de girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="fe65f-119">Talent'ta tümleştirmeyi açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe65f-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="fe65f-120">**Sistem yönetimi** sayfasında **Tümleştirme yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe65f-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="fe65f-121">Güvenli Dosya Aktarım Protokolü (FTP) uç noktasını ve güvenli FTP klasörü yolunu girin.</span><span class="sxs-lookup"><span data-stu-id="fe65f-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="fe65f-122">Güvenli FTP uç noktasına ve klasör yoluna erişecek kullanıcının kullanıcı adını ve parolasını girin.</span><span class="sxs-lookup"><span data-stu-id="fe65f-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="fe65f-123">Bağlantıyı gerektiği gibi test edin ve **Bordro tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fe65f-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="fe65f-124">Tümleştirme açıldığında veri dışa aktarma paketi ve dosyalar oluşturulur ve sıklık ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="fe65f-125">Bu sıklığı ihtiyaç duyduğunuz şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe65f-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="fe65f-126">Azure depolama hesapları ve Azure Depolama bağlantı dizeleri hakkında daha fazla bilgi için aşağıdaki Azure konularına bakın:</span><span class="sxs-lookup"><span data-stu-id="fe65f-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="fe65f-127">Azure depolama hesapları hakkında</span><span class="sxs-lookup"><span data-stu-id="fe65f-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="fe65f-128">Azure Depolama bağlantı dizelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fe65f-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="fe65f-129">Bordro tümleştirmesinin etkinleştirilmesinin teknik ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="fe65f-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="fe65f-130">Bordro tümleştirmesinin açılmasının iki temel etkisi vardır:</span><span class="sxs-lookup"><span data-stu-id="fe65f-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="fe65f-131">"Bordro tümleştirmesini dışa aktar" adlı dışa veri aktarma projesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fe65f-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="fe65f-132">Bu proje, bordro tümleştirmesi için gerekli olan varlıkları ve alanları içerir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="fe65f-133">Projeyi incelemek için **Sistem yönetimi**'ne gidin, **Veri yönetimi** kutucuğunu seçin ve ardından projeler listesinden veri projesini açın.</span><span class="sxs-lookup"><span data-stu-id="fe65f-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="fe65f-134">Bu toplu iş, veri dışa aktarma projesini yürütür, sonuçta elde edilen veri paketini şifreler ve veri paketi dosyasını **Tümleştirme Yapılandırması** ekranında yapılandırılan SFTP son noktasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="fe65f-135">SFTP son noktasına aktarılan veri paketi, pakette benzersiz bir anahtar kullanılarak şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="fe65f-136">Anahtar yalnızca Ceridian tarafından erişilebilen bir Azure Key Vault'ta yer alır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="fe65f-137">Veri paketi içeriğinin şifresini çözmek ve içeriği incelemek mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="fe65f-138">Veri paketinin içeriğini incelemeniz gerekiyorsa "Bordro tümleştirmesini dışa aktar" veri projesini el ile dışa aktarmanız, indirmeniz ve sonra açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="fe65f-139">El ile dışa aktarmada şifreleme uygulanmaz veya paket transfer edilmez.</span><span class="sxs-lookup"><span data-stu-id="fe65f-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="fe65f-140">Verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fe65f-140">Configure your data</span></span> 

<span data-ttu-id="fe65f-141">Bordro işlemek için Talent'ta insan kaynağı verilerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="fe65f-142">Kazanç ve ücret bilgileriyle birlikte işler ve pozisyonlar gibi kurumsal verileri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="fe65f-143">Bu bilgiler personel ödemesi oluşturmak için gerekli olan istihdam, ödeme ve kesinti bilgilerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="fe65f-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="fe65f-144">İnsan kaynağı verileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="fe65f-145">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="fe65f-145">Benefits</span></span> 

<span data-ttu-id="fe65f-146">İnsan kaynakları, bir kuruluşun çalışanları için sunduğu veya işlediği kazançları, kesintileri ve çalışan ücret planlarını ayarlamak ve bunları yönetmek için kullanılan araçları sağlar.</span><span class="sxs-lookup"><span data-stu-id="fe65f-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="fe65f-147">Kazançları oluştururken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="fe65f-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="fe65f-148">Kazanç planları</span><span class="sxs-lookup"><span data-stu-id="fe65f-148">Benefit plans</span></span>

- <span data-ttu-id="fe65f-149">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-149">Plan (required)</span></span>
- <span data-ttu-id="fe65f-150">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-150">Type (required)</span></span>
- <span data-ttu-id="fe65f-151">Bordro etkisi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-151">Payroll impact (required)</span></span>
- <span data-ttu-id="fe65f-152">Borçları kurtar</span><span class="sxs-lookup"><span data-stu-id="fe65f-152">Recover arrears</span></span>
- <span data-ttu-id="fe65f-153">Kesinti yöntemi</span><span class="sxs-lookup"><span data-stu-id="fe65f-153">Deduction method</span></span>
- <span data-ttu-id="fe65f-154">Kesinti önceliği</span><span class="sxs-lookup"><span data-stu-id="fe65f-154">Deduction priority</span></span>
- <span data-ttu-id="fe65f-155">Dönemi sınırla</span><span class="sxs-lookup"><span data-stu-id="fe65f-155">Limit period</span></span>
- <span data-ttu-id="fe65f-156">Sınır tutar</span><span class="sxs-lookup"><span data-stu-id="fe65f-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="fe65f-157">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="fe65f-157">Benefits</span></span>

- <span data-ttu-id="fe65f-158">Plan (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-158">Plan (required)</span></span>
- <span data-ttu-id="fe65f-159">Tür (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-159">Type (required)</span></span>
- <span data-ttu-id="fe65f-160">Seçenek (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-160">Option (required)</span></span>
- <span data-ttu-id="fe65f-161">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-161">Benefit ID (required)</span></span>
- <span data-ttu-id="fe65f-162">Sıklık</span><span class="sxs-lookup"><span data-stu-id="fe65f-162">Frequency</span></span>
- <span data-ttu-id="fe65f-163">Temel</span><span class="sxs-lookup"><span data-stu-id="fe65f-163">Basis</span></span>
- <span data-ttu-id="fe65f-164">Tutar veya oran</span><span class="sxs-lookup"><span data-stu-id="fe65f-164">Amount or rate</span></span>
- <span data-ttu-id="fe65f-165">Kazanç kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="fe65f-166">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="fe65f-166">Supported frequencies</span></span> 

- <span data-ttu-id="fe65f-167">Haftalık</span><span class="sxs-lookup"><span data-stu-id="fe65f-167">Weekly</span></span>
- <span data-ttu-id="fe65f-168">İki haftada bir</span><span class="sxs-lookup"><span data-stu-id="fe65f-168">Bi-weekly</span></span>
- <span data-ttu-id="fe65f-169">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="fe65f-169">Semi-monthly</span></span>
- <span data-ttu-id="fe65f-170">Aylık</span><span class="sxs-lookup"><span data-stu-id="fe65f-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="fe65f-171">Desteklenen tabanlar</span><span class="sxs-lookup"><span data-stu-id="fe65f-171">Supported bases</span></span> 

- <span data-ttu-id="fe65f-172">Sabit tutar</span><span class="sxs-lookup"><span data-stu-id="fe65f-172">Fixed amount</span></span>
- <span data-ttu-id="fe65f-173">Kazançların yüzdesi</span><span class="sxs-lookup"><span data-stu-id="fe65f-173">Percent of earnings</span></span>
- <span data-ttu-id="fe65f-174">Üretime yönelik saatler</span><span class="sxs-lookup"><span data-stu-id="fe65f-174">Productive hours</span></span>

<span data-ttu-id="fe65f-175">Dayforce, kazanç planında tanımlanan bordro etkisine göre aşağıdaki kesintileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe65f-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="fe65f-176">Talent'ta seçim</span><span class="sxs-lookup"><span data-stu-id="fe65f-176">Selection in Talent</span></span>        | <span data-ttu-id="fe65f-177">Dayforce'ta sonuç</span><span class="sxs-lookup"><span data-stu-id="fe65f-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="fe65f-178">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="fe65f-178">None</span></span>                       | <span data-ttu-id="fe65f-179">Kesinti oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="fe65f-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="fe65f-180">Yalnızca kesinti</span><span class="sxs-lookup"><span data-stu-id="fe65f-180">Deduction only</span></span>             | <span data-ttu-id="fe65f-181">Personel kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fe65f-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="fe65f-182">Yalnızca katkı</span><span class="sxs-lookup"><span data-stu-id="fe65f-182">Contribution only</span></span>          | <span data-ttu-id="fe65f-183">İşveren kesintisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fe65f-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="fe65f-184">Kesinti ve katkı</span><span class="sxs-lookup"><span data-stu-id="fe65f-184">Deduction and contribution</span></span> | <span data-ttu-id="fe65f-185">Personel ve işveren kesintileri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fe65f-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="fe65f-186">Kazanç programı tanımlama ve yönetme hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="fe65f-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="fe65f-187">Personel kazançları programı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe65f-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="fe65f-188">Yeni kazanç oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe65f-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="fe65f-189">Kazanç uygunluk kurallarını ve ilkelerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="fe65f-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="fe65f-190">Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma</span><span class="sxs-lookup"><span data-stu-id="fe65f-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="fe65f-191">Ücret</span><span class="sxs-lookup"><span data-stu-id="fe65f-191">Compensation</span></span> 

<span data-ttu-id="fe65f-192">Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="fe65f-193">Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="fe65f-194">İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="fe65f-195">Dayforce personelin saatlik veya yıllık ücretlerini hesaplamak için ücret bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="fe65f-196">Sabit ücret planları ve ödeme oranı dönüştürmeleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="fe65f-197">Personelin bir sabit ücret planıyla ilişkilendirilmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="fe65f-198">Ücret planları hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="fe65f-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="fe65f-199">Sabit ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe65f-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="fe65f-200">Değişken ücret planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe65f-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="fe65f-201">Maaş/ücret yapısı ve planları geliştirme</span><span class="sxs-lookup"><span data-stu-id="fe65f-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="fe65f-202">İşlem ücreti</span><span class="sxs-lookup"><span data-stu-id="fe65f-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="fe65f-203">Ücret işlemini tanımlama ve sonuçları hesaplama</span><span class="sxs-lookup"><span data-stu-id="fe65f-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="fe65f-204">Personeli sabit ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="fe65f-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="fe65f-205">Personeli değişken ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="fe65f-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="fe65f-206">İşler</span><span class="sxs-lookup"><span data-stu-id="fe65f-206">Jobs</span></span> 

<span data-ttu-id="fe65f-207">Bir iş, işi gerçekleştiren kişiden beklenen görev ve sorumlulukların toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="fe65f-208">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="fe65f-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="fe65f-209">İşin bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe65f-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="fe65f-210">Yeni işler tanımlama</span><span class="sxs-lookup"><span data-stu-id="fe65f-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="fe65f-211">Pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="fe65f-211">Positions</span></span>

<span data-ttu-id="fe65f-212">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="fe65f-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="fe65f-213">Örneğin, "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş pozisyonlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="fe65f-214">Bir pozisyon, bir departmanda bulunur.</span><span class="sxs-lookup"><span data-stu-id="fe65f-214">A position exists in a department.</span></span> <span data-ttu-id="fe65f-215">Her pozisyonla yalnızca bir çalışan ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="fe65f-216">Pozisyonları ayarlarken aşağıdaki verileri ve yapılandırmayı göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="fe65f-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="fe65f-217">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-217">Position (required)</span></span>
- <span data-ttu-id="fe65f-218">Açıklama (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-218">Description (required)</span></span>
- <span data-ttu-id="fe65f-219">İş (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-219">Job (required)</span></span>
- <span data-ttu-id="fe65f-220">Departman (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-220">Department (required)</span></span>
- <span data-ttu-id="fe65f-221">Pozisyon türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-221">Position type (required)</span></span>
- <span data-ttu-id="fe65f-222">Tam zamanlı eşdeğeri</span><span class="sxs-lookup"><span data-stu-id="fe65f-222">Full-time equivalent</span></span>
- <span data-ttu-id="fe65f-223">Yıllık mesai saatleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="fe65f-224">Tüzel kişilik tarafından ödenen (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="fe65f-225">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-225">Pay cycle (required)</span></span>
- <span data-ttu-id="fe65f-226">Varsayılan mali boyut – Maliyet merkezi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="fe65f-227">Çalışan ataması: Çalışan, atama başlangıç tarihi, atama bitiş tarihi, neden kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="fe65f-228">Aynı departmanda birden fazla pozisyon aynı işle ilişkilendirilmişse bunlar Dayforce'ta tek bir pozisyonda konsolide edilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="fe65f-229">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="fe65f-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="fe65f-230">Departmanlar, işler ve pozisyonları kullanarak iş gücünüzü düzenleme</span><span class="sxs-lookup"><span data-stu-id="fe65f-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="fe65f-231">Pozisyonları ayarlama</span><span class="sxs-lookup"><span data-stu-id="fe65f-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="fe65f-232">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="fe65f-232">Departments</span></span>

<span data-ttu-id="fe65f-233">Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="fe65f-234">Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur.</span><span class="sxs-lookup"><span data-stu-id="fe65f-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="fe65f-235">İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe65f-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="fe65f-236">Departmanların kâr ve zarar sorumluluğu olabilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="fe65f-237">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="fe65f-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="fe65f-238">Departman oluşturma ve departman hiyerarşisi ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="fe65f-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="fe65f-239">Yeni departmanlar tanımlama</span><span class="sxs-lookup"><span data-stu-id="fe65f-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="fe65f-240">Ödeme döngüleri ve ödeme dönemleri</span><span class="sxs-lookup"><span data-stu-id="fe65f-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="fe65f-241">Ödeme döngüsü, bordronun ne sıklıkta çalıştırıldığını ve çalışanlara ödeme yapılan belirli günleri belirler.</span><span class="sxs-lookup"><span data-stu-id="fe65f-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="fe65f-242">Örneğin, bir ödeme döngüsü aylık olabilir ve personele ayın son günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="fe65f-243">Alternatif olarak, bir ödeme döngüsü haftalık olabilir ve personele ödeme döneminin bitişinden sonraki Salı günü ödeme yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="fe65f-244">Ödeme döngüleri, bu pozisyonlardaki çalışanlara ne zaman ödeme yapıldığını kontrol etmek için pozisyonlara atanır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="fe65f-245">Ödeme döngülerini oluşturduktan sonra her döngü için ödeme dönemleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe65f-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="fe65f-246">Her ödeme dönemi, sağladığınız bilgilere göre varsayılan bir ödeme tarihi içerir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="fe65f-247">Ancak ödeme döneminin bir tatil gününe denk gelmesi gibi istisnalara izin vermek için ödeme döneminde varsayılan ödeme tarihini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe65f-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="fe65f-248">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="fe65f-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="fe65f-249">Ödeme döngüsü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-249">Pay cycle (required)</span></span>
- <span data-ttu-id="fe65f-250">Ödeme döngüsü sıklığı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="fe65f-251">Dönem başlangıç tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="fe65f-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="fe65f-252">Varsayılan ödeme tarihi (ilk ödeme dönemi gerekir)</span><span class="sxs-lookup"><span data-stu-id="fe65f-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="fe65f-253">Bu bilgiler ödeme grupları olarak Dayforce ile tümleştirilir ve her ödeme döngüsü için ülke veya bölgeye göre ayrılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="fe65f-254">Tümleştirmeden önce en az bir ödeme dönemi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="fe65f-255">Dayforce, ilk ödeme döneminin başlangıç tarihine ve Talent'ta ayarlanan varsayılan ödeme tarihine bağlı olarak ödeme grubu takvimlerini ve ödeme tarihlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe65f-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="fe65f-256">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="fe65f-256">Earning codes</span></span>

<span data-ttu-id="fe65f-257">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fe65f-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="fe65f-258">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametrelere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="fe65f-259">Dayforce'ta aşağıdaki bilgiler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="fe65f-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="fe65f-260">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-260">Earning Code (required)</span></span>
- <span data-ttu-id="fe65f-261">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65f-261">Description</span></span>
- <span data-ttu-id="fe65f-262">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="fe65f-262">Unit of measure</span></span>
- <span data-ttu-id="fe65f-263">Üretken</span><span class="sxs-lookup"><span data-stu-id="fe65f-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="fe65f-264">Çalışan verileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-264">Worker data</span></span>

<span data-ttu-id="fe65f-265">Sahip olduğunuz çeşitli çalışan türlerine ilişkin kayıtlar, insan kaynaklarınız ve bordro sistemleriniz için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="fe65f-266">Girdiğiniz bilgiler çalışanları ve kişisel bilgileri izlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="fe65f-267">Çalışanlar hakkında aşağıdaki bilgileri koruyabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="fe65f-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="fe65f-268">**Temel**: İletişim bilgileri, demografik bilgiler, kimlik bilgileri, aile bilgileri, askerlik hizmeti durumu, göçmenlik bilgileri ile kişisel ve acil durum iletişim kişileri gibi temel bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="fe65f-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="fe65f-269">**İstihdam**: Şirket veya kuruluş ilişkisi, pozisyon ataması, başlangıç ve bitiş tarihleri, iş uygunluğu, istihdam koşulları, emeklilik, tatil ve tayin bilgileri gibi bir çalışanın istihdamıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="fe65f-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="fe65f-270">**İzin ve devamsızlık**: Çalışma takvimleri, devamsızlık işlemleri ve devamsızlık ayarı gibi bir çalışanın devamsızlığıyla ilgili bilgileri tutun.</span><span class="sxs-lookup"><span data-stu-id="fe65f-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="fe65f-271">**Ücret ve bordro**: Plan kaydı, ödüller, performans, komisyon, vergi bilgileri, emeklilik ve maaş kesintileri gibi bir çalışanın ücret planlarıyla ilgili bilgileri ve bordro bilgilerini tutun.</span><span class="sxs-lookup"><span data-stu-id="fe65f-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="fe65f-272">Çalışan bilgilerini girerken Dayforce'ta kullanılan aşağıdaki verileri ve yapılandırmaları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="fe65f-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="fe65f-273">Genel bilgiler</span><span class="sxs-lookup"><span data-stu-id="fe65f-273">General information</span></span>

- <span data-ttu-id="fe65f-274">Personel numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-274">Personnel number (required)</span></span>
- <span data-ttu-id="fe65f-275">Ad (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-275">First name (required)</span></span>
- <span data-ttu-id="fe65f-276">Soyadı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-276">Last name (required)</span></span>
- <span data-ttu-id="fe65f-277">İkinci adı</span><span class="sxs-lookup"><span data-stu-id="fe65f-277">Middle name</span></span>
- <span data-ttu-id="fe65f-278">Kıdem tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-278">Seniority date</span></span>
- <span data-ttu-id="fe65f-279">Bilinen hali</span><span class="sxs-lookup"><span data-stu-id="fe65f-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="fe65f-280">Kişisel bilgiler</span><span class="sxs-lookup"><span data-stu-id="fe65f-280">Personal information</span></span>

- <span data-ttu-id="fe65f-281">Medeni durum (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-281">Marital status (required)</span></span>
- <span data-ttu-id="fe65f-282">Doğum tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-282">Birth date (required)</span></span>
- <span data-ttu-id="fe65f-283">Cinsiyet (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-283">Gender (required)</span></span>
- <span data-ttu-id="fe65f-284">Engelli kişi</span><span class="sxs-lookup"><span data-stu-id="fe65f-284">Person with disabilities</span></span>
- <span data-ttu-id="fe65f-285">Uyruğu ülkesi bölgesi (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="fe65f-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="fe65f-286">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-286">Address information</span></span>

- <span data-ttu-id="fe65f-287">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-287">Primary (required)</span></span>
- <span data-ttu-id="fe65f-288">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-288">Country/region (required)</span></span>
- <span data-ttu-id="fe65f-289">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-289">Postal code (required)</span></span>
- <span data-ttu-id="fe65f-290">Cadde Numarası (gerekli) (Yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="fe65f-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="fe65f-291">Bina Tamamlayıcı (yalnızca Meksika için)</span><span class="sxs-lookup"><span data-stu-id="fe65f-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="fe65f-292">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-292">City (required)</span></span>
- <span data-ttu-id="fe65f-293">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-293">State (required)</span></span>
- <span data-ttu-id="fe65f-294">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="fe65f-295">İletişim bilgileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-295">Contact information</span></span> 

- <span data-ttu-id="fe65f-296">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-296">Primary (required)</span></span>
- <span data-ttu-id="fe65f-297">İlgili kişi numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-297">Contact number (required)</span></span>
- <span data-ttu-id="fe65f-298">Dahili</span><span class="sxs-lookup"><span data-stu-id="fe65f-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="fe65f-299">Bordro bilgileri ve kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="fe65f-299">Payroll information and earning codes</span></span>

<span data-ttu-id="fe65f-300">Personele belirli bir ödeme sıklığında özel kazançlar atanabilir ve çalışanlar, tercih edilen bir ödeme yöntemine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="fe65f-301">Bu tercihlerin ve ayarların kullanıldığının sağlanmasına yardımcı olmak için Dayforce'ta aşağıdaki alanlar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="fe65f-302">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="fe65f-302">Earning codes</span></span>

- <span data-ttu-id="fe65f-303">Pozisyon (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-303">Position (required)</span></span>
- <span data-ttu-id="fe65f-304">Kazanç Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-304">Earning Code (required)</span></span>
- <span data-ttu-id="fe65f-305">Sıklık (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-305">Frequency (required)</span></span>
- <span data-ttu-id="fe65f-306">Tutar (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="fe65f-307">Bordro bilgileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-307">Payroll information</span></span>

- <span data-ttu-id="fe65f-308">Ödeme Yöntemi</span><span class="sxs-lookup"><span data-stu-id="fe65f-308">Payment Method</span></span>
- <span data-ttu-id="fe65f-309">Ekonomik Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-309">Economic Region (required)</span></span>
- <span data-ttu-id="fe65f-310">Personel Kazanç Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-310">Employee Benefits ID</span></span>
- <span data-ttu-id="fe65f-311">Ulusal Kimlik Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-311">National ID Number (required)</span></span>
- <span data-ttu-id="fe65f-312">Askerlik Hizmet Numarası</span><span class="sxs-lookup"><span data-stu-id="fe65f-312">Military Service Number</span></span>
- <span data-ttu-id="fe65f-313">Vardiya Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-313">Shift ID (required)</span></span>
- <span data-ttu-id="fe65f-314">Vergi Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-314">Tax Number (required)</span></span>
- <span data-ttu-id="fe65f-315">Sendika Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-315">Union ID (required)</span></span>
- <span data-ttu-id="fe65f-316">İş Günü Kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-316">Work Day ID (required)</span></span>
- <span data-ttu-id="fe65f-317">Çalışma İzni Numarası</span><span class="sxs-lookup"><span data-stu-id="fe65f-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="fe65f-318">Meksika'da ödeme yöntemleri olarak **Nakit**, **Çek** (şirketin fiziksel çeki) ve **Elektronik Ödeme** desteklenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="fe65f-319">Hiçbir ödeme yöntemi belirtilmemişse varsayılan olarak **Çek** kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="fe65f-320">İstihdam ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="fe65f-320">Employment details</span></span>

<span data-ttu-id="fe65f-321">İstihdam ayrıntıları geçmişi, personelin Dayforce'ta işe alma, işten çıkarma ve yeniden işe alma durumlarını oluşturmada temel bilgi olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="fe65f-322">Dayforce, bir defada yalnızca bir etkin istihdam kaydını destekler.</span><span class="sxs-lookup"><span data-stu-id="fe65f-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="fe65f-323">İşe başlama tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-323">Employment start date (required)</span></span>
- <span data-ttu-id="fe65f-324">İş bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-324">Employment end date</span></span>
- <span data-ttu-id="fe65f-325">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-325">Start date</span></span>
- <span data-ttu-id="fe65f-326">Ayarlanan başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-326">Adjusted start date</span></span>
- <span data-ttu-id="fe65f-327">İşten çıkarma tarihi (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="fe65f-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="fe65f-328">İşten çıkarma nedeni (işten çıkarma halinde gereklidir)</span><span class="sxs-lookup"><span data-stu-id="fe65f-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="fe65f-329">Personelin önemli tarihleri aşağıdaki bilgiler kullanılarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="fe65f-330">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-330">Talent</span></span>                | <span data-ttu-id="fe65f-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe65f-332">En son işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-332">Most recent hire date</span></span> | <span data-ttu-id="fe65f-333">Geçerli sonlandırılmamış işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="fe65f-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="fe65f-334">İşten çıkarma tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-334">Termination date</span></span>      | <span data-ttu-id="fe65f-335">Geçerli sonlandırılmamış işten çıkış tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="fe65f-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="fe65f-336">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-336">Start date</span></span>            | <span data-ttu-id="fe65f-337">Ayarlanan başlama tarihi, başlama tarihi veya geçerli etkin olmayan işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="fe65f-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="fe65f-338">Orijinal işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-338">Original hire date</span></span>    | <span data-ttu-id="fe65f-339">En erken işe başlama tarihi istihdam geçmişi kaydı</span><span class="sxs-lookup"><span data-stu-id="fe65f-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="fe65f-340">Ücret</span><span class="sxs-lookup"><span data-stu-id="fe65f-340">Compensation</span></span>

<span data-ttu-id="fe65f-341">Bir istihdam dönemi boyunca her personelin birincil pozisyonu ile sabit ücret planı ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="fe65f-342">Bu dönem personelin işe alındığı (veya işe başlama tarihi) tarihte başlar ve işten çıkış tarihine kadar devam eder.</span><span class="sxs-lookup"><span data-stu-id="fe65f-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="fe65f-343">Yürürlük Tarihi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-343">Effective Date (required)</span></span>
- <span data-ttu-id="fe65f-344">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-344">Expiration date</span></span>
- <span data-ttu-id="fe65f-345">Ödeme Oranı (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-345">Pay Rate (required)</span></span>
- <span data-ttu-id="fe65f-346">Ödeme Oranı Dönüştürmeleri (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="fe65f-347">Yıllık eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="fe65f-348">Saatlik eşdeğer (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="fe65f-349">Saatlik personelin birden fazla pozisyonu varsa birincil pozisyonun sabit ücreti, personel düzeyinde taban oranı/maaş olarak Dayforce'ta içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="fe65f-350">Birincil olmayan pozisyonlar için saatlik oran Dayforce'ta ilgili pozisyona kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="fe65f-351">Maaşlı personelin birden fazla pozisyonu varsa tüm etkin pozisyonlar için kümülatif saat oranı ve yıllık maaş oluşturulur ve personel düzeyinde taban oranı/maaş olarak türetilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="fe65f-352">Kimlik numaraları</span><span class="sxs-lookup"><span data-stu-id="fe65f-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="fe65f-353">Sosyal Güvenlik Kimlik Tanımlayıcı</span><span class="sxs-lookup"><span data-stu-id="fe65f-353">Social Security identifier</span></span> 

<span data-ttu-id="fe65f-354">Her personelin bir birincil kimlik tanımlayıcısı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="fe65f-355">Bu kimlik tanımlayıcı **SSK** kimlik türünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="fe65f-356">Dayforce'ta bu, personelin işe alınması için gereken Sosyal Güvenlik kimlik tanımlayıcı olarak otomatik türetilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="fe65f-357">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-357">Primary (required)</span></span>
- <span data-ttu-id="fe65f-358">Kimlik Türü = "SSN"</span><span class="sxs-lookup"><span data-stu-id="fe65f-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="fe65f-359">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="fe65f-359">Issued Date</span></span>
- <span data-ttu-id="fe65f-360">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-360">Expiration Date</span></span>

<span data-ttu-id="fe65f-361">Personel, **SSN** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="fe65f-362">Ancak numaranın etkin veya süresinin dolmuş olup olmadığına bakılmaksızın yalnızca **Birincil** olarak işaretlenen kayıt Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="fe65f-363">Banka hesapları ve tahsilatlar</span><span class="sxs-lookup"><span data-stu-id="fe65f-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="fe65f-364">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel için geçerli banka hesap bilgileri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="fe65f-365">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-365">Talent</span></span>                         | <span data-ttu-id="fe65f-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe65f-367">Banka hesap numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="fe65f-368">SWIFT kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-368">SWIFT code (required)</span></span>          | <span data-ttu-id="fe65f-369">Meksika'da bordro işlemleri için **Banka Kodu** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="fe65f-370">Şube numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="fe65f-371">Banka hesabı türü (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-371">Bank account type (required)</span></span>   | <span data-ttu-id="fe65f-372">Meksika'da bordro işlemleri için **Hesap türü** alanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="fe65f-373">Desteklenen değerler **Cari** ve **Bordro**'yu içerir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="fe65f-374">Banka hesabı transferleri aracılığıyla ödeme yapılmasını tercih eden personel, birincil adresi Meksika'da olan ve bir Meksika bankasındaki geçerli bir banka hesabıyla ilişkilendirilmiş tüzel kişilik altında bulunan bir bakiye hesabına bağlantı sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="fe65f-375">Bakiye hesabı olmayan diğer hesaplar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="fe65f-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="fe65f-376">Adres bilgileri</span><span class="sxs-lookup"><span data-stu-id="fe65f-376">Address information</span></span>

<span data-ttu-id="fe65f-377">Her personelin bir birincil konumu olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-377">Every employee must have one primary location.</span></span> <span data-ttu-id="fe65f-378">Dayforce'ta bu konum, personelin vergiye esas birincil ikamet yerini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="fe65f-379">Birincil (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-379">Primary (required)</span></span>
- <span data-ttu-id="fe65f-380">Ülke/bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-380">Country/region (required)</span></span>
- <span data-ttu-id="fe65f-381">Posta kodu (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="fe65f-382">Cadde (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-382">Street (required)</span></span>
- <span data-ttu-id="fe65f-383">Cadde Numarası (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-383">Street Number (required)</span></span>
- <span data-ttu-id="fe65f-384">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="fe65f-384">Building Complement</span></span>
- <span data-ttu-id="fe65f-385">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-385">City (required)</span></span>
- <span data-ttu-id="fe65f-386">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-386">State (required)</span></span>
- <span data-ttu-id="fe65f-387">Ülke (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="fe65f-388">Amerika Birleşik Devletleri ve Kanada’da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fe65f-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="fe65f-389">Amerika Birleşik Devletleri ve Kanada’daki personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="fe65f-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="fe65f-390">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-390">Departments are required on positions.</span></span>
- <span data-ttu-id="fe65f-391">Maliyet merkezleri mali boyut olarak ayarlanmalı ve varsayılan mali boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="fe65f-392">Departman gerektiren Pozisyonlar için Talent gerektirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe65f-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="fe65f-393">Bunu yapmak için **İnsan Kaynakları Paylaşılan Pozisyonlar > Pozisyonlar > Pozisyonlarda departmanlar gerektir**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="fe65f-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="fe65f-394">Bu ayarın tümleştirme için zorunlu olmasını öneririz.</span><span class="sxs-lookup"><span data-stu-id="fe65f-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="fe65f-395">İş türleri</span><span class="sxs-lookup"><span data-stu-id="fe65f-395">Job types</span></span>

<span data-ttu-id="fe65f-396">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="fe65f-397">Amerika Birleşik Devletleri ve Kanada'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="fe65f-398">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="fe65f-399">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="fe65f-400">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="fe65f-401">İş türü</span><span class="sxs-lookup"><span data-stu-id="fe65f-401">Job type</span></span>   | <span data-ttu-id="fe65f-402">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65f-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="fe65f-403">Saatlik</span><span class="sxs-lookup"><span data-stu-id="fe65f-403">Hourly</span></span>     | <span data-ttu-id="fe65f-404">Saatlik</span><span class="sxs-lookup"><span data-stu-id="fe65f-404">Hourly</span></span>      |
| <span data-ttu-id="fe65f-405">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="fe65f-405">Salaried</span></span>   | <span data-ttu-id="fe65f-406">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="fe65f-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="fe65f-407">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="fe65f-407">Position types</span></span> 

<span data-ttu-id="fe65f-408">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="fe65f-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="fe65f-409">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="fe65f-410">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="fe65f-411">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="fe65f-411">Position type</span></span>   | <span data-ttu-id="fe65f-412">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65f-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="fe65f-413">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="fe65f-413">Full-time</span></span>       | <span data-ttu-id="fe65f-414">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="fe65f-414">Full time employee</span></span> |
| <span data-ttu-id="fe65f-415">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="fe65f-415">Part-time</span></span>       | <span data-ttu-id="fe65f-416">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="fe65f-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="fe65f-417">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="fe65f-417">Reason codes</span></span>

<span data-ttu-id="fe65f-418">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="fe65f-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="fe65f-419">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="fe65f-420">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="fe65f-421">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-421">Reason code</span></span>    | <span data-ttu-id="fe65f-422">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65f-422">Description</span></span>      | <span data-ttu-id="fe65f-423">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="fe65f-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="fe65f-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="fe65f-424">RESIGNATION</span></span>    | <span data-ttu-id="fe65f-425">İstifa</span><span class="sxs-lookup"><span data-stu-id="fe65f-425">Resignation</span></span>      | <span data-ttu-id="fe65f-426">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-426">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="fe65f-427">TERMINATION</span></span>    | <span data-ttu-id="fe65f-428">Bitiş</span><span class="sxs-lookup"><span data-stu-id="fe65f-428">Termination</span></span>      | <span data-ttu-id="fe65f-429">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-429">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="fe65f-430">RETIREMENT</span></span>     | <span data-ttu-id="fe65f-431">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="fe65f-431">Retirement</span></span>       | <span data-ttu-id="fe65f-432">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-432">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-433">OTHER</span><span class="sxs-lookup"><span data-stu-id="fe65f-433">OTHER</span></span>          | <span data-ttu-id="fe65f-434">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="fe65f-434">Other Reasons</span></span>    | <span data-ttu-id="fe65f-435">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-435">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="fe65f-436">DEATH</span></span>          | <span data-ttu-id="fe65f-437">Ölüm</span><span class="sxs-lookup"><span data-stu-id="fe65f-437">Death</span></span>            | <span data-ttu-id="fe65f-438">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-438">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="fe65f-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="fe65f-440">İzin</span><span class="sxs-lookup"><span data-stu-id="fe65f-440">Leave of Absence</span></span> | <span data-ttu-id="fe65f-441">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-441">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="fe65f-442">CONTRACTEND</span></span>    | <span data-ttu-id="fe65f-443">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="fe65f-443">End of Contract</span></span>  | <span data-ttu-id="fe65f-444">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-444">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="fe65f-445">SALARYCHANGE</span></span>   | <span data-ttu-id="fe65f-446">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="fe65f-446">Change of Salary</span></span> | <span data-ttu-id="fe65f-447">Ücret</span><span class="sxs-lookup"><span data-stu-id="fe65f-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="fe65f-448">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="fe65f-448">Marital status</span></span>

<span data-ttu-id="fe65f-449">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="fe65f-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="fe65f-450">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="fe65f-451">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-451">Talent</span></span>                 | <span data-ttu-id="fe65f-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="fe65f-453">Evli</span><span class="sxs-lookup"><span data-stu-id="fe65f-453">Married</span></span>                | <span data-ttu-id="fe65f-454">Evli</span><span class="sxs-lookup"><span data-stu-id="fe65f-454">Married</span></span>              |
| <span data-ttu-id="fe65f-455">Tekli</span><span class="sxs-lookup"><span data-stu-id="fe65f-455">Single</span></span>                 | <span data-ttu-id="fe65f-456">Tekli</span><span class="sxs-lookup"><span data-stu-id="fe65f-456">Single</span></span>               |
| <span data-ttu-id="fe65f-457">Dul</span><span class="sxs-lookup"><span data-stu-id="fe65f-457">Widowed</span></span>                | <span data-ttu-id="fe65f-458">Dul</span><span class="sxs-lookup"><span data-stu-id="fe65f-458">Widowed</span></span>              |
| <span data-ttu-id="fe65f-459">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="fe65f-459">Divorced</span></span>               | <span data-ttu-id="fe65f-460">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="fe65f-460">Divorced</span></span>             |
| <span data-ttu-id="fe65f-461">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="fe65f-461">Registered Partnership</span></span> | <span data-ttu-id="fe65f-462">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="fe65f-462">Domestic Partnership</span></span> |
| <span data-ttu-id="fe65f-463">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="fe65f-463">None</span></span>                   | <span data-ttu-id="fe65f-464">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="fe65f-464">None</span></span>                 |
| <span data-ttu-id="fe65f-465">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="fe65f-465">Cohabiting</span></span>             | <span data-ttu-id="fe65f-466">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="fe65f-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="fe65f-467">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="fe65f-467">Gender</span></span>

<span data-ttu-id="fe65f-468">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="fe65f-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="fe65f-469">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="fe65f-470">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-470">Talent</span></span>       | <span data-ttu-id="fe65f-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="fe65f-472">Erkek</span><span class="sxs-lookup"><span data-stu-id="fe65f-472">Male</span></span>         | <span data-ttu-id="fe65f-473">Erkek</span><span class="sxs-lookup"><span data-stu-id="fe65f-473">Male</span></span>            |
| <span data-ttu-id="fe65f-474">Kadın</span><span class="sxs-lookup"><span data-stu-id="fe65f-474">Female</span></span>       | <span data-ttu-id="fe65f-475">Kadın</span><span class="sxs-lookup"><span data-stu-id="fe65f-475">Female</span></span>          |
| <span data-ttu-id="fe65f-476">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="fe65f-476">Non-specific</span></span> | <span data-ttu-id="fe65f-477">*Desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="fe65f-478">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="fe65f-478">Earning codes</span></span>

<span data-ttu-id="fe65f-479">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fe65f-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="fe65f-480">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="fe65f-481">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="fe65f-482">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="fe65f-482">Supported frequencies</span></span>

- <span data-ttu-id="fe65f-483">Tümü</span><span class="sxs-lookup"><span data-stu-id="fe65f-483">All</span></span>
- <span data-ttu-id="fe65f-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="fe65f-484">EVERYPAY</span></span>
- <span data-ttu-id="fe65f-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="fe65f-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="fe65f-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="fe65f-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="fe65f-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="fe65f-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="fe65f-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-488">1OFMTH</span></span>
- <span data-ttu-id="fe65f-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-489">LASTOFMTH</span></span>
- <span data-ttu-id="fe65f-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-490">2OFMTH</span></span>
- <span data-ttu-id="fe65f-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-491">3OFMTH</span></span>
- <span data-ttu-id="fe65f-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-492">4OFMTH</span></span>
- <span data-ttu-id="fe65f-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-493">5OFMTH</span></span>
- <span data-ttu-id="fe65f-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-494">1N2OFMTH</span></span>
- <span data-ttu-id="fe65f-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-495">3N4OFMTH</span></span>
- <span data-ttu-id="fe65f-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-496">1N3OFMTH</span></span>
- <span data-ttu-id="fe65f-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-497">1N4OFMTH</span></span>
- <span data-ttu-id="fe65f-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-498">2N3OFMTH</span></span>
- <span data-ttu-id="fe65f-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-499">2N4OFMTH</span></span>
- <span data-ttu-id="fe65f-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="fe65f-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="fe65f-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="fe65f-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="fe65f-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="fe65f-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="fe65f-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="fe65f-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="fe65f-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="fe65f-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="fe65f-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="fe65f-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="fe65f-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="fe65f-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="fe65f-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="fe65f-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="fe65f-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="fe65f-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="fe65f-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="fe65f-512">Adresler</span><span class="sxs-lookup"><span data-stu-id="fe65f-512">Addresses</span></span>

<span data-ttu-id="fe65f-513">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="fe65f-514">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="fe65f-515">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-515">Talent</span></span>          | <span data-ttu-id="fe65f-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="fe65f-517">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="fe65f-517">Country/Region</span></span>  | <span data-ttu-id="fe65f-518">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-518">Country Code</span></span>          |
| <span data-ttu-id="fe65f-519">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-519">Zip/Postal Code</span></span> | <span data-ttu-id="fe65f-520">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-520">Postal Code</span></span>           |
| <span data-ttu-id="fe65f-521">İl</span><span class="sxs-lookup"><span data-stu-id="fe65f-521">State</span></span>           | <span data-ttu-id="fe65f-522">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-522">State Code</span></span>            |
| <span data-ttu-id="fe65f-523">Şehir</span><span class="sxs-lookup"><span data-stu-id="fe65f-523">City</span></span>            | <span data-ttu-id="fe65f-524">Şehir</span><span class="sxs-lookup"><span data-stu-id="fe65f-524">City</span></span>                  |
| <span data-ttu-id="fe65f-525">İlçe</span><span class="sxs-lookup"><span data-stu-id="fe65f-525">County</span></span>          | <span data-ttu-id="fe65f-526">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="fe65f-526">County (Municipality)</span></span> |
| <span data-ttu-id="fe65f-527">Sokak</span><span class="sxs-lookup"><span data-stu-id="fe65f-527">Street</span></span>          | <span data-ttu-id="fe65f-528">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="fe65f-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="fe65f-529">Vergi bölgeleri</span><span class="sxs-lookup"><span data-stu-id="fe65f-529">Tax regions</span></span>

<span data-ttu-id="fe65f-530">Vergi bölgeleri, bordro oluşturma sırasında uygulanması gereken uygun vergiyi belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="fe65f-531">Vergi bölgeleri, Dayforce'a konum adresleri olarak eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="fe65f-532">Varsayılan vergi bölgesi, çalışanın etkin konumuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="fe65f-533">Vergi bölgesi (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-533">Tax region (required)</span></span>
- <span data-ttu-id="fe65f-534">Ülke/Bölge (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-534">Country/Region (required)</span></span>
- <span data-ttu-id="fe65f-535">İl (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-535">State (required)</span></span>
- <span data-ttu-id="fe65f-536">İlçe</span><span class="sxs-lookup"><span data-stu-id="fe65f-536">County</span></span> 
- <span data-ttu-id="fe65f-537">Şehir (gerekli)</span><span class="sxs-lookup"><span data-stu-id="fe65f-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="fe65f-538">Meksika'da bordro oluşturmak için verilerinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fe65f-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="fe65f-539">Meksika'da personel için ödeme oluşturuyorsanız aşağıdaki öğeler yapılandırılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="fe65f-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="fe65f-540">Pozisyonlarda departmanların olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-540">Departments are required on positions.</span></span>
- <span data-ttu-id="fe65f-541">Maliyet merkezleri mali boyut olarak ayarlanmalı ve Varsayılan Mali Boyut dizesindeki ilk öğe olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="fe65f-542">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="fe65f-542">Job types</span></span>

<span data-ttu-id="fe65f-543">Benzer işleri kategorilere gruplamak için iş türleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="fe65f-544">Meksika'da bordro işlemek için iş türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="fe65f-545">İş türü örnekleri arasında tam zamanlı ve yarı zamanlı veya maaş ve saatlik ödeme yer alır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="fe65f-546">İş türleri, personelin saatlik veya maaşlı olduğunu belirten ödeme türleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="fe65f-547">Aşağıdaki iş türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="fe65f-548">İş türü</span><span class="sxs-lookup"><span data-stu-id="fe65f-548">Job type</span></span>   | <span data-ttu-id="fe65f-549">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65f-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="fe65f-550">Saatlik</span><span class="sxs-lookup"><span data-stu-id="fe65f-550">Hourly</span></span>     | <span data-ttu-id="fe65f-551">MX Saatlik</span><span class="sxs-lookup"><span data-stu-id="fe65f-551">MX Hourly</span></span>   |
| <span data-ttu-id="fe65f-552">Maaşlı</span><span class="sxs-lookup"><span data-stu-id="fe65f-552">Salaried</span></span>   | <span data-ttu-id="fe65f-553">MX Maaşlı</span><span class="sxs-lookup"><span data-stu-id="fe65f-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="fe65f-554">Pozisyon türleri</span><span class="sxs-lookup"><span data-stu-id="fe65f-554">Position types</span></span> 

<span data-ttu-id="fe65f-555">Pozisyonun tam zamanlı, yarı zamanlı veya başka bir pozisyon olduğunu tanımlamak için pozisyon türlerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="fe65f-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="fe65f-556">Pozisyon türleri, personelin tam zamanlı veya yarı zamanlı olduğunu belirten ödeme sınıfları olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="fe65f-557">Aşağıdaki pozisyon türleri ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="fe65f-558">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="fe65f-558">Position type</span></span>   | <span data-ttu-id="fe65f-559">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65f-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="fe65f-560">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="fe65f-560">Full-time</span></span>       | <span data-ttu-id="fe65f-561">Tam zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="fe65f-561">Full time employee</span></span> |
| <span data-ttu-id="fe65f-562">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="fe65f-562">Part-time</span></span>       | <span data-ttu-id="fe65f-563">Yarı zamanlı personel</span><span class="sxs-lookup"><span data-stu-id="fe65f-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="fe65f-564">Neden kodları</span><span class="sxs-lookup"><span data-stu-id="fe65f-564">Reason codes</span></span>

<span data-ttu-id="fe65f-565">Neden kodları personelin durumu hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="fe65f-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="fe65f-566">Neden kodları, personelin pozisyonunda veya istihdam durumundaki değişikliklerin nedenini belirten durum nedenleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="fe65f-567">Aşağıdaki neden kodları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="fe65f-568">Neden kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-568">Reason code</span></span>            | <span data-ttu-id="fe65f-569">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65f-569">Description</span></span>                    | <span data-ttu-id="fe65f-570">Uygulanabilir senaryolar</span><span class="sxs-lookup"><span data-stu-id="fe65f-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="fe65f-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="fe65f-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="fe65f-572">İlk bordrodan önce ayrılma</span><span class="sxs-lookup"><span data-stu-id="fe65f-572">Departure before first payroll</span></span> | <span data-ttu-id="fe65f-573">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-573">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="fe65f-574">RESIGNATION</span></span>            | <span data-ttu-id="fe65f-575">İstifa</span><span class="sxs-lookup"><span data-stu-id="fe65f-575">Resignation</span></span>                    | <span data-ttu-id="fe65f-576">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-576">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="fe65f-577">PENSION</span></span>                | <span data-ttu-id="fe65f-578">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="fe65f-578">Pension</span></span>                        | <span data-ttu-id="fe65f-579">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-579">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="fe65f-580">TERMINATION</span></span>            | <span data-ttu-id="fe65f-581">Bitiş</span><span class="sxs-lookup"><span data-stu-id="fe65f-581">Termination</span></span>                    | <span data-ttu-id="fe65f-582">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-582">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="fe65f-583">RETIREMENT</span></span>             | <span data-ttu-id="fe65f-584">Emeklilik</span><span class="sxs-lookup"><span data-stu-id="fe65f-584">Retirement</span></span>                     | <span data-ttu-id="fe65f-585">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-585">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="fe65f-586">ABSENTEE</span></span>               | <span data-ttu-id="fe65f-587">Devamsızlık</span><span class="sxs-lookup"><span data-stu-id="fe65f-587">Absentee</span></span>                       | <span data-ttu-id="fe65f-588">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-588">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-589">OTHER</span><span class="sxs-lookup"><span data-stu-id="fe65f-589">OTHER</span></span>                  | <span data-ttu-id="fe65f-590">Diğer Nedenler</span><span class="sxs-lookup"><span data-stu-id="fe65f-590">Other Reasons</span></span>                  | <span data-ttu-id="fe65f-591">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-591">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="fe65f-592">CLOSURE</span></span>                | <span data-ttu-id="fe65f-593">İşletmenin Kapanması</span><span class="sxs-lookup"><span data-stu-id="fe65f-593">Business Closure</span></span>               | <span data-ttu-id="fe65f-594">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-594">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="fe65f-595">DEATH</span></span>                  | <span data-ttu-id="fe65f-596">Ölüm</span><span class="sxs-lookup"><span data-stu-id="fe65f-596">Death</span></span>                          | <span data-ttu-id="fe65f-597">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-597">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="fe65f-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="fe65f-599">İzin</span><span class="sxs-lookup"><span data-stu-id="fe65f-599">Leave of Absence</span></span>               | <span data-ttu-id="fe65f-600">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-600">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="fe65f-601">CONTRACTEND</span></span>            | <span data-ttu-id="fe65f-602">Sözleşme Bitişi</span><span class="sxs-lookup"><span data-stu-id="fe65f-602">End of Contract</span></span>                | <span data-ttu-id="fe65f-603">Çalışanı işten çıkar</span><span class="sxs-lookup"><span data-stu-id="fe65f-603">Terminate worker</span></span>     |
| <span data-ttu-id="fe65f-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="fe65f-604">SALARYCHANGE</span></span>           | <span data-ttu-id="fe65f-605">Maaş Değişikliği</span><span class="sxs-lookup"><span data-stu-id="fe65f-605">Change of Salary</span></span>               | <span data-ttu-id="fe65f-606">Ücret</span><span class="sxs-lookup"><span data-stu-id="fe65f-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="fe65f-607">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="fe65f-607">Terms of employment</span></span>

<span data-ttu-id="fe65f-608">İstihdam koşulları, istihdam koşullarının kategorilerini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="fe65f-609">Koşullar, istihdam göstergesi değerleri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="fe65f-610">Aşağıdaki istihdam koşulları ve açıklamalar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="fe65f-611">Çalışma koşulları</span><span class="sxs-lookup"><span data-stu-id="fe65f-611">Terms of employment</span></span>   | <span data-ttu-id="fe65f-612">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe65f-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="fe65f-613">Normal</span><span class="sxs-lookup"><span data-stu-id="fe65f-613">Regular</span></span>               | <span data-ttu-id="fe65f-614">Normal</span><span class="sxs-lookup"><span data-stu-id="fe65f-614">Regular</span></span>     |
| <span data-ttu-id="fe65f-615">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="fe65f-615">Direct</span></span>                | <span data-ttu-id="fe65f-616">Doğrudan</span><span class="sxs-lookup"><span data-stu-id="fe65f-616">Direct</span></span>      |
| <span data-ttu-id="fe65f-617">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="fe65f-617">Internship</span></span>            | <span data-ttu-id="fe65f-618">Stajyerlik</span><span class="sxs-lookup"><span data-stu-id="fe65f-618">Internship</span></span>  |
| <span data-ttu-id="fe65f-619">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="fe65f-619">Permanent</span></span>             | <span data-ttu-id="fe65f-620">Kalıcı</span><span class="sxs-lookup"><span data-stu-id="fe65f-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="fe65f-621">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="fe65f-621">Marital status</span></span>

<span data-ttu-id="fe65f-622">Medeni durum değerleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="fe65f-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="fe65f-623">Aşağıdaki tabloda medeni durum değerlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="fe65f-624">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-624">Talent</span></span>                 | <span data-ttu-id="fe65f-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="fe65f-626">Evli</span><span class="sxs-lookup"><span data-stu-id="fe65f-626">Married</span></span>                | <span data-ttu-id="fe65f-627">Evli</span><span class="sxs-lookup"><span data-stu-id="fe65f-627">Married</span></span>                   |
| <span data-ttu-id="fe65f-628">Tekli</span><span class="sxs-lookup"><span data-stu-id="fe65f-628">Single</span></span>                 | <span data-ttu-id="fe65f-629">Tekli</span><span class="sxs-lookup"><span data-stu-id="fe65f-629">Single</span></span>                    |
| <span data-ttu-id="fe65f-630">Dul</span><span class="sxs-lookup"><span data-stu-id="fe65f-630">Widowed</span></span>                | <span data-ttu-id="fe65f-631">Dul</span><span class="sxs-lookup"><span data-stu-id="fe65f-631">Widowed</span></span>                   |
| <span data-ttu-id="fe65f-632">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="fe65f-632">Divorced</span></span>               | <span data-ttu-id="fe65f-633">Boşanmış</span><span class="sxs-lookup"><span data-stu-id="fe65f-633">Divorced</span></span>                  |
| <span data-ttu-id="fe65f-634">Tescilli Birliktelik</span><span class="sxs-lookup"><span data-stu-id="fe65f-634">Registered Partnership</span></span> | <span data-ttu-id="fe65f-635">Medeni Birliktelik</span><span class="sxs-lookup"><span data-stu-id="fe65f-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="fe65f-636">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="fe65f-636">None</span></span>                   | <span data-ttu-id="fe65f-637">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="fe65f-638">Birlikte yaşıyor</span><span class="sxs-lookup"><span data-stu-id="fe65f-638">Cohabiting</span></span>             | <span data-ttu-id="fe65f-639">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="fe65f-640">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="fe65f-640">Gender</span></span>

<span data-ttu-id="fe65f-641">Cinsiyet gösterimleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="fe65f-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="fe65f-642">Aşağıdaki tabloda cinsiyet gösterimlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="fe65f-643">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-643">Talent</span></span>       | <span data-ttu-id="fe65f-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="fe65f-645">Erkek</span><span class="sxs-lookup"><span data-stu-id="fe65f-645">Male</span></span>         | <span data-ttu-id="fe65f-646">Erkek</span><span class="sxs-lookup"><span data-stu-id="fe65f-646">Male</span></span>                      |
| <span data-ttu-id="fe65f-647">Kadın</span><span class="sxs-lookup"><span data-stu-id="fe65f-647">Female</span></span>       | <span data-ttu-id="fe65f-648">Kadın</span><span class="sxs-lookup"><span data-stu-id="fe65f-648">Female</span></span>                    |
| <span data-ttu-id="fe65f-649">Özgün değil</span><span class="sxs-lookup"><span data-stu-id="fe65f-649">Non-specific</span></span> | <span data-ttu-id="fe65f-650">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="fe65f-651">Ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="fe65f-651">Payment method</span></span>

<span data-ttu-id="fe65f-652">Ödeme yöntemleri, personele ve şirkete çalışanlara nasıl ödeme yapılacağını tanımlamak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="fe65f-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="fe65f-653">Ödeme yöntemleri Dayforce'a eşlenir ve tümleştirme işleminden sonra uygunsa kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="fe65f-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="fe65f-654">Aşağıdaki tabloda ödeme yöntemlerinin Dayforce'a nasıl eşlendiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="fe65f-655">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-655">Talent</span></span>             | <span data-ttu-id="fe65f-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="fe65f-657">Nakit</span><span class="sxs-lookup"><span data-stu-id="fe65f-657">Cash</span></span>               | <span data-ttu-id="fe65f-658">Nakit</span><span class="sxs-lookup"><span data-stu-id="fe65f-658">Cash</span></span>                      |
| <span data-ttu-id="fe65f-659">Elektronik Ödeme</span><span class="sxs-lookup"><span data-stu-id="fe65f-659">Electronic Payment</span></span> | <span data-ttu-id="fe65f-660">Transfer et</span><span class="sxs-lookup"><span data-stu-id="fe65f-660">Transfer</span></span>                  |
| <span data-ttu-id="fe65f-661">Denetle</span><span class="sxs-lookup"><span data-stu-id="fe65f-661">Check</span></span>              | <span data-ttu-id="fe65f-662">Çek</span><span class="sxs-lookup"><span data-stu-id="fe65f-662">Cheque</span></span>                    |
| <span data-ttu-id="fe65f-663">Banka Ödeme Emri</span><span class="sxs-lookup"><span data-stu-id="fe65f-663">Bank Draft</span></span>         | <span data-ttu-id="fe65f-664">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="fe65f-665">Diğer</span><span class="sxs-lookup"><span data-stu-id="fe65f-665">Other</span></span>              | <span data-ttu-id="fe65f-666">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="fe65f-667">Banka hesabı türü</span><span class="sxs-lookup"><span data-stu-id="fe65f-667">Bank account type</span></span>

<span data-ttu-id="fe65f-668">Banka hesap türleri, personele elektronik ödeme yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="fe65f-669">Banka hesap türleri, transfer hesabı bilgileri olarak Dayforce'a eşlenir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="fe65f-670">Banka hesap türleri, uygunsa tümleştirme işleminden sonra kabul edilen değerlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="fe65f-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="fe65f-671">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-671">Talent</span></span>            | <span data-ttu-id="fe65f-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="fe65f-673">Cari Hesap</span><span class="sxs-lookup"><span data-stu-id="fe65f-673">Checking Account</span></span>  | <span data-ttu-id="fe65f-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="fe65f-674">CheckingAccount</span></span>           |
| <span data-ttu-id="fe65f-675">Bordro Hesabı</span><span class="sxs-lookup"><span data-stu-id="fe65f-675">Payroll Account</span></span>   | <span data-ttu-id="fe65f-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="fe65f-676">PayrollAccount</span></span>            |
| <span data-ttu-id="fe65f-677">Tasarruf Hesabı</span><span class="sxs-lookup"><span data-stu-id="fe65f-677">Savings Account</span></span>   | <span data-ttu-id="fe65f-678">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="fe65f-679">BankGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="fe65f-679">BankGirot account</span></span> | <span data-ttu-id="fe65f-680">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="fe65f-681">PlusGirot hesabı</span><span class="sxs-lookup"><span data-stu-id="fe65f-681">PlusGirot account</span></span> | <span data-ttu-id="fe65f-682">*Meksika'da desteklenmez*</span><span class="sxs-lookup"><span data-stu-id="fe65f-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="fe65f-683">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="fe65f-683">Earning codes</span></span>

<span data-ttu-id="fe65f-684">Kazanç kodları, çalışanların aldığı her tür kazancı benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fe65f-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="fe65f-685">Kodlar, muhasebe kuralları, vergi kanunları, raporlama gereksinimleri ve brütleştirme özelliği gibi kazançlarla ilgili çeşitli parametreleri içerir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="fe65f-686">Desteklenmeyen bir sıklık kullanılıyorsa hesaplama için **Her Ödeme** sıklığı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe65f-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="fe65f-687">Desteklenen sıklıklar</span><span class="sxs-lookup"><span data-stu-id="fe65f-687">Supported frequencies</span></span>

- <span data-ttu-id="fe65f-688">Tümü</span><span class="sxs-lookup"><span data-stu-id="fe65f-688">All</span></span>
- <span data-ttu-id="fe65f-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="fe65f-689">EVERYPAY</span></span>
- <span data-ttu-id="fe65f-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="fe65f-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="fe65f-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="fe65f-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="fe65f-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="fe65f-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="fe65f-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-693">1OFMTH</span></span>
- <span data-ttu-id="fe65f-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-694">LASTOFMTH</span></span>
- <span data-ttu-id="fe65f-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-695">2OFMTH</span></span>
- <span data-ttu-id="fe65f-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-696">3OFMTH</span></span>
- <span data-ttu-id="fe65f-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-697">4OFMTH</span></span>
- <span data-ttu-id="fe65f-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-698">5OFMTH</span></span>
- <span data-ttu-id="fe65f-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-699">1N2OFMTH</span></span>
- <span data-ttu-id="fe65f-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-700">3N4OFMTH</span></span>
- <span data-ttu-id="fe65f-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-701">1N3OFMTH</span></span>
- <span data-ttu-id="fe65f-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-702">1N4OFMTH</span></span>
- <span data-ttu-id="fe65f-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-703">2N3OFMTH</span></span>
- <span data-ttu-id="fe65f-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-704">2N4OFMTH</span></span>
- <span data-ttu-id="fe65f-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="fe65f-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="fe65f-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="fe65f-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="fe65f-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="fe65f-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="fe65f-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="fe65f-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="fe65f-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="fe65f-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="fe65f-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="fe65f-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="fe65f-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="fe65f-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="fe65f-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="fe65f-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="fe65f-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="fe65f-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="fe65f-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="fe65f-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="fe65f-717">Adresler</span><span class="sxs-lookup"><span data-stu-id="fe65f-717">Addresses</span></span>

<span data-ttu-id="fe65f-718">Belirli ülke veya bölge, il ve ilçe (belediye) kodlarının tanımlanması için Dayforce'un ve ülke içi/bölge içi sağlayıcıların tanıyabileceği belirli biçimler gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="fe65f-719">Şehirlere ilişkin biçim esnek olmasına rağmen, her şehir bir ille ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="fe65f-720">Talent</span><span class="sxs-lookup"><span data-stu-id="fe65f-720">Talent</span></span>              | <span data-ttu-id="fe65f-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="fe65f-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="fe65f-722">Ülke/Bölge</span><span class="sxs-lookup"><span data-stu-id="fe65f-722">Country/Region</span></span>      | <span data-ttu-id="fe65f-723">Ülke Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-723">Country Code</span></span>          |
| <span data-ttu-id="fe65f-724">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-724">Zip/Postal Code</span></span>     | <span data-ttu-id="fe65f-725">Posta Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-725">Postal Code</span></span>           |
| <span data-ttu-id="fe65f-726">İl</span><span class="sxs-lookup"><span data-stu-id="fe65f-726">State</span></span>               | <span data-ttu-id="fe65f-727">İl Kodu</span><span class="sxs-lookup"><span data-stu-id="fe65f-727">State Code</span></span>            |
| <span data-ttu-id="fe65f-728">Şehir</span><span class="sxs-lookup"><span data-stu-id="fe65f-728">City</span></span>                | <span data-ttu-id="fe65f-729">Şehir</span><span class="sxs-lookup"><span data-stu-id="fe65f-729">City</span></span>                  |
| <span data-ttu-id="fe65f-730">İlçe</span><span class="sxs-lookup"><span data-stu-id="fe65f-730">County</span></span>              | <span data-ttu-id="fe65f-731">İlçe (Belediye)</span><span class="sxs-lookup"><span data-stu-id="fe65f-731">County (Municipality)</span></span> |
| <span data-ttu-id="fe65f-732">Sokak</span><span class="sxs-lookup"><span data-stu-id="fe65f-732">Street</span></span>              | <span data-ttu-id="fe65f-733">Adres Satırı 1</span><span class="sxs-lookup"><span data-stu-id="fe65f-733">Address Line 1</span></span>        |
| <span data-ttu-id="fe65f-734">Cadde Numarası</span><span class="sxs-lookup"><span data-stu-id="fe65f-734">Street Number</span></span>       | <span data-ttu-id="fe65f-735">Adres Satırı 2</span><span class="sxs-lookup"><span data-stu-id="fe65f-735">Address Line 2</span></span>        |
| <span data-ttu-id="fe65f-736">Bina Tamamlayıcı</span><span class="sxs-lookup"><span data-stu-id="fe65f-736">Building Complement</span></span> | <span data-ttu-id="fe65f-737">Adres Satırı 5</span><span class="sxs-lookup"><span data-stu-id="fe65f-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="fe65f-738">Pasaport numarası</span><span class="sxs-lookup"><span data-stu-id="fe65f-738">Passport number</span></span>

<span data-ttu-id="fe65f-739">Personel pasaport bilgilerini bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-739">Employees can declare passport information.</span></span> <span data-ttu-id="fe65f-740">Bu bilgiler, **Pasaport** kimlik türünü içerir ve Meksika'ya özel personel bilgilerinin bir parçası olarak Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="fe65f-741">Kimlik Türü = "Pasaport"</span><span class="sxs-lookup"><span data-stu-id="fe65f-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="fe65f-742">Verildiği Tarih</span><span class="sxs-lookup"><span data-stu-id="fe65f-742">Issued Date</span></span>
- <span data-ttu-id="fe65f-743">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="fe65f-743">Expiration Date</span></span>

<span data-ttu-id="fe65f-744">Personel, **Pasaport** kimlik türü için birden fazla kimlik numarası bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="fe65f-745">Ancak yalnızca geçerli etkin pasaport girişi Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="fe65f-746">Tüm pasaport girişlerinin süresi dolmuşsa en son verilen pasaport Dayforce'a tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fe65f-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

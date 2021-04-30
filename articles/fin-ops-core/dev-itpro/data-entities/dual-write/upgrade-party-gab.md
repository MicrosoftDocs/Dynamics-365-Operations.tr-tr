---
title: Taraf ve genel adres defteri modeline yükseltme
description: Bu konuda, çift yazma verilerinin taraf ve genel adres defteri modeline nasıl yükseltileceği açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 76e64d483e833782733277a64d8dc37cbeba6130
ms.sourcegitcommit: 011468a6cffea8641bebc2922e0676d9f44b36fc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857382"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="1e847-103">Taraf ve genel adres defteri modeline yükseltme</span><span class="sxs-lookup"><span data-stu-id="1e847-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1e847-104">[Azure Data Factory template](https://aka.ms/dual-write-gab-adf), çift yazmadaki mevcut **Hesap**, **İlgili Kişi** ve **Satıcı** tablo verilerini taraf ve genel adres defteri modeline yükseltmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1e847-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="1e847-105">Şablon, Finance and Operations uygulamaları ve müşteri etkileşimi uygulamalarındaki veriler arasında mutabakat sağlar.</span><span class="sxs-lookup"><span data-stu-id="1e847-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="1e847-106">İşlemin sonunda, **Taraf** kayıtlarına ait **Taraf** ve **İlgili Kişi** alanları oluşturulur ve müşteri etkileşimi uygulamalarındaki **Hesap**, **İLgili Kişi** ve **Satıcı** kayıtlarıyla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="1e847-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="1e847-107">Finance and Operations uygulaması içinde yeni **Taraf** kayıtları oluşturmak için bir .csv dosyası (`FONewParty.csv`) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1e847-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="1e847-108">Bu konu, Data Factory şablonunu kullanma ve verilerinizi yükseltme yönergelerini sağlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="1e847-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="1e847-109">Herhangi bir özelleştirmeleriniz yoksa, şablonu olduğu gibi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e847-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="1e847-110">**Hesap**, **İlgili Kişi** ve **Satıcı** için özelleştirmeleriniz varsa aşağıdaki yönergeleri kullanarak şablonu değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1e847-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="1e847-111">Şablon yalnızca **Taraf** verilerini yükseltmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1e847-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="1e847-112">Gelecek bir sürümde, posta ve elektronik adresler de dahil edilecektir.</span><span class="sxs-lookup"><span data-stu-id="1e847-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e847-113">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="1e847-113">Prerequisites</span></span>

<span data-ttu-id="1e847-114">Bu önkoşullar gereklidir:</span><span class="sxs-lookup"><span data-stu-id="1e847-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="1e847-115">Azure aboneliği</span><span class="sxs-lookup"><span data-stu-id="1e847-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="1e847-116">Şablona erişim</span><span class="sxs-lookup"><span data-stu-id="1e847-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="1e847-117">Mevcut bir çift yazma müşterisi olmak.</span><span class="sxs-lookup"><span data-stu-id="1e847-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="1e847-118">Yükseltmek için hazırlık</span><span class="sxs-lookup"><span data-stu-id="1e847-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="1e847-119">**Tamamen eşitlenmiş**: Her iki ortam **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** için tamamen eşitlenmiş durumda.</span><span class="sxs-lookup"><span data-stu-id="1e847-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="1e847-120">**Tümleştirme anahtarları**: Müşteri etkileşimi uygulamalarındaki **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** tabloları kullanıma hazır gönderilen tümleştirme anahtarlarını kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="1e847-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="1e847-121">Tümleştirme anahtarlarını özelleştirdiyseniz, şablonu özelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1e847-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="1e847-122">**Taraf numarası**: Yükseltilecek tüm **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** kayıtlarında bir **Taraf** numarası bulunur.</span><span class="sxs-lookup"><span data-stu-id="1e847-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="1e847-123">**Taraf** numarası olmayan kayıtlar yok sayılır.</span><span class="sxs-lookup"><span data-stu-id="1e847-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="1e847-124">Bu kayıtları yükseltmek istiyorsanız, yükseltme işlemine başlamadan önce onlara bir **Taraf** numarası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1e847-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="1e847-125">**Sistem kesintisi**: Yükseltme işlemi sırasında, hem Finance and Operations hem de müşteri etkileşimi uygulamalarını çevrimdışına almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1e847-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="1e847-126">**Anlık görüntü**: Hem Finance and Operations hem de müşteri etkileşimi uygulamalarının anlık görüntüsünü alın.</span><span class="sxs-lookup"><span data-stu-id="1e847-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="1e847-127">Gerekirse önceki durumu geri yüklemek için anlık görüntüleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="1e847-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="1e847-128">Dağıtım</span><span class="sxs-lookup"><span data-stu-id="1e847-128">Deployment</span></span>

1. <span data-ttu-id="1e847-129">[Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) konumundan şablonu indirin.</span><span class="sxs-lookup"><span data-stu-id="1e847-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="1e847-130">[Microsoft Azure](https://portal.azure.com/)'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1e847-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="1e847-131">[Kaynak grubu](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1e847-131">Create a [resource group](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="1e847-132">Oluşturduğunuz kaynak grubunda bir [depolama hesabı](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1e847-132">Create a [storage account](https://docs.microsoft.com/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="1e847-133">Yukarıda oluşturduğunuz kaynak grubunda bir [veri fabrikası](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1e847-133">Create a [data factory](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="1e847-134">Veri fabrikasını açın ve **Yaz ve İzle** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1e847-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="1e847-135">**Yönet** sekmesinde **ARM şablonu** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1e847-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="1e847-136">**Taraf** şablonunu içe aktarmak için **ARM şablonunu içer aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1e847-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="1e847-137">Şablonu veri fabrikasına aktarın.</span><span class="sxs-lookup"><span data-stu-id="1e847-137">Import the template into the data factory.</span></span> <span data-ttu-id="1e847-138">**Proje ayrıntıları** ve **Kurulum ayrıntıları** için aşağıdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="1e847-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="1e847-139">Alan</span><span class="sxs-lookup"><span data-stu-id="1e847-139">Field</span></span> | <span data-ttu-id="1e847-140">Değer</span><span class="sxs-lookup"><span data-stu-id="1e847-140">Value</span></span>
    ---|---
    <span data-ttu-id="1e847-141">Abonelik</span><span class="sxs-lookup"><span data-stu-id="1e847-141">Subscription</span></span> | <span data-ttu-id="1e847-142">Azure aboneliği</span><span class="sxs-lookup"><span data-stu-id="1e847-142">Azure subscription</span></span>
    <span data-ttu-id="1e847-143">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="1e847-143">Resource group</span></span> | <span data-ttu-id="1e847-144">Altında depolama hesabı oluşturulan kaynağı sağlayın.</span><span class="sxs-lookup"><span data-stu-id="1e847-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="1e847-145">Bölge</span><span class="sxs-lookup"><span data-stu-id="1e847-145">Region</span></span> | <span data-ttu-id="1e847-146">Bölge belirtin.</span><span class="sxs-lookup"><span data-stu-id="1e847-146">Specify region.</span></span>
    <span data-ttu-id="1e847-147">Fabrika Adı</span><span class="sxs-lookup"><span data-stu-id="1e847-147">Factory Name</span></span> | <span data-ttu-id="1e847-148">Fabrika adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1e847-148">Specify factory name.</span></span>
    <span data-ttu-id="1e847-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="1e847-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="1e847-150">Uygulamanın anahtarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1e847-150">Specify the application's key.</span></span>
    <span data-ttu-id="1e847-151">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="1e847-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="1e847-152">Azure Blob depolama bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="1e847-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="1e847-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="1e847-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="1e847-154">Kullanıcı adı olarak belirttiğiniz kullanıcı hesabının parolası.</span><span class="sxs-lookup"><span data-stu-id="1e847-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="1e847-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="1e847-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="1e847-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="1e847-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="1e847-157">Uygulamanızın altında bulunduğu kiracı bilgilerini (etki alanı adı veya kiracı kimliği) belirtin.</span><span class="sxs-lookup"><span data-stu-id="1e847-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="1e847-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="1e847-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="1e847-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="1e847-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="1e847-160">Uygulamanın istemci kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1e847-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="1e847-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="1e847-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="1e847-162">Dynamics'e bağlanmak için kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="1e847-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="1e847-163">Daha fazla bilgi için bkz. [Her ortam için el ile bir Resource Manager şablonu yükseltme](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Bağlantılı hizmet özellikleri](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties) ve [Azure Data Factory kullanarak veri kopyalama](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="1e847-163">For more information, see [Manually promote a Resource Manager template for each environment](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](https://docs.microsoft.com/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="1e847-164">Dağıtımdan sonra, veri fabrikasının bağlantılı hizmetini, veri kümelerini ve veri akışını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="1e847-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Veri kümeleri, veri akışı ve bağlantılı hizmet](media/data-factory-validate.png)

11. <span data-ttu-id="1e847-166">**Yönet**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1e847-166">Navigate to **Manage**.</span></span> <span data-ttu-id="1e847-167">**Bağlantılar** altından, **Bağlantılı Hizmet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1e847-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="1e847-168">**DynamicsCrmLinkedService** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1e847-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="1e847-169">**Bağlantılı hizmeti düzenle ( Dynamics CRM)** formuna aşağıdaki değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="1e847-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="1e847-170">Alan</span><span class="sxs-lookup"><span data-stu-id="1e847-170">Field</span></span> | <span data-ttu-id="1e847-171">Değer</span><span class="sxs-lookup"><span data-stu-id="1e847-171">Value</span></span>
    ---|---
    <span data-ttu-id="1e847-172">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="1e847-172">Name</span></span> | <span data-ttu-id="1e847-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="1e847-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="1e847-174">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e847-174">Description</span></span> | <span data-ttu-id="1e847-175">Varlık verilerini getirmek üzere CRM kurulumuyla bağlantı kurulacak bağlantılı hizmetler</span><span class="sxs-lookup"><span data-stu-id="1e847-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="1e847-176">Tümleştirme çalışma zamanı aracılığıyla bağlan</span><span class="sxs-lookup"><span data-stu-id="1e847-176">Connect via integration runtime</span></span> | <span data-ttu-id="1e847-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e847-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="1e847-178">Dağıtım türü</span><span class="sxs-lookup"><span data-stu-id="1e847-178">Deployment type</span></span> | <span data-ttu-id="1e847-179">Çevrimiçi</span><span class="sxs-lookup"><span data-stu-id="1e847-179">Online</span></span>
    <span data-ttu-id="1e847-180">Hizmet URI'si</span><span class="sxs-lookup"><span data-stu-id="1e847-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="1e847-181">Kimlik doğrulaması türü</span><span class="sxs-lookup"><span data-stu-id="1e847-181">Authentication type</span></span> | <span data-ttu-id="1e847-182">Office365</span><span class="sxs-lookup"><span data-stu-id="1e847-182">Office365</span></span>
    <span data-ttu-id="1e847-183">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="1e847-183">User name</span></span> |
    <span data-ttu-id="1e847-184">Parola veya Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e847-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="1e847-185">Parola</span><span class="sxs-lookup"><span data-stu-id="1e847-185">Password</span></span>
    <span data-ttu-id="1e847-186">Parola</span><span class="sxs-lookup"><span data-stu-id="1e847-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="1e847-187">Şablonu çalıştır</span><span class="sxs-lookup"><span data-stu-id="1e847-187">Run the template</span></span>

1. <span data-ttu-id="1e847-188">Finance and Operations uygulamasını kullanarak aşağıdaki **Hesap**, **İlgili Kişi** ve **Satıcı** çift yazmasını durdurun.</span><span class="sxs-lookup"><span data-stu-id="1e847-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="1e847-189">Müşteriler V3 (hesaplar)</span><span class="sxs-lookup"><span data-stu-id="1e847-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="1e847-190">Müşteriler V3(ilgili kişiler)</span><span class="sxs-lookup"><span data-stu-id="1e847-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="1e847-191">CDS İlgili Kişileri V2(ilgili kişiler)</span><span class="sxs-lookup"><span data-stu-id="1e847-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="1e847-192">CDS İlgili Kişileri V2(ilgili kişiler)</span><span class="sxs-lookup"><span data-stu-id="1e847-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="1e847-193">Satıcı V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="1e847-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="1e847-194">Dataverse'de haritaların `msdy_dualwriteruntimeconfig` tablosundan kaldırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="1e847-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="1e847-195">AppSource'tan [Çift Yazma Taraf ve Genel Adres Defteri Çözümleri](https://aka.ms/dual-write-gab)'ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="1e847-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="1e847-196">Finance and Operations uygulamasında, aşağıdaki tablolar veri içeriyorsa bu tablolar için **Başlangıç Eşitlemesi**'ni çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1e847-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="1e847-197">Selamlamalar</span><span class="sxs-lookup"><span data-stu-id="1e847-197">Salutations</span></span>
    + <span data-ttu-id="1e847-198">Kişisel karakter türleri</span><span class="sxs-lookup"><span data-stu-id="1e847-198">Personal character types</span></span>
    + <span data-ttu-id="1e847-199">Kapanış sözleri</span><span class="sxs-lookup"><span data-stu-id="1e847-199">Complimentary closing</span></span>
    + <span data-ttu-id="1e847-200">İlgili kişi unvanları</span><span class="sxs-lookup"><span data-stu-id="1e847-200">Contact person titles</span></span>
    + <span data-ttu-id="1e847-201">Karar verici roller</span><span class="sxs-lookup"><span data-stu-id="1e847-201">Decision making roles</span></span>
    + <span data-ttu-id="1e847-202">Bağlılık programı düzeyleri</span><span class="sxs-lookup"><span data-stu-id="1e847-202">Loyalty levels</span></span>

5. <span data-ttu-id="1e847-203">Müşteri etkileşimi uygulamasında aşağıdaki eklenti adımlarını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="1e847-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="1e847-204">Hesap Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-204">Account Update</span></span>
         + <span data-ttu-id="1e847-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Hesap güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="1e847-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Hesap güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="1e847-207">İlgili Kişi Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-207">Contact Update</span></span>
         + <span data-ttu-id="1e847-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: İlgili kişi güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="1e847-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: İlgili kişi güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="1e847-210">msdyn_party Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-210">msdyn_party Update</span></span>
         + <span data-ttu-id="1e847-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="1e847-212">msdyn_vendor Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="1e847-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="1e847-214">Müşteri etkileşimi uygulamasında aşağıdaki iş akışlarını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="1e847-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="1e847-215">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e847-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e847-216">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e847-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e847-217">İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e847-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="1e847-218">Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e847-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="1e847-219">Hesaplar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e847-220">Satıcılar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="1e847-221">İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="1e847-222">Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="1e847-223">Veri fabrikasında, aşağıdaki görüntüde gösterildiği şekilde **Şimdi tetikle**'yi seçerek şablonu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1e847-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="1e847-224">Bu işlemin tamamlanması veri hacmine göre birkaç saat sürebilir.</span><span class="sxs-lookup"><span data-stu-id="1e847-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Tetik çalıştırması](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="1e847-226">**Hesap**, **İlgili Kişi** ve **Satıcı** için özelleştirmeleriniz varsa şablonu değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1e847-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="1e847-227">Finance and Operations uygulamasında yeni **Taraf** kayıtlarını içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="1e847-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="1e847-228">Azure blob depolamadan `FONewParty.csv` dosyasını indirin.</span><span class="sxs-lookup"><span data-stu-id="1e847-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="1e847-229">Yol: `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="1e847-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="1e847-230">`FONewParty.csv` dosyasını bir Excel dosyasına dönüştürüp Excel dosyasını Finance and Operations uygulamasına aktarın.</span><span class="sxs-lookup"><span data-stu-id="1e847-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="1e847-231">csv içe aktarma işlemi sizin için uygunsa, csv dosyasını doğrudan içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e847-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="1e847-232">Veri hacmine bağlı olarak içe aktarma birkaç saat sürebilir.</span><span class="sxs-lookup"><span data-stu-id="1e847-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="1e847-233">Daha fazla bilgi için bkz. [Verileri içeri ve dışarı aktarma işlerine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span><span class="sxs-lookup"><span data-stu-id="1e847-233">For more information, see [Data import and export jobs overview](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job).</span></span>

    ![Dataverse taraf kayıtlarını içe aktarma](media/data-factory-import-party.png)

9. <span data-ttu-id="1e847-235">Müşteri etkileşimi uygulamalarında aşağıdaki eklenti adımlarını devre dışı etkinleştirin:</span><span class="sxs-lookup"><span data-stu-id="1e847-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="1e847-236">Hesap Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-236">Account Update</span></span>
         + <span data-ttu-id="1e847-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Hesap güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="1e847-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Hesap güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="1e847-239">İlgili Kişi Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-239">Contact Update</span></span>
         + <span data-ttu-id="1e847-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: İlgili kişi güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="1e847-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: İlgili kişi güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="1e847-242">msdyn_party Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-242">msdyn_party Update</span></span>
         + <span data-ttu-id="1e847-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="1e847-244">msdyn_vendor Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="1e847-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1e847-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="1e847-246">Müşteri etkileşimi uygulamalarında, önceki adımlarda devre dışı bıraktıysanız aşağıdaki iş akışlarını etkinleştirin:</span><span class="sxs-lookup"><span data-stu-id="1e847-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="1e847-247">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e847-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e847-248">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e847-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e847-249">İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e847-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="1e847-250">Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e847-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="1e847-251">Hesaplar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="1e847-252">Satıcılar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="1e847-253">İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="1e847-254">Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1e847-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="1e847-255">**Taraf** ile ilgili haritaları [Taraf ve genel adres defteri](party-gab.md)'nde belirtildiği şekilde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1e847-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1e847-256">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="1e847-256">Troubleshooting</span></span>

1. <span data-ttu-id="1e847-257">İşlem başarısız olursa, başarısız olan etkinlikten başlayarak veri fabrikasını yeniden çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1e847-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="1e847-258">Bazı dosyalar veri doğrulama amacıyla kullanabileceğiniz veri fabrikası tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1e847-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="1e847-259">Veri fabrikası, virgülle sınırlanmış csv dosyaları temel alınarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="1e847-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="1e847-260">Virgül içeren bir alan değeri varsa, sonuçlarla karışabilir.</span><span class="sxs-lookup"><span data-stu-id="1e847-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="1e847-261">Virgülleri kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1e847-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="1e847-262">**İzleme** sekmesi, tüm adımlar ve işlenen veriler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1e847-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="1e847-263">Hata ayıklamak için belirli bir adımı seçin.</span><span class="sxs-lookup"><span data-stu-id="1e847-263">Select a specific step to debug it.</span></span>

    ![İzleme sekmesi](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="1e847-265">Şablon hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="1e847-265">Learn more about the template</span></span>

<span data-ttu-id="1e847-266">Şablonla ilgili açıklamaları [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) dosyasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e847-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>

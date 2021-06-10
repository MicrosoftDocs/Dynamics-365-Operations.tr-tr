---
title: Taraf ve genel adres defteri modeline yükseltme
description: Bu konuda, çift yazma verilerinin taraf ve genel adres defteri modeline nasıl yükseltileceği açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112685"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="3225b-103">Taraf ve genel adres defteri modeline yükseltme</span><span class="sxs-lookup"><span data-stu-id="3225b-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3225b-104">[Microsoft Azure Data Factory şablonu](https://aka.ms/dual-write-gab-adf), çift yazmadaki mevcut **Hesap**, **İlgili Kişi** ve **Satıcı** tablo verilerini taraf ve genel adres defteri modeline yükseltmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3225b-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="3225b-105">Şablon, Finance and Operations uygulamaları ve müşteri etkileşimi uygulamalarındaki veriler arasında mutabakat sağlar.</span><span class="sxs-lookup"><span data-stu-id="3225b-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="3225b-106">İşlemin sonunda, **Taraf** kayıtlarına ait **Taraf** ve **İlgili Kişi** alanları oluşturulur ve müşteri etkileşimi uygulamalarındaki **Hesap**, **İLgili Kişi** ve **Satıcı** kayıtlarıyla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="3225b-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="3225b-107">Finance and Operations uygulaması içinde yeni **Taraf** kayıtları oluşturmak için bir .csv dosyası (`FONewParty.csv`) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3225b-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="3225b-108">Bu konu, Data Factory şablonunu kullanma ve verilerinizi yükseltme yönergelerini sağlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="3225b-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="3225b-109">Herhangi bir özelleştirmeleriniz yoksa, şablonu olduğu gibi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3225b-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="3225b-110">**Hesap**, **İlgili Kişi** ve **Satıcı** için özelleştirmeleriniz varsa aşağıdaki yönergeleri kullanarak şablonu değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3225b-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="3225b-111">Şablon yalnızca **Taraf** verilerini yükseltmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3225b-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="3225b-112">Gelecek bir sürümde, posta ve elektronik adresler de dahil edilecektir.</span><span class="sxs-lookup"><span data-stu-id="3225b-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3225b-113">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="3225b-113">Prerequisites</span></span>

<span data-ttu-id="3225b-114">Parti ve genel adres defteri modeline yükseltmek için aşağıdaki önkoşullar gereklidir:</span><span class="sxs-lookup"><span data-stu-id="3225b-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="3225b-115">Azure aboneliği</span><span class="sxs-lookup"><span data-stu-id="3225b-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="3225b-116">Şablona erişim</span><span class="sxs-lookup"><span data-stu-id="3225b-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="3225b-117">Mevcut bir çift yazma müşterisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3225b-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="3225b-118">Yükseltmek için hazırlık</span><span class="sxs-lookup"><span data-stu-id="3225b-118">Prepare for the upgrade</span></span>
<span data-ttu-id="3225b-119">Yükseltmeye hazırlanmak için aşağıdaki etkinlikler gereklidir:</span><span class="sxs-lookup"><span data-stu-id="3225b-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="3225b-120">**Tamamen eşitlenmiş**: Her iki ortam **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** için tamamen eşitlenmiş durumda.</span><span class="sxs-lookup"><span data-stu-id="3225b-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="3225b-121">**Tümleştirme anahtarları**: Müşteri etkileşimi uygulamalarındaki **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** tabloları kullanıma hazır gönderilen tümleştirme anahtarlarını kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="3225b-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="3225b-122">Tümleştirme anahtarlarını özelleştirdiyseniz, şablonu özelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3225b-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="3225b-123">**Taraf numarası**: Yükseltilecek tüm **Hesap (Müşteri)**, **İlgili Kişi** ve **Satıcı** kayıtlarında bir **Taraf** numarası bulunur.</span><span class="sxs-lookup"><span data-stu-id="3225b-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="3225b-124">**Taraf** numarası olmayan kayıtlar yok sayılır.</span><span class="sxs-lookup"><span data-stu-id="3225b-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="3225b-125">Bu kayıtları yükseltmek istiyorsanız, yükseltme işlemine başlamadan önce onlara bir **Taraf** numarası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3225b-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="3225b-126">**Sistem kesintisi**: Yükseltme işlemi sırasında, hem Finance and Operations hem de Customer Engagement uygulamalarını çevrimdışına almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3225b-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="3225b-127">**Anlık görüntü**: Hem Finance and Operations hem de Customer Engagement uygulamalarının anlık görüntüsünü alın.</span><span class="sxs-lookup"><span data-stu-id="3225b-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="3225b-128">Gerekirse önceki durumu geri yüklemek için anlık görüntüleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="3225b-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="3225b-129">Dağıtım</span><span class="sxs-lookup"><span data-stu-id="3225b-129">Deployment</span></span>

1. <span data-ttu-id="3225b-130">[Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) konumundan şablonu indirin.</span><span class="sxs-lookup"><span data-stu-id="3225b-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="3225b-131">[Microsoft Azure](https://portal.azure.com/)'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="3225b-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="3225b-132">[Kaynak grubu](/azure/azure-resource-manager/management/manage-resource-groups-portal) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3225b-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="3225b-133">Oluşturduğunuz kaynak grubunda bir [depolama hesabı](/azure/storage/common/storage-account-create?tabs=azure-portal) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3225b-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="3225b-134">Yukarıda oluşturduğunuz kaynak grubunda bir [veri fabrikası](/azure/data-factory/quickstart-create-data-factory-portal) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3225b-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="3225b-135">Veri fabrikasını açın ve **Yaz ve İzle** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3225b-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="3225b-136">**Yönet** sekmesinde **ARM şablonu** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3225b-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="3225b-137">**Taraf** şablonunu içe aktarmak için **ARM şablonunu içer aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3225b-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="3225b-138">Şablonu veri fabrikasına aktarın.</span><span class="sxs-lookup"><span data-stu-id="3225b-138">Import the template into the data factory.</span></span> <span data-ttu-id="3225b-139">**Proje ayrıntıları** ve **Kurulum ayrıntıları** için aşağıdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="3225b-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="3225b-140">Alan</span><span class="sxs-lookup"><span data-stu-id="3225b-140">Field</span></span> | <span data-ttu-id="3225b-141">Değer</span><span class="sxs-lookup"><span data-stu-id="3225b-141">Value</span></span>
    ---|---
    <span data-ttu-id="3225b-142">Abonelik</span><span class="sxs-lookup"><span data-stu-id="3225b-142">Subscription</span></span> | <span data-ttu-id="3225b-143">Azure aboneliği</span><span class="sxs-lookup"><span data-stu-id="3225b-143">Azure subscription</span></span>
    <span data-ttu-id="3225b-144">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="3225b-144">Resource group</span></span> | <span data-ttu-id="3225b-145">Altında depolama hesabı oluşturulan kaynağı sağlayın.</span><span class="sxs-lookup"><span data-stu-id="3225b-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="3225b-146">Bölge</span><span class="sxs-lookup"><span data-stu-id="3225b-146">Region</span></span> | <span data-ttu-id="3225b-147">Bölge belirtin.</span><span class="sxs-lookup"><span data-stu-id="3225b-147">Specify region.</span></span>
    <span data-ttu-id="3225b-148">Fabrika Adı</span><span class="sxs-lookup"><span data-stu-id="3225b-148">Factory Name</span></span> | <span data-ttu-id="3225b-149">Fabrika adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3225b-149">Specify factory name.</span></span>
    <span data-ttu-id="3225b-150">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="3225b-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="3225b-151">Uygulamanın anahtarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3225b-151">Specify the application's key.</span></span>
    <span data-ttu-id="3225b-152">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="3225b-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="3225b-153">Azure Blob depolama bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="3225b-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="3225b-154">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="3225b-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="3225b-155">Kullanıcı adı olarak belirttiğiniz kullanıcı hesabının parolası.</span><span class="sxs-lookup"><span data-stu-id="3225b-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="3225b-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="3225b-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="3225b-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="3225b-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="3225b-158">Uygulamanızın altında bulunduğu kiracı bilgilerini (etki alanı adı veya kiracı kimliği) belirtin.</span><span class="sxs-lookup"><span data-stu-id="3225b-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="3225b-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="3225b-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="3225b-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="3225b-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="3225b-161">Uygulamanın istemci kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3225b-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="3225b-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="3225b-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="3225b-163">Dynamics 365'e bağlanmak için kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="3225b-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="3225b-164">Daha fazla bilgi için aşağıdaki konulardan birine başvurun:</span><span class="sxs-lookup"><span data-stu-id="3225b-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="3225b-165">Her ortam için kaynak yöneticisi şablonunu el ile yükseltme</span><span class="sxs-lookup"><span data-stu-id="3225b-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="3225b-166">Bağlı hizmet özellikleri</span><span class="sxs-lookup"><span data-stu-id="3225b-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="3225b-167">Azure Data Factory kullanarak veri kopyalama</span><span class="sxs-lookup"><span data-stu-id="3225b-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="3225b-168">Dağıtımdan sonra, veri fabrikasının bağlantılı hizmetini, veri kümelerini ve veri akışını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3225b-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Veri kümeleri, veri akışı ve bağlantılı hizmet](media/data-factory-validate.png)

11. <span data-ttu-id="3225b-170">**Yönet**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3225b-170">Navigate to **Manage**.</span></span> <span data-ttu-id="3225b-171">**Bağlantılar** altından, **Bağlantılı Hizmet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3225b-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="3225b-172">**DynamicsCrmLinkedService** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3225b-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="3225b-173">**Bağlantılı hizmeti düzenle ( Dynamics CRM)** formuna aşağıdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="3225b-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="3225b-174">Alan</span><span class="sxs-lookup"><span data-stu-id="3225b-174">Field</span></span> | <span data-ttu-id="3225b-175">Değer</span><span class="sxs-lookup"><span data-stu-id="3225b-175">Value</span></span>
    ---|---
    <span data-ttu-id="3225b-176">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="3225b-176">Name</span></span> | <span data-ttu-id="3225b-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="3225b-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="3225b-178">Tanım</span><span class="sxs-lookup"><span data-stu-id="3225b-178">Description</span></span> | <span data-ttu-id="3225b-179">Varlık verilerini getirmek üzere CRM kurulumuyla bağlantı kurulacak bağlantılı hizmetler</span><span class="sxs-lookup"><span data-stu-id="3225b-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="3225b-180">Tümleştirme çalışma zamanı aracılığıyla bağlan</span><span class="sxs-lookup"><span data-stu-id="3225b-180">Connect via integration runtime</span></span> | <span data-ttu-id="3225b-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3225b-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="3225b-182">Dağıtım türü</span><span class="sxs-lookup"><span data-stu-id="3225b-182">Deployment type</span></span> | <span data-ttu-id="3225b-183">Çevrimiçi</span><span class="sxs-lookup"><span data-stu-id="3225b-183">Online</span></span>
    <span data-ttu-id="3225b-184">Hizmet URI'si</span><span class="sxs-lookup"><span data-stu-id="3225b-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="3225b-185">Kimlik doğrulaması türü</span><span class="sxs-lookup"><span data-stu-id="3225b-185">Authentication type</span></span> | <span data-ttu-id="3225b-186">Office365</span><span class="sxs-lookup"><span data-stu-id="3225b-186">Office365</span></span>
    <span data-ttu-id="3225b-187">Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="3225b-187">User name</span></span> |
    <span data-ttu-id="3225b-188">Parola veya Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="3225b-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="3225b-189">Parola</span><span class="sxs-lookup"><span data-stu-id="3225b-189">Password</span></span>
    <span data-ttu-id="3225b-190">Parola</span><span class="sxs-lookup"><span data-stu-id="3225b-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="3225b-191">Şablonu çalıştır</span><span class="sxs-lookup"><span data-stu-id="3225b-191">Run the template</span></span>

1. <span data-ttu-id="3225b-192">Finance and Operations uygulamasını kullanarak aşağıdaki **Hesap**, **İlgili Kişi** ve **Satıcı** çift yazma eşlemelerini durdurun.</span><span class="sxs-lookup"><span data-stu-id="3225b-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="3225b-193">Müşteriler V3 (hesaplar)</span><span class="sxs-lookup"><span data-stu-id="3225b-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="3225b-194">Müşteriler V3(ilgili kişiler)</span><span class="sxs-lookup"><span data-stu-id="3225b-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="3225b-195">CDS İlgili Kişileri V2(ilgili kişiler)</span><span class="sxs-lookup"><span data-stu-id="3225b-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="3225b-196">CDS İlgili Kişileri V2(ilgili kişiler)</span><span class="sxs-lookup"><span data-stu-id="3225b-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="3225b-197">Satıcı V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="3225b-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="3225b-198">Dataverse'de haritaların `msdy_dualwriteruntimeconfig` tablosundan kaldırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="3225b-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="3225b-199">AppSource'tan [Çift Yazma Taraf ve Genel Adres Defteri Çözümleri](https://aka.ms/dual-write-gab)'ni yükleyin.</span><span class="sxs-lookup"><span data-stu-id="3225b-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="3225b-200">Finance and Operations uygulamasında, aşağıdaki tablolar veri içeriyorsa bu tablolar için **Başlangıç Eşitlemesi**'ni çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3225b-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="3225b-201">Selamlamalar</span><span class="sxs-lookup"><span data-stu-id="3225b-201">Salutations</span></span>
    + <span data-ttu-id="3225b-202">Kişisel karakter türleri</span><span class="sxs-lookup"><span data-stu-id="3225b-202">Personal character types</span></span>
    + <span data-ttu-id="3225b-203">Kapanış sözleri</span><span class="sxs-lookup"><span data-stu-id="3225b-203">Complimentary closing</span></span>
    + <span data-ttu-id="3225b-204">İlgili kişi unvanları</span><span class="sxs-lookup"><span data-stu-id="3225b-204">Contact person titles</span></span>
    + <span data-ttu-id="3225b-205">Karar verici roller</span><span class="sxs-lookup"><span data-stu-id="3225b-205">Decision making roles</span></span>
    + <span data-ttu-id="3225b-206">Bağlılık programı düzeyleri</span><span class="sxs-lookup"><span data-stu-id="3225b-206">Loyalty levels</span></span>

5. <span data-ttu-id="3225b-207">Müşteri etkileşimi uygulamasında aşağıdaki eklenti adımlarını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="3225b-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="3225b-208">Hesap Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-208">Account Update</span></span>
         + <span data-ttu-id="3225b-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Hesap güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="3225b-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Hesap güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="3225b-211">İlgili Kişi Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-211">Contact Update</span></span>
         + <span data-ttu-id="3225b-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: İlgili kişi güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="3225b-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: İlgili kişi güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="3225b-214">msdyn_party Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-214">msdyn_party Update</span></span>
         + <span data-ttu-id="3225b-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="3225b-216">msdyn_vendor Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="3225b-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="3225b-218">Müşteri etkileşimi uygulamasında aşağıdaki iş akışlarını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="3225b-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="3225b-219">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3225b-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3225b-220">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3225b-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3225b-221">İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3225b-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="3225b-222">Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3225b-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="3225b-223">Hesaplar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3225b-224">Satıcılar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="3225b-225">İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="3225b-226">Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="3225b-227">Veri fabrikasında, aşağıdaki görüntüde gösterildiği şekilde **Şimdi tetikle**'yi seçerek şablonu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3225b-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="3225b-228">Bu işlemin tamamlanması veri hacmine göre birkaç saat sürebilir.</span><span class="sxs-lookup"><span data-stu-id="3225b-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Tetik çalıştırması](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="3225b-230">**Hesap**, **İlgili Kişi** ve **Satıcı** için özelleştirmeleriniz varsa şablonu değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3225b-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="3225b-231">Finance and Operations uygulamasında yeni **Taraf** kayıtlarını içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="3225b-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="3225b-232">Azure blob depolamadan `FONewParty.csv` dosyasını indirin.</span><span class="sxs-lookup"><span data-stu-id="3225b-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="3225b-233">Yol: `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="3225b-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="3225b-234">`FONewParty.csv` dosyasını bir Excel dosyasına dönüştürüp Excel dosyasını Finance and Operations uygulamasına aktarın.</span><span class="sxs-lookup"><span data-stu-id="3225b-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="3225b-235">csv içe aktarma işlemi sizin için uygunsa, csv dosyasını doğrudan içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3225b-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="3225b-236">Veri hacmine bağlı olarak içe aktarma birkaç saat sürebilir.</span><span class="sxs-lookup"><span data-stu-id="3225b-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="3225b-237">Daha fazla bilgi için bkz. [Verileri içeri ve dışarı aktarma işlerine genel bakış](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="3225b-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Dataverse taraf kayıtlarını içe aktarma](media/data-factory-import-party.png)

9. <span data-ttu-id="3225b-239">Müşteri etkileşimi uygulamalarında aşağıdaki eklenti adımlarını devre dışı etkinleştirin:</span><span class="sxs-lookup"><span data-stu-id="3225b-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="3225b-240">Hesap Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-240">Account Update</span></span>
         + <span data-ttu-id="3225b-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Hesap güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="3225b-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Hesap güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="3225b-243">İlgili Kişi Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-243">Contact Update</span></span>
         + <span data-ttu-id="3225b-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: İlgili kişi güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="3225b-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: İlgili kişi güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="3225b-246">msdyn_party Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-246">msdyn_party Update</span></span>
         + <span data-ttu-id="3225b-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="3225b-248">msdyn_vendor Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="3225b-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3225b-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="3225b-250">Müşteri etkileşimi uygulamalarında, önceki adımlarda devre dışı bıraktıysanız aşağıdaki iş akışlarını etkinleştirin:</span><span class="sxs-lookup"><span data-stu-id="3225b-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="3225b-251">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3225b-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3225b-252">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3225b-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3225b-253">İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3225b-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="3225b-254">Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3225b-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="3225b-255">Hesaplar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="3225b-256">Satıcılar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="3225b-257">İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="3225b-258">Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3225b-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="3225b-259">**Taraf** ile ilgili haritaları [Taraf ve genel adres defteri](party-gab.md)'nde belirtildiği şekilde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3225b-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="3225b-260">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="3225b-260">Troubleshooting</span></span>

1. <span data-ttu-id="3225b-261">İşlem başarısız olursa, başarısız olan etkinlikten başlayarak veri fabrikasını yeniden çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3225b-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="3225b-262">Bazı dosyalar veri doğrulama amacıyla kullanabileceğiniz veri fabrikası tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3225b-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="3225b-263">Veri fabrikası, virgülle sınırlanmış csv dosyaları temel alınarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="3225b-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="3225b-264">Virgül içeren bir alan değeri varsa, sonuçlarla karışabilir.</span><span class="sxs-lookup"><span data-stu-id="3225b-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="3225b-265">Virgülleri kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3225b-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="3225b-266">**İzleme** sekmesi, tüm adımlar ve işlenen veriler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3225b-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="3225b-267">Hata ayıklamak için belirli bir adımı seçin.</span><span class="sxs-lookup"><span data-stu-id="3225b-267">Select a specific step to debug it.</span></span>

    ![İzleme sekmesi](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="3225b-269">Şablon hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="3225b-269">Learn more about the template</span></span>

<span data-ttu-id="3225b-270">Şablon hakkında ek bilgileri [Azure Data Factory için Yorumlar şablonu benioku](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)'da bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3225b-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>

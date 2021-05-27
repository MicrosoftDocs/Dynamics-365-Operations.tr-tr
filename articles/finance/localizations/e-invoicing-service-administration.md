---
title: Elektronik faturalama yönetim bileşenleri
description: Bu konu, elektronik faturalama yönetimiyle ilgili bileşenler hakkında bilgi sağlar.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980936"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="bc4ab-103">Elektronik faturalama yönetim bileşenleri</span><span class="sxs-lookup"><span data-stu-id="bc4ab-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bc4ab-104">Bu konu, elektronik faturalama yönetimiyle ilgili bileşenler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="bc4ab-105">Elektronik faturalama hizmetinin nasıl yapılandırılacağı hakkında bilgiler de sağlar.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="bc4ab-106">Azure</span><span class="sxs-lookup"><span data-stu-id="bc4ab-106">Azure</span></span>

<span data-ttu-id="bc4ab-107">Key Vault ve depolama hesabının gizli dizilerini oluşturmak için Microsoft Azure kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="bc4ab-108">Sonra, Elektronik faturalamanın yapılandırmasında gizli dizileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="bc4ab-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="bc4ab-109">Lifecycle Services</span></span>

<span data-ttu-id="bc4ab-110">LCS dağıtım projenizde mikro hizmetleri etkinleştirmek amacıyla Microsoft Dynamics Lifecycle Services'i (LCS) kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="bc4ab-111">LCS içindeki mikro hizmetin yüklenmesi için en az bir katman 2 sanal makine gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="bc4ab-112">Ortam planlama hakkında daha fazla bilgi için [ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="bc4ab-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="bc4ab-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="bc4ab-114">Dynamics 365 Regulatory Configuration Services (RCS), elektronik faturalamayı yapılandırmak için kullanılan arabirimdir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="bc4ab-115">Ortamlar ve elektronik faturalama özellikleri gibi kaynaklar RCS'de oluşturulur, sürdürülür ve barındırılır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="bc4ab-116">Kaynaklar hazır olduğunda, elektronik faturalama hizmetine yayınlanırlar.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="bc4ab-117">RCS kaydı için, bkz. [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="bc4ab-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="bc4ab-118">RCS hakkında daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="bc4ab-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="bc4ab-119">Elektronik faturalama ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="bc4ab-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="bc4ab-120">Elektronik faturaları konfigüre etmek için RCS'yi kullanabilmeniz için önce, RCS'yi Elektronik faturalama ile iletişime izin verecek şekilde konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="bc4ab-121">Bu konfigürasyon **Elektronik raporlama parametreleri** sayfasındaki **Elektronik faturalama** sekmesinde tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="bc4ab-122">Hizmet bitiş noktası</span><span class="sxs-lookup"><span data-stu-id="bc4ab-122">Service endpoint</span></span>

<span data-ttu-id="bc4ab-123">Elektronik faturalama çeşitli Azure veri merkezi coğrafyalarında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="bc4ab-124">Aşağıdaki tabloda her bölge için kullanılabilirlik listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="bc4ab-125">Azure veri merkezi coğrafyası</span><span class="sxs-lookup"><span data-stu-id="bc4ab-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="bc4ab-126">Amerika Birleşik Devletleri</span><span class="sxs-lookup"><span data-stu-id="bc4ab-126">United States</span></span>              |
| <span data-ttu-id="bc4ab-127">Avrupa</span><span class="sxs-lookup"><span data-stu-id="bc4ab-127">Europe</span></span>                     |
| <span data-ttu-id="bc4ab-128">Birleşik Krallık</span><span class="sxs-lookup"><span data-stu-id="bc4ab-128">United Kingdom</span></span>             |
| <span data-ttu-id="bc4ab-129">Asya</span><span class="sxs-lookup"><span data-stu-id="bc4ab-129">Asia</span></span>                       |

### <a name="service-environments"></a><span data-ttu-id="bc4ab-130">Hizmet ortamları</span><span class="sxs-lookup"><span data-stu-id="bc4ab-130">Service environments</span></span>

<span data-ttu-id="bc4ab-131">Hizmet ortamları, Elektronik faturalamanın elektronik faturalama özelliklerinin yürütülmesini desteklemek için oluşturulan mantıksal bölümlerdir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="bc4ab-132">Güvenlik gizli dizileri ve dijital sertifikalar ve idare (erişim izinleri), hizmet ortamı düzeyinde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="bc4ab-133">Müşteriler istedikleri sayıda servis ortamı oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="bc4ab-134">Bir müşterinin oluşturduğu tüm servis ortamları birbirinden bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="bc4ab-135">Hizmet ortamları, RCS'de oluşturulup tutulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="bc4ab-136">Hizmet ortamları hazır olduğunda, elektronik faturalama hizmetine yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="bc4ab-137">Hizmet ortamı durumu</span><span class="sxs-lookup"><span data-stu-id="bc4ab-137">Service environment status</span></span>

<span data-ttu-id="bc4ab-138">Hizmet ortamları, durum ile yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-138">Service environments can be managed through status.</span></span> <span data-ttu-id="bc4ab-139">Olası seçenekler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bc4ab-139">The possible options are:</span></span>

- <span data-ttu-id="bc4ab-140">**Yayınlanmadı** – Ortam oluşturuldu, ancak henüz yayınlanmadı.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="bc4ab-141">**Yayınlandı** – Ortam elektronik faturalama içinde yayınlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="bc4ab-142">**Değiştirildi** – Yayınlanmış bir ortamın öznitelikleri değiştirildi, ancak değişiklikler henüz yayınlanmadı.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="bc4ab-143">Müşteri gizli dizileri</span><span class="sxs-lookup"><span data-stu-id="bc4ab-143">Customer secrets</span></span>

<span data-ttu-id="bc4ab-144">Elektronik faturalama servisi, tüm iş verilerinizi şirketinize ait Azure kaynaklarında depolamaktan sorumlu olur.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="bc4ab-145">Hizmetin doğru çalışmasını ve elektronik faturalama eklentisi için gereken ve bu eklenti tarafından oluşturulan tüm iş verilerine düzgün biçimde erişildiğinden emin olmak için iki ana Azure kaynağı oluşturmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="bc4ab-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="bc4ab-146">Elektronik faturaları depolayacak bir Azure depolama hesabı (Blob depolama)</span><span class="sxs-lookup"><span data-stu-id="bc4ab-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="bc4ab-147">Sertifikaları ve depolama hesabının Tekdüzen Kaynak Tanımlayıcısı'nı (URI) depolamak için bir Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="bc4ab-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="bc4ab-148">Özel bir Key Vault kaynağı ve müşteri depolama hesabıyla özel olarak Elektronik Faturalama ile kullanılmak üzere ayrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="bc4ab-149">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir Key Vault oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="bc4ab-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="bc4ab-150">Key Vault'un sağlığını izlemek ve uyarı almak üzere, Key Vault için Azure İzleyici'yi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="bc4ab-151">Key Vault günlüğünü etkinleştirerek, Key Vault'larınıza nasıl, ne zaman ve kim tarafından erişildiğini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="bc4ab-152">Daha fazla bilgi için bkz. [Azure Key Vault için izleme ve uyarı](/azure/key-vault/general/alert) ve [Key Vault günlüğünü etkinleştirme](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="bc4ab-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="bc4ab-153">Bir en iyi uygulama olarak, gizli anahtarları düzenli olarak döndürün.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="bc4ab-154">Daha fazla bilgi için bkz. [Gizli anahtar belgeleri](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="bc4ab-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="bc4ab-155">Kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="bc4ab-155">Users</span></span>

<span data-ttu-id="bc4ab-156">Her bir hizmet ortamı, elektronik faturalamalarda Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'tan bağlanabilecek kullanıcıları listelemelidir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="bc4ab-157">Yayınlama</span><span class="sxs-lookup"><span data-stu-id="bc4ab-157">Publication</span></span>

<span data-ttu-id="bc4ab-158">Hizmet ortamlarının kullanılması için elektronik faturalama hizmetine yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="bc4ab-159">Finance ve Supply Chain Management tarafından yalnızca yayınlanan ortamlara erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="bc4ab-160">Ek olarak, hizmet ortamının özniteliklerinde yapılacak güncelleştirmeler elektronik faturalama servisi üzerinde geçerli olmadan önce hizmet ortamı yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="bc4ab-161">Bağlı uygulamalar</span><span class="sxs-lookup"><span data-stu-id="bc4ab-161">Connected applications</span></span>

<span data-ttu-id="bc4ab-162">Bağlı uygulamalar, RCS üzerinden erişmek isteyebileceğiniz Finance ve Supply Chain Management kurulumlarıdır.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="bc4ab-163">Uygulama URL'si ve kiracısının yanı sıra bağlı bir uygulama, RCS'nin ortama bağlanmasına olanak veren kimlik bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="bc4ab-164">Bağlı uygulamalar sayesinde, Finance ve Supply Chain Management'ta elektronik faturalama özelliğinin bir kısmını, tüm elektronik faturalama özelliğini çalışır hale getirmek için konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="bc4ab-165">Finance ve Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="bc4ab-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="bc4ab-166">Elektronik faturalama ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="bc4ab-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="bc4ab-167">Elektronik faturalama üzerinden elektronik faturalar kesmek amacıyla Finance ve Supply Chain Management'ı kullanabilmeniz için hizmetle iletişim kurulmasına izin verecek şekilde konfigüre edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="bc4ab-168">Elektronik faturalama tümleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="bc4ab-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="bc4ab-169">Finance ve Supply Chain Management ile Elektronik faturalama arasındaki iletişimi etkinleştirmek için **Özellik yönetimi** çalışma alanındaki **Elektronik faturalama tümleştirme** özelliğini açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="bc4ab-170">Hizmet bitiş noktası</span><span class="sxs-lookup"><span data-stu-id="bc4ab-170">Service endpoint</span></span>

<span data-ttu-id="bc4ab-171">Servis uç noktası, elektronik faturalamanın bulunduğu URL'dir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="bc4ab-172">Elektronik fatura kesebilmek için Finance ve Supply Chain Management'ta servis uç noktalarının yapılandırılarak hizmetle iletişim kurulmasına izin vermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="bc4ab-173">Hizmet uç noktasını konfigüre etmek için **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametresi**'ne gidin ve **Gönderme hizmetleri** sekmesinde, **Elektronik faturalama URL'si** alanına, **Servis uç noktası** bölümünde açıklanan şekilde tabloya URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="bc4ab-174">Ortamlar</span><span class="sxs-lookup"><span data-stu-id="bc4ab-174">Environments</span></span>

<span data-ttu-id="bc4ab-175">Finance ve Supply Chain Management'a girilen ortam adı, RCS'de oluşturulan ve Elektronik faturalamaya yayınlanan ortam adına başvurur.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="bc4ab-176">Ortam, elektronik fatura kesmeye yönelik her isteğin, Elektronik faturalamanın hangi elektronik faturalama özelliğinin talebi işlemesi gerektiğini belirleyebildiği bir ortam içermesi için **Elektronik belge parametresi** sayfasının **Gönderim servisleri** sekmesinde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="bc4ab-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc4ab-177">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bc4ab-177">Additional resources</span></span>

- [<span data-ttu-id="bc4ab-178">RCS'de elektronik faturaları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bc4ab-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="bc4ab-179">Finance ve Supply Chain Management'ta elektronik fatura kesme</span><span class="sxs-lookup"><span data-stu-id="bc4ab-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

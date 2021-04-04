---
title: Elektronik faturalama eklentisini yönetim bileşenleri
description: Bu konu, elektronik faturalama eklentisinin yönetimiyle ilgili bileşenler hakkında bilgi sağlar.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592586"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="78e17-103">Elektronik faturalama eklentisini yönetim bileşenleri</span><span class="sxs-lookup"><span data-stu-id="78e17-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="78e17-104">Bu konu, elektronik faturalama eklentisinin yönetimiyle ilgili bileşenler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="78e17-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="78e17-105">Elektronik faturalama eklentisi hizmetinin nasıl yapılandırılacağı hakkında bilgiler de sağlar.</span><span class="sxs-lookup"><span data-stu-id="78e17-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="78e17-106">Azure</span><span class="sxs-lookup"><span data-stu-id="78e17-106">Azure</span></span>

<span data-ttu-id="78e17-107">Anahtar kasası ve depolama hesabının gizli dizilerini oluşturmak için Microsoft Azure kullanın.</span><span class="sxs-lookup"><span data-stu-id="78e17-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="78e17-108">Sonra, Elektronik faturalama eklentisinin yapılandırmasında gizli dizileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="78e17-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="78e17-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="78e17-109">Lifecycle Services</span></span>

<span data-ttu-id="78e17-110">LCS dağıtım projenizde mikro hizmetler için eklentiyi etkinleştirmek amacıyla Microsoft Dynamics Lifecycle Services'i (LCS) kullanın.</span><span class="sxs-lookup"><span data-stu-id="78e17-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="78e17-111">LCS içindeki mikro hizmet eklentisinin yüklenmesi için en az bir katman 2 sanal makine gereklidir.</span><span class="sxs-lookup"><span data-stu-id="78e17-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="78e17-112">Ortam planlama hakkında daha fazla bilgi için [ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="78e17-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="78e17-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="78e17-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="78e17-114">Dynamics 365 Regulatory Configuration Services (RCS), elektronik faturalama eklentisini konfigüre etmek için kullanılan arabirimdir.</span><span class="sxs-lookup"><span data-stu-id="78e17-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="78e17-115">Ortamlar ve elektronik faturalama özellikleri gibi kaynaklar RCS'de oluşturulur, sürdürülür ve barındırılır.</span><span class="sxs-lookup"><span data-stu-id="78e17-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="78e17-116">Kaynaklar hazır olduğunda, elektronik faturalama eklentisi hizmetine yayınlanırlar.</span><span class="sxs-lookup"><span data-stu-id="78e17-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="78e17-117">RCS kaydı için, bkz. [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="78e17-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="78e17-118">RCS hakkında daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="78e17-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="78e17-119">Elektronik faturalama eklentisi ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="78e17-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="78e17-120">Elektronik faturaları konfigüre etmek için RCS'yi kullanabilmeniz için önce, RCS'yi Elektronik faturalama eklentisi ile iletişime izin verecek şekilde konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="78e17-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="78e17-121">Bu konfigürasyon **Elektronik raporlama parametreleri** sayfasındaki **Elektronik faturalama eklentisi** sekmesinde tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="78e17-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="78e17-122">Hizmet bitiş noktası</span><span class="sxs-lookup"><span data-stu-id="78e17-122">Service endpoint</span></span>

<span data-ttu-id="78e17-123">Elektronik faturalama eklentisi çeşitli Azure veri merkezi coğrafyalarında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="78e17-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="78e17-124">Aşağıdaki tabloda her bölge için kullanılabilirlik listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="78e17-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="78e17-125">Azure veri merkezi coğrafyası</span><span class="sxs-lookup"><span data-stu-id="78e17-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="78e17-126">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="78e17-126">East US</span></span>                    |
| <span data-ttu-id="78e17-127">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="78e17-127">West US</span></span>                    |
| <span data-ttu-id="78e17-128">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="78e17-128">North EU</span></span>                   |
| <span data-ttu-id="78e17-129">Batı AB</span><span class="sxs-lookup"><span data-stu-id="78e17-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="78e17-130">Hizmet ortamları</span><span class="sxs-lookup"><span data-stu-id="78e17-130">Service environments</span></span>

<span data-ttu-id="78e17-131">Hizmet ortamları, Elektronik faturalama eklentisinin elektronik faturalama özelliklerinin yürütülmesini desteklemek için oluşturulan mantıksal bölümlerdir.</span><span class="sxs-lookup"><span data-stu-id="78e17-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="78e17-132">Güvenlik gizli dizileri ve dijital sertifikalar ve idare (erişim izinleri), hizmet ortamı düzeyinde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="78e17-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="78e17-133">Müşteriler istedikleri sayıda servis ortamı oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="78e17-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="78e17-134">Bir müşterinin oluşturduğu tüm servis ortamları birbirinden bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="78e17-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="78e17-135">Hizmet ortamları, RCS'de oluşturulup tutulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="78e17-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="78e17-136">Hizmet ortamları hazır olduğunda, elektronik faturalama eklentisi hizmetine yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="78e17-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="78e17-137">Hizmet ortamı durumu</span><span class="sxs-lookup"><span data-stu-id="78e17-137">Service environment status</span></span>

<span data-ttu-id="78e17-138">Hizmet ortamları, durum ile yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="78e17-138">Service environments can be managed through status.</span></span> <span data-ttu-id="78e17-139">Olası seçenekler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="78e17-139">The possible options are:</span></span>

- <span data-ttu-id="78e17-140">**Yayınlanmadı** – Ortam oluşturuldu, ancak henüz yayınlanmadı.</span><span class="sxs-lookup"><span data-stu-id="78e17-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="78e17-141">**Yayınlandı** – Ortam elektronik faturalama eklentisi içinde yayınlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="78e17-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="78e17-142">**Değiştirildi** – Yayınlanmış bir ortamın öznitelikleri değiştirildi, ancak değişiklikler henüz yayınlanmadı.</span><span class="sxs-lookup"><span data-stu-id="78e17-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="78e17-143">Müşteri gizli dizileri</span><span class="sxs-lookup"><span data-stu-id="78e17-143">Customer secrets</span></span>

<span data-ttu-id="78e17-144">Elektronik faturalama eklentisi servisi, tüm iş verilerinizi şirketinize ait Azure kaynaklarında depolamaktan sorumlu olur.</span><span class="sxs-lookup"><span data-stu-id="78e17-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="78e17-145">Hizmetin doğru çalışmasını ve elektronik faturalama eklentisi için gerekli olan ve bu eklenti tarafından oluşturulan ve yalnızca eklenti tarafından oluşturulmuş tüm iş verilerine erişmesini sağlamak için iki ana Azure kaynağı oluşturmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="78e17-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="78e17-146">Elektronik faturaları depolayacak bir Azure depolama hesabı (Blob depolama)</span><span class="sxs-lookup"><span data-stu-id="78e17-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="78e17-147">Sertifikaları ve depolama hesabının Tekdüzen Kaynak Tanımlayıcısı'nı (URI) depolamak için bir Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="78e17-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="78e17-148">Özel bir Anahtar Kasası kaynağı ve müşteri depolama hesabıyla özel olarak Elektronik faturalama eklentisi ile kullanılmak üzere ayrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="78e17-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="78e17-149">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="78e17-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="78e17-150">Kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="78e17-150">Users</span></span>

<span data-ttu-id="78e17-151">Her bir hizmet ortamı, elektronik faturalama eklentilerinde Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'tan bağlanabilecek kullanıcıları listelemelidir.</span><span class="sxs-lookup"><span data-stu-id="78e17-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="78e17-152">Yayınlama</span><span class="sxs-lookup"><span data-stu-id="78e17-152">Publication</span></span>

<span data-ttu-id="78e17-153">Hizmet ortamlarının kullanılması için elektronik faturalama eklentisi hizmetine yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="78e17-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="78e17-154">Finance ve Supply Chain Management tarafından yalnızca yayınlanan ortamlara erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="78e17-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="78e17-155">Ek olarak, hizmet ortamının özniteliklerinde yapılacak güncelleştirmeler elektronik faturalama servisi üzerinde geçerli olmadan önce hizmet ortamı yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="78e17-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="78e17-156">Bağlı uygulamalar</span><span class="sxs-lookup"><span data-stu-id="78e17-156">Connected applications</span></span>

<span data-ttu-id="78e17-157">Bağlı uygulamalar, RCS üzerinden erişmek isteyebileceğiniz Finance ve Supply Chain Management kurulumlarıdır.</span><span class="sxs-lookup"><span data-stu-id="78e17-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="78e17-158">Uygulama URL'si ve kiracısının yanı sıra bağlı bir uygulama, RCS'nin ortama bağlanmasına olanak veren kimlik bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="78e17-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="78e17-159">Bağlı uygulamalar sayesinde, Finance ve Supply Chain Management'ta elektronik faturalama özelliğinin bir kısmını, tüm elektronik faturalama özelliğini çalışır hale getirmek için konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="78e17-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="78e17-160">Finance ve Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="78e17-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="78e17-161">Elektronik faturalama eklentisi ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="78e17-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="78e17-162">Elektronik faturalama eklentisi üzerinden elektronik faturalar kesmek amacıyla Finance ve Supply Chain Management'ı kullanabilmeniz için eklentinin hizmetle iletişim kurulmasına izin verecek şekilde konfigüre edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="78e17-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="78e17-163">Elektronik faturalama eklentisi tümleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="78e17-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="78e17-164">Finance ve Supply Chain Management ile Elektronik faturalama eklentisi arasındaki iletişimi etkinleştirmek için **Özellik yönetimi** çalışma alanındaki **Elektronik faturalama eklentisi tümleştirme** özelliğini açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="78e17-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="78e17-165">Hizmet bitiş noktası</span><span class="sxs-lookup"><span data-stu-id="78e17-165">Service endpoint</span></span>

<span data-ttu-id="78e17-166">Servis uç noktası, elektronik faturalama eklentisinin bulunduğu URL'dir.</span><span class="sxs-lookup"><span data-stu-id="78e17-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="78e17-167">Elektronik fatura kesebilmek için Finance ve Supply Chain Management'ta servis uç noktalarının yapılandırılarak hizmetle iletişim kurulmasına izin vermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="78e17-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="78e17-168">Hizmet uç noktasını konfigüre etmek için **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametresi**'ne gidin ve **Gönderme hizmetleri** sekmesinde, **Elektronik faturalama eklentisi URL'si** alanına, **Servis uç noktası** bölümünde açıklanan şekilde tabloya URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="78e17-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="78e17-169">Ortamlar</span><span class="sxs-lookup"><span data-stu-id="78e17-169">Environments</span></span>

<span data-ttu-id="78e17-170">Finance ve Supply Chain Management'a girilen ortam adı, RCS'de oluşturulan ve Elektronik faturalama eklentisine yayınlanan ortam adına başvurur.</span><span class="sxs-lookup"><span data-stu-id="78e17-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="78e17-171">Ortam, elektronik fatura kesmeye yönelik her isteğin, Elektronik faturalama eklentisinin hangi elektronik faturalama özelliğinin talebi işlemesi gerektiğini belirleyebildiği bir ortam içermesi için **Elektronik belge parametresi** sayfasının **Gönderim servisleri** sekmesinde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="78e17-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="78e17-172">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="78e17-172">Additional resources</span></span>

- [<span data-ttu-id="78e17-173">RCS'de elektronik faturaları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="78e17-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="78e17-174">Finance ve Supply Chain Management'ta elektronik fatura kesme</span><span class="sxs-lookup"><span data-stu-id="78e17-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Elektronik faturalama eklentisini yönetim bileşenleri
description: Bu konu, elektronik faturalama eklentisinin yönetimiyle ilgili bileşenler hakkında bilgi sağlar.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104450"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="a0147-103">Elektronik faturalama eklentisini yönetim bileşenleri</span><span class="sxs-lookup"><span data-stu-id="a0147-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a0147-104">Bu konu, elektronik faturalama eklentisinin yönetimiyle ilgili bileşenler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a0147-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="a0147-105">Elektronik faturalama eklentisi hizmetinin nasıl yapılandırılacağı hakkında bilgiler de sağlar.</span><span class="sxs-lookup"><span data-stu-id="a0147-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="a0147-106">Azure</span><span class="sxs-lookup"><span data-stu-id="a0147-106">Azure</span></span>

<span data-ttu-id="a0147-107">Anahtar kasası ve depolama hesabının gizli dizilerini oluşturmak için Microsoft Azure kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0147-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="a0147-108">Sonra, Elektronik faturalama eklentisinin yapılandırmasında gizli dizileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0147-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="a0147-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a0147-109">Lifecycle Services</span></span>

<span data-ttu-id="a0147-110">LCS dağıtım projenizde mikro hizmetler için eklentiyi etkinleştirmek amacıyla Microsoft Dynamics Lifecycle Services'i (LCS) kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0147-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="a0147-111">LCS'de, **Önizleme özelliği yönetimi** kutucuğunu seçin ve sonra **E-faturalama hizmeti** özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a0147-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="a0147-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="a0147-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="a0147-113">Dynamics 365 Regulatory Configuration Services (RCS), elektronik faturalama eklentisini konfigüre etmek için kullanılan arabirimdir.</span><span class="sxs-lookup"><span data-stu-id="a0147-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="a0147-114">Ortamlar ve elektronik faturalama özellikleri gibi kaynaklar RCS'de oluşturulur, sürdürülür ve barındırılır.</span><span class="sxs-lookup"><span data-stu-id="a0147-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="a0147-115">Kaynaklar hazır olduğunda, elektronik faturalama eklentisi hizmetine yayınlanırlar.</span><span class="sxs-lookup"><span data-stu-id="a0147-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="a0147-116">RCS hakkında daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="a0147-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="a0147-117">Elektronik faturalama eklentisi ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="a0147-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="a0147-118">Elektronik faturaları konfigüre etmek için RCS'yi kullanabilmeniz için önce, RCS'yi Elektronik faturalama eklentisi ile iletişime izin verecek şekilde konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="a0147-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="a0147-119">Bu konfigürasyon **Elektronik raporlama parametreleri** sayfasındaki **Elektronik faturalama eklentisi** sekmesinde tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a0147-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="a0147-120">Hizmet bitiş noktası</span><span class="sxs-lookup"><span data-stu-id="a0147-120">Service endpoint</span></span>

<span data-ttu-id="a0147-121">Elektronik faturalama eklentisi uç noktasının URL'si, Azure veri merkezi coğrafyasına göre değişebilir.</span><span class="sxs-lookup"><span data-stu-id="a0147-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="a0147-122">Aşağıdaki tabloda her bölge için kullanılabilirlik listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="a0147-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="a0147-123">Azure veri merkezi coğrafyası</span><span class="sxs-lookup"><span data-stu-id="a0147-123">Azure datacenter geography</span></span> | <span data-ttu-id="a0147-124">Hizmet uç noktası URL'si</span><span class="sxs-lookup"><span data-stu-id="a0147-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="a0147-125">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="a0147-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="a0147-126">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="a0147-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="a0147-127">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="a0147-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="a0147-128">Batı AB</span><span class="sxs-lookup"><span data-stu-id="a0147-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="a0147-129">Başvuru kodu</span><span class="sxs-lookup"><span data-stu-id="a0147-129">Application ID</span></span>

<span data-ttu-id="a0147-130">Uygulama kimliği, Elektronik faturalama eklenti uygulamasının kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="a0147-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="a0147-131">Bu durumda değer sabittir: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="a0147-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="a0147-132">LCS ortam kimliği</span><span class="sxs-lookup"><span data-stu-id="a0147-132">LCS environment ID</span></span>

<span data-ttu-id="a0147-133">LCS ortamı kimliği, kuruluşunuzun LCS aboneliğinin kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="a0147-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="a0147-134">Hizmet ortamları</span><span class="sxs-lookup"><span data-stu-id="a0147-134">Service environments</span></span>

<span data-ttu-id="a0147-135">Hizmet ortamları, Elektronik faturalama eklentisinin elektronik faturalama özelliklerinin yürütülmesini desteklemek için oluşturulan mantıksal bölümlerdir.</span><span class="sxs-lookup"><span data-stu-id="a0147-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="a0147-136">Güvenlik gizli dizileri ve dijital sertifikalar ve idare (erişim izinleri), hizmet ortamı düzeyinde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a0147-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="a0147-137">Müşteriler istedikleri sayıda servis ortamı oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="a0147-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="a0147-138">Bir müşterinin oluşturduğu tüm servis ortamları birbirinden bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="a0147-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="a0147-139">Hizmet ortamları, RCS'de oluşturulup tutulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a0147-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="a0147-140">Hizmet ortamları hazır olduğunda, elektronik faturalama eklentisi hizmetine yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a0147-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="a0147-141">Hizmet ortamı durumu</span><span class="sxs-lookup"><span data-stu-id="a0147-141">Service environment status</span></span>

<span data-ttu-id="a0147-142">Hizmet ortamları, durum ile yönetilebilir.</span><span class="sxs-lookup"><span data-stu-id="a0147-142">Service environments can be managed through status.</span></span> <span data-ttu-id="a0147-143">Olası seçenekler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a0147-143">The possible options are:</span></span>

- <span data-ttu-id="a0147-144">**Yayınlanmadı** – Ortam oluşturuldu, ancak henüz yayınlanmadı.</span><span class="sxs-lookup"><span data-stu-id="a0147-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="a0147-145">**Yayınlandı** – Ortam elektronik faturalama eklentisi içinde yayınlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a0147-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="a0147-146">**Değiştirildi** – Yayınlanmış bir ortamın öznitelikleri değiştirildi, ancak değişiklikler henüz yayınlanmadı.</span><span class="sxs-lookup"><span data-stu-id="a0147-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="a0147-147">Müşteri gizli dizileri</span><span class="sxs-lookup"><span data-stu-id="a0147-147">Customer secrets</span></span>

<span data-ttu-id="a0147-148">Elektronik faturalama eklentisi servisi, tüm iş verilerinizi şirketinize ait Azure kaynaklarında depolamaktan sorumlu olur.</span><span class="sxs-lookup"><span data-stu-id="a0147-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="a0147-149">Hizmetin doğru çalışmasını ve elektronik faturalama eklentisi için gerekli olan ve bu eklenti tarafından oluşturulan ve yalnızca eklenti tarafından oluşturulmuş tüm iş verilerine erişmesini sağlamak için iki ana Azure kaynağı oluşturmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="a0147-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="a0147-150">Elektronik faturaları depolayacak bir Azure depolama hesabı (Blob depolama)</span><span class="sxs-lookup"><span data-stu-id="a0147-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="a0147-151">Sertifikaları ve depolama hesabının Tekdüzen Kaynak Tanımlayıcısı'nı (URI) depolamak için bir Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a0147-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="a0147-152">Özel bir Anahtar Kasası kaynağı ve müşteri depolama hesabıyla özel olarak Elektronik faturalama eklentisi ile kullanılmak üzere ayrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a0147-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="a0147-153">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="a0147-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="a0147-154">Kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="a0147-154">Users</span></span>

<span data-ttu-id="a0147-155">Her bir hizmet ortamı, elektronik faturalama eklentilerinde Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'tan bağlanabilecek kullanıcıları listelemelidir.</span><span class="sxs-lookup"><span data-stu-id="a0147-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="a0147-156">Yayınlama</span><span class="sxs-lookup"><span data-stu-id="a0147-156">Publication</span></span>

<span data-ttu-id="a0147-157">Hizmet ortamlarının kullanılması için elektronik faturalama eklentisi hizmetine yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a0147-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="a0147-158">Finance ve Supply Chain Management tarafından yalnızca yayınlanan ortamlara erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="a0147-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="a0147-159">Ek olarak, hizmet ortamının özniteliklerinde yapılacak güncelleştirmeler elektronik faturalama servisi üzerinde geçerli olmadan önce hizmet ortamı yayınlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a0147-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="a0147-160">Bağlı uygulamalar</span><span class="sxs-lookup"><span data-stu-id="a0147-160">Connected applications</span></span>

<span data-ttu-id="a0147-161">Bağlı uygulamalar, RCS üzerinden erişmek isteyebileceğiniz Finance ve Supply Chain Management kurulumlarıdır.</span><span class="sxs-lookup"><span data-stu-id="a0147-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="a0147-162">Uygulama URL'si ve kiracısının yanı sıra bağlı bir uygulama, RCS'nin ortama bağlanmasına olanak veren kimlik bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="a0147-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="a0147-163">Bağlı uygulamalar sayesinde, Finance ve Supply Chain Management'ta elektronik faturalama özelliğinin bir kısmını, tüm elektronik faturalama özelliğini çalışır hale getirmek için konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0147-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="a0147-164">Finance ve Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a0147-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="a0147-165">Elektronik faturalama eklentisi ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="a0147-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="a0147-166">Elektronik faturalama eklentisi üzerinden elektronik faturalar kesmek amacıyla Finance ve Supply Chain Management'ı kullanabilmeniz için eklentinin hizmetle iletişim kurulmasına izin verecek şekilde konfigüre edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0147-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="a0147-167">Elektronik faturalama eklentisi tümleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="a0147-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="a0147-168">Finance ve Supply Chain Management ile Elektronik faturalama eklentisi arasındaki iletişimi etkinleştirmek için **Özellik yönetimi** çalışma alanındaki **Elektronik faturalama eklentisi tümleştirme** özelliğini açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0147-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="a0147-169">Hizmet bitiş noktası</span><span class="sxs-lookup"><span data-stu-id="a0147-169">Service endpoint</span></span>

<span data-ttu-id="a0147-170">Servis uç noktası, elektronik faturalama eklentisinin bulunduğu URL'dir.</span><span class="sxs-lookup"><span data-stu-id="a0147-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="a0147-171">Elektronik fatura kesebilmek için Finance ve Supply Chain Management'ta servis uç noktalarının yapılandırılarak hizmetle iletişim kurulmasına izin vermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0147-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="a0147-172">Hizmet uç noktasını konfigüre etmek için **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametresi**'ne gidin ve **Gönderme hizmetleri** sekmesinde, **Elektronik faturalama eklentisi URL'si** alanına, **Servis uç noktası** bölümünde açıklanan şekilde tabloya URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="a0147-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="a0147-173">Ortamlar</span><span class="sxs-lookup"><span data-stu-id="a0147-173">Environments</span></span>

<span data-ttu-id="a0147-174">Finance ve Supply Chain Management'a girilen ortam adı, RCS'de oluşturulan ve Elektronik faturalama eklentisine yayınlanan ortam adına başvurur.</span><span class="sxs-lookup"><span data-stu-id="a0147-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="a0147-175">Ortam, elektronik fatura kesmeye yönelik her isteğin, Elektronik faturalama eklentisinin hangi elektronik faturalama özelliğinin talebi işlemesi gerektiğini belirleyebildiği bir ortam içermesi için **Elektronik belge parametresi** sayfasının **Gönderim servisleri** sekmesinde konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a0147-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0147-176">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a0147-176">Additional resources</span></span>

- [<span data-ttu-id="a0147-177">RCS'de elektronik faturaları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a0147-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="a0147-178">Finance ve Supply Chain Management'ta elektronik fatura kesme</span><span class="sxs-lookup"><span data-stu-id="a0147-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)

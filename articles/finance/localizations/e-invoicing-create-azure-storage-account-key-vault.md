---
title: Azure depolama hesabı ve bir anahtar kasası oluşturma
description: Bu konu, bir Azure depolama hesabı ve anahtar kasası oluşturma yöntemini açıklamaktadır.
author: gionoder
manager: AnnBe
ms.date: 02/12/2021
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
ms.openlocfilehash: 14463abe7782d786d286fcc619dee00ce85bb620
ms.sourcegitcommit: 4adc57b0e43d9627dca70762ac941762ec4934e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2021
ms.locfileid: "5479357"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="e6441-103">Azure depolama hesabı ve bir anahtar kasası oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6441-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="e6441-104">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="e6441-104">Prerequisites</span></span>

<span data-ttu-id="e6441-105">Bu konudaki adımları tamamlayabilmek için aşağıdaki görevlerin tamamlanmış olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="e6441-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="e6441-106">Azure'da anahtar kasası kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e6441-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="e6441-107">Daha fazla bilgi için bkz. [Azure Anahtar Kasası hakkında](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="e6441-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="e6441-108">Bir Azure depolama hesabı (Blob deposu) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e6441-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="e6441-109">Daha fazla bilgi için bkz [Azure Depolama Hesabını sürdürme](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="e6441-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="e6441-110">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="e6441-110">Overview</span></span>

<span data-ttu-id="e6441-111">Bu konuda, iki ana adımı tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="e6441-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="e6441-112">Depolama hesabı URI'sini almak için Azure depolama hesabını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="e6441-113">Depolama hesabı URI'sini depolamak için anahtar kasasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="e6441-114">Depolama hesabı URI'sini almak için Azure depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e6441-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="e6441-115">Elektronik faturalama eklentisi ile kullanmayı planladığınız depolama hesabını açın.</span><span class="sxs-lookup"><span data-stu-id="e6441-115">Open the storage account that you plan to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="e6441-116">**Blob hizmeti** \> **Kapsayıcılar** öğesine gidin ve yeni bir kapsayıcı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e6441-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="e6441-117">Kapsayıcı için bir ad girin ve **Ortak erişim düzeyi** alanını **Özel (anonim erişim yok**) olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="e6441-118">Kapsayıcıyı açın ve **Ayarlar \> Erişim ilkesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e6441-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="e6441-119">Depolanan erişim ilkesi eklemek için **İlke ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e6441-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="e6441-120">**Tanımlayıcı** ve **İzinler** alanlarını uygun şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="e6441-121">**İzinler** alanında, tüm izinleri seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e6441-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Blob depolama izni verme](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="e6441-123">Başlangıç ve bitiş tarihlerini girin.</span><span class="sxs-lookup"><span data-stu-id="e6441-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="e6441-124">Bitiş tarihi gelecekte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e6441-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="e6441-125">İlkeyi kaydetmek için **Tamam**'ı seçin ve sonra değişikliklerinizi kapsayıcıya kaydedin.</span><span class="sxs-lookup"><span data-stu-id="e6441-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="e6441-126">Depolama hesabına dönün ve **Depolama Gezgini (Önizleme)** ögesini açın.</span><span class="sxs-lookup"><span data-stu-id="e6441-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="e6441-127">Kapsayıcıyı sağ tıklayın ve sonra da **Paylaşılan Erişim İmzasını Al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e6441-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="e6441-128">**Paylaşılan Erişim İmzası** iletişim kutusunda, değeri **URI** alanına kopyalayın ve saklayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="e6441-129">Bu değer sonraki yordamda kullanılacak ve *paylaşılan erişim imza URI*'si olarak anılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e6441-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![URI değerini seçme ve kopyalama](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="e6441-131">Depolama hesabı URI'sini depolamak için anahtar kasasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e6441-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="e6441-132">Elektronik faturalama eklentisi ile kullanmayı planladığınız anahtar kasasını açın.</span><span class="sxs-lookup"><span data-stu-id="e6441-132">Open the key vault that you intend to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="e6441-133">**Ayarlar** \> **Gizli anahtarlar** ögesine gidin ve yeni bir gizli anahtar oluşturmak için **Oluştur/içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e6441-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="e6441-134">**Gizli anahtar oluştur** sayfasında **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e6441-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="e6441-135">Gizli anahtarın adını girin.</span><span class="sxs-lookup"><span data-stu-id="e6441-135">Enter the name of the secret.</span></span> <span data-ttu-id="e6441-136">Bu ad, Regulatory Configuration Service (RCS) içindeki servisin kurulumu sırasında kullanılacaktır ve *anahtar kasası gizli anahtar adı* olarak anılacak.</span><span class="sxs-lookup"><span data-stu-id="e6441-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="e6441-137">**Değer** alanında, **Paylaşılan Erişim İmza URI'si** ögesini seçin ve **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e6441-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="e6441-138">Elektronik faturalama eklentisini, oluşturduğunuz gizli anahtara doğru güvenli erişim düzeyine vermek için erişim ilkesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-138">Set up the access policy to grant the Electronic invoicing add-on the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="e6441-139">**Ayarlar \> Erişim ilkesi** ögesine gidin ve **Erişim ilkesi ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e6441-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="e6441-140">**Get** ve **List** işlemleri için gizli anahtar izinlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Servis erişimi verme](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="e6441-142">**Get** ve **List** işlemleri için sertifika izinlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Sertifika izni verme](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="e6441-144">**Sorumlu Seç** alanında, **Seçili yok** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e6441-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="e6441-145">**Sorumlu** iletişim kutusunda, **E-faturalama Hizmeti** ekleyerek sorumluyu seçin.</span><span class="sxs-lookup"><span data-stu-id="e6441-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="e6441-146">**Ekle**'yi seçin ve **Anahtar Kasa değişikliklerini kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e6441-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="e6441-147">**Genel Bakış** sayfasında, anahtar kasası için **DNS adı** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="e6441-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="e6441-148">Bu değer, servisin kurulumu sırasında, RCS'de kullanılır ve *anahtar kasa URI*'si olarak anılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e6441-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]


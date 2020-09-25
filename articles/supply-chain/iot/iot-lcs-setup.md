---
title: LCS'de IoT Zekası eklentisini yükleme
description: Bu konu, Microsoft Dynamics LifeCycle Services (LCS) Içindeki IoT Zekası eklentisinin nasıl yükleneceğini açıklamaktadır.
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae6b36c40d2f2f9e5266dfb3e2d1cbbb57755222
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803103"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="e2a60-103">LCS'de IoT Zekası eklentisini yükleme</span><span class="sxs-lookup"><span data-stu-id="e2a60-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2a60-104">Bu konu, Microsoft Dynamics LifeCycle Services (LCS) Içindeki IoT Zekası eklentisinin nasıl yükleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e2a60-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e2a60-105">Eklentilerin tanıtım/deneme ortamına yüklenemeyeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="e2a60-106">Eklentiyi yükleyebilmek için önce [Azure kaynaklarını oluşturmanız gerekir](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="e2a60-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="e2a60-107">LCS ortamını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e2a60-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="e2a60-108">LCS'yi açın ve Microsoft Dynamics 365 Supply Chain Management ortamınıza gidin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="e2a60-109">**Ortam eklentileri** bölümüne kaydırın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="e2a60-110">Ortam için etkinleştirilmiş eklentilerin listesini göstermek için **Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="e2a60-111">**Yüklemek için bir eklenti seçin** iletişim kutusunda **IoT Zekası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="e2a60-112">**Eklenti ayarlama** iletişim kutusunda IoT Hub'ın ve Redis önbelleğinin ayrıntılarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="e2a60-113">[Azure kaynakları oluştur](iot-azure-setup.md) altında oluşturduğunuz anahtar kasasında gerekli değerleri bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2a60-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="e2a60-114">**Kiracı kimliği:** Azure portalında, anahtar kasasına gidin ve sonra sol gezinti bölmesinde **Genel bakış**'ı seçip **Dizin kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="e2a60-115">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="e2a60-116">**IoT Olay Hub'ı ile uyumlu bitiş noktası Anahtar Kasası URI'si:** Anahtar kasasına gidin ve sol gezinti bölmesinde **Genel bakış**'ı seçip **DNS adı** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="e2a60-117">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="e2a60-118">**IoT Olayı Hub'ı ile uyumlu bitiş noktası gizli dizi adı:** Anahtar kasasına gidin ve sol gezinti bölmesinde, **Gizli diziler**'i seçip IoT Hub'ın olay hub'ı bağlantı dizesinin depolandığı gizli dizisinin adını kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="e2a60-119">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="e2a60-120">**Redis önbelleği anahtar kasası URI'si:** Anahtar kasasına gidin ve sol gezinti bölmesinde **Genel bakış**'ı seçip **DNS adı** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="e2a60-121">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="e2a60-122">**Redis önbelleği uç nokta gizli dizi adı:** Anahtar kasasına gidin ve sol gezinti bölmesinde, **Gizli diziler**'i seçip Redis önbelleği bağlantı dizesinin depolandığı gizli dizisinin adını kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="e2a60-123">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="e2a60-124">Hüküm ve koşulları kabul etmek için onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="e2a60-125">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-125">Select **Install**.</span></span>
8. <span data-ttu-id="e2a60-126">"Eklenti yükleme için başarıyla tetiklendi" yazılı bir ileti kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e2a60-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="e2a60-127">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-127">Select **OK**.</span></span>

<span data-ttu-id="e2a60-128">LCS ayarlama artık tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="e2a60-128">LCS setup is now completed.</span></span> <span data-ttu-id="e2a60-129">Sonraki adım, [senaryoları ayarlamak içindir](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="e2a60-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="e2a60-130">Eklentiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="e2a60-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="e2a60-131">Supply Chain Management'ta [senaryoları devre dışı bırakın](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="e2a60-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="e2a60-132">LCS'de, Supply Chain Management ortamınızın ayrıntılarına gidin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="e2a60-133">**Ortam eklentileri** bölümüne kaydırın.</span><span class="sxs-lookup"><span data-stu-id="e2a60-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="e2a60-134">IoT Zekası eklentisi için **Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a60-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>

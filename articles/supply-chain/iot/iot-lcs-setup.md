---
title: LCS'de IoT Zekası eklentisini yükleme
description: Bu konu, Microsoft Dynamics LifeCycle Services (LCS) Içindeki IoT Zekası eklentisinin nasıl yükleneceğini açıklamaktadır.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386569"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="336e9-103">LCS'de IoT Zekası eklentisini yükleme</span><span class="sxs-lookup"><span data-stu-id="336e9-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="336e9-104">Bu konu, Microsoft Dynamics LifeCycle Services (LCS) Içindeki IoT Zekası eklentisinin nasıl yükleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="336e9-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="336e9-105">Eklentiyi yükleyebilmek için önce [Azure kaynaklarını oluşturmanız gerekir](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="336e9-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="336e9-106">LCS ortamını ayarlama</span><span class="sxs-lookup"><span data-stu-id="336e9-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="336e9-107">LCS'yi açın ve Microsoft Dynamics 365 Supply Chain Management ortamınıza gidin.</span><span class="sxs-lookup"><span data-stu-id="336e9-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="336e9-108">**Ortam eklentileri** bölümüne kaydırın.</span><span class="sxs-lookup"><span data-stu-id="336e9-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="336e9-109">Ortam için etkinleştirilmiş eklentilerin listesini göstermek için **Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="336e9-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="336e9-110">**Yüklemek için bir eklenti seçin** iletişim kutusunda **IoT Zekası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e9-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="336e9-111">**Eklenti ayarlama** iletişim kutusunda IoT Hub'ın ve Redis önbelleğinin ayrıntılarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="336e9-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="336e9-112">[Azure kaynakları oluştur](iot-azure-setup.md) altında oluşturduğunuz anahtar kasasında gerekli değerleri bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="336e9-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="336e9-113">**Kiracı kimliği:** Azure portalında, anahtar kasasına gidin ve sonra sol gezinti bölmesinde **Genel bakış**'ı seçip **Dizin kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="336e9-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="336e9-114">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="336e9-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="336e9-115">**IoT Olay Hub'ı ile uyumlu bitiş noktası Anahtar Kasası URI'si:** Anahtar kasasına gidin ve sol gezinti bölmesinde **Genel bakış**'ı seçip **DNS adı** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="336e9-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="336e9-116">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="336e9-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="336e9-117">**IoT Olayı Hub'ı ile uyumlu bitiş noktası gizli dizi adı:** Anahtar kasasına gidin ve sol gezinti bölmesinde, **Gizli diziler**'i seçip IoT Hub'ın olay hub'ı bağlantı dizesinin depolandığı gizli dizisinin adını kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="336e9-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="336e9-118">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="336e9-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="336e9-119">**Redis önbelleği anahtar kasası URI'si:** Anahtar kasasına gidin ve sol gezinti bölmesinde **Genel bakış**'ı seçip **DNS adı** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="336e9-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="336e9-120">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="336e9-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="336e9-121">**Redis önbelleği uç nokta gizli dizi adı:** Anahtar kasasına gidin ve sol gezinti bölmesinde, **Gizli diziler**'i seçip Redis önbelleği bağlantı dizesinin depolandığı gizli dizisinin adını kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="336e9-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="336e9-122">Bu değeri **Eklenti ayarlama** iletişim kutusuna yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="336e9-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="336e9-123">Hüküm ve koşulları kabul etmek için onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="336e9-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="336e9-124">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="336e9-124">Select **Install**.</span></span>
8. <span data-ttu-id="336e9-125">"Eklenti yükleme için başarıyla tetiklendi" yazılı bir ileti kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="336e9-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="336e9-126">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e9-126">Select **OK**.</span></span>

<span data-ttu-id="336e9-127">LCS ayarlama artık tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="336e9-127">LCS setup is now completed.</span></span> <span data-ttu-id="336e9-128">Sonraki adım, [senaryoları ayarlamak içindir](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="336e9-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="336e9-129">Eklentiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="336e9-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="336e9-130">Supply Chain Management'ta [senaryoları devre dışı bırakın](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="336e9-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="336e9-131">LCS'de, Supply Chain Management ortamınızın ayrıntılarına gidin.</span><span class="sxs-lookup"><span data-stu-id="336e9-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="336e9-132">**Ortam eklentileri** bölümüne kaydırın.</span><span class="sxs-lookup"><span data-stu-id="336e9-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="336e9-133">IoT Zekası eklentisi için **Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e9-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>

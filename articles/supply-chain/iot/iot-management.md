---
title: IoT Zekası'nı izleme ve yönetme
description: Bu konu, IoT Zekası'nın nasıl izleneceğini ve yönetileceğini açıklar.
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
ms.openlocfilehash: 97a87b78a0178424f00e464262bb7f69e8a5b4a0
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386568"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="4b7d5-103">IoT Zekası'nı izleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="4b7d5-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b7d5-104">Bu konu, IoT Zekası'nın nasıl izleneceğini ve yönetileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="4b7d5-105">Microsoft Dynamics 365 Supply Chain Management'ta senaryoları izleme</span><span class="sxs-lookup"><span data-stu-id="4b7d5-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="4b7d5-106">IoT Zekası işlemesini çeşitli yerlerden izleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4b7d5-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="4b7d5-107">**Modüller \> Üretim denetimi \> Sorgular ve raporlar \> IoT Zekası \> Bildirimler** - Çözüme ulaşmamış bildirimlerin listesini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="4b7d5-108">**Modüller \> Üretim denetimi \> Sorgular ve raporlar \> IoT Zekası \> Kapanan bildirimler** - Çözüme ulaşmış veya kapatılmış bildirimlerin listesini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="4b7d5-109">**Modüller \> Üretim denetimi \> Sorgular ve raporlar \> IoT Zekası \> Ölçüm anahtarları** - **Kaynak Durumu** zaman serisi grafiklerinin ölçüm anahtarlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="4b7d5-110">**Modüller \> Üretim denetimi \> Üretim yürütme \> Kaynak durumu** – **Yapılandır** iletişim kutusunu kullanarak belirli ölçümleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="4b7d5-111">Senaryo bir özel durum algılarsa, özel durumun ayrıntılarını gösteren bir bildirim görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="4b7d5-112">**Çalışma alanları \> Üretim katı yönetimi \> Bildirimleri** - Çözüme ulaşmamış bildirimlerin listesini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="4b7d5-113">Çalışan bir IoT Zekası senaryosunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="4b7d5-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="4b7d5-114">Bir senaryo çalışırken şu değişiklikleri yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4b7d5-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="4b7d5-115">Yeni sensör şeması tanımları ekleme.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="4b7d5-116">Yeni sinyal verisi değerleri seçme.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-116">Select new signal data values.</span></span>
+ <span data-ttu-id="4b7d5-117">Var olan sinyal verisi değerlerinin seçimini iptal etme.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="4b7d5-118">Yeni sinyal verisi değerleri ekleme ve eşleme.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="4b7d5-119">Eşik değerlerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-119">Update threshold values.</span></span>

<span data-ttu-id="4b7d5-120">Bir senaryo çalışırken şu değişiklikler yapılamaz:</span><span class="sxs-lookup"><span data-stu-id="4b7d5-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="4b7d5-121">Etkin bir senaryo tarafından kullanılmakta olan tüm şema tanımlarını silme veya değiştirme.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="4b7d5-122">Etkin senaryonun seçili şema yollarını değiştirme.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="4b7d5-123">Benzetim seçenekleri</span><span class="sxs-lookup"><span data-stu-id="4b7d5-123">Simulation options</span></span>

<span data-ttu-id="4b7d5-124">Fabrika makine sinyallerinin benzetimini yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b7d5-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="4b7d5-125">Daha fazla bilgi edinmek için şu konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="4b7d5-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="4b7d5-126">IoT DevKit AZ3166'yı Azure IoT Hub'a bağlama</span><span class="sxs-lookup"><span data-stu-id="4b7d5-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="4b7d5-127">Raspberry Pi online simulator'ı Azure IoT Hub'a (Node. js) bağlama</span><span class="sxs-lookup"><span data-stu-id="4b7d5-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="4b7d5-128">Aygıt Benzetimi çözüm hızlandırıcısına genel bakış</span><span class="sxs-lookup"><span data-stu-id="4b7d5-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)

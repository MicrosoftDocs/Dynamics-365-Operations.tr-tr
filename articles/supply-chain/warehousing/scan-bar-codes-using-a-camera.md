---
title: Dynamics 365 for Finance and Operations - Ambarlama'da kamera kullanarak barkod okutma
description: Bu konuda, bir mobil cihazda kamera kullanarak barkodları taramak için Dynamics 365 for Finance and Operations – Ambarlama'nın nasıl kurulacağı açıklanmıştır.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e78d0a82d3ca66a6912ea1a9517296ca241edf1c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "319443"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="e3804-103">Dynamics 365 for Finance and Operations - Ambarlama'da kamera kullanarak barkod okutma</span><span class="sxs-lookup"><span data-stu-id="e3804-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3804-104">Bu konuda, bir mobil cihazda kamera kullanarak barkodları taramak için Dynamics 365 for Finance and Operations – Ambarlama'nın nasıl kurulacağı açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="e3804-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="e3804-105">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="e3804-105">Prerequisites</span></span>
<span data-ttu-id="e3804-106">Bu özelliği kullanmak için Ambarlama 1.2.0.0 sürümünün yüklü olması ve cihazınızın bir kameraya sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e3804-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="e3804-107">Güncelleştirmeden sonra uygulamayı açtığınızda, Dynamics 365 for Finance and Operations – Ambarlama uygulamasına kamerayı kullanma izni vermeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="e3804-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="e3804-108">Cihazınızda kamera yoksa istem görüntülenmez ve kamerayı tarayıcı olarak kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="e3804-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="e3804-109">Ayarlama</span><span class="sxs-lookup"><span data-stu-id="e3804-109">Setup</span></span>
<span data-ttu-id="e3804-110">Ambarlama uygulamasının Görüntüleme ayarlarında kameranın barkod taraması için kullanılıp kullanılmayacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3804-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="e3804-111">**Kamerayı tarayıcı olarak kullan**'ı etkinleştirirseniz kamerayı, **Tarama**'ya ayarlanmış tercih edilen giriş moduna sahip her giriş alanında kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3804-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="e3804-112">Giriş alanının taranabilir olup olmadığını denetlemek için Dynamics 365 for Finance and Operations'taki **Ambar uygulaması alan adları** sayfasında **Tercih edilen giriş modu**'nu **Tarama** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e3804-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="e3804-113">Bu seçenek belirlendiğinde, Ambarlama uygulamasında tarama yapmak için kamera kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e3804-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="e3804-114">Ambarlama uygulamasında uygulama alan adlarını yapılandırma hakkında bilgi için bkz. [Ambarlama uygulamasında uygulama alan adlarını yapılandırma](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="e3804-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="e3804-115">Desteklenen barkod biçimleri</span><span class="sxs-lookup"><span data-stu-id="e3804-115">Supported bar code formats</span></span>
<span data-ttu-id="e3804-116">Kod 128, Kod 39, Kod 93, EAN-8, EAN-13, UPC-E, UPC-A ve QR kodları da dahil olmak üzere en yaygın barkod biçimleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="e3804-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="e3804-117">Gezinme</span><span class="sxs-lookup"><span data-stu-id="e3804-117">Navigation</span></span>
<span data-ttu-id="e3804-118">Kamera sayfası, giriş alanının Tarama'ya ayarlanmış tercih edilen giriş moduna sahip olduğu her sayfada başlatılır. Kamera sayfasındayken, gezinmek için aşağıdaki seçenekleri kullanın:</span><span class="sxs-lookup"><span data-stu-id="e3804-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="e3804-119">Görev ve ayrıntılar sayfasına dönmek için geri düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3804-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="e3804-120">Girişi el ile yazabileceğiniz sayfaya gitmek için Görev ve ayrıntılar sayfasındaki kurşun kalem simgesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3804-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="e3804-121">Kamera sayfasına dönmek için Görev ve ayrıntılar sayfasındaki kameraya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e3804-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="e3804-122">Görev ve ayrıntılar sayfası</span><span class="sxs-lookup"><span data-stu-id="e3804-122">Task and details page</span></span> | <span data-ttu-id="e3804-123">Kamera sayfası</span><span class="sxs-lookup"><span data-stu-id="e3804-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![kamera-tarama-örnek-görev-ayrıntı-sayfa](./media/camera-scanning-example-task-detail-page50.png)          | ![kamera-tarama-örnek-kamera-sayfa-küçük](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="e3804-126">Kamera sayfasında, Kamera düğmesine tıkladığınızda, barkodu tanımlamaya çalışırken soluk görünür.</span><span class="sxs-lookup"><span data-stu-id="e3804-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="e3804-127">Barkod 5 saniye içinde tanımlanmazsa işlem zaman aşımına uğrar ve Kamera düğmesi tekrar kullanılabilir olur.</span><span class="sxs-lookup"><span data-stu-id="e3804-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="e3804-128">Ardından barkodu tekrar taramayı deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3804-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="e3804-129">Kamerayı barkoda yönelttiğinizde en iyi sonuca ulaşmak için barkodu köşeli parantez içinde hizalayın.</span><span class="sxs-lookup"><span data-stu-id="e3804-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="e3804-130">Barkod başarılı bir şekilde tarandığında sonuç işlenir ve bir sonraki adıma geçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3804-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="e3804-131">Sonraki adım, Tarama'ya ayarlanmış tercih edilen giriş moduna sahip başka bir giriş alanı içeriyorsa kamera yeniden başlatılır.</span><span class="sxs-lookup"><span data-stu-id="e3804-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="e3804-132">Sonraki adım tarama alanı değilse kamera sayfası başlatılmaz.</span><span class="sxs-lookup"><span data-stu-id="e3804-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>


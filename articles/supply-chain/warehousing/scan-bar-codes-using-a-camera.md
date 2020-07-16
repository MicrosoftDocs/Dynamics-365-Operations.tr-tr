---
title: Ambar uygulamasında kamera kullanarak barkod okutma
description: Bu konuda, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için ambar uygulamasının nasıl ayarlanacağı açıklanmaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: fd4818ab936e1c93000793da756c97df6d05b2a9
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530018"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a><span data-ttu-id="17e0d-103">Ambar uygulamasında kamera kullanarak barkod okutma</span><span class="sxs-lookup"><span data-stu-id="17e0d-103">Scan bar codes using a camera in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17e0d-104">Bu konuda, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için ambar uygulamasının nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="17e0d-104">This topic explains how to set up the warehouse app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="17e0d-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="17e0d-105">Prerequisites</span></span>
<span data-ttu-id="17e0d-106">Bu özelliği kullanmak için ambar uygulamasının 1.2.0.0 sürümünün yüklü olması ve cihazınızda bir kamera olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="17e0d-106">To use this feature, you need to have version 1.2.0.0 of the warehouse app installed, and your device must have a camera.</span></span> <span data-ttu-id="17e0d-107">Güncelleştirmeden sonra uygulamayı açtığınızda, uygulamaya kamerayı kullanma izni vermeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="17e0d-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="17e0d-108">Cihazınızda kamera yoksa istem görüntülenmez ve kamerayı tarayıcı olarak kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="17e0d-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="17e0d-109">Ayar</span><span class="sxs-lookup"><span data-stu-id="17e0d-109">Setup</span></span>
<span data-ttu-id="17e0d-110">Ambar uygulamasının Görüntüleme ayarlarında kameranın barkod taraması için kullanılıp kullanılmayacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17e0d-110">In the Display settings of the warehouse application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="17e0d-111">**Kamerayı tarayıcı olarak kullan**'ı etkinleştirirseniz kamerayı, **Tarama**'ya ayarlanmış tercih edilen giriş moduna sahip her giriş alanında kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17e0d-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="17e0d-112">Giriş alanının taranabilir olup olmadığını denetlemek için **Ambar uygulaması alan adları** sayfasında **Tercih edilen giriş modu**'nu **Tarama** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="17e0d-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="17e0d-113">Bu seçenek belirlendiğinde, ambar uygulamasında tarama yapmak için kamera kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="17e0d-113">When this option is selected, a camera can be used for scanning in the warehouse app.</span></span> <span data-ttu-id="17e0d-114">Ambar uygulamasında uygulama alan adlarını yapılandırma hakkında bilgi için bkz. [Ambar uygulamasında uygulama alan adlarını yapılandırma](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="17e0d-114">For information about how to configure app field names in Warehousing, see [Configure app field names in warehouse app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="17e0d-115">Desteklenen barkod biçimleri</span><span class="sxs-lookup"><span data-stu-id="17e0d-115">Supported bar code formats</span></span>
<span data-ttu-id="17e0d-116">Kod 128, Kod 39, Kod 93, EAN-8, EAN-13, UPC-E, UPC-A ve QR kodları da dahil olmak üzere en yaygın barkod biçimleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="17e0d-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="17e0d-117">Gezinme</span><span class="sxs-lookup"><span data-stu-id="17e0d-117">Navigation</span></span>
<span data-ttu-id="17e0d-118">Kamera sayfası, giriş alanının Tarama'ya ayarlanmış tercih edilen giriş moduna sahip olduğu her sayfada başlatılır. Kamera sayfasındayken, gezinmek için aşağıdaki seçenekleri kullanın:</span><span class="sxs-lookup"><span data-stu-id="17e0d-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="17e0d-119">Görev ve ayrıntılar sayfasına dönmek için geri düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17e0d-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="17e0d-120">Girişi el ile yazabileceğiniz sayfaya gitmek için Görev ve ayrıntılar sayfasındaki kurşun kalem simgesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17e0d-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="17e0d-121">Kamera sayfasına dönmek için Görev ve ayrıntılar sayfasındaki kameraya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17e0d-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="17e0d-122">Görev ve ayrıntılar sayfası</span><span class="sxs-lookup"><span data-stu-id="17e0d-122">Task and details page</span></span> | <span data-ttu-id="17e0d-123">Kamera sayfası</span><span class="sxs-lookup"><span data-stu-id="17e0d-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Kamera tarama örnek görevi ayrıntı sayfası](./media/camera-scanning-example-task-detail-page50.png)          | ![Kamera tarama örnek kamera sayfa küçük](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="17e0d-126">Kamera sayfasında, Kamera düğmesine tıkladığınızda, barkodu tanımlamaya çalışırken soluk görünür.</span><span class="sxs-lookup"><span data-stu-id="17e0d-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="17e0d-127">Barkod 5 saniye içinde tanımlanmazsa işlem zaman aşımına uğrar ve Kamera düğmesi tekrar kullanılabilir olur.</span><span class="sxs-lookup"><span data-stu-id="17e0d-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="17e0d-128">Ardından barkodu tekrar taramayı deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17e0d-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="17e0d-129">Kamerayı barkoda yönelttiğinizde en iyi sonuca ulaşmak için barkodu köşeli parantez içinde hizalayın.</span><span class="sxs-lookup"><span data-stu-id="17e0d-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="17e0d-130">Barkod başarılı bir şekilde tarandığında sonuç işlenir ve bir sonraki adıma geçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17e0d-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="17e0d-131">Sonraki adım, Tarama'ya ayarlanmış tercih edilen giriş moduna sahip başka bir giriş alanı içeriyorsa kamera yeniden başlatılır.</span><span class="sxs-lookup"><span data-stu-id="17e0d-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="17e0d-132">Sonraki adım tarama alanı değilse kamera sayfası başlatılmaz.</span><span class="sxs-lookup"><span data-stu-id="17e0d-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>


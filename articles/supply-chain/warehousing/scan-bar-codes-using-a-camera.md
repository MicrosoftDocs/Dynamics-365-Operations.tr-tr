---
title: Ambar Yönetimi mobil uygulamasında kamera kullanarak barkodları tarama
description: Bu konuda, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için Ambar Yönetimi mobil uygulamasının nasıl ayarlanacağı açıklanmaktadır.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831230"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="6ebd4-103">Ambar Yönetimi mobil uygulamasında kamera kullanarak barkodları tarama</span><span class="sxs-lookup"><span data-stu-id="6ebd4-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ebd4-104">Bu konuda, bir mobil cihazdaki kamerayı kullanarak barkodları taramak için Ambar Yönetimi mobil uygulamasının nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="6ebd4-105">Ayar</span><span class="sxs-lookup"><span data-stu-id="6ebd4-105">Setup</span></span>

<span data-ttu-id="6ebd4-106">Ambar Yönetimi mobil uygulamasının Görüntüleme ayarlarında kameranın barkod taraması için kullanılıp kullanılmayacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="6ebd4-107">**Kamerayı tarayıcı olarak kullan**'ı etkinleştirirseniz kamerayı, **Tarama**'ya ayarlanmış tercih edilen giriş moduna sahip her giriş alanında kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="6ebd4-108">Giriş alanının taranabilir olup olmadığını denetlemek için **Ambar uygulaması alan adları** sayfasında **Tercih edilen giriş modu**'nu **Tarama** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="6ebd4-109">Bu seçenek belirlendiğinde, Ambar Yönetimi mobil uygulamasında tarama yapmak için kamera kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="6ebd4-110">- Daha fazla bilgi için bkz. [Ambar Yönetimi mobil uygulaması için alanları yapılandırma](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="6ebd4-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="6ebd4-111">Desteklenen barkod biçimleri</span><span class="sxs-lookup"><span data-stu-id="6ebd4-111">Supported bar code formats</span></span>

<span data-ttu-id="6ebd4-112">Kod 128, Kod 39, Kod 93, EAN-8, EAN-13, UPC-E, UPC-A ve QR kodları da dahil olmak üzere en yaygın barkod biçimleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="6ebd4-113">Gezinme</span><span class="sxs-lookup"><span data-stu-id="6ebd4-113">Navigation</span></span>

<span data-ttu-id="6ebd4-114">Kamera sayfası, giriş alanının *Tarama*'ya ayarlanmış **tercih edilen giriş moduna** sahip olduğu her sayfada başlatılır. Kamera sayfasındayken, gezinmek için aşağıdaki seçenekleri kullanın:</span><span class="sxs-lookup"><span data-stu-id="6ebd4-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="6ebd4-115">**Görev ve ayrıntılar** sayfasına dönmek için geri düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="6ebd4-116">Girişi el ile yazabileceğiniz sayfaya gitmek için **Görev ve ayrıntılar** sayfasındaki kurşun kalem simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="6ebd4-117">Kamera sayfasına dönmek için **Görev ve ayrıntılar** sayfasındaki kamerayı seçin.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="6ebd4-118">Kamera sayfasında, Kamera düğmesini seçtiğinizde, barkodu tanımlamaya çalışırken soluk görünür.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="6ebd4-119">Barkod 5 saniye içinde tanımlanmazsa işlem zaman aşımına uğrar ve Kamera düğmesi tekrar kullanılabilir olur.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="6ebd4-120">Ardından barkodu tekrar taramayı deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="6ebd4-121">Kamerayı barkoda yönelttiğinizde en iyi sonuca ulaşmak için barkodu köşeli parantez içinde hizalayın.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="6ebd4-122">Barkod başarılı bir şekilde tarandığında sonuç işlenir ve bir sonraki adıma geçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="6ebd4-123">Sonraki adım, Tarama'ya ayarlanmış tercih edilen giriş moduna sahip başka bir giriş alanı içeriyorsa kamera yeniden başlatılır.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="6ebd4-124">Sonraki adım tarama alanı değilse kamera sayfası başlatılmaz.</span><span class="sxs-lookup"><span data-stu-id="6ebd4-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
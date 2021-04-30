---
title: İşlem tabanlı e-postalara ve makbuz e-postalarına QR kodu veya barkod ekleme
description: Bu konu, Microsoft Dynamics 365 Commerce'de işlem tabanlı e-postalara ve makbuz e-postalarına sıra kimliklerini temsil eden QR kodlarının ve barkodların nasıl ekleneceğini açıklamaktadır.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 791b244c867ea4263f08250abf220a1b75784cad
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907875"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="92822-103">İşlem tabanlı e-postalara ve makbuz e-postalarına QR kodu veya barkod ekleme</span><span class="sxs-lookup"><span data-stu-id="92822-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92822-104">Bu konu, Microsoft Dynamics 365 Commerce'de işlem tabanlı e-postalara ve makbuz e-postalarına sıra kimliklerini temsil eden QR kodlarının ve barkodların nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="92822-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="92822-105">Bir perakende ortamında sipariş arama sürecini hızlandırmaya yardımcı olacak şekilde, işlem tabanlı e-postalara QR kodlarını ve barkodları kolayca dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92822-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="92822-106">E-postalara QR kodları ve Barkodlar eklemek için, oluşturma ve işleme servinden QR kodu veya barkod görüntüsü isteyen bir HTML **\<img\>** etiketi kullanın.</span><span class="sxs-lookup"><span data-stu-id="92822-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="92822-107">Microsoft bu hizmeti sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="92822-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="92822-108">Ancak, bir sorgu dizesinde geçirilen bir değere dayalı olarak dinamik olarak oluşturulan QR kodları veya Barkod hizmeti veren birçok ücretsiz veya uygun fiyatlı hizmet vardır.</span><span class="sxs-lookup"><span data-stu-id="92822-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="92822-109">İşlem tabanlı bir e-postaya QR kodu veya barkod ekleme</span><span class="sxs-lookup"><span data-stu-id="92822-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="92822-110">Bir e-ticaret satın alma işleminin parçası olarak gönderilen işlem tabanlı bir e-postaya bir QR kodu veya barkod eklemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="92822-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="92822-111">İşlem tabanlı e-posta şablonu için kaynak HTML'i açın ve QR kodu veya barkod hizmetinize işaret eden bir HTML **\<img\>** etiketi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="92822-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="92822-112">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="92822-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="92822-113">Önceki örnekle ilgili aşağıda bir açıklama verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="92822-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="92822-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** QR kodu veya barkod hizmetinizin etki alanını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="92822-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="92822-115">**data**, QR kodu veya barkod hizmetinin, QR kodu veya barkod olarak işlenmesi gereken içeriği almak için kullandığı parametreyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="92822-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="92822-116">**%salesid%** değeri bu parametreye atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="92822-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="92822-117">Bu örnekte, değerin görüntü için alternatif metin olarak da kullanıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="92822-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="92822-118">**param1** ve **param2** ek isteğe bağlı parametreleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="92822-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="92822-119">**Retail ve Commerce \> Headquarters kurulum \> parametreler \> kuruluş e-posta şablonları**'na gidin ve güncelleştirilmiş HTML'i uygun işlem tabanlı e-posta şablonuna yükleyin.</span><span class="sxs-lookup"><span data-stu-id="92822-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="92822-120">QR kodu ve barkod hizmeti sağlayıcıları arasında parametreler farklılık gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="92822-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="92822-121">Bu nedenle, değer atamanız gereken parametreleri onaylamak için servis sağlayıcınızla mutlaka iletişim kurun.</span><span class="sxs-lookup"><span data-stu-id="92822-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="92822-122">Bir makbuz e-postasına QR kodu veya barkod ekleme</span><span class="sxs-lookup"><span data-stu-id="92822-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="92822-123">Satış noktasında (POS) bir satın alma yapıldıktan sonra gönderilebilecek bir makbuz e-postasına QR kodu veya barkod eklemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="92822-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="92822-124">Makbuz e-postası şablonu için kaynak HTML'i açın ve QR kodu veya barkod hizmetinize işaret eden bir HTML **\<img\>** etiketi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="92822-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="92822-125">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="92822-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="92822-126">Önceki örnekle ilgili aşağıda bir açıklama verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="92822-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="92822-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** QR kodu veya barkod hizmetinizin etki alanını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="92822-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="92822-128">**data**, QR kodu veya barkod hizmetinin, QR kodu veya barkod olarak işlenmesi gereken içeriği almak için kullandığı parametreyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="92822-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="92822-129">**%receiptid%** değeri bu parametreye atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="92822-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="92822-130">Bu örnekte, değerin görüntü için alternatif metin olarak da kullanıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="92822-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="92822-131">**param1** ve **param2** ek isteğe bağlı parametreleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="92822-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="92822-132">**Retail ve Commerce \> Headquarters kurulum \> parametreler \> kuruluş e-posta şablonları**'na gidin ve güncelleştirilmiş HTML'i **emailrecpt** e-posta kimliğine yükleyin.</span><span class="sxs-lookup"><span data-stu-id="92822-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="92822-133">QR kodu ve barkod hizmeti sağlayıcıları arasında parametreler farklılık gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="92822-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="92822-134">Bu nedenle, değer atamanız gereken parametreleri onaylamak için servis sağlayıcınızla mutlaka iletişim kurun.</span><span class="sxs-lookup"><span data-stu-id="92822-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92822-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="92822-135">Additional resources</span></span>

[<span data-ttu-id="92822-136">Modern POS'tan (MPOS) e-posta makbuzları gönderme</span><span class="sxs-lookup"><span data-stu-id="92822-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="92822-137">Hareket olayları için e-posta şablonları oluşturma</span><span class="sxs-lookup"><span data-stu-id="92822-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)

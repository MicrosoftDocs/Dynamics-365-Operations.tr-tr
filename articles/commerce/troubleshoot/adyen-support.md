---
title: Adyen için Dynamics 365 Payment Connector sorunlarını giderme
description: Bu konu, Adyen için Microsoft Dynamics 365 Payment Connector ile ilgili sorunlar olduğunda destek almanıza yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801831"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="914e2-103">Adyen için Dynamics 365 Payment Connector sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="914e2-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="914e2-104">Bu konu, Adyen için Microsoft Dynamics 365 Payment Connector ile ilgili sorunlar olduğunda destek almanıza yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="914e2-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="914e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="914e2-105">Description</span></span>

<span data-ttu-id="914e2-106">Aşağıdaki alanlarda Adyen için Dynamics 365 Payment Connector ile sorunlarınız var ve Adyen ekibinden destek istiyorsunuz:</span><span class="sxs-lookup"><span data-stu-id="914e2-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="914e2-107">Satış noktası (POS), modern satış noktası (MPOS), arama merkezi veya Dynamics 365 Commerce yapılandırması</span><span class="sxs-lookup"><span data-stu-id="914e2-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="914e2-108">Adyen ödeme servisi sağlayıcısı (PSP) referans numarası (örneğin, el ile yapılan anahtar girişi \[MKE\] reddi dahil, retlerle ilgili sorularınız varsa)</span><span class="sxs-lookup"><span data-stu-id="914e2-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="914e2-109">Test veya canlı satıcı ortamlarında çalışmayan her şey</span><span class="sxs-lookup"><span data-stu-id="914e2-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="914e2-110">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="914e2-110">Resolution</span></span>

<span data-ttu-id="914e2-111">Adyen ekibi ile destek sürecini başlatmak için aşağıdaki e-posta şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="914e2-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="914e2-112">Sorun giderme işlemlerini hızlandırmak için, e-postanın gerekli tüm ayrıntıları içerdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="914e2-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="914e2-113">Alan</span><span class="sxs-lookup"><span data-stu-id="914e2-113">Field</span></span>        | <span data-ttu-id="914e2-114">Değer</span><span class="sxs-lookup"><span data-stu-id="914e2-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="914e2-115">Gittiği yer</span><span class="sxs-lookup"><span data-stu-id="914e2-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="914e2-116">Bilgi</span><span class="sxs-lookup"><span data-stu-id="914e2-116">Cc</span></span>           | |
| <span data-ttu-id="914e2-117">Konu satırı</span><span class="sxs-lookup"><span data-stu-id="914e2-117">Subject line</span></span> | <span data-ttu-id="914e2-118">Microsoft Dynamics Destek talebi</span><span class="sxs-lookup"><span data-stu-id="914e2-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="914e2-119">Gövde</span><span class="sxs-lookup"><span data-stu-id="914e2-119">Body</span></span>         | <p><span data-ttu-id="914e2-120">Merhaba Destek Ekibi,</span><span class="sxs-lookup"><span data-stu-id="914e2-120">Hi Support,</span></span></p><p><span data-ttu-id="914e2-121">Lütfen aşağıdaki sorun için destek sağlayın:</span><span class="sxs-lookup"><span data-stu-id="914e2-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="914e2-122">Tüccar hesabı</span><span class="sxs-lookup"><span data-stu-id="914e2-122">Merchant account</span></span></li><li><span data-ttu-id="914e2-123">Ortam (test/üretim)</span><span class="sxs-lookup"><span data-stu-id="914e2-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="914e2-124">Kanal (POS/çağrı merkezi/Commerce e-ticaret)</span><span class="sxs-lookup"><span data-stu-id="914e2-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="914e2-125">PSP referans numarası, sorun belirli bir işlemi kapsıyorsa (PSP referans numarasını makbuzda, Adyen müşteri alanında veya POS terminalindeki işlemler menüsünde bulabilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="914e2-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="914e2-126">Varsa hata iletisinin ekran görüntüsü veya fotoğrafı</span><span class="sxs-lookup"><span data-stu-id="914e2-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="914e2-127">Olay Görüntüleyicisi günlükleri (.txt biçiminde)</span><span class="sxs-lookup"><span data-stu-id="914e2-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="914e2-128">Sorunun açıklaması ve denediğiniz sorun giderme adımları</span><span class="sxs-lookup"><span data-stu-id="914e2-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="914e2-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="914e2-129">Additional resources</span></span>

[<span data-ttu-id="914e2-130">Dynamics 365 Commerce için Adyen bağlayıcıyla ödeme kabul etme</span><span class="sxs-lookup"><span data-stu-id="914e2-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="914e2-131">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="914e2-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="914e2-132">Dynamics 365 için Adyen Payment Connector sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="914e2-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

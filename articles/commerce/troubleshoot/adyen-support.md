---
title: Adyen için Dynamics 365 Payment Connector sorunlarını giderme
description: Bu konu, Adyen için Microsoft Dynamics 365 Payment Connector ile ilgili sorunlar olduğunda destek almanıza yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 707efeba9553b996e4e33a4754e42a9d22643e33
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019601"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="bd1d1-103">Adyen için Dynamics 365 Payment Connector sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="bd1d1-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd1d1-104">Bu konu, Adyen için Microsoft Dynamics 365 Payment Connector ile ilgili sorunlar olduğunda destek almanıza yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="bd1d1-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="bd1d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd1d1-105">Description</span></span>

<span data-ttu-id="bd1d1-106">Aşağıdaki alanlarda Adyen için Dynamics 365 Payment Connector ile sorunlarınız var ve Adyen ekibinden destek istiyorsunuz:</span><span class="sxs-lookup"><span data-stu-id="bd1d1-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="bd1d1-107">Satış noktası (POS), modern satış noktası (MPOS), arama merkezi veya Dynamics 365 Commerce yapılandırması</span><span class="sxs-lookup"><span data-stu-id="bd1d1-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="bd1d1-108">Adyen ödeme servisi sağlayıcısı (PSP) referans numarası (örneğin, el ile yapılan anahtar girişi \[MKE\] reddi dahil, retlerle ilgili sorularınız varsa)</span><span class="sxs-lookup"><span data-stu-id="bd1d1-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="bd1d1-109">Test veya canlı satıcı ortamlarında çalışmayan her şey</span><span class="sxs-lookup"><span data-stu-id="bd1d1-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="bd1d1-110">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="bd1d1-110">Resolution</span></span>

<span data-ttu-id="bd1d1-111">Adyen ekibi ile destek sürecini başlatmak için aşağıdaki e-posta şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="bd1d1-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="bd1d1-112">Sorun giderme işlemlerini hızlandırmak için, e-postanın gerekli tüm ayrıntıları içerdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="bd1d1-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="bd1d1-113">Alan</span><span class="sxs-lookup"><span data-stu-id="bd1d1-113">Field</span></span>        | <span data-ttu-id="bd1d1-114">Değer</span><span class="sxs-lookup"><span data-stu-id="bd1d1-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="bd1d1-115">Gittiği yer</span><span class="sxs-lookup"><span data-stu-id="bd1d1-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="bd1d1-116">Bilgi</span><span class="sxs-lookup"><span data-stu-id="bd1d1-116">Cc</span></span>           | |
| <span data-ttu-id="bd1d1-117">Konu satırı</span><span class="sxs-lookup"><span data-stu-id="bd1d1-117">Subject line</span></span> | <span data-ttu-id="bd1d1-118">Microsoft Dynamics Destek talebi</span><span class="sxs-lookup"><span data-stu-id="bd1d1-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="bd1d1-119">Gövde</span><span class="sxs-lookup"><span data-stu-id="bd1d1-119">Body</span></span>         | <p><span data-ttu-id="bd1d1-120">Merhaba Destek Ekibi,</span><span class="sxs-lookup"><span data-stu-id="bd1d1-120">Hi Support,</span></span></p><p><span data-ttu-id="bd1d1-121">Lütfen aşağıdaki sorun için destek sağlayın:</span><span class="sxs-lookup"><span data-stu-id="bd1d1-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="bd1d1-122">Tüccar hesabı</span><span class="sxs-lookup"><span data-stu-id="bd1d1-122">Merchant account</span></span></li><li><span data-ttu-id="bd1d1-123">Ortam (test/üretim)</span><span class="sxs-lookup"><span data-stu-id="bd1d1-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="bd1d1-124">Kanal (POS/çağrı merkezi/Commerce e-ticaret)</span><span class="sxs-lookup"><span data-stu-id="bd1d1-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="bd1d1-125">PSP referans numarası, sorun belirli bir işlemi kapsıyorsa (PSP referans numarasını makbuzda, Adyen müşteri alanında veya POS terminalindeki işlemler menüsünde bulabilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="bd1d1-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="bd1d1-126">Varsa hata iletisinin ekran görüntüsü veya fotoğrafı</span><span class="sxs-lookup"><span data-stu-id="bd1d1-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="bd1d1-127">Olay Görüntüleyicisi günlükleri (.txt biçiminde)</span><span class="sxs-lookup"><span data-stu-id="bd1d1-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="bd1d1-128">Sorunun açıklaması ve denediğiniz sorun giderme adımları</span><span class="sxs-lookup"><span data-stu-id="bd1d1-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="bd1d1-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bd1d1-129">Additional resources</span></span>

[<span data-ttu-id="bd1d1-130">Dynamics 365 Commerce için Adyen bağlayıcıyla ödeme kabul etme</span><span class="sxs-lookup"><span data-stu-id="bd1d1-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="bd1d1-131">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="bd1d1-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="bd1d1-132">Dynamics 365 için Adyen Payment Connector sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="bd1d1-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

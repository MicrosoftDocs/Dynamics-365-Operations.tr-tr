---
title: İade siparişinde para iadesi reddedildi
description: Bu konu, faturalama için kullanılan kredi kartı orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğundan, bir iade siparişindeki para iadesi reddedildiğinde size yardımcı olacak sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 99fd4b816b1a3a1fe3c2d1579be45b43fdc3d385
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020768"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="cd42b-103">İade siparişinde para iadesi reddedildi</span><span class="sxs-lookup"><span data-stu-id="cd42b-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd42b-104">Bu konu, faturalama için kullanılan kredi kartı orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğundan, bir iade siparişindeki para iadesi reddedildiğinde size yardımcı olacak sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd42b-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="cd42b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd42b-105">Description</span></span>

<span data-ttu-id="cd42b-106">İade siparişini faturalamak için kullanılan kredi kartı, orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğunda para iadesi reddediliyor.</span><span class="sxs-lookup"><span data-stu-id="cd42b-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="cd42b-107">Şu hata iletisini alırsınız: "Bazı Ödemeler deftere nakil için doğru durumda değil.</span><span class="sxs-lookup"><span data-stu-id="cd42b-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="cd42b-108">Lütfen faturalamadan önce tüm ödemelerin durumunu yeniden doğrulayın."</span><span class="sxs-lookup"><span data-stu-id="cd42b-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="cd42b-109">Ödeme onayı ayrıntıları aşağıdaki hata iletisini içerecektir: "adyen Gateway SendRequest (), 'InternalServerError'.22144 durumuyla başarısız oldu; Adyen'den boş yanıt döndürüldü.(22001);"</span><span class="sxs-lookup"><span data-stu-id="cd42b-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![İade siparişinde reddedilen para iadesi hatası](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="cd42b-111">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="cd42b-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="cd42b-112">Adyen'de görünmeyen iadeleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="cd42b-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="cd42b-113">Görünmeyen iadeleri etkinleştirmek için, Adyen destek ekibiyle iletişim kurmak ve Adyen satıcı hesabınızda görünmeyen iadelerin etkinleştirilmesini istemek için [Adyen için Dynamics 365 Payment Connector sorunlarını giderme](adyen-support.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="cd42b-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd42b-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cd42b-114">Additional resources</span></span>

[<span data-ttu-id="cd42b-115">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="cd42b-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="cd42b-116">Dynamics 365 için Adyen Payment Connector sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="cd42b-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

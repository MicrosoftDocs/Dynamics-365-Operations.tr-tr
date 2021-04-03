---
title: İade siparişinde para iadesi reddedildi
description: Bu konu, faturalama için kullanılan kredi kartı orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğundan, bir iade siparişindeki para iadesi reddedildiğinde size yardımcı olacak sorun giderme kılavuzu sağlar.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: e202c6b4b9e025d5af1cd5eb6235884aab6444e6
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585579"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="00c28-103">İade siparişinde para iadesi reddedildi</span><span class="sxs-lookup"><span data-stu-id="00c28-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00c28-104">Bu konu, faturalama için kullanılan kredi kartı orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğundan, bir iade siparişindeki para iadesi reddedildiğinde size yardımcı olacak sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="00c28-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="00c28-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00c28-105">Description</span></span>

<span data-ttu-id="00c28-106">İade siparişini faturalamak için kullanılan kredi kartı, orijinal ödeme yetkilendirmesi sırasında kullanılan karttan farklı olduğunda para iadesi reddediliyor.</span><span class="sxs-lookup"><span data-stu-id="00c28-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="00c28-107">Şu hata iletisini alırsınız: "Bazı Ödemeler deftere nakil için doğru durumda değil.</span><span class="sxs-lookup"><span data-stu-id="00c28-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="00c28-108">Lütfen faturalamadan önce tüm ödemelerin durumunu yeniden doğrulayın."</span><span class="sxs-lookup"><span data-stu-id="00c28-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="00c28-109">Ödeme onayı ayrıntıları aşağıdaki hata iletisini içerecektir: "adyen Gateway SendRequest (), 'InternalServerError'.22144 durumuyla başarısız oldu; Adyen'den boş yanıt döndürüldü.(22001);"</span><span class="sxs-lookup"><span data-stu-id="00c28-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![İade siparişinde reddedilen para iadesi hatası](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="00c28-111">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="00c28-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="00c28-112">Adyen'de görünmeyen iadeleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="00c28-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="00c28-113">Görünmeyen iadeleri etkinleştirmek için, Adyen destek ekibiyle iletişim kurmak ve Adyen satıcı hesabınızda görünmeyen iadelerin etkinleştirilmesini istemek için [Adyen için Dynamics 365 Payment Connector sorunlarını giderme](adyen-support.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="00c28-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00c28-114">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="00c28-114">Additional resources</span></span>

[<span data-ttu-id="00c28-115">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="00c28-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="00c28-116">Dynamics 365 için Adyen Payment Connector sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="00c28-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

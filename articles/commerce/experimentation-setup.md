---
title: Deneme ayarlama
description: Bu konuda, üçüncü taraf bir hizmette deneme ayarlamanın nasıl yapılacağı anlatılmaktadır.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 29c21ceb4c259f463f4a039942e51141201a9809
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097059"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="a802c-103">Deneme ayarlama</span><span class="sxs-lookup"><span data-stu-id="a802c-103">Set up an experiment</span></span>

<span data-ttu-id="a802c-104">[Bir varsayım tanımladıktan ve hangi başarı ölçümlerini kullanmak istediğinizi belirledikten](experimentation-identify.md) sonra üçüncü taraf hizmette denemenizi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a802c-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="a802c-105">Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a802c-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a802c-106">Ek adımlar ayrı konularda ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="a802c-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="a802c-107">[ ![Deneme kullanıcı yolculuğu - Ayarlama](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a802c-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="a802c-108">Üçüncü taraf hizmetinde denemenizi ayarlama</span><span class="sxs-lookup"><span data-stu-id="a802c-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="a802c-109">Artık denemenizi çalıştırmak ve izlemek için üçüncü taraf hizmetinizi seçmiş ve deneme bağlayıcısını ayarlamanız olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a802c-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="a802c-110">Bu önkoşullar [Dynamics 365 Commerce'ta deneme](experimentation-overview.md) bölümünde listelenir.</span><span class="sxs-lookup"><span data-stu-id="a802c-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="a802c-111">Üçüncü taraf hizmetinde denemenizi oluşturmak için gereken adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a802c-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="a802c-112">Bağlayıcı doğru yapılandırılırsa, üçüncü taraf hizmetinde ayarladığınız tüm denemelerin listesi, yaklaşık 5 dakika içinde Commerce site oluşturucuda görünür.</span><span class="sxs-lookup"><span data-stu-id="a802c-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="a802c-113">Başarı ölçümlerinizi ayarlama</span><span class="sxs-lookup"><span data-stu-id="a802c-113">Set up your success metrics</span></span>
<span data-ttu-id="a802c-114">Her deneme varyasyonların etkisini ölçmek ve varsayımı doğrulamak için ölçümlere gereksinim duyar.</span><span class="sxs-lookup"><span data-stu-id="a802c-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="a802c-115">Dynamics 365 Commerce'taki canlı telemetri olaylarını kullanarak üçüncü taraf hizmetindeki ölçümlerin hesaplanmasını sağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a802c-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a802c-116">Başarı ölçümlerinizi ayarlamak için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="a802c-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="a802c-117">Commerce site oluşturucuda sol gezinti bölmesinde **Sayfalar** sekmesini seçin ve sonra ölçümleri toplamak istediğiniz sayfayı seçin.</span><span class="sxs-lookup"><span data-stu-id="a802c-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="a802c-118">İzlemek istediğiniz sayfanın veya modülün sağ özellik bölmesindeki **İzlenecek olay kimlikleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a802c-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="a802c-119">**Görüntüle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a802c-119">Select **View**.</span></span> <span data-ttu-id="a802c-120">Tüm olay kimliklerinin listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a802c-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="a802c-121">İzlemek istediğiniz olayı kopyalayın ve olay anahtarını üçüncü taraf hizmetinde belirtilen konuma yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="a802c-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="a802c-122">Birden fazla olaya gereksinim duyarsanız, anahtarları tek tek kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="a802c-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="a802c-123">Sayfa görünümleri ve gelir izleme dahil tüm kullanılabilir olay ve özniteliklerin nasıl görüntüleneceğini öğrenmek için bkz. [Tanılama ve sorun giderme için Commerce bileşeni olayları](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="a802c-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="a802c-124">Üçüncü taraf hizmetinde, ölçümleri izlemek için diğer adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a802c-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="a802c-125">Önceki adım</span><span class="sxs-lookup"><span data-stu-id="a802c-125">Previous step</span></span>
[<span data-ttu-id="a802c-126">Varsayım tanımlama ve deneme için ölçümleri belirleme</span><span class="sxs-lookup"><span data-stu-id="a802c-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="a802c-127">Sonraki adım</span><span class="sxs-lookup"><span data-stu-id="a802c-127">Next step</span></span>
[<span data-ttu-id="a802c-128">Deneme bağlama ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="a802c-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

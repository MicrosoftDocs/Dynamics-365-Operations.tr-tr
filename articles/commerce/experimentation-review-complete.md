---
title: Varyasyon yükseltme ve deneme tamamlama
description: Bu konu, Dynamics 365 Commerce'ta başarılı bir varyasyonun nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklar.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930304"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="fdc6e-103">Varyasyon yükseltme ve deneme tamamlama</span><span class="sxs-lookup"><span data-stu-id="fdc6e-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="fdc6e-104">Bu konu, denemede en iyi sonuçları üreten değişimin nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="fdc6e-105">Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="fdc6e-106">Ek adımlar ayrı konularda ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="fdc6e-107">[ ![Deneme kullanıcı yolculuğu - İnceleme ve Tamamlama](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="fdc6e-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="fdc6e-108">[Denemenizi çalıştırdıktan](experimentation-run-monitor.md) ve canlı sitenizde hangi varyasyonu kullanmak istediğinizi belirlemek için yeterli veri topladıktan sonra varyasyonu yükseltip denemeyi sonlandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="fdc6e-109">Varyasyon yükseltme</span><span class="sxs-lookup"><span data-stu-id="fdc6e-109">Promote a variation</span></span>
<span data-ttu-id="fdc6e-110">Hangi varyasyonun en iyi sonuçları ürettiğine karar vermek için, üçüncü taraf hizmetteki denemeyle ilgili verileri ve analizleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="fdc6e-111">Web sitenizin tüm kullanıcıları tarafından kullanılabilmesi için canlı sitedeki geçerli içeriği kazanan varyasyonla değiştirmek için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="fdc6e-112">Site oluşturucuda **Denemeler** sekmesine gidin ve denemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="fdc6e-113">Üst çubukta **Denemeyi tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="fdc6e-114">**Denemeyi tamamla** iletişim kutusu menüsünde, **Deneme verilerini gözden geçir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="fdc6e-115">Ölçümleri doğrulayabileceğiniz ve hangi varyasyonun en iyi performansı gösterdiğini belirleyebileceğiniz üçüncü taraf hizmeti açılır.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="fdc6e-116">Site oluşturucudaki **Denemeyi tamamla** iletişim kutusu menüsünde kazanan varyasyonu ve ardından **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="fdc6e-117">Üçüncü taraf hizmetini açın ve denemeyi durdurun.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="fdc6e-118">Site oluşturucuda, orijinal canlı sayfanın üzerine yazmak ve web sitenizin tüm kullanıcılarına sunulması için kazanan varyasyonu yayımlamak üzere **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="fdc6e-119">Geçerli canlı sayfayı saklamayı ve bir varyasyon yayımlamamayı tercih ederseniz, **Özgün sayfayı yeniden yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="fdc6e-120">Denemenizi silme</span><span class="sxs-lookup"><span data-stu-id="fdc6e-120">Delete your experiment</span></span>
<span data-ttu-id="fdc6e-121">Commerce'ta tamamlanmış bir denemeyi silmeniz gerekli olmasa da alan kazanmak veya çalışma alanınızı temizlemek için denemeyi silmeyi tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="fdc6e-122">Bir denemeyi silmek için aşağıdakileri yapın.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="fdc6e-123">Site oluşturucuda **Denemeler** sekmesine gidin ve denemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="fdc6e-124">Deneme hala etkinse, devam etmeden önce üçüncü taraf hizmetinde denemeyi durdurun.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="fdc6e-125">Varyasyon içeriğini canlı siteden kaldırmak için komut çubuğunda **Yayımdan Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="fdc6e-126">Denemeyi silmek için komut çubuğunda **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="fdc6e-127">Önceki adım</span><span class="sxs-lookup"><span data-stu-id="fdc6e-127">Previous step</span></span>
[<span data-ttu-id="fdc6e-128">Deneme çalıştırma ve izleme</span><span class="sxs-lookup"><span data-stu-id="fdc6e-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)

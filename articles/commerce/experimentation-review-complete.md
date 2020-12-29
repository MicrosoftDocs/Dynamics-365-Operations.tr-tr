---
title: Varyasyon yükseltme ve deneme tamamlama
description: Bu konu, Dynamics 365 Commerce'ta başarılı bir varyasyonun nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklar.
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
ms.openlocfilehash: c7da601323663d4c1ea76f7cad7bdab8e7632d1c
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4416569"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="e6ab1-103">Varyasyon yükseltme ve deneme tamamlama</span><span class="sxs-lookup"><span data-stu-id="e6ab1-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="e6ab1-104">Bu konu, denemede en iyi sonuçları üreten değişimin nasıl yükseltileceğini ve denemenin nasıl tamamlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="e6ab1-105">Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e6ab1-106">Ek adımlar ayrı konularda ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="e6ab1-107">[ ![Deneme kullanıcı yolculuğu - İnceleme ve Tamamlama](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="e6ab1-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="e6ab1-108">[Denemenizi çalıştırdıktan](experimentation-run-monitor.md) ve canlı sitenizde hangi varyasyonu kullanmak istediğinizi belirlemek için yeterli veri topladıktan sonra varyasyonu yükseltip denemeyi sonlandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="e6ab1-109">Varyasyon yükseltme</span><span class="sxs-lookup"><span data-stu-id="e6ab1-109">Promote a variation</span></span>
<span data-ttu-id="e6ab1-110">Hangi varyasyonun en iyi sonuçları ürettiğine karar vermek için, üçüncü taraf hizmetteki denemeyle ilgili verileri ve analizleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="e6ab1-111">Ardından web sitenizin tüm kullanıcıları tarafından kullanılabilmesi için canlı sitedeki geçerli içeriği, kazanan varyasyonla değiştirerek yükseltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="e6ab1-112">Kazanan varyasyonu yükseltmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="e6ab1-113">Commerce site oluşturucuda, sol gezinti bölmesinde **Denemeler**'i seçin ve ardından denemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="e6ab1-114">Komut çubuğunda **Denemeyi tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="e6ab1-115">**Denemeyi tamamla** iletişim kutusunda **Deneme verilerini gözden geçir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="e6ab1-116">Ölçümleri doğrulayabileceğiniz ve hangi varyasyonun en iyi performansı gösterdiğini belirleyebileceğiniz üçüncü taraf hizmeti açılır.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="e6ab1-117">**Denemeyi tamamla** iletişim kutusunda kazanan varyasyonu ve ardından **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="e6ab1-118">Üçüncü taraf hizmetini açın ve denemeyi durdurun.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="e6ab1-119">Site oluşturucuda, orijinal canlı sayfanın üzerine yazmak ve web sitenizin tüm kullanıcılarına sunulması için kazanan varyasyonu yayımlamak üzere **Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="e6ab1-120">Geçerli canlı sayfayı saklamayı ve bir varyasyon yayımlamamayı tercih ederseniz, **Özgün sayfayı yeniden yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="e6ab1-121">Denemenizi silme</span><span class="sxs-lookup"><span data-stu-id="e6ab1-121">Delete your experiment</span></span>
<span data-ttu-id="e6ab1-122">Commerce'ta tamamlanmış bir denemeyi silmeniz gerekli olmasa da alan kazanmak veya çalışma alanınızı temizlemek için denemeyi silmeyi tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="e6ab1-123">Commerce site oluşturucuda deneme silmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6ab1-124">Sol gezinti bölmesinde **Denemeler**'i seçin ve ardından denemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="e6ab1-125">Deneme hala etkinse, devam etmeden önce üçüncü taraf hizmetinde denemeyi durdurun.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="e6ab1-126">Varyasyon içeriğini canlı siteden kaldırmak için komut çubuğunda **Yayımdan Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="e6ab1-127">Denemeyi silmek için **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e6ab1-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="e6ab1-128">Önceki adım</span><span class="sxs-lookup"><span data-stu-id="e6ab1-128">Previous step</span></span>
[<span data-ttu-id="e6ab1-129">Deneme çalıştırma ve izleme</span><span class="sxs-lookup"><span data-stu-id="e6ab1-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)

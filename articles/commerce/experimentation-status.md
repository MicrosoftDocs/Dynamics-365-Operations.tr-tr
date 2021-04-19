---
title: Denemenin durumunu inceleme
description: Bu konu, bir denemenin Dynamics 365 Commerce'teki deneme yaşam döngüsündeki hangi duruma sahip olduğunu açıklamaktadır.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f7bdd292893ee42d49bdf977a55d8b10896ca1cd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792451"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="60393-103">Denemenin durumunu inceleme</span><span class="sxs-lookup"><span data-stu-id="60393-103">Review the status of an experiment</span></span>
<span data-ttu-id="60393-104">Dynamics 365 Commerce'ta bir deneme ayarlama ve çalıştırmayla ilgili birçok adım bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="60393-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="60393-105">Deneme yalan döngüsü hakkında daha fazla bilgi için bkz. [Dynamics 365 Commerce'ta deneme](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="60393-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="60393-106">Bir denemenin yaşam döngüsü içinde nerede olduğunu öğrenmek için Commerce site oluşurucunun sol gezinme bölümündeki **Denemeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60393-106">To learn where an experiment is in the lifecycle, in Commerce site builder select **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="60393-107">Deneme oluşturmayı etkinleştirmek, varyasyonlar atamak ve verileri analiz etmek için kullanılan üçüncü taraf hizmetindeki ve Commerce'taki her bir denemenin durumunu içeren bir denemeler listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="60393-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="60393-108">**Commerce durumu** sütununda, aşağıdaki değerler görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="60393-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="60393-109">**Taslak** - Deneme Commerce içindeki bir sayfaya veya parçaya bağlı ve düzenleniyor.</span><span class="sxs-lookup"><span data-stu-id="60393-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="60393-110">**Yayımlandı** - Deneme varyasyonları web sitenizde görüntülenmeye hazır.</span><span class="sxs-lookup"><span data-stu-id="60393-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="60393-111">Deneme üçüncü taraf hizmetinde çalışıyorsa, web sitesi kullanıcıları sayfa veya parçanın üçüncü taraf hizmet tarafından seçilen bir varyasyonunu görür.</span><span class="sxs-lookup"><span data-stu-id="60393-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="60393-112">**Yayımdan kaldırıldı** - Deneme artık web sitenizde yok.</span><span class="sxs-lookup"><span data-stu-id="60393-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="60393-113">Deneme üçüncü taraf hizmetinde çalışıyorsa, web sitesi kullanıcıları sayfa veya parçanın üçüncü taraf hizmet tarafından seçilen bir varyasyonunu görür.</span><span class="sxs-lookup"><span data-stu-id="60393-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="60393-114">**Tamamlandı** - Deneme çalışmasını tamamladı ve bir varyasyon tüm web sitesi kullanıcıları için canlı siteye yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="60393-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="60393-115">Benzer şekilde, **üçüncü taraf durumu** sütununda, denemelerin üçüncü taraf hizmette bulunduğu durumu göstermek için aşağıdaki değerler görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="60393-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="60393-116">**Taslak** - Deneme üçüncü taraf hizmetinde ayarlandı ancak başlatılmadı.</span><span class="sxs-lookup"><span data-stu-id="60393-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="60393-117">**Çalışıyor** - Deneme üçüncü taraf hizmetinde başlatıldı ve veri topluyor.</span><span class="sxs-lookup"><span data-stu-id="60393-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="60393-118">**Duraklatıldı** - Deneme duraklatıldı, veri toplamıyor.</span><span class="sxs-lookup"><span data-stu-id="60393-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="60393-119">Yeniden veri toplaması için denemeyi sürdürmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="60393-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="60393-120">**Arşivlendi** - Deneme çalışmasını tamamladı ve sonraki başvurular için üçüncü taraf hizmette kataloğa alındı.</span><span class="sxs-lookup"><span data-stu-id="60393-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="60393-121">Aşağıdaki diyagramda her iki durum kümesi ve bunların birbirleriyle ilişkileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="60393-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="60393-122">[ ![Deneme durumları](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="60393-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
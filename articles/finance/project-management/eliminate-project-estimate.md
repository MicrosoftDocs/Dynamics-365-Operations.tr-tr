---
title: Proje tahminini eleme
description: Bu konu, tamamlandıktan sonra projenin tahmini kaldırılması hakkında bilgi sağlar.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410274"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="26092-103">Proje tahminini eleme</span><span class="sxs-lookup"><span data-stu-id="26092-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26092-104">Proje tahminleri, proje için tahmin edilen ve planlanan iş için mali görünüm sağlar.</span><span class="sxs-lookup"><span data-stu-id="26092-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="26092-105">Bir proje için tahminlerle tanışmak için, projeyi tahmin projesine eklemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="26092-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="26092-106">Tahmin projesi her zaman varolan bir projeye dayalıdır, ancak birden çok proje tek bir tahmin projesine başvuruda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="26092-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="26092-107">Yalnızca sabit fiyatlı ve yatırım projeleri tahmin projelerine bağlanabilir ve bu projeler tahmin kapsamındaki projeyle aynı proje grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="26092-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="26092-108">Tahmin kapsamındaki bir projeyi elemek için, bu projenin tamamlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="26092-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="26092-109">Aşağıdaki adımlarda bir tahmini nasıl ortadan kaldıracağınız açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="26092-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="26092-110">**Proje yönetimi ve muhasebe** > **Tüm projeler**'e gidin ve projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="26092-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="26092-111">**Yönet** sekmesinde **tahminler** 'i seçin ve **tahmin** sayfasında, **yok et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26092-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="26092-112">**Genel** sekmesindeki **tahmini kaldırma** sayfasında , aşağıdaki seçenekleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="26092-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="26092-113">**Dönem kodu**: Uygun tahmin projeleri seçmek için kullanılacak dönem kodunu belirleyin.</span><span class="sxs-lookup"><span data-stu-id="26092-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="26092-114">**Tahmin tarihi**: Eleme için uygun tahmin tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="26092-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="26092-115">**Süren iş uyarılarını kaldırın**: Süren iş (WIP) ile ilişkilendirilmiş bir tahmin elendiğinde bildirim sağlamak için bu seçeneği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="26092-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="26092-116">Bu seçenek etkin olmadığında, tahmin edilemeyen hareketler varsa eleme devam edemez.</span><span class="sxs-lookup"><span data-stu-id="26092-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="26092-117">Bu seçenek yalnızca tahmin projesine eleme uygulandığında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="26092-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="26092-118">Periyodik deftere nakilleri kullanıyorsanız bu kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="26092-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="26092-119">Bu ayar , **proje parametreleri** sayfasındaki **tahmin** sekmesinde yer alan ve **tahmin edilmemiş hareketlerin bulunduğu sırada eleme izni**olan ayarlar ile çalışır.</span><span class="sxs-lookup"><span data-stu-id="26092-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="26092-120">**Aşamayı tamamlandı olarak ayarla**: eliminasyon çalıştırıldıktan sonra tahmin projesinin aşamasını **tamamlandı** olarak ayarlamak için bu seçeneği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="26092-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="26092-121">**Tahmin listesini yazdır**: Tahmin proje listesi yazılacağı zaman dahil edilecek bilgileri seçin.</span><span class="sxs-lookup"><span data-stu-id="26092-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="26092-122">**Bilgi Günlüğünü Göster**: Bu seçeneğin bilgi günlüğünü görüntülemesi için etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="26092-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="26092-123">**Deftere nakil tarihi**: tahminin genel muhasebe deftere nakil tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="26092-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="26092-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="26092-124">Select **OK**.</span></span>
5. <span data-ttu-id="26092-125">Eliminasyon işlemi tamamlandıktan sonra, elenen tahmin projesi negatif bir değerle görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="26092-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="26092-126">Bir tahmini elemeyi düşünmüyorsanız, elenen tahmini seçin ve **eleme işlemini tersine çevir** 'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26092-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   

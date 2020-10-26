---
title: Varsayım tanımlama ve deneme için ölçümleri belirleme
description: Bu konuda, Dynamics 365 Commerce uygulamasında bir e-ticaret web sitesinde çalıştıracağınız denemeler için varsayım ve başarı ölçümlerinin nasıl belirleneceği açıklanır.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930306"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="b033e-103">Varsayım tanımlama ve deneme için başarı ölçümleri belirleme</span><span class="sxs-lookup"><span data-stu-id="b033e-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="b033e-104">Deneme yaşam döngüsünün ilk aşaması, deneme için varsayım tanımlamayı ve başarıyı değerlendirmek için izlenecek ölçümleri belirlemeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="b033e-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="b033e-105">Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde [deneme ayarlama ve çalıştırmayla](experimentation-overview.md) ilgili tüm adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b033e-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b033e-106">Ek adımlar ayrı konularda ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="b033e-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="b033e-107">[ ![Deneme kullanıcı yolculuğu - Tanımlama](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b033e-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="b033e-108">Varsayım, denemin sonucunu tahmin ettiğiniz bir ifadedir.</span><span class="sxs-lookup"><span data-stu-id="b033e-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="b033e-109">Varsayım tanımlaya rol alan birçok etken vardır: örneğin kullanıcı davranışı araştırması ve topladığınız web sitesi verileri.</span><span class="sxs-lookup"><span data-stu-id="b033e-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="b033e-110">Varsayımla, deneminiz ile doğrulamak istediğiniz varsayımı veya teoriyi tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="b033e-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="b033e-111">Denemeniz için bir varsayım örneği şu olabilir: "*giriş sayfamdaki beyaz bir tişört resmi, yaz aylarında lacivert bir kazaktan daha yüksek tıklama oranı oluşturur çünkü insanlar yazın hafif ve açık renkli kıyafetler giymek ister*"</span><span class="sxs-lookup"><span data-stu-id="b033e-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="b033e-112">Bu durumda, beyaz tişört ve lacivert kazak içeren varyasyonlar oluşturur ve her ikisini aynı anda yayımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="b033e-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="b033e-113">Bir varsayımını doğrulamak için, denemenin başarısı veya başarısızlığı doğrudan kullanıcı eylemlerine bağlı olmalıdır; örneğin, web sitesi kullanıcısının bir bağlantıya veya düğmeye tıklaması gibi.</span><span class="sxs-lookup"><span data-stu-id="b033e-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="b033e-114">Bu eylemlerin, denemeyi izleyen üçüncü taraf hizmetine bildirilecek olaylara karşılık gelmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b033e-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="b033e-115">Zaman içinde, eylem gerçekleştiren kullanıcıların yüzdesi raporlar oluşturmak ve çözümlemeler yapmak için kullanabileceğiniz bir ölçüm olarak hesaplanacaktır.</span><span class="sxs-lookup"><span data-stu-id="b033e-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="b033e-116">Kullanılabilir tüm olayları ve öznitelikleri incelemek için [Tanılama ve sorun giderme için Commerce bileşeni olayları](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="b033e-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="b033e-117">Önceki adım</span><span class="sxs-lookup"><span data-stu-id="b033e-117">Previous step</span></span>
[<span data-ttu-id="b033e-118">Dynamics 365 Commerce'ta deneme</span><span class="sxs-lookup"><span data-stu-id="b033e-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="b033e-119">Sonraki adım</span><span class="sxs-lookup"><span data-stu-id="b033e-119">Next step</span></span>
[<span data-ttu-id="b033e-120">Deneme ayarlama</span><span class="sxs-lookup"><span data-stu-id="b033e-120">Set up an experiment</span></span>](experimentation-setup.md)
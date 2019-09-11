---
title: Tahminler, iş emirleri ve projeler
description: Bu konu, Varlık yönetimindeki Proje yönetimi ve muhasebe modülüyle tahminler ve iş emri tümleştirmesini açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886828"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="66cf3-103">Tahminler, iş emirleri ve projeler</span><span class="sxs-lookup"><span data-stu-id="66cf3-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="66cf3-104">Varlık Yönetiminde, **Proje yönetimi ve muhasebe** modülüyle tümleştirme, kullanıcıların bakım işi türü tahminlerinde ve iş emri işlerinde maliyetleri izlemesine izin vererek maliyet kontrolünü en iyi duruma getirmek için yapılır.</span><span class="sxs-lookup"><span data-stu-id="66cf3-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="66cf3-105">Bakım işi türü tahminlerini izlemek için iki ayar yapılmalıdır:</span><span class="sxs-lookup"><span data-stu-id="66cf3-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="66cf3-106">**Varlık yönetimi** > **Kurulum** > **Varlık yönetimi parametreleri** > **Varlık** bağlantısı > **Proje** hızlı sekmesi > **Bakım tahmini projesi** alanında bir proje seçin.</span><span class="sxs-lookup"><span data-stu-id="66cf3-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="66cf3-107">**Bakım iş türü varsayılanlarında** bir bakım işi türü varsayılan satırı oluşturduğunuzda, satır için otomatik olarak bir faaliyet numarası oluşturulur (**Varlık yönetimi** > **Kurulum** > **İşler** > **Bakım işi türü varsayılanları**).</span><span class="sxs-lookup"><span data-stu-id="66cf3-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="66cf3-108">Bakım işi türü tahminleri iki amaca hizmet eder: **Proje yönetimi ve muhasebe** modülündeki bakım işi türü tahminlerindeki maliyetleri izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66cf3-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="66cf3-109">Ayrıca, bir iş emri işinde bir bakım işi türü seçtiğinizde, tahminler otomatik olarak bir iş emri iş projesine transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="66cf3-110">İş emri işlerinde maliyetleri izlemek için, önce iş emri projeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="66cf3-111">Yordamın açıklaması için [İş emri projesi kurulumu](../setup-for-work-orders/work-order-project-setup.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="66cf3-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="66cf3-112">İş emri işi projeleri</span><span class="sxs-lookup"><span data-stu-id="66cf3-112">Work order job projects</span></span>

<span data-ttu-id="66cf3-113">Bir iş emrinde iş emri işi oluşturduğunuzda iş emri projesi **Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumundaki** iş emirlerinin ana proje kurulumu tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="66cf3-114">İş emri işi projeleri, aşağıdaki iş emri bilgilerinin bir birleşimi kullanılarak oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="66cf3-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="66cf3-115">İş emrinde seçilen iş emri türü</span><span class="sxs-lookup"><span data-stu-id="66cf3-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="66cf3-116">İş emri işindeki varlıkla ilgili işlem yapılacak yerleşim</span><span class="sxs-lookup"><span data-stu-id="66cf3-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="66cf3-117">İş emri işindeki varlıkla ilgili varlık türü</span><span class="sxs-lookup"><span data-stu-id="66cf3-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="66cf3-118">İş emrinde ayarlanan Beklenen başlangıç ve bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="66cf3-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="66cf3-119">Yukarıda belirtilen bilgilerin tümünün bir iş emrinde bulunmaması mümkündür.</span><span class="sxs-lookup"><span data-stu-id="66cf3-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="66cf3-120">Bu nedenle, bir iş emri üst projesi için yapılan arama mevcut veri birleşimi kullanılarak ve iş emri verileriyle ilgili proje kodu seçilerek gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="66cf3-121">Örnek: Aşağıdaki şekilde, "Kamyon Motoru" varlık türünün kurulumu, bu varlık türüyle oluşturulan her iş emri işinin "000186" Proje kodunun bir alt projesi olacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![Şekil 1](media/01-integration-to-pma.png)

<span data-ttu-id="66cf3-123">İş emri işindeki proje kodunun ve ilgili faaliyet numarasının amacı **(Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm iş emirleri** > listeden iş emrini seçin > **Satır ayrıntıları** hızlı sekmesi > **Proje kodu** alanı ve **Faaliyet numarası** alanı), **Proje yönetimi ve muhasebe** modülünde iş emri işiyle ilgili maliyetleri ve iş emri işinde seçilen kıymetleri izlemektir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="66cf3-124">Aşağıdaki şekilde, iş emri projelerinin ve ilgili proje faaliyetlerinin grafik genel görünümünü görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="66cf3-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![Şekil 2](media/02-integration-to-pma.png)

<span data-ttu-id="66cf3-126">Bir iş emrinde yeni bir iş emri işi oluşturulduğunda, iş için otomatik olarak bir iş emri projesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="66cf3-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="66cf3-127">İş emri işiyle ilgili varlığın mali boyutları otomatik olarak iş emri projesine transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="66cf3-128">İş emri işi için oluşturulan proje faaliyeti bakım işi türü, bakım işi türü varyantı ve ticaret ile ilgili bilgiler ile ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="66cf3-129">Bu veriler örneğin bir iş emrinden bir satınalma siparişi oluşturursanız (bkz. [Tedarik](../work-orders/procurement.md)) veya zaman kaydı için **Proje yönetimi ve muhasebe** modülünü kullanıyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="66cf3-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="66cf3-130">Varlık işlem yapılacak bir yerleşime yüklenmişse ve bu varlık daha sonra başka bir işlem yapılacak yerleşime yüklenmişse, yeni işlem yapılacak yerleşimle ilgili mali boyutlar varlıkta otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="66cf3-131">Ardından, varlık için bir iş emri işi oluşturduğunuzda, iş emri işi için iş emri projesi artık varlıkla ilgili olan mali boyutları otomatik olarak alır.</span><span class="sxs-lookup"><span data-stu-id="66cf3-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="66cf3-132">Bu, işlem yapılacak yerleşimleri kullandığınızda, maliyetlerin herhangi bir zamanda yüklenmiş olduğu işlem yapılacak yerleşimlerde her zaman izlenebileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="66cf3-133">Mali boyutların otomatik güncelleştirilmesi, proje denetleme ve raporlama maliyetlerinin eksiksiz olarak izlenebilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="66cf3-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="66cf3-134">İş emri projeleri, iş emri yaşam döngüsü durumları, proje aşamaları ve proje türleri</span><span class="sxs-lookup"><span data-stu-id="66cf3-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="66cf3-135">İş emri yaşam döngüsü durumlarının ve iş emirlerindeki ilgili proje aşamalarının doğru kullanımını sağlamak için **Proje yönetimi ve muhaseb** modülüyle ilişkili olarak bağımlılıkları göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="66cf3-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="66cf3-136">**Proje yönetimi ve muhasebe** modülünde, proje aşamaları **Proje yönetimi ve muhasebe parametrelerindeki** proje türlerinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="66cf3-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="66cf3-137">**Proje yönetimi ve muhasebe parametrelerinde**, kullanacağınız tüm proje türleri için ilgili proje aşaması onay kutularını seçmeyi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="66cf3-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="66cf3-138">Aşağıdaki şekilde, "Zaman ve malzeme" ve "Dahili" proje türleri için beş aşama seçilmiştir: **Oluşturuldu** - **Tahmin edildi** - **Zamanlandı** - **İşlemde"** - **Tamamlandı**.</span><span class="sxs-lookup"><span data-stu-id="66cf3-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="66cf3-139">Bu beş aşama hem dahili bakım hem de servis bakım işleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="66cf3-140">**Varlık Yönetiminde** proje türleri **İş emri proje kurulumu** formu > **Proje grubu** bağlantısında ayarladığınız proje grupları tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="66cf3-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="66cf3-141">**İş emri proje kurulumunda** oluşturduğunuz iş emirleri iş emirleri oluştururken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="66cf3-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="66cf3-142">Bir iş emri oluşturulduğunda, iş emri için otomatik olarak bir iş emri projesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="66cf3-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="66cf3-143">İş emri yaşam döngüsü durumlarının her birinin ilgili proje aşaması olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="66cf3-144">Bir iş emri yaşam döngüsü durumuyla ilgili proje aşaması, iş emri projesinde tanımlanan proje grubu için etkin bir aşama olarak tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="66cf3-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="66cf3-145">İş emri projesi, bir iş emrinde otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="66cf3-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="66cf3-146">Yeni bir iş emri oluşturduğunuzda iş emri projesi otomatik tahsisatı **İş emri projesi kurulumundaki** (**Varlık yönetimi** > **Kurulum** > **İŞ emirleri** > **Proje kurulumu**) kurulumu temel alır.</span><span class="sxs-lookup"><span data-stu-id="66cf3-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="66cf3-147">İş emri proje grupları, ilgili proje türleri, proje aşamaları ve iş emri yaşam döngüsü durumları arasındaki ilişkilendirmeler aşağıdaki şekilde gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![Şekil 3](media/03-integration-to-pma.png)

![Şekil 4](media/04-integration-to-pma.png)

![Şekil 5](media/05-integration-to-pma.png)

<span data-ttu-id="66cf3-151">İş emri projelerinin nasıl ayarlanacağı ile ilgili olarak [İş emri proje kurulumu](../setup-for-work-orders/work-order-project-setup.md), iş emri yaşam döngüsü durumlarının nasıl oluşturulacağıyla ilgili olarak [İş emri yaşam döngüsü durumları](../setup-for-work-orders/work-order-lifecycle-states.md) konularına bakın.</span><span class="sxs-lookup"><span data-stu-id="66cf3-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="66cf3-152">Aşağıdaki şekil **Proje yönetimi ve muhasebe** modülüyle tümleştirmeye olanak tanımak için **Varlık Yönetimi** modülünde oluşturulan çeşitli projelerin grafik genel görünümünü ve projelerin ilgili olduğu iş süreçlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="66cf3-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![Şekil 6](media/06-integration-to-pma.png)


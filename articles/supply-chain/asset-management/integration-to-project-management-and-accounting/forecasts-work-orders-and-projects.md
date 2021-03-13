---
title: Tahminler, iş emirleri ve projeler
description: Bu konu, Varlık yönetimindeki Proje yönetimi ve muhasebe modülüyle tahminler ve iş emri tümleştirmesini açıklamaktadır.
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f062b5463b54e9bcf32ed6f17263811c4bb24138
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021048"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="9cab5-103">Tahminler, iş emirleri ve projeler</span><span class="sxs-lookup"><span data-stu-id="9cab5-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9cab5-104">Varlık Yönetiminde, **Proje yönetimi ve muhasebe** modülüyle tümleştirme, kullanıcıların bakım işi türü tahminlerinde ve iş emri işlerinde maliyetleri izleyebilmesine izin vererek maliyet kontrolünü en iyi duruma getirmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9cab5-104">In Asset Management, integration with the **Project management and accounting** module helps optimize cost control, so that users can track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="9cab5-105">Bakım işi türü tahminlerini izlemek için iki ayar gereklidir:</span><span class="sxs-lookup"><span data-stu-id="9cab5-105">Tracking of maintenance job type forecasts requires two settings:</span></span>

1. <span data-ttu-id="9cab5-106">**Varlık Yönetimi** > **Kurulum** > **Varlık yönetimi parametreleri**'nde bir proje seçin ve ardından **Varlıklar** sekmesinde > **Proje** hızlı sekmesinde bulunan **Bakım tahmini projesi** alanında bir proje seçin.</span><span class="sxs-lookup"><span data-stu-id="9cab5-106">Select a project in **Asset management** > **Setup** > **Asset management parameters**, and then, on the **Assets** tab > on the **Project** FastTab, in the **Maintenance forecast project** field, select a project.</span></span>

2. <span data-ttu-id="9cab5-107">**Bakım iş türü varsayılanları** sayfasında bir bakım işi türü varsayılan satırı oluşturduğunuzda, satır için otomatik olarak bir faaliyet numarası oluşturulur (**Varlık yönetimi** > **Kurulum** > **İşler** > **Bakım işi türü varsayılanları**).</span><span class="sxs-lookup"><span data-stu-id="9cab5-107">When you create a maintenance job type default line, an activity number is automatically created for the line on the **Maintenance job type defaults** page (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="9cab5-108">Bakım işi türü tahminleri iki amaca hizmet eder:</span><span class="sxs-lookup"><span data-stu-id="9cab5-108">Maintenance job type forecasts serve two purposes:</span></span> 

- <span data-ttu-id="9cab5-109">**Proje yönetimi ve muhasebe** modülündeki bakım işi türü tahminlerinde maliyetleri izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cab5-109">You can track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> 
- <span data-ttu-id="9cab5-110">Bir iş emri işinde bir bakım işi türü seçtiğinizde, tahminler otomatik olarak bir iş emri iş projesine transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-110">Forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="9cab5-111">İş emri işlerinde maliyetleri izlemek için, önce iş emri projeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-111">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="9cab5-112">Daha fazla bilgi için bkz. [İş emri proje kurulumu](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="9cab5-112">For more information, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="9cab5-113">İş emri işi projeleri</span><span class="sxs-lookup"><span data-stu-id="9cab5-113">Work order job projects</span></span>

<span data-ttu-id="9cab5-114">Bir iş emrinde iş emri işi oluşturduğunuzda, iş emri projesi **İş emri proje kurulumu** sayfasındaki iş emirlerinin ana proje kurulumu tarafından belirlenir (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumu**).</span><span class="sxs-lookup"><span data-stu-id="9cab5-114">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders on the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>

<span data-ttu-id="9cab5-115">İş emri işi projeleri, aşağıdaki iş emri bilgilerinin bir birleşimi kullanılarak oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="9cab5-115">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="9cab5-116">İş emrinde seçilen iş emri türü</span><span class="sxs-lookup"><span data-stu-id="9cab5-116">The work order type selected on the work order</span></span> 
- <span data-ttu-id="9cab5-117">İş emri işindeki varlıkla ilgili işlem yapılacak yerleşim</span><span class="sxs-lookup"><span data-stu-id="9cab5-117">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="9cab5-118">İş emri işindeki varlıkla ilgili olan varlık türü</span><span class="sxs-lookup"><span data-stu-id="9cab5-118">The asset type that is related to the asset on the work order job</span></span>  
- <span data-ttu-id="9cab5-119">İş emrinde ayarlanan beklenen başlangıç ve bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="9cab5-119">The expected start and end times that are set on the work order</span></span>  

<span data-ttu-id="9cab5-120">Bu bilgilerden bazıları bir iş emrinde bulunmayabilir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-120">Some of this information might not be found on a work order.</span></span> <span data-ttu-id="9cab5-121">Bu nedenle, bir iş emri üst projesi için yapılan arama mevcut veri birleşimi kullanılarak ve iş emri verileriyle ilgili proje kodu seçilerek gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-121">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds to work order data.</span></span>

<span data-ttu-id="9cab5-122">Örneğin, aşağıdaki örnekte, **Kamyon Motoru** varlık türünün ayarlanma şekli nedeniyle,  **Kamyon Motoru** varlık türü ile oluşturulan her iş emri işi 000186 proje kodunun alt projesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9cab5-122">For example, in the following illustration, because of the way that the **Truck Engine** asset type is set up, every work order job that is created with the **Truck Engine** asset type will be a sub-project of project ID 000186.</span></span>

![Şekil 1](media/01-integration-to-pma.png)

<span data-ttu-id="9cab5-124">İş emri işindeki proje kodunun ve ilgili faaliyet numarasının amacı, iş emri işiyle ilgili maliyetleri ve bunun üzerinde seçilen varlığı **Proje yönetimi ve muhasebe** modülünde izlemektir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-124">The purpose of the project ID on the work order job, and the related activity number, is to track costs that are related to the work order job, and the asset that is selected on it, in the **Project management and accounting** module.</span></span> <span data-ttu-id="9cab5-125">(Proje kodunu ve faaliyet numarasını görüntülemek için **Varlık yönetimi** > **Ortak** > **İş emirleri** > **Tüm iş emirleri** öğesini ve ardından iş emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="9cab5-125">(To view the project ID and activity number, select **Asset management** > **Common** > **Work orders** > **All work orders**, and then select the work order.</span></span> <span data-ttu-id="9cab5-126">**Satır ayrıntıları** hızlı sekmesinde, **Proje kodu** alanı proje kodunu ve **Faaliyet numarası** alanı faaliyet numarasını gösterir.) Varlık Yönetiminde maliyet kontrolü ile ilgili daha fazla bilgi için bkz. [Maliyet ve tarih kontrolü](../controlling-and-reporting/cost-and-date-control.md).</span><span class="sxs-lookup"><span data-stu-id="9cab5-126">On the **Line details** FastTab, the **Project ID** field shows the project ID, and the **Activity number** field shows the activity number.) For more information about cost control in Asset Management, see [Cost and date control](../controlling-and-reporting/cost-and-date-control.md).</span></span>

<span data-ttu-id="9cab5-127">Aşağıdaki örnekte, iş emri projelerinin ve ilgili proje faaliyetlerinin grafik genel görünümü gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-127">The following illustration shows a graphical overview of work order projects and related project activities.</span></span>

![Şekil 2](media/02-integration-to-pma.png)

<span data-ttu-id="9cab5-129">Bir iş emrinde yeni bir iş emri işi oluşturulduğunda, iş için otomatik olarak bir iş emri projesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cab5-129">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="9cab5-130">İş emri işiyle ilgili olan varlığın mali boyutları otomatik olarak iş emri projesine transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-130">The financial dimensions for the asset that is related to the work order job are automatically transferred to the work order project.</span></span>

<span data-ttu-id="9cab5-131">İş emri işinde oluşturulan proje faaliyetine ilgili bilgiler eklenir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-131">The project activity that is created for a work order job has related information attached to it.</span></span> <span data-ttu-id="9cab5-132">Bu bilgiler bakım işi türü, bakım iş türü varyantı ve zanaat ile ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-132">This information is about the maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="9cab5-133">Bunlar, örneğin bir iş emrinden bir satınalma siparişi oluşturursanız (bkz. [Tedarik](../work-orders/procurement.md)) veya zaman kaydı için **Proje yönetimi ve muhasebe** modülünü kullanıyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="9cab5-133">It's useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>

<span data-ttu-id="9cab5-134">Varlık işlem yapılacak bir yerleşime yüklenmişse ancak daha sonra başka bir işlem yapılacak yerleşime yüklenmişse, yeni işlem yapılacak yerleşimle ilgili mali boyutlar varlıkta otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-134">If the asset was installed on a functional location but is later installed on a different functional location, the financial dimensions that are related to the new functional location are automatically updated on the asset.</span></span> <span data-ttu-id="9cab5-135">Ardından, varlık için bir iş emri işi oluşturduğunuzda, iş emri işi için iş emri projesi artık varlıkla ilgili olan mali boyutları otomatik olarak alır.</span><span class="sxs-lookup"><span data-stu-id="9cab5-135">Then, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="9cab5-136">Bu nedenle, işlem yapılacak yerleşimleri kullandığınızda, maliyetler herhangi bir zamanda yüklenmiş olduğu işlem yapılacak yerleşimlerde her zaman izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-136">Therefore, when you use functional locations, costs can always be tracked on the functional locations that an asset was installed on at any given time.</span></span> <span data-ttu-id="9cab5-137">Mali boyutların otomatik güncelleştirilmesi, proje denetleme ve raporlama maliyetlerinin eksiksiz olarak izlenebilmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9cab5-137">The automatic update of financial dimensions helps guarantee complete traceability of costs for project control and reporting.</span></span>

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="9cab5-138">İş emri projeleri, iş emri yaşam döngüsü durumları, proje aşamaları ve proje türleri</span><span class="sxs-lookup"><span data-stu-id="9cab5-138">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="9cab5-139">İş emri yaşam döngüsü durumlarının ve iş emirlerindeki ilgili proje aşamalarının doğru şekilde kullanılmasını sağlamaya yardımcı olmak için **Proje yönetimi ve muhasebe** modülüyle ilişkili olarak bağımlılıkları göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="9cab5-139">To help guarantee that work order lifecycle states and related project stages on work orders are used correctly, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="9cab5-140">**Proje yönetimi ve muhasebe** modülünde, proje aşamaları **Proje yönetimi ve muhasebe parametreleri** sayfasındaki proje türlerinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9cab5-140">In the **Project management and accounting** module, project stages are set up on project types on the **Project management and accounting parameters** page.</span></span>  
- <span data-ttu-id="9cab5-141">**Proje yönetimi ve muhasebe parametrelerinde** sayfasında, kullanacağınız tüm proje türleri için ilgili proje aşamalarını seçmek için onay kutularını kullanın.</span><span class="sxs-lookup"><span data-stu-id="9cab5-141">On the **Project management and accounting parameters** page, use the check boxes to select relevant project stages for all the project types that you will use.</span></span> <span data-ttu-id="9cab5-142">Aşağıdaki örneklerde, **Zaman ve malzeme** ve **Dahili** proje türleri için beş aşama seçilmiştir: (**Oluşturuldu**, **Tahmin edildi**, **Zamanlandı**, **İşlemde** ve **Tamamlandı**).</span><span class="sxs-lookup"><span data-stu-id="9cab5-142">In the following illustrations, five stages (**Created**, **Estimated**, **Scheduled**, **In process**, and **Finished**) have been selected for the **Time and material** and **Internal** project types.</span></span> <span data-ttu-id="9cab5-143">Bu beş aşama hem dahili bakım işleri hem de servis bakım işleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-143">Those five stages are relevant to both internal maintenance jobs and service maintenance jobs.</span></span>
- <span data-ttu-id="9cab5-144">**Varlık Yönetimi** modülünde, proje türleri **İş emri proje kurulumu** sayfası > **Proje grubu** sekmesinde ayarlanan proje grupları tarafından tanımlanır (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumu**).</span><span class="sxs-lookup"><span data-stu-id="9cab5-144">In the **Asset Management** module, project types are defined by the project groups that you set up on the **Work order project setup** page > **Project group** tab (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  
- <span data-ttu-id="9cab5-145">**İş emri proje kurulumu** sayfasında ayarlanan proje grupları iş emirleri oluştururken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9cab5-145">The project groups that are set up on the **Work order project setup** page are used when you create work orders.</span></span> <span data-ttu-id="9cab5-146">Bir iş emri oluşturulduğunda, iş emri için otomatik olarak bir iş emri projesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cab5-146">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="9cab5-147">Her iş emri yaşam döngüsü durumunun ilgili proje aşaması olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-147">Every work order lifecycle state must have a related project stage.</span></span>  
- <span data-ttu-id="9cab5-148">Bir iş emri yaşam döngüsü durumuyla ilgili olan proje aşaması, iş emri projesinde tanımlanan proje grubu için etkin bir aşama olarak tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9cab5-148">The project stage that is related to a work order lifecycle state must be defined as an active stage for the project group that is defined in the work order project.</span></span> <span data-ttu-id="9cab5-149">İş emri projesi, bir iş emrinde otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cab5-149">The work order project is automatically created on a work order.</span></span>
- <span data-ttu-id="9cab5-150">Yeni bir iş emri oluşturduğunuzda, iş emri projesi otomatik tahsisatı **İş emri projesi kurulumu** sayfasındaki kurulumu temel alır.</span><span class="sxs-lookup"><span data-stu-id="9cab5-150">When you create a new work order, the automatic allocation of a work order project is based on the setup on the **Work order project setup** page.</span></span>  

<span data-ttu-id="9cab5-151">Aşağıdaki örnekte iş emri proje grupları, ilgili proje türleri, proje aşamaları ve iş emri yaşam döngüsü durumları arasındaki ilişkilendirmeler gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-151">The following illustrations show the associations between work order project groups, related project types, project stages, and work order lifecycle states.</span></span>

![Şekil 3](media/03-integration-to-pma.png)

![Şekil 4](media/04-integration-to-pma.png)

![Şekil 5](media/05-integration-to-pma.png)

<span data-ttu-id="9cab5-155">İş emri projelerini ayarlamayla ilgili bilgi için bkz. [İş emri proje kurulumu](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="9cab5-155">For information about how to set up work order projects, see [Work order project setup](../setup-for-work-orders/work-order-project-setup.md).</span></span> <span data-ttu-id="9cab5-156">İş emri yaşam döngüsü durumları oluşturma hakkında bilgi için bkz. [İş emri yaşam döngüsü durumları](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="9cab5-156">For information about how to create work order lifecycle states, see [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md).</span></span>

<span data-ttu-id="9cab5-157">Aşağıdaki örnekte **Varlık yönetimi** modülünde **Proje yönetimi ve muhasebe** modülüyle tümleştirmeyi etkinleştirmek için oluşturulan çeşitli projelere ilişkin grafik genel görünüm gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-157">The following illustration shows a graphical overview of the various projects that are created in the **Asset management** module to enable integration with the **Project management and accounting** module.</span></span> <span data-ttu-id="9cab5-158">Ayrıca, projelerin ilişkili olduğu iş süreçlerini de gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cab5-158">It also shows the work processes that the projects are related to.</span></span>

![Şekil 6](media/06-integration-to-pma.png)


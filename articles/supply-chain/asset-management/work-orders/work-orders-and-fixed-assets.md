---
title: İş emirleri ve sabit kıymetler
description: Bu konuda Kıymet Yönetimi'nde iş emirleri ve sabit kıymetler açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250842"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="4b44c-103">İş emirleri ve sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="4b44c-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="4b44c-104">Varlık Yönetiminde, varlıklar sabit kıymetlerle ilişkilendirilebilir ve bu varlıklar için iş emirleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b44c-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="4b44c-105">Bu işlevi kullanırsanız, **Proje yönetimi ve muhasebe** modülü ve **Sabit kıymetler** modülündeki sabit kıymetlerin, ilgili yatırım projelerinin ve yatırım projelerine kaydedilen maliyetlerin eksiksiz bir genel bakışını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b44c-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="4b44c-106">**Sabit kıymet numarası** alanı, yalnızca iş emri iş projesinde proje türü olarak "Yatırım" türü seçilirse iş emri iş projesinde doldurulur.</span><span class="sxs-lookup"><span data-stu-id="4b44c-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Şekil 1](media/24-work-orders.png)

<span data-ttu-id="4b44c-108">Aşağıdaki prosedürde varlıklar, iş emirleri, iş emri iş projeleri ve sabit kıymetler arasındaki ilişki açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4b44c-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="4b44c-109">Aşağıdaki şekilde gösterildiği gibi bir sabit kıymetle ilişkilendirmek üzere bir varlık oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b44c-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Şekil 2](media/25-work-orders.png)

2. <span data-ttu-id="4b44c-111">İş emri türlerini (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **İş emri türleri**) ayarladığınızda yatırımları işlemek için bir iş emri türü oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="4b44c-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="4b44c-112">Ayrıca bkz. [İş emri türleri](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="4b44c-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Şekil 3](media/26-work-orders.png)

3. <span data-ttu-id="4b44c-114">İş emri proje grupları (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumu** > **Proje grubu** bağlantısı) ayarladığınızda **Proje yönetimi ve muhasebe** modülünde (**Proje yönetimi ve muhasebe** > **Kurulum** > **Deftere nakil** > **Proje grupları**) yatırımlar için kullanılan iş emri türü ile yatırımlar için oluşturulan proje grubu arasında bir ilişki oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="4b44c-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Şekil 4](media/27-work-orders.png)

4. <span data-ttu-id="4b44c-116">Sabit kıymet nesnesiyle ilgili bir iş emri oluşturduğunuzda yatırımları işlemek için kullanılan iş emri türünü (örneğin "yatırım") seçin.</span><span class="sxs-lookup"><span data-stu-id="4b44c-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="4b44c-117">İş emri oluşturulduğunda ilgili iş emri türü **Tüm iş emirleri**'nde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4b44c-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Şekil 5](media/28-work-orders.png)

6. <span data-ttu-id="4b44c-119">İş emri oluşturulduğunda iş emriyle ilgili proje, **proje yönetimi ve muhasebe** > **Tüm projeler**'de oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b44c-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="4b44c-120">Projeyle ilgili bilgileri iş emrindeki **Proje kodu** bağlantısına tıklayarak görebilirsiniz (**Varlık yönetimi**'nde, iş emrini Ayrıntılar görünümünde açın > **Satır ayrıntıları** hızlı sekmesi > **Genel** sekmesi > **Proje kodu** alanı).</span><span class="sxs-lookup"><span data-stu-id="4b44c-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Şekil 6](media/29-work-orders.png)

7. <span data-ttu-id="4b44c-122">**Sabit kıymetler**'de, bir sabit kıymetle ilişkilendirilmiş projelerin genel bakışını görebilirsiniz (**Sabit kıymetler** > **Sabit kıymetler** > **Sabit kıymetler** > **Sabit kıymet sayısı** alanındaki sabit kıymete tıklayın > **İlgili bilgiler** bölmesi > **İlişkili projeler** bölümündeki içerikleri görüntüleyin).</span><span class="sxs-lookup"><span data-stu-id="4b44c-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>


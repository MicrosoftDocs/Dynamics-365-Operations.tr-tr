---
title: İş emirleri ve sabit kıymetler
description: Bu konuda Kıymet Yönetimi'nde iş emirleri ve sabit kıymetler açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4eadbdc452a5b7d28adfa0f102a9a727faad3c07
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016715"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="82b8b-103">İş emirleri ve sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="82b8b-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="82b8b-104">Varlık Yönetiminde, varlıklar sabit kıymetlerle ilişkilendirilebilir ve bu varlıklar için iş emirleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82b8b-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="82b8b-105">Bu işlevi kullanırsanız, Microsoft Dynamics 365 for Finance and Operations'da **Proje yönetimi ve muhasebe** ve **Sabit kıymetler** modüllerindeki sabit kıymetlerin, ilgili yatırım projelerinin ve yatırım projelerine kaydedilen maliyetlerin eksiksiz bir genel bakışını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82b8b-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="82b8b-106">**Sabit kıymet numarası** alanı, yalnızca iş emri işi projesinde proje türü olarak **Yatırım** türü ayarlanırsa iş emri iş projesinde doldurulur.</span><span class="sxs-lookup"><span data-stu-id="82b8b-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="82b8b-107">Aşağıdaki şekilde, **Proje yönetimi ve muhasebe** modülündeki bir yatırım projesi ile bir iş emri ili projesi arasındaki ilişki gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="82b8b-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Şekil 1](media/24-work-orders.png)

<span data-ttu-id="82b8b-109">Aşağıdaki prosedürde varlıklar, iş emirleri, iş emri iş projeleri ve sabit kıymetler arasındaki ilişki açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="82b8b-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="82b8b-110">Bir sabit kıymetle ilişkilendirdiğiniz bir varlık oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="82b8b-110">You create an asset that you relate to a fixed asset.</span></span>

![Şekil 2](media/25-work-orders.png)

2. <span data-ttu-id="82b8b-112">**İş emri türleri** sayfasında iş emri türlerini (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **İş emri türleri**) ayarladığınızda yatırımları işlemek için bir iş emri türü oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="82b8b-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="82b8b-113">Ayrıca bkz. [İş emri türleri](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="82b8b-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Şekil 3](media/26-work-orders.png)

3. <span data-ttu-id="82b8b-115">**İŞ emri proje kurulumu** sayfasının **Proje grubu** sekmesinde iş emri proje grupları (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Proje kurulumu**) ayarladığınızda **Proje yönetimi ve muhasebe** modülündeki **Proje grupları** sayfasında (**Proje yönetimi ve muhasebe** > **Kurulum** > **Deftere nakil** > **Proje grupları**) yatırımlar için kullanılan iş emri türü ile yatırımlar için oluşturulan proje grubu arasında bir ilişki oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="82b8b-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Şekil 4](media/27-work-orders.png)

4. <span data-ttu-id="82b8b-117">Sabit kıymetle ilgili bir iş emri oluşturduğunuzda yatırımları işlemek için kullanılan iş emri türünü (örneğin **Yatırım**) seçin.</span><span class="sxs-lookup"><span data-stu-id="82b8b-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="82b8b-118">İş emri oluşturulduğunda ilgili iş emri türü **Tüm iş emirleri** sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="82b8b-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Şekil 5](media/28-work-orders.png)

6. <span data-ttu-id="82b8b-120">İş emri oluşturulduğunda, iş emriyle ilişkili proje, **proje yönetimi ve muhasebe** modülündeki **Tüm projeler** sayfasında oluşturulur (**Proje yönetimi ve muhasebe** > **Projeler** > **Tüm projeler**).</span><span class="sxs-lookup"><span data-stu-id="82b8b-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="82b8b-121">Projeyle ilgili bilgileri görüntülemek için, **Varlık yönetimi** modülündeki **Tüm iş emirleri** sayfasının ayrıntılar görünümünde bulunan **Satır ayrıntıları** hızlı sekmesinin **Genel** sekmesindeki **Proje kodu** alanında yer alan bağlantıyı seçin (**Varlık yönetimi** > **Ortak** > **İŞ emirleri** > **Tüm iş emirleri**).</span><span class="sxs-lookup"><span data-stu-id="82b8b-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Şekil 6](media/29-work-orders.png)

7. <span data-ttu-id="82b8b-123">Bir sabit kıymetle ilişkili projelerin genel görünümünü görmek için **Sabit kıymetler** > **Sabit kıymetler** > **Sabit kıymetler**'i seçin ve **Sabit kıymet numarası** alanında, ayrıntılar görünümünü açmak için sabit kıymetin bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="82b8b-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="82b8b-124">Sayfanın sağ tarafındaki **İlgili bilgi** bölmesini genişletin ve **İlişkili projeler** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="82b8b-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>


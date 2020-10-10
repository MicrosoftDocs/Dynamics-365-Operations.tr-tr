---
title: Kıymet görünümü
description: Bu konuda Kıymet Yönetimi'ndeki kıymet görünümü açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc4cd9ada9c1f64b434cd657eb5f5654c1328ef4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888774"
---
# <a name="asset-view"></a><span data-ttu-id="8e3e7-103">Kıymet görünümü</span><span class="sxs-lookup"><span data-stu-id="8e3e7-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8e3e7-104">Bu konuda Kıymet Yönetimi'ndeki kıymet görünümü açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="8e3e7-105">**Kıymet görünümü** sayfası etkin kıymetleri ve işlem yapılacak yerleşimleri ağaç görünümünde gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="8e3e7-106">Bu nedenle kıymetin işlem yapılacak yerleşimlerle ilişkisine genel bakışı kolayca alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="8e3e7-107">Ayrıca işlem yapılacak yerleşimler, kıymetler ve ilgili ürün reçeteleri (BOM) hakkında ayrıntılı bilgileri de görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="8e3e7-108">Ayrıca kıymetle ilgili etkin bakım talepleri ve iş emirlerine hızlı bir genel bakış da alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="8e3e7-109">**Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Kıymet görünümü** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="8e3e7-110">Sayfada gösterilen görünümü değiştirmek için **Görünüm** alanından yeni bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e3e7-111">**Kıymet görünümü** sayfasını açtığınızda gösterilen varsayılan görünüm **Kıymet yönetimi parametreleri** sayfasının **Kıymetler** sekmesindeki **Görünüm** alanında (**Kıymet yönetimi** \> **Kurulum** \> **Kıymet yönetimi parametreleri**) seçili değere bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="8e3e7-112">Sayfanın sağ tarafında, hızlı sekme seçili görünümün ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="8e3e7-113">Ağaç görünümünün üst kısmında görünen içerik haritası izi ağaç görünümünde geçerli seçimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="8e3e7-114">Bu içerik haritası izi aşağıdaki biçimi kullanır:</span><span class="sxs-lookup"><span data-stu-id="8e3e7-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="8e3e7-115">İşlem yapılacak yerleşim kimliği / İşlem yapılacak yerleşim kimliği (birden fazla işlem yapılacak yerleşim varsa) \> Kıymet Kimliği / Kıymet Kimliği (birden fazla kıymet varsa) - Madde numarası.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="8e3e7-116">Ağaç görünümünde bir kıymet seçtiyseniz kıymetle ilgili bakım taleplerini veya iş emirlerini görüntülemek için **Etkin talepler** veya **Etkin iş emirleri** öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="8e3e7-117">Ayrıca ilgili görünümü açmak için **Aç** \> **İşlem yapılacak yerleşim**, **Kıymet** veya **Kıymet ürün reçetesi**'ni de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="8e3e7-118">**Görünüm** alanında seçebileceğiniz **Kıymet işlem yapılacak yerleşimleri** seçeneği bir kıymet seçebildiğiniz tüm kıymet aramalarında da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="8e3e7-119">Ağaç görünümü örneğin [kıymet oluşturduğunuz](../objects/create-an-object.md), bakım talebi oluşturduğunuz veya bir iş emri oluşturduğunuz **Kıymet görünümü** sekmesinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8e3e7-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>

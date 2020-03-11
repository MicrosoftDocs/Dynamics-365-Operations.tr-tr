---
title: Kaldırılan veya artık kullanılmayan Platform özellikleri
description: Bu konu, Finance and Operations uygulamalarının platofrm güncellemelerinde kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087895"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="284a9-103">Kaldırılan veya artık kullanılmayan Platform özellikleri</span><span class="sxs-lookup"><span data-stu-id="284a9-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="284a9-104">Bu konu, Finance and Operations uygulamalarının platofrm güncellemelerinde kaldırılmış veya kaldırılması planlanan özellikleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="284a9-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="284a9-105">*Kaldırılan* özellik artık üründe bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="284a9-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="284a9-106">*Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="284a9-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="284a9-107">Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="284a9-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="284a9-108">Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="284a9-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="284a9-109">Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="284a9-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="284a9-110">Platform güncelleştirmesi 32</span><span class="sxs-lookup"><span data-stu-id="284a9-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="284a9-111">İş akışı isteği değişikliği iletişim kutusu artık kullanıcı seçimi açılan listesini içermiyor</span><span class="sxs-lookup"><span data-stu-id="284a9-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="284a9-112">**Kullanımı sonlandırma/kaldırma nedeni**</span><span class="sxs-lookup"><span data-stu-id="284a9-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="284a9-113">Değişiklik isteği istenmeyen bir kullanıcıya gönderilebileceğinden bu bir güvenlik sorunudur.</span><span class="sxs-lookup"><span data-stu-id="284a9-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="284a9-114">Bu aynı zamanda bir kullanılabilirlik sorunudur ve kullanıcıyı iş akışının kaynağını belirlemeye ve bunları el ile seçmelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="284a9-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="284a9-115">**Başka bir özellikle mi değiştirildi?**</span><span class="sxs-lookup"><span data-stu-id="284a9-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="284a9-116">Hayır</span><span class="sxs-lookup"><span data-stu-id="284a9-116">No</span></span> |
| <span data-ttu-id="284a9-117">**Etkilenen ürün alanları**</span><span class="sxs-lookup"><span data-stu-id="284a9-117">**Product areas affected**</span></span>         | <span data-ttu-id="284a9-118">İş akışı</span><span class="sxs-lookup"><span data-stu-id="284a9-118">Workflow</span></span> |
| <span data-ttu-id="284a9-119">**Dağıtım seçeneği**</span><span class="sxs-lookup"><span data-stu-id="284a9-119">**Deployment option**</span></span>              | <span data-ttu-id="284a9-120">Tümü</span><span class="sxs-lookup"><span data-stu-id="284a9-120">All</span></span> |
| <span data-ttu-id="284a9-121">**Durum**</span><span class="sxs-lookup"><span data-stu-id="284a9-121">**Status**</span></span>                         | <span data-ttu-id="284a9-122">Kullanıcı seçimi açılan listesi, platform güncelleştirmesi 32 ' deki istek değişimi iletişim kutusundan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="284a9-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="284a9-123">İstek değişikliği istekleri oluşturana otomatik olarak istendiği gibi gönderilecek.</span><span class="sxs-lookup"><span data-stu-id="284a9-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="284a9-124">Bu işlevsellik hakkında daha fazla bilgi için bkz [İş akışı onay sürecindeki eylemler](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="284a9-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="284a9-125">Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular</span><span class="sxs-lookup"><span data-stu-id="284a9-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="284a9-126">Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../migration-upgrade/deprecated-features.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="284a9-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>


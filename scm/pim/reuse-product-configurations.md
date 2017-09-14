---
title: "Ürün yapılandırmalarını yeniden kullanma"
description: "Ürün için mevcut bir yapılandırmayı otomatik olarak yeniden kullanmak istediğinizi belirtebilirsiniz. Ardından bir kullanıcı bir yapılandırma oturumunu tamamladığında sistem, kullanıcının seçimiyle eşleşen bir yapılandırma olup olmadığını doğrular. Eşleşen bir yapılandırma bulunursa ürün reçetesine (BOM) karşılık gelen yapılandırma kodu ve rota yeniden kullanılır."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: b4d61c869577a3e18d1ac951f32dae286937a51c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2017

---

# <a name="reuse-product-configurations"></a><span data-ttu-id="405e5-105">Ürün yapılandırmalarını yeniden kullanma</span><span class="sxs-lookup"><span data-stu-id="405e5-105">Reuse product configurations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="405e5-106">Ürün için mevcut bir yapılandırmayı otomatik olarak yeniden kullanmak istediğinizi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="405e5-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="405e5-107">Ardından bir kullanıcı bir yapılandırma oturumunu tamamladığında sistem, kullanıcının seçimiyle eşleşen bir yapılandırma olup olmadığını doğrular.</span><span class="sxs-lookup"><span data-stu-id="405e5-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="405e5-108">Eşleşen bir yapılandırma bulunursa ürün reçetesine (BOM) karşılık gelen yapılandırma kodu ve rota yeniden kullanılır.</span><span class="sxs-lookup"><span data-stu-id="405e5-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="405e5-109">Yapılandırmaları yeniden kullanma gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="405e5-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="405e5-110">Yapılandırmaları yeniden kullanmayı etkinleştirmek için **Ürün yapılandırma modeli ayrıntıları**sayfasında bileşenler ve öznitelikler için aşağıdaki bilgileri belirtmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="405e5-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="405e5-111">**Bileşenler ve alt bileşenler**: **Genel** Hızlı sekmesinde **Konfigürasyonları yeniden kullan** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="405e5-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="405e5-112">**Öznitelikler**: **Öznitelikler** Hızlı Sekmesinde **Yeniden kullanıma dahil et** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="405e5-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="405e5-113">Bu seçenek yalnızca ilgili bileşen yeniden kullanım için etkinleştirildiğinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="405e5-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="405e5-114">Yeniden kullanım için hiçbir öznitelik seçmezseniz, bir yapılandırma oturumu sırasında kullanıcının seçimlerinden bağımsız olarak yapılandırma her zaman yeniden kullanılır.</span><span class="sxs-lookup"><span data-stu-id="405e5-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="405e5-115">Mevcut yapılandırmadaki öznitelik değerleri kullanıcının seçimleriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="405e5-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="405e5-116">Örneğin, bir yapılandırma oturumu sırasında kullanıcı renk olarak **Mavi** seçerse sistem bileşenin mevcut bir yapılandırmasında renk olarak mavinin bulunup bulunmadığını doğrular.</span><span class="sxs-lookup"><span data-stu-id="405e5-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="405e5-117">Yapılandırma yeniden kullanmayı sıfırlama</span><span class="sxs-lookup"><span data-stu-id="405e5-117">Resetting configuration reuse</span></span>
<span data-ttu-id="405e5-118">Yapılandırma yeniden kullanmayı sıfırladığınızda önceden oluşturduğunuz yapılandırmalar artık değerlendirilmez.</span><span class="sxs-lookup"><span data-stu-id="405e5-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="405e5-119">Ürün reçetesi veya rota değiştiğinde ancak ilgili öznitelikler değişmediğinde yapılandırma yeniden kullanmayı sıfırlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="405e5-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="405e5-120">Yapılandırma yeniden kullanmayı bileşen için **Genel** Hızlı Sekmesinde sıfırlarsınız.</span><span class="sxs-lookup"><span data-stu-id="405e5-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>





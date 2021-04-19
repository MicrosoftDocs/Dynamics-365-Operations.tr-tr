---
title: Seyahat durumu kurulumu
description: Bu konuda, kullanıcıların yolculuklara atayabilecekleri durum değerlerinin nasıl oluşturulabileceği açıklanmaktadır.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 80433c17ed9d790d88b20ecc253c8e4459ffea10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829800"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="c51eb-103">Seyahat durumu kurulumu</span><span class="sxs-lookup"><span data-stu-id="c51eb-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c51eb-104">**Seyahat durumları** sayfasında, kullanıcıların seyahatlere atayabileceği durum değerleri kümesini oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="c51eb-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="c51eb-105">Kullanıcılar bir seyahatin tüm seviyelerine seyahat durumu değerleri atayabilir: seyahat, sevkiyat konteyneri, folyo, satın alma siparişi ve madde (satın alma satırları ve transfer emri satırları).</span><span class="sxs-lookup"><span data-stu-id="c51eb-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="c51eb-106">İki amaç için kullanılırlar:</span><span class="sxs-lookup"><span data-stu-id="c51eb-106">They are used for two purposes:</span></span>

- <span data-ttu-id="c51eb-107">Kullanıcıyı seyahatin, sevkiyat konteynerinin, folyonun, satın alma siparişinin veya maddenin (satın alma satırları ve transfer emri satırları) durumu hakkında bilgilendirmek.</span><span class="sxs-lookup"><span data-stu-id="c51eb-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="c51eb-108">Değişikliği veya silmeyi önleyerek maliyet alanının kullanımını sınırlamak.</span><span class="sxs-lookup"><span data-stu-id="c51eb-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="c51eb-109">Seyahat durumlarınızı ayarlamak için **Varış yeri maliyeti \> Kurulum \> Seyahat durumları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c51eb-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="c51eb-110">Buradan, eylem bölmesindeki düğmeleri kullanarak durumları ekleyebilir, kaldırabilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c51eb-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="c51eb-111">Her maliyet alanının kendi seyahat durumları kümesi ve hiyerarşisi vardır.</span><span class="sxs-lookup"><span data-stu-id="c51eb-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="c51eb-112">Bu nedenle, **Seyahat durumları** sayfasında, **Maliyet alanı** alanında, önce görüntülemek veya seyahat durumları oluşturmak istediğiniz maliyet alanını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c51eb-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="c51eb-113">Ardından, her seyahat durumu için aşağıdaki tabloda açıklanan alanları gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c51eb-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="c51eb-114">Bir seyahatin durumunun, izleme denetim merkezi kullanılarak oluşturulan kurallar gibi sistem olayları tarafından da otomatik olarak değiştirilebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c51eb-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="c51eb-115">Alan</span><span class="sxs-lookup"><span data-stu-id="c51eb-115">Field</span></span> | <span data-ttu-id="c51eb-116">Tanım</span><span class="sxs-lookup"><span data-stu-id="c51eb-116">Description</span></span> |
|---|---|
| <span data-ttu-id="c51eb-117">Seyahat durumu</span><span class="sxs-lookup"><span data-stu-id="c51eb-117">Voyage status</span></span> | <span data-ttu-id="c51eb-118">Seyahat durumunun adını girin.</span><span class="sxs-lookup"><span data-stu-id="c51eb-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="c51eb-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="c51eb-119">Description</span></span> | <span data-ttu-id="c51eb-120">Seyahat durumunun bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="c51eb-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="c51eb-121">Değiştir</span><span class="sxs-lookup"><span data-stu-id="c51eb-121">Modify</span></span> | <span data-ttu-id="c51eb-122">Kullanıcıların bu durumdaki seyahatleri değiştirmesine izin veriliyorsa bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c51eb-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="c51eb-123">Delete</span><span class="sxs-lookup"><span data-stu-id="c51eb-123">Delete</span></span> | <span data-ttu-id="c51eb-124">Kullanıcıların bu durumdaki seyahatleri silmelerine izin veriliyorsa bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c51eb-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="c51eb-125">Zorunlu</span><span class="sxs-lookup"><span data-stu-id="c51eb-125">Mandatory</span></span> | <span data-ttu-id="c51eb-126">Seyahat durumunun atlanmaması amacıyla seyahat durumunu zorunlu hale getirmek için bu onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c51eb-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="c51eb-127">Üst öğe</span><span class="sxs-lookup"><span data-stu-id="c51eb-127">Parent</span></span> | <span data-ttu-id="c51eb-128">Durum değerleri arasında bir hiyerarşi oluşturmak için bu alanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="c51eb-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="c51eb-129">Seyahat durumları hiyerarşide üst durumlardan alt durumlara doğru yalnızca aşağı yönde değiştirilebilir (el ile veya otomatik olarak).</span><span class="sxs-lookup"><span data-stu-id="c51eb-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="c51eb-130">Yalnızca kuruluşunuzun kullandığı belirli seyahat durumlarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c51eb-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="c51eb-131">Tipik seyahat durumları arasında *Onaylandı*, *Taşımadaki Mallar*, *Teslim Alındı*, *Maliyetlendirilme için hazır* ve *Maliyetlendirildi* değerleri bulunur.</span><span class="sxs-lookup"><span data-stu-id="c51eb-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="c51eb-132">Ancak başka durumlar da olabilir.</span><span class="sxs-lookup"><span data-stu-id="c51eb-132">However, other statuses might be present.</span></span>

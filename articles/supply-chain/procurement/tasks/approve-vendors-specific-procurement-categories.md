---
title: Belirli tedarik kategorileri için satıcıları onaylama
description: Satınalma talebi oluşturulduğunda satınalma ilkelerinin nasıl ayarlandığına bağlı olarak onaylanan veya tercih edilen bir satıcıyı seçmek gerekebilir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eec50e2e8f08fabb64f89c17159b97ba770026f8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836356"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="4761f-103">Belirli tedarik kategorileri için satıcıları onaylama</span><span class="sxs-lookup"><span data-stu-id="4761f-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4761f-104">Satınalma talebi oluşturulduğunda satınalma ilkelerinin nasıl ayarlandığına bağlı olarak onaylanan veya tercih edilen bir satıcıyı seçmek gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="4761f-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="4761f-105">Bu prosedür belirli bir tedarik kategorisi için bir satıcının onaylanan veya tercih edilen olduğunu nasıl belirleyeceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="4761f-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="4761f-106">Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4761f-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="4761f-107">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4761f-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="4761f-108">Tedarik ve kaynak > Satıcılar > Tüm satıcılar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4761f-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="4761f-109">Bir kategori için onaylanan veya tercih edilen satıcı olarak ayarlamak istediğiniz satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="4761f-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="4761f-110">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4761f-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="4761f-111">Kategoriler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4761f-111">Click Categories.</span></span>
5. <span data-ttu-id="4761f-112">Kategori ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4761f-112">Click Add category.</span></span>
6. <span data-ttu-id="4761f-113">Kategori alanından OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4761f-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="4761f-114">Satıcı kategorisi durumu alanından 'Tercih edilen'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4761f-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="4761f-115">Bir kategori için birden fazla tercih edilen satıcı belirlemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="4761f-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="4761f-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4761f-116">Click Save.</span></span>
9. <span data-ttu-id="4761f-117">Tedarik ve kaynak > Tedarik kategorileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4761f-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="4761f-118">Ağaçtan, 'CCORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4761f-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="4761f-119">Satıcılar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="4761f-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="4761f-120">Seçtiğiniz satıcı Ofis ve masa aksesuarları kategorisi için tercih edilen satıcı olarak görünüyorsa işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4761f-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="4761f-121">Bu prosedürü görev kılavuzu olarak çalıştırıyorsanız satıcılar listesine inebilmek için Kilidi aç düğmesine tıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4761f-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="4761f-122">Tercih edilen ve onaylanan satıcıları bu sayfada eklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="4761f-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="4761f-123">Ağaçtan, 'OFFICE AND DESK ACCESSORIES'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="4761f-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="4761f-124">Ağaçtan 'Makaslar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4761f-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="4761f-125">Ana kategoriden satıcıları devral: alanından Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4761f-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="4761f-126">Ana kategoriden satıcıları devral: alanından Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4761f-126">Select Yes in the Inherit vendors from parent category: field.</span></span>


---
title: Belirli tedarik kategorileri için satıcıları onaylama
description: Bu konu, Dynamics 365 Supply Chain Management'ta belirli tedarik kategorileri için satıcıların nasıl onaylanacağını açıklamaktadır.
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439243"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="2b1e3-103">Belirli tedarik kategorileri için satıcıları onaylama</span><span class="sxs-lookup"><span data-stu-id="2b1e3-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b1e3-104">Bu konu, Dynamics 365 Supply Chain Management'ta belirli tedarik kategorileri için satıcıların nasıl onaylanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2b1e3-105">Satınalma talebi oluşturulduğunda satınalma ilkelerinin nasıl ayarlandığına bağlı olarak onaylanan veya tercih edilen bir satıcıyı seçmek gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="2b1e3-106">Bu prosedür belirli bir tedarik kategorisi için bir satıcının onaylanan veya tercih edilen olduğunu nasıl belirleyeceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="2b1e3-107">Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="2b1e3-108">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="2b1e3-109">Gezinti Bölmesi'nde **Modüller > Tedarik ve kaynak atama > Satıcılar > Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="2b1e3-110">Bir kategori için onaylanan veya tercih edilen satıcı olarak ayarlamak istediğiniz satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="2b1e3-111">Eylem Bölmesinde, **Genel**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="2b1e3-112">**Kategoriler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-112">Select **Categories**.</span></span>
5. <span data-ttu-id="2b1e3-113">**Kategori ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-113">Select **Add category**.</span></span>
6. <span data-ttu-id="2b1e3-114">**Kategori** alanından **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="2b1e3-115">**Satıcı kategorisi durumu** alanından **Tercih edilen**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="2b1e3-116">Bir kategori için birden fazla tercih edilen satıcı belirlemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="2b1e3-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-117">Select **Save**.</span></span>
9. <span data-ttu-id="2b1e3-118">Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Tedarik kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="2b1e3-119">Ağaçtan, **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="2b1e3-120">**Satıcılar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="2b1e3-121">Seçtiğiniz satıcı Ofis ve masa aksesuarları kategorisi için tercih edilen satıcı olarak görünüyorsa işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="2b1e3-122">Bu prosedürü görev kılavuzu olarak çalıştırıyorsanız satıcılar listesine inebilmek için **Kilidi aç** düğmesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="2b1e3-123">Tercih edilen ve onaylanan satıcıları bu sayfada eklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="2b1e3-124">Ağaçta **OFFICE AND DESK ACCESSORIES**'i genişletin ve **Makaslar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="2b1e3-125">**Ana kategoriden satıcıları devral:** alanından **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="2b1e3-126">**Ana kategoriden satıcıları devral:** alanından **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2b1e3-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>


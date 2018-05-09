--- 
title: "Bir satıcı hesabı oluşturma"
description: "Bu yordam, bir satıcı hesabı oluşturmayı ve adres ve kişi bilgileri eklemeyi göstermektedir."
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: aaa5b503af95883c2c7fdfb2ad7f3e3062d28961
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-vendor-account"></a><span data-ttu-id="95c0f-103">Bir satıcı hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="95c0f-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95c0f-104">Bu yordam, bir satıcı hesabı oluşturmayı ve adres ve kişi bilgileri eklemeyi göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="95c0f-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="95c0f-105">Bu yordam satınalma ve finansal amaçlar için olan tüm alanları doldurmayı göstermez.</span><span class="sxs-lookup"><span data-stu-id="95c0f-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="95c0f-106">Bu alanlar hakkında daha fazla bilgi için lütfen alan açıklamalarını okuyun.</span><span class="sxs-lookup"><span data-stu-id="95c0f-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="95c0f-107">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95c0f-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="95c0f-108">Satıcı hesapları genellikle bir satınalma profesyoneli veya alacak hesapları personeli tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="95c0f-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="95c0f-109">Bir satıcı hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="95c0f-109">Create a vendor account</span></span>
1. <span data-ttu-id="95c0f-110">Tedarik ve kaynak > Satıcılar > Tüm satıcılar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="95c0f-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-111">Click New.</span></span>
3. <span data-ttu-id="95c0f-112">Satıcı hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="95c0f-113">Değer otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="95c0f-113">The value may be populated automatically.</span></span> <span data-ttu-id="95c0f-114">Bu durumda, bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95c0f-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="95c0f-115">Bir kişi veya kuruluş için satıcı hesapları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95c0f-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="95c0f-116">Bu, hangi alanların kullanılabileceğini etkiler.</span><span class="sxs-lookup"><span data-stu-id="95c0f-116">This will affect which fields are available.</span></span> <span data-ttu-id="95c0f-117">Bu örnekte, bir organizasyon için bir satıcı hesabı oluşturacağız.</span><span class="sxs-lookup"><span data-stu-id="95c0f-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="95c0f-118">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="95c0f-119">Satıcı ise bir zaten sisteminizde kayıtlı bir tarafsa, açılan aşağı menüyü kullanarak satıcıyı bu alanda seçerseniz, yeni bir satıcı hesabı zaten kayıtlı adres ve ilgili kişi bilgilerini devralır.</span><span class="sxs-lookup"><span data-stu-id="95c0f-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="95c0f-120">Grup alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="95c0f-121">Satıcı grubu aşağıdaki parametrelerden herhangi birine ortak olarak sahip olan satıcıları gruplandırmak için kullanılır: Ödeme koşulları, kapatma dönemi, satış vergisi grubu da dahil olmak üzere genel muhasebe hesapları, stok defterine nakil grupları; varsayılan genel muhasebe hesapları; ürün kodlarını filtre ve tahmin yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="95c0f-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="95c0f-122">Personel sayısı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="95c0f-123">Organizasyon numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="95c0f-124">Bir adres ekleyin</span><span class="sxs-lookup"><span data-stu-id="95c0f-124">Add an address</span></span>
1. <span data-ttu-id="95c0f-125">Adresler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="95c0f-126">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-126">Click Add.</span></span>
3. <span data-ttu-id="95c0f-127">Amaç alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="95c0f-128">Bir veya daha fazla sayıda amaç seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95c0f-128">You can select one or more purposes.</span></span> <span data-ttu-id="95c0f-129">Bunlar belirli bir amaç için doğru adresin seçilmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="95c0f-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="95c0f-130">Örneğin, amaç “Fatura” ise, faturalar gönderilirken bu adres kullanılır.</span><span class="sxs-lookup"><span data-stu-id="95c0f-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="95c0f-131">Ad veya açıklama alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="95c0f-132">Ülke/bölge alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="95c0f-133">Adresi ayrıntılarını girin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-133">Enter the address details.</span></span> <span data-ttu-id="95c0f-134">Seçtiğiniz ülke/bölge, ülke/bölge adres biçimine karşılık gelerek size sunulacak olan alanları belirleyecektir.</span><span class="sxs-lookup"><span data-stu-id="95c0f-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="95c0f-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="95c0f-136">İletişim bilgileri ekleyin</span><span class="sxs-lookup"><span data-stu-id="95c0f-136">Add contact information</span></span>
1. <span data-ttu-id="95c0f-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-137">Click Add.</span></span>
2. <span data-ttu-id="95c0f-138">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="95c0f-139">Tür alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="95c0f-140">İletişim numarası/adresi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="95c0f-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="95c0f-141">Birincil ilgili kişi ise, Birincil onay kutusunu işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95c0f-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="95c0f-142">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-142">Click Save.</span></span>
6. <span data-ttu-id="95c0f-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-143">Close the page.</span></span>
7. <span data-ttu-id="95c0f-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="95c0f-144">Close the page.</span></span>



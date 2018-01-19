---
title: "Bir departman yaratın ve onu departman hiyerarşisiyle ilişkilendirin."
description: "Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir. Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur. İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz. Departmanların kâr ve zarar sorumluluğu olabilir."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 8da8f726e8192c208c1cf51595c96f47d6213d7a
ms.contentlocale: tr-tr
ms.lasthandoff: 01/19/2018

---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a><span data-ttu-id="51447-106">Bir departman yaratın ve onu departman hiyerarşisiyle ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="51447-106">Create a department and associate it with the department hierarchy</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="51447-107">Bir bölüm bir kuruluşun bir kategori veya işlevsel alanını temsil eden işletme bir birimdir.</span><span class="sxs-lookup"><span data-stu-id="51447-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="51447-108">Departman satış, muhasebe veya İnsan kaynakları gibi kuruluşun belirli bir alanından sorumludur.</span><span class="sxs-lookup"><span data-stu-id="51447-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="51447-109">İşlevsel alanlara bildirmek için bölümleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51447-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="51447-110">Departmanların kâr ve zarar sorumluluğu olabilir.</span><span class="sxs-lookup"><span data-stu-id="51447-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="51447-111">Bir departman maliyet merkezleri grubu da içerebilir.</span><span class="sxs-lookup"><span data-stu-id="51447-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="51447-112">Departmanlar için pozisyonlar atanabilir.</span><span class="sxs-lookup"><span data-stu-id="51447-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="51447-113">Bir bölüm oluşturmak için **İnsan Kaynakları** &gt; **Departmanlar** &gt; **Departmanlar** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="51447-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="51447-114">Aşağıdaki tabloda, kullanılabilecek alanlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="51447-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="51447-115">Alan</span><span class="sxs-lookup"><span data-stu-id="51447-115">Field</span></span>               | <span data-ttu-id="51447-116">Açıklama</span><span class="sxs-lookup"><span data-stu-id="51447-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51447-117">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="51447-117">Name</span></span>                | <span data-ttu-id="51447-118">Departman için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="51447-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="51447-119">Departman numarası</span><span class="sxs-lookup"><span data-stu-id="51447-119">Department number</span></span>   | <span data-ttu-id="51447-120">**Numara serileri** sayfasında **kuruluş numarası**'na bir numara serisi kodu atadıysanız varsayılan değer otomatik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="51447-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="51447-121">Arama adı</span><span class="sxs-lookup"><span data-stu-id="51447-121">Search name</span></span>         | <span data-ttu-id="51447-122">Departman için aramada kullanılabilecek bir ad veya kısa ad girin.</span><span class="sxs-lookup"><span data-stu-id="51447-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="51447-123">Not</span><span class="sxs-lookup"><span data-stu-id="51447-123">Memo</span></span>                | <span data-ttu-id="51447-124">Buraya ek bilgi girin</span><span class="sxs-lookup"><span data-stu-id="51447-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="51447-125">Hiyerarşide</span><span class="sxs-lookup"><span data-stu-id="51447-125">In hierarchy</span></span>        | <span data-ttu-id="51447-126">Seçili bir onay kutusu, departman hiyerarşisine bir departman dahil edildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="51447-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="51447-127">Bir bölümü bölüm hiyerarşisine ekleme hakkında daha fazla bilgi için bu makalenin ilerisindeki bilgilere bakın.</span><span class="sxs-lookup"><span data-stu-id="51447-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="51447-128">DUNS numarası</span><span class="sxs-lookup"><span data-stu-id="51447-128">DUNS number</span></span>         | <span data-ttu-id="51447-129">DUNS Veri Evrensel Sayı Sistemi anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="51447-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="51447-130">Bu, Dun & Bradstreet tarafından verilen bir dokuz basamaklı bir sayıdır.</span><span class="sxs-lookup"><span data-stu-id="51447-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="51447-131">Yönetici</span><span class="sxs-lookup"><span data-stu-id="51447-131">Manager</span></span>             | <span data-ttu-id="51447-132">Departmanı yöneten kişiyi girin.</span><span class="sxs-lookup"><span data-stu-id="51447-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="51447-133">Adresler</span><span class="sxs-lookup"><span data-stu-id="51447-133">Addresses</span></span>           | <span data-ttu-id="51447-134">Departman için adres bilgilerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="51447-134">Add the address information for the department.</span></span> <span data-ttu-id="51447-135">Örneğin, departmanın bulunduğunu bina için posta adresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="51447-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="51447-136">İletişim bilgileri</span><span class="sxs-lookup"><span data-stu-id="51447-136">Contact information</span></span> | <span data-ttu-id="51447-137">Departman için ilgili kişi verilerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="51447-137">Add contact information for the department.</span></span> <span data-ttu-id="51447-138">Örneğin, departmanda hizmet masası için bir telefon numarası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="51447-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="51447-139">Bölüm hiyerarşisine bir bölüm eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="51447-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="51447-140">**İnsan Kaynakları** &gt; **Departmanlar** &gt; **Departman hiyerarşisi**'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="51447-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="51447-141">**Düzenle**'yi tıklatın ve departmanın altında olması gereken kuruluş seçin.</span><span class="sxs-lookup"><span data-stu-id="51447-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="51447-142">**Ekle**'yi seçin ve listede **Departman**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="51447-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="51447-143">Görüntülenen departman listesinde hiyerarşiye eklemek için departmanı seçin.</span><span class="sxs-lookup"><span data-stu-id="51447-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="51447-144">Değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="51447-144">Save your changes.</span></span> <span data-ttu-id="51447-145">Hiyerarşi taslak sürümünü oluşturulduğuna dair bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="51447-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="51447-146">Hazır olduğunuzda, hiyerarşisi tasarımcısı içerisinde **Yayımla**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="51447-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="51447-147">Hiyerarşinin ne zaman yayımlanacağını belirtecek bir geçerlilik tarihi girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51447-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="51447-148">Örneğin, bir sonraki takvim yılı başına yeni bir departman eklemek için yürürlük tarihini yeni takvim yılının 1 Ocak'ı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="51447-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="51447-149">Hiyerarşi değişiklikleri o tarihte geçerlilik kazanır.</span><span class="sxs-lookup"><span data-stu-id="51447-149">The changes to the hierarchy will take effect on that date.</span></span>






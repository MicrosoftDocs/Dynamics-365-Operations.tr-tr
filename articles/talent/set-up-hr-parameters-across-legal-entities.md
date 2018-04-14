---
title: "Tüzel kişilikler arasında İK parametreleri ayarlama"
description: "Konum kayıtları gibi şirketler arasında paylaşılan kayıtlar için paylaşılan parametreleri ayarlamanız gerekir. Bu makalede, tüzel kişilikler arasında İnsan kaynakları parametrelerinin nasıl ayarlandığı açıklanmaktadır."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2e73441a3f4190561d1d16db40ee1581267c8dfb
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="678b4-104">Tüzel kişilikler arasında İK parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="678b4-104">Set up HR parameters across legal entities</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="678b4-105">Konum kayıtları gibi şirketler arasında paylaşılan kayıtlar için paylaşılan parametreleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="678b4-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="678b4-106">Bu makalede, tüzel kişilikler arasında İnsan kaynakları parametrelerinin nasıl ayarlandığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="678b4-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="678b4-107">Bazı kayıt türleri konum kayıtları gibi şirketler arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="678b4-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="678b4-108">Bu kayıtlar için paylaşılan parametreleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="678b4-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="678b4-109">Örneğin, **İnsan Kaynakları parametreleri paylaşılan** sayfasını tüzel kişilikler arasında İnsan Kaynakları parametreleri ayarlamak için kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="678b4-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="678b4-110">**İnsan Kaynakları paylaşılan parametreleri** sayfasında, parametreler kendi işlevselliğine dayalı alanlar halinde gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="678b4-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="678b4-111">Daha önce yayımlanan işlev</span><span class="sxs-lookup"><span data-stu-id="678b4-111">Previously released functionality</span></span>
<span data-ttu-id="678b4-112">**kimlik** sekmesinde sayfada listelenen kimlik numaralarını temsil eden kimlik türleri seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="678b4-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="678b4-113">Çalışanlar için kimlik bilgilerini girmeden önce kimlik tiplerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="678b4-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="678b4-114">Sosyal Güvenlik numarası, Ulusal kimlik numarası, yabancı kimlik numarası ve kişisel kimlik kodu hakkında bilgiler **kimlik türü** sayfasında saklanır.</span><span class="sxs-lookup"><span data-stu-id="678b4-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="678b4-115">Yeni bir kimlik türü tanımlamak veya mevcut türlerin listesini gözden geçirmek için **Personel yönetimi** &gt; **Bağlantılar sekmesi** &gt; **Kurulum** &gt; **Kimlik türleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="678b4-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="678b4-116">Basit bir kod ve açıklama girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="678b4-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="678b4-117">Dynamics 365 for Talent kullanıyorsanız</span><span class="sxs-lookup"><span data-stu-id="678b4-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="678b4-118">**kimlik** sekmesinde sayfada listelenen kimlik numaralarını temsil eden kimlik türleri seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="678b4-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="678b4-119">Çalışanlar için kimlik bilgilerini girmeden önce kimlik tiplerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="678b4-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="678b4-120">Sosyal Güvenlik numarası, Ulusal kimlik numarası, yabancı kimlik numarası ve kişisel kimlik kodu hakkında bilgiler **kimlik türü** sayfasında saklanır.</span><span class="sxs-lookup"><span data-stu-id="678b4-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="678b4-121">Yeni bir kimlik türü tanımlamak veya mevcut türlerin listesini gözden geçirmek için **İnsan Kaynakları** &gt; **Kurulum** &gt; **Kimlik türleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="678b4-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="678b4-122">Basit bir kod ve açıklama girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="678b4-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="678b4-123">**Numara sıraları** sekmesinde, aşağıdaki kayıtlar için kullanılan numara serilerini seçebilirsiniz: Personel numarası, pozisyon, kullanıcı isteği kimliği, I-9 belgesi, başvuran, tartışma, yararı kimliği ve personel eylem (Bu kayıt türü etkinleştirilmişse).</span><span class="sxs-lookup"><span data-stu-id="678b4-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="678b4-124">Numara serisi referanslarını ve kodlarını tanımlamak için **Numara serisi** listesi sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="678b4-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="678b4-125">Bu sayfayı bulmak için sayfa arama özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="678b4-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="678b4-126">**pozisyonlar** sekmesinde, varsayılan olarak atama için kullanılabilir olan yeni pozisyonlar olup olmadığını gösterin:</span><span class="sxs-lookup"><span data-stu-id="678b4-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="678b4-127">**Her zaman** – Pozisyonlar oluşturulurken çalışanları yeni pozisyonlara atayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="678b4-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="678b4-128">Pozisyonlar oluşturulurken, **Pozisyon** sayfasının **Genel** sekmesindeki **Atama için kullanılabilir** tarih ve saat, oluşturma tarihi ve saatine otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="678b4-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="678b4-129">**Hiçbir zaman** – pozisyonlar oluşturduğunuzda yeni konumlara çalışanları atayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="678b4-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="678b4-130">Bu seçeneği belirlerseniz, her yeni pozisyon için kullanılabilir duruma geldiğinde **konumu** sayfasını açmanız ve daha sonra **genel** sekmesinde, çalışan atamasını etkinleştirmek için **atama için kullanılabilir** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="678b4-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="678b4-131">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="678b4-131">See also</span></span>
--------

[<span data-ttu-id="678b4-132">Şirkete özgü İK parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="678b4-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)





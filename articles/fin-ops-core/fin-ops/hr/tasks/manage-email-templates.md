---
title: E-posta şablonlarını yönetme
description: Bu konu, e-posta şablonlarının nasıl yönetileceğini açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a911fea9e7d1009160a021e53533c0ce49efbfe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143708"
---
# <a name="manage-email-templates"></a><span data-ttu-id="18e12-103">E-posta şablonlarını yönetme</span><span class="sxs-lookup"><span data-stu-id="18e12-103">Manage email templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18e12-104">Yeni bir belgeye kuruluşunuzun bilgilerini vertabanından transfer edebilirve bunu başvuranlarla ve adaylarla etkili iletişim kurmak için şablonlarda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18e12-104">You can transfer information from your organization's database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="18e12-105">Bunu yapmak için sistem verilerinin ekleneceği standart metin ve yer işaretleri içeren bir şablon oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18e12-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="18e12-106">Örneğin, bir başvuran için adres ve iletişim bilgilerini içeren, söz konusu başvuranla iletişim kurarken kullanabileceğiniz bir Microsoft Word belgesine ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18e12-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="18e12-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="18e12-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="18e12-108">E-posta şablonlarınızda kullanmak istediğiniz yer işaretlerini seçin</span><span class="sxs-lookup"><span data-stu-id="18e12-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="18e12-109">Gezinti bölmesinde **Modüller > İnsan Kaynakları > İşe alma > İletişim > Başvuru yer işaretleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="18e12-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="18e12-110">Listede, istenen yazışma eylemini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="18e12-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="18e12-111">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="18e12-111">Select **Edit**.</span></span>
4. <span data-ttu-id="18e12-112">Seçili Yazışma eylemi için bir e-posta şablonu kullanın ve yer işareti alanları taşımak için istediğiniz alanları seçin.</span><span class="sxs-lookup"><span data-stu-id="18e12-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="18e12-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="18e12-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="18e12-114">Bir e-posta şablonu oluştur</span><span class="sxs-lookup"><span data-stu-id="18e12-114">Create an email template</span></span>
1. <span data-ttu-id="18e12-115">Gezinti bölmesinde **Modüller > İnsan Kaynakları > İşe alma > İletişim > Başvuru e-posta şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="18e12-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="18e12-116">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="18e12-116">Select **New**.</span></span>
3. <span data-ttu-id="18e12-117">**Yazışma eylemi** alanından **Görüşme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="18e12-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="18e12-118">Bu tür e-posta iletişiminde kullanmak için yer işaretlerini içeren Yazışma eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="18e12-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="18e12-119">**E-posta şablonu** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="18e12-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="18e12-120">**Konu** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="18e12-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="18e12-121">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="18e12-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="18e12-122">Listede, istenen yer işareti alanını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="18e12-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="18e12-123">Yer işaretleri alanlarını ihtiyaç duyduğunuz yerlere girerken E-mail adresinizi yazmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="18e12-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="18e12-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="18e12-124">Select **Save**.</span></span>


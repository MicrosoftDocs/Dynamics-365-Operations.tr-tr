--- 
title: "E-posta şablonlarını yönetme"
description: "Yeni bir belgeye kuruluşunuzun bilgilerini vertabanından transfer edebilirve bunu başvuranlarla ve adaylarla etkili iletişim kurmak için şablonlarda kullanabilirsiniz."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 67817a3db1aa7d90fd64509b707f075b22010dcb
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="manage-email-templates"></a><span data-ttu-id="81790-103">E-posta şablonlarını yönetme</span><span class="sxs-lookup"><span data-stu-id="81790-103">Manage email templates</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81790-104">Yeni bir belgeye kuruluşunuzun bilgilerini vertabanından transfer edebilirve bunu başvuranlarla ve adaylarla etkili iletişim kurmak için şablonlarda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81790-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="81790-105">Bunu yapmak için sistem verilerinin ekleneceği standart metin ve yer işaretleri içeren bir şablon oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81790-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="81790-106">Örneğin, bir başvuran için adres ve iletişim bilgilerini içeren, söz konusu başvuranla iletişim kurarken kullanabileceğiniz bir Microsoft Word belgesine ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81790-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="81790-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="81790-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="81790-108">E-posta şablonlarınızda kullanmak istediğiniz yer işaretlerini seçin</span><span class="sxs-lookup"><span data-stu-id="81790-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="81790-109">Başvuran yer işaretlerine gidin.</span><span class="sxs-lookup"><span data-stu-id="81790-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="81790-110">Listede, istenen yazışma eylemini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="81790-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="81790-111">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="81790-111">Click Edit.</span></span>
4. <span data-ttu-id="81790-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="81790-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="81790-113">Seçili Yazışma eylemi için bir e-posta şablonu kullanın ve yer işareti alanları taşımak için istediğiniz alanları seçin.</span><span class="sxs-lookup"><span data-stu-id="81790-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="81790-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="81790-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="81790-115">Bir e-posta şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="81790-115">Create an email template</span></span>
1. <span data-ttu-id="81790-116">İnsan Kaynakları > İşe alma > İletişim > Başvuru e-posta şablonları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="81790-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="81790-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="81790-117">Click New.</span></span>
3. <span data-ttu-id="81790-118">Yazmışma eylemi alanından 'Görüşme' seçin.</span><span class="sxs-lookup"><span data-stu-id="81790-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="81790-119">Bu tür e-posta iletişiminde kullanmak için yer işaretlerini içeren Yazışma eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="81790-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="81790-120">E-posta şablonu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="81790-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="81790-121">Konu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="81790-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="81790-122">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="81790-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="81790-123">Listede, istenen yer işareti alanını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="81790-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="81790-124">Yer işaretleri alanlarını ihtiyaç duyduğunuz yerlere girerken E-mail adresinizi yazmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="81790-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="81790-125">Yer işaretleri eklemek istediğiniz alanlar E-mail adresinizi yazmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="81790-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="81790-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="81790-126">Click Save.</span></span>



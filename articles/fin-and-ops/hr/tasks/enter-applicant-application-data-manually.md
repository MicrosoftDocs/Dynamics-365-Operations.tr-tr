--- 
title: "Başvuran ve başvuru verilerini el ile girme"
description: "Bu yordam başvuranlar ve başvuruları hakkındaki bilgileri el ile girmeyi gösterir."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 60b3d155826d234744c9805b18edf0226e237ed3
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="04935-103">Başvuran ve başvuru verilerini el ile girme</span><span class="sxs-lookup"><span data-stu-id="04935-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04935-104">Bu yordam başvuranlar ve başvuruları hakkındaki bilgileri el ile girmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="04935-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="04935-105">Başvuranlar için kişisel bilgileri, görüşme tarihi ve saatlerin, referansları, yetkinlikleri ve konaklama taleplerini girebilir ve muhafaza edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04935-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="04935-106">Ayrıca başvuranların iş başvurularının durumunu güncelleştirebilir ve başvuranlar ile iletişim kurmak için mektup veya e-posta iletileri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04935-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="04935-107">Bir başvuran kaydı oluşturduğunuzda, Genel Adres Defteri'nde o başvuran kişi için kayıt oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="04935-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="04935-108">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="04935-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="04935-109">Yeni bir başvuran kaydı oluşturun</span><span class="sxs-lookup"><span data-stu-id="04935-109">Create a new applicant record</span></span>
1. <span data-ttu-id="04935-110">İnsan Kaynakları > İşe alma > Başvuranlar > Başvuranlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="04935-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="04935-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04935-111">Click New.</span></span>
3. <span data-ttu-id="04935-112">Ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="04935-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="04935-113">Soyadı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="04935-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="04935-114">Varsa, Başvuranın ek bilgi girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04935-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="04935-115">Örneğin, başvuranın en yüksek eğitim derecesini, geçerli iş unvanını veya önceki işveren bilgileri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="04935-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="04935-116">İletişim bilgileri bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="04935-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="04935-117">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="04935-117">Click Add.</span></span>
7. <span data-ttu-id="04935-118">Açıklama alanına 'İletişim e-postası' yazın.</span><span class="sxs-lookup"><span data-stu-id="04935-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="04935-119">Tür alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="04935-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="04935-120">İletişim numarası/adresi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="04935-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="04935-121">Bu e-posta adresi, Başvuranla e-posta iletişimini üretmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="04935-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="04935-122">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="04935-122">Click Add.</span></span>
11. <span data-ttu-id="04935-123">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="04935-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="04935-124">İletişim numarası/adresi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="04935-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="04935-125">Başvuran kişisel bilgileri.</span><span class="sxs-lookup"><span data-stu-id="04935-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="04935-126">Gerekirse, başvuran için ek kişisel bilgiler girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04935-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="04935-127">Örneğin, bu doğum tarihi, etnik köken, cinsiyet ve medeni durumu içerebilir.</span><span class="sxs-lookup"><span data-stu-id="04935-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="04935-128">,Eylem Bölmesinde, Yetkinlikler öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04935-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="04935-129">Başvuranın kendi becerilerini, mesleki deneyimlerini, eğitimini, testlerini veya sertifikalarını da dahil olmak üzere uzmanlık profilini girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04935-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="04935-130">Bu bilgiler, şirketinizin verilerde tanımlanan işlerle ilişkili yetenekleri başvuranın becerilerine eşlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="04935-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="04935-131">Başvuran için bir başvuru oluşturun</span><span class="sxs-lookup"><span data-stu-id="04935-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="04935-132">Başvurular'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04935-132">Click Applications.</span></span>
2. <span data-ttu-id="04935-133">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04935-133">Click New.</span></span>
3. <span data-ttu-id="04935-134">İşe alma projesi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04935-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04935-135">Bir işe alma projesini seçerek, başvuran bu işle projesinde bulunan belirli bir yer açılması ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="04935-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="04935-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="04935-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="04935-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04935-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="04935-138">Varsayılan olarak iş, seçili işe alma projesi ve departmana dayanır.</span><span class="sxs-lookup"><span data-stu-id="04935-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="04935-139">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04935-139">Click Save.</span></span>
    * <span data-ttu-id="04935-140">Uygulama kaydettikten sonra, başvuranın deneyimi, ödülleri ve kapak mektubu gibi belgeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04935-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  



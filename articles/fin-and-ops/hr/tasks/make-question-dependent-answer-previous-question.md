--- 
title: "Önceki sorunun yanıtına bağımlı sorular hazırlama"
description: "Koşullu sorular, yanıtlayan kişinin önceki soruya verdiği cevaba göre hangi sorunun bir sonra sorulacağını belirlemenize olanak sağlar."
author: ShylaThompson
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3e0a6d63a266bf49764c8cdcfd407ff0733ea27c
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="make-questions-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="26f25-103">Önceki sorunun yanıtına bağımlı sorular hazırlama</span><span class="sxs-lookup"><span data-stu-id="26f25-103">Make questions dependent on the answer of the previous question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26f25-104">Koşullu sorular, yanıtlayan kişinin önceki soruya verdiği cevaba göre hangi sorunun bir sonra sorulacağını belirlemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="26f25-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="26f25-105">Örneğin, "Kahve mi Çay mı tercih ediyorsunuz" sorusunu sorarsanız, yanıtlayanın cevapta çay mı kahve mi vermiş olduğuna göre mantıksal bir takip sorusu ile devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f25-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="26f25-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="26f25-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="26f25-107">Mevcut soru formunu bulun</span><span class="sxs-lookup"><span data-stu-id="26f25-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="26f25-108">Soru formu > Tasarım > Soru formları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="26f25-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="26f25-109">Listede, WorkFH soru formunu seçin.</span><span class="sxs-lookup"><span data-stu-id="26f25-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="26f25-110">Soru formuna tüm soruları ve alt soruları ekleyin</span><span class="sxs-lookup"><span data-stu-id="26f25-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="26f25-111">Sorular'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="26f25-111">Click Questions.</span></span>
2. <span data-ttu-id="26f25-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="26f25-112">Click New.</span></span>
3. <span data-ttu-id="26f25-113">Sorular alanında 00016 numaralı soruyu seçin.</span><span class="sxs-lookup"><span data-stu-id="26f25-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="26f25-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="26f25-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="26f25-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="26f25-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="26f25-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="26f25-116">Click Save.</span></span>
7. <span data-ttu-id="26f25-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="26f25-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="26f25-118">Soru formu sırasını Koşullu olarak ayarlayın ve soruyu uygun soruya bağımlı hale getirin</span><span class="sxs-lookup"><span data-stu-id="26f25-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="26f25-119">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="26f25-119">Click Edit.</span></span>
2. <span data-ttu-id="26f25-120">Kurulum bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="26f25-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="26f25-121">Soru sıralaması alanında 'Koşullu' seçin.</span><span class="sxs-lookup"><span data-stu-id="26f25-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="26f25-122">Koşullu soru'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="26f25-122">Click Conditional question.</span></span>
5. <span data-ttu-id="26f25-123">Ağaçta seçin 'Questions\Explain why you answered the previous question the way you did?'.</span><span class="sxs-lookup"><span data-stu-id="26f25-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="26f25-124">Birincil soru alanında 00009 numaralı soruyu seçin.</span><span class="sxs-lookup"><span data-stu-id="26f25-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="26f25-125">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="26f25-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="26f25-126">Yanıt alanında, soruyu koşullandırmak istediğiniz yanıt seçeneğinin yanıt sıra kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="26f25-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="26f25-127">Örneğin, ilk yanıt seçeneği için 1 girin.</span><span class="sxs-lookup"><span data-stu-id="26f25-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="26f25-128">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="26f25-128">Click Save.</span></span>
10. <span data-ttu-id="26f25-129">Ağaçta 'Questions\I am paid fairly for the work I do.'.</span><span class="sxs-lookup"><span data-stu-id="26f25-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="26f25-130">Soru ağacının bağımlılığı göstermek için güncelleştirildiğinin farkına varın.</span><span class="sxs-lookup"><span data-stu-id="26f25-130">Note that the question tree updated to show the dependency.</span></span>  



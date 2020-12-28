---
title: Görev ayrımını ayarlamak
description: Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688185"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="7fe1d-103">Görev ayrımını ayarlamak</span><span class="sxs-lookup"><span data-stu-id="7fe1d-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7fe1d-104">Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="7fe1d-105">Bu kavram, görev ayrımı adını taşır.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="7fe1d-106">Örneğin, malların giriş kabul etmek ve satıcının ödemesini işlemek için aynı kişi istemeyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="7fe1d-107">Görevlerin ayrılması dolandırıcılık riskini azaltır, hataları ve düzensizlikleri tespit etmenizi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="7fe1d-108">Görev ayrımlarını ayrıca dahili denetim kurallarının uygulanması için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="7fe1d-109">Bir kural yaratmak için aşağıdaki yordamı takip edin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="7fe1d-110">Bu yordamı tamamlamak için sistem yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="7fe1d-111">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi DAT'dir.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="7fe1d-112">**Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Görev ayrımı > Görev ayırma kuralları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="7fe1d-113">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-113">Click **New**.</span></span>
3. <span data-ttu-id="7fe1d-114">**Ad** alanına kural için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="7fe1d-115">**İlk görev** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7fe1d-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="7fe1d-117">Kural tarafından denetlenen ilk görevi seçin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="7fe1d-118">**İkinci görev** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="7fe1d-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="7fe1d-120">Kural tarafından denetlenen ikinci görevi seçin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="7fe1d-121">**Önem derecesi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="7fe1d-122">Aynı kullanıcının veya rolün her iki görevi de gerçekleştirdiğinde oluşacak riskin önemini seçin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="7fe1d-123">**Güvenlik riski** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="7fe1d-124">Güvenlik riski için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="7fe1d-125">**Güvenlik azaltma** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="7fe1d-126">Güvenlik riskini ortadan kaldırmak için yapılacaklar eylemler için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="7fe1d-127">Örneğin, işlemi daha ayrıntılı inceleyerek, aylık yönetim incelemesi yapılmasını veya kaynakların diğer departmanlarla paylaşılmasını sağlayarak riski azaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="7fe1d-128">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fe1d-128">Click **Save**.</span></span>


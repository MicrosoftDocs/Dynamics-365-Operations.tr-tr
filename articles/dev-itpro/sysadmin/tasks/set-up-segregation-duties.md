--- 
title: "Görev ayrımını ayarlamak"
description: "Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0e20272f09cc8c75bdd93ebcc996cf58b98ccf67
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="ff03a-103">Görev ayrımını ayarlamak</span><span class="sxs-lookup"><span data-stu-id="ff03a-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff03a-104">Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff03a-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="ff03a-105">Bu kavram, görev ayrımı adını taşır.</span><span class="sxs-lookup"><span data-stu-id="ff03a-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="ff03a-106">Örneğin, malların giriş kabul etmek ve satıcının ödemesini işlemek için aynı kişi istemeyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff03a-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="ff03a-107">Görevlerin ayrılması dolandırıcılık riskini azaltır, hataları ve düzensizlikleri tespit etmenizi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="ff03a-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="ff03a-108">Görev ayrımlarını ayrıca dahili denetim kurallarının uygulanması için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff03a-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="ff03a-109">Bir kural yaratmak için aşağıdaki yordamı takip edin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="ff03a-110">Bu yordamı tamamlamak için sistem yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ff03a-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="ff03a-111">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi DAT'dir.</span><span class="sxs-lookup"><span data-stu-id="ff03a-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="ff03a-112">Sistem Yönetimi > Güvenlik > Görev ayrımı > Görev ayrımı kuralları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="ff03a-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-113">Click New.</span></span>
3. <span data-ttu-id="ff03a-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ff03a-115">Kural için bir isim girin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="ff03a-116">Birinci görev alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ff03a-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ff03a-118">Kural tarafından denetlenen ilk görevi seçin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="ff03a-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ff03a-120">İkinci görev alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ff03a-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ff03a-122">Kural tarafından denetlenen ikinci görevi seçin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="ff03a-123">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ff03a-124">Önem alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="ff03a-125">Aynı kullanıcının veya rolün her iki görevi de gerçekleştirdiğinde oluşacak riskin önemini seçin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="ff03a-126">Güvenlik riski alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="ff03a-127">Güvenlik riski için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="ff03a-128">Risk azaltma alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="ff03a-129">Güvenlik riskini ortadan kaldırmak için yapılacaklar eylemler için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ff03a-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="ff03a-130">Örneğin, işlemi daha ayrıntılı inceleyerek, aylık yönetim incelemesi yapılmasını veya kaynakların diğer departmanlarla paylaşılmasını sağlayarak riski azaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff03a-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="ff03a-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff03a-131">Click Save.</span></span>



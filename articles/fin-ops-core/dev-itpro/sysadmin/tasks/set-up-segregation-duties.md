---
title: Görev ayrımını ayarlamak
description: Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745753"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="2ee8c-103">Görev ayrımını ayarlamak</span><span class="sxs-lookup"><span data-stu-id="2ee8c-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ee8c-104">Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="2ee8c-105">Bu kavram, görev ayrımı adını taşır.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="2ee8c-106">Örneğin, aynı kişinin malların girişini kabul etmesini ve satıcıya ödemeyi işlemesini isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="2ee8c-107">Görevlerin ayrılması dolandırıcılık riskini azaltır, hataları ve düzensizlikleri tespit etmenizi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="2ee8c-108">Görev ayrımlarını ayrıca dahili denetim kurallarının uygulanması için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="2ee8c-109">Bir kural yaratmak için aşağıdaki yordamı takip edin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="2ee8c-110">Bu yordamı tamamlamak için sistem yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="2ee8c-111">**Sistem yönetimi** > **Güvenlik** > **Görev ayrımı** > **Görev ayrımı kuralları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="2ee8c-112">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-112">Click **New**.</span></span>
3. <span data-ttu-id="2ee8c-113">**Ad** alanına kural için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="2ee8c-114">**İlk görev** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2ee8c-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="2ee8c-116">Kural tarafından denetlenen ilk görevi seçin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="2ee8c-117">**İkinci görev** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="2ee8c-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="2ee8c-119">Kural tarafından denetlenen ikinci görevi seçin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="2ee8c-120">**Önem derecesi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="2ee8c-121">Aynı kullanıcının veya rolün her iki görevi de gerçekleştirdiğinde oluşacak riskin önemini seçin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="2ee8c-122">**Güvenlik riski** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="2ee8c-123">Güvenlik riski için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="2ee8c-124">**Güvenlik azaltma** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="2ee8c-125">Güvenlik riskini ortadan kaldırmak için yapılacaklar eylemler için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="2ee8c-126">Örneğin, işlemi daha ayrıntılı inceleyerek, aylık yönetim incelemesi yapılmasını veya kaynakların diğer departmanlarla paylaşılmasını sağlayarak riski azaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="2ee8c-127">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="2ee8c-128">Görev ayrımı kurallarına uygunluk, kural oluşturduğunuzda doğrulanmaz.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="2ee8c-129">Mevcut roller için çakışma oluşturan bir kural oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="2ee8c-130">Mevcut kullanıcı rolü atamaları yeni kuralla çakışıyor da olabilir.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="2ee8c-131">Bir kuralı oluşturduktan veya değiştirdikten sonra uyumluluğu doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2ee8c-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="2ee8c-132">Daha fazla bilgi için bkz. [Görev ayrımındaki çakışmaları tanımlama ve çözümleme](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="2ee8c-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
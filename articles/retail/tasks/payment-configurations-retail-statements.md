--- 
title: " Perakende ekstreleri için ödeme yapılandırmaları"
description: "Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende mağaza ödeme yöntemlerine ilişkin yapılandırmaları gösterir."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 51faf6d45fde8aa7e2adad69306891f17c943e85
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="2230d-103"> Perakende ekstreleri için ödeme yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="2230d-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2230d-104">Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende mağaza ödeme yöntemlerine ilişkin yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="2230d-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="2230d-105">Bu kayıt, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2230d-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="2230d-106">Retail and commerce > Channels > Retail stores > All retail stores (Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="2230d-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="2230d-107">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2230d-108">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2230d-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2230d-109">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2230d-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="2230d-110">Ödeme yöntemleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2230d-110">Click Payment methods.</span></span>
6. <span data-ttu-id="2230d-111">Nakil bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="2230d-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="2230d-112">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2230d-112">Click Edit.</span></span>
    * <span data-ttu-id="2230d-113">Bu ödeme yöntemi için alınan tutarların genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="2230d-114">Bu ödeme yöntemi için alınan tutarların nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="2230d-115">Alınan toplam hareket tutarı ile bu ödeme yöntemi için sayılan tutar arasındaki olası farkların nakledileceği bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="2230d-116">Bu alana, fark tutarının ne zaman başka bir fark hesabına nakledileceğini belirlemek için bir tutar girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2230d-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="2230d-117">Bu özelliği büyük farkları izlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2230d-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="2230d-118">"Maksimum fark tutarı" alanında belirlenen değerden daha yüksek olduğunda, alınan toplam hareket tutarı ile sayılan tutar arasındaki olası farkları nakletmek için bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="2230d-119">Bankaya nakledilen tutarları ayrı bir hesaba nakletmek için "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-119">Select "Yes" to post bank drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="2230d-120">Bu alanda, bankaya nakledilen para tutarlarının genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2230d-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="2230d-121">Banka para nakil tutarlarının nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="2230d-122">Bankaya nakledilen tutarları banka hesabına aktarırken kullanılacak banka hareketi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="2230d-123">Kasaya nakledilen tutarları ayrı bir hesaba nakletmek için "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-123">Select "Yes" to post safe drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="2230d-124">Kasya nakledilen para tutarlarının genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="2230d-125">Kasaya nakil tutarlarının nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="2230d-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="2230d-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2230d-126">Click Save.</span></span>



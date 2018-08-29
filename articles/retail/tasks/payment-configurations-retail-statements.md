--- 
title: "Perakende ekstrelerini etkileyen ödeme yöntemi ayarlarını yapılandırma"
description: "Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende mağaza ödeme yöntemlerine ilişkin yapılandırmaları gösterir."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ba21db9ee97dc4d851c77a906927ef513940b743
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="configure-payment-method-settings-that-affect-retail-statements"></a><span data-ttu-id="a9516-103">Perakende ekstrelerini etkileyen ödeme yöntemi ayarlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a9516-103">Configure payment method settings that affect retail statements</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a9516-104">Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende mağaza ödeme yöntemlerine ilişkin yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9516-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="a9516-105">Bu kayıt, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a9516-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="a9516-106">Retail and commerce > Channels > Retail stores > All retail stores (Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a9516-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="a9516-107">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a9516-108">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9516-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a9516-109">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9516-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="a9516-110">Ödeme yöntemleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9516-110">Click Payment methods.</span></span>
6. <span data-ttu-id="a9516-111">Nakil bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="a9516-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="a9516-112">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9516-112">Click Edit.</span></span>
    * <span data-ttu-id="a9516-113">Bu ödeme yöntemi için alınan tutarların genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="a9516-114">Bu ödeme yöntemi için alınan tutarların nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="a9516-115">Alınan toplam hareket tutarı ile bu ödeme yöntemi için sayılan tutar arasındaki olası farkların nakledileceği bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="a9516-116">Bu alana, fark tutarının ne zaman başka bir fark hesabına nakledileceğini belirlemek için bir tutar girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9516-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="a9516-117">Bu özelliği büyük farkları izlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9516-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="a9516-118">"Maksimum fark tutarı" alanında belirlenen değerden daha yüksek olduğunda, alınan toplam hareket tutarı ile sayılan tutar arasındaki olası farkları nakletmek için bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="a9516-119">Bankaya nakledilen tutarları ayrı bir hesaba nakletmek için "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="a9516-120">Bu alanda, bankaya nakledilen para tutarlarının genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9516-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="a9516-121">Banka para nakil tutarlarının nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="a9516-122">Bankaya nakledilen tutarları banka hesabına aktarırken kullanılacak banka hareketi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="a9516-123">Kasaya nakledilen tutarları ayrı bir hesaba nakletmek için "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="a9516-124">Kasya nakledilen para tutarlarının genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="a9516-125">Kasaya nakil tutarlarının nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="a9516-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="a9516-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9516-126">Click Save.</span></span>



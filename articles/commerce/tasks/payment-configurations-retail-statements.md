---
title: " Perakende ekstreleri için ödeme yapılandırmaları"
description: Bu yordam, Ticaret ekstrelerinin oluşturulması ve nakledilmesini etkileyen Ticaret mağaza ödeme yöntemlerine ilişkin yapılandırmaları gösterir.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8723f786c2eaf5f045007de32ce5cbe57563eaf9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205709"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="eef73-103"> Perakende ekstreleri için ödeme yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="eef73-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eef73-104">Bu yordam, Ticaret ekstrelerinin oluşturulması ve nakledilmesini etkileyen Ticaret mağaza ödeme yöntemlerine ilişkin yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="eef73-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="eef73-105">Bu kayıt, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="eef73-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="eef73-106">Perakende ve Ticaret > Kanallar > Mağazalar > Tüm mağazalar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="eef73-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="eef73-107">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eef73-108">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eef73-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="eef73-109">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eef73-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="eef73-110">Ödeme yöntemleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eef73-110">Click Payment methods.</span></span>
6. <span data-ttu-id="eef73-111">Nakil bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="eef73-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="eef73-112">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eef73-112">Click Edit.</span></span>
    * <span data-ttu-id="eef73-113">Bu ödeme yöntemi için alınan tutarların genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="eef73-114">Bu ödeme yöntemi için alınan tutarların nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="eef73-115">Alınan toplam hareket tutarı ile bu ödeme yöntemi için sayılan tutar arasındaki olası farkların nakledileceği bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="eef73-116">Bu alana, fark tutarının ne zaman başka bir fark hesabına nakledileceğini belirlemek için bir tutar girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eef73-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="eef73-117">Bu özelliği büyük farkları izlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eef73-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="eef73-118">"Maksimum fark tutarı" alanında belirlenen değerden daha yüksek olduğunda, alınan toplam hareket tutarı ile sayılan tutar arasındaki olası farkları nakletmek için bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="eef73-119">Bankaya nakledilen tutarları ayrı bir hesaba nakletmek için "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="eef73-120">Bu alanda, bankaya nakledilen para tutarlarının genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eef73-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="eef73-121">Banka para nakil tutarlarının nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="eef73-122">Bankaya nakledilen tutarları banka hesabına aktarırken kullanılacak banka hareketi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="eef73-123">Kasaya nakledilen tutarları ayrı bir hesaba nakletmek için "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="eef73-124">Kasya nakledilen para tutarlarının genel muhasebe hesabına mı yoksa banka hesabına mı nakledileceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="eef73-125">Kasaya nakil tutarlarının nakledileceği hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="eef73-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="eef73-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eef73-126">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
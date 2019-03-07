---
title: Müşteri için ileri tarih atılmış çeki kaydetme ve deftere nakletme
description: Bir müşteriden alınan bir vadeli çekin ayrıntılarını kaydedebilirsiniz.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 131e4f364c62d03b95fb4b77f472828b9483d5e1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "347388"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="dfa2e-103">Müşteri için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="dfa2e-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dfa2e-104">Bir müşteriden alınan bir vadeli çekin ayrıntılarını kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="dfa2e-105">Veya vadeli çeki nakledip finansal işlem oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="dfa2e-106">Bir müşteriden alınan vadeli çeki kayıt ve nakletmeden önce aşağıdaki görevleri tamamlayın: • Nakit ve banka yönetimi sayfası'nda vadeli çeki ayarlayın • Vadeli çeklerin ödenmesi için bir ödeme yöntemi ayarlayın Bu yordamın rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="dfa2e-107">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="dfa2e-108">Alacak hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="dfa2e-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-109">Click New.</span></span>
3. <span data-ttu-id="dfa2e-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dfa2e-111">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-111">Click Lines.</span></span>
5. <span data-ttu-id="dfa2e-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="dfa2e-113">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="dfa2e-114">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="dfa2e-115">Vadeli çekte belirlenmiş olan miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="dfa2e-116">Ödeme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="dfa2e-117">Ödeme yöntemi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="dfa2e-118">Vadeli çekin ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="dfa2e-119">Vadeli çekler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="dfa2e-120">Vade tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="dfa2e-121">Vadeli çekin vade tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="dfa2e-122">Amir banka şubesi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="dfa2e-123">Vadeli çekin banka detaylarını girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="dfa2e-124">Çek numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="dfa2e-125">Amir banka adına alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="dfa2e-126">Vadeli çekin banka detaylarını girin.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="dfa2e-127">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-127">Click Post.</span></span>
16. <span data-ttu-id="dfa2e-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dfa2e-128">Close the page.</span></span>


---
title: RFQ'lar için puanlama yöntemi oluşturma
description: Bu prosedür, size bir puanlama yönteminin nasıl oluşturulacağını göstermektedir.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba3f0b2be16c02129616025c0ee6258996189c6a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211826"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="1bb8b-103">RFQ'lar için puanlama yöntemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1bb8b-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1bb8b-104">Bu prosedür, size bir puanlama yönteminin nasıl oluşturulacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="1bb8b-105">Puanlama yöntemi resmi teklif talebine (RFQ) yanıt olarak gönderilen tekliflerin karşılaştırılabilmesi için kullanılan bir ölçüt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="1bb8b-106">Örneğin, bir satıcıyı geçmiş performansı üzerinden değerlendirmek veya şirketin çevre dostu veya iyi bir işbirlikçi olup olmadığını değerlendirmek isteyebilir veya fiyata göre teklifleri karşılaştırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="1bb8b-107">Bu türe ait RFQ'ler için varsayılan puanlama yöntemi olduğundan talep türüyle bir puanlama yöntemini ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="1bb8b-108">Bu görevler genellikle satınalma yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="1bb8b-109">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="1bb8b-110">Tedarik ve kaynak atama > Ayarlar > Teklif talebi > Skor yöntemi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="1bb8b-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-111">Click New.</span></span>
3. <span data-ttu-id="1bb8b-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1bb8b-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1bb8b-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-114">Click Save.</span></span>
6. <span data-ttu-id="1bb8b-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-115">Click New.</span></span>
7. <span data-ttu-id="1bb8b-116">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="1bb8b-117">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1bb8b-118">RFQ için bir puanlama yöntemi seçildiğinde bu tanım puanlama yöntemi adı ile birlikte görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="1bb8b-119">Aralık başlangıcı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="1bb8b-120">Aralık, tedarik profesyonelinin puan olarak girebileceği değerleri sınırlar.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="1bb8b-121">RFQ üzerinde birden çok puanlama kriteri varsa girilen puanlar birbirlerine eklenir ve toplam, tekliflerin karşılaştırılmasını sağlayacak şekilde kullanılabilir duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="1bb8b-122">Aralık bitişi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="1bb8b-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-123">Click New.</span></span>
12. <span data-ttu-id="1bb8b-124">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="1bb8b-125">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="1bb8b-126">Aralık başlangıcı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="1bb8b-127">Aralık bitişi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1bb8b-127">In the Range to field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
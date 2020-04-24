---
title: RFQ'lar için puanlama yöntemi oluşturma
description: Bu prosedür, size bir puanlama yönteminin nasıl oluşturulacağını göstermektedir.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8657098519391ee488025e175e1499c58a55ce
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204666"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="7d08a-103">RFQ'lar için puanlama yöntemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7d08a-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d08a-104">Bu prosedür, size bir puanlama yönteminin nasıl oluşturulacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="7d08a-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="7d08a-105">Puanlama yöntemi resmi teklif talebine (RFQ) yanıt olarak gönderilen tekliflerin karşılaştırılabilmesi için kullanılan bir ölçüt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="7d08a-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="7d08a-106">Örneğin, bir satıcıyı geçmiş performansı üzerinden değerlendirmek veya şirketin çevre dostu veya iyi bir işbirlikçi olup olmadığını değerlendirmek isteyebilir veya fiyata göre teklifleri karşılaştırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d08a-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="7d08a-107">Bu türe ait RFQ'ler için varsayılan puanlama yöntemi olduğundan talep türüyle bir puanlama yöntemini ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d08a-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="7d08a-108">Bu görevler genellikle satınalma yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="7d08a-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="7d08a-109">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d08a-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="7d08a-110">Tedarik ve kaynak atama > Ayarlar > Teklif talebi > Skor yöntemi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7d08a-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="7d08a-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d08a-111">Click New.</span></span>
3. <span data-ttu-id="7d08a-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7d08a-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7d08a-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7d08a-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7d08a-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d08a-114">Click Save.</span></span>
6. <span data-ttu-id="7d08a-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d08a-115">Click New.</span></span>
7. <span data-ttu-id="7d08a-116">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7d08a-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="7d08a-117">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7d08a-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7d08a-118">RFQ için bir puanlama yöntemi seçildiğinde bu tanım puanlama yöntemi adı ile birlikte görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7d08a-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="7d08a-119">Aralık başlangıcı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7d08a-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="7d08a-120">Aralık, tedarik profesyonelinin puan olarak girebileceği değerleri sınırlar.</span><span class="sxs-lookup"><span data-stu-id="7d08a-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="7d08a-121">RFQ üzerinde birden çok puanlama kriteri varsa girilen puanlar birbirlerine eklenir ve toplam, tekliflerin karşılaştırılmasını sağlayacak şekilde kullanılabilir duruma getirilir.</span><span class="sxs-lookup"><span data-stu-id="7d08a-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="7d08a-122">Aralık bitişi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7d08a-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="7d08a-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d08a-123">Click New.</span></span>
12. <span data-ttu-id="7d08a-124">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7d08a-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="7d08a-125">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7d08a-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="7d08a-126">Aralık başlangıcı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7d08a-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="7d08a-127">Aralık bitişi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7d08a-127">In the Range to field, enter a number.</span></span>


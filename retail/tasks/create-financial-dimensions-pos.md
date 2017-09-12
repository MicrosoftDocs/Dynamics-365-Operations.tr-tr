--- 
title: " POS kayıtları için mali boyutlar oluşturma ve kayıtlardaki boyut değerlerini yapılandırma"
description: "Bu yordam satış noktası (POS) kayıtları için mali boyutlar oluşturma konusunda açıklama içerir kayıtlarda mali boyut değerlerinin nasıl yapılandırılacağını gösterir."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8a3a6abc19bae20b7899628d0463cf458955671a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="3e173-103"> POS kayıtları için mali boyutlar oluşturma ve kayıtlardaki boyut değerlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3e173-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3e173-104">Bu yordam satış noktası (POS) kayıtları için mali boyutlar oluşturma konusunda açıklama içerir kayıtlarda mali boyut değerlerinin nasıl yapılandırılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e173-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="3e173-105">Bu prosedür, boyut kümeleri ve hesap yapıları oluşturma gibi diğer ilgili adımları içermez.</span><span class="sxs-lookup"><span data-stu-id="3e173-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="3e173-106">Bu konular diğer görevlerde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="3e173-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="3e173-107">Bu kayıt, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3e173-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="3e173-108">General ledger > Chart of accounts > Dimensions > Financial dimensions (Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="3e173-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="3e173-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e173-109">Click New.</span></span>
3. <span data-ttu-id="3e173-110">Şuradan alınan değerleri kullan alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="3e173-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="3e173-111">Boyut adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3e173-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="3e173-112">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e173-112">Click Activate.</span></span>
6. <span data-ttu-id="3e173-113">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e173-113">Click Close.</span></span>
7. <span data-ttu-id="3e173-114">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e173-114">Click Activate.</span></span>
8. <span data-ttu-id="3e173-115">Boyut değerlerini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e173-115">Click Dimension values.</span></span>
9. <span data-ttu-id="3e173-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3e173-116">Close the page.</span></span>
10. <span data-ttu-id="3e173-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e173-117">Click Save.</span></span>
11. <span data-ttu-id="3e173-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3e173-118">Close the page.</span></span>
12. <span data-ttu-id="3e173-119">Retail and commerce > Channel setup > POS setup > Registers (Perakende ve ticaret > Kanal kurulumu > POS kurulumu > Kayıtlar) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="3e173-119">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="3e173-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3e173-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="3e173-121">Finansal boyutlar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="3e173-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="3e173-122">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e173-122">Click Edit.</span></span>
16. <span data-ttu-id="3e173-123">Terminal alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e173-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="3e173-124">Listede, güncelleştirilecek kayda ilişkin boyut değerini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3e173-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="3e173-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e173-125">Click Save.</span></span>



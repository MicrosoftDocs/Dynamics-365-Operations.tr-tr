---
title: Pozisyonun raporlama ilişkilerini değiştirme
description: Bu yordam, bir personel için raporlama ilişkisinin nasıl değiştirileceğini gösterir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3285222b11905999f0eadb846ac785342c16aa38
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010892"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="c9c58-103">Pozisyonun raporlama ilişkilerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c9c58-103">Modify reporting relationships for a position</span></span>



<span data-ttu-id="c9c58-104">Bu yordam, bir personel için raporlama ilişkisinin nasıl değiştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9c58-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="c9c58-105">Raporlama ilişkisi, iş akışı içinde belgeleri yönlendirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c9c58-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="c9c58-106">Yordam, personelin ayrıca ek hiyerarşilere nasıl atanacağını da gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9c58-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="c9c58-107">Örneğin bir personel, proje yöneticisine resmi olmayan bir raporlama ilişkisi olan bir projede takımının bir parçası olabilir.</span><span class="sxs-lookup"><span data-stu-id="c9c58-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="c9c58-108">Ek olarak konuma, çeşitli Proje veya Matris senaryoları kapsayacak raporlama ilişkileri tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c9c58-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="c9c58-109">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c9c58-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c9c58-110">İnsan Kaynakları > Pozisyonlar > Pozisyonlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c9c58-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="c9c58-111">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="c9c58-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c9c58-112">Örneğin, '000091' değerine sahip pozisyon alanı üzerinde filtreleme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="c9c58-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="c9c58-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c9c58-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c9c58-114">Pozisyonu konumlandırmak için Raporlar'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="c9c58-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="c9c58-115">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c9c58-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="c9c58-116">Raporlar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c9c58-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="c9c58-117">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c9c58-117">Click Create.</span></span>
8. <span data-ttu-id="c9c58-118">İlişkiler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c9c58-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="c9c58-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c9c58-119">Click Add.</span></span>
10. <span data-ttu-id="c9c58-120">Tablonun solundaki onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c9c58-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="c9c58-121">Hiyerarşi adı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c9c58-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="c9c58-122">Örnek: Proje</span><span class="sxs-lookup"><span data-stu-id="c9c58-122">Example: Project</span></span>  
12. <span data-ttu-id="c9c58-123">Pozisyonlara raporlar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c9c58-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="c9c58-124">Örnek:  000437</span><span class="sxs-lookup"><span data-stu-id="c9c58-124">Example:  000437</span></span>
13. <span data-ttu-id="c9c58-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c9c58-125">Click Save.</span></span>


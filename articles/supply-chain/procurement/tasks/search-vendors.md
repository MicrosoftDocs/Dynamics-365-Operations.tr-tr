---
title: Satıcı arama
description: Belirli ölçütlere dayalı satıcı araması yapmayı öğrenin.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1982c8dffbc7a65263babce7738045b744db2592
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149539"
---
# <a name="search-for-vendors"></a><span data-ttu-id="5b24b-103">Satıcı arama</span><span class="sxs-lookup"><span data-stu-id="5b24b-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b24b-104">Belirli ölçütlere dayalı satıcı araması yapmayı öğrenin.</span><span class="sxs-lookup"><span data-stu-id="5b24b-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="5b24b-105">Bu örnek, belirli bir tedarik kategorisi için onaylanmış ve belli bir ülkede bulunan ve birincil adresi olan satıcılar için arama yapma gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b24b-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="5b24b-106">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b24b-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="5b24b-107">Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="5b24b-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="5b24b-108">Tedarik ve kaynak > Satıcılar > Satıcı arama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b24b-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="5b24b-109">Tedarik kategorisi seçim sayfasını açmak için Artı simgesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b24b-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="5b24b-110">Ağaçtan, 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5b24b-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="5b24b-111">Bu yordamı bir görev kılavuzu olarak çalıştırıyorsanız, doğru düğümü seçmeden önce kilidi Aç düğmesini tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="5b24b-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="5b24b-112">USMF kullanmıyorsanız mevcut bulunan kategorilerden birini seçin.</span><span class="sxs-lookup"><span data-stu-id="5b24b-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="5b24b-113">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b24b-113">Click Add.</span></span>
    * <span data-ttu-id="5b24b-114">Burada birden fazla kategori seçmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="5b24b-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="5b24b-115">Bunu yaparsanız, arama, kategorilerin en az biri için onaylanan tüm satıcıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="5b24b-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="5b24b-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b24b-116">Click OK.</span></span>
6. <span data-ttu-id="5b24b-117">Ülke/bölge alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5b24b-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="5b24b-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b24b-118">Click OK.</span></span>


---
title: Satıcı arama
description: Belirli ölçütlere dayalı satıcı araması yapmayı öğrenin.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7caa146532d2bce06b009c45da635327766a88d1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020717"
---
# <a name="search-for-vendors"></a><span data-ttu-id="f1e6c-103">Satıcı arama</span><span class="sxs-lookup"><span data-stu-id="f1e6c-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1e6c-104">Belirli ölçütlere dayalı satıcı araması yapmayı öğrenin.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="f1e6c-105">Bu örnek, belirli bir tedarik kategorisi için onaylanmış ve belli bir ülkede bulunan ve birincil adresi olan satıcılar için arama yapma gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="f1e6c-106">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="f1e6c-107">Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="f1e6c-108">Tedarik ve kaynak > Satıcılar > Satıcı arama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="f1e6c-109">Tedarik kategorisi seçim sayfasını açmak için Artı simgesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="f1e6c-110">Ağaçtan, 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="f1e6c-111">Bu yordamı bir görev kılavuzu olarak çalıştırıyorsanız, doğru düğümü seçmeden önce kilidi Aç düğmesini tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="f1e6c-112">USMF kullanmıyorsanız mevcut bulunan kategorilerden birini seçin.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="f1e6c-113">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-113">Click Add.</span></span>
    * <span data-ttu-id="f1e6c-114">Burada birden fazla kategori seçmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="f1e6c-115">Bunu yaparsanız, arama, kategorilerin en az biri için onaylanan tüm satıcıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="f1e6c-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-116">Click OK.</span></span>
6. <span data-ttu-id="f1e6c-117">Ülke/bölge alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="f1e6c-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f1e6c-118">Click OK.</span></span>


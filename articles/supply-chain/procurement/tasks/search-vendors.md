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
ms.openlocfilehash: cf93307600aac6fa6e45524092ec4811742010e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244051"
---
# <a name="search-for-vendors"></a><span data-ttu-id="8d6c3-103">Satıcı arama</span><span class="sxs-lookup"><span data-stu-id="8d6c3-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d6c3-104">Belirli ölçütlere dayalı satıcı araması yapmayı öğrenin.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="8d6c3-105">Bu örnek, belirli bir tedarik kategorisi için onaylanmış ve belli bir ülkede bulunan ve birincil adresi olan satıcılar için arama yapma gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="8d6c3-106">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="8d6c3-107">Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="8d6c3-108">Tedarik ve kaynak > Satıcılar > Satıcı arama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="8d6c3-109">Tedarik kategorisi seçim sayfasını açmak için Artı simgesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="8d6c3-110">Ağaçtan, 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="8d6c3-111">Bu yordamı bir görev kılavuzu olarak çalıştırıyorsanız, doğru düğümü seçmeden önce kilidi Aç düğmesini tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="8d6c3-112">USMF kullanmıyorsanız mevcut bulunan kategorilerden birini seçin.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="8d6c3-113">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-113">Click Add.</span></span>
    * <span data-ttu-id="8d6c3-114">Burada birden fazla kategori seçmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="8d6c3-115">Bunu yaparsanız, arama, kategorilerin en az biri için onaylanan tüm satıcıları bulacaktır.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="8d6c3-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-116">Click OK.</span></span>
6. <span data-ttu-id="8d6c3-117">Ülke/bölge alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="8d6c3-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d6c3-118">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
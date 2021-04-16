---
title: Ana hesap kategorilerini ayarlama
description: Bu konuda, Dynamics 365 Finance'da ana hesap kategorilerinin nasıl ayarlanacağı açıklanmaktadır.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2dcaa27f20ca050d278aa378e90946b8cb40449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815128"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="7561d-103">Ana hesap kategorilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7561d-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7561d-104">Bu konuda, ana hesap kategorilerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7561d-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="7561d-105">Ana hesap kategorileri, finansal raporlamada ve Power BI'da varsayılan raporlar için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7561d-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="7561d-106">Varsayılan olarak oluşturulan ana hesap kategorileri yeniden adlandırılabilir ancak silinemez.</span><span class="sxs-lookup"><span data-stu-id="7561d-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="7561d-107">Ek hesap kategorileri raporlama ve çözümleme amacıyla oluşturulabilir ve kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7561d-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="7561d-108">Bu konu, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7561d-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="7561d-109">Bir ana hesap kategorisi oluştur</span><span class="sxs-lookup"><span data-stu-id="7561d-109">Create a main account category</span></span>
1. <span data-ttu-id="7561d-110">Gezinti bölmesinde **Modüller > Genel muhasebe > Hesap planı > Hesaplar > Ana hesap kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7561d-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="7561d-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7561d-111">Select **New**.</span></span>
3. <span data-ttu-id="7561d-112">**Ana hesap kategorisi** alanında benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="7561d-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="7561d-113">**Açıklama alanında**, ana hesap kategorisi için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="7561d-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="7561d-114">**Ana hesap türü** alanında, kategoriyle bağlantılandırılacak ana hesap türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="7561d-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="7561d-115">Ana hesapları hesap kategorisine bağla</span><span class="sxs-lookup"><span data-stu-id="7561d-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="7561d-116">**Ana hesapları bağla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7561d-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="7561d-117">Listede, **Bağlı** sütundaki kutuları işaretleyerek ana hesap kategorisine atanacak ana hesapları seçin.</span><span class="sxs-lookup"><span data-stu-id="7561d-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="7561d-118">Bu kategori finansal raporlama ve çözümleme için kullanıldığında ana hesapları bir ana hesap kategorisine atamak hesapların bakiyelerini toplar.</span><span class="sxs-lookup"><span data-stu-id="7561d-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="7561d-119">Ana hesapları seçmek için **Bağlantılı** seçeneğini işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="7561d-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="7561d-120">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7561d-120">Select **OK**.</span></span>
5. <span data-ttu-id="7561d-121">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7561d-121">Select **Yes**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
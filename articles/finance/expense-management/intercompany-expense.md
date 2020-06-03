---
title: Şirketlerarası giderler
description: Bir kuruluştaki bir tüzel kişilikte çalışan bir çalışan, aynı kuruluştaki başka bir tüzel kişilik için iş yapabilir. Bu durumda, şirketlerarası gider özelliğini, çalışanın giderini işin gerçekleştirildiği tüzel kişiliğe atamak için kullanabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390896"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="fc173-104">Şirketlerarası giderler</span><span class="sxs-lookup"><span data-stu-id="fc173-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc173-105">Bir kuruluştaki bir tüzel kişilikte çalışan bir çalışan, aynı kuruluştaki başka bir tüzel kişilik için iş yapabilir.</span><span class="sxs-lookup"><span data-stu-id="fc173-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="fc173-106">Bu durumda, şirketlerarası gider özelliğini, çalışanın giderini işin gerçekleştirildiği tüzel kişiliğe atamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fc173-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="fc173-107">Çalışanı çalıştıran tüzel kişilik, kiralayan tüzel kişilik olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="fc173-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="fc173-108">Çalışanın gider oluşturduğu tüzel kişilik, ödünç alan tüzel kişilik olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="fc173-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="fc173-109">Bir çalışan, kiralayan tüzel kişilikte farklı bir tüzel kişilik için gerçekleştiren işler için giderler oluşturmadan ve göndermeden önce, **Gider yönetimi parametreleri** sayfasında, **Şirketlerarası gider satırlarına izin ver** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fc173-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="fc173-110">Şirketlerarası giderler için vergilerin deftere nakli</span><span class="sxs-lookup"><span data-stu-id="fc173-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc173-111">Gider raporunuza borç alan (hedef) tüzel varlık yerine borç veren (kaynak) tüzel varlıkla ilişkili vergi grupları kullanmak istiyorsanız bunu, Genel muhasebe satış vergisi kurulumunda yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fc173-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="fc173-112">**Şirketlerarası vergilerin deftere nakli için tüzel varlık** Genel muhasebe parametresi **Kaynak** olarak ve **Satış vergisi vergilendirme kurallarını uygula** parametresi **Hayır** olarak ayarlandığında, borç veren tüzel varlığın vergi birleşimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc173-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="fc173-113">Aynı parametre **Hedef** olarak ayarlandığında, borç alan tüzel varlığın vergi birleşimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fc173-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="fc173-114">Amerika Birleşik Devletleri'ndeki tüzel varlıklar için parametre **Kaynak** olarak ayarlandığında, **Satış vergisi alacakları** alanı da yeni **Genel muhasebe deftere nakil grupları** sayfasında yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fc173-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="fc173-115">Muhasebe altyapısı, vergi ile ilgili muhasebe girişi için bu alandaki bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="fc173-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="fc173-116">Bu davranış, proje ile veya proje olmadan deftere nakledilen gider satırları için tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="fc173-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  

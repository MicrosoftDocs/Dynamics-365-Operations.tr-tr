---
title: Konsolidasyon işleminde tüzel kişilik hazırlama
description: Konsolidasyon sırasında, birkaç tüzel kişilik hesabı kümesinden hareketleri tek bir tüzel kişilik hesabı kümesinde birleştirebilirsiniz. Bu konuda, bir konsolidasyon için tüzel kişiliğin nasıl hazırlanacağı açıklanmaktadır.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 07988e71276c6439e392bce2087f3a8923f5f40b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230214"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="937c1-104">Konsolidasyon işleminde tüzel kişilik hazırlama</span><span class="sxs-lookup"><span data-stu-id="937c1-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="937c1-105">Konsolidasyon sırasında, birkaç tüzel kişilik hesabı kümesinden hareketleri tek bir tüzel kişilik hesabı kümesinde birleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="937c1-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="937c1-106">Bu konuda, bir konsolidasyon için tüzel kişiliğin nasıl hazırlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="937c1-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="937c1-107">Microsoft Dynamics 365 Finance için Management Reporter'ı kullanarak birden çok tüzel kişilik için mali sonuçları konsolide bir biçimde birleştirmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="937c1-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="937c1-108">Management Reporter, tüzel kişiliklerde konsolide mali raporlar oluşturmanıza, diğer kaynaklardan konsolidasyon verilerini içeri aktarmak için Excel'i kullanmanıza ve Dynamics 365 Finance'te konsolidasyon sürecini çalıştırmak zorunda kalmadan tutarları istediğiniz sayıda raporlama para birimlerine çevirmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="937c1-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="937c1-109">Konsolide tüzel kişilikten mali tablolar gibi raporları yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="937c1-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="937c1-110">Ancak, konsolide tüzel kişiliği günlük hareketler için kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="937c1-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="937c1-111">Konsolide tüzel kişilikten farklı veritabanları kullanan tüzel kişiliklerden gelen verileri konsolide edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="937c1-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="937c1-112">Bu konsolidasyon işlemine *içeri aktarma konsolidasyonu* denir.</span><span class="sxs-lookup"><span data-stu-id="937c1-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="937c1-113">Alternatif olarak, tüzel kişilikler konsolide tüzel kişilikle aynı veritabanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="937c1-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="937c1-114">Bu konsolidasyon işlemine *çevrimiçi konsolidasyon* denir.</span><span class="sxs-lookup"><span data-stu-id="937c1-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="937c1-115">Konsolide tüzel kişilik, yan kuruluşların sonuçlarını ve bakiyelerini toplar.</span><span class="sxs-lookup"><span data-stu-id="937c1-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="937c1-116">Konsolidasyon için konsolide tüzel kişilik hazırlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="937c1-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="937c1-117">**Genel muhasebe \> Kurulum \> Kuruluş \> Tüzel kişilikler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="937c1-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="937c1-118">Konsolide tüzel kişilik olacak tüzel kişiliği oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="937c1-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="937c1-119">**Finansal konsolidasyon işlemi için kullan** onay kutusunu seçin ve konsolide tüzel kişilik hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="937c1-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="937c1-120">Bu bilgileri tam olarak konsolide tüzel kişilik için mali tablolarda görünmesini istediğiniz şekilde girdiğinize emin olun.</span><span class="sxs-lookup"><span data-stu-id="937c1-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="937c1-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="937c1-121">Close the page.</span></span>
5. <span data-ttu-id="937c1-122">Sayfanın sağ üst köşesindeki alanda konsolide tüzel kişiliği seçin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="937c1-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="937c1-123">**Genel muhasebe \> Kurulum \> Kayıt defteri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="937c1-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="937c1-124">Konsolide tüzel kişilik için hesap planını, mali takvimi, muhasebe para birimini, isteğe bağlı raporlama para birimini ve varsayılan döviz kuru türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="937c1-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="937c1-125">**Genel muhasebe \> Kurulum \> Döviz \> Döviz kurları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="937c1-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="937c1-126">Yan kuruluş tüzel kişiliklerin para birimleri için ilgili dönemlerde döviz kurları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="937c1-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="937c1-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="937c1-127">Close the page.</span></span>
11. <span data-ttu-id="937c1-128">Konsolide tüzel kişiliğin yabancı para birimleri kullanan yan kuruluşları varsa şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="937c1-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="937c1-129">**Genel muhasebe \> Kurulum \> Deftere nakil \> Otomatik hareketler için hesaplar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="937c1-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="937c1-130">**Deftere nakil türü** alanında uygun bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="937c1-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="937c1-131">Tüzel kişiliğin ana tüzel kişilikle finansal veya operasyonel olarak birbirine bağımlı yabancı yan kuruluşları varsa **Konsolidasyon farkları için kar/zarar hesabı** deftere nakil türü için uygun bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="937c1-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="937c1-132">Ana tüzel kişilikten finansal ve operasyonel olarak bağımsız bir yan kuruluşu veya ana tüzel kişilikten finansal ve operasyonel olarak bağımsız olan birkaç yan kuruluşun sonuçlarını içeren bir tüzel kişiliği konsolide ediyorsanız ve verileri konsolide etmek için çeviri yöntemleri kullanıyorsanız **Konsolidasyon farkları için bakiye hesabı** deftere nakil türü için uygun bir hesap seçin.</span><span class="sxs-lookup"><span data-stu-id="937c1-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="937c1-133">**Ana hesap** alanında, yabancı para birimi yeniden değerleme ayarlamaları için kullanılacak ana hesapları seçin.</span><span class="sxs-lookup"><span data-stu-id="937c1-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="937c1-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="937c1-134">Close the page.</span></span>

    <span data-ttu-id="937c1-135">Konsolide tüzel kişiliği bir dönemin başlarında oluşturursanız konsolidasyon döneminde döviz kurları değiştikçe döviz tutarlarını yeniden değerleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="937c1-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="937c1-136">Konsolide tüzel kişilik artık **Konsolide et** periyodik işi için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="937c1-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="937c1-137">Bir içeri aktarma konsolidasyonu veya çevrimiçi konsolidasyon yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="937c1-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="937c1-138">İçeri aktarma konsolidasyonu yapmak için **Genel muhasebe \> Periyodik \> Konsolide et \> Konsolide et \[İçeri aktarma kaynağı\]**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="937c1-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="937c1-139">Çevrimiçi konsolidasyon yapmak için **Genel muhasebe \> Periyodik \> Konsolide et \> Konsolidasyon \[Çevrimiçi\]**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="937c1-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="937c1-140">Konsolidasyonu işlemeden önce, yan tüzel kişilikleri konsolidasyon için hazırlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="937c1-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="937c1-141">Daha fazla bilgi için bkz. [Konsolidasyon için bir bağlı tüzel kişilik ayarlama](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="937c1-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
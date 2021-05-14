---
title: Mali raporlama ile ilgili SSS
description: Bu konuda, diğer kullanıcıların mali raporlama ile ilgili soruları listelenmektedir.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923037"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="2dfbc-103">Mali raporlama ile ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="2dfbc-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="2dfbc-104">Bu konu, finansal raporlama hakkında sık sorulan soruların yanıtlarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="2dfbc-105">Ağaç güvenliğini kullanarak bir rapora erişimi nasıl kısıtlayabilirim?</span><span class="sxs-lookup"><span data-stu-id="2dfbc-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="2dfbc-106">Aşağıdaki örnek, ağaç güvenliğini kullanarak bir rapora erişimin nasıl kısıtlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="2dfbc-107">USMF demo şirketi, tüm Financial Reporting kullanıcılarının erişemeyeceği bir Bilanço raporuna sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="2dfbc-108">Erişimi sınırlamak için rapora yalnızca belirli kullanıcıların erişmesini sağlamak üzere tek bir rapora erişimi kısıtlamak için ağaç güvenliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="2dfbc-109">Erişimi kısıtlamak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2dfbc-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="2dfbc-110">Financial Reporter Report Designer'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="2dfbc-111">Yeni ağaç tanımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-111">Create a new tree definition.</span></span> <span data-ttu-id="2dfbc-112">**Dosya > Yeni > Ağaç Tanımı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="2dfbc-113">**Birim Güvenliği** sütununda **Özet** satırına çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="2dfbc-114">**Kullanıcılar ve Gruplar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="2dfbc-115">Bu rapora erişmesi gereken kullanıcıları veya grupları seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="2dfbc-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-116">Select **Save**.</span></span>
7. <span data-ttu-id="2dfbc-117">Rapor tanımına yeni ağaç tanımınızı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="2dfbc-118">Ağaç tanımında **Ayar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="2dfbc-119">**Raporlama birimi seçimi** altında **Tüm birimleri dahil et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="2dfbc-120">Hangi hesapların bakiyelerimle eşleşmediğini nasıl belirleyeceğim?</span><span class="sxs-lookup"><span data-stu-id="2dfbc-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="2dfbc-121">Eşleşen bakiyeleri olmayan bir raporunuz varsa her hesabı ve farklarını tanımlamak için gerçekleştirebileceğiniz adımlar burada verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="2dfbc-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="2dfbc-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="2dfbc-123">Financial Reporter Report Designer'da yeni satır tanımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="2dfbc-124">**Düzenle > Boyutlardan Satır Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="2dfbc-125">**MainAccount**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="2dfbc-126">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-126">Select **OK**.</span></span>
5. <span data-ttu-id="2dfbc-127">Satır tanımını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-127">Save the row definition.</span></span>
6. <span data-ttu-id="2dfbc-128">Yeni sütun tanımı oluşturun</span><span class="sxs-lookup"><span data-stu-id="2dfbc-128">Create a new column definition</span></span>
7. <span data-ttu-id="2dfbc-129">Yeni rapor tanımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-129">Create a new report definition.</span></span>
8. <span data-ttu-id="2dfbc-130">**Ayarlar**'ı seçin ve bu seçeneğin işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="2dfbc-131">Raporu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-131">Generate the report.</span></span> 
10. <span data-ttu-id="2dfbc-132">Raporu Microsoft Excel'e dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="2dfbc-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="2dfbc-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="2dfbc-134">Dynamics 365 Finance'te **Genel Muhasebe > Sorgular ve Raporlar > Mizan**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="2dfbc-135">Aşağıdaki parametreleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2dfbc-135">Set the following parameters:</span></span>
   - <span data-ttu-id="2dfbc-136">**Başlangıç Tarihi** - Mali yılın başlangıç tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="2dfbc-137">**Bitiş Tarihi** - Raporu oluşturduğunuz tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="2dfbc-138">**Finansal Boyut** - Bu alanı **Ana Hesap kümesi** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="2dfbc-139">**Hesapla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="2dfbc-140">Raporu Microsoft Excel'e dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="2dfbc-141">Artık Mali Raporlayıcı Excel raporundan Mizan raporuna veri kopyalayabilirsiniz ve böylece **Kapanış Bakiyesi** sütunlarını karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2dfbc-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
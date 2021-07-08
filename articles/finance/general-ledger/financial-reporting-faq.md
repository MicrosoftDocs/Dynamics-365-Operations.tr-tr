---
title: Mali raporlama ile ilgili SSS
description: Bu konuda, Mali raporlama hakkında sık sorulan bazı soruların yanıtları sağlanmaktadır.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266645"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="1fa76-103">Mali raporlama ile ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="1fa76-103">Financial reporting FAQ</span></span>

<span data-ttu-id="1fa76-104">Bu konuda, Mali raporlama hakkında sık sorulan soruların yanıtları sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1fa76-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="1fa76-105">Ağaç güvenliğini kullanarak bir rapora erişimi nasıl kısıtlayabilirim?</span><span class="sxs-lookup"><span data-stu-id="1fa76-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="1fa76-106">Aşağıdaki örnekte, ağaç güvenliği kullanılarak bir rapora erişimin nasıl kısıtlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1fa76-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="1fa76-107">USMF demo şirketi, tüm Mali raporlama kullanıcılarının erişemeyeceği bir **Bilanço** raporuna sahiptir.</span><span class="sxs-lookup"><span data-stu-id="1fa76-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="1fa76-108">Rapora yalnızca belirli kullanıcıların erişmesini sağlamak üzere tek bir rapora erişimi kısıtlamak için ağaç güvenliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1fa76-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="1fa76-109">Financial Reporter Report Designer'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1fa76-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="1fa76-110">Yeni bir ağaç tanımı oluşturmak için **Dosya \> Yeni \> Ağaç Tanımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="1fa76-111">**Birim Güvenliği** sütununda **Özet** satırına çift dokunun (veya çift tıklayın).</span><span class="sxs-lookup"><span data-stu-id="1fa76-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="1fa76-112">**Kullanıcılar ve Gruplar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="1fa76-113">Rapora erişmesi gereken kullanıcıları veya grupları seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="1fa76-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-114">Select **Save**.</span></span>
7. <span data-ttu-id="1fa76-115">Rapor tanımına yeni ağaç tanımınızı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="1fa76-116">Ağaç tanımında **Ayar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="1fa76-117">Ardından, **Raporlama birimi seçimi** altında **Tüm birimleri dahil et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="1fa76-118">Hangi hesapların bakiyelerimle eşleşmediğini nasıl belirleyeceğim?</span><span class="sxs-lookup"><span data-stu-id="1fa76-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="1fa76-119">Eşleşen bakiyeleri olmayan bir raporunuz varsa her hesabı ve farkını tanımlamak için aşağıdaki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="1fa76-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="1fa76-120">Financial Reporter Report Designer'te</span><span class="sxs-lookup"><span data-stu-id="1fa76-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="1fa76-121">Yeni bir satır tanımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1fa76-121">Create a new row definition.</span></span>
2. <span data-ttu-id="1fa76-122">**Düzenle \> Boyutlardan Satır Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="1fa76-123">**MainAccount**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="1fa76-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-124">Select **OK**.</span></span>
5. <span data-ttu-id="1fa76-125">Satır tanımını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-125">Save the row definition.</span></span>
6. <span data-ttu-id="1fa76-126">Yeni bir sütun tanımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1fa76-126">Create a new column definition.</span></span>
7. <span data-ttu-id="1fa76-127">Yeni bir rapor tanımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1fa76-127">Create a new report definition.</span></span>
8. <span data-ttu-id="1fa76-128">**Ayarlar**'ı seçin ve bu seçeneğin işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="1fa76-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="1fa76-129">Raporu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1fa76-129">Generate the report.</span></span> 
10. <span data-ttu-id="1fa76-130">Raporu Microsoft Excel'e dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="1fa76-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="1fa76-131">Dynamics 365 Finance'te</span><span class="sxs-lookup"><span data-stu-id="1fa76-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="1fa76-132">**Genel muhasebe \> Sorgular ve raporlar \> Mizan**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="1fa76-133">Aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="1fa76-133">Set the following fields:</span></span>

    - <span data-ttu-id="1fa76-134">**Başlangıç Tarihi**: Mali yılın başlangıç tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="1fa76-135">**Bitiş Tarihi**: Raporu oluşturduğunuz tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="1fa76-136">**Mali Boyut**: Bu alanı **Ana hesap kümesi** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1fa76-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="1fa76-137">**Hesapla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="1fa76-138">Raporu Excel'e dışarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="1fa76-138">Export the report to Excel.</span></span>

<span data-ttu-id="1fa76-139">Artık Financial Reporter Excel raporundan **Mizan** raporuna veri kopyalayarak **Kapanış Bakiyesi** sütunlarını karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1fa76-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="1fa76-140">Report Designer'da bir rapor tasarladığımda veya mali rapor oluşturduğumda şu iletiyi alıyorum: "Veri sağlayıcı altyapısındaki bir sorun nedeniyle işlem tamamlanamadı."</span><span class="sxs-lookup"><span data-stu-id="1fa76-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="1fa76-141">Nasıl yanıt vermeliyim?</span><span class="sxs-lookup"><span data-stu-id="1fa76-141">How should I respond?</span></span>

<span data-ttu-id="1fa76-142">Bu ileti, Mali raporlama kullanılırken sistem veri reyonunda mali meta verileri almaya çalıştığında bir sorun oluştuğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fa76-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="1fa76-143">Bu sorunu çözmenin iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="1fa76-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="1fa76-144">Report Designer'da **Araçlar \> Tümleştirme durumu**'na giderek verilerin tümleştirme durumunu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="1fa76-145">Tümleştirme tamamlanmamışsa tamamlanmasını bekleyin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="1fa76-146">Ardından, iletiyi aldığınızda yaptığınız işlemi yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="1fa76-147">Sorunu tanımlamak ve üzerinde çalışmak için Destek ile iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="1fa76-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="1fa76-148">Sistemde tutarsız veriler olabilir.</span><span class="sxs-lookup"><span data-stu-id="1fa76-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="1fa76-149">Destek mühendisleri, bu sorunu sunucuda tanımlamanıza ve güncelleştirme gerektirebilecek belirli verileri bulmanıza yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1fa76-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

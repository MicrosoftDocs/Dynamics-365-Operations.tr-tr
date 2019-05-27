---
title: ER seçili veri kaynaklarına veri modeli eşle
description: Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının, Elektronik raporlama (ER) veri modelini seçili Dynamics 365 for Finance and Operations, Enterprise edition veri kaynaklarıyla nasıl eşleyeceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551242"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="a6a1c-103">ER seçili veri kaynaklarına veri modeli eşle</span><span class="sxs-lookup"><span data-stu-id="a6a1c-103">ER Map data model to selected data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a6a1c-104">Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının, Elektronik raporlama (ER) veri modelini seçili Dynamics 365 for Finance and Operations, Enterprise edition veri kaynaklarıyla nasıl eşleyeceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="a6a1c-105">Bu model eşleme, daha sonra elektronik ödeme belgeleri yönetmek için kullanılacak biçim yapılandırmasında bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="a6a1c-106">Bu örnekte, Litware, Inc örnek şirketi için bir veri modelini veri kaynaklarına eşleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="a6a1c-107">Bu adımları tamamlamak için ilk önce "Model eşleme için veri kaynaklarını seçin" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="a6a1c-108">ER yapılandırmaları ağacını açın</span><span class="sxs-lookup"><span data-stu-id="a6a1c-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="a6a1c-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a6a1c-110">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="a6a1c-111">Oluşturulan model eşlemesini seçin</span><span class="sxs-lookup"><span data-stu-id="a6a1c-111">Select created model mapping</span></span>
1. <span data-ttu-id="a6a1c-112">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="a6a1c-113">Model yapılandırması "Ödemeler (Basitleştirilmiş model)" önceden oluşturulmuş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="a6a1c-114">Aksi durumda, bu aşamada durun ve "Seçilen etki alanının veri modeli ile yeni bir yapılandırma oluşturma" görev kılavuzunu tamamladıktan sonra devam edin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="a6a1c-115">Model tasarımcısı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-115">Click Model designer.</span></span>
3. <span data-ttu-id="a6a1c-116">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="a6a1c-117">'CT eşleme' kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="a6a1c-118">CT eşleme</span><span class="sxs-lookup"><span data-stu-id="a6a1c-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="a6a1c-119">Oluşturulan veri kaynaklarını, veri modeli öğelerine bağlayın</span><span class="sxs-lookup"><span data-stu-id="a6a1c-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="a6a1c-120">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-120">Click Designer.</span></span>
2. <span data-ttu-id="a6a1c-121">Ağaç altından 'İşleme tarihi ve saati (ProcessingDateTime)' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="a6a1c-122">Ağaçta 'Processing date(ProcessingDateTime)' seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="a6a1c-123">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-123">Click Bind.</span></span>
5. <span data-ttu-id="a6a1c-124">Ağaçta 'Payment message identification(MessageIdentification)' seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="a6a1c-125">Ağaçta, 'Hareketler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="a6a1c-126">Ağaçta 'Transactions\Journal batch number(JournalNum)' seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="a6a1c-127">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-127">Click Bind.</span></span>
9. <span data-ttu-id="a6a1c-128">Ağaçta 'Ödemeler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="a6a1c-129">Ağaçta, 'Hareketler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="a6a1c-130">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-130">Click Bind.</span></span>
12. <span data-ttu-id="a6a1c-131">Ağaçta 'Payments= Transactions' genişletin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="a6a1c-132">Ağaçta 'Payments= Transactions\Creditor' genişletin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="a6a1c-133">Ağaçta 'Payments= Transactions\Creditor\Account' genişletin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="a6a1c-134">Ağaçta 'Payments= Transactions\Creditor\Account\Currency code(Currency)' seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="a6a1c-135">Ağaçta genişletin 'Transactions\vendBankAccountInTransactionCompany()'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="a6a1c-136">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="a6a1c-137">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-137">Click Bind.</span></span>
19. <span data-ttu-id="a6a1c-138">Ağaçta seçin 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="a6a1c-139">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="a6a1c-140">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-140">Click Bind.</span></span>
22. <span data-ttu-id="a6a1c-141">Ağaçta seçin 'Payments= Transactions\Creditor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="a6a1c-142">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="a6a1c-143">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-143">Click Bind.</span></span>
25. <span data-ttu-id="a6a1c-144">Ağaçta seçin 'Payments= Transactions\Creditor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="a6a1c-145">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="a6a1c-146">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="a6a1c-147">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-147">Click Bind.</span></span>
29. <span data-ttu-id="a6a1c-148">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="a6a1c-149">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="a6a1c-150">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-150">Click Bind.</span></span>
32. <span data-ttu-id="a6a1c-151">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="a6a1c-152">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="a6a1c-153">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-153">Click Bind.</span></span>
35. <span data-ttu-id="a6a1c-154">Ağaçta seçin 'Payments= Transactions\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="a6a1c-155">Ağaçta genişletin 'Transactions\findVendTable()'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="a6a1c-156">Ağaç altından 'Transactions\findVendTable()\name()' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="a6a1c-157">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-157">Click Bind.</span></span>
39. <span data-ttu-id="a6a1c-158">Ağaçta seçin 'Payments= Transactions\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="a6a1c-159">Ağaçta genişletin 'Transactions\>Relations'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="a6a1c-160">Ağaçta genişletin 'Transactions\>Relations\Currency table(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="a6a1c-161">Ağaçta seçin 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="a6a1c-162">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-162">Click Bind.</span></span>
44. <span data-ttu-id="a6a1c-163">Ağaçta genişletin 'Payments= Transactions\Debtor'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="a6a1c-164">Ağaçta genişletin 'Payments= Transactions\Debtor\Account'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="a6a1c-165">Ağaçta seçin 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="a6a1c-166">Ağaçta seçin 'Bank Account(BankAccount)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="a6a1c-167">Ağaçta genişletin 'Bank Account(BankAccount)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="a6a1c-168">Ağaçta seçin 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="a6a1c-169">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-169">Click Bind.</span></span>
51. <span data-ttu-id="a6a1c-170">Ağaçta seçin 'Bank Account(BankAccount)\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="a6a1c-171">Ağaçta seçin 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="a6a1c-172">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-172">Click Bind.</span></span>
54. <span data-ttu-id="a6a1c-173">Ağaçta seçin 'Payments= Transactions\Debtor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="a6a1c-174">Ağaçta seçin 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="a6a1c-175">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-175">Click Bind.</span></span>
57. <span data-ttu-id="a6a1c-176">Ağaçta genişletin 'Payments= Transactions\Debtor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="a6a1c-177">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="a6a1c-178">Ağaçta seçin 'Bank Account(BankAccount)\Name'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="a6a1c-179">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-179">Click Bind.</span></span>
61. <span data-ttu-id="a6a1c-180">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="a6a1c-181">Ağaçta seçin 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="a6a1c-182">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-182">Click Bind.</span></span>
64. <span data-ttu-id="a6a1c-183">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="a6a1c-184">Ağaçta seçin 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="a6a1c-185">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-185">Click Bind.</span></span>
67. <span data-ttu-id="a6a1c-186">Ağaçta seçin 'Payments= Transactions\Debtor\Name'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="a6a1c-187">Ağaçta seçin 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="a6a1c-188">Ağaçta genişletin 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="a6a1c-189">Ağaçta seçin 'Company information(Company)\Name'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="a6a1c-190">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-190">Click Bind.</span></span>
72. <span data-ttu-id="a6a1c-191">Ağaçta seçin 'Payments= Transactions\Description'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="a6a1c-192">Ağaçta seçin 'Transactions\Description(Txt)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="a6a1c-193">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-193">Click Bind.</span></span>
75. <span data-ttu-id="a6a1c-194">Ağaçta seçin 'Payments= Transactions\End to end identification code(End2EndID)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="a6a1c-195">Ağaçta, 'Transactions\$$EndToEndID' seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="a6a1c-196">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-196">Click Bind.</span></span>
78. <span data-ttu-id="a6a1c-197">Ağaçta seçin 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="a6a1c-198">Ağaçta, 'Transactions\$Amount' seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="a6a1c-199">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-199">Click Bind.</span></span>
81. <span data-ttu-id="a6a1c-200">Ağaçta seçin 'Payments= Transactions\Transaction date(TransactionDate)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="a6a1c-201">Ağaçta seçin 'Transactions\Date(TransDate)'.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="a6a1c-202">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="a6a1c-203">Oluşturulan eşleme doğrulama</span><span class="sxs-lookup"><span data-stu-id="a6a1c-203">Validate created mapping</span></span>
1. <span data-ttu-id="a6a1c-204">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-204">Click Validate.</span></span>
    * <span data-ttu-id="a6a1c-205">Tüm bağlamaların doğru yapıldığından emin olmak için yeni eşlemeyi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="a6a1c-206">Hata Listesi bölümünü genişletmek veya daraltmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="a6a1c-207">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-207">Click Save.</span></span>
4. <span data-ttu-id="a6a1c-208">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-208">Close the page.</span></span>
5. <span data-ttu-id="a6a1c-209">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-209">Close the page.</span></span>
6. <span data-ttu-id="a6a1c-210">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="a6a1c-211">Model yapılandırmasının geçerli sürümünün durumunu değiştirin</span><span class="sxs-lookup"><span data-stu-id="a6a1c-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="a6a1c-212">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-212">Click Change status.</span></span>
    * <span data-ttu-id="a6a1c-213">Ödeme biçimi tasarımında kullanılabilmesi için tasarlanan model yapılandırmasının durumunu Taslak'tan Tamamlandı'ya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="a6a1c-214">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-214">Click Complete.</span></span>
    * <span data-ttu-id="a6a1c-215">Tamamlandı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-215">Select Complete.</span></span>  
3. <span data-ttu-id="a6a1c-216">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a6a1c-217">Örneğin, "sürüm 1".</span><span class="sxs-lookup"><span data-stu-id="a6a1c-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="a6a1c-218">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-218">Click OK.</span></span>
5. <span data-ttu-id="a6a1c-219">Geçerli yapılandırmanın tamamlanmış sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="a6a1c-220">Oluşturulan yapılandırmanın tamamlanmış sürüm 1 olarak kaydedildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a6a1c-220">Note that the created configuration is saved as completed version 1.</span></span>  


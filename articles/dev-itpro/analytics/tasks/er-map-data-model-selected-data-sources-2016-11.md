--- 
title: "ER seçili veri kaynaklarına veri modeli eşle"
description: "Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının, Elektronik raporlama (ER) veri modelini seçili , Dynamics 365 for Finance and Operations, Enterprise edition veri kaynaklarıyla nasıl eşleyeceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="444b8-103">ER seçili veri kaynaklarına veri modeli eşle</span><span class="sxs-lookup"><span data-stu-id="444b8-103">ER Map data model to selected data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="444b8-104">Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının, Elektronik raporlama (ER) veri modelini seçili , Dynamics 365 for Finance and Operations, Enterprise edition veri kaynaklarıyla nasıl eşleyeceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="444b8-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="444b8-105">Bu model eşleme, daha sonra elektronik ödeme belgeleri yönetmek için kullanılacak biçim yapılandırmasında bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="444b8-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="444b8-106">Bu örnekte, Litware, Inc örnek şirketi için bir veri modelini veri kaynaklarına eşleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="444b8-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="444b8-107">Bu adımları tamamlamak için ilk önce "Model eşleme için veri kaynaklarını seçin" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="444b8-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="444b8-108">ER yapılandırmaları ağacını açın</span><span class="sxs-lookup"><span data-stu-id="444b8-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="444b8-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="444b8-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="444b8-110">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="444b8-111">Oluşturulan model eşlemesini seçin</span><span class="sxs-lookup"><span data-stu-id="444b8-111">Select created model mapping</span></span>
1. <span data-ttu-id="444b8-112">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="444b8-113">Model yapılandırması "Ödemeler (Basitleştirilmiş model)" önceden oluşturulmuş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="444b8-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="444b8-114">Aksi durumda, bu aşamada durun ve "Seçilen etki alanının veri modeli ile yeni bir yapılandırma oluşturma" görev kılavuzunu tamamladıktan sonra devam edin.</span><span class="sxs-lookup"><span data-stu-id="444b8-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="444b8-115">Model tasarımcısı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-115">Click Model designer.</span></span>
3. <span data-ttu-id="444b8-116">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="444b8-117">'CT eşleme' kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="444b8-118">CT eşleme</span><span class="sxs-lookup"><span data-stu-id="444b8-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="444b8-119">Oluşturulan veri kaynaklarını, veri modeli öğelerine bağlayın</span><span class="sxs-lookup"><span data-stu-id="444b8-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="444b8-120">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="444b8-120">Click Designer.</span></span>
2. <span data-ttu-id="444b8-121">Ağaç altından 'İşleme tarihi ve saati (ProcessingDateTime)' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="444b8-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="444b8-122">Ağaçta 'Processing date(ProcessingDateTime)' seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="444b8-123">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-123">Click Bind.</span></span>
5. <span data-ttu-id="444b8-124">Ağaçta 'Payment message identification(MessageIdentification)' seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="444b8-125">Ağaçta, 'Hareketler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="444b8-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="444b8-126">Ağaçta 'Transactions\Journal batch number(JournalNum)' seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="444b8-127">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-127">Click Bind.</span></span>
9. <span data-ttu-id="444b8-128">Ağaçta 'Ödemeler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="444b8-129">Ağaçta, 'Hareketler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="444b8-130">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-130">Click Bind.</span></span>
12. <span data-ttu-id="444b8-131">Ağaçta 'Payments= Transactions' genişletin.</span><span class="sxs-lookup"><span data-stu-id="444b8-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="444b8-132">Ağaçta 'Payments= Transactions\Creditor' genişletin.</span><span class="sxs-lookup"><span data-stu-id="444b8-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="444b8-133">Ağaçta 'Payments= Transactions\Creditor\Account' genişletin.</span><span class="sxs-lookup"><span data-stu-id="444b8-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="444b8-134">Ağaçta 'Payments= Transactions\Creditor\Account\Currency code(Currency)' seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="444b8-135">Ağaçta genişletin 'Transactions\vendBankAccountInTransactionCompany()'.</span><span class="sxs-lookup"><span data-stu-id="444b8-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="444b8-136">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="444b8-137">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-137">Click Bind.</span></span>
19. <span data-ttu-id="444b8-138">Ağaçta seçin 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="444b8-139">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="444b8-140">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-140">Click Bind.</span></span>
22. <span data-ttu-id="444b8-141">Ağaçta seçin 'Payments= Transactions\Creditor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="444b8-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="444b8-142">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="444b8-143">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-143">Click Bind.</span></span>
25. <span data-ttu-id="444b8-144">Ağaçta seçin 'Payments= Transactions\Creditor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="444b8-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="444b8-145">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="444b8-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="444b8-146">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span><span class="sxs-lookup"><span data-stu-id="444b8-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="444b8-147">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-147">Click Bind.</span></span>
29. <span data-ttu-id="444b8-148">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="444b8-149">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="444b8-150">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-150">Click Bind.</span></span>
32. <span data-ttu-id="444b8-151">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="444b8-152">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="444b8-153">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-153">Click Bind.</span></span>
35. <span data-ttu-id="444b8-154">Ağaçta seçin 'Payments= Transactions\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="444b8-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="444b8-155">Ağaçta genişletin 'Transactions\findVendTable()'.</span><span class="sxs-lookup"><span data-stu-id="444b8-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="444b8-156">Ağaç altından 'Transactions\findVendTable()\name()' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="444b8-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="444b8-157">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-157">Click Bind.</span></span>
39. <span data-ttu-id="444b8-158">Ağaçta seçin 'Payments= Transactions\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="444b8-159">Ağaçta genişletin 'Transactions\>Relations'.</span><span class="sxs-lookup"><span data-stu-id="444b8-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="444b8-160">Ağaçta genişletin 'Transactions\>Relations\Currency table(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="444b8-161">Ağaçta seçin 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="444b8-162">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-162">Click Bind.</span></span>
44. <span data-ttu-id="444b8-163">Ağaçta genişletin 'Payments= Transactions\Debtor'.</span><span class="sxs-lookup"><span data-stu-id="444b8-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="444b8-164">Ağaçta genişletin 'Payments= Transactions\Debtor\Account'.</span><span class="sxs-lookup"><span data-stu-id="444b8-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="444b8-165">Ağaçta seçin 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="444b8-166">Ağaçta seçin 'Bank Account(BankAccount)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="444b8-167">Ağaçta genişletin 'Bank Account(BankAccount)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="444b8-168">Ağaçta seçin 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="444b8-169">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-169">Click Bind.</span></span>
51. <span data-ttu-id="444b8-170">Ağaçta seçin 'Bank Account(BankAccount)\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="444b8-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="444b8-171">Ağaçta seçin 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="444b8-172">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-172">Click Bind.</span></span>
54. <span data-ttu-id="444b8-173">Ağaçta seçin 'Payments= Transactions\Debtor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="444b8-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="444b8-174">Ağaçta seçin 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="444b8-175">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-175">Click Bind.</span></span>
57. <span data-ttu-id="444b8-176">Ağaçta genişletin 'Payments= Transactions\Debtor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="444b8-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="444b8-177">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="444b8-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="444b8-178">Ağaçta seçin 'Bank Account(BankAccount)\Name'.</span><span class="sxs-lookup"><span data-stu-id="444b8-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="444b8-179">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-179">Click Bind.</span></span>
61. <span data-ttu-id="444b8-180">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="444b8-181">Ağaçta seçin 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="444b8-182">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="444b8-182">Click Bind.</span></span>
64. <span data-ttu-id="444b8-183">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="444b8-184">Ağaçta seçin 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="444b8-185">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-185">Click Bind.</span></span>
67. <span data-ttu-id="444b8-186">Ağaçta seçin 'Payments= Transactions\Debtor\Name'.</span><span class="sxs-lookup"><span data-stu-id="444b8-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="444b8-187">Ağaçta seçin 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="444b8-188">Ağaçta genişletin 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="444b8-189">Ağaçta seçin 'Company information(Company)\Name'.</span><span class="sxs-lookup"><span data-stu-id="444b8-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="444b8-190">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-190">Click Bind.</span></span>
72. <span data-ttu-id="444b8-191">Ağaçta seçin 'Payments= Transactions\Description'.</span><span class="sxs-lookup"><span data-stu-id="444b8-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="444b8-192">Ağaçta seçin 'Transactions\Description(Txt)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="444b8-193">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-193">Click Bind.</span></span>
75. <span data-ttu-id="444b8-194">Ağaçta seçin 'Payments= Transactions\End to end identification code(End2EndID)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="444b8-195">Ağaçta, 'Transactions\$$EndToEndID' seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="444b8-196">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-196">Click Bind.</span></span>
78. <span data-ttu-id="444b8-197">Ağaçta seçin 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="444b8-198">Ağaçta, 'Transactions\$Amount' seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="444b8-199">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-199">Click Bind.</span></span>
81. <span data-ttu-id="444b8-200">Ağaçta seçin 'Payments= Transactions\Transaction date(TransactionDate)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="444b8-201">Ağaçta seçin 'Transactions\Date(TransDate)'.</span><span class="sxs-lookup"><span data-stu-id="444b8-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="444b8-202">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="444b8-203">Oluşturulan eşleme doğrulama</span><span class="sxs-lookup"><span data-stu-id="444b8-203">Validate created mapping</span></span>
1. <span data-ttu-id="444b8-204">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-204">Click Validate.</span></span>
    * <span data-ttu-id="444b8-205">Tüm bağlamaların doğru yapıldığından emin olmak için yeni eşlemeyi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="444b8-206">Hata Listesi bölümünü genişletmek veya daraltmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="444b8-207">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-207">Click Save.</span></span>
4. <span data-ttu-id="444b8-208">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="444b8-208">Close the page.</span></span>
5. <span data-ttu-id="444b8-209">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="444b8-209">Close the page.</span></span>
6. <span data-ttu-id="444b8-210">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="444b8-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="444b8-211">Model yapılandırmasının geçerli sürümünün durumunu değiştirin</span><span class="sxs-lookup"><span data-stu-id="444b8-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="444b8-212">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-212">Click Change status.</span></span>
    * <span data-ttu-id="444b8-213">Ödeme biçimi tasarımında kullanılabilmesi için tasarlanan model yapılandırmasının durumunu Taslak'tan Tamamlandı'ya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="444b8-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="444b8-214">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-214">Click Complete.</span></span>
    * <span data-ttu-id="444b8-215">Tamamlandı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-215">Select Complete.</span></span>  
3. <span data-ttu-id="444b8-216">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="444b8-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="444b8-217">Örneğin, "sürüm 1".</span><span class="sxs-lookup"><span data-stu-id="444b8-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="444b8-218">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-218">Click OK.</span></span>
5. <span data-ttu-id="444b8-219">Geçerli yapılandırmanın tamamlanmış sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="444b8-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="444b8-220">Oluşturulan yapılandırmanın tamamlanmış sürüm 1 olarak kaydedildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="444b8-220">Note that the created configuration is saved as completed version 1.</span></span>  



---
title: ER seçili veri kaynaklarına veri modeli eşle
description: Bu konuda, Elektronik raporlama (ER) veri modelinin seçili Microsoft Dynamics 365 Finance veri kaynaklarıyla nasıl eşleneceğini açıklanmaktadır.
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e2ba94c9ec3ecc33f0c697d9f18f763749e4ba1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093760"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="161bb-103">ER seçili veri kaynaklarına veri modeli eşle</span><span class="sxs-lookup"><span data-stu-id="161bb-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="161bb-104">Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının, Elektronik raporlama (ER) veri modelini seçili veri kaynaklarıyla nasıl eşleyeceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="161bb-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="161bb-105">Bu model eşleme, daha sonra elektronik ödeme belgeleri yönetmek için kullanılacak biçim yapılandırmasında bir veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="161bb-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="161bb-106">Bu örnekte, Litware, Inc örnek şirketi için bir veri modelini veri kaynaklarına eşleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="161bb-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="161bb-107">Bu adımları tamamlamak için ilk önce "Model eşleme için veri kaynaklarını seçin" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="161bb-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="161bb-108">ER yapılandırmaları ağacını açın</span><span class="sxs-lookup"><span data-stu-id="161bb-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="161bb-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="161bb-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="161bb-110">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="161bb-111">Oluşturulan model eşlemesini seçin</span><span class="sxs-lookup"><span data-stu-id="161bb-111">Select created model mapping</span></span>
1. <span data-ttu-id="161bb-112">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="161bb-113">Model yapılandırması "Ödemeler (Basitleştirilmiş model)" önceden oluşturulmuş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="161bb-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="161bb-114">Aksi durumda, bu aşamada durun ve "Seçilen etki alanının veri modeli ile yeni bir yapılandırma oluşturma" görev kılavuzunu tamamladıktan sonra devam edin.</span><span class="sxs-lookup"><span data-stu-id="161bb-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="161bb-115">Model tasarımcısı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-115">Click Model designer.</span></span>
3. <span data-ttu-id="161bb-116">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="161bb-117">'CT eşleme' kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="161bb-118">CT eşleme</span><span class="sxs-lookup"><span data-stu-id="161bb-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="161bb-119">Oluşturulan veri kaynaklarını, veri modeli öğelerine bağlayın</span><span class="sxs-lookup"><span data-stu-id="161bb-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="161bb-120">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="161bb-120">Click Designer.</span></span>
2. <span data-ttu-id="161bb-121">Ağaç altından 'İşleme tarihi ve saati (ProcessingDateTime)' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="161bb-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="161bb-122">Ağaçta 'Processing date(ProcessingDateTime)' seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="161bb-123">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-123">Click Bind.</span></span>
5. <span data-ttu-id="161bb-124">Ağaçta 'Payment message identification(MessageIdentification)' seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="161bb-125">Ağaçta, 'Hareketler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="161bb-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="161bb-126">Ağaçta 'Transactions\Journal batch number(JournalNum)' seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="161bb-127">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-127">Click Bind.</span></span>
9. <span data-ttu-id="161bb-128">Ağaçta 'Ödemeler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="161bb-129">Ağaçta, 'Hareketler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="161bb-130">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-130">Click Bind.</span></span>
12. <span data-ttu-id="161bb-131">Ağaçta 'Payments= Transactions' genişletin.</span><span class="sxs-lookup"><span data-stu-id="161bb-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="161bb-132">Ağaçta 'Payments= Transactions\Creditor' genişletin.</span><span class="sxs-lookup"><span data-stu-id="161bb-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="161bb-133">Ağaçta 'Payments= Transactions\Creditor\Account' genişletin.</span><span class="sxs-lookup"><span data-stu-id="161bb-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="161bb-134">Ağaçta 'Payments= Transactions\Creditor\Account\Currency code(Currency)' seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="161bb-135">Ağaçta genişletin 'Transactions\vendBankAccountInTransactionCompany()'.</span><span class="sxs-lookup"><span data-stu-id="161bb-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="161bb-136">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="161bb-137">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-137">Click Bind.</span></span>
19. <span data-ttu-id="161bb-138">Ağaçta seçin 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="161bb-139">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="161bb-140">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-140">Click Bind.</span></span>
22. <span data-ttu-id="161bb-141">Ağaçta seçin 'Payments= Transactions\Creditor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="161bb-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="161bb-142">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="161bb-143">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-143">Click Bind.</span></span>
25. <span data-ttu-id="161bb-144">Ağaçta seçin 'Payments= Transactions\Creditor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="161bb-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="161bb-145">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="161bb-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="161bb-146">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span><span class="sxs-lookup"><span data-stu-id="161bb-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="161bb-147">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-147">Click Bind.</span></span>
29. <span data-ttu-id="161bb-148">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="161bb-149">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="161bb-150">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-150">Click Bind.</span></span>
32. <span data-ttu-id="161bb-151">Ağaçta seçin 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="161bb-152">Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="161bb-153">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-153">Click Bind.</span></span>
35. <span data-ttu-id="161bb-154">Ağaçta seçin 'Payments= Transactions\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="161bb-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="161bb-155">Ağaçta genişletin 'Transactions\findVendTable()'.</span><span class="sxs-lookup"><span data-stu-id="161bb-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="161bb-156">Ağaç altından 'Transactions\findVendTable()\name()' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="161bb-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="161bb-157">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-157">Click Bind.</span></span>
39. <span data-ttu-id="161bb-158">Ağaçta seçin 'Payments= Transactions\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="161bb-159">Ağaçta genişletin 'Transactions\>Relations'.</span><span class="sxs-lookup"><span data-stu-id="161bb-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="161bb-160">Ağaçta genişletin 'Transactions\>Relations\Currency table(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="161bb-161">Ağaçta seçin 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="161bb-162">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-162">Click Bind.</span></span>
44. <span data-ttu-id="161bb-163">Ağaçta genişletin 'Payments= Transactions\Debtor'.</span><span class="sxs-lookup"><span data-stu-id="161bb-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="161bb-164">Ağaçta genişletin 'Payments= Transactions\Debtor\Account'.</span><span class="sxs-lookup"><span data-stu-id="161bb-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="161bb-165">Ağaçta seçin 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="161bb-166">Ağaçta seçin 'Bank Account(BankAccount)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="161bb-167">Ağaçta genişletin 'Bank Account(BankAccount)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="161bb-168">Ağaçta seçin 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="161bb-169">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-169">Click Bind.</span></span>
51. <span data-ttu-id="161bb-170">Ağaçta seçin 'Bank Account(BankAccount)\IBAN'.</span><span class="sxs-lookup"><span data-stu-id="161bb-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="161bb-171">Ağaçta seçin 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="161bb-172">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-172">Click Bind.</span></span>
54. <span data-ttu-id="161bb-173">Ağaçta seçin 'Payments= Transactions\Debtor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="161bb-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="161bb-174">Ağaçta seçin 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="161bb-175">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-175">Click Bind.</span></span>
57. <span data-ttu-id="161bb-176">Ağaçta genişletin 'Payments= Transactions\Debtor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="161bb-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="161bb-177">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="161bb-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="161bb-178">Ağaçta seçin 'Bank Account(BankAccount)\Name'.</span><span class="sxs-lookup"><span data-stu-id="161bb-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="161bb-179">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-179">Click Bind.</span></span>
61. <span data-ttu-id="161bb-180">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="161bb-181">Ağaçta seçin 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="161bb-182">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="161bb-182">Click Bind.</span></span>
64. <span data-ttu-id="161bb-183">Ağaçta seçin 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="161bb-184">Ağaçta seçin 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="161bb-185">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-185">Click Bind.</span></span>
67. <span data-ttu-id="161bb-186">Ağaçta seçin 'Payments= Transactions\Debtor\Name'.</span><span class="sxs-lookup"><span data-stu-id="161bb-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="161bb-187">Ağaçta seçin 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="161bb-188">Ağaçta genişletin 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="161bb-189">Ağaçta seçin 'Company information(Company)\Name'.</span><span class="sxs-lookup"><span data-stu-id="161bb-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="161bb-190">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-190">Click Bind.</span></span>
72. <span data-ttu-id="161bb-191">Ağaçta seçin 'Payments= Transactions\Description'.</span><span class="sxs-lookup"><span data-stu-id="161bb-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="161bb-192">Ağaçta seçin 'Transactions\Description(Txt)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="161bb-193">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-193">Click Bind.</span></span>
75. <span data-ttu-id="161bb-194">Ağaçta seçin 'Payments= Transactions\End to end identification code(End2EndID)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="161bb-195">Ağaçta, 'Transactions\$$EndToEndID' seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="161bb-196">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-196">Click Bind.</span></span>
78. <span data-ttu-id="161bb-197">Ağaçta seçin 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="161bb-198">Ağaçta, 'Transactions\$Amount' seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="161bb-199">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-199">Click Bind.</span></span>
81. <span data-ttu-id="161bb-200">Ağaçta seçin 'Payments= Transactions\Transaction date(TransactionDate)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="161bb-201">Ağaçta seçin 'Transactions\Date(TransDate)'.</span><span class="sxs-lookup"><span data-stu-id="161bb-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="161bb-202">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="161bb-203">Oluşturulan eşleme doğrulama</span><span class="sxs-lookup"><span data-stu-id="161bb-203">Validate created mapping</span></span>
1. <span data-ttu-id="161bb-204">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-204">Click Validate.</span></span>
    * <span data-ttu-id="161bb-205">Tüm bağlamaların doğru yapıldığından emin olmak için yeni eşlemeyi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="161bb-206">Hata Listesi bölümünü genişletmek veya daraltmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="161bb-207">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-207">Click Save.</span></span>
4. <span data-ttu-id="161bb-208">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="161bb-208">Close the page.</span></span>
5. <span data-ttu-id="161bb-209">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="161bb-209">Close the page.</span></span>
6. <span data-ttu-id="161bb-210">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="161bb-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="161bb-211">Model yapılandırmasının geçerli sürümünün durumunu değiştirin</span><span class="sxs-lookup"><span data-stu-id="161bb-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="161bb-212">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-212">Click Change status.</span></span>
    * <span data-ttu-id="161bb-213">Ödeme biçimi tasarımında kullanılabilmesi için tasarlanan model yapılandırmasının durumunu Taslak'tan Tamamlandı'ya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="161bb-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="161bb-214">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-214">Click Complete.</span></span>
    * <span data-ttu-id="161bb-215">Tamamlandı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-215">Select Complete.</span></span>  
3. <span data-ttu-id="161bb-216">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="161bb-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="161bb-217">Örneğin, "sürüm 1".</span><span class="sxs-lookup"><span data-stu-id="161bb-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="161bb-218">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-218">Click OK.</span></span>
5. <span data-ttu-id="161bb-219">Geçerli yapılandırmanın tamamlanmış sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="161bb-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="161bb-220">Oluşturulan yapılandırmanın tamamlanmış sürüm 1 olarak kaydedildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="161bb-220">Note that the created configuration is saved as completed version 1.</span></span>  


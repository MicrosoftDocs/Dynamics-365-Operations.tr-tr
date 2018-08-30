--- 
title: "Elektronik raporlama (ER) veri modellerini seçili veri kaynaklarına eşleme"
description: "Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının, Elektronik raporlama (ER) veri modelini seçili , Dynamics 365 for Finance and Operations, Enterprise edition (Kasım 2016) veri kaynaklarıyla nasıl eşleyeceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: f347c19d940330c830509be4d11127f9e3324deb
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="map-electronic-reporting-er-data-models-to-selected-data-sources"></a>Elektronik raporlama (ER) veri modellerini seçili veri kaynaklarına eşleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının, Elektronik raporlama (ER) veri modelini seçili , Dynamics 365 for Finance and Operations veri kaynaklarıyla nasıl eşleyeceğini açıklar. Bu model eşleme, daha sonra elektronik ödeme belgeleri yönetmek için kullanılacak biçim yapılandırmasında bir veri kaynağı olarak kullanılır. Bu örnekte, Litware, Inc örnek şirketi için bir veri modelini veri kaynaklarına eşleyeceksiniz. Bu adımları tamamlamak için ilk önce "Model eşleme için veri kaynaklarını seçin" yordamındaki adımları tamamlamanız gerekir.


## <a name="open-er-configurations-tree"></a>ER yapılandırmaları ağacını açın
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Yapılandırmalar'a tıklayın.

## <a name="select-created-model-mapping"></a>Oluşturulan model eşlemesini seçin
1. Ağaçta, 'Ödemeler (Basitleştirilmiş model)' seçin.
    * Model yapılandırması "Ödemeler (Basitleştirilmiş model)" önceden oluşturulmuş olduğundan emin olun. Aksi durumda, bu aşamada durun ve "Seçilen etki alanının veri modeli ile yeni bir yapılandırma oluşturma" görev kılavuzunu tamamladıktan sonra devam edin.  
2. Model tasarımcısı'na tıklayın.
3. Modeli veri kaynağına eşle'yi tıklayın.
4. 'CT eşleme' kaydını seçin.
    * CT eşleme  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Oluşturulan veri kaynaklarını, veri modeli öğelerine bağlayın
1. Tasarımcı'yı tıklatın.
2. Ağaç altından 'İşleme tarihi ve saati (ProcessingDateTime)' seçimini yapın.
3. Ağaçta 'Processing date(ProcessingDateTime)' seçin.
4. Bağla'ya tıklayın.
5. Ağaçta 'Payment message identification(MessageIdentification)' seçin.
6. Ağaçta, 'Hareketler'i genişletin.
7. Ağaçta 'Transactions\Journal batch number(JournalNum)' seçin.
8. Bağla'ya tıklayın.
9. Ağaçta 'Ödemeler'i seçin.
10. Ağaçta, 'Hareketler'i seçin.
11. Bağla'ya tıklayın.
12. Ağaçta 'Payments= Transactions' genişletin.
13. Ağaçta 'Payments= Transactions\Creditor' genişletin.
14. Ağaçta 'Payments= Transactions\Creditor\Account' genişletin.
15. Ağaçta 'Payments= Transactions\Creditor\Account\Currency code(Currency)' seçin.
16. Ağaçta genişletin 'Transactions\vendBankAccountInTransactionCompany()'.
17. Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.
18. Bağla'ya tıklayın.
19. Ağaçta seçin 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.
20. Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.
21. Bağla'ya tıklayın.
22. Ağaçta seçin 'Payments= Transactions\Creditor\Account\Number'.
23. Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.
24. Bağla'ya tıklayın.
25. Ağaçta seçin 'Payments= Transactions\Creditor\Agent'.
26. Ağaçta seçin 'Payments= Transactions\Creditor\Agent\Name'.
27. Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Name'.
28. Bağla'ya tıklayın.
29. Ağaçta seçin 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.
30. Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.
31. Bağla'ya tıklayın.
32. Ağaçta seçin 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.
33. Ağaçta seçin 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.
34. Bağla'ya tıklayın.
35. Ağaçta seçin 'Payments= Transactions\Creditor\Name'.
36. Ağaçta genişletin 'Transactions\findVendTable()'.
37. Ağaç altından 'Transactions\findVendTable()\name()' seçimini yapın.
38. Bağla'ya tıklayın.
39. Ağaçta seçin 'Payments= Transactions\Currency code(Currency)'.
40. Ağaçta genişletin 'Transactions\>Relations'.
41. Ağaçta genişletin 'Transactions\>Relations\Currency table(Currency)'.
42. Ağaçta seçin 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.
43. Bağla'ya tıklayın.
44. Ağaçta genişletin 'Payments= Transactions\Debtor'.
45. Ağaçta genişletin 'Payments= Transactions\Debtor\Account'.
46. Ağaçta seçin 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.
47. Ağaçta seçin 'Bank Account(BankAccount)'.
48. Ağaçta genişletin 'Bank Account(BankAccount)'.
49. Ağaçta seçin 'Bank Account(BankAccount)\Currency(CurrencyCode)'.
50. Bağla'ya tıklayın.
51. Ağaçta seçin 'Bank Account(BankAccount)\IBAN'.
52. Ağaçta seçin 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.
53. Bağla'ya tıklayın.
54. Ağaçta seçin 'Payments= Transactions\Debtor\Account\Number'.
55. Ağaçta seçin 'Bank Account(BankAccount)\Bank account number(AccountNum)'.
56. Bağla'ya tıklayın.
57. Ağaçta genişletin 'Payments= Transactions\Debtor\Agent'.
58. Ağaçta seçin 'Payments= Transactions\Debtor\Agent\Name'.
59. Ağaçta seçin 'Bank Account(BankAccount)\Name'.
60. Bağla'ya tıklayın.
61. Ağaçta seçin 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.
62. Ağaçta seçin 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.
63. Bağla'yı tıklatın.
64. Ağaçta seçin 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.
65. Ağaçta seçin 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.
66. Bağla'ya tıklayın.
67. Ağaçta seçin 'Payments= Transactions\Debtor\Name'.
68. Ağaçta seçin 'Company information(Company)'.
69. Ağaçta genişletin 'Company information(Company)'.
70. Ağaçta seçin 'Company information(Company)\Name'.
71. Bağla'ya tıklayın.
72. Ağaçta seçin 'Payments= Transactions\Description'.
73. Ağaçta seçin 'Transactions\Description(Txt)'.
74. Bağla'ya tıklayın.
75. Ağaçta seçin 'Payments= Transactions\End to end identification code(End2EndID)'.
76. Ağaçta, 'Transactions\$$EndToEndID' seçin.
77. Bağla'ya tıklayın.
78. Ağaçta seçin 'Payments= Transactions\Instructed amount(InstructedAmount)'.
79. Ağaçta, 'Transactions\$Amount' seçin.
80. Bağla'ya tıklayın.
81. Ağaçta seçin 'Payments= Transactions\Transaction date(TransactionDate)'.
82. Ağaçta seçin 'Transactions\Date(TransDate)'.
83. Bağla'ya tıklayın.

## <a name="validate-created-mapping"></a>Oluşturulan eşleme doğrulama
1. Doğrula'ya tıklayın.
    * Tüm bağlamaların doğru yapıldığından emin olmak için yeni eşlemeyi doğrulayın.  
2. Hata Listesi bölümünü genişletmek veya daraltmak için oka tıklayın.
3. Kaydet'e tıklayın.
4. Sayfayı kapatın.
5. Sayfayı kapatın.
6. Sayfayı kapatın.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Model yapılandırmasının geçerli sürümünün durumunu değiştirin
1. Durumu değiştir öğesine tıklayın.
    * Ödeme biçimi tasarımında kullanılabilmesi için tasarlanan model yapılandırmasının durumunu Taslak'tan Tamamlandı'ya değiştirin.  
2. Tamamla öğesine tıklayın.
    * Tamamlandı'yı seçin.  
3. Açıklama alanına bir değer girin.
    * Örneğin, "sürüm 1".  
4. Tamam'a tıklayın.
5. Geçerli yapılandırmanın tamamlanmış sürümünü seçin.
    * Oluşturulan yapılandırmanın tamamlanmış sürüm 1 olarak kaydedildiğini unutmayın.  



--- 
title: "ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışa aktarma"
description: "Bu yordamda, Satıcı ödeme günlüğünde ödeme satırlarının ve ISO2022 Alacak transferi örneğini kullanarak bir satıcı ödemesi dosyasının nasıl oluşturulacağını gösterir."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışa aktarma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordamda, Satıcı ödeme günlüğünde ödeme satırlarının ve ISO2022 Alacak transferi örneğini kullanarak bir satıcı ödemesi dosyasının nasıl oluşturulacağını gösterir. 

Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.

Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın beşincisidir. Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="create-payment-lines"></a>Ödeme satırları oluşturun
1. Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.
2. Yeni'ye tıklayın.
3. Listede, seçili satırı işaretleyin.
4. Ad alanına bir değer girin veya buradan bir değer seçin.
5. Satırlar seçeneğine tıklayın.
6. Ödeme teklifi'ne tıklayın.
7. Ödeme teklifi oluştur'a tıklayın.
8. Eklenecek kayıtlar bölümünü genişletin.
9. Filtre'ye tıklayın.
10. Listede, Satıcılar tablosu ve Satıcı hesabı alanı için satır seçin.
11. Ölçütler alanında bir değer girin veya seçin.
    * Ödeme yapmak için satıcı hareketlerini seçmek amacıyla herhangi bir ölçütü uygulayabilirsiniz. Bu örnek satıcı hesabı olarak DE-001'i kullanır.  
12. Tamam'a tıklayın.
13. Tamam'a tıklayın.
14. Ödemeleri oluştur'a tıklayın.

## <a name="generate-an-iso20022-payment-file"></a>ISO20022 ödeme dosyası oluşturma



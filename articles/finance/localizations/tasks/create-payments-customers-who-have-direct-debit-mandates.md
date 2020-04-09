---
title: Hesaptan ödeme talimatları olan bir müşteri için ödemeler oluşturma
description: Bu yordam, hesaptan ödeme yapılandırması ve ödenecek bir faturası olan müşteriler için bir ISO20022 hesaptan ödeme dosyasının nasıl oluşturulacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a4714f1f1b24554684219fc1d766b4b87cff7bb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141615"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Hesaptan ödeme talimatları olan bir müşteri için ödemeler oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, hesaptan ödeme yapılandırması ve ödenecek bir faturası olan müşteriler için bir ISO20022 hesaptan ödeme dosyasının nasıl oluşturulacağını gösterir. Bir faturayı oluşturmak ve deftere nakletmek isteğe bağlıdır. Ödenecek fatura yerine müşteri ön ödeme senaryosunu desteklemek için bir ödeme dosyası oluşturmadan önce günlükte bir talimat seçebilirsiniz.



Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.



Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın beşincisidir. Bu görevi tamamlamadan önce önceki görevleri tamamlamanız gerekir. Öncelikle müşteri ödeme elektronik raporlama yapılandırmalarını içe aktarmanız, ödeme yöntemini yapılandırmanız ve şirket ve müşteri bilgilerini ayarlamanız gerekir. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Hesaptan ödeme talimatı bilgileri olan bir serbest metin faturasını deftere nakletme
1. Alacak hesapları > Faturalar > Tüm serbest metin faturaları'na gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer girin veya seçin.
    * Örneğin, DE-010 öğesini seçin.  
4. Ödeme yöntemi alanında bir değer girin veya bir değer seçin.
    * Örneğin, Elektronik'i seçin.  
5. Hesaptan ödeme talimatı alanında bir değer girin veya bir değer seçin.
6. Satır ekle'ye tıklayın.
7. Tanım alanına bir değer girin.
8. Ana hesap alanında istediğiniz değerleri belirtin.
9. Birim fiyatı alanına bir sayı girin.
10. Deftere Naklet öğesine tıklayın.
11. Tamam'a tıklayın.

## <a name="create-a-payment"></a>Ödeme oluşturma
1. Alacak hesapları > Ödemeler > Ödeme günlüğü'ne gidin.
2. Yeni'ye tıklayın.
3. Ad alanına bir değer girin veya buradan bir değer seçin.
4. Satırlar seçeneğine tıklayın.
5. Ödeme teklifi'ne tıklayın.
6. Ödeme teklifi oluştur'a tıklayın.
7. Eklenecek kayıtlar bölümünü genişletin.
8. Filtre'ye tıklayın.
9. Listede, Müşteri hareketleri tablosu ve Ödeme yöntemi alanı için bir satır seçin.
    * Ödenecek müşteri hareketlerini seçmek için herhangi bir ölçütü uygulayabilirsiniz. Bu örnekte, filtre hareketleri için ödeme yöntemi olarak Elektronik'i kullanın.  
10. Ölçütler alanında bir değer girin veya seçin.
11. Tamam'a tıklayın.
12. Tamam'a tıklayın.
13. Ödemeleri oluştur'a tıklayın.

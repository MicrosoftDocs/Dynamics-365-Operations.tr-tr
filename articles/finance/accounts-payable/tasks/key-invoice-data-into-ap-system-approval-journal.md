---
title: Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme
description: Bu konu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı açıklar.
author: abruer
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d01c04fcf707109cd7bc6f056846506914e96dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838897"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme

[!include [banner](../../includes/banner.md)]

Bu konu, fatura kaydını fatura oluşturmak için nasıl kullanacağınızı ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınızı açıklar.

## <a name="create-and-post-and-invoice"></a>Fatura oluşturun ve nakledin
1. Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura kaydı**'na gidin.
2. **Yeni**'yi seçin.
3. Kullanmak istediğiniz fatura kaydının adını seçin.
4. Defteri açıp gider satırlarını girmek için **Satırlar**'ı seçin.
5. Bir satıcı seçin. Örneğin, `US-104` girin veya seçin
6. **Fatura** alanına bir değer girin.
7. **Tanım** alanına bir değer girin.
8. **Alacak** alanına bir sayı girin.
9. **Onaylanan** alanında, açılır menüden bir onaylayan belirleyin.
10. **Naklet**'i seçin.

## <a name="approve-an-invoice"></a>Fatura onaylayın
1. Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura onayı**'na gidin.
2. **Yeni**'yi seçin.
3. Kullanmak istediğiniz fatura onayı günlüğünün adını seçin.
4. Onaylamak istediğiniz faturaları seçebileceğiniz bir sayfayı görüntülemek için **Satırlar**'ı seçin.
5. Onaya hazır olan faturaların tümünü görüntülemek için **Fişleri bul**'u seçin.
6. Oluşturduğunuz faturayı işaretleyin ve **Seç**'e tıklayın. Yukarıda seçtiğiniz fişler, seçiminizden sonra bu listeye taşınır.  
7. **Tamam**'ı seçin.
8. Faturaya bir gider hesabı eklemek için **Hesap numarası** alanını seçin.
9. Hesap numarası girin ve sekme tuşuyla alandan çıkın. Örneğin `600120` yazın.
10. **Naklet**'i seçin.
11. Nakledilen girişleri görüntülemek için **Fiş**'i seçin. Onay Bekleyen Fatura hesabı ters kaydedilir ve yerine gerçek gider hesabı geçirilir.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
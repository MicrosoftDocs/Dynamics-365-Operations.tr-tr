---
title: Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme
description: Bu makalede, fatura kaydını fatura oluşturmak için nasıl kullanacağınız ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınız açıklanmaktadır.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afe1471949bbf892f4e28ed3bea830ee491a517f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909228"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Onay günlüğü kullanarak fatura verilerini borç hesaplarına girme

[!include [banner](../../includes/banner.md)]

Bu makalede, fatura kaydını fatura oluşturmak için nasıl kullanacağınız ve bunun ardından, onay günlüğünü gider hesaplarını güncelleştirmek için nasıl kullanacağınız açıklanmaktadır.

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

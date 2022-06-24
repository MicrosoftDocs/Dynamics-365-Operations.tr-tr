---
title: ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışa aktarma
description: Bu yordamda, Satıcı ödeme günlüğünde ödeme satırlarının ve ISO2022 Alacak transferi örneğini kullanarak bir satıcı ödemesi dosyasının nasıl oluşturulacağını gösterir.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac84055586eff678ea489b35198b1c2dfab13658
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856481"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışarı aktarma

[!include [banner](../../includes/banner.md)]

Bu makalede, satıcı ödeme günlüğünde ödeme satırlarının nasıl oluşturulacağı ve ISO2022 Alacak transferi örneği kullanılarak bir satıcı ödemesi dosyasının nasıl oluşturulacağı açıklanmaktadır.

Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın beşincisidir. Bu örneği tamamlamak için DEMF demo verisini kullanın.

## <a name="example"></a>Örnek

1.    **Borç hesapları > Ödemeler > Ödeme günlüğü'ne** gidin.
2.    **Yeni**'yi tıklatın.
3.    **Ad** alanına bir değer girin veya buradan bir değer seçin.
4.    **Satırlar >Ödeme teklifi > Ödeme teklifi oluştur**'a tıklayın.
5.    **Eklenecek kayıtlar** bölümünü genişletin.
6.    **Filtrele** öğesine tıklayın.
7.    Listede, **Satıcılar tablosu** ve **Satıcı hesabı alanı** için satır seçin.
8.    **Ölçütler** alanında bir değer girin veya seçin. Ödeme yapmak için satıcı hareketlerini seçmek amacıyla herhangi bir ölçütü uygulayabilirsiniz. Bu örnek satıcı hesabı olarak DE-001'i kullanır.
12.    **Tamam** seçeneğini tıklatın.
13.    **Tamam** seçeneğini tıklatın.
14.    **Ödemeleri oluştur**'a tıklayın.
15. ISO20022 ödeme dosyası oluşturma.
    1.    **Ödemeler oluştur**'u tıklatın.
    2.    **Ödeme yöntemi** alanında bir değer girin veya bir değer seçin.
    3.    **Dosya adı** alanına bir değer girin. Bu örnekte, EUR ödemesi nedeniyle oluşturulan dosya SEPA uyumlu olacaktır. ISO20022 kredi transferi ve diğer satıcı ödeme biçimleri de diğer para birimlerinde ödemeler oluşturmak için kullanılabilir.
    4.    **Banka hesabı** alanında bir değer girin veya seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
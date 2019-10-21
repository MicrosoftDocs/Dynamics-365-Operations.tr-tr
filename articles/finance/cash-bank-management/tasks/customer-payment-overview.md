---
title: Müşteri ödemesine genel bakış
description: Bu görev kılavuzu, müşteri ödemelerini girmek için kullanılan çeşitli yöntemleri açıklar.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7777ba38e4bf41b17fae698200017b933fc9e876
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188177"
---
# <a name="customer-payment-overview"></a>Müşteri ödemesine genel bakış

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu, müşteri ödemelerini girmek için kullanılan çeşitli yöntemleri açıklar. Bu görevde USMF demo şirketi kullanılmaktadır.

1. **Gezinti bölmesi Modüller > Alacak hesapları > Ödemeler > Ödeme günlüğü**'ne gidin.
2. **Yeni**'ye tıklayın.
3. Müşteri ödemelerinin kaydedileceği ödeme günlüğünü seçin.
4. Günlüğü seçin veya el ile girin.
5. **Eylem Bölmesinde**, **Müşteri ödemeleri gir**'e tıklayın. Müşteri ödemeleri girmek aynı anda bir müşteri ödemesi kaydetmek için kullanılır. Üstte, ödeme bilgilerini girin ve sonra aynı sayfada ödeme tarafından ödenen faturaları işaretleyebilirsiniz.  
6. Ödemeyi aldığınız müşteriyi girin. Müşteri bilmiyor ancak ödenen hareketi biliyorsanız, ödemeyi girmek için Hareket alanını kullanabilirsiniz. Hareket alanında faturayı girin veya seçin. Müşteri, siz hareketi seçtikten sonra otomatik olarak varsayılan olur.
7. **Ödeme referansı** alanına, bir ödeme referansı girin. Ödeme referansı, müşterinin çek numarası veya müşterinin elektronik ödemesinden bir referans olabilir. Ödeme referansı, ödemeyi bir havale makbuzuna dahil etmek için seçmeniz durumunda gereklidir.  
8. **Havale makbuzu** alanında, ödemenin banka havalesi üzerine dahil edilecek olup olmadığını seçin. 
9. **Tutar** alanına, müşteri ödemesi tutarını girin. Ödeme tutarı varsayılan olmaz. El ile girilmelidir. 
10. Müşteri tarafından ödenen faturaları işaretleyin. Ödeme bir ön ödemeyse, kapatma için herhangi bir fatura işaretlemeniz gerekmez. Ödeme yine de kaydedilebilir ve deftere nakledilebilir. Fatura için kapatma daha sonra gerçekleştirilebilir.
11. Seçilen faturaya kapatılacak olan ödemenin miktarını girin. Bu alan, ödeme için kısmi bir ödeme olduğunda kullanılabilir. Bir tutar girmezseniz, kapatılacak tutar sizin için otomatik olarak belirlenir.
12. **Günlüğe kaydet** öğesine tıklayın. Ödemeyi günlüğe kaydetmeden önce mahsup hesabın tanımlanmış olduğundan emin olun. **Günlüğe kaydet** seçeneğini kullanmak, ödemenin kaydedilip günlüğe taşınmasını sağlar. Bir sonraki ödemeyi girerek devam edebilirsiniz.
13. Sayfayı kapatın.
14. **Eylem bölmesinde**, Satırlar'a tıklayın. Satırları açarken, **Müşteri ödemeleri girin** sayfasında kaydetmiş olduğunuz ve günlüğe kaydedilen tüm ödemeleri görürsünüz. Ayrıca, bu sayfayı yeni müşteri ödemeleri girmek veya mevcut müşteri ödemesini deftere nakletmeden önce düzenlemek için kullanabilirsiniz.
15. Başka bir ödeme oluşturmak için **Yeni** seçeneğine tıklayın. 
16. Ödemeyi aldığınız müşteriyi seçin. Müşteriyi bilmiyor ancak ödeme tarafından ödenen bir faturayı biliyorsanız, Fatura alanını kullanarak faturayı el ile girin veya seçin. Fatura seçildikten sonra müşteri varsayılan olarak seçilir.  
17. Ödenen faturaları işaretlemek için **Hareketleri kapat** seçeneğine tıklayın. Ödemeyi herhangi bir fatura karşılık kapatmanıza gerek yoktur. Bu bir ön ödemeyse veya hangi faturanın ödendiğini bilmiyorsanız, ödemeyi girebilir ve deftere nakledebilirsiniz. Ödeme, daha sonraki bir zamanda bir faturaya karşılık kapatılabilir.  
18. Ödeme ile ödenen faturaları işaretleyin. 
19. **Tutar** alanında, faturaya kapatılacak olan ödemenin tutarını girin.
20. **Tamam**'a tıklayın.
21. **Ödeme referansı** alanına, bir ödeme referansı girin. Ödeme referansı, ödemeyi bir havale makbuzuna dahil etmek için seçmeniz durumunda gereklidir.  
22. **Eylem bölmesinde** müşteri ödemelerini deftere nakletmek için **Deftere naklet**'e tıklayın. 


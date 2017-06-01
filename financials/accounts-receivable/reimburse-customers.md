---
title: "Müşterilere tediye"
description: "Bu makalede bir müşteri grubu için iade hareketlerinin nasıl oluşturulacağı açıklanmaktadır. Bir müşterinin alacak bakiyesi varsa, müşteriye bakiye tutarı için iade yapabilirsiniz."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3201166eb7054205647a54ed80f98968fcfda6e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="reimburse-customers"></a>Müşterilere tediye

[!include[banner](../includes/banner.md)]


Bu makalede bir müşteri grubu için iade hareketlerinin nasıl oluşturulacağı açıklanmaktadır. Bir müşterinin alacak bakiyesi varsa, müşteriye bakiye tutarı için iade yapabilirsiniz. 

Başlamadan önce yerine getirilmesi gereken önkoşullar aşağıdaki tabloda gösterilmiştir.

| Önkoşul                                                            | Açıklama                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tüzel kişilik için minimum para iadesi tutarını belirtin.          | **Borç hesapları parametreleri** sayfasındaki **Genel** altındaki **Minimum para iadesi** alanında müşterilerin fazla ödemeleri için para iadesi yapılabilecek minimum tutarı girin. |
| İsteğe bağlı: Para iadesi yapılabilecek her bir müşteri için bir satıcı hesabı ekleyin. | **Müşteriler** sayfasındaki **Muhtelif bilgiler** hızlı sekmesindeki **Satıcı hesabı** alanından müşteri için satıcı hesabını seçin.                                           |

Para iadesi hareketleri oluşturduğunuzda borç bakiyesi miktarı için bir satıcı faturası oluşturulur. Para iadesi işlemi, müşteri hesabı için borç bakiyesini kaldırır ve müşteriye karşılık gelen satıcı hesabı için bir borç bakiyesi oluşturur.

1.  Alacak hesapları altından **Para iadesi** işlemini yürütün.
2.  Şu adımlardan birini izleyin:
    -   Belirli müşteri hesaplarına para iadesi yapmak için**Seç** düğmesini tıklayın ve ilgili müşteri hesaplarını belirtin.
    -   Tüm müşteri hesaplarını iade etmek için **Tamam**'ı tıklatın.

    Borç tutarları, müşterilerin satıcı hesaplarına transfer edilir ve normal ödemeler olarak işlenir. Müşteri bir satıcı hesabına sahip değilse müşteri için otomatik olarak tek seferlik bir satıcı hesabı oluşturur.
3.  Oluşturulan para iadesi hareketlerini görmek için, **Para iadesi** sayfasını kullanın.
4.  Borç hesaplarında para iadesi işlemi tarafından oluşturulan satıcı faturaları için bir ödeme oluşturun.






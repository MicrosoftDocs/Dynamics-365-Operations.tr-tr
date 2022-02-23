---
title: Müşterilere tediye
description: Bu makalede bir müşteri grubu için iade hareketlerinin nasıl oluşturulacağı açıklanmaktadır. Bir müşterinin alacak bakiyesi varsa, müşteriye bakiye tutarı için iade yapabilirsiniz.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ee884fb22c1a38e2d3022085fed7e3e6077d1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644549"
---
# <a name="reimburse-customers"></a>Müşterilere tediye

[!include [banner](../includes/banner.md)]

Bu makalede bir müşteri grubu için iade hareketlerinin nasıl oluşturulacağı açıklanmaktadır. Bir müşterinin alacak bakiyesi varsa, müşteriye bakiye tutarı için iade yapabilirsiniz. 

Başlamadan önce yerine getirilmesi gereken önkoşullar aşağıdaki tabloda gösterilmiştir.

| Önkoşul                                                            | Açıklama |
|-------------------------------------------------------------------------|-------------|
| Tüzel kişilik için minimum para iadesi tutarını belirtin.          | **Borç hesapları parametreleri** sayfasındaki **Genel** altındaki **Minimum para iadesi** alanında müşterilerin fazla ödemeleri için para iadesi yapılabilecek minimum tutarı girin. |
| İsteğe bağlı: Para iadesi yapılabilecek her bir müşteri için bir satıcı hesabı ekleyin. | **Müşteriler** sayfasındaki **Muhtelif bilgiler** hızlı sekmesindeki **Satıcı hesabı** alanından müşteri için satıcı hesabını seçin. |

Para iadesi hareketleri oluşturduğunuzda borç bakiyesi miktarı için bir satıcı faturası oluşturulur. Para iadesi işlemi, müşteri hesabı için borç bakiyesini kaldırır ve müşteriye karşılık gelen satıcı hesabı için bir borç bakiyesi oluşturur.

1. Alacak hesaplarında **Para iadesi** işlemini çalıştırın (**Alacak hesapları \> Periyodik görevler \> Para iadesi**).
2. Genel muhasebe boyutlarına bakılmaksızın, tüm hareketleri gruplandırmak için **Müşteriyi özetle** seçeneğini **Evet** olarak ayarlayın. Yalnızca benzer defter boyutları olan hareketleri gruplandırmak için, seçeneği **Hayır** olarak ayarlayın.
3. Kapatılmayan borç tutarları olan müşterileri seçmek için **Bekleyen borç hareketleri olan müşterileri dahil et**'i seçin.
4. Belirli müşteri hesaplarına para iadesi yapmak için **Dahil edilecek kayıtlar** hızlı sekmesinde **Filtre**'yi seçin ve ardından sorguda müşteri hesaplarını belirtin.

    Borç tutarları, müşterilerin satıcı hesaplarına transfer edilir ve normal ödemeler olarak işlenir. Müşteri bir satıcı hesabına sahip değilse müşteri için otomatik olarak tek seferlik bir satıcı hesabı oluşturur.

5. Oluşturulan para iadesi hareketlerini görüntülemek için **Para iadesi** raporunu kullanın (**Alacak Hesapları \> Sorgular ve raporlar \> Para iadesi raporu**).
6. Borç hesaplarında para iadesi işlemi tarafından oluşturulan satıcı faturaları için bir ödeme oluşturun. Satıcılara nasıl ödeme yapıalcak hakkında bilgi için bkz. [Satıcı ödemesine genel bakış](../accounts-payable/Vendor-payments-workspace.md).

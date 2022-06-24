---
title: Satınalma siparişleri ve faturalarda azalmalardan sonra devrolan bütçeyi güncelleştirme
description: Bu makalede, satınalma siparişleri iptal edildiğinde veya azaltıldığında ve faturalar azaltıldığında devrolan bütçedeki değişikliklerin nasıl denetleneceği açıklanmaktadır.
author: TaylorVH
ms.date: 02/11/2022
ms.topic: article
ms.search.form: LedgerFund
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-savanh
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2022-02-01
ms.openlocfilehash: 7f0ef0ffdf697609e811f754b4378b1f7a81c494
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897972"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Satınalma siparişleri ve faturalarda azalmalardan sonra devrolan bütçeyi güncelleştirme

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, satınalma siparişleri iptal edildiğinde veya azaltıldığında ve faturalar azaltıldığında devrolan bütçedeki değişikliklerin nasıl denetleneceği açıklanmaktadır.

Satınalma siparişlerinin yıl sonunda nasıl işlendiği hakkında bilgi için bkz. [Yıl sonunda satın alma siparişlerini işleme](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Fatura farkları için devrolan bütçe indirimlerini açma veya kapatma

Sistem, satınalma siparişi iptal edildiğinde veya azaltıldığında devrolan bütçeyi her zaman güncelleştirebilir. Ancak, bir fatura azaltıldığında devrolan bütçeyi güncelleştirmek istiyorsanız *Satınalma siparişine karşı bir fatura fark ile azaltıldığında nakli yekun bütçesini azalt* özelliğini açmanız gerekir. Yöneticiler **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanında bu özelliği arayarak özelliği açabilir veya kapatabilir.

## <a name="purchase-order-reductions-and-cancellations"></a>Satınalma siparişi azaltmaları ve iptalleri

*Satınalma siparişine karşı bir fatura fark ile azaltıldığında nakli yekun bütçesini azalt* özelliğinin açık olup olmamasına bakılmaksızın, uygun bir satınalma siparişi iptal edildiğinde veya azaldığında devrolan bütçe güncelleştirilir. Her genel muhasebe fonunu, aşağıdaki seçeneklerden biriyle yanıt verecek şekilde ayarlayabilirsiniz:

- Devrolan bütçeyi oluşturulan şekliyle koruma.
- İptal edilen veya azaltılan tutarı kaldırmak için devrolan bütçeyi otomatik olarak ayarlama.

Yalnızca fon içeren dağıtımlara sahip satınalma siparişi satırları otomatik bütçe ayarlama için uygundur. Otomatik bütçe ayarlaması, satınalma siparişi son haline getirildiğinde veya satınalma siparişini azaltma işlemi onaylandığında gerçekleşir.

## <a name="invoice-reductions"></a>Fatura azaltmaları

*Satınalma siparişine karşı bir fatura fark ile azaltıldığında nakli yekun bütçesini azalt* özelliği açık olduğunda, satın alma siparişinin azaltılmasının veya iptal edilmesinin yanı sıra bir fatura azaltıldığında her bir fonun devrolan bütçeyi azaltıp azaltmayacağını belirtebilirsiniz. Faturanın, devrolan bütçeye sahip bir satınalma siparişi için olması gerekir. Azaltmalar arasında fiyat farkları, ücret farkları ve vergi farkları bulunur. Faturalama sırasında, devrolan satınalma siparişi azaltıldığında bir fark oluşturulur. Fatura deftere nakledildiğinde, satınalma siparişi taahhüdü fark miktarına göre azaltılır. Bu özellik aynı zamanda fark tutarı için otomatik bütçe ayarlaması da oluşturur.

*Satınalma siparişine karşı bir fatura fark ile azaltıldığında nakli yekun bütçesini azalt* özelliği kapalı olduğunda, bu senaryoda devrolan bütçe azaltılmaz. Bu nedenle, fark tutarı için kalan devrolan bütçe bırakılır.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Her bir fon için devrolan bütçe seçeneklerini yapılandırma

Bir satınalma siparişi veya fatura azaltıldığında devrolan bütçeyi azaltması gereken her bir genel muhasebe fonu için aşağıdaki adımları izleyin

1. **Genel muhasebe \> Hesap planı \> Fonlar \> Fonlar** bölümüne gidin.
1. Ayarlamak istediğiniz fonu seçin
1. **Satınalma siparişi yıl sonu süreci** bölümünde, **Seçili yıl sonu seçeneğini geçersiz kıl** seçeneğinin *Evet* olarak ayarlandığından emin olun.
1. **Nakli yekun bütçesi durumu** bölümünde, **Devredilen bir satınalma siparişi iptal edildiğinde veya azaltıldığında bütçeyi eski durumuna getir** alanını gereken şekilde ayarlayın. *Satınalma siparişine karşı bir fatura fark ile azaltıldığında nakli yekun bütçesini azalt* özelliğinin sisteminizde açık olup olmamasına bağlı olarak bu ayarların etkileri kısmen farklıdır.

    - Bu özellik devre dışı bırakıldığında, sistem yalnızca iptal edilen veya azaltılan satın alma siparişleri için harekete geçer. Seçenek ayarları aşağıdaki şekilde çalışır:

        - *Hayır*: Sistem, iptal edilmiş veya azaltılmış satın alma siparişlerinin kalan bakiyesi için bütçe kaydı girişi oluşturur.
        - *Evet*: Sistem satınalma siparişlerinin iptal edilmesine veya azaltılmasına izin verir ancak bütçe kaydı girişi oluşturmaz. Devrolan bütçe, diğer belgelerin tüketim için kullanılabilir.

    - Bu özellik etkinleştirildiğinde, sistem hem fatura farkları hem de iptal edilen veya azaltılan satın alma siparişleri için harekete geçer. Seçenek ayarları aşağıdaki şekilde çalışır:

        - *Hayır*: Sistem, fatura farklarında fark azaltma tutarı için satınalma siparişine karşılık olarak bir bütçe kaydı girişi oluşturur. İptal edilen veya azaltılan satınalma siparişlerinde bu ayar, özellik kapalıyken sahip olduğu etkiye sahiptir.
        - *Evet*: Sistem, fatura farklarında fatura azaltmalarına izin verir, ancak bir bütçe kaydı girişi oluşturmaz. Devrolan bütçe, diğer belgelerin tüketim için kullanılabilir. İptal edilen veya azaltılan satınalma siparişlerinde bu ayar, özellik kapalıyken sahip olduğu etkiye sahiptir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Yıl sonunda satınalma siparişlerini işleme](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Genel bütçe ayırma işlemlerini koru](general-budget-reservation-tasks.md)
- [Kamu sektöründe fonlar](funds-public-sector.md)
- [Kamu sektörü için bir fon ayarlama](tasks/set-up-fund-public-sector.md)

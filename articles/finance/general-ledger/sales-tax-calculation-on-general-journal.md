---
title: Yevmiye defteri satırlarında satış vergisi hesaplaması
description: Bu konu, yevmiye defteri satırlarında farklı hesap türleri (satıcı, müşteri, genel muhasebe ve proje) için satış vergilerinin nasıl hesaplandığını açıklamaktadır.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 51d43c8e6d16201e1f8c392c13ead20287782dcc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448667"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Yevmiye defteri satırlarında satış vergisi hesaplaması
[!include [banner](../includes/banner.md)]

Bu konu, yevmiye defteri satırlarında farklı hesap türleri (satıcı, müşteri, genel muhasebe ve proje) için satış vergilerinin nasıl hesaplandığını açıklamaktadır.

Bu işlem üç adıma ayrılabilir:

- Satış vergisi yönünü belirleyin.

- Geçici bir satış vergisi tablosunda depolanacak satış vergisi tutarını belirleyin.

- Fişteki satış vergisi tutarını ve hesabını belirleyin.

## <a name="determine-the-sales-tax-direction"></a>Satış vergisi yönünü belirleme

Satış vergisi yönünü belirleme şekli, fişteki hesabın türüne göre değişir. Satış vergisi yönü, hesap türü ve satış vergisi kodu bileşimine göre belirlenir. Aşağıdaki bölümlerde olasılıklar daha ayrıntılı açıklanmaktadır. 

### <a name="account-type-is-project"></a>Hesap türü Proje'dir

Bir fişte hesap türü **Proje** olan bir günlük satırı varsa, fişteki tüm günlük satırları aynı vergi yönünü uygular. Aşağıdaki resimde kural gösterilmektedir. Aşağıdaki noktalar, proje hesapları için olası vergi yönlerini gösterir.

•   Satış vergisi kodu kullanım vergisi ise, satış vergisi yönü Kullanım Vergisi'dir.

•   Satış vergisi kodu vergiden muaf ise, satış vergisi yönü Vergiden Muaf Satınalma'dır.

•   Satış vergisi kodu intracom KDV'siyse, satış vergisi yönü Satış Vergisi Borcu'dur.

•   Satış vergisi kodu ters gider ise, satış vergisi yönü Satış Vergisi Borcu'dur.

Aksi takdirde, satış vergisi yönü Satış Vergisi Alacağı olur.

Aşağıdaki diyagramda kural grafik olarak gösterilmektedir.

![Proje hesapları için vergi yönü olasılıkları](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Hesap türü Satıcı'dır

Bir fişte hesap türü **Satıcı** olan bir günlük satırı varsa, fişteki tüm günlük satırları aynı vergi yönünü uygular. Aşağıdaki noktalar, satıcı hesapları için olası vergi yönlerini gösterir. 

•   Satış vergisi kodu kullanım vergisi ise, satış vergisi yönü Kullanım Vergisi'dir.

•   Satış vergisi kodu vergiden muaf ise, satış vergisi yönü Vergiden Muaf Satınalma'dır.

•   Satış vergisi kodu intracom KDV'siyse, satış vergisi yönü Satış Vergisi Borcu'dur.

•   Satış vergisi kodu ters gider ise, satış vergisi yönü Satış Vergisi Borcu'dur.

Aksi takdirde, satış vergisi yönü Satış Vergisi Alacağı olur.

Aşağıdaki diyagramda kural grafik olarak gösterilmektedir.

![Satıcı hesapları için vergi yönü olasılıkları](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Hesap türü Müşteri'dir

Bir fişte hesap türü **Müşteri** olan bir günlük satırı varsa, fişteki tüm günlük satırları aynı vergi yönünü uygular. Aşağıdaki noktalar, müşteri hesapları için olası vergi yönlerini gösterir.

•   Satış vergisi kodu vergiden muaf ise, satış vergisi yönü Vergiden Muaf Satınalma'dır.

•   Satış vergisi kodu intracom KDV'siyse, satış vergisi yönü Satış Vergisi Alacağı'dır.

•   Satış vergisi kodu ters gider ise, satış vergisi yönü Satış Vergisi Alacağı'dır.

Aksi takdirde, satış vergisi yönü Satış Vergisi Borcu olur.

Aşağıdaki diyagramda kural grafik olarak gösterilmektedir.

![Müşteri hesapları için vergi yönü olasılıkları](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a>Hesap türü Genel Muhasebe'dir

Aşağıdaki şekilde, bir fişte yalnızca hesap türü **Genel Muhasebe** olan günlük satırları olduğu zaman uygulanan kural gösterilmektedir. Aşağıdaki noktalar genel muhasebe hesapları için olası vergi yönlerini gösterir.

•   Satış vergisi kodu kullanım vergisi ise, satış vergisi yönü Kullanım Vergisi'dir.

•   Satış vergisi kodu vergiden muaf ise, satış vergisi yönü Vergiden Muaf Satınalma'dır.

Aksi takdirde, günlük tutarı borç (pozitif) ise satış vergisi yönü Satış Vergisi Alacağı; günlük tutarı alacak (negatif) ise, satış vergisi yönü Satış Vergisi Borcu olur.

Aşağıdaki diyagramda kural grafik olarak gösterilmektedir.

![Genel muhasebe hesapları için vergi yönü olasılıkları](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>Satış vergisi yönünü geçersiz kılma

Fiş yalnızca hesap türünün **Genel Muhasebe** olduğu satırları içeriyorsa satış vergisi yönünün üzerine yazabilirsiniz.

**Genel muhasebe \> Hesap planı \> Hesaplar \> Ana hesaplar**'a gidin ve **Tüzel varlık geçersiz kılmaları** hızlı sekmesini seçin.

## <a name="determine-the-sales-tax-amount"></a>Satış vergisi tutarını belirleme

Bu bölümde, satış vergisi tutar işaretinin nasıl hesaplandığı açıklanmaktadır.

![Satış vergisi hareketleri sayfası](media/sales-tax-amount-sign.jpg)

Aşağıdaki tabloda, geçici satış vergisi tablosundaki satış vergisi tutarlarının işaretini belirlemeye yönelik genel kural gösterilmektedir.

| Günlük satırı tutarı | Satış vergisi yönü  | Satış vergisi tutar işareti |
|---------------------|----------------------|-----------------------|
| Pozitif            | Satış Vergisi Alacağı | Pozitif              |
| Pozitif            | Satış Vergisi Borcu    | Negatif              |
| Negatif            | Satış Vergisi Alacağı | Negatif              |
| Negatif            | Satış Vergisi Borcu    | Pozitif              |

**Genel muhasebe** satırında bir satış vergisi grubu veya madde satış vergisi grubu seçildiğinde yalnızca **Proje** veya **Genel muhasebe** satırları olan fişler için özel bir kural vardır. Bu kural, yevmiye defterleri için Bağımsız satış vergisi hesaplamasını etkinleştir özelliğiyle kontrol edilir. Bu özellik kapatılınca **Genel muhasebe** satırının vergi tutarı **Proje** satırının borç/alacak yönünü kullanır. Bu özellik açılınca **Genel muhasebe** satırının vergi tutarı kendi borç/alacak yönünü kullanır. Aşağıdaki tablolarda her senaryoya ilişkin kural gösterilmektedir. 

**Özellik açıkken uygulanan kural**

| Projenin günlük satırı tutarı | Satış vergisi yönü  | Satış vergisi tutar işareti |
|--------------------------------|----------------------|-----------------------|
| Pozitif                       | Satış Vergisi Alacağı | Pozitif              |
| Negatif                       | Satış Vergisi Alacağı | Negatif              |

**Özellik kapalıyken uygulanan kural**

| Genel muhasebenin günlük satırı tutarı  | Satış vergisi yönü  | Satış vergisi tutar işareti |
|--------------------------------|----------------------|-----------------------|
| Pozitif                       | Satış Vergisi Alacağı | Pozitif              |
| Negatif                       | Satış Vergisi Alacağı | Negatif              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Fişteki satış vergisi tutarını ve hesabını belirleme

Satış vergilerini deftere naklettiğinizde, ana hesap, genel muhasebe deftere nakil grubu profilinden alınır. Satış vergileri alacak olduğu zaman, sistem profilde belirtilen Satış Vergisi Alacağı hesabını kullanır. Borç olan satış vergileri için, sistem profilde belirtilen Satış Vergisi Borcu hesabını kullanır.

Aşağıdaki tabloda genel kural gösterilmektedir.

| Satış vergisi yönü  | Satış vergisi tutar işareti | Satış vergisi hesabı      | Fişteki tutar |
|----------------------|-----------------------|------------------------|-------------------|
| Satış Vergisi Alacağı | Pozitif              | Vergi Alacak Hesabı | Pozitif (Borç)  |
| Satış Vergisi Alacağı | Negatif              | Vergi Alacak Hesabı | Negatif (Alacak)  |
| Satış Vergisi Borcu    | Pozitif              | Vergi Borç Hesabı    | Negatif (Alacak)  |
| Satış Vergisi Borcu    | Negatif              | Vergi Borç Hesabı    | Pozitif (Borç)  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
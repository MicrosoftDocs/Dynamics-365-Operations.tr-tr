---
title: Sabit kıymet hareketi seçenekleri
description: Bu makalede, sabit kıymet hareketleri oluşturmak için kullanılabilecek çeşitli yöntemler açıklanmaktadır.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: kfend
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 402679b6f1003f14f7e277a326784edaaea719d5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883372"
---
# <a name="fixed-asset-transaction-options"></a>Sabit kıymet hareketi seçenekleri

[!include [banner](../includes/banner.md)]

Bu makalede, sabit kıymet hareketleri oluşturmak için kullanılabilecek çeşitli yöntemler açıklanmaktadır.

Sabit kıymetleri Borç hesapları, Alacak hesapları, Tedarik ve kaynak atama ve Genel muhasebeye bağlanacak şekilde ayarlayabilirsiniz. Ayrıca, bu maddeleri dahili olarak kullanmak üzere Stok yönetimindeki maddeleri Sabit kıymetlere de aktarabilirsiniz.

## <a name="accounts-payable"></a>Borç hesapları
Sabit kıymet hareketlerini günlük fişi sayfasına girebilirsiniz. Bu sayfa, Fatura günlüğü sayfasından açılabilir. Günlük fişi sayfasını Fatura onay günlüğü sayfasından da açabilirsiniz. Mahsup hesabı türü alanında, Sabit kıymetleri seçin. Sonra, Mahsup hesap alanında bir sabit kıymet numarası seçin. Sabit kıymetler sekmesinde, Hareket türü ve Değerler alanlarında değerleri girin.

## <a name="accounts-receivable"></a>Alacak hesapları
Sabit kıymet hareketlerini Serbest metin faturası sayfasına girebilirsiniz.  Serbest metin faturası sayfasında, fatura satırları kılavuzunda bir satır öğesini seçin. Satır ayrıntıları Hızlı Sekmesine tıklayın. Elden çıkarma hareketi için sabit kıymet numarasını ve defteri girin. Serbest metin faturaları için, sabit kıymet hareket türü her zaman Satış çıkışıdır.

## <a name="procurement-and-sourcing"></a>Tedarik ve kaynak atama
Sabit kıymet hareketlerini Satınalma siparişi sayfasına girebilirsiniz. Bir satınalma siparişi oluşturmak için gereken bilgileri girin ve Tamam'a tıklayın. Satınalma sipariş sayfasında, Satır ayrıntıları Hızlı Sekmesine tıklayın. Ardından, Sabit kıymetler sekmesinde, sabit kıymet hakkındaki bilgileri girin. 

Mevcut bir sabit kıymet için alım hareketi nakletmek için sabit kıymet numarasını, defteri ve hareket türünü belirtin. Bu bilgiler eksik ise sabit kıymet deftere nakledilemez. Yeni bir sabit kıymet için alım hareketi nakletmek için, Yeni sabit kıymet seçeneğini seçin ve ardından yeni kıymeti atamak için sabit kıymet grubunu seçin. Ancak madde standart bir maliyet stok modeli kullanan bir stok modeli grubundaysa, bir satır için hiçbir sabit kıymet alanı mevcut değildir. Ayrıca, Sabit kıymetler parametreleri sayfasında tanımlanan seçenekler satın alma modüllerinden alım hareketlerini nakledip nakledemeyeceğinizi belirler. 

Sabit kıymet alımı için bir satınalma siparişi veya Stoktan sabit kıymetlere günlüğü kullanıldığında, stok değeri etkilenir.

## <a name="general-ledger"></a>Genel muhasebe
Tüm sabit kıymet hareket türleri Genel günlük sayfasına nakledilebilir. Ayrıca, sabit kıymet hareketlerini deftere nakletmek için Sabit kıymetlerdeki günlükleri kullanabilirsiniz.

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Sabit kıymet hareketleri tiplerini girme seçenekleri


| Hareket türü                    | Modül                   | Seçenekler                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Alım, Alım düzeltmesi | Sabit kıymetler             | Sabit kıymetler, Stoktan sabit kıymetlere   |
|                                     | Genel muhasebe           | Genel günlük                           |
|                                     | Borç hesapları         | Fatura günlüğü, Fatura onay günlüğü |
|                                     | Tedarik ve kaynak atama | Satın alma siparişi                            |
| Amortisman                        | Sabit kıymetler             | Sabit kıymetler                              |
|                                     | Genel muhasebe           | Yevmiye fişi                           |
| Elden çıkarma                            | Sabit kıymetler             | Sabit kıymetler                              |
|                                     | Genel muhasebe           | Yevmiye fişi                           |
|                                     | Alacak hesapları      | Dekont / Serbest metin faturası                         |

Amortisman hareket türü günlük satırı el ile oluşturulduğunda veya bir veri varlığı aracılığıyla içeri aktarıldığında kalan değer sabit kıymetin amortisman dönemleri için güncelleştirilmez. Kalan değer, amortisman teklif işlemi, günlük satırı oluşturmak için kullanıldığında güncelleştirilir.

Daha fazla bilgi için bkz: [Sabit kıymet tümleştirmesi](fixed-asset-integration.md).

Sistem, aynı dönemde amortismanı iki kez deftere nakletmeyi engeller. Örneğin, iki kullanıcı Ocak ayı için ayrı ayrı amortisman teklifleri oluşturursa ilk kullanıcıdan gelen amortisman ilk yevmiye defterine nakledilir. İkinci kullanıcı amortismanı ikinci yevmiye defterine naklettiğinde sistem, amortismanın son çalıştırıldığı tarihi denetler ve amortismanı aynı dönemde ikinci kez deftere nakletmez.

### <a name="transactions-that-require-a-different-voucher-number"></a>Farklı bir fiş numarası gerektiren hareketler

Aşağıdaki Sabit kıymet hareketleri farklı makbuz numaraları kullanır:

- Bir kıymet üzerinde ek bir alım yapılır ve "yakalama" amortismanı hesaplanır.
- Bir kıymet bölünür.
- Elden çıkarma amortismanını hesaplamak için bir parametre açılır ve ardından kıymet elden çıkarılır.
- Bir kıymetin servis tarihi alım tarihinden öncedir. Bu nedenle, bir amortisman düzeltmesi deftere nakledilir.

> [!NOTE]
> Hareketleri girerken tüm hareketlerin aynı sabit kıymet için geçerli olduğundan emin olun. Fiş birden fazla sabit kıymet içeriyorsa **Yeni Fiş** alanı, Genel muhasebedeki **Günlük adları** sayfasında **Yalnızca bir fiş numarası** olarak ayarlansa bile deftere nakledilmez. Fişe birden fazla sabit kıymet eklerseniz "Fiş başına yalnızca bir sabit kıymet hareketi olabilir" iletisini alırsınız ve fişi deftere nakledemezsiniz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

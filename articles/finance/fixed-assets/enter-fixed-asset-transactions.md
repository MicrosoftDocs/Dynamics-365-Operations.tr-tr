---
title: Sabit kıymet hareketi seçenekleri
description: Bu konu, sabit kıymet hareketleri oluşturmak için kullanılabilecek çeşitli yöntemler açıklanmaktadır.
author: ShylaThompson
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3540cf17050a953a97c7291a1bcbe5ebf6fb670e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815728"
---
# <a name="fixed-asset-transaction-options"></a>Sabit kıymet hareketi seçenekleri

[!include [banner](../includes/banner.md)]

Bu konu, sabit kıymet hareketleri oluşturmak için kullanılabilecek çeşitli yöntemler açıklanmaktadır.

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

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Sabit kıymet hareketleri tiplerini girme seçenekleri


| Hareket türü                    | Modül                   | Seçenekler                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Alım, Alım düzeltmesi | Sabit kıymetler             | Sabit kıymetler, Stoktan sabit kıymetlere   |
|                                     | Genel muhasebe           | Genel günlük                           |
|                                     | Borç hesapları         | Fatura günlüğü, Fatura onay günlüğü |
|                                     | Tedarik ve kaynak atama | Satın alma siparişi                            |
| Amortisman                        | Sabit kıymetler             | Sabit kıymetler                              |
|                                     | Genel muhasebe           | Yevmiye fişi                           |
| Elden çıkarma                            | Sabit kıymetler             | Sabit kıymetler                              |
| ** **                               | Genel muhasebe           | Yevmiye fişi                           |
| ** **                               | Alacak hesapları      | Dekont / Serbest metin faturası                         |


Sabit kıymetlerin amortisman dönemleri kalan değerleri, bir amortisman hareketi türü günlük satırı, el ile oluşturulur ve bir veri varlığı üzerinden içeri aktarılır. Bu değer, amortisman teklif işlemi, günlük satırı oluşturmak için kullanıldığında güncelleştirilir.

Daha fazla bilgi için bkz: [Sabit kıymet tümleştirmesi](fixed-asset-integration.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
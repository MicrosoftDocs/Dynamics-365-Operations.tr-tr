---
title: Sabit kıymet amortismanı
description: Bu konuda sabit kıymetlerin amortismanına genel bir bakış sunulmuştur.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ec8544b885485781b0b9c0a59ec47f90fdceb6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826894"
---
# <a name="fixed-asset-depreciation"></a>Sabit kıymet amortismanı

[!include [banner](../includes/banner.md)]

Bu konuda sabit kıymetlerin amortismanına genel bir bakış sunulmuştur.

Amortisman, normalde sabit varlığın değerini bilançoda düşüren periyodik bir harekettir ve kâr-zarar hesabından bir masraf olarak düşülür. Bu nedenle ana hesap bilançoda genellikle periyodik amortismanı alacaklandırmak için kullanılır. Mahsup hesap, hesap planının kâr ve zarar bölümündeki bir hesaptır.

## <a name="depreciation-adjustment"></a>Amortisman Düzeltmeleri
Genellikle, yalnızca deftere nakledilmiş bir amortisman hareketine yönelik düzeltmeler bir amortisman düzeltmesi şeklinde deftere nakledilir. Bu nedenle ana hesap ve mahsup hesap tıpkı amortisman hesapları gibi ayarlanır. Amortisman düzeltmesi olumlu veya olumsuz bir tutar olabilir, ancak ana hesabın (bir bilanço hesabı olarak) ve mahsup hesabın (genellikle bir kar ve zarar hesabı olarak) işlevselliği aynı kalır.

## <a name="extraordinary-depreciation"></a>Olağandışı amortisman
Olağandışı amortisman, temel amortisman gibi çalışır. Bu nedenle, bir ana hesap bilançoya amortisman tutarını alacaklandırmak ve sabit kıymetin değerini azaltmak için kullanılır. Mahsup hesap, mali dönem için hesaplanan amortismanın bir harcama olarak kaydedildiği kâr-zarar hesabıdır. 

Olağandışı amortisman, temel amortismandan bağımsız olarak çalışır. Olağandışı amortismanı ayrı bir hareket türü olarak kullanarak olağandışı amortismanı temel amortismandan farklı olarak deftere nakledebilir ve raporlayabilirsiniz.

## <a name="special-depreciation-allowance"></a>Özel amortisman payı
Kıymetin servise konulduğu ve amortismana ayrıldığı ilk yıl süresince fazladan amortisman tutarları almak için özel amortisman paylarını kullanabilirsiniz. Özel amortisman paylarının diğer her türlü amortisman hesaplamasından önce alınması gerekir. Özel amortisman payları genellikle sabit kıymetin servis ömrünün ileriki zamanlarına kadar bilinmediğinden bu amortisman türünü genel muhasebeye nakledilmeyen bir defter ile kullanmak en iyisidir. Bu defterlerin hareket geçmişlerini, Genel muhasebe defterine nakledilmeyen hareketleri sil periyodik işlevini kullanabilirsiniz. Ardından sabit kıymet defteri için amortisman geçmişini silebilir, bilindiği zaman özel amortisman payını deftere nakledebilir ve ardından yıl için kalan amortisman hareketlerini deftere nakledebilirsiniz. 

Sınırsız sayıda özel amortisman payı kaydı oluşturabilirsiniz. Bu kayıtları, bir kıymet grubu defterine atadıktan sonra kıymet defterine uygulanırlar. 

Özel amortisman payı yüzde veya sabit bir tutar olarak girilir. Amortisman tekliflerini naklettiğinizde, özel amortisman payı hareketleri amortisman hareketlerinden bağımsız hareketler olarak deftere nakledilir.

## <a name="depreciation-calendars"></a>Amortisman takvimleri
Her defterin sabit kıymetlere amortisman ayırırken kullanılan bir takvimi vardır. Varsayılan olarak, defterde bir takvim belirtmezseniz defter, muhasebe mali takvimini kullanır. Defter ile ilişkili amortisman profili bir mali amortisman yılını kullandığında defter için bir mali takvim seçmeniz gerekir. 

Genel muhasebe defterinde **Mali takvimler** sayfasını kullanarak paylaşılan takvimler oluşturabilirsiniz.

Daha fazla bilgi için bkz: [Amortisman yöntemleri ve kuralları](depreciation-methods-conventions.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
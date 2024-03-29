---
title: Ürün reçetelerini tamamlandı olarak raporlama
description: Bu makalede ürün reçetelerini tamamlandı olarak raporlama hakkında bilgi verilmektedir.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMReportFinish, BOMReportFinishMax, BOMSetupReportFinish
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff88622c2cbbdcff6130fb8c500ea12a1e454ecb5f33834bc0a69718038c9e89
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766595"
---
# <a name="report-boms-as-finished"></a>Ürün reçetelerini tamamlandı olarak raporlama

[!include [banner](../includes/banner.md)]

Bu makalede ürün reçetelerini tamamlandı olarak raporlama hakkında bilgi verilmektedir.

**Tamamlandı bildirimi** ve **Mak. Raporu tamamlandı olarak** sayfaları ürün reçetelerini (BOM) tamamlandı olarak bildirmek için kullanılır. Kavramsal açıdan, bir ürün Reçetesini tamamlandı olarak raporlama işlemi, bir üretim emrini tamamlandı olarak raporlama süreciyle aynıdır. Bu işlem örneğin basit montaj ve paket hazırlama işlemleri gibi, üretim emirlerinin daha gelişmiş yeteneklerine ihtiyaç duyulmayan durumlarda kullanılabilir. **Tamamlandı bildirimi** sayfası birden fazla ürün reçetelerini toplu şekilde tamamlandı olarak bildirmenize olanak sağlar. **Maks. Tamamlandı raporu** sayfası, bir kerede yalnızca bir ürün reçetesini tamamlandı olarak bildirmenize olanak tanır. **Tamamlandı olarak bildir** sayfası Stok yönetimindeki bir menü öğesinden kullanılabilir ve her iki sayfa da **Serbest bırakılan ürünler** sayfasında menü öğesi olarak bulunmaktadır.

## <a name="report-as-finished-page"></a>Tamamlandı olarak bildirme sayfası
**Tamamlandı bildirimi** sayfasını serbest bırakılmış bir üründen açarsanız, bu sayfa standart stok varsayılan miktarını tamamlandı olarak bildirmenizi önerir. Varsayılan olarak, etkin ürün reçetesi versiyonu gösterilir, ancak onaylanmış başka sürümler varsa, ürün reçetesi versiyonunun değiştirebilirsiniz. Bu sayfa ayrıca tamamlandı olarak bildirilmesi gereken serbest bırakılmış ürünlerin kayıtlarını silmenize ve yeni kayıtlar oluşturmanızı sağlar. Ürünleri seçerken bir sorgu kullanmak için **Seçin** menü öğesine tıklatın. El ile **Tamam** seçeneğini tıklatarak seçili ürünler için tamamlandı olarak raporlamayı onaylayabilirsiniz. Alternatif olarak, işlemi toplu olarak yürütülecek şekilde de ayarlayabilirsiniz. Tamamlandı bildirimi işlemi teyit edildiğinde, sistem stok naklinin işleneceği bir ürün reçetesi günlüğü oluşturur. Bu günlük bitmiş ürün için bir satır öğesi ve her ürün reçetesi satırı için bir satır öğesi içerir. Günlüğün otomatik olarak deftere mi nakledileceğini yoksa ek ayarlamalar için açık mı bırakılacağını kontrol edebilirsiniz.

## <a name="max-report-as-finished-page"></a>Maksimum tamamlandı olarak bildirme sayfası
**Mak. Tamamlandı bildirimi** sayfası üzerinde, her ürün reçetesi satırı tamamlandığı bildirilen ürün parçalarının sayısını gösterir. Bu hesaplama, her bir malzeme satırının fiziksel olarak eldeki mevcut stoku temel alır. Aşağıdaki örnekte, madde numarası FG'nin bir tanesi, RM10 parça hammaddesinden iki parça ve RM20 hammaddesinden bir parça tüketir. Elde sadece 10 adet RM10 olduğundan, tamamlandır olarak bildirilebilecek maksimum FG miktarı beş parça olur. Bu değer **Mak. Tamamlandı bildirimi** alanında gösterilir.

| Raf | Madde kodu | Miktar | Eldeki | Maksimum Tamamlandı bildirimi |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Birden çok düzeye sahip ürün reçeteleri
Bir ürün reçetesinin birden çok düzeyi varsa, **Açılım** alanını kullanarak malzemelerin tüm düzeylerde nasıl kullanarak hesaba katılacağı kontrol edebilirsiniz . Bu alan hem **tamamlandı bildirimi** sayfasında hem de **Mak. Raporu tamamlandı olarak** sayfasında mevcuttur. Aşağıdaki seçenekler bulunur:

-   **Hiçbir Zaman** – Temeldeki ürün reçeteleri bir malzeme eksikliği olduğunda açılmaz.
-   **Her Zaman** – Temeldeki tüm ürün reçeteleri tamamen açılır. Bu yüzden, yarı tamamlanmış bileşen maddeleri için serbest eldeki stoklardan hiçbiri kullanılmaz.
-   **Eksiklik** – Temeldeki ürün reçeteleri yalnızca istediğiniz malzeme miktarı tam olarak mevcut değilse açılır.

### <a name="example"></a>Örnek

Bu örnekte, üç parça bitmiş ürün (madde numarası FG) tamamlandı olarak bildirilmeye hazırdır. Burada gösterildiği gibi iki düzeyli bir ürün reçetesi mevcuttur.

| Raf | Madde kodu | Ürün reçetesi satır miktarı | Eldeki |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | COMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Aşağıdaki tablolar **Açılım** ayarının ürün reçetesi günlüğü satırlarının oluşturulmasını nasıl etkilediğini gösterir. **Açılımı: Hiçbir zaman**

| Raf | Madde kodu | Miktar |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -3       |

Önceki tablonun gösterdiği gibi yalnızca madde numarası COMP günlükten düşülen olarak kabul edilir. COMP'un parçası olan RM numaralı öğe, günlük satırına açılmaz ve eldeki iki COMP parçası hesaba dahil edilmez. **Açılım: Her zaman**

| Raf | Madde kodu | Miktar |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | -3       |

Bu durumda, madde numarası COMP ham maddesi olan madde numarası RM'ye açılır. Elde mevcut bulunan iki adet COMP, tüketilecek RM miktarına dahil edilmez. **Açılım: Eksiklik**

| Raf | Madde kodu | Miktar |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | COMP        | -2       |
| 1     | RM          | -1       |

Bu durumda, madde numarasının COMP'un eldeki iki parçası değerlendirilir. Fakat madde FG'den üç adet gerekli olduğu için, bir adet COMP daha üretebilmek için, madde numarası RM'den de bir adet daha gerekmektedir.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
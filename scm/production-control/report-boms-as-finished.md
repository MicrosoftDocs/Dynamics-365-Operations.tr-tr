---
title: "Ürün reçetelerini tamamlandı olarak rapor"
description: "Bu makalede, ürün reçetelerini tamamlandı olarak raporlama hakkında bilgi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMReportFinish, BOMReportFinishMax
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 318c88f88277a8300b1fcda5056a9a92c9a81eae
ms.lasthandoff: 03/31/2017


---

# <a name="report-boms-as-finished"></a>Ürün reçetelerini tamamlandı olarak rapor

Bu makalede, ürün reçetelerini tamamlandı olarak raporlama hakkında bilgi sağlar.

**Tamamlandı bildirimi** ve **Mak. Raporu tamamlandı olarak** sayfaları ürün reçetelerini (BOM) tamamlandı olarak bildirmek için kullanılır. Kavramsal açıdan, bir ürün Reçetesini tamamlandı olarak raporlama işlemi, bir üretim emrini tamamlandı olarak raporlama süreciyle aynıdır. Bu işlem örneğin basit montaj ve paket hazırlama işlemleri gibi, üretim emirlerinin daha gelişmiş yeteneklerine ihtiyaç duyulmayan durumlarda kullanılabilir. **Tamamlandı bildirimi** sayfası birden fazla ürün reçetelerini toplu şekilde tamamlandı olarak bildirmenize olanak sağlar. **Mak. Raporu tamamlandı olarak** sayfa, tek bir ürün Reçetesini bir kerede tamamlandı olarak bildirmek sağlar. **Tamamlandı bildirimi** sayfa Stok Yönetimi'nde bir menü öğesi ile kullanılabilir ve her iki sayfa üzerinde bir menü öğeleri olarak kullanılabilir **ürünleri piyasaya** sayfa.

## <a name="report-as-finished-page"></a>Tamamlandı olarak bildirme sayfası
**Tamamlandı bildirimi **sayfasını serbest bırakılmış bir üründen açarsanız, bu sayfa standart stok varsayılan miktarını tamamlandı olarak bildirmenizi önerir. Varsayılan olarak, etkin ürün reçetesi versiyonu gösterilir, ancak onaylanmış başka sürümler varsa, ürün reçetesi versiyonunun değiştirebilirsiniz. Bu sayfa ayrıca tamamlandı olarak bildirilmesi gereken serbest bırakılmış ürünlerin kayıtlarını silmenize ve yeni kayıtlar oluşturmanızı sağlar. Ürünleri seçerken bir sorgu kullanmak için **Seçin** menü öğesine tıklatın. El ile **Tamam** seçeneğini tıklatarak seçili ürünler için tamamlandı olarak raporlamayı onaylayabilirsiniz. Alternatif olarak, işlemi toplu olarak yürütülecek şekilde de ayarlayabilirsiniz. Tamamlandı bildirimi işlemi teyit edildiğinde, sistem stok naklinin işleneceği bir ürün reçetesi günlüğü oluşturur. Bu günlük bitmiş ürün için bir satır öğesi ve her ürün reçetesi satırı için bir satır öğesi içerir. Günlüğün otomatik olarak deftere mi nakledileceğini yoksa ek ayarlamalar için açık mı bırakılacağını kontrol edebilirsiniz.

## <a name="max-report-as-finished-page"></a>Maksimum Rapor bitmiş sayfa olarak
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

Önceki tablonun gösterdiği gibi yalnızca madde numarası günlükte düşülen COMP kabul edilir. Günlük satırına madde numarası COMP parçası olan RM açılımı değildir ve COMP iki eldeki parçalarını kabul edilemiyor. **Açılım: Her zaman**

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



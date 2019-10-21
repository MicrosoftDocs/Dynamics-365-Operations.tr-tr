---
title: Ambar iş ilkelerine genel bakış
description: Ambar işi ilkeleri ambar işinin üretimdeki ambar işlemleri tarafından oluşturulup oluşturulmadığını, iş emri türüne, stok yerleşimine ve ürüne dayanarak kontrol eder.
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7476cf797685feb4c50e3cefef4c53ca37b82dff
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251420"
---
# <a name="warehouse-work-policies-overview"></a>Ambar iş ilkelerine genel bakış

[!include [banner](../includes/banner.md)]

Ambar işi ilkeleri ambar işinin üretimdeki ambar işlemleri tarafından oluşturulup oluşturulmadığını, iş emri türüne, stok yerleşimine ve ürüne dayanarak kontrol eder.

Bu iş ilkesi ambar işinin üretimdeki ambar işlemleri için oluşturulup oluşturulmadığını denetler. **İş emri türleri**, bir **stok konumu** ve bir **ürün** birleşimini kullanarak iş ilkesini ayarlayabilirsiniz. Örneğin, L0101 numaralı ürün 001 numaralı çıktı konumuna tamamlandı olarak bildirilir. Bunun üzerine, tamamlanan mal 001 numaralı çıktı konumundaki başka bir üretim emrinde tüketilir. Bu durumda, L0101 numaralı ürünü 001 numaralı çıktı konumuna tamamlandı olarak bildirdiğiniz zaman mamul mallara yönelik işin oluşturulmasını önlemek için bir iş ilkesi ayarlayabilirsiniz. İş ilkesi, aşağıdaki bilgilerle açıklanabilen ayrı bir varlıktır:

-   **İş ilkesi adı**(iş ilkesinin benzersiz tanımlayıcısı)
-   **İş emri türleri** ve **İş oluşturma yöntemi**
-   **Stok konumları**
-   **Ürünler**

## <a name="work-order-types"></a>İş emri türleri
Aşağıdaki iş emri türlerini seçebilirsiniz:

-   Yerine konan mamul mallar
-   Yerine konan ortak ürün ve yan ürün
-   Hammadde çekme

**İş oluşturma yöntemi** alanı **Asla** değerine sahiptir. Bu değer iş ilkesinin seçili iş emri türü için ambar işinin oluşturulmasını önleyeceğini belirtir.

## <a name="inventory-locations"></a>Stok konumları
İş ilkesinin geçerli olduğu bir konum seçebilirsiniz. İş ilkesi ile ilişkilendirilmiş bir konum yoksa iş ilkesi herhangi bir işleme uygulanmaz. **Konumlar** sayfasında, belirli bir konum için iş ilkesi seçimini yapabilir veya iptal edebilirsiniz.

## <a name="products"></a>Ürünler
İş ilkesinin geçerli olduğu bir ürün seçebilirsiniz. İş ilkesini tüm ürünlere veya seçili ürünlere uygulayabilirsiniz.

## <a name="example"></a>Örnek
Aşağıdaki örnekte, PRD-001 ve PRD-00*2* olmak üzere iki üretim emri bulunmaktadır. Üretim emri PRD-001, SC1 ürününün O1 konumuna tamamlandı olarak bildirildiği **Derleme** adlı bir işleme sahiptir. Üretim emri PRD-002 **Boyama** adlı bir işleme sahiptir ve O1 konumundan SC1 ürününü kullanır. Üretim emri PRD-002 ayrıca O1 konumundan RM1 hammaddesini de kullanır. RM1, BULK-001 ambar konumunda depolanır ve hammadde çekme işlemi için ambar işi tarafından O1 konumuna çekilir. Malzeme çekme işi PRD-002 üretimi serbest bırakıldığında oluşturulur. 

[![Ambar iş ilkeleri](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Bu senaryo için bir ambar işi ilkesi yapılandırmayı planlarken, aşağıdaki bilgileri göz önünde bulundurmalısınız:

-   Yerine konan mamul mallar için ambar işi, SC1 ürününü PRD-001 üretim emrinden O1 konumuna tamamlandı olarak bildirdiğinizde gerekli değildir. Bunun nedeni PRD-002 üretim emrinin **Boyama** işleminin SC1 ürününü aynı konumda kullanmasıdır.
-   Hammadde çekme için ambar işi RM1 hammaddesini BULK-001 ambar konumundan O1 konumuna taşımak için gereklidir.

Bu noktalara göre, ayarlayabileceğiniz iş ilkesine bir örneği aşağıda bulabilirsiniz.


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <strong>İş ilkesi adı</strong><br> | <strong>İş emri türleri</strong><br> |
|         Yerine koyma yok - 01     `          |     - Mamul ürünü yerine koy<br>      |
|                                       |    <strong>Yerleşimler</strong><br>     |
|                                       |                 - O1                  |
|                                       |    <strong>Ürünler</strong> <br>     |
|                                       |                 - SC1                 |

Aşağıdaki yordamlar bu senaryo için ambar iş ilkesini ayarlama konusunda adım adım yönergeler sağlar. Bir üretim emrinin plaka denetimli olmayan bir konuma tamamlandı olarak nasıl bildirileceğini gösteren örnek bir kurulum da açıklanmıştır.

## <a name="set-up-a-warehouse-work-policy"></a>Ambar iş ilkesi ayarlama
Ambar işlemi her zaman ambar çalışmasını içermezler. Bir çalışma ilkesi tanımlayarak, hammadde çekme ve tamamlanmış malların yerine koyması işlerinin oluşturulmasını, çeşitli bir ürün dizisi veya belirtilen konumlar için engelleyebilirsiniz. Bu yordamı oluşturmak için USMF demo verileri şirketi kullanılmıştır. 

ADIMLAR (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Ambar Yönetimi &gt; Kurulum &gt; İş &gt; İş ilkeleri'ne gidin.        |
| 2.  | Yeni'ye tıklayın.                                                                 |
| 3.  | Çalışma ilkesi ad alanına 'Hiçbir yerine koyma çalışma' yazın.                    |
| 4.  | Kaydet'e tıklayın.                                                                |
| 5.  | Ekle öğesine tıklayın.                                                                 |
| 6.  | Listede, seçili satırı işaretleyin.                                        |
| 7.  | İş siparişi türü alanına, 'Mamul mallar yerine koyma' seçeneğini işaretleyin.            |
| 8.  | Ekle öğesine tıklayın.                                                                 |
| 9.  | Listede, seçili satırı işaretleyin.                                        |
| 10. | İş emri türü alanında, "Ortak ürün ve yan ürün yerine koyma" seçeneğini işaretleyin. |
| 11. | Stok konumları bölümünü genişletin.                                    |
| 12. | Ekle öğesine tıklayın.                                                                 |
| 13. | Listede, seçili satırı işaretleyin.                                        |
| 14. | Ambar listesinde '51' girin.                                         |
| 15. | Konum alanına bir '001' girin veya seçin.                              |
| 16. | Ürünler bölümünü genişletin.                                               |
| 17. | Ürün seçimi alanında, 'Seçili'yi işaretleyin.                         |
| 18. | Ekle öğesine tıklayın.                                                                 |
| 19. | Listede, seçili satırı işaretleyin.                                        |
| 20. | Madde numarası alanında 'L0101' girin veya seçin.                         |
| 21. | Kaydet'e tıklayın.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Üretim emrini plaka denetimli olmayan bir konuma tamamlandı olarak bildirme
Bu yordamda, plaka kontrollü olmayan bir konumuna tamamlandı olarak raporlama yapılmasına ilişkin bir örnek gösterilmiştir. Geçerli bir iş politikasının olması bu görev için bir ön koşuldur. Önceki yordamda iş ilkesinin kurulumu gösterilmiştir. 

ADIMLAR (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Alt görev: Bir çıkış konumu ayarlayın.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Organizasyon yönetimi &gt; Kaynaklar &gt; Kaynak grupları'na gidin.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Listede, kaynak grubu &#39;5102&#39; seçin.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Düzenle öğesine tıklayın.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Çıkış ambar alanında, &#39;51&#39; girin.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Çıkış konumu alanında &#39;001&#39; girin.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Konum 001, plaka kontrollü bir konum değildir. Konum için geçerli bir çalışma politikası bulunuyorsa sadece, plaka dışı bir çıkış konumu ayarlayabilirsiniz.</td>
</tr>
<tr>
<td colspan="3"><strong>Alt görev: Bir üretim emri oluşturun ve bunu tamamlandı olarak rapor edin.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Sayfayı kapatın.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Üretim denetimi &gt; Üretim emirleri &gt; Tüm üretim emirleri'ne gidin.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Yeni üretim emri'ne tıklayın.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Madde numarası alanında &#39;L0101&#39; girin.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Oluştur'a tıklayın.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Eylem Bölmesinde, Üretim emri öğesine tıklayın.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Tahmin seçeneğine tıklayın.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Tamam'ı tıklatın.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Başlat'a tıklayın.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Genel sekmesine tıklayın.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Otomatik malzeme listesi tüketimi alanında, &#39;Hiçbir zaman&#39; seçin.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Tamam'a tıklayın.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Tamamlandı olarak bildir öğesine tıklayın.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Genel sekmesine tıklayın.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Kabul hatası alanında Evet'i seçin.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Tamam'ı tıklatın.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Eylem Bölmesinde, Ambar öğesine tıklayın.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>İş ayrıntıları öğesine tıklayın.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Üretim emri, tamamlandı olarak rapor edilmişse, hiçbir iş üretilmez. Bu durum, Ürün L0101, konum 001'e bitirildi olarak rapor edildiğinde işin oluşturulmasının engellenmesi için tanımlanan bir iş politikası bulunmasından kaynaklanır.</td>
</tr>
</tbody>
</table>




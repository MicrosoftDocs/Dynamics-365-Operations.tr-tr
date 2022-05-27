---
title: Faturalama zamanlamaları sonlandırma
description: Bu konuda, Abonelik faturalamasında faturalama zamanlamalarının ve faturalama zamanlama satırlarının nasıl sonlandırılacağı açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e823ce950d6a4687dc7cda14e06bffdbb4f37f7e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690990"
---
# <a name="terminate-billing-schedules"></a>Faturalama zamanlamaları sonlandırma

[!include [banner](../includes/banner.md)]

Bu konuda, Abonelik faturalamasında faturalama zamanlamalarının ve faturalama zamanlama satırlarının nasıl sonlandırılacağı açıklanmaktadır. Faturalama zamanlamasını sonlandırabilmeniz için durumunun **Etkin** olması gerekir. Durumu **Beklemede** olmamalıdır. Benzer şekilde, bir faturalama zamanlama satırını sonlandırabilmeniz için durumunun **Etkin** olması gerekir. Bir faturalama zamanlama satırını sonlandırdığınızda faturalama zamanlamasının başlık bölümü etkilenmez.

Faturama zamanlamasını veya faturalama zamanlama satırını sonlandırmak için aşağıdaki konumlardan birine gidin:

- **Tüm/Ekin faturalama zamanlamaları** liste sayfası
- **Tüm faturalama zamanlamaları** sayfasındaki belirli bir faturalama planı
- **Tüm faturalama zamanlamaları** sayfasındaki belirli bir faturalama zamanlama satırı

> [!NOTE]
> Aynı anda birkaç faturalama zamanlamasını sonlandırmak istiyorsanız **Toplu sonlandırma işleme** sayfasını kullanın.

## <a name="terminate-a-billing-schedule-or-line"></a>Faturalama zamanlamasını veya satırını sonlandırma

Faturama zamanlamasını veya faturalama zamanlama satırını sonlandırmak için aşağıdaki adımları izleyin.

1. Faturalama zamanlaması veya faturalama zamanlama satırı seçin ve ardından **Sonlandır**'ı seçin. 
2. **Sonlandırma tarihi**, **Sonlandırma türü** ve **Neden kodu** alanlarını ayarlayın.
3. **Kredi seçeneği** alanını **Alacak faturası düzenle** olarak ayarlayın.
4. **Sonlandır**'ı seçin.

Faturalama zamanlamasının durumu, seçtiğiniz sonlandırma türüne göre değişir. Sonlandırma türü olarak **Kalan fatura**'yı öğesini seçtiyseniz faturalama zamanlamasındaki tüm satırların durumu **Son faturalama** olur. Faturalama zamanlamasının durumu, son fatura işlenene kadar **Etkin** kalır. Durum, son fatura işlendikten sonra **Sonlandırıldı** olarak güncelleştirilir. Sonlandırma türü olarak **Zamanlamayı ayarla**'yı seçtiyseniz faturalama zamanlamasının durumu hemen **Sonlandırıldı** olarak güncelleştirilir.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Faturalama zamanlamasını veya satırını sonlandırma ve geri ödeme yapma

Faturama zamanlamasını veya faturalama zamanlama satırını sonlandırmak be geri ödeme yapmak için aşağıdaki adımları izleyin.

1. Faturalama zamanlaması veya faturalama zamanlama satırı seçin ve ardından **Sonlandır**'ı seçin.
2. **Sonlandırma tarihi**, **Sonlandırma türü**, **Neden kodu** ve **Kredi seçeneği** alanlarını ayarlayın.
3. **Geri ödeme ile sonlandır**'ı seçin. **Toplu sonlandırma işleme** sayfası görüntülenir ve faturalama zamanlamasını görüntüleyecek şekilde filtrelenir.
4. Faturalama zamanlamaları satırlarını görüntülemek için **Önizlemeyi görüntüle**'yi seçin ve ardından **İşlem**'i seçin.

Kredi işlendikten sonra faturalama zamanlamasına uygulanan krediyi gözden geçirmek için **Fatura ayrıntısını görüntüle** sayfasını açın. Kredi tutarı 0'dan (sıfır) fazlaysa gelecekteki tüm faturalanmamış satırlar silinir ve faturalama zamanlamasına uygulanan kredi için eksi tutarları gösteren fatura ayrıntısı satırları ile değiştirilir.

### <a name="view-example"></a>Örneği görüntüle

Faturalama zamanlaması aşağıdaki bilgileri içerir:

- Başlangıç tarihi 1 Ocak 2020'dir.
- Bitiş tarihi 31 Aralık 2020'dir.
- Faturalama dönemi tutarı aylık 100,00 TL'dir.
- Ocak ile Temmuz ayları arasındaki faturalama dönemleri için faturalar oluşturulmuştur.
- Sözleşme fesih tarihi 15 Haziran 2020'dir.

Kredi düzeltmesi işlendiğinde gelecekteki tüm fatura dönemleri (Ağustos-Aralık arası) **Fatura ayrıntısını görüntüle** sayfasından kaldırılır. Temmuz faturalama döneminden sonrasına bir kredi düzeltme satırı eklenir:

- 16 Haziran – 31 Temmuz, kredi tutarı 150,00 TL

Faturalanmamış gelir özelliği kullanılıyorsa **Faturalanmamış gelir yevmiye defteri girişi denetimi** sayfası, sonlandırma girişiyle güncelleştirilir.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Kredi uygulamadan faturalama zamanlaması veya satırı sonlandırma

Faturalama zamanlamasını veya faturalama zamanlama satırını kredi uygulamadan sonlandırmak için aşağıdaki adımları izleyin.

1. Faturalama zamanlaması veya faturalama zamanlama satırı seçin ve ardından **Sonlandır**'ı seçin.
2. **Sonlandırma tarihi** alanını ayarlayın.
3. **Sonlandırma türü** alanını **Düzeltme yok** olarak ayarlayın. **Kredi seçeneği** alanı otomatik olarak **Kredi yok** olarak ayarlanır.
3. **Neden kodu** alanını ayarlayın.
4. **Sonlandırma notları** alanında, gerekli olan notları girin.
5. **Sonlandır**'ı seçin. 

Sonlandırma işlendiğinde sonlandırma tarihinden sonraki tüm faturalama ayrıntısı satırları kaldırılır. (Bu satırlar bitiş tarihinin dahil olduğu satırı içerir.) Sonlandırılan satırlar için fatura oluşturulamaz. Sonlandırma kaldırılırsa sonlandırılan tüm satırlar **Fatura ayrıntılarını görüntüle** sayfasına geri eklenir ve faturalama için kullanılabilir hale gelir.

## <a name="fields"></a>Alanlar

**Fatura ayrıntılarını görüntüle** sayfası, aşağıdaki alanları içerir.

| Alan | Açıklama |
|-------|-------------| 
| Ayrılma tarihi | Faturalama zamanlamasını veya faturalama zamanlama satırını sonlandırmak istediğiniz tarihi seçin. |
| Sonlandırma türü | <p>Sonlandırma türünü seçin:</p><ul><li>**Zamanlamayı ayarla**: Sonlandırma tarihinde satırın faturalama dönemlerini kesin ve satırın durumunu **Son faturalama** olarak değiştirin. Satır öğesi için bir erteleme zamanlaması varsa artık dikkate alınmaması gereken tutar tersine çevrilerek ayarlanır. Faturalama başlangıç tarihi bitiş tarihinden sonraysa kalan faturalama dönemleri kaldırılır.</li><li>**Kalan fatura**: Faturalama dönemi için kalan tutarı sonlandırma dönemine ekleyin ve satırın durumunu **Son faturalama** olarak değiştirin. Satır öğesi için bir erteleme zamanlaması varsa erteleme bitiş tarihi güncelleştirilir. Faturalama başlangıç tarihi bitiş tarihinden sonraysa kalan tüm faturalama dönemlerinin toplam tutarı faturalama dönemine eklenir ve kalan faturalama dönemleri kaldırılır.</li><li>**Düzeltme yok**: Belirtilen sonlandırma tarihinde satırın faturalama dönemlerini sonlandırın. Herhangi bir düzeltme yapılmaz. Bu sonlandırma türü seçildiğinde **Kredi seçeneği** alanı **Kredi yok**, **Günlük olarak dağıt** alanı **Hayır** olarak ayarlanır. Her iki alan da daha sonra salt okunur hale gelir ve değiştirilemez.</li></ul> |
| Alacak seçeneği | <p>Faturalama zamanlama satırını sonlandırdığınızda kredinin nasıl uygulanacağını seçin:</p><ul><li>**Kredi düzeltmesi**: Bir satır sonlandırıldığında faturalama zamanlaması için bir kredi düzeltmesi oluşturun. Kredi düzeltmesi, faturalama zamanlaması için gelecekteki bir faturalama döneminde görüntülenir. Düzeltme ayrıca, kredinin faturalama zamanlamasına uygulanması bitene kadar bir sonraki faturalama dönemi için fatura tutarını otomatik olarak ayarlar.</li><li>**Alacak faturası düzenle**: Faturalama zamanlaması veya faturalama zamanlama satırı sonlandırıldığında bir alacak dekontu oluşturun.</li><li>**Kredi yok**: Faturalama zamanlaması veya faturalama zamanlama satırı sonlandırıldığında kredi düzeltmesi veya alacak dekontu oluşturmayın. Bu seçenek yalnızca bir faturalama zamanlamasını sonlandırmak için **Düzeltme yok** türünde bir sonlandırma kullandığınızda değerlendirilebilir.</li></ul><p>Varsayılan seçenek, **Yinelenen sözleşme faturalama parametreleri** sayfasındandır.</p> |
| Neden kodu | Sonlandırma için neden kodunu seçin. |
| Neden açıklaması | Neden kodunun açıklaması. |
| Sonlandırma notları | Sonlandırma hakkında notunuz varsa girin. |

<!--## Additional information-->

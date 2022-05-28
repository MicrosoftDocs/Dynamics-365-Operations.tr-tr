---
title: Kiralamaları sabit varlıklarla ilişkilendirme
description: Bu konuda, mevcut bir sabit varlığın yeni bir kiralamayla nasıl ilişkilendirileceği açıklanır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0ae7a850ceb13cb41ee5adc406e71105cdad4fe
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712160"
---
# <a name="associate-fixed-assets-with-leases"></a>Kiralamaları sabit varlıklarla ilişkilendirme

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, mevcut bir sabit varlığın yeni bir kiralamayla nasıl ilişkilendirileceği açıklanır. Bir sabit varlığı kiralamayla ilişkilendirdiğinizde, ilk kabuldeki kullanım hakkı (ROU) varlığı sabit varlığın alım maliyeti olur.

Sabit bir varlığı kiralamayla ilişkilendirmeden önce Sabit varlıklarda sabit varlık için bir kayıt oluşturmanız gerekir. Ardından, **Kiralama özeti** sayfasında kiralama oluşturmanız ve varlığı bu kiralamaya bağlamanız gerekir.

1. [Kiralama ekleme veya kopyalama](add-lease.md) konu başlığındaki adımları izleyerek kiralama ekleyin. **Kiralama ekle** sayfasındaki **Sabit varlık numarası** alanında henüz alınmamış olan varlığı seçin.
2. **Defterler**'i seçin ve ödeme planını onaylayın.
3. **İlk kabul**'ü seçin.
4. **Varlık kiralama günlüğü**'nü seçin.

    Kiralama için ilk kabul günlüğü girişi, genellikle ROU varlığı hesabına borçlandırılan tutar için sabit varlığı borçlandırır.

    Sabit varlıkla ilgili hareket türü ve defteri artık görüntüleyebilirsiniz.

5. **Günlük ayrıntılar**'ı seçin.
6. Günlük girişiyle ilgili ayrı satırları görüntülemek için **Satırlar**'ı seçin.
7. Varlığı içeren günlük girişini seçin ve ardından **Sabit Varlıklar** sekmesini seçin.

    **Sabit varlıklar** sekmesi hareket türünü ve defteri gösterir. Varsayılan olarak, **Hareket türü** alanı **Alım** olarak ayarlanır, **Defter** alanı sabit varlık için geçerli defter olarak ayarlanır.

İlk kabul günlüğü girişi deftere nakledildikten sonra, hareket sabit varlık için alım hareketi olarak görünür. Hareket tablosunu görüntülemek için **Sabit varlıklar \> Sabit varlıklar \> Sabit varlıklar** bölümüne gidin, uygun varlığı seçin ve **Değerlemeler**'i seçin. İlk kabul günlüğü girişinde belirtilen sabit varlık için bir alım hareketi oluşturulduğu görebilirsiniz.

Artık Sabit varlıklardaki standart amortisman işlevi kullanılarak sabit varlığa amortisman uygulanabilir. Amortisman hakkında daha fazla bilgi için bkz. [Amortisman yöntemleri ve kuralları](../fixed-assets/depreciation-methods-conventions.md).

Kiralama, sabit kıymetle ilişkilendirildiğinde sabit kıymet defterindeki **Servis ömrü** alanı aşağıdaki ölçütlerden en küçük değerle uyumlu olacak şekilde güncelleştirilir: 

 - Varlığın faydalı ömrü
 - İlişkili kiralama defterindeki kiralama süresi

Kiralama defteri için **Sahiplik aktarımı** alanı **Evet** olarak ayarlanmışsa **Servis ömrü** alanındaki değer her zaman varlığın faydalı ömrü olur. 
 
Varlık kiralama sırasında kullanım hakkı varlığına uygulanan amortismanda olduğu gibi, kullanım hakkı varlığına süreli kiralama boyunca amortisman uygulanmasını sağlamak için kiralamanın her ayarlanışında Servis ömrü güncelleştirilir.

> [!NOTE]
> Sabit varlığı bir kiralamayla ilişkilendirirseniz Varlık kiralamada **Varlık amortismanı** ve **Kira değer düşüşü** düğmeleri devre dışı bırakılır. Sabit varlıklardaki varlık amortismanı ve kira değer düşüşü hareketlerini görüntüleyebilirsiniz. Bir sorgu formu açan **Varlık hareketleri** düğmesi de devre dışı bırakılır. **Varlık hareketleri** sorgu formunu Sabit varlıklarda da açabilirsiniz.  

**Sabit kıymetler** ve **Sabit kıymet defteri** sayfaları, bir sabit kıymetle ilişkili kiralama kimliğini görüntüler. Sabit kıymet bir kiralama ile ilişkilendirilmişse **Sabit kıymetler** sayfasındaki **Kiralama bilgileri** hızlı sekmesinde kiralama kimliği ve kiralama açıklaması görüntülenir. Kiralama defterleriyle ilişkili sabit kıymet defterleri için **Kiralama kimliği**, **Kiralama açıklaması** ve **Defter türü** alanları, bir kiralama defteriyle ilişkili olduklarını belirtmek için **Kiralama bilgileri** hızlı sekmesinde seçilen sabit kıymet defterine ilişkin bilgileri görüntüler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

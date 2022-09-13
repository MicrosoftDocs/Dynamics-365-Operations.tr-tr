---
title: Satış ve transfer satırı çekme özel durumlarını el ile işleme
description: Bu makalede, bozuk satış ve transfer emri verilerinin neden olduğu sorunları gidermek amacıyla yöneticilerin stok hareketlerini nasıl el ile çekebileceği veya (çekme işlemini geri alabileceği) anlatılmaktadır.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403704"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Satış ve transfer satırı çekme özel durumlarını el ile işleme

[!include [banner](../includes/banner.md)]

Satış ve transfer satırı çekme istisnalarının el ile yönetilmesi, yöneticilerin bozuk satış ve transfer emri verilerinin neden olduğu sorunları çözmesine olanak tanır. Bu, ambar işlemleri devam ederken, güvenilen kullanıcıların satış ve transfer emri satırlarıyla ilişkili stok hareketlerini el ile çekmesini (veya çekme işlemini geri almasını) sağlar.

Burada açıklanan işlevsellik, sistemin her zamanki şekilde ambar işlemleri yığınını işlemeyi tamamlayamadığı durumlarda kullanılmalıdır. Varsayılan olarak, yalnızca sistem yöneticisi rolüne sahip kullanıcıların bunu kullanmasına izin verilir. Ancak, gereksinim duyduğunuz gibi *Satış satırlarını el ile çek* ayrıcalığını başka rollere atayarak işleve erişim izni verebilirsiniz.

## <a name="turn-on-this-feature-for-your-system"></a>Sisteminiz için bu özelliği etkinleştirme

Bu makalede açıklanan özellikleri kullanabilmeniz için ilgili özelliğin sisteminizde açılmış olması gerekir. Yöneticiler, özelliklerin durumunu kontrol etmek ve açmak için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanında bu özellikler aşağıdaki adlar kullanılarak listelenir:

- *Yönetici veya benzer güvenilen kullanıcılar için el ile satış satırı çekme hizmeti*<br>(Supply Chain Management sürüm 10.0.25 itibarıyla, bu özellik zorunludur ve kapatılamaz.)
- *Yönetici veya benzer güvenilen kullanıcılar için el ile transfer satırı çekme hizmeti*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Satış veya transfer emri satırlarıyla ilgili hareketleri düzeltme

Satış veya transfer emri satırlarıyla ilgili hareketleri düzeltmek için aşağıdaki yordamı kullanın.

1. Düzeltmek istediğiniz emrin türüne bağlı olarak şu adımlardan birini izleyin:

    - Bir satış siparişiyle ilişkili bir hareketi düzeltmek için, **Ambar yönetimi \> Periyodik görevler \> Temizleme \> Satış satırını el ile çek**'e gidin.
    - Bir transfer emriyle ilişkili bir hareketi düzeltmek için, **Ambar yönetimi \> Periyodik görevler \> Temizleme \> Transfer satırlarını el ile çek**'e gidin.

1. **Satış satırlarını el ile çek** veya **Transfer satırlarını el ile çek** sayfasında, aradığınız satırı bulmak için kılavuzun üst kısmındaki filtreleri kullanın ve daha sonra üst kılavuzdaki hedef sipariş satırını seçin.
1. Seçili satırla ilgili daha fazla bilgi görüntülemek için alt bölümdeki **Stok hareketleri**, **Yükleme satırları**, **İş satırları** ve **Konteyner satırları** sekmelerini kullanın. Bu sekmelerdeki bilgiler, ilgili ambar süreçleri ve durumlarına ilişkin temel bir genel bakış sağlar.
1. Eylem Bölmesi'nde, stok hareketleri için **Çekme** sayfasında seçili sipariş satırını açmak için **Çek**'i seçin. Ambarda serbest bırakılmış sipariş satırları için de bu adımı tamamlayabilirsiniz. (Genellikle, ambarda serbest bırakılan sipariş satırları **Çekme** sayfasında açılamaz.)

    > [!NOTE]
    > **Çekme** sayfasını açtığınızda çeşitli uyarılar alabilirsiniz. Bu uyarıların önerdiği tüm eylemleri gerçekleştirin. Örneğin, ambar çalışmasına bağlı sipariş satırlarıyla ilgili bir uyarı alabilirsiniz. Bu durumda, el ile düzeltmeyi gerçekleştirmeden önce standart [iş iptali](cancel-warehouse-work.md) işlevini kullanarak işi iptal etmeyi denemek mantıklıdır.

1. **Hareketler** kılavuzundaki satırı seçin ve sonra **Hareketler** araç çubuğunda **Malzeme çekme satırı ekle**'yi seçin.
1. Seçili satır, **Malzeme çekme satırları** kılavuzuna taşınacaktır. Gerekli bilgileri eksik olan sütunlar için uygun değerleri ayarlayın. (Örneğin, maddenin çekilmesi/geri alınması gereken konumu ve plakayı belirtin.)
1. **Malzeme çekme satırları** bölümünde, **Tümünü çekmeyi onayla**'yı seçin.

## <a name="correct-load-line-quantities"></a>Yük satır miktarlarını düzeltme

Bir yük satırı miktarını düzeltmek için aşağıdaki yordamı kullanın.

1. Düzeltmek istediğiniz emrin türüne bağlı olarak şu adımlardan birini izleyin:

    - Bir satış siparişiyle ilişkili bir hareketi düzeltmek için, **Ambar yönetimi \> Periyodik görevler \> Temizleme \> Satış satırını el ile çek**'e gidin.
    - Bir transfer emriyle ilişkili bir hareketi düzeltmek için, **Ambar yönetimi \> Periyodik görevler \> Temizleme \> Transfer satırlarını el ile çek**'e gidin.

1. **Satış satırlarını el ile çek** veya **Transfer satırlarını el ile çek** sayfasında, aradığınız satırı bulmak için kılavuzun üst kısmındaki filtreleri kullanın ve daha sonra üst kılavuzdaki hedef sipariş satırını seçin.
1. Alt bölümdeki **Yük satırları** sekmesinde, araç çubuğunda **Yük satırlarını el ile düzelt**'i seçin.
1. **Yük satırlarını el ile düzelt** sayfasında, **Stok hareketleri** kılavuzunda, seçili yük satırıyla ilişkili stok hareketlerini gözden geçirin.
1. Üstteki kılavuzda, aşağıdaki sütunlardaki yük satırı miktarlarını gerektiği gibi düzeltin:

    - **Oluşturulan iş miktarı**
    - **Çekilen miktar**
    - **Planlanmış çapraz sevk miktarı**

    Sistem, bu sütunlarda yaptığınız tüm değişiklikleri doğrular.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

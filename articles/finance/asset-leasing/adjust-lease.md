---
title: Kiralamaları düzeltme
description: Bu konuda, kiralamaların nasıl düzeltileceği açıklanmaktadır. Kiralama süreleri değiştirilirse, kiralama süresi uzatılırsa veya başka koşullar değişirse düzeltme gerekebilir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449026"
---
# <a name="adjust-leases"></a>Kiralamaları düzeltme

[!include [banner](../includes/banner.md)]

Bu konuda, kiralamaların nasıl düzeltileceği açıklanmaktadır. Kiralama süreleri değiştirilirse, kiralama süresi uzatılırsa veya başka koşullar değişirse düzeltme gerekebilir. Varlık kiralama, Muhasabe Standartları Kodlaması Konu 842 (ASC) ve Uluslararası Mali Raporlama Standardı 16 (IFRS 16) belgelerinde kiralama değişiklikleriyle ilgili olarak sağlanan kılavuza uyar. ASC 842-20-15-1, kiralama değişikliğini kiralamanın kapsamında veya değerlendirilmesinde değişikliğe neden olan sözleşme hüküm ve koşullarındaki herhangi bir değişiklik olarak tanımlar. IFRS 16'nın 39. paragrafında, kiracının kiralama yükümlülüğünü kira ödemelerini yansıtacak şekilde değiştirmesi gerektiği belirtilir.

ASC 842 veya IFRS 16'ya bağlı olan kuruluşlar için kiralama, gelecekteki en düşük kira ödemelerinin (PVFMLP) şimdiki değerindeki değişikliği yansıtacak şekilde yeniden ölçülür. PVFMLP arttıkça oluşturulan günlük girişi yeni PVFMLP ile eski PVFMLP arsındaki fark için kullanım hakkı varlığı (ROU) açısından borç ve kiralama yükümlüğü açısından alacak olacaktır. PVFMLP azaldıkça günlük girişi fark için kiralama yükümlüğü açısından borç ve ROU varlığı açısından alacak olacaktır.

Düzeltme ROU varlığını 0 (sıfır) değerinden daha aşağıya düşürürse kalan tutar, **Kira deftere nakil hesapları** sayfasında belirtilen kiralama değişikliği nakil hesabının kazancına alacak olarak kaydedilecektir. Sistem, bu hareketleri ve sınıflandırma değişiklikleri, başlangıçtaki doğrudan maliyetler, kiralama teşvikleri, ön ödemeler ve kiralama değişikliklerinden doğan parçalara ayırma maliyetleri gibi diğer düzeltme girişlerini de hesaplar.

Kiralama düzeltme hareketleri hakkında özel bir kılavuz için IFRS 16 ve ASC 842 belgelerini incelemenizi öneririz.

Kiralamayı düzenlemek için bu adımları izleyin. Değiştirilen veriler, Planlama oluştur işlemi çalıştırıldıktan sonra kiralama planlarını güncelleştirir.

1. **Varlık kiralama \> Kiralamalar \> Kiralama özeti**'ne gidin.
2. **Kiralama özeti** sayfasında, düzenlenecek kirayı seçin ve ardından **Kiralamayı düzelt**'i seçin.
3. **Kiralamayı düzelt** sayfasında düzeltilen kiralamaya ilişkin yeni bilgileri girin.

    **Kiralamayı düzelt** sayfasının **Kiralama ekle** sayfasına benzediğinizi görebilirsiniz. Ek olarak, bir kira eklediğinizde belirttiğiniz başlangıç tarihinin yeni kiralamanın ne zaman başlayacağını belirlemesi gibi, **Kiralamayı düzelt** sayfasındaki **Değiştirme tarihi** alanı da değiştirilen kiralamanın ne zaman başlayacağını belirler. Bu tarih, ödeme planı satırlarındaki başlangıç tarihinden sonra olamaz.

    > [!NOTE]
    > **ROU ile ilgili konular** alanları bu kiralama düzeltmesine uyar. Değiştirilmiş kira ile ilişkilendirilmiş başlangıçtaki doğrudan maliyetler, kiralama teşvikleri, ön ödemeler veya parçalara ayırma maliyetleri yoksa bu alanları boş bırakmanız gerekir. Özgün tutarlar güncelleştirilmiş kiralamaya uygulanmaz. Kiralama değiştirildiğinde oluşan tüm ek maliyetler **Kiralamayı düzelt** sayfasına girilmelidir.
    > 
    > Örneğin, kiraya verenin kiralamanın uzatılmasının kabul edilmesi için 1.000 ABD doları teşvik sağladığını düşünelim. Bu durumda, uzatmayı dahil etmek için kiralamayı düzelttiğinizde **Kiralama teşvikleri** alanına **1.000** rakamını girersiniz. Kiralama düzeltmeyle ilişkili bir teşvik yoksa daha önce bu alana girilmiş olan tüm değerleri temizlemeniz gerekir. Aynı mantık ROU ile ilgili konular için de geçerlidir.

    Düzeltilmiş kiralamanın ödeme planı satırları ileriye yönelik olarak oluşturulmalıdır. İleriye yönelik olarak oluşturulan ödeme planı satırları, kiralama değişiklikleri geçerli olmadan önce başlatılamaz.

    Aşağıdaki adımlar, kiralamanın ilk kabulüyle ile ilgili adımlarla neredeyse aynıdır.

4. Düzeltilen ödeme planını oluşturmak için **Planlama oluştur**'u seçin. Kiralama için ödeme planının oluşturulduğuna dair bir ileti alırsınız.

    > [!IMPORTANT]
    > **Planlama oluştur**'u seçmeden önce değiştirme tarihinin ve ödeme planı satırlarının doğru olduğundan emin olun. Ayrıca, tüm başlangıçtaki doğrudan maliyetlerin, kiralama teşviklerinin, ön ödemelerin veya parçalara ayırma maliyetlerinin yalnızca bu düzeltmeden doğan maliyetlere karşılık geldiğinden emin olun.

5. Yeni oluşturulan ödeme planını görüntülemek için **Defterler**'i seçin ve **Ödeme planı** sayfasını açın.
6. **Ödeme planı** sayfasında, ödeme planını onaylamadan önce düzeltilen ödeme tutarlarını düzenleyebilirsiniz. Planı onaylamak için **Planlamayı onayla**'yı seçin.

    Ödeme planı onaylandığında yeni varlık amortismanı ve yeni kiralama yükümlülüğü planlamaları oluşturulur.

7. Yeni girişler tarafından oluşturulan yeni kiralama yükümlüğü amortismanı planlamasını görüntülemek için **Ödeme planı** sayfasını kapatın ve **Yükümlülük amortisman planlaması** sayfasını açın.
8. Yeni oluşturulan varlık amortisman planlamasını görüntülemek için **Defter ayrıntıları** sayfasından **Varlık amortisman planlaması** sayfasını açın.
9. Düzeltme günlüğü girişini oluşturmak için **İşlev \> Kiralama düzeltmesi**'ni seçin. Düzeltme günlüğü girişinin oluşturulduğuna dair bir ileti alırsınız. 
10. Günlük girişini görüntülemek için **Günlükler \> Varlık kiralama günlüğü**'nü seçin.
11. Günlük girişini deftere nakletmek için satırı seçin ve **Deftere naklet**'i seçin.

## <a name="view-lease-versions"></a>Kiralama sürümlerini görüntüleme

Kiralama değiştirilmişse kiralamanın farklı sürümlerini görebilirsiniz. Ayrıca geçmiş planları ve geçmiş kiralama ayrıntılarını da görebilirsiniz.

1. **Kiralama özeti** sayfasında, kiralamayı seçin ve sonra Eylem Bölmesinde **Kiralama sürüm geçmişi**'ni seçin.

    Seçilen kiralama düzeltilmişse **Kiralama sürüm geçmişi** sayfası kiralamanın farklı sürümlerini gösterir. Özgün kiralama **1** ile, sonraki sürümler ile artan numara sırasıyla etiketlenir.

    Seçili bir kira sürümünün mali boyutlarını, sözleşme ayrıntılarını, konumunu ve ödeme planı satırlarını görüntüleyebilirsiniz.

2. Geçmiş planlamaları görüntülemek için **Kiralama özeti** sayfasından değiştirilen kiralamayı açın, istediğiniz defteri seçin ve ardından Eylem Bölmesinde **Defter sürüm geçmişi**'ni seçin.
3. **Defter sürümü** sayfasında, görüntülemek istediğiniz sürümü ve planlamayı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
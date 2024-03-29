---
title: Kiralamaları düzeltme
description: Bu makalede, kiralamaların nasıl düzeltileceği açıklanmaktadır. Kiralama süreleri değiştirilirse, kiralama süresi uzatılırsa veya başka koşullar değişirse düzeltme gerekebilir.
author: moaamer
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 48d1a261a43d6e3a68dfc0aae6f06c0d7d6b82db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898341"
---
# <a name="adjust-leases"></a>Kiralamaları düzeltme

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, kiralamaların nasıl düzeltileceği açıklanmaktadır. Kiralama süreleri değiştirilirse, kiralama süresi uzatılırsa veya başka koşullar değişirse düzeltme gerekebilir. Varlık kiralama, Muhasabe Standartları Kodlaması Konu 842 (ASC) ve Uluslararası Mali Raporlama Standardı 16 (IFRS 16) belgelerinde kiralama değişiklikleriyle ilgili olarak sağlanan kılavuza uyar. ASC 842-20-15-1, kiralama değişikliğini kiralamanın kapsamında veya değerlendirilmesinde değişikliğe neden olan sözleşme hüküm ve koşullarındaki herhangi bir değişiklik olarak tanımlar. IFRS 16'nın 39. paragrafında, kiracının kiralama yükümlülüğünü kira ödemelerini yansıtacak şekilde değiştirmesi gerektiği belirtilir.

ASC 842 veya IFRS 16'ya bağlı olan kuruluşlar için kiralama, gelecekteki en düşük kira ödemelerinin (PVFMLP) şimdiki değerindeki değişikliği yansıtacak şekilde yeniden ölçülür. PVFMLP arttıkça oluşturulan günlük girişi yeni PVFMLP ile eski PVFMLP arsındaki fark için kullanım hakkı varlığı (ROU) hesabı açısından borç ve kiralama yükümlüğü hesabı açısından alacak olacaktır. PVFMLP azaldıkça günlük girişi fark için kiralama yükümlüğü hesabı açısından borç ve ROU varlığı hesabı açısından alacak olacaktır.

Düzeltme ROU varlığını 0 (sıfır) değerinden daha aşağıya düşürürse kalan tutar, **Kira deftere nakil hesapları** sayfasında belirtilen kiralama değişikliği nakil hesabının kazancına alacak olarak kaydedilecektir. Sistem, bu hareketleri ve sınıflandırma değişiklikleri, başlangıçtaki doğrudan maliyetler, kiralama teşvikleri, ön ödemeler ve kiralama değişikliklerinden doğan parçalara ayırma maliyetleri gibi diğer düzeltme girişlerini de hesaplar.

Kiralama düzeltme hareketleri hakkında özel bir kılavuz için IFRS 16 ve ASC 842 belgelerini incelemenizi öneririz.

## <a name="lease-adjustment-wizard"></a>Kiralama düzeltmesi sihirbazı

Kiralama düzeltmek için aşağıdaki adımları tamamlayın. Değiştirilen veriler, **Kira düzeltme** sihirbazından deftere nakledildikten sonra kira zamanlamalarını güncelleştirir. Çalışmanızı kaydedebilir ve sihirbazı istediğiniz zaman kapatabilir ve daha sonra çalışmanıza devam etmek için geri gelebilirsiniz.

Kira düzeltmeleri sayfasından **Kira düzeltme** sihirbazını açmak için bu adımları izleyin.

1. **Varlık kiralama \> Kiralamalar \> Kiralama özeti**'ne gidin. 
2. Düzeltilecek kiralamayı seçin ve ardından **Düzeltme sihirbazı**'nı seçin.
3. Gerekli değişiklikleri girmek için sihirbazdaki istemleri izleyin.

**Kira düzeltme** sihirbazını **Kira ayarlamaları** sayfasından açmak için devam etmekte olan bir ayarlamada şu adımları izleyin.

1.  **Kira \> Kiralamalar \> Kiralama düzeltmeleri**'ne gidin.
2.  **Devam ediyor** düzeltme durumuna sahip bir kira seçin ve ardından **Düzeltme sihirbazı**'nı seçin.
3.  **Değişiklik başlangıç tarihi** ve **Deftere nakil tarihi** alanlarına uygun tarihleri girin.
4.  **Sonraki**'yi seçin.

    Kiralama artık, hakkında yeni bilgiler girebileceğiniz **Kira düzeltmeleri** sayfasına eklenir.

    Kiralama ayarlandıktan sonra, kullanım hakkı ile ilgili alanlar bu alan için geçerlidir. Değiştirilmiş kira ile ilişkilendirilmiş başlangıçtaki doğrudan maliyetler, kiralama teşvikleri, ön ödemeler veya parçalara ayırma maliyetleri yoksa karşılık gelen alanları boş bırakın. Özgün tutarlar güncelleştirilmiş kiralamaya uygulanmaz. 

    Örneğin, kiraya verenin kiralamanın uzatılmasının kabul edilmesi için 1.000 ABD doları teşvik sağladığını düşünelim. Bu durumda, uzatmayı dahil etmek için kiralamayı düzelttiğinizde **Düzeltmeden doğan kiralama teşvikleri** alanına **1.000** rakamını girin.

    Ödeme planı satırları artık **Değişiklik başlangıç tarihi** alanında ay ve sonraki aylardaki tüm ödemeleri gösterir. Değişiklikler olası olduğundan, ödeme planı satırları değişiklik başlamadan önce başlatılamaz. Değişiklik başlangıç tarihinden önce ödeme planı satırlarını görüntülemek için **Kira sürümü geçmişi** sayfasına gidin.

8.  **Sonraki**'yi seçin.

    Bir sonraki sayfada, değişiklik öncesi kira yükümlülüğünün taşıma değerleri ve değişiklik sonrası beklenen yeni kira yükümlülüğü gibi beklenen kira düzeltmesi ile ilgili önemli ayrıntılar gösterilmektedir. Sayfada, beklenen kira düzeltmesi için günlük girişinin önizlemesi de gösterilir.

9.  Kira düzeltmesi iş akışı etkinse ve düzeltme henüz onaylanmamışsa, kira düzeltmesini iş akışı sistemine göndermek için **İş akışına gönder**'i seçin. Kira düzeltmesi şş akışının nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [Kira düzeltmeleri iş akışlarını kullanma](use-create-lease-wrkflw.md).

    > [!NOTE]
    > Bu noktada sistem, düzeltmeye genel bakış ve düzeltme günlüğü girişinin ilk hesaplanmasından bu yana kiraya karşı hiçbir hareketin deftere nakledilmediğini doğrulamak için düzeltme değişkenlerini yeniden hesaplar. Herhangi bir değer değişirse, düzeltmeye genel bakış kılavuzu güncelleştirilir ve kira düzeltmelerini iş akışı sistemine yeniden göndermeden önce bilgileri gözden geçirebilirsiniz.

10. Bir iş akışı etkin değilse veya kira düzeltmesi onaylandıysa, değişiklikleri işlemek ve düzeltme günlüğü girişini deftere nakletmek için **Bitir**'i seçin.

    > [!NOTE] 
    > Bu noktada sistem, düzeltmeye genel bakış ve düzeltme günlüğü girişinin ilk hesaplanmasından bu yana kiraya karşı hiçbir hareketin deftere nakledilmediğini doğrulamak için düzeltme değişkenlerini yeniden hesaplar. Herhangi bir değer değişirse düzeltmeye genel bakış kılavuzu güncelleştirilir ve **Bitir**'i seçmeden önce değişiklikleri gözden geçirebilirsiniz. İş akışı etkinse ve kira düzeltmesi onaylandıysa, düzeltmeye genel bakışta yapılacak değişiklikler onay durumunun yeniden **Gönderilmedi** olarak ayarlanmasına neden olur. Bu durumda, kira düzeltmesini iş akışı sistemine yeniden göndermeniz gerekir.

    **Kira düzeltmeleri** sayfasında, düzeltme durumu artık **Tamamlandı** olarak ayarlanır.

    **Kira düzeltmeleri** sayfasında, **Düzeltmeye genel bakış** ve **Düzeltme girişi önizlemesi** hızlı sekmelerini görüntülemeye devam edebilirsiniz. Kira ayrıntıları ve tarih bilgileri, ilgili kiralamanın sürüm geçmişinde gösterilir.

    Artık değiştirilen bilgiler kullanılarak yeni bir kira sürümü ve yeni bir zamanlama kümesi oluşturulur. 

13. Yeni zamanlamaları görüntülemek için kiralamaya gidin ve **Defterler**'i seçin.
14. Yeni oluşturulan ödeme çizelgesini görüntülemek için **Ödeme planı**'nı seçin.
15. Yeni bilgilerden oluşturulan yeni kiralama yükümlüğü amortismanı planlamasını görüntülemek için **Ödeme planı** sayfasını kapatın ve **Yükümlülük amortisman planlaması** sayfasını açın.
16. Yeni oluşturulan varlık amortisman planlamasını görüntülemek için **Defter ayrıntıları** sayfasından **Varlık amortisman planlaması** sayfasını açın.
17. Düzeltme günlüğü girişini görüntülemek için **Günlükler \> Varlık kiralama günlüğü**'nü seçin.

## <a name="cancel-a-lease-adjustment"></a>Kira düzeltmesini iptal etme

Devam eden bir kira düzeltmesini silmek için bu adımları izleyin.

1.  **Kira \> Kiralamalar \> Kiralama düzeltmeleri**'ne gidin.
2.  İptal edilecek devam eden kira düzeltmesini seçin.
3.  **Düzeltmeyi iptal et**'i seçin. 
4.  **Tamam**'ı seçin.

    > [!NOTE] 
    > **Kira düzeltme** sihirbazında **İptal Et**'i seçerseniz, sihirbazda tamamladığınız en son değişiklik geri alınır ancak devam eden bir düzeltme kaldırılmaz.

## <a name="use-the-lease-adjustment-workflow"></a>Kira düzeltmesi iş akışını kullanma

Bu bölümde, kira düzeltme iş akışının nasıl kullanılacağı açıklanmaktadır. Kira düzeltmesi iş akışı, bir dizi onay adımı sağlayarak ve bunları bir kira düzeltmesini nihai hale gelmeden önce onaylayan belirli kullanıcılara atayarak kira düzeltmelerini tutarlı bir şekilde yönetmenize yardımcı olur. Kira düzeltmesi iş akışında onaylandıktan sonra, kira düzeltmesini tamamlamak için **Kira düzeltme** sihirbazını kullanabilirsiniz.

1.  Kira düzeltmesini onaya göndermek için **Kira \> Kiralamalar \> Kira düzelmeleri**'ne gidin.
2.  Kira düzeltmesinin kira kimliğini seçin ve ardından **Düzeltme sihirbazı**'nı seçin.
3.  Sihirbazın son sayfasında, **Onaya gönder**'i seçin.
4.  Düzeltme hakkında bir açıklama girin ve **Tamam**'ı seçin.

    İş akışı durumu **Onay bekliyor** olarak değiştirilir ve sihirbazdaki tüm alanlar düzenlemeye karşı kilitlidir.

5.  Kira düzeltmesini onaylamak için **Kira \> Kiralamalar \> Kira düzelmeleri**'ne gidin.
6.  Kira düzeltmesinin kira kimliğini seçin ve **Düzeltmeye genel bakış** ve **Düzeltme girişi önizlemesi** hızlı sekmelerini gözden geçirin.
7.  **İş Akışı \> Onaylandı**'yı seçin.

    **Kira düzeltmeleri** sayfasında, iş akışı durumu artık **Onaylandı** olarak ayarlanır. Bu noktada, kira düzeltmesi, düzeltme günlüğü girişi aracılığıyla deftere nakledilmeye hazırdır.

8.  Kira düzeltmesini işlemeye devam etmek ve düzeltme girişini deftere nakletmek için **Kira \> Kiralamalar \> Kira düzeltmeleri**'ne gidin.
9.  Kira düzeltmesinin kira kimliğini seçin ve ardından **Düzeltme sihirbazı**'nı seçin.
10. Sihirbazın son sayfasına ulaşana kadar **İleri**'yi seçin ve sonra **Bitir**'i seçin.

Sistem, onaylanan düzeltme değişkenlerinin güncel olduğundan emin olmak için kiralamanın taşıma değerlerini yeniden hesaplar. Herhangi bir değişiklik varsa, onay durumu tekrar **Taslak** olarak ayarlanır ve kira düzeltmesini iş akışı sistemine yeniden göndermeniz gerekir.

## <a name="view-lease-versions"></a>Kiralama sürümlerini görüntüleme

Kiralama düzeltilmişse kiralamanın farklı sürümlerini görebilirsiniz. Ayrıca geçmiş planları ve geçmiş kiralama ayrıntılarını da görebilirsiniz.

1. **Kiralama özeti** sayfasında, kiralamayı seçin ve sonra Eylem Bölmesinde **Kiralama sürüm geçmişi**'ni seçin.

    Seçilen kiralama düzeltilmişse **Kiralama sürüm geçmişi** sayfası kiralamanın farklı sürümlerini gösterir. Özgün kiralama **1** ile, sonraki sürümler ile artan numara sırasıyla etiketlenir.

    Seçili bir kira sürümünün mali boyutlarını, sözleşme ayrıntılarını, konumunu ve ödeme planı satırlarını görüntüleyebilirsiniz.

2. Geçmiş planlamaları görüntülemek için **Kiralama özeti** sayfasından değiştirilen kiralamayı açın, istediğiniz defteri seçin ve ardından Eylem Bölmesinde **Defter sürüm geçmişi**'ni seçin.
3. **Defter sürümü** sayfasında, görüntülenecek bir sürüm ve zamanlama seçin.

## <a name="adjust-a-lease-book"></a>Kiralama defteri düzeltme

Yalnızca kiralama defteri düzeltmek için aşağıdaki adımları izleyin.

1. **Varlık kiralama** \> **Kiralamalar** \> **Kiralama özeti**'ne gidin.
2. Bir kiralama seçin ve açın.
3. **Kiralama ayrıntıları** sayfasında **Defterler**'i seçin.
4. Eylem bölmesindeki **Defter ayrıntıları** sayfasında, **Bakım** grubunda, **Defteri düzelt**'i seçin. 
5. Ödeme zamanlaması satırlarını kaldırın.
6. **Kira değiştirme tarihi** alanına değiştirilme tarihini girin. Daha sonra, varsa, tüm ek kıymet/sorumlulukların (ilk doğrudan maliyet, kira teşvik, kira ön ödemesi, Boşalma maliyeti ve net değer garantisi) kaldırılmasını göz önünde bulundurun. 
7. Kira ayarlamasının yanlış hesaplamalarını önlemeye yardımcı olmak için, değiştirme tarihiyle eşleşen yeni ödeme tarihleri için yeni ödeme planı satırları ekleyin. 

> [!NOTE] 
> Kirayı ayarlamak için **Kira ayarlama** sihirbazını kullanmanızı öneririz. Sihirbaz el ile gerçekleştirilen adımların sayısını azaltır, ayarlamadan sonra bakiyelerin önizlemesini sağlar ve deftere nakletmeden önce tutarları değiştirmenizi sağlar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

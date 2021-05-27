---
title: Kalite yönetimi test grupları
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle birden çok testin kullanılabilmesi için, test gruplarının nasıl oluşturulacağını açıklar.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 020a610e6a7e4d4b35ceb176d542bae32503a615
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021768"
---
# <a name="quality-management-test-groups"></a>Kalite yönetimi test grupları

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle birden çok testin kullanılabilmesi için, test gruplarının nasıl oluşturulacağını açıklar.

Test grubuna atanmış bireysel testleri ayarlamak, düzenlemek ve görüntülemek için **Test grupları** sayfasını kullanın. Sayfanın üst bölümü, test gruplarını gösterir ve alt bölümü seçili bir test grubuna atanan testleri görüntüler.

Test grubuna; örnekleme planı, kabul edilebilir kalite düzeyi ve bozucu test gereksinimi dahil olmak üzere birçok ilke atarsınız. Ardından, tek bir testi bir test grubuna atadığınızda, sıra, belgeler ve geçerlilik tarihleri gibi ek bilgiler tanımlarsınız. Nicel bir test için tanımladığınız bilgilere kabul edilebilir ölçüm değerleri de dahildir. Nitel bir test için bu bilgilere test değişkeni ve varsayılan sonuç dahildir.

Bir kalite emrine atanan test grubu, belirtilen öğe üzerinde gerçekleştirilmesi gereken testlerin varsayılan kümesini tanımlar. Bununla birlikte, kalite emri testlerini değiştirebilirsiniz, ekleyebilir veya silebilirsiniz. Test sonuçları, kalite emrindeki her test için rapor edilir.

Bir test grubu tanımladığınızda, isteğe bağlı olarak bir madde örnekleme belirtebilirsiniz. Madde örneklemeleri, test edilecek ürünün tutarını tanımlamak için kullanılır. Daha fazla bilgi için bkz. [Kalite yönetimi madde örnekleme](quality-item-sampling.md). Test grubundaki testlerin yıkıcı olduğunu da belirtebilirsiniz. Bir yıkıcı testte, madde örneği yok edilir ve miktar, eldeki stoktan kaldırılır.

## <a name="example-of-a-test-group"></a>Test grubu örneği

Bir üretim şirketi, kalite yönergelerindeki her sapma için bir test grubu tanımlıyor. Çeşitli test grupları, örnekleme planları arasındaki farklılıkları, birlikte gerçekleştirilmesi gereken testler kümesini, kabul edilebilir kalite düzeyini ve diğer etkenleri yansıtır. Nicel testleri için, kabul edilebilir ölçüm değerleri için de farklılıklar vardır. Kalite talimatlarını uygulamak için şirket, **Kalite ilişkilendirmeleri** sayfasında otomatik olarak kalite emirleri oluşturmak amacıyla kullanılan her kurala bir test grubu atar. Ayrıca el ile oluşturulan kalite emirlerine bir test grubu atar.

## <a name="create-a-test-group"></a>Test grubu oluşturma

Test grubu oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Test grupları** öğesine gidin.
1. Eylem Bölmesi'nde, sayfanın üst bölümünde ızgaraya satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Test grubu** – Test grubu için benzersiz bir kod ya da ad girin.
    - **Açıklama** – Test grubunun detaylı bir açıklamasını girin.
    - **Kabul edilebilir kalite düzeyi** – Test grubunun başarılı sayılması için toplam test sonuçlarından yüzde kaçının geçer not alması gerektiğini girin.
    - **Madde örnekleme** – Bir madde örnekleme seçin. Daha fazla bilgi için bkz. [Kalite yönetimi madde örnekleme](quality-item-sampling.md).
    - **Yıkıcı** – Test grubunun test edilen maddeleri yok ettiğini belirtmek için bu onay kutusunu işaretleyin.

1. Yeni satır seçiliyken, sayfanın üst kısmındaki **Genel** sekmesini seçin. **Özet** sekmesinde seçili test grubu için bazı ayarlar burada tekrarlanır. Ayrıca, grup için aşağıdaki alanları da ayarlayabilirsiniz:

    - **Stok toplu iş özniteliğini güncelleştir** – Bu seçeneği burada *Evet* olarak ayarladığınızda sayfanın alt kısmındaki test grubuna eklenen her yeni test için otomatik olarak *Evet* olarak ayarlanır.
    - **Toplu iş değerlendirmesini güncelleştir** – Bu seçeneği *Evet* olarak ayarladığınızda, test edilmekte olan madde toplu olarak denetleniyorsa, toplu iş değerlendirmesi **Başarısız kalite emri toplu iş değerlendirmesi** veya **Başarılı kalite emri toplu iş değerlendirmesi** alanında seçilen değerle otomatik olarak güncelleştirilir.
    - **Başarısız kalite emri toplu iş değerlendirmesi** – Bu test grubunu içeren bir kalite emri, AQL gereksinimlerini karşılamadığında atanması gereken toplu iş değerlendirme kodunu seçin.
    - **Başarılı kalite emri toplu iş değerlendirmesi** – Bu test grubunu içeren bir kalite emri, AQL gereksinimlerini karşıladığında atanması gereken toplu iş değerlendirme kodunu seçin.
    - **Stok durumunu güncelleştir** – Bu seçeneği *Evet* olarak ayarladığınızda, test edilmekte olan maddeyle ilgili depolama boyutu grubunda **Stok durumu** etkinleştirilirse, durum otomatik olarak, **Başarısız kalite emri durumu** veya **Başarılı kalite emri durumu** alanında seçilen durumla güncelleştirilir.
    - **Başarısız kalite emri durumu** – Bu test grubunu içeren bir kalite emri, AQL gereksinimlerini karşılamadığında maddeye atanması gereken stok durumunu seçin.
    - **Başarılı kalite emri durumu** – Bu test grubunu içeren bir kalite emri, AQL gereksinimlerini karşıladığında maddeye atanması gereken stok durumunu seçin.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Bir test grubuna bir niteleyici test ekleme

Bir test grubuna bir niteleyici test eklemek için, aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Test grupları** öğesine gidin.
1. Sayfanın üst kısmındaki **Genel bakış** sekmesinde, test eklemek istediğiniz test grubunu seçin.
1. Izgaraya satır eklemek için, sayfanın alt kısmındaki **Genel bakış** sekmesinde araç çubuğundan **Ekle**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Sıra numarası** – Testlerin gerçekleştirileceği sırayı belirtmek için bir tamsayı girin. Daha küçük sıra numaralarına sahip testler, daha büyük sıra numarası olan testlerden önce çalıştırılır.

        > [!NOTE]
        > Sıra numaraları arasında bir boşluk bırakmanız önerilir. Örneğin, ilk testiniz için **Sıra numarası** alanını *10* olarak ayarlayın ve sonra her ek test için değeri 10 artırın. Bu şekilde, daha sonra satırları silmek ve istediğiniz sırada yerleştirmek için yeniden oluşturmak zorunda kalmadan yeni testler ekleyebilirsiniz.

    - **Test** – Gerçekleştirmek istediğiniz testi seçin. Niteleyici sınaması için, **Tür** alanının *Seçenek* olarak ayarlandığı bir test seçin.
    - **Geçerli** – Testin geçerli olduğu ilk tarihi seçin. Bu alanı boş bırakırsanız bir sınır olmaz.
    - **Bitiş tarihi** – Testin geçerli olduğu son tarihi seçin. Bu alanı boş bırakır veya *Asla* olarak ayarlarsanız sınır olmaz.
    - **Test değeri belirleme** – Aynı test için birden çok sonuç kaydedildiği zaman AQL'nin nasıl belirlenmesi gerektiğini seçin. Niteleyici test için yalnızca *Manuel* seçilebilir. Diğer değerlerden birini (*Ortalama*, *Minimum* veya *Maksimum*) seçerseniz, test grubunu kaydettiğinizde hata iletisi alırsınız.
    - **Öznitelik** – Test sonuçlarını bir toplu iş özniteliğiyle kaydetmek istiyorsanız, burada özniteliği seçin ve **Stok toplu iş özniteliğini güncelleştir** onay kutusunu seçin.
    - **Stok toplu iş özniteliğini güncelleştirme** – **Öznitelik** alanında seçili toplu iş özellikler için test sonuçlarını kaydetmek için bu onay kutusunu işaretleyin.

1. Sayfanın alt bölümünde, **Genel** sekmesini seçin. **Genel bakış** sekmesinde seçili test için bazı ayarlar burada tekrarlanır. Ayrıca, test için aşağıdaki alanları da ayarlayabilirsiniz:

    - **Analiz raporu sertifikası** – Test sonuçlarının, analiz sertifikası (CoA) üzerine yazdırılması gerektiğini belirtmek için bu seçeneği *Evet* olarak ayarlayın. Bu rapor kalite emrinden oluşturulabilir.
    - **Hata durumunda eylem** – Bunun için AQL karşılanmazsa testin başarılı ya da başarısız olup olmadığını belirtmek için *Kabul et* veya *Başarısız* seçeneklerinden birini seçin.
    - **Kabul edilebilir kalite düzeyi** – Testin başarılı sayılması için toplam test sonuçlarından yüzde kaçının geçer not alması gerektiğini girin.

1. Sayfanın alt bölümünde, **Test** sekmesinde, aşağıdaki alanları ayarlayın:

    - **Değişken** – Niteliksel test sonuçlarını kaydetmek için test değişkenini seçin.
    - **Varsayılan sonuç** – Test sonuçları için kaydedilmesi gereken varsayılan sonucu seçin.
    - **Test aracı** – Test için kullanılacak cihazı seçin. Bir test aracı tanımlanmışsa, araç otomatik olarak test grubunda test için girilir.

1. Sayfayı kapatın.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Bir test grubuna bir niteleyici test ekleme

Bir test grubuna bir niceleyici test eklemek için, aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Kalite kontrol \> Test grupları** öğesine gidin.
1. Sayfanın üst kısmındaki **Genel bakış** sekmesinde, test eklemek istediğiniz test grubunu seçin.
1. Izgaraya satır eklemek için, sayfanın alt kısmındaki **Genel bakış** sekmesinde araç çubuğundan **Ekle**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Sıra numarası** – Testlerin gerçekleştirileceği sırayı belirtmek için bir tamsayı girin. Daha küçük sıra numaralarına sahip testler, daha büyük sıra numarası olan testlerden önce çalıştırılır.

        > [!NOTE]
        > Sıra numaraları arasında bir boşluk bırakmanız önerilir. Örneğin, ilk testiniz için **Sıra numarası** alanını *10* olarak ayarlayın ve sonra her ek test için değeri 10 artırın. Bu şekilde, daha sonra satırları silmek ve istediğiniz sırada yerleştirmek için yeniden oluşturmak zorunda kalmadan yeni testler ekleyebilirsiniz.

    - **Test** – Gerçekleştirmek istediğiniz testi seçin. Niceleyici test için, **Tür** alanının *Kesir* veya *Tamsayı* olarak ayarlandığı bir test seçin.
    - **Geçerli** – Testin geçerli olduğu ilk tarihi seçin. Bu alanı boş bırakırsanız bir sınır olmaz.
    - **Bitiş tarihi** – Testin geçerli olduğu son tarihi seçin. Bu alanı boş bırakır veya *Asla* olarak ayarlarsanız sınır olmaz.
    - **Test değeri belirleme** – Aynı test için birden çok sonuç kaydedildiği zaman AQL'nin nasıl belirlenmesi gerektiğini seçin. Mevcut seçenekler: *Ortalama*, *Minimum*, *Maksimum* ve *El ile*.
    - **Öznitelik** – Test sonuçlarını bir toplu iş özniteliğiyle kaydetmek istiyorsanız, burada özniteliği seçin ve **Stok toplu iş özniteliğini güncelleştir** onay kutusunu seçin.
    - **Stok toplu iş özniteliğini güncelleştirme** – **Öznitelik** alanında seçili toplu iş özellikler için test sonuçlarını kaydetmek için bu onay kutusunu işaretleyin.

1. Sayfanın alt bölümünde, **Genel** sekmesini seçin. **Genel bakış** sekmesinde seçili test için bazı ayarlar burada tekrarlanır. Ayrıca, test için aşağıdaki alanları da ayarlayabilirsiniz:

    - **Analiz raporu sertifikası** – Test sonuçlarının, (CoA) üzerine yazdırılması gerektiğini belirtmek için bu seçeneği *Evet* olarak ayarlayın. Bu rapor kalite emrinden oluşturulabilir.
    - **Hata durumunda eylem** – Bunun için AQL karşılanmazsa testin başarılı ya da başarısız olup olmadığını belirtmek için *Kabul et* veya *Başarısız* seçeneklerinden birini seçin.
    - **Kabul edilebilir kalite düzeyi** – Testin başarılı sayılması için toplam test sonuçlarından yüzde kaçının geçer not alması gerektiğini girin.

1. Sayfanın alt bölümünde, **Test** sekmesinde, aşağıdaki alanları ayarlayın:

    - **Standart** – Test sonuçları için beklenen tutarı (tamsayı veya kesir) girin. Girdiğiniz değer, test sonuçlarına varsayılan olarak girilir. Ayrıca, **Min** ve **Maks** alanlarına otomatik olarak varsayılan değer olarak girilir.
    - **Min** – Test sonuçları için izin verilen minimum değeri girin. Girdiğiniz değer, **Standart** alanda ayarlanan tutardan az olmalıdır. **Min** alanını güncelleştirdiğinizde, **Minimum tolerans (%)** alanı otomatik olarak güncelleştirilir. Benzer şekilde, **Minimum tolerans (%)** alanını güncelleştirdiğinizde, **Min** alanı otomatik olarak güncelleştirilir.
    - **Maks** – Test sonuçları için izin verilen maksimum değeri girin. Girdiğiniz değer, **Standart** alanda ayarlanan tutardan fazla olmalıdır. **Maks** alanını güncelleştirdiğinizde, **Maksimum tolerans (%)** alanı otomatik olarak güncelleştirilir. Benzer şekilde, **Maksimum tolerans (%)** alanını güncelleştirdiğinizde, **Maks** alanı otomatik olarak güncelleştirilir.
    - **Test aracı** – Test için kullanılacak cihazı seçin. Bir test aracı tanımlanmışsa, araç otomatik olarak test grubunda test için girilir.

1. Sayfayı kapatın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimi test gereçleri](quality-management-processes.md)
- [Kalite yönetimi testleri](quality-management-processes.md)
- [Kalite yönetimi test değişkenleri](quality-management-processes.md)
- [Kalite ilişkileri](quality-management-processes.md)
- [Toplu iş öznitelikleri](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

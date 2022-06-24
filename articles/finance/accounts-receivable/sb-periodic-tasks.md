---
title: Yinelenen sözleşme faturalamasındaki dönemsel görevler
description: Bu makale, Yinelenen sözleşme faturalamasında sunulan dönemsel görevleri açıklar.
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904802"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Yinelenen sözleşme faturalamasındaki dönemsel görevler

Bu makale, Yinelenen sözleşme faturalamasında sunulan dönemsel görevleri açıklar.

## <a name="generate-invoice"></a>Fatura oluştur

**Tüm fatura planları** ve **Fatura ayrıntısını görüntüle** sayfalarında ayarladığınız bilgilerden aylık yinelenen toplu faturaları oluşturmak için **Fatura oluştur** sayfasını kullanın. Bir fatura oluşturulduğunda satış siparişi işleme satırı için madde açıklaması, faturalanan plan satırının madde açıklaması ve fatura başlangıç ve bitiş tarihleriyle güncelleştirilir.

## <a name="generate-invoice-batch-processing"></a>Fatura toplu işlemleri oluştur

Yinelenen toplu işlem aracılığıyla yinelenen faturaları oluşturmak için **Fatura toplu işlemleri oluştur** sayfasını kullanın. Kullanılabilen parametreler **Fatura oluştur** sayfasındaki parametrelerle aynıdır, ancak bunlar birden fazla kez çalıştırılabilecek bir toplu işleme kaydedilebilir.

## <a name="price-update"></a>Fiyat güncelleştirme

Tek bir eylemde birden çok fatura planındaki birkaç maddenin fiyatlarını güncelleştirmek için Fiyat güncelleştirme yardımcı programını kullanın. Fiyatlar, belirtilen bir yüzdeye veya tutara göre güncelleştirilebilir. Satır listesinde yalnızca maddelerin geçerli birim fiyatları gösterilir. Fiyat güncelleştirmesinden sonraki fiyatlar gösterilmez.

Fiyat güncelleştirme yardımcı programı ile ilgili aşağıdaki noktalara dikkat edin:

- Belirli bir yıla ait satış siparişi zaten oluşturulmuşsa (yani, maddeler faturalanmamışsa), satır maddelerinin fiyatı etkilenmez.
- Fiyat güncelleştirme yardımcı programı, **Etkin** veya **Beklemede** durumundaki satır maddeleri için kullanılabilir. Beklemedeki maddeler için bekleme uygulandığı zaman **Planı düzelt** seçeneğinin **Hayır** olarak ayarlanmış olması gerekir.
- Fiyat güncelleştirme yardımcı programı görev aktarma, aşama bazında faturalama veya gelir bölme kullanılan kullanım maddelerine sahip satır maddeleri için kullanılamaz.

### <a name="price-update-example"></a>Fiyat güncelleştirme örneği

Bir fatura planı oluşturulur ve yenileme maddesi eklenir. Birim fiyatı 750 ABD dolarıdır. Maddenin ilk yılı 15 Aralık 2021'de ödenir. Fatura planı, 1 Ocak ile 31 Aralık 2022 arasındaki dönem için oluşturulur.

Yenileme sırasında, **Fatura oluştur** işlemi 2022 yılı için satış siparişi oluşturur. Fiyat güncelleştirme yardımcı programı çalıştırıldıktan sonra fiyat 750 ABD dolarından 800 ABD dolarına çıkarılır.

2022 için fatura planı zaten faturalandırıldığından 2022 için satış siparişi ve fatura planı etkilenmez ve birim fiyatı 750 ABD doları olarak kalır. 2023 için fatura planı henüz faturalandırılmadığından, 2023 için fatura planı satırı ve satır ayrıntısı 800 ABD doları olarak güncelleştirilir.

### <a name="update-prices--flat-pricing-method"></a>Fiyatları güncelleştirme - Sabit fiyatlandırma yöntemi

Sabit fiyatlandırma yöntemini kullanan maddelere ait fiyatları güncelleştirdiğinizde, fiyatı artırmak için bir yüzde veya tutar belirtebilirsiniz.

Sabit fiyatlandırma yöntemini kullanan maddele için Fiyat güncelleştirme yardımcı programını çalıştırmak üzere aşağıdaki adımları izleyin.

1. **Fiyat güncelleştirme** yardımcı programı sayfasında, **Sabit** fiyatlandırma yöntemini seçin.
2. **Artırma yöntemi** alanında, maddelerin fiyatını güncelleştirmek için kullanılan artırma yöntemini seçin.
3. Seçtiğiniz artırma yöntemine bağlı olarak, **Yüzde** alanında yüzdeyi veya **Tutar** alanında tutarı belirtin.
4. **Eklenecek kayıtlar** hızlı sekmesinde, veri filtreleri eklemek için **Filtrele** düğmesini kullanın.
5. Kayıt aralığını görüntülemek için **Önizlemeyi görüntüle**'yi seçin.
6. Bazı satırları işlemek istemiyorsanız bunları işaretleyin ve **Kaldır**'ı seçin.
7. **Tamam**'ı seçin.

### <a name="update-prices--standard-pricing-method"></a>Fiyatları güncelleştirme - Standart fiyatlandırma yöntemi

Bir maddenin fiyatı madde kaydında değiştirilirse, madde standart fiyatlandırma yöntemini kullanıyorsa fiyat tüm fatura planı satırları için güncelleştirilebilir.

1. **Fiyat güncelleştirme** yardımcı programı sayfasında, **Standart** fiyatlandırma yöntemini seçin.
2. **Eklenecek kayıtlar** hızlı sekmesinde, veri filtreleri eklemek için **Filtrele** düğmesini kullanın.
3. Kayıt aralığını görüntülemek için **Önizlemeyi görüntüle**'yi seçin.
4. Bazı satırları işlemek istemiyorsanız bunları işaretleyin ve **Kaldır**'ı seçin.
5. **Tamam**'ı seçin.

## <a name="mass-hold-processing"></a>Toplu bekletme işlemleri

Bekletme seçeneklerini aynı anda birden fazla fatura planına uygulamak için **Toplu bekletme** sayfasını kullanın.

Yalnızca bir fatura planını veya bir fatura planı satırını beklemede durumuna almak için **Tüm fatura planları** sayfasını açın ve **Bekletme uygula**'yı seçin. Bekletme durumunu kaldırmak için **Bekletmeyi kaldır** sayfasını kullanın.

### <a name="put-billing-schedules-on-hold"></a>Fatura planlarını beklemede durumuna alma

Birden fazla fatura planını bekletmek için aşağıdaki adımları izleyin.

1. **Toplu bekletme** sayfasında, **İşlem seçeneği** alanını **Bekletme uygula** olarak ayarlayın.
2. **Neden kodu** alanında neden kodu seçin.
3. **Planı düzelt** seçeneğini ayarlayın:

    - **Evet**: Seçeneği **Evet** olarak ayarlarsanız, **Bekletme tarihi** alanında bir bekletme tarihi belirtin. Bekletme tarihinden sonraki tüm fatura planı satırları kaldırılır.
    - **Hayır**: Fatura planı satırları değiştirilmez. Yalnızca durum değiştirilir. Durum **Beklede** olarak güncelleştirilir.

4. **Eklenecek kayıtlar** hızlı sekmesinde, veri filtreleri eklemek için **Filtrele** düğmesini kullanın.
5. Kayıt aralığını görüntülemek için **Önizlemeyi görüntüle**'yi seçin.
6. Bazı satırları işlemek istemiyorsanız bunları işaretleyin ve **Kaldır**'ı seçin.
7. **Tamam**'ı seçin.

Fatura planları listesine geri döndüğünüzde, fatura planlarının durumunun **Beklemede** olarak değiştiğini görmeniz gerekir.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Birkaç fatura planından bekletmeyi kaldırma

1. **Toplu bekletme** sayfasında, **İşlem seçeneği** alanını **Bekletmeyi kaldır** olarak ayarlayın.
2. **Neden kodu** alanına neden kodunu girin.
3. **Kaldırma tarihi** alanında, bekletmenin kaldırılması tarihi seçin.
4. **Sürdürme tarihi** ve **Erteleme tarihi** alanlarını gerektiği gibi ayarlayın. Erteleme tarihi ertelenebilecek tüm satırlara eklenir.
5. **Eklenecek kayıtlar** hızlı sekmesinde, veri filtreleri eklemek için **Filtrele** düğmesini kullanın.
6. Kayıt aralığını görüntülemek için **Önizlemeyi görüntüle**'yi seçin.
7. Bazı satırları işlemek istemiyorsanız bunları işaretleyin ve **Kaldır**'ı seçin.
8. **Tamam**'ı seçin.

> [!NOTE]
> Bekletmeyi kaldırmak için, **Yinelenen sözleşme faturalama parametreleri** sayfasındaki **Bekletmeyi kaldır kullanıcı grubunu geçersiz kıl** değerini ayarlayın.

Örneğin, faturalama satırının başlangıç tarihinin 1 Şubat 2022 ve bitiş tarihinin 28 Şubat 2022 olduğunu düşünelim. Faturlama tutarı 200 ABD dolarıdır. **Bekletme tarihi** alanı 10 Şubat 2022 olarak ayarlanmıştır. Bu nedenle, Şubat dönemi 10 Şubat tarihinden sonraki tarihleri dışarıda bırakacak şekilde düzeltilir. Yeni dönem 1 Şubat ile 9 Şubat arasındadır, tutar ise 64,29 ABD dolarıdır (günlük eşit bölüştürme aracılığıyla). 10 Şubat tarihindeki veya sonrasındaki tüm fatura planı satırları kaldırılır.

**Bekletmeyi kaldırma** işlemi tamamlanmışsa ve **Kaldırma tarihi** alanı 10 Şubat 2022 olarak ayarlanmışsa, iki faturalama dönemi olacaktır. İlk faturalama dönemi 1 Şubat ile 9 Şubat arasındadır, tutar ise 64,29 ABD dolarıdır. İkinci faturalama dönemi 10 Şubat ile 28 Şubat arasındadır, tutar ise 135,71 ABD dolarıdır.

## <a name="mass-termination-processing"></a>Toplu sonlandırma işlemleri

Sonlandırma tarihi belirtilerek gösterilen fatura planı satırlarını sonlandırmak için **Toplu sonlandırma** sayfasını kullanın.

Gelir ve gider erteleme kullanıyorsanız, **Tüm fatura planları** sayfasında **Sonlandırma tarihi** alanının **Planı düzelt** olarak ayarlandığı fatura planları geri ödeme için uygundur.

Çoklu öğe tahsisatı (MEA) işlevini kullanan fatura planları **Toplu sonlandırma** sayfasında görünmez. Yine de fatura planında sonlandırma işlevini kullanarak fatura planlarını ayrı ayrı sonlandırabilirsiniz.

> [!NOTE]
> **Fatura oluştur** toplu işine dahil olan fatura planı satırları bu işlemde kullanılamaz.

Her alan ve işlem hakkında daha fazla bilgi için bkz. [Faturalama planlarını sonlandırma](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Toplu arşiv işlemi

Birden fazla fatura planını arşivlemek için **Toplu arşiv** sayfasını kullanın. Yalnızca sonlandırılan fatura planları arşivlenebilir.

Bir fatura planı arşivlendikten sonra aşağıdaki olaylar gerçekleşir:

- Durumu **Arşivlendi** olarak değiştirilir.
- Fatura planları kalıcı olarak kilitlenir.
- Fatura planı satırları artık sorgu sayfalarında yer almaz.

> [!NOTE]
> Bir fatura planının arşivlenmesi kalıcı bir eylemdir ve geri alınamaz.

Fatura planlarını arşivlemek için aşağıdaki adımları izleyin.

1. **Toplu arşiv** sayfasındaki **Faturalama bitiş tarihi** alanında bir faturalama bitiş tarihi belirtin. Sonlandırılan tüm fatura planlarını görmek için bu alanı boş bırakın.
2. Gösterilen kayıtları sınırlamak için **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele** düğmesini kullanın.
3. **Önizlemeyi görüntüle**'yi seçin.
4. Bazı kayıtları arşivlemek istemiyorsanız bunları işaretleyin ve **Kaldır**'ı seçin.
5. Sayfadaki kayıtları arşivlemek için **Tamam**'ı seçin.

## <a name="mass-stubbing-process"></a>Toplu koçan oluşturma işlemi

Tüm seçili fatura planı satırlarını faturalandı (koçan) veya faturalanmadı (ters koçan) olarak işaretlemek için **Toplu koçan oluşturma** sayfasını kullanın. Koçan oluşturma ve koçanı tersine çevirme işlemleri genellikle başka bir sistemde faturalanmış olup içeri aktarılan fatura planı satırları üzerinde gerçekleştirilir. Koçanı oluşturulan fatura planı satırları koçanı oluşturulmuş olarak görünür ve müşteri için fatura oluşturmaz.

### <a name="stub-records"></a>Kayıtların koçanını oluşturma

1. **Toplu koçan oluşturma** sayfasındaki **İşlem seçenekleri** alanında **Koçan**'ı seçin.
2. **Fatura kesme tarihi** alanında, işlemi uygulamak istediğiniz satırları belirtmek için bir kesme tarihi ayarlayın. Yalnızca faturalama başlangıç tarihi, belirtilen kesme tarihinde veya daha önce olan kayıtlar gösterilir.
3. Koçanını oluşturmak istediğiniz satırları görmek için **Önizlemeyi görüntüle**'yi seçin.
4. İşlemden bir satırı çıkarmak için satırı işaretleyip **Kaldır**'ı seçin.
5. Satırların koçanını oluşturmak için **İşle**'yi seçin.

### <a name="reverse-stub-records"></a>Kayıt koçanını tersine çevirme

1. **Toplu koçan oluşturma** sayfasındaki **İşlem seçenekleri** alanında **Koçanı tersine çevir**'i seçin.
2. **Fatura kesme tarihi** alanında, işlemi uygulamak istediğiniz satırları belirtmek için bir kesme tarihi ayarlayın. Yalnızca faturalama başlangıç tarihi, belirtilen kesme tarihinde veya daha önce olan kayıtlar gösterilir.
3. Koçanı tersine çevirmek istediğiniz satırları görmek için **Önizlemeyi görüntüle**'yi seçin.
4. İşlemden bir satırı çıkarmak için satırı işaretleyip **Kaldır**'ı seçin.
5. Satır koçanını tersine çevirmek için **İşle**'yi seçin.

## <a name="update-completion-date-process"></a>Tamamlanma tarihi işlemlerini güncelleştir

Birden çok fatura planı veya kullanıcı için belirli aşama maddelerinin tamamlanma tarihini güncelleştirmek üzere **Tamamlanma tarihini güncelleştir** sayfasını kullanın. **Tamamlanma yüzdesi** yöntemini kullanan aşama şablonlarındaki maddeler için tamamlanma yüzdesini de güncelleştirebilirsiniz.

1. **Tamamlanma tarihini güncelleştir** sayfasında, **Kilometre taşı işlemleri**'ne gidin ve **Tamamlanma yüzdesini güncelleştir**'i seçin.
2. **Yüzde tutarı** alanına, tamamlanan toplam yüzdeyi girin.
3. Aşama şablonuyla ilgili madde numarasını seçin.
4. Filtre ölçütü olarak belirli bir **Son kullanıcı hesabı**, **Fatura planı numarası** veya **Madde numaraları** seçmek için **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.
5. Değişikliği işlemek için **Tamam**'ı seçin. İşlem tamamlandığında, aşama tahsisatına yeni bir satır eklenir. Bu satır, aşama şablonu için tamamlanan yüzdeyi gösterir.

## <a name="unbilled-revenue-mass-processing"></a>Faturalanmamış gelir toplu işlemleri

Faturalanmamış gelir günlüğü girişi oluşturmak veya bir ya da daha fazla seçili fatura planı veya fatura ayrıntısı satırları için günlük girişi koçanı oluşturmak üzere **Faturalanmamış gelir toplu işlemleri** sayfasını kullanın.

- **Günlük girişi oluştur**: Birden fazla fatura planı satırı için faturalandırılmamış gelir günlüğü girişlerini oluşturun. Listede görünecek kayıt aralığını seçmek için **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele** düğmesini kullanın. Liste, yalnızca faturalandırılmamış gelir günlüğü girişleri oluşturulmamış olan fatura planı satırlarını gösterir. İlk günlük girişleri oluşturulur. Erteleme maddeleri için erteleme çizelgeleri de oluşturulur.
- **Koçan yevmiye defteri girişi**: Faturalandırılmamış günlük girişlerinin zaten oluşturulduğu fatura planı satırlarını işaretleyin. Bu seçenek, faturalandırılmamış günlük girişinin başka bir sistemden deftere nakledilmesi durumunda kullanılır. Faturandırılmamış gelir günlüğü koçan olarak işaretlenir ve genel muhasebe defterine hareket nakledilmez.
- **Koçan yevmiye defteri girişini tersine çevir**: İşlenmiş koçan yevmiye defteri girişlerini tersine çevirin. **Koçan yevmiye defteri girişinin** işlenmesi sırasında hata yapıldıysa bu seçenek, fatura planı satırından **Koçan oluşturuldu** onay kutusunun işaretini kaldırır.
- **Koçan faturalama ayrıntısı satırı**: Bu süreci, faturalandırılmamış gelir harici bir sistemde işlenirse ve bazı fatura ayrıntısı satırları zaten önceden faturalandırılmışsa bu işlemi kullanın. Bu işlem, faturalandırılmamış gelir hesaplarında doğru tutarın görünmesini sağlar.
- **Koçan faturalama ayrıntısı satırını tersine çevir**: Tüm **Koçan faturalama ayrıntısı satırı** eylemlerini tersine çevirin.

**Günlük adı** alanı, **Yevmiye defteri girişi oluştur**'u genel muhasebe defterine nakletmek için kullanılır.

> [!NOTE]
> Koçan işlemi, tutarları genel muhasebe defterine nakletmez. **Günlük adı** alanı tüm koçan ve koçanı tersine çevirme işlemleri için kullanılamaz.

### <a name="unbilled-revenue-stub-example"></a>Faturalandırılmamış gelirin koçanını oluşturma örneği

Ekim 2021-Eylül 2022 arasındaki bir yıl için bir fatura planı ayarlanır. Faturalandırılmamış gelir bir harici sistemde zaten işlendi. Fatura planının dokuz ayı zaten faturalandı. Her faturalama döneminin tutarı 250 ABD dolarıdır. Yılın başlangıcında, faturalandırılmamış gelirden deftere nakledilen toplam tutar 3.000 ABD dolarıdır. Dokuz ay sonra 2.250 ABD doları zaten faturalandırılmıştır, faturalandırılmamış gelirde 750 ABD doları kalır.

Fatura planını yalnızca üç aylık faturalandırılmamış gelirin kalacağı şekilde ayarlamak için, aşağıdaki adımları izleyin.

1. **Fatura ayrıntısını görüntüle** sayfasında, Ekim 2021-Eylül 2022 dönemi, S0001 numaralı madde ve aylık 250 ABD doları tutarı için bir fatura planı oluşturun.
2. Fatura planı için **Yevmiye defteri girişi oluştur** seçeneğini belirleyin. 3.000 ABD doları tutarı, faturalandırılmamış gelire nakledilir.
3. **Koçan faturalama ayrıntısı satırı**'nı seçin ve hareket tarihini Haziran 2022 (dokuz ay) olarak belirleyin. Fatura planı satırları önizlemede görünmez. Etkilenen satırlar hareket tarihine bağlıdır.
4. **Tamam**'ı seçin.

Faturalanan ilk dokuz ay için koçan oluşturulmuştur.

[![Fatura ayrıntısı satırları koçanını görüntüleme.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

3.000 ABD doları faturalandırılmamış gelirden tersine çevrildi ve faturalandırılmamış gelirde 750 ABD doları nakledildi. Faturalandırılmamış gelir nakillerini görmek için satır ayrıntıları sayfasının **Yenilemeler** sekmesindeki **Faturalanmamış gelir yevmiye defteri girişi denetimi**'ni seçin.

[![Faturalanmamış gelir yevmiye defteri girişi denetimi.](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Faturalanmamış gelir yevmiye defteri girişi, önceki dönemden tüm faturalandırma satırı ayrıntılarının faturalandırılmış olması koşuluyla istediğiniz yenileme dönemi için oluşturulabilir. Örneğin, bir fatura planı satırının 12 aylık bir dönem (Ocak-Aralık 2021) için aylık faturalama sıklığı vardır. Satırda üç dönem vardır: başlangıç dönemi, ikinci dönem (Ocak-Aralık 2022) ve üçüncü dönem (Ocak-Aralık 2023). 2021'deki ilk 12 aydan tüm fatura ayrıntısı satırları için fatura oluşturulduktan sonra ikinci dönemin faturalanmamış geliri için yevmiye defteri girişi oluşturulabilir.
>
> Faturalanmamış gelir özelliğini kullanan erteleme maddeleri için fatura satırı ve iskonto satırları işlenir. Bu maddeler için faturalanmamış yevmiye defteri girişi ve fatura satırı ve iskonto satırı için erteleme planı oluşturulur.
>
> Ertelenemeyen maddeler ve ertelenebilir maddeler için oluşturulan yevmiye defteri girişleri, farklı gelir hesaplarına alacak nakleder.

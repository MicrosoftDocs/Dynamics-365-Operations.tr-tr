---
title: CTP kullanarak satış siparişi teslimat tarihlerini hesaplama
description: Teslim edilebilir miktar (CTP) işlevi müşterilere belirli malları taahhüt edebileceğiniz gerçekçi tarihler vermenizi sağlar. Bu makalede, her planlama altyapısı (Planlama Optimizasyonu ve yerleşik altyapı) için CTP'nin nasıl ayarlanacağı ve kullanılacağı açıklanır.
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3b8e3dc9f0e7aaf019aa4d7284458206e7daadb2
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714873"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>CTP kullanarak satış siparişi teslimat tarihlerini hesaplama

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Teslim edilebilir miktar (CTP) işlevi müşterilere belirli malları taahhüt edebileceğiniz gerçekçi tarihler vermenizi sağlar. Her satış satırı için, mevcut eldeki stok, üretim kapasitesi ve taşıma sürelerini hesaba katan bir tarih sağlayabilirsiniz.

CTP, kapasite bilgilerini dikkate alarak, [karşılanabilir miktar](../../sales-marketing/delivery-dates-available-promise-calculations.md) (KM) işlevini uzatır. KM yalnızca malzeme kullanılabilirliğini dikkate alır ve sonsuz kapasite kaynakları olduğunu varsayarken, CTP hem malzeme hem de kapasitenin kullanılabilirliğini dikkate alır. Bu nedenle, talebin belirli bir zaman dilimi içinde karşılanıp karşılanmayacağına ilişkin daha gerçekçi bir tablo sağlar.

CTP, kullandığınız master planlama altyapısına (Planlama Optimizasyonu veya yerleşik altyapı) bağlı olarak az miktarda farklı davranır. Bu makalede, her altyapı bunun nasıl ayarlanacağı açıklanmaktadır. Planlama Optimizasyonu için CTP şu anda yerleşik altyapı tarafından desteklenen CTP senaryolarının yalnızca bir alt kümesini desteklemektedir.

## <a name="turn-on-ctp-for-planning-optimization"></a>Planlama Optimizasyonu için CTP'yi etkinleştirme

Yerleşik master planlama altyapısı için CTP her zaman kullanılabilir. Ancak, Planlama Optimizasyonu için CTP'yi kullanmak istiyorsanız, bu özellik sisteminizde açık olmalıdır. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanında bu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Master planlama*
- **Özellik adı:** *(Önizleme) Planlama Optimizasyonu için CTP*

## <a name="how-ctp-compares-to-atp"></a>CTP'nin KM ile karşılaştırması

CTP ve KM birbirine benzer, ancak CTP genellikle aşağıdaki örnekte gösterildiği gibi daha doğru sonuç verebilir.

Madde A; B ve C maddelerinden oluşturulan bir maddedir ve Madde A'nın eldeki miktarı 0'dır (sıfır). Yalnızca malzemeyi dikkate alan bir KM denetimi kullanırsanız, KM miktarı da 0 (sıfır) olacaktır. Ancak bir CTP denetimi yaparsanız sistem, B ve C maddelerinin kullanılabilirliğini denetler, Madde A'yı oluşturmak için gerekli olan kaynakları denetler ve A maddesinden ne kadar oluşturulabileceğini hesaplar. Ek olarak, CTP hesaplaması, B ve C maddelerinin daha fazla olmasını sağlamak ve bunları daha fazla A maddesi yapmak üzere kullanmak için gereken kaynakları ve malzemeleri denetleyebilir.

Malzeme ve kaynakları dikkate alan bir CTP hesaplaması, özellikle de denetlenen madde bir sipariş için derleme maddesi olduğunda, yalnızca malzemelerin denetlendiği bir hesaplamadan daha büyük bir miktar gösterebilir. Başka bir deyişle, CTP işlevi açılım işlevine dayanır ve beklenen teslimat tarihini hesaplamak üzere seçili satış siparişi satırı için çalıştırılabilir.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Kullandığınız master planlama altyapısına göre CTP nasıl farklılık gösterir?

Aşağıdaki tablo, Planlama Optimizasyonu için CTP ile yerleşik master planlama altyapısı için CTP arasındaki farkları özetler.

| Öğe | Planlama İyileştirmesi | Yerleşik master planlama altyapısı |
|---|---|---|
| Siparişler, sipariş satırları ve ürünler için **Teslimat tarihi kontrolü** ayarı | *Planlama İyileştirmesi için CTP* | *CTP* |
| Hesaplama zamanı | Hesaplama işlemi, dinamik bir planı zamanlanmış bir görev olarak çalıştırılarak tetiklenir. | Bir satış siparişi satırını her girdiğinizde veya güncelleştirdiğinizde hesaplama hemen tetiklenir. |
| **Planlama Optimizasyonu için CTP durumu** alan değeri | <p>Siparişlerin ve satırların oluşturulmasından veya son güncelleştirilmesinden bu yana dinamik planın çalıştırılmadığı siparişler ve sipariş satırları için *Hazır değil* değeri gösterilir.</p><p>*Hazır* değeri, CTP'nin dinamik plan çalıştırılarak onaylı teslim tarihlerini hesaplamak için kullanıldığı siparişler ve satırlar için görüntülenir.</p> | *Hazır* değeri her zaman gösterilir. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>Varsayılan teslimat tarihi kontrol yöntemlerini ayarlama

Sistem, her sipariş ve sipariş satırı için teslimat tarihi tahminlerini hesaplamak üzere çeşitli yöntemlerden birini kullanabilir. Genel varsayılan yöntem olarak en sık kullanmak istediğiniz teslimat tarihi kontrol yöntemini ayarlamalısınız. Her bir ürün için varsayılan geçersiz kılmalar da ayarlayabilirsiniz. Daha sonra, gereksinim duyduğunuz şekilde her sipariş ve/veya sipariş satırı için varsayılan yöntemleri geçersiz kılabilirsiniz.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>Genel varsayılan teslimat tarihi kontrolünü ayarlama

Varsayılan teslimat tarihi kontrol yöntemi, bir geçersiz kılmanın geçerli olmadığı tüm yeni sipariş satırlarına uygulanacaktır. Bir yöntem seçmek için şu adımları izleyin.

1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
1. **Sevkiyatlar** sekmesinin **Teslimat denetimi** hızlı sekmesindeki **Teslimat tarihi kontrolü** alanında, şirketiniz için varsayılan yöntem olarak kullanmak istediğiniz yöntemi seçin:

    - *Yok* – Teslimat tarihlerini hesaplamaz.
    - *Satış sağlama süresi* – Satış sağlama süresi, satış siparişinin oluşturulmasından maddelerin sevk edilmesi arasındaki zaman anlamına gelir. Teslim tarihi hesaplaması, bir varsayılan gün sayısına dayanır ve stok kullanılabilirliğini, bilinen talebi veya planlanan tedariki dikkate almaz.
    - *KM* – KM, mevcut bulunan ve müşteriye belirli bir tarihte taahhüt edilebilecek bir madde miktarıdır. KM hesaplaması kaydedilmemiş stok, sağlama süreleri, planlanan girişler ve sorunları içerir.
    - *KM + Çıkış marjı* – Sevkiyat tarihi, KM tarihi ile maddenin çıkış marjının toplamına eşittir. Çıkış marjı, maddelerin sevkiyata hazırlanması için gereken süredir.
    - *CTP* – Yerleşik master planlama altyapısı tarafından sağlanan CTP hesaplamasını kullanır. Planlama Optimizasyonunu kullanıyorsanız, *CTP* teslim tarihi kontrol yöntemine izin verilmez ve bu yöntem seçilirse, hesaplama çalıştırıldığında hataya neden olur.
    - *Planlama Optimizasyonu için CTP* – Planlama Optimizasyonu tarafından sağlanan CTP hesaplamasını kullanır. Yerleşik master planlama altyapısını kullanıyorsanız, bu seçeneğin hiçbir etkisi olmaz.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Belirli ürünler için teslim tarihi denetimi geçersiz kılmalarını ayarlama

Genel varsayılan yönteminiz olarak ayarlanmış olandan farklı bir teslimat tarihi kontrol yöntemi kullanmak istediğiniz belirli ürünler için geçersiz kılmalar atayabilirsiniz.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Ayarlamak istediğiniz ürünü seçin.
1. Eylem Bölmesinde **Stoğu yönet** sekmesinde, **Sipariş ayarları** grubunda, **Varsayılan sipariş ayarları**'nı seçin.
1. **Varsayılan sipariş ayarları** sayfasındaki **Satış siparişi** hızlı sekmesinde, **Teslimat denetimini geçersiz kıl** seçeneğini *Evet* olarak ayarlayın.
1. **Teslimat tarihi kontrolü** alanında, seçili ürün için kullanılacak yöntemi seçin. [Genel varsayılan teslimat tarihi denetimini ayarlama](#global-default) bölümünde açıklanan seçenekler de kullanılabilir.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>Planlama Optimizasyonu hesaplamaları için CTP'yi zamanlama

Planlama Optimizasyonu için CTPyi kullandığınızda, sistemi CTP hesaplamaları yapacak şekilde tetiklemek için dinamik bir plan çalıştırmanız ve ilgili tüm siparişler için teyit edilen sevk ve giriş tarihlerini ayarlamanız gerekir. Plan, onaylanan sevk ve giriş tarihlerinin gerekli olduğu tüm maddeleri içermelidir. (Yerleşik planlama altyapısı için CTP kullandığınızda, CTP hesaplamaları hemen yerel olarak yapılır. Bu nedenle, CTP sonuçlarını görmek için dinamik bir plan çalıştırmanız gerekmez.)

Tarihlerin tüm kullanıcılar için uygun zamanda kullanılabilir olmasını sağlamak için toplu işleri, ilgili planları yinelenen bir temelde çalışacak şekilde ayarlamanız önerilir. Örneğin, dinamik plan çalıştırmak üzere ayarlanmış bir toplu iş, her 30 dakikada bir teyit edilen sevk ve giriş tarihlerini ayarlar. Bu nedenle, siparişleri giren ve içe aktaran kullanıcılar teyit edilen sevk ve giriş tarihlerini almak için maksimum 30 dakika beklemek zorunda kalacak.

Belirli bir zamanlamada dinamik bir plan çalıştırmak üzere toplu iş ayarlamak için aşağıdaki adımları izleyin.

1. **Master planlama \> Master planlama \> Çalıştır \> Master planlama** öğesine gidin.
1. **Master planlama** iletişim kutusunda **Parametreler** hızlı sekmesinde, **Master plan** alanını, çalıştırmak istediğiniz dinamik plana ayarlayın.
1. **Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** öğesini *Evet* olarak ayarlayın.
1. **Yineleme**'yi seçin ve zamanlamayı gerektiği gibi ayarlayın.
1. Zamanlamayı kaydetmek için **Tamam**'ı seçin.
1. Toplu iş oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.

## <a name="use-ctp-for-built-in-master-planning"></a>Yerleşik master planlama için CTP'yi kullanma

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Yerleşik master planlama için CTP'yi kullanarak yeni bir sipariş oluşturma

Her yeni satış siparişi veya sipariş satırı eklediğinizde, sistem buna varsayılan bir teslim tarihi kontrol yöntemi atar. Sipariş başlığı her zaman genel varsayılan yöntemle başlar. Sipariş edilen bir maddeye geçersiz kılma atanmışsa, yeni sipariş satırı bu geçersiz kılma işlemini kullanır. Aksi takdirde, yeni sipariş satırı genel varsayılan yöntemi de kullanır. Dolayısıyla, varsayılan yöntemlerinizi en sık kullandığınız teslimat tarihi kontrol yöntemiyle eşleşecek şekilde ayarlamalısınız. Sipariş oluşturduktan sonra, varsayılan yöntemi sipariş başlığı ve/veya sipariş satırı düzeyinde gereksinim duyduğunuz şekilde geçersiz kılabilirsiniz. Daha fazla bilgi için bkz. [Varsayılan teslimat tarihi kontrol yöntemlerini ayarlama](#default-methods) ve [Varolan satış siparişlerini CTP'yi kullanacak şekilde değiştirme](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Yerleşik master planlama için CTP kullandığınızda onaylanan teslimat tarihlerini görüntüleme

Yerleşik master planlama altyapısını kullanıyorsanız, CTP hesaplamaları, **Teslimat tarihi denetimi** alanının *CTP* olarak ayarlandığı siparişlere ve/veya sipariş satırlarına uygulanır.

Yerleşik master planlama için CTP kullanan satış satırları için sistem, bir satış satırını her kaydettiğinizde **Onaylanan sevk tarihi** ve **Teyit edilen giriş tarihi** alanlarını otomatik olarak ayarlar. Daha sonra bir satış satırında ilgili bir değişiklik yaparsanız (örneğin, miktarı veya tesisi değiştirerek), tarihler hemen yeniden hesaplanır.

- Bir satış siparişi satırı için onaylanan teslim tarihlerini görüntülemek için satış siparişini açın ve satış satırını seçin. Ardından, **Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** ve **Teyit edilen giriş tarihi** değerlerini inceleyin.
- Bir siparişin tamamı için onaylanan teslim tarihlerini görüntülemek için satış siparişini açın ve **Başlık** görünümünü seçin. Ardından, **Teslimat** hızlı sekmesinde **Onaylanan sevkiyat tarihi** ve **Teyit edilen giriş tarihi** değerlerini inceleyin.

## <a name="use-ctp-for-planning-optimization"></a>Planlama İyileştirmesi için CTP'yi kullanma

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Planlama Optimizasyonu için CTP'yi kullanarak yeni bir sipariş oluşturma

Her yeni satış siparişi veya sipariş satırı eklediğinizde, sistem buna varsayılan bir teslim tarihi kontrol yöntemi atar. Sipariş başlığı her zaman genel varsayılan yöntemle başlar. Sipariş edilen bir maddeye geçersiz kılma atanmışsa, yeni sipariş satırı bu geçersiz kılma işlemini kullanır. Aksi takdirde, yeni sipariş satırı genel varsayılan yöntemi de kullanır. Dolayısıyla, varsayılan yöntemlerinizi en sık kullandığınız teslimat tarihi kontrol yöntemiyle eşleşecek şekilde ayarlamalısınız. Sipariş oluşturduktan sonra, varsayılan yöntemi sipariş başlığı ve/veya sipariş satırı düzeyinde gereksinim duyduğunuz şekilde geçersiz kılabilirsiniz. Daha fazla bilgi için bkz. [Varsayılan teslimat tarihi kontrol yöntemlerini ayarlama](#default-methods) ve [Varolan satış siparişlerini CTP'yi kullanacak şekilde değiştirme](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Planlama Optimizasyonu için CTP kullanırken onaylanan teslim tarihlerini görüntüleme

Planlama Optimizasyonu kullanıyorsanız CTP hesaplamaları, **Teslimat tarihi denetimi** alanının *Planlama Optimizasyonu için CTP* olarak ayarlandığı siparişlere ve/veya sipariş satırlarına uygulanır.

Planlama Optimizasyonu için CTP kullanan satış satırları için, **Onaylanan sevk tarihi** ve **Teyit edilen giriş tarihi** alanları, uygun dinamik plan çalıştırılıncaya kadar (genellikle periyodik bir toplu iş kullanılarak) boş kalır. Bunlar daha sonra otomatik olarak ayarlanır. Daha fazla bilgi için bkz. [Planlama Optimizasyonu hesaplamaları için CTP'yi zamanlama](#batch-job).

**Planlama Optimizasyonu için CTP durumu** alanı, teyit edilen tarihlerin Planlama Optimizasyonu için CTP kullanan her satır için hesaplanıp hesaplanmadığını belirtir. Bu alan, onaylanan teslimat tarihlerinin henüz hesaplanmadığı veya başka değişiklikler nedeniyle artık geçerli olmadığı satırlar ve siparişler için *Hazır değil* değerini gösterir. Hesaplanan satırlar ve siparişler için *Hazır* değeri gösterir. Her satır ve siparişin tamamı için durumu görüntüleyebilirsiniz.

- Bir satış siparişi satırının durumunu görüntülemek için satış siparişini açın ve satış satırını seçin. Ardından, **Teslimat ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde, **Planlama Optimizasyonu için CTP durumu** değerini inceleyin. Satırın **Onaylanan sevk tarihi** ve **Teyit edilen giriş tarihi** alanları, hesaplandıktan sonra bu sekmede de görüntülenir.
- Bir siparişin tamamı için durumu görüntülemek için satış siparişini açın ve **Başlık** görünümünü seçin. Ardından, **Teslimat** hızlı sekmesinde, **Planlama Optimizasyonu için CTP durumu** değerini inceleyin. Siparişin **Onaylanan sevk tarihi** ve **Teyit edilen giriş tarihi** alanları, hesaplandıktan sonra bu sekmede de görüntülenir.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Bir satış siparişi satırını, teyit edilen tarihler Planlama Optimizasyonu için CTP tarafından hesaplandıktan sonra güncelleştirirseniz, uygun dinamik plan çalıştırılıncaya kadar sistem bu tarihleri temizler.
> - Varolan teyit edilen tarihleri etkileyebilen ilgili bir ayarı düzenlerseniz (örneğin, sağlama sürelerini, rezervasyonları veya işaretleri değiştirerek), ilgili varolan siparişlerin teyit edilen tarihlerini temizlemeniz gerekir. Bu eylem, ilgili her satırın durumunun *Hazır değil* olarak değiştirilmesine neden olur. Daha sonra bu değişiklik, sistemin dinamik planı bir sonraki çalıştırmasında teyit edilen tarihleri yeniden hesaplamasını sağlar.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>Varolan satış siparişlerini CTP kullanacak şekilde değiştirme

Herhangi bir zamanda açık bir sipariş için **Teslimat tarihi kontrolü** değerini değiştirebilirsiniz. Başlık düzeyinde ve/veya her bir satır için gereken değeri istediğiniz gibi değiştirebilirsiniz.

### <a name="change-to-ctp-at-the-order-header-level"></a>Sipariş başlığı düzeyinde CTP'ye değiştirme

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Bir siparişi, sipariş başlığı düzeyinde CTP kullanacak şekilde değiştirmek için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Siparişler \> Tüm satış siparişleri**'ne gidin.
1. Ayarlamak istediğiniz satış siparişini açın veya yeni bir sipariş oluşturun.
1. **Satış siparişi ayrıntıları** sayfasında, başlık bilgilerini açmak için **Başlık**'ı seçin.
1. **Teslimat** hızlı sekmesinde, kullanmakta olduğunuz planlama altyapısına bağlı olarak **Teslimat tarihi kontrolü** alanını aşağıdaki değerlerden birine ayarlayın:

    - *CTP* – Yerleşik master planlama altyapısı tarafından sağlanan CTP hesaplamasını kullanır. Planlama Optimizasyonu kullanıyorsanız, *CTP* teslim tarihi kontrol yöntemine izin verilmez. Bu nedenle, bu değeri seçerseniz, hesaplama çalıştığı zaman bir hata oluşacaktır.
    - *Planlama Optimizasyonu için CTP* – Planlama Optimizasyonu tarafından sağlanan CTP hesaplamasını kullanır. Yerleşik master planlama altyapısını kullanıyorsanız, bu ayarın hiçbir etkisi olmaz.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Değişiklerinizi uygulamak için **Tamam**'ı seçin.

### <a name="change-to-ctp-at-the-order-line-level"></a>Sipariş satırı düzeyinde CTP'ye değiştirme

Farklı bir teslimat tarihi kontrol yöntemi kullanarak sipariş satırı oluşturduysanız, istediğiniz zaman CTP'yi kullanabilirsiniz. Satır düzeyinde yaptığınız değişiklikler başka satırları etkilemez. Ancak bu değişiklikler, güncelleştirilmiş her satır hesaplamasının nasıl değiştiğine bağlı olarak, genel sipariş teslimat tarihlerinin ileri veya geri hareket etmelerine neden olabilirler. <!-- KFM: Confirm this intro at next revision -->

Bir siparişi, yerleşik master planlama için satır düzeyinde CTP kullanacak şekilde değiştirmek için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Siparişler \> Tüm satış siparişleri**'ne gidin.
1. Ayarlamak istediğiniz satış siparişini açın veya yeni bir sipariş oluşturun.
1. **Satış siparişi ayrıntıları** sayfasındaki **Satış siparişi satırı** hızlı sekmesinde, ayarlamak istediğiniz satış siparişi satırını seçin.
1. **Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde, kullanmakta olduğunuz planlama altyapısına bağlı olarak **Teslimat tarihi kontrolü** alanını aşağıdaki değerlerden birine ayarlayın:

    - *CTP* – Yerleşik master planlama altyapısı tarafından sağlanan CTP hesaplamasını kullanır. Planlama Optimizasyonu kullanıyorsanız, *CTP* teslim tarihi kontrol yöntemine izin verilmez. Bu nedenle, bu değeri seçerseniz, hesaplama çalıştığı zaman bir hata oluşacaktır.
    - *Planlama Optimizasyonu için CTP* – Planlama Optimizasyonu tarafından sağlanan CTP hesaplamasını kullanır. Yerleşik master planlama altyapısını kullanıyorsanız, bu ayarın hiçbir etkisi olmaz.

    **Mevcut sevk ve giriş tarihleri** iletişim kutusu görüntülenir ve kullanılabilir sevk ve giriş tarihlerini gösterir. Bu iletişim kutusu, önceki bölümde açıklandığı gibi, sipariş başlığı için çalıştığı şekilde sipariş satırları için de aynı şekilde çalışır.

1. Eylem bölmesinde, **Kaydet**'i seçin.

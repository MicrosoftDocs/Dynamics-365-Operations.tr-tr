---
title: İndirimleri işleme, inceleme ve deftere nakletme
description: Bu konuda, indirim yönetimi anlaşmaları üzerinde işlem yapmak, iskontoları hesaplamak, oluşturulan işlemleri gözden geçirmek, işlemleri deftere nakletmek ve deftere nakilleri gözden geçirmek açıklanmıştır.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 803b4d8b287f2b0dc523654e3e1852209f4ea039
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573549"
---
# <a name="process-review-and-post-rebates"></a>İndirimleri işleme, inceleme ve deftere nakletme

[!include [banner](../includes/banner.md)]

Bu konuda, indirim yönetimi anlaşmaları üzerinde işlem yapmak, iskontoları hesaplamak, oluşturulan işlemleri gözden geçirmek, işlemleri deftere nakletmek ve deftere nakilleri gözden geçirmek açıklanmıştır.

## <a name="change-the-status-of-a-deal"></a>Bir anlaşma durumunu değiştirme

İzlemeye yardımcı olmak amacıyla, her bir anlaşmaya durum atayabilirsiniz. Durum yalnızca bilgi amaçlıdır.

1. Bir anlaşma seçin (örneğin, [**tüm indirim yönetimi anlaşmaları** sayfasında](rebate-management-deals.md)).
1. Eylem Bölmesi'nde, **İndirim yönetimi anlaşmaları** sekmesindeki **Koru** grubunda **Durumu değiştir**'i seçin.
1. **Durumu Değiştir** iletişim kutusunda, **indirim durumu** alanını yeni bir durum olarak ayarlayın.
1. **Tamam**'ı seçin.

## <a name="calculate-fifo-purchase-prices"></a>FIFO Satın alma fiyatlarını hesaplama

**Fiyat tabanı** alanının *FIFO* olarak ayarlandığı [anlaşmalar](rebate-management-deals.md) için indirimleri hesaplamak üzere, **FIFO satın alma fiyatını hesapla** periyodik görevinin çalıştırılması gerekir. Sistem, satılan stokun değerini hesaplamak için ilk gelen ilk çıkar (FIFO) kuralını kullanır. Bu değer daha sonra satıcı indirimlerinin hesaplanması için kullanılacaktır.

**İndirimler yönetimi \> Periyodik görevler \> FIFO satın alma fiyatını hesapla**'ya gidin. Görünen iletişim kutusunda, hesaplamayı çalıştırmak için **Tamam**'ı seçin.

## <a name="create-source-transactions"></a>Kaynak hareketleri oluşturma

Geçerli bir İndirim yönetimi anlaşması oluşturmadan önce veya sonra kaynak işlemleri olan satış siparişlerini veya satınalma siparişlerini oluşturabilirsiniz.

Her bir anlaşma satırını, bir satış siparişi veya satınalma siparişi için teslimatı ya da faturayı deftere naklederek otomatik olarak bir indirim provizyonu oluşturacak şekilde ayarlayabilirsiniz. Anlaşma satırı için **Hareket türü** alanını *Teslimat* veya *Fatura* olarak ayarlayın ve **Deftere naklederken işle** seçeneğini *Evet* olarak ayarlayın. **Hareket türü** alanı *Sipariş* olarak ayarlanmışsa deftere nakil sırasında işleme devre dışı bırakılır. Anlaşma etkinleştirildikten sonra oluşturulan kaynak hareketleri için bu konunun daha ilerideki [İndirim yönetimi anlaşmalarını işleme](#process-deals) bölümünde açıklandığı gibi provizyonu yine de işleyebilirsiniz.

### <a name="enable-price-details"></a>Fiyat ayrıntılarını etkinleştir

Kaynak hareketleri oluşturmadan önce alacaklar hesapları için **Fiyat ayrıntılarını etkinleştir** seçeneğini etkinleştirmelisiniz.

1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
1. **Fiyatlar** sekmesindeki **Fiyat ayrıntıları** hızlı sekmesinde, **Fiyat ayrıntılarını etkinleştir** seçeneğini *Evet* olarak ayarlayın.

### <a name="create-a-source-transaction"></a>Kaynak hareketi oluşturma

Kaynak hareketi oluşturmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. **Yeni**'yi seçin.

    İndirim talepleri gerçekleşen durumu taklit etmek için şimdi müşterinin indirime hak kazanacağı miktar ve ürünün bulunduğu bir satış emri oluşturmalısınız.

1. **Müşteri hesabı** alanında, indirim anlaşması için uygun olacak bir müşteri girin veya seçin.
1. Satış siparişi oluşturmak için **Tamam**'ı seçin.
1. **Satış siparişi satırları** hızlı sekmesinde bir satır ekleyin ve bunun için aşağıdaki alanları ayarlayın:

    - **Madde numarası**: İndirim için uygun olan bir madde belirtin.
    - **Miktar**: **Temel** alanının *Miktar* olduğu satırı içeren bir indirim anlaşması için uygun olan miktarı belirtin.
    - **Birim fiyat**: **Temel** alanının *Değer* olduğu bir satırı içeren bir indirim anlaşması için uygun olan fiyatı belirtin.
    - **Site**: Ürünün kullanılabilir olduğu ve indirim anlaşması için uygun olan bir site seçin.
    - **Ambar**: Ürünün kullanılabilir olduğu ve indirim anlaşması için uygun olan bir ambar seçin.

1. **Satış siparişi satırları** hızlı sekmesindeki araç çubuğunda **Satış siparişi satırı \> Fiyat ayrıntıları**'nı seçin. Bu komut, yalnızca önceki bölümde açıklandığı gibi fiyat ayrıntılarını etkinleştirirseniz kullanılabilir.
1. **Fiyat ayrıntıları** sayfasında, **İndirim yönetimi** hızlı sekmesini seçin. Bu hızlı sekme, mevcut sipariş satırı için geçerli olan tüm indirim yönetimi anlaşmalarını listeler ve siparişin tahmini indirim tutarını gösterir. Tutarların yalnızca gelecekteki indirim taleplerinin tahminleri olduğunu unutmayın. Gerçek indirim tutarları farklı olabilir. Gerçek tutarları etkileyebilen faktörlerin bazıları şunlardır:

    - Müşterinin dönemsel indirim anlaşması kapsamında elde ettiği toplam satış hacmi.
    - Müşterinin tüm miktarda ya da kısmi miktarda iade edip etmediği.
    - Geçerli satış siparişinin İndirim yönetimi anlaşması için tanımlanan işlem türünde (*Sipariş, Teslimat* veya *Fatura*) alınıp alınmadığı.
    - Anlaşmanın **Çıkış** değeri. **Çıkış** alanının *Madde* olarak gösterildiği anlaşmalar için boş bir indirim tutarı gösterilir.

1. **Ayrıntı** hızlı sekmesinde, **Marj tahmini** bölümünün aşağıdaki alanları içerdiğine dikkat edin. Bu alanlar İndirim yönetimi tarafından eklenir. Hepsi birim başına değerleri gösterir (**İndirim yönetimi** hızlı sekmesindeki alanlar satır için toplam değerleri gösterir).

    - **İndirim yönetimi indirim tutarı** (yalnızca satış siparişleri)
    - **İndirim yönetimi kâr payı tutarı** (yalnızca satış siparişleri)
    - **İndirim yönetimi satıcı indirimi tutarı** (satış siparişleri ve satınalma siparişleri)

1. **Fiyat ayrıntılarını** kapatın.
1. Satış siparişi, yeni görüntülediğiniz indirimler için uygun değilse indirimleri hariç tutmak için aşağıdaki adımları izleyin. (Ancak genellikle indirimleri hariç tutmazsınız.)

    1. **Satış siparişi satırları** hızlı sekmesinde ilgili satırı seçin.
    1. **Satır ayrıntıları** hızlı sekmesindeki **Fiyat ve iskonto** sekmesinde, **İndirim yönetiminden hariç tut** seçeneğini *Evet* olarak ayarlayın. Bu seçenek satınalma siparişleri için uygulanmaz. Ayrıca müşteri indirimleri yalnızca bu seçenek *Evet* olarak ayarlandığında hariç tutulur. Müşteri kâr payı ve satıcı indirimleri hala uygulanabilir.

1. Eylem bölmesinde, **Çek ve paketle** sekmesinde, **Oluştur** grubunda, **Sevk irsaliyesini deftere naklet**'i seçin.
1. **Parametreler** hızlı sekmesindeki **Miktar** alanında, *Tümü* seçeneğini belirleyin.
1. **Tamam**'ı seçin.
1. İşlemi onaylamanız istendiğinde, **Tamam**'ı seçin.
1. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
1. **Parametreler** hızlı sekmesindeki **Miktar** alanında *Tümü* veya *Sevk irsaliyesi*'ni seçin.
1. **Tamam**'ı seçin.
1. İşlemi onaylamanız istendiğinde, **Tamam**'ı seçin.

## <a name="process-rebate-management-deals"></a><a name="process-deals"></a>İndirim yönetimi anlaşmalarını işleme

Bir anlaşmayı işlediğinizde sistem ayarlanan tüm ilgili indirimleri ve kâr paylarını hesaplar. Yalnızca hesaplanmaya hazır ve durumu *etkin* olan hesaplama dönemleri olan seçili anlaşmalar işlenir. İşleme tamamlandıktan sonra, sistem incelenebilecek ve deftere nakledebileceğiniz bir dizi işlem oluşturur.

> [!NOTE]
> Tüm durumlarda, indirimler her bir anlaşma **Mutabakat Ölçütü** ayarı tarafından belirtilen düzeyde (*Anlaşma* veya *satır*) işlenir. Tek satırlı hesaplamaları yalnızca **Mutabakat ölçütü** alanının *satır* olarak ayarlandığı anlaşmalar için yapabilirsiniz.

### <a name="process-all-lines-for-one-or-more-deals"></a>Bir veya daha fazla anlaşma için tüm satırları işleme

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. İşlemek istediğiniz her bir anlaşma için satırı seçin (veya işlemek istediğiniz anlaşmayı açın).
1. Eylem bölmesinde, **indirim yönetimi anlaşmaları** sekmesinde, **Oluştur** grubunda, aşağıdaki komutlardan birini seçin:

    - **İşlem \> sağlama**: Her bir ilgili indirim anlaşması için bir dizi tahakkuk sağlayın, ancak deftere nakletmeyin. Bu menü öğesi, **İndirim çıkışı** alanının *Madde* olarak ayarlandığı anlaşmalar için kullanılamaz.
    - **İşlem \> İndirim yönetimi**: Her bir anlaşma için indirimin değerini sağlayan bir dizi işlem işler.
    - **İşlem \> Silme**: İndirim anlaşması ve belirtilen dönem için her kaynak hareketi için, bir hüküm ve indirim yönetimi için deftere nakledilen tutarlar arasındaki farkı işleyin. Bu menü öğesi, **İndirim çıkışı** alanının *Madde* olarak ayarlandığı anlaşmalar için kullanılamaz.

1. Görüntülenen iletişim kutusunda, Hesaplama için tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. Hesaplamayı çalıştırmak için **Tamam**'ı seçin.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Seçili bir anlaşma için bir veya daha fazla belirli anlaşma satırını işleyin

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. Bir satırını işlemek istediğiniz anlaşmayı açın.
1. Sağ üst köşedeki **satırlar** sekmesini seçin.
1. **İndirim Yönetimi** hızlı sekmesinde, işlemek istediğiniz her bir anlaşma satırı için satırı seçin.
1. **İndirim Yönetimi** hızlı sekmesindeki araç çubuğunda, aşağıdaki komutlardan birini seçin. (Bu komutlar yalnızca, **mutabakat ölçütü** alanının *satır* olarak ayarlandığı anlaşmalar için mevcuttur.)

    - **İşlem \> sağlama**: Her bir ilgili anlaşma satırı için bir dizi tahakkuk sağlayın, ancak deftere nakletmeyin. Bu menü öğesi, **İndirim çıkışı** alanının *Madde* olarak ayarlandığı anlaşmalar için kullanılamaz.
    - **İşlem \> İndirim yönetimi**: Her bir anlaşma satırı için indirimin değerini sağlayan bir dizi işlem işler.
    - **İşlem \> Silme**: İndirim anlaşması ve belirtilen dönem için her kaynak hareketi için, bir hüküm ve indirim yönetimi için deftere nakledilen tutarlar arasındaki farkı işleyin. Bu menü öğesi, **İndirim çıkışı** alanının *Madde* olarak ayarlandığı anlaşmalar için kullanılamaz. 

1. Görüntülenen iletişim kutusunda, Hesaplama için tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. Hesaplamayı çalıştırmak için **Tamam**'ı seçin.

### <a name="process-deals-using-a-batch-job"></a>Bir toplu işi kullanarak anlaşmaları işleme

Belirli anlaşmalar veya anlaşma satırlarını işlemek yerine, aynı anda birden fazla anlaşmayı işlemek için bir toplu iş çalıştırabilirsiniz. İsteğe bağlı olarak kayıt filtreleri uygulayabilir ve/veya tekrarlayan bir çizelge ayarlayabilirsiniz. Bir toplu işi kullanarak anlaşmaları işlemek için, aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - Her ilgili anlaşma için, deftere nakletmeden bir dizi tahakkuk sağlamak için **indirim Yönetimi \> periyodik görevler \> İşleme \> Sağlama** bölümüne gidin.
    - Her bir anlaşma satırı için indirimin değerini sağlayan bir dizi işlem işlemek için **İndirim yönetimi \> Periyodik görevler \> İşleme \> İndirim yönetimi** bölümüne gidin.
    - Yeni indirim anlaşması işlemlerinin hesaplanabilmesi için daha önce deftere nakledilmiş işlemleri silmek üzere tersine çevirmek için **İndirim yönetimi \> Periyodik görevler \> İşleme \> Sil** bölümüne gidin.

1. Görüntülenen iletişim kutusunda, **parametreler** hızlı sekmesinde, **Dönem** bölümünde, Hesaplama işlemlerinin tarih aralığını tanımlamak için **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. **Garanti Dönemi** bölümünde, Hesaplama için garantiye yönelik tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. **Dahil edilecek kayıtlar** Hızlı sekmesi'nde, toplu işlerin işleneceği anlaşmaları sınırlamak için filtreler ayarlayabilirsiniz. Bu ayarlar, diğer toplu iş türlerinde çalıştıkları gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinde gerektiğinde toplu işleme ve planlama seçeneklerini ayarlayabilirsiniz. Bu ayarlar, diğer toplu iş türlerinde çalıştıkları gibi çalışır.
1. Hesaplamayı çalıştırmak ve/veya zamanlamak için **Tamam**'ı seçin.

### <a name="process-deals-by-using-the-rebate-workbench"></a>İndirim workbench'ini kullanarak anlaşmaları işleme

Özel anlaşmaları veya anlaşma satırlarını işlemek yerine aynı anda birden çok anlaşmayı işlemek için *indirim workbench*'ini kullanabilirsiniz. İsteğe bağlı olarak kayıt filtreleri uygulayabilir ve/veya tekrarlayan bir çizelge ayarlayabilirsiniz. Herhangi bir satırı seçmeniz gerekmez. Sistem, ayarladığınız tarih ve filtre gereksinimlerini karşılayan tüm satırları işler.

İndirim workbench'ini kullanarak anlaşmaları işlemek için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> İndirim yönetimi anlaşmaları \> İndirim workbench'i** bölümüne gidin.
1. Eylem Bölmesi'ndeki **İndirim workbench'i** sekmesinde, **İşlem** grubunda, aşağıdaki komutlardan birini seçin:

    - **İşlem \> Sağla**: Her ilgili anlaşma satırı için bir dizi tahakkuk sağlayın ancak tahakkukları deftere nakletmeyin.
    - **İşlem \> İndirim yönetimi**: Her bir anlaşma satırı için indirimin değerini sağlayan bir dizi işlem işler.
    - **İşlem \> Sil**: İndirim anlaşması ve belirtilen dönem başına her kaynak hareketi için deftere nakledilen provizyon ve indirim yönetimi arasındaki farkı işleyin.

1. **İndirim yönetimi** iletişim kutusundak, **Dönem** bölümünde, hesaplama için tarih aralığını tanımlamak için **Başlangıç tarihi** ve **Bitiş tarihi** alanlarını ayarlayın.
1. **Garanti dönemi** bölümünde, hesaplama için garantiye yönelik tarih aralığını tanımlamak üzere **Başlangıç tarihi** ve **Bitiş tarihi** alanlarını ayarlayın.
1. **Dahil edilecek kayıtlar** Hızlı sekmesi'nde, toplu işlerin işleneceği anlaşmaları sınırlamak için filtreler ayarlayabilirsiniz. Bu ayarlar, diğer toplu iş türlerinde çalıştıkları gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinde gerektiğinde toplu işleme ve planlama seçeneklerini ayarlayabilirsiniz. Bu ayarlar, diğer toplu iş türlerinde çalıştıkları gibi çalışır.
1. Hesaplamayı çalıştırmak ve/veya zamanlamak için **Tamam**'ı seçin.

## <a name="view-and-edit-rebate-management-transactions"></a>Indirim yönetimi işlemlerini görüntüleme ve Düzenleme

Bir veya daha fazla anlaşma işlediğinizde sistem deftere nakletmeden önce görüntüleyebileceğiniz ve belki de düzenleyebileceğiniz işlemler oluşturur.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-deals-list-page"></a>İndirim anlaşmaları listesi sayfasını kullanarak İndirim yönetimi hareketlerini görüntüleme ve düzenleme

İndirim anlaşmaları listesi sayfasını kullanarak İndirim yönetimi hareketlerini görüntülemek ve düzenlemek için aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - İşlemlerini görüntülemek için anlaşmayı seçin (örneğin, [**tüm indirim yönetimi anlaşmaları** sayfasında](rebate-management-deals.md)). Eylem bölmesinde, **indirim yönetimi anlaşmaları** sekmesinde, **İşlemler** grubunda, görüntülemek istediğiniz işlem türüne bağlı olarak **İşlemler** veya **garanti işlemlerini** seçin.
    - Ayrıntılarını görüntülemek için anlaşmayı açın (örneğin, [**tüm indirim yönetimi anlaşmaları** sayfasında](rebate-management-deals.md)). **İndirim yönetimi** hızlı sekmesinde, hareketlerini görüntülemek üzere anlaşma satırını seçin. Ardından, araç çubuğunda, görüntülemek istediğiniz işlem türüne bağlı olarak **İşlemler** veya **Garanti işlemleri**'ni seçin. (Bu düğmeler yalnızca, **mutabakat ölçütü** alanının *satır* olarak ayarlandığı anlaşmalar için mevcuttur.)

1. **İndirim yönetimi tarih işlemleri** veya **indirim yönetimi garanti işlemleri** sayfası görüntülenir. Her satır tek bir indirim veya garanti döneminden alınan işlemler koleksiyonunu temsil eden bir kılavuz içerir. Kılavuzda bir satır seçin ve sonra eylem bölmesinde, Bu satıra ait işlemleri görüntülemek için **kaynak işlemlerini** seçin.
1. Görüntülenen sayfa, seçili satıra ait seçili türün işlem listesini gösterir. İşlem türüne bağlı olarak her işlem ilgili detayları sağlar. Garanti işlemleri için yalnızca listeyi görüntüleyebilirsiniz. Diğer işlem türleri için bu sayfada aşağıdaki eylemleri gerçekleştirebilirsiniz:

    - Sayfadaki tüm talep edilen işlemlerin toplam değerini doğrulamak için **talep edilen tutar** alanını görüntüleyin.
    - Herhangi bir işlemle ilgili daha fazla bilgi görüntülemek için, işlemi seçin ve **genel**, **mali boyut** veya **Boyut** sekmesini seçin.
    - Uygulanan indirimleri görüntülemek için, Eylem bölmesinde **İndirim işlemleri**'ni seçin. Daha fazla bilgi için [indirim azaltma ilkeleri](rebate-reduction-principle.md) konusuna bakın.
    - Bir talep işlemi kullanıyorsanız, işlemleri talep edilmiş veya talep edilmemiş olarak işaretlemek için ilgili satırları seçin ve eylem bölmesinde, aşağıdaki komutlardan birini seçin. (Talep işlemlerini, [**İndirim yönetimi parametreleri** sayfasında](rebate-management-parameters.md) etkinleştirin.)

        - **Talep edildi olarak ayarla \> Tümü**: Tüm işlemleri talep edildi olarak işaretler.
        - **Talep edildi olarak ayarla \> Seçili**: Seçili işlemleri talep edildi olarak işaretler.
        - **Talep edilmedi olarak ayarla \> Tümü**: Tüm işlemleri talep edilmedi olarak işaretler.
        - **Talep edilmedi olarak ayarla \> Seçili**: Seçili işlemleri talep edilmedi olarak işaretler.

    - Tüm ilgili satırlar için talebi deftere nakletmek üzere Eylem Bölmesinde **Deftere Naklet**'i seçin. Bir talepler işlemi kullanıyorsanız (**İndirim yönetimi parametreleri** sayfasında **Talep işlemini kullan** seçeneği etkinleştirildiğinde), yalnızca **Talep Edildi** olarak işaretlenmiş satırlar deftere nakledilir. Aksi takdirde, seçili indirim hareketi için tüm kaynak hareketler deftere nakledilir. **Deftere naklet** düğmesi yalnızca indirim hareketleri için kullanılabilir. Sağlama ve silme hareketleri için kullanılamaz. **Deftere Naklet** iletişim kutusunda, **Başlangıç tarihi** ve **Bitiş tarihi** alanları otomatik olarak ayarlanır. **Deftere nakil tarihi** alanını ayarlayın ve **Tamam**'ı seçin.
    - Açık veya deftere nakledilmemiş işlemler için Gösterilen tutarı ayarlamak için, işlemi seçin ve aşağıdaki adımlardan birini izleyin:

        - **Düzeltilen tutar** alanındaki değeri Düzenleyin.
        - Eylem bölmesinde, **Düzeltmeyi ayarla**'yı seçin. Ardından, görüntülenen açılan iletişim kutusunda **Düzeltilen tutar** alanına bir değer girin.

> [!NOTE]
> Talepler işlemini kullanıyorsanız, bir sonraki dönemi işlediğiniz zaman, işlem listesi önceki deftere nakil işleminden talep edilmeyen işlemleri ve Seçili döneme ait yeni işlemleri içerir.

### <a name="view-and-edit-rebate-management-transactions-by-using-the-rebate-workbench"></a>İndirim workbench'ini kullanarak İndirim yönetimi hareketlerini görüntüleme ve düzenleme

İndirim workbench'ini kullanarak İndirim yönetimi hareketlerini görüntülemek ve düzenlemek için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> İndirim yönetimi anlaşmaları \> İndirim workbench'i** bölümüne gidin.
1. **Göster** alanını *Deftere nakledilmemiş* olarak ayarlayın.
1. **İndirim workbench'i** sayfası hareketlerin listesini gösterir. Her hareket, ilgili ayrıntıları sağlar. İşlem türüne bağlı olarak bu ayrıntılar farklılık gösterir. Bu sayfada aşağıdaki eylemleri gerçekleştirebilirsiniz:

    - Herhangi bir işlemle ilgili daha fazla bilgi görüntülemek için, işlemi seçin ve **genel**, **mali boyut** veya **Boyut** sekmesini seçin.
    - Talep işlemi kullanıyorsanız işlemleri talep edildi veya talep edilmedi olarak işaretleyebilirsiniz. İlgili satırları seçin ve ardından Eylem Bölmesi'ndeki **İndirim workbench'i** sekmesinde aşağıdaki komutlardan birini seçin. (Talep işlemlerini [**İndirim yönetimi parametreleri**](rebate-management-parameters.md) sayfasında etkinleştirin.)

        - **Talep edildi olarak ayarla**: Seçili işlemleri talep edildi olarak işaretler.
        - **Talep edilmedi olarak ayarla**: Seçili işlemleri talep edilmedi olarak işaretler.

    - Bir veya daha fazla satır için talebi deftere nakletmek için ilgili satırları seçin. Eylem Bölmesi'ndeki **İndirim workbench'i** sekmesinde, **Deftere naklet**'i seçin. **Deftere Naklet** düğmesi, provizyon, indirim ve silme hareketler için kullanılabilir. **Deftere Naklet** iletişim kutusunda, **Başlangıç tarihi** ve **Bitiş tarihi** alanları otomatik olarak ayarlanır. **Deftere nakil tarihi** alanını ayarlayın ve **Tamam**'ı seçin.
    - Açık veya deftere nakledilmemiş işlemler için Gösterilen tutarı ayarlamak için, işlemi seçin ve aşağıdaki adımlardan birini izleyin:

        - **Düzeltilen tutar** alanındaki değeri Düzenleyin.
        - Eylem Bölmesi'ndeki **İndirim workbench'i** sekmesinde, **Düzeltmeyi ayarla**'yı seçin. Ardından, görüntülenen açılan iletişim kutusunda **Düzeltilen tutar** alanına bir değer girin.

> [!NOTE]
> Talepler işlemini kullanıyorsanız, bir sonraki dönemi işlediğiniz zaman, işlem listesi önceki deftere nakil işleminden talep edilmeyen işlemleri ve Seçili döneme ait yeni işlemleri içerir.

## <a name="post-rebates-transactions"></a>İndirim işlemlerini deftere nakletme

İşlenmiş bir provizyonun değerini, indirim yönetimi tutarını ve silmeyi deftere nakletmek için deftere nakil işlemini çalıştırmanız gerekir. Deftere nakil işlemi, provizyon, indirim yönetimi veya silme hareketlerini deftere nakledilmiş olarak işaretler ve hedef hareketi oluşturur. Hedef işlemi gözden geçirmeniz gerekmezse, bu işlemler otomatik olarak deftere nakledilecek şekilde ayarlanabilir.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Sistemi tüm hedef işlemleri otomatik olarak deftere nakletmek için ayarla

Sisteminizi, bir provizyon deftere nakil işlemi, indirim yönetimi tutarı veya silme tarafından oluşturuldukları anda tüm hedef işlemleri deftere nakledebilmek üzere ayarlamak için, **indirim yönetimi parametreleri** sayfasında **günlükleri otomatik olarak deftere naklet** ve/veya **serbest metin faturalarını otomatik olarak deftere naklet** seçeneğini etkinleştirin. Daha fazla bilgi için bkz. [İndirim yönetimi parametreleri](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Bir veya daha fazla anlaşma için işlemleri deftere nakletme

İlgili anlaşmaları işledikten sonra, bir veya daha fazla anlaşma için oluşturulan işlemleri gözden geçirip deftere nakletmek için aşağıdaki adımları izleyin.

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. Deftere nakletmek istediğiniz her bir anlaşma için satırı seçin (veya deftere nakletmek istediğiniz anlaşmayı açın).
1. Eylem bölmesinde, **indirim yönetimi anlaşmaları** sekmesinde, **Oluştur** grubunda, aşağıdaki komutlardan birini seçin:

    - **Deftere naklet \> Sağlama**: Oluşturduğunuz mevcut tahakkuk işlemlerini deftere nakledin.
    - **Deftere naklet \> İndirim yönetimi**: Oluşturduğunuz indirim işlemlerini deftere nakledin.
    - **Deftere naklet \> Sil**: Oluşturduğunuz indirim işlemlerini silin.

1. Görüntülenen iletişim kutusunda **Deftere nakletme tarihi** alanını ayarlayın. Ardından deftere nakledilecek işlemler için tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. İşlemleri deftere nakletmek için **Tamam**'ı seçin.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Seçili bir anlaşma için bir veya daha fazla belirli anlaşma satırı için işlemleri deftere nakletme

İlgili anlaşmaları işledikten sonra, seçil anlaşma için bir veya daha özel fazla satırı için oluşturulan işlemleri gözden geçirip deftere nakletmek için aşağıdaki adımları izleyin. Bu yordam yalnızca, **Mutabakat ölçütü** alanının *Satır* olarak ayarlandığı anlaşmalar için geçerlidir.

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. İşlemleri deftere nakletmek istediğiniz satırı içeren anlaşmayı açın.
1. Sağ üst köşedeki **satırlar** sekmesini seçin.
1. **İndirim Yönetimi** hızlı sekmesinde, deftere nakletmek istediğiniz her bir anlaşma satırı için satırı seçin.
1. **İndirim Yönetimi** hızlı sekmesindeki araç çubuğunda, aşağıdaki komutlardan birini seçin. (Bu komutlar yalnızca, **mutabakat ölçütü** alanının *satır* olarak ayarlandığı anlaşmalar için mevcuttur.)

    - **Deftere naklet \> Sağlama**: Oluşturduğunuz mevcut tahakkuk işlemlerini deftere nakledin.
    - **Deftere naklet \> İndirim yönetimi**: Oluşturduğunuz indirim işlemlerini deftere nakledin.
    - **Deftere naklet \> Sil**: Oluşturduğunuz indirim işlemlerini silin.

1. Görüntülenen iletişim kutusunda **Deftere nakletme tarihi** alanını ayarlayın. Ardından deftere nakledilecek işlemler için tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. İşlemleri deftere nakletmek için **Tamam**'ı seçin.

### <a name="post-transactions-using-a-batch-job"></a>İşlemleri toplu iş kullanarak deftere nakletme

Belirli anlaşmalar veya anlaşma satırları için işlemleri deftere nakletmek yerine aynı anda birden fazla anlaşma için işlemleri deftere nakletmek üzere bir toplu iş çalıştırabilirsiniz. İsteğe bağlı olarak kayıt filtreleri uygulayabilir ve/veya tekrarlayan bir çizelge ayarlayabilirsiniz. Bir toplu işi kullanarak anlaşmaları deftere nakletmek için, aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - **İndirim Yönetimi \> Periyodik görevler \> Deftere Naklet \> Sağla** bölümüne giderek, oluşturduğunuz mevcut tahakkuk işlemlerini deftere nakledin.
    - **İndirim Yönetimi \> Periyodik görevler \> Deftere Naklet \> İndirim yönetimi** bölümüne giderek, oluşturduğunuz indirim işlemlerini deftere nakledin.
    - **İndirim Yönetimi \> Periyodik görevler \> Deftere Naklet \> Sil** bölümüne giderek, oluşturduğunuz silme işlemlerini deftere nakledin.

1. Görüntülenen iletişim kutusunda **parametreler** hızlı sekmesinde, **Dönem** bölümünde, **deftere nakil tarihi** alanını ayarlayın. Ardından deftere nakledilecek işlemler için tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. **Garanti Dönemi** bölümünde, deftere nakledilecek garantilere yönelik tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. **Dahil edilecek kayıtlar** Hızlı sekmesi'nde, toplu işlerin işleneceği anlaşmaları sınırlamak için filtreler ayarlayabilirsiniz. Bu ayarlar, diğer toplu iş türlerinde çalıştıkları gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinde gerektiğinde toplu işleme ve planlama seçeneklerini ayarlayabilirsiniz. Bu ayarlar, diğer toplu iş türlerinde çalıştıkları gibi çalışır.
1. Hesaplamayı çalıştırmak ve/veya zamanlamak için **Tamam**'ı seçin.

### <a name="post-transactions-by-using-the-rebate-workbench"></a>İndirim workbench'ini kullanarak işlemleri deftere nakletme

Provision, indirim veya silme hareketlerini işledikten sonra, tüm anlaşmalar için bir veya daha fazla özel hareket satırı için oluşturulan hareketleri gözden geçirmek ve deftere nakletmek üzere indirim workbench'ini kullanmak için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> İndirim yönetimi anlaşmaları \> İndirim workbench'i** bölümüne gidin.
1. Izgarada, deftere nakletmek istediğiniz her bir hareket satırı için satırı seçin. Nakledilmemiş provizyon, indirim ve/veya silme hareketlerini seçebilirsiniz. Geçerli olan kurallar şunlardır:

    - Sistem ayrıca seçtiğiniz satırlarla aynı **İndirim hareket numarası** değerine sahip tüm satırları deftere nakleder.
    - Sistem, talep edildiği gibi işaretlenmemiş *İndirim* hareket türünün hiçbir satırını deftere nakletmez.
    - Önceden deftere nakledilmemiş satırları seçerseniz sistem, deftere nakledilen satırları atlar.
    - **Deftere Naklet** düğmesi yalnızca deftere nakledilmemiş en az bir satır seçerseniz kullanılabilir.

1. Eylem Bölmesi'ndeki **İndirim workbench'i** sekmesinde, **İşlem** grubunda **Deftere Naklet**'i seçin.
1. **Deftere Naklet** iletişim kutusunda, **Deftere nakil tarihi** alanını ayarlayın. **Başlangıç tarihi** ve **Bitiş tarihi** alanları, seçilen satırlar için en erken **Başlangıç tarihi** değerine ve en son **Bitiş tarihi** değerine göre otomatik olarak ayarlanır.
1. İşlemleri deftere nakletmek için **Tamam**'ı seçin.

## <a name="review-rebate-management-journals"></a><a name="review-journals"></a>İndirim yönetimi günlüklerini gözden geçirme

İşlemleriniz deftere nakledildikten sonra, sonuçta elde edilen günlükleri, belgeleri veya maddeleri gözden geçirebilirsiniz. İndirimler ve kâr payları ile ilgili hedef işlemler deftere nakil profilinde ayarlanan ödeme türüne ve indirimin çıktı türüne dayanır. Örneğin, indirim çıkışı *Madde* olarak ayarlanırsa, müşteri indirimi için bir satış siparişi oluşturulur ve satıcı indirimi için bir satınalma siparişi oluşturulur. Bu siparişler hedef hareketler üzerinden görüntülenebilir. Alternatif olarak, ödeme borç hesapları kullanacak şekilde ayarlanmışsa, Müşteri indirimleri için müşteri üzerinde ayarlanmış satıcı için bir satıcı faturası oluşturulur.

### <a name="review-journals-by-using-the-rebate-deals-list-page"></a>İndirim anlaşmaları listesi sayfasını kullanarak günlükleri inceleme

İndirim yönetimi ile ilişkili yevmiye defteri girişlerini gözden geçirmek için aşağıdaki adımları izleyin.

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. Yevmiye defteri girişlerini incelemek için anlaşmayı seçin.
1. Eylem bölmesinde, **indirim yönetimi anlaşmaları** sekmesinde, **İşlemler** grubunda, bakmak istediğiniz işlem türüne bağlı olarak **İşlemler** veya **Garanti işlemleri**'ni seçin.
1. **Göster** alanını *Tümü* veya *Deftere Nakledildi* olarak ayarlayın.
1. İncelemek istediğiniz işlem koleksiyonunu bulun ve seçin, sonra eylem bölmesinde, aşağıdaki düğmelerden birini seçin. (Bu düğmeler yalnızca seçili işlem koleksiyonu için ilgili deftere nakil varsa kullanılabilir.)

    - **Hedef işlemleri**: İlgili günlükleri ve seçili anlaşma tarafından oluşturulan diğer belge tiplerini gözden geçirin.
    - **Maddeler**: Seçili anlaşma tarafından oluşturulan ilgili satış siparişlerini veya satınalma siparişlerini gözden geçirin.

1. İlgili günlüklerin, belgelerin veya maddelerin listesi görüntülenir. Herhangi bir günlük, belge veya öğe hakkında daha fazla bilgi görüntülemek için, ilgili satırı seçin ve eylem bölmesinde **Ayrıntıları görüntüle**'yi seçin.

### <a name="review-journals-by-using-the-rebate-workbench"></a>İndirim workbench'ini kullanarak günlükleri inceleme

İndirim workbench'ini kullanarak günlükleri incelemek için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> İndirim yönetimi anlaşmaları \> İndirim workbench'i** bölümüne gidin.
1. **Göster** alanını _Tümü_ veya _Deftere Nakledildi_ olarak ayarlayın.
1. İncelemek istediğiniz satırı bulup seçin. Ardından Eylem Bölmesi'ndeki **İndirim workbench'i** sekmesinde, **Görüntüleme** grubunda, **Hedef hareketler**'i seçin. Bu düğme, yalnızca seçilen satır için ilgili deftere nakiller mevcutsa kullanılabilir.
1. İlgili günlüklerin, belgelerin veya maddelerin listesi görüntülenir. Herhangi bir günlük, belge veya öğe hakkında daha fazla bilgi görüntülemek için, ilgili satırı seçin ve eylem bölmesinde **Ayrıntıları görüntüle**'yi seçin.

## <a name="rebate-management-transactions-on-the-deduction-workbench"></a>Kesinti workbench'inde indirim yönetimi hareketleri

Aşağıdaki **Ödeme türü** değerlerinden birine sahip bir İndirim yönetimi hareketini deftere naklettiğinizde, sistem ilgili müşteri hesabı için bir müşteri kesinti günlüğü veya serbest metin faturası oluşturur:

- Müşteri kesintileri
- Vergi faturası müşteri kesintileri
- Ticari harcama
- Raporlama

Hedef hareketi oluşturulup deftere nakledildikten sonra, **Kesinti workbench'i** sayfasında (**Satış ve pazarlama \> Ticari Tahsisatlar \> Kesintiler \> Kesinti workbench'i**) açık hareket olarak kullanılabilir. Açık işlemlerin **Talep türü** değeri *İndirim yönetimi*'dir ve izlenebilirliği etkinleştirmek için **İndirim hareketi numarası** değeri mevcuttur. Tarih, İndirim yönetimi hedef hareketinin deftere nakil tarihine ayarlanır. Açık hareketleri aynı müşteri hesabı için mevcut kesintilerde kapatmak üzere kesinti workbench'ini kullanmak için, Eylem Bölmesi'nde **Koru \> Eşleştir**'i seçin.

Daha fazla bilgi için bkz. [Kesinti workbench'ini kullanarak kesintileri yönetme](deduction-workbench.md).

## <a name="purge-unposted-transactions"></a>Deftere nakledilmemiş işlemleri temizleme

Provision, indirim veya silme hareketlerini işledikten sonra, seçilen deftere nakledilmemiş hareketleri temizlemek için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> İndirim yönetimi anlaşmaları \> İndirim workbench'i** bölümüne gidin.
2. **Göster** alanını *Deftere nakledilmemiş* olarak ayarlayın.
3. Silinecek hareketleri bulup seçin. Eylem Bölmesi'ndeki **İndirim workbench'i** sekmesinde, **İşlem** grubunda **Temizle**'yi seçin.
4. Deftere nakledilmemiş hareketleri silmek için **Tamam**'ı seçin.

## <a name="cancel-a-posted-provision"></a>Deftere nakledilen provizyonu iptal etme

Provizyonu işleyip deftere naklettikten sonra, deftere nakledilen provizyon hareketlerini iptal etmek için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> İndirim yönetimi anlaşmaları \> İndirim workbench'i** bölümüne gidin.
2. **Göster** alanını *Deftere Nakledildi* olarak ayarlayın.
3. İptal edilecek provizyon hareketlerini bulup seçin. Ardından, Eylem Bölmesi'ndeki **İndirim workbench'i** sekmesinde, **İşlem** grubunda **Provizyonu iptal et**'i seçin.
4. Hareketleri tersine çevirmek için **Tamam**'ı seçin.

Bu provisyon ters işlemleri de ilgili [İndirim yönetimi günlüklerinde](#review-journals) görünür.

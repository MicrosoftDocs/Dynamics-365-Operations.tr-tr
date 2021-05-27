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
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 5188fa271cd9eb24140a9edcf507a3da72b61074
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020543"
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

## <a name="process-rebate-management-deals"></a>İndirim yönetimi anlaşmalarını işleme

Bir anlaşmayı işlediğinizde sistem ayarlanan tüm ilgili indirimleri ve kâr paylarını hesaplar. Yalnızca hesaplanmaya hazır ve durumu *etkin* olan hesaplama dönemleri olan seçili anlaşmalar işlenir. İşleme tamamlandıktan sonra, sistem incelenebilecek ve deftere nakledebileceğiniz bir dizi işlem oluşturur.

> [!NOTE]
> Tüm durumlarda, indirimler her bir anlaşma **Mutabakat Ölçütü** ayarı tarafından belirtilen düzeyde (*Anlaşma* veya *satır*) işlenir. Tek satırlı hesaplamaları yalnızca **Mutabakat ölçütü** alanının *satır* olarak ayarlandığı anlaşmalar için yapabilirsiniz.

### <a name="process-all-lines-for-one-or-more-deals"></a>Bir veya daha fazla anlaşma için tüm satırları işleme

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. İşlemek istediğiniz her bir anlaşma için satırı seçin (veya işlemek istediğiniz anlaşmayı açın).
1. Eylem bölmesinde, **indirim yönetimi anlaşmaları** sekmesinde, **Oluştur** grubunda, aşağıdaki komutlardan birini seçin:

    - **İşlem \> sağlama**: Her bir ilgili indirim anlaşması için bir dizi tahakkuk sağlayın, ancak deftere nakletmeyin.
    - **İşlem \> İndirim yönetimi**: Her bir anlaşma için indirimin değerini sağlayan bir dizi işlem işler.
    - **İşlem \> Sil**: Yeni indirim anlaşması işlemlerinin hesaplanabilmesi için daha önce deftere nakledilmiş işlemleri silmek üzere tersine çevirir.

1. Görüntülenen iletişim kutusunda, Hesaplama için tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. Hesaplamayı çalıştırmak için **Tamam**'ı seçin.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Seçili bir anlaşma için bir veya daha fazla belirli anlaşma satırını işleyin

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. Bir satırını işlemek istediğiniz anlaşmayı açın.
1. Sağ üst köşedeki **satırlar** sekmesini seçin.
1. **İndirim Yönetimi** hızlı sekmesinde, işlemek istediğiniz her bir anlaşma satırı için satırı seçin.
1. **İndirim Yönetimi** hızlı sekmesindeki araç çubuğunda, aşağıdaki komutlardan birini seçin. (Bu komutlar yalnızca, **mutabakat ölçütü** alanının *satır* olarak ayarlandığı anlaşmalar için mevcuttur.)

    - **İşlem \> sağlama**: Her bir ilgili anlaşma satırı için bir dizi tahakkuk sağlayın, ancak deftere nakletmeyin.
    - **İşlem \> İndirim yönetimi**: Her bir anlaşma satırı için indirimin değerini sağlayan bir dizi işlem işler.
    - **İşlem \> Sil**: Yeni indirim anlaşması işlemlerinin hesaplanabilmesi için daha önce deftere nakledilmiş işlemleri silmek üzere tersine çevirir.

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

## <a name="view-and-edit-rebate-management-transactions"></a>Indirim yönetimi işlemlerini görüntüleme ve Düzenleme

Bir veya daha fazla anlaşma işlediğinizde sistem deftere nakletmeden önce görüntüleyebileceğiniz ve belki de düzenleyebileceğiniz işlemler oluşturur.

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

    - Bir veya daha fazla satır için talebi deftere nakletmek için ilgili satırları seçin ve eylem bölmesinde, **Deftere Naklet**'i seçin. (**Deftere naklet** düğmesi yalnızca indirim işlemleri için kullanılabilir. Bu, sağlama ve silme işlemleri için kullanılamaz.) **Deftere naklet** iletişim kutusunda, **Başlangıç tarihi** ve **bitiş tarihi** alanları otomatik olarak ayarlanır. **Deftere nakil tarihi** alanını ayarlayın ve **Tamam**'ı seçin.
    - Açık veya deftere nakledilmemiş işlemler için Gösterilen tutarı ayarlamak için, işlemi seçin ve aşağıdaki adımlardan birini izleyin:

        - **Düzeltilen tutar** alanındaki değeri Düzenleyin.
        - Eylem bölmesinde, **Düzeltmeyi ayarla**'yı seçin. Ardından, görüntülenen açılan iletişim kutusunda **Düzeltilen tutar** alanına bir değer girin.

> [!NOTE]
> Bir sonraki dönemi işlediğiniz zaman, işlem listesi önceki deftere nakil işleminden talep edilmeyen işlemleri ve Seçili döneme ait yeni işlemleri içerir.

## <a name="post-rebates-transactions"></a>İndirim işlemlerini deftere nakletme

İndirimlerin ve kesintilerin değerini deftere nakletmek için, sisteminizi otomatik olarak deftere nakletmek üzere ayarlamadıysanız, deftere nakil işlemini çalıştırmanız gerekir.

### <a name="set-up-the-system-to-post-all-transactions-automatically"></a>Sistemi tüm işlemleri otomatik olarak deftere nakletmek için ayarla

Sisteminizi, oluşturuldukları anda tüm işlemleri deftere nakledebilmek üzere ayarlamak için, **indirim yönetimi parametreleri** sayfasında **günlükleri otomatik olarak deftere naklet** ve/veya **serbest metin faturalarını otomatik olarak deftere naklet** seçeneğini etkinleştirin. Daha fazla bilgi için bkz. [İndirim yönetimi parametreleri](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Bir veya daha fazla anlaşma için işlemleri deftere nakletme

Otomatik deftere nakletmeyi kullanmıyorsanız, ilgili anlaşmaları işledikten sonra, bir veya daha fazla anlaşma için oluşturulan işlemleri gözden geçirip deftere nakletmek için aşağıdaki adımları izleyin.

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. Deftere nakletmek istediğiniz her bir anlaşma için satırı seçin (veya deftere nakletmek istediğiniz anlaşmayı açın).
1. Eylem bölmesinde, **indirim yönetimi anlaşmaları** sekmesinde, **Oluştur** grubunda, aşağıdaki komutlardan birini seçin:

    - **Deftere naklet \> Sağlama**: Oluşturduğunuz mevcut tahakkuk işlemlerini deftere nakledin.
    - **Deftere naklet \> İndirim yönetimi**: Oluşturduğunuz indirim işlemlerini deftere nakledin.
    - **Deftere naklet \> Sil**: Oluşturduğunuz indirim işlemlerini silin.

1. Görüntülenen iletişim kutusunda **Deftere nakletme tarihi** alanını ayarlayın. Ardından deftere nakledilecek işlemler için tarih aralığını tanımlamak üzere **başlangıç tarihi** ve **bitiş tarihi** alanlarını ayarlayın.
1. İşlemleri deftere nakletmek için **Tamam**'ı seçin.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Seçili bir anlaşma için bir veya daha fazla belirli anlaşma satırı için işlemleri deftere nakletme

Otomatik deftere nakletmeyi kullanmıyorsanız, ilgili anlaşmaları işledikten sonra, seçili anlaşma için bir veya daha fazla belirli anlaşma satırı için oluşturulan işlemleri gözden geçirip deftere nakletmek için aşağıdaki adımları izleyin.

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

## <a name="review-rebate-management-journals"></a>İndirim yönetimi günlüklerini gözden geçirme

İşlemleriniz deftere nakledildikten sonra, sonuçta elde edilen günlükleri, belgeleri veya maddeleri gözden geçirebilirsiniz. İndirimler ve kâr payları ile ilgili hedef işlemler deftere nakil profilinde ayarlanan ödeme türüne ve indirimin çıktı türüne dayanır. Örneğin, indirim çıktısı *madde* olarak ayarlanmışsa bir satış siparişi oluşturulur ve hedef işlemler aracılığıyla görüntülenebilir. Alternatif olarak, ödeme borç hesapları kullanacak şekilde ayarlanmışsa, Müşteri indirimleri için müşteri üzerinde ayarlanmış satıcı için bir satıcı faturası oluşturulur.

İndirim yönetimi ile ilişkili günlük girişlerini gözden geçirmek için aşağıdaki adımları izleyin.

1. Çalışmak istediğiniz işlem türü için uygun [indirim anlaşmaları listesi sayfasını](rebate-management-deals.md) açın.
1. Günlük girişlerini incelemek için anlaşmayı seçin.
1. Eylem bölmesinde, **indirim yönetimi anlaşmaları** sekmesinde, **İşlemler** grubunda, bakmak istediğiniz işlem türüne bağlı olarak **İşlemler** veya **İndirim işlemlerini** seçin.
1. **Göster** alanının *tüm* veya *deftere nakledilmiş* olarak ayarlandığından emin olun.
1. İncelemek istediğiniz işlem koleksiyonunu bulun ve seçin, sonra eylem bölmesinde, aşağıdaki düğmelerden birini seçin. (Bu düğmeler yalnızca seçili işlem koleksiyonu için ilgili deftere nakil varsa kullanılabilir.)

    - **Hedef işlemleri**: İlgili günlükleri ve seçili anlaşma tarafından oluşturulan diğer belge tiplerini gözden geçirin.
    - **Maddeler**: Seçili anlaşma tarafından oluşturulan ilgili maddeleri gözden geçirin.

1. İlgili günlüklerin, belgelerin veya maddelerin listesi görüntülenir. Herhangi bir günlük, belge veya öğe hakkında daha fazla bilgi görüntülemek için, ilgili satırı seçin ve eylem bölmesinde **Ayrıntıları görüntüle**'yi seçin.

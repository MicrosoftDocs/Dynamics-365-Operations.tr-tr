---
title: Sistemin yönlendirdiği iş sıralaması
description: Bu makale, sistemin yönlendirdiği iş sıralaması hakkında bilgi sağlar. Bu işlevsellik, sistemin yürütülmek üzere kullanıcılara sunduğu iş emirlerini sıralamanızı ve filtrelemenizi sağlar. Ambar malzeme çekme sürecini yönetmek için ek ölçütlerin gerekli olduğu senaryolarda yardımcı olur.
author: Mirzaab
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 1dab8d8bdace046f0f061713600fd1eab69e7c12
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335480"
---
# <a name="system-directed-work-sequencing"></a>Sistemin yönlendirdiği iş sıralaması

[!include [banner](../includes/banner.md)]

Sistemin yönlendirdiği iş sıralaması, sistemin yürütülmek üzere kullanıcılara sunduğu iş emirlerini sıralamanızı ve filtrelemenizi sağlar. Ambar malzeme çekme sürecini yönetmek için ek ölçütlerin (sevkiyat zamanı, malzeme çekme alanı, yerleşim profili veya çeşitli ölçütlerin birleşimi gibi) gerekli olduğu senaryolarda yardımcı olur.

Bu işlevsellik, kullanıcıların oluşturulan tüm iş emirlerini değerlendirecek bir veya daha fazla sorgu ve bir sıra ayarlayabileceği, sistemin yönlendirdiği bir sorgu sırası ekleyerek, geçerli sistemin yönlendirdiği malzeme çekme işlevini genişletir. Yalnızca mobil cihaz menü öğesinin kurulumunda belirtilen ölçütlere uyan iş emirleri yakalanıp sunulur.

Bu nedenle, bu işlevsellik, belirtilen ölçütlere uyan iş emirlerini tanımladığı şekilde ambar çekme işlemlerinin daha iyi duruma getirilmesini sağlar, bunları doğru mobil cihaz menü öğesine atar ve sonra belirli bir beceri kümesi, malzeme çekme ekipmanı veya başka bir gereksinime göre bir çalışana sunar.

> [!NOTE]
> Farklı ölçütler gerekiyorsa, birden çok mobil cihaz menü öğesi kullanılmalıdır.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Kuruluş çapında sistemin yönlendirdiği iş sıralaması özelliği

Sistemin yönlendirdiği iş sıralamasını kullanabilmeniz için özelliğin sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Kuruluş çapında sistemin yönlendirdiği iş sıralaması*

## <a name="setup"></a>Ayar

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu makale altında sunulan değerleri kullanarak bu senaryoyla çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklenmiş olduğu bir sistemde çalışmanız gerekir. Ayrıca, **USMF** hukuk varlığını seçmelisiniz. Senaryo, tanıtım verilerinden ambar *51*'i kullanır.

> [!IMPORTANT]
> Siparişleri ambara serbest bırakmadan önce, çekme yerleşimlerinin siparişlerdeki tüm maddeler için yeterli stok içerdiğinden emin olun.
>
> Varsayılan USMF verileri bu senaryoyu desteklemelidir. Tanıtım verilerini kullanmıyorsanız satış siparişi çekmek üzere hangi malzeme çekme konumlarının kullanıldığını öğrenmek için **Yerleşim yönergesi** ayarını inceleyin. Stoku ayarlamanız gerekiyorsa, el ile hareketler oluşturabilir, stok yenilemeyi veya başka bir akışı kullanabilirsiniz.

### <a name="set-up-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi ayarlama

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Mobil cihaz menü öğeleri listesinde **Satış Malzeme Çekme – Sistem**'i seçin. Gerekli menü öğesi zaten mevcut olmalıdır. 
1. Şu ayarları onaylayın:

    - **Genel** hızlı sekmesinde **Yöneten** alanı *Sistem yönlendirmesinde* olarak ayarlanmalıdır.
    - **İş sınıfları** hızlı sekmesi aşağıdaki ayarları göstermelidir.

        | İş sınıfı kodu | İş siparişi türü |
        |---|---|
        | Satışlar | Satış siparişleri |
        | Satış Siparişi Çekme | Satış siparişleri |

1. Eylem bölmesinde **Sistemin yönlendirdiği iş sıralaması sorguları**'nı seçin.
1. **Düzenle** öğesini seçin.
1. Mevcut satırı silin ve sonra **Evet**'i seçerek eylemi onaylayın.
1. Eylem bölmesinde, bir satır oluşturmak için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** *1*
    - **Açıklama alanı:** *20'den az iş miktarı ve Azalan*

1. **Kaydet**'i seçin.
1. Eylem bölmesinde **Sorgu düzenle**'yi seçin.
1. **Birleşimler** sekmesinde, **İş satırları** tablosunu göstermek için birleştirme hiyerarşisini genişletin.
1. **İş satırları** tablo birleşimini seçin.
1. **Tablo birleşimi ekle**'yi seçin.
1. Görüntülenen listede, aşağıdaki ayarlara sahip satırı bulun ve seçin:

    - **Birleştirme modu:** *n:1*
    - **İlişki:** *Yerleşimler (Yerleşim)*

1. **Seç** öğesini seçin.

    Yerleşimler tablo birleşimine eklenir.

1. **Sıralama** sekmesinde, satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *İş miktarı* (Görünen ileti kutusunda, bu alana göre sıralama eklemek için **Evet**'i seçin.)
    - **Arama yönü:** *Azalan*

1. **Aralık** sekmesini seçin.

    Sıralamaya yalnızca belirli iş ölçütlerinin dahil edilmesi gerekiyorsa bunları **Aralık** sekmesinde belirtebilirsiniz. Bu örnekte, yalnızca miktarın 20 beher'den (en düşük ölçü birimi) az olduğu işleri dahil etmek istiyorsunuz.

    Bazı satırların zaten dahil edildiğini unutmayın. Bu satırların kaldırılmaması gerekir.

1. Bir satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *Stok iş miktarı*
    - **Ölçüt:** *\<20* (20'den az)

1. Bir satır daha eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *İş türü*
    - **Ölçüt:** *Malzeme çekme*

1. Bir satır daha eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Türetilmiş tablo:** *Yerleşimler*
    - **Alan:** *Yerleşim profili kodu*
    - **Ölçüt:** *!STAGE*

        > [!IMPORTANT]
        > *STAGE*'in önüne ünlem işareti (*!*) eklemeyi unutmayın.

1. Sorguyu kaydedip kapatmak için **Tamam**'ı seçin.
1. **Kaydet**'i seçin.
1. **Mobil cihaz menü öğeleri** sayfasına dönmek için sayfayı kapatın.

> [!NOTE]
> Bu kurulum, mobil cihaz menü öğesine uygun iş akışı için kullanılacak ölçütleri tanımlar. Sorguya başka ölçüt satırları eklerseniz, sistem ilk olarak en düşük sıra numaralı sorgu satırını kullanır. Başka bir deyişle, kullanıcıya önce sıra numarası 1 için uygun olan tüm işler ve ardından 2 numaralı sıra için tüm işler sunulur. Bu nedenle, belirli bir aralık ve sıralamanın birlikte kullanılması gerekiyorsa, bunlar aynı sistemin yönlendirdiği iş sırası sorgusunda belirtilmelidir.
>
> Bu kurulum, miktarın 20 beher'den az olduğu en az bir satır bulunan tüm işleri yakalar. Bu nedenle, işin, miktarı tam 20 beher veya 20 beherden fazla bir satırı varsa, bu, miktarın 20 beher'den az olduğu en az bir satırı olması koşuluyla geçerli olacaktır.

### <a name="location-directives"></a>Konum yönergeleri

Varsayılan Contoso verilerini kullanıyorsanız, yerleşim yönergesi eyleminin sorgusu için değişiklik yapılması gerekmez. Ancak, özelliği Contoso dışı bir ortama uyguladığınızda yerleşim yönergelerinin satış siparişlerindeki maddeleri yakalayacağından emin olmak için yeni bir yerleşim yönergesi oluşturun. Tanıtım ortamındaki ayarları doğrulamak için aşağıdaki adımları izleyin.

1. **Ambar Yönetimi** \> **Kurulum** \> **Konum yönergeleri** seçeneğine gidin.
1. **İş siparişi türü** alanında *Satış siparişi*'ni seçin.
1. *51 malzeme çekme* adlı yerleşim yönergesini seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, **Çek** eyleminin satırını seçin.
1. Kılavuzun yukarısında **Sorguyu düzenle**'yi seçin.
1. **Aralık** sorgusunu inceleyin.

    1. **Alan** alanının *Yerleşim* olarak ayarlandığı satırı bulun.
    2. **Ölçüt** alanının boş olduğundan emin olun (yani sınırlama yoktur).

## <a name="scenario"></a>Senaryo

### <a name="create-sales-order-picking-work"></a>Satış siparişi malzeme çekme işi oluşturma

Sistemin yönlendirdiği malzeme çekme işlemi çalıştırılmadan önce bazı giden işler oluşturulmalıdır. Bu senaryo için, belirtilen sistemin yönlendirdiği iş sırası sorgularını temel alan dört satış siparişi oluşturacaksınız.

Her satış siparişi için stok miktarlarını rezerve edeceksiniz. Bu nedenle, stok rezervasyonu veya stok rezervasyonunun bir kısmı iptal edilmedikçe, rezerve edilen stok diğer siparişler için ambardan çekilemez.

Bunun ardından, giden işi oluşturmak için her bir satış siparişini ambara serbest bırakacaksınız.

#### <a name="sales-order-1"></a>Satış siparişi 1

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem bölmesinde, satış siparişi 1'i oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri** bölümünde, **Müşteri hesabı** alanını *ABD-004* olarak ayarlayın.
    - **Genel** bölümünde, **Ambar** alanını *51* yapın.

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin. Satış siparişi numarasını not edin.
1. Yeni satış siparişine bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *M9200*
    - **Miktar:** *20*

1. Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.
1. **Rezervasyon** sayfasında stoku rezerve etmek için **Lotu rezerve et**'i seçin.
1. **Rezervasyon** sayfasını kapatın.
1. Eylem bölmesindeki **Ambar** sekmesinde **Ambara serbest bırak**'ı seçerek ambar için iş oluşturun.

    Satış siparişi için oluşturulan dalga kimliğini ve sevkiyat kimliklerini gösteren bilgi iletileri alırsınız.

#### <a name="sales-order-2"></a>Satış siparişi 2

1. Eylem bölmesinde, satış siparişi 2'yi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-007*
    - **Ambar:** *51*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin. Satış siparişi numarasını not edin.
1. Yeni satış siparişine bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *M9200*
    - **Miktar:** *5*

1. **Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *M9201*
    - **Miktar:** *1*

1. Her iki satır için stok rezerve edin.
1. Siparişi ambara serbest bırakın.

#### <a name="sales-order-3"></a>Satış siparişi 3

1. Eylem bölmesinde, satış siparişi 3'ü oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-009*
    - **Ambar:** *51*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin. Satış siparişi numarasını not edin.
1. Yeni satış siparişine bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *M9200*
    - **Miktar:** *7*

1. **Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *M9202*
    - **Miktar:** *8*

1. Her iki satır için stok rezerve edin.
1. Siparişi ambara serbest bırakın.

#### <a name="sales-order-4"></a>Satış siparişi 4

1. Eylem bölmesinde, satış siparişi 4'ü oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-010*
    - **Ambar:** *51*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin. Satış siparişi numarasını not edin.
1. Yeni satış siparişine bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *M9200*
    - **Miktar:** *25*

1. **Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *M9202*
    - **Miktar:** *10*

1. Her iki satır için stok rezerve edin.
1. Siparişi ambara serbest bırakın.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Oluşturulan iş için iş kodlarını alma

1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. Yalnızca ambar *51*'in gösterilmesi için **Ambar** alanına filtre uygulayın.
1. Dört iş kodu oluşturulması gerekir. Her satış siparişinin iş kodunu not edin.

    | Satış siparişi kodu | İş Kodu | İş miktarı |
    |---|---|---|
    | Satış Siparişi 1 | İş Kodu 1 | 20 beher |
    | Satış Siparişi 2 | İş Kodu 2 | 6 beher (her iki satırın toplamı) |
    | Satış Siparişi 3 | İş Kodu 3 | 15 beher (her iki satırın toplamı) |
    | Satış Siparişi 4 | İş Kodu 4 | 35 beher (her iki satırın toplamı) |

Akışı mobil cihazda çalıştırmadan önce, yalnızca yeni oluşturduğunuz işin ambar *51* için *Açık* durumda ve iş emri türünün *Satış siparişi* olduğundan emin olun. Aksi takdirde, sistem-doğrudan malzeme çekme işlemi tüm uygun işleri içereceği için, testin sonuçları farklılık gösterebilir.

1. **Ambar yönetimi \> İş \> Giden \> Açık satış işi**'ne gidin.
1. **Açık satış işi** kılavuzunda, yalnızca ambar *51* için işin gösterilmesi için **Ambar** alanına filtre uygulayın.
1. Yalnızca daha önce oluşturduğunuz dört iş kodunun gösterildiğini onaylayın.
1. **İş** sayfasını kapatın.

### <a name="mobile-device-flow-execution"></a>Mobil cihaz akışını yürütme

Kuruluma bağlı olarak, sistem, en yüksek iş satırı miktarından en düşük miktara sıralanan kullanıcı işini akışa alır. Her satırdaki miktar 20 beher'den az olacaktır.

Bu kurulumun, miktarın 20 beher'den az olduğu en az bir satır bulunan tüm işleri yakalayacağını unutmayın. Bu nedenle, işte miktarı tam 20 beher veya 20 beher'den fazla başka bir satır varsa, o da geçerli olur.

#### <a name="mobile-app"></a>Mobil uygulama

1. Ambar uygulamasında ambar *51*'deki bir kullanıcı olarak oturum açın.
1. **Giden \> Satış Malzeme Çekme - Sistem**'e gidin.

    İş kodu *4* için malzeme çekme adımı sunulur. Sistemin yönlendirdiği sorgu siparişinin kurulumunda işin azalan iş satırı miktarına göre sıralanacağını belirttiğiniz için ilk olarak bu iş kodu sunulur.

1. Gerekli çekme işlemini tamamlayın ve iş kodunu kapanışa sokun.

    Bunun ardından iş kodu *3* sunulur. İş satırlarından biri, iş satırı miktarına göre sırada sonraki öğe olarak yer alır.

1. Çekme işlemini tamamlayın ve iş kodunu kapanışa sokun.

    Bunun ardından iş kodu *2* sunulur. Bu çalışmanın çekme satırı sırada sonraki öğedir.

1. Çekme işlemini tamamlayın ve iş kodunu kapanışa sokun.

    Size artık başka iş sunulmaz. İş kodu *1* bu mobil cihaz menü öğesi için uygun değildir çünkü sorgu iş başlıklarının yalnızca iş satırlarındaki miktar 20 beher'den az olduğu zaman değerlendirileceğini belirtmektedir.

## <a name="tips"></a>İpuçları

Sistemin yönlendirdiği iş sırası sorguları *dahildir*. Bu olguyu bazı kurulumlar için hatırlamanız önemlidir. Örneğin, belirli bir menü öğesinin yalnızca iş biriminin *beher* olduğu işleri işlemesini istiyor ve sorgunun **Aralık** sekmesinde bu kısıtlamayı belirtiyorsunuz. Bu durumda, en az bir iş satırının iş birimi *beher* olarak ayarlandığı tüm işler çalışana sunulur. Bu nedenle, bu iş, iş birimi *beher*'den farklı (*kutu* veya *palet* vb.) iş satırları olan işler de içerebilir. Sorgu yalnızca iş birimi *beher* olan iş satırı bulunmayan işleri hariç tutacaktır.

Bu nedenle, bu senaryodaki örnekte iş kodu *4* de sorgu tarafından yakalanmıştır. Oluşturulduğu zaman iki satır eklenmiştir: biri 25 beher, diğeri 10 beher için. En az bir iş satırı 20 beher'den az miktarda olduğu için, iş yine de kullanıcıya sunulmuştur.

Senaryoya bağlı olarak, molaları kullanarak bu davranışı önleyebilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
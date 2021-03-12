---
title: Yerine koyma kümeleri
description: Yerine koyma kümeleri, aynı anda birden fazla plakayı çekmek ve daha sonra farklı yerlerde yerine koymak için bir yol sunar. Bunlar, plakaların genellikle stoğun tam paletleri olmadığı perakende işletmeler için çok yararlı olabilir.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 297792e90b3d2da0d738f5cbaa14779bc17ea3c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996210"
---
# <a name="putaway-clusters"></a>Yerine koyma kümeleri

[!include [banner](../includes/banner.md)]

Yerine koyma kümeleri, aynı anda birden fazla plakayı çekmek ve daha sonra farklı yerlerde yerine koymak için bir yol sunar. Bu işlem genellikle bir *çoklu teslimat rotası* olarak adlandırılır. Yerine koyma kümeleri, plakaların genellikle stoğun tam palet olmadığı perakende işletmeleri için çok yararlı olabilir. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Küme yerine koyma özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Küme yerine koyma özelliği*

## <a name="setup-for-the-example-scenario"></a>Örnek senaryo için kurulum

### <a name="cluster-profiles"></a>Küme profilleri

Küme yerine koyma profili, giriş sırasında maddeye atanan konuma bağlı olarak maddenin nereye gideceğini belirler. Farklı yerine koyma kümeleri gerekiyorsa her mobil cihaz menü öğesi için farklı yerine koyma kümesi oluşturulmalıdır.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Küme profilleri**'ne tıklayın.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Üst bilgi** görünümünde aşağıdaki değerleri ayarlayın:

    - **Yerine koyma kümesi profil kodu:** *Küme yerine koyma*
    - **Yerine koyma kümesi profil kodu adı:** *Küme yerine koyma*
    - **Küme türü:** *Yerine koyma*
    - **Sıra numarası:** Varsayılan değeri kabul edin.

1. Gerekli alanları **Genel** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Küme atama zamanlaması:** *Giriş sırasında*

        Bu alan, stok alındığı zaman yerine koyma kümesinin hemen mi atanacağını, yoksa daha mı sıralanıp sıralanmaması gerektiğini tanımlar.

    - **Küme atama kuralı:** *El ile*

        Bu alan, küme atamasının sistem tarafından mı, yoksa kullanıcı tarafından el ile mi belirleneceğini tanımlar.

    - **Yönerge kodu:** Boş bırakın.
    - **Yerine koyma kümesi konumu:** *Giriş*

        Aşağıdaki değerler kullanılabilir:

        - **Giriş**: Hemen giriş sırasında bir konum bulunur.
        - **Küme kapatma** Küme kapatıldığında bir konum bulunur.
        - **Kullanıcı tarafından yönlendirilir**: Plaka yerine koyma amacıyla kümeden çekildiğinde bir konum bulunur. Bu durumda, yerine koyma işi oluşturulduğunda hiçbir konum belirtilmemiştir. Yerine koyma işlemi sırasında, kullanıcı, yerine koyma adımını başlatmak için plaka veya iş kimliğini taramalıdır. Sistem daha sonra yerine koyma konumunu yeniden bulur ve kullanıcıya çekilen miktarın nereye koyulacağını bildirir.

    - **Kullanıcı bazında yerine koyma kümesi:** *Hayır*

        Bu alan, kümeler otomatik olarak atandığında her kümenin kullanıcı bazında benzersiz olup olmayacağını tanımlar. Yalnızca **Küme atama kuralı** alanı *Otomatik* olarak ayarlandığında kullanılabilir.

    - **Birim kısıtlaması:** Bu alanı boş bırakın.

        Bu alan, profilin geçerli olabilmesi için alınması gereken birimi tanımlar. Boş bırakılırsa tüm birimler geçerlidir.

    - **İş birimi kırılımı:** *Bireysel*

        Bu alan, bir küme kapatıldığında tüm stoğun tek bir plaka üzerine birleştirilip birleştirilmemesi (küme kimliği ve plaka kullanılarak) ve alınan plakalar üzerine tek bir plaka olarak mı, yoksa ayrı ayrı mı yerine konulması gerektiğini tanımlar. **Yerine koyma kümesi konumu** alanı *Giriş* olarak ayarlandığında bu alan kullanılamaz.

    - **Küme, Ana Plaka olarak devam eder:** *Hayır*

        Bu seçenek *Evet* olarak ayarlanırsa yerine koyma adımı tamamlandığında küme kimliği bir üst plaka olur ve küme kimliğindeki tüm maddeler bu üst plakaya bağlanır.

1. **Küme sıralaması** hızlı sekmesinde, yerine koyma sıralama ölçütleri tanımlayabilirsiniz. Araç çubuğundaki **Yeni**'yi seçerek bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** Varsayılan değeri kabul edin.
    - **Alan adı:** *WMSLocationId*

        Bu alan, bu satırın sıralama ölçütü olarak kullanacağı alanı belirler.

    - **Sıralama:** *Artan*

        Bu alan, sıralamanın artan veya azalan sırada olacağını tanımlar.

1. **Küme işi şablonu** hızlı sekmesinde, satır eklemek için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **İş emri türü:** *Satın alma siparişleri*
    - **İş şablonu:** *61 SAS Doğrudan*

1. Eylem Bölmesinde, **Kaydet**'i ve sonra **Sorguyu düzenle**'yi seçin.
1. **Küme yerine koyma** iletişim kutusundaki **Aralık** sekmesinde **Ekle**'yi seçerek sorguya ikinci bir satır ekleyin: Ardından, aşağıdaki tabloda gösterildiği gibi sorgu satırlarını güncelleştirin.

    | Tablo | Türetilen tablo | Alan | Ölçütler |
    |---|---|---|---|
    | Work | Work | Ambar | *61* |
    | Work | Work | İş Kodu | Bu alanı boş bırakın. |

1. Sorguyu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. Eylem Bölmesi'nde **Kaydet**'i seçin ve ardından sayfayı kapatın.

> [!IMPORTANT]
> **Küme kimliği oluştur**, *Evet* olarak ayarlandığında soluk görünen küme profilindeki alanlar kullanılamaz ve bu özellik kullanıldığında dikkate alınmaz.

### <a name="mobile-device-menu-items"></a>Mobil cihaz menü öğeleri

Bu özellik için iki yeni mobil cihaz menü öğesi mevcuttur. Alınan stoğu, girişin ardından yerine koyma kümesine sıralamak için **Al ve kümeyi sırala** menü öğesi kullanılır. **Küme yerine koyma** menü öğesi, küme atandıktan sonra yerine koymak için kullanılır.

#### <a name="receive-and-sort-cluster"></a>Al ve kümeyi sırala

Stok almak ve kümeye sıralamak için yeni bir mobil cihaz menü öğesi oluşturun. Bu menü öğesi, stok alındıktan sonra bir gelen iş oluşturur ve bu da alıcı menü öğesinin yerine koyma kümeleri için kullanılacağını gösterir.

> [!NOTE]
> **Al ve kümeyi sırala** menü öğesi aşağıdaki alıcı menü öğeleriyle kullanılabilir:
>
> - Satınalma siparişi satırı teslim alma
> - Satınalma siparişi madde teslim alma
> - Yük maddesi teslim alma

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Üst bilgi** görünümünde aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Al ve kümeyi sırala*
    - **Başlık:** *Al ve kümeyi sırala*
    - **Mod:** *İş*
    - **Varolan çalışmayı kullan:** *Hayır*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **İş oluşturma işlemi:** *Satın alma siparişi madde teslim alma*
    - **Plaka oluştur:** *Evet*
    - **Yerine koyma kümesini ata:** *Evet*

        > [!NOTE]
        > **Yerine koyma kümesi ata** seçeneği teslim alma açısından yalnızca tek adımlı *İş oluşturma işlemi* etkinliği için kullanılabilir.

    Kalan alanlar için varsayılan değerleri kabul edin.

1. Eylem bölmesinde, **Kaydet**'i seçin.

#### <a name="cluster-putaway"></a>Küme yerine koyma

Küme atandıktan sonra kümeyi yerine koymak için yeni bir mobil cihaz menü öğesi oluşturun.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Üst bilgi** görünümünde aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Küme yerine koyma*
    - **Başlık:** *Küme yerine koyma*
    - **Mod:** *İş*
    - **Mevcut işi kullan:** *Evet*

1. **Genel** hızlı sekmesinde **Yöneten** alanı *Küme yerine koyma* olarak ayarlanmalıdır. Kalan alanlar için varsayılan değerleri kabul edin.
1. **İş sınıfları** hızlı sekmesinde, mobil cihaz menü öğesi için geçerli iş sınıfını ayarlayın:

    - **İş sınıfı kodu:** *Purchase*
    - **İş emri türü:** *Satın alma siparişleri*

1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="mobile-device-menu"></a>Mobil cihaz menüsü

Yeni oluşturduğunuz menü öğelerini mobil uygulamanın gelen menüsüne ekleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. Menü listesinde **Gelen**'i seçin.
1. **Mevcut menüler ve menü öğeleri** listesinde, **Kümeyi teslim al ve sırala**'yı bulup seçin.
1. Seçilen menü öğesini **Menü yapısı** listesine taşımak için sağ ok düğmesini seçin.
1. Menü öğesini menüde istenen konuma taşımak için yukarı ok ve aşağı ok düğmelerini kullanın.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Kalan menü öğelerini eklemek için 4 ile 7. adımlar arasındaki işlemleri tekrarlayın.

    - Küme atama
    - Küme yerine koyma

## <a name="example-scenario"></a>Örnek senaryo

Bu senaryo, küme küme yerine koymayı işlemeyi simüle eder.

### <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

1. **Borç hesapları \> Satın alma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Satıcı hesabı:** *1001*
    - **Ambar:** *61*

1. **Tamam**'ı seçin.

    **Tüm satın alma siparişleri** sayfası görüntülenir.

1. **Tüm satın alma siparişleri** sayfasında, **Satın alma siparişi satırları** hızlı sekmesinde aşağıdaki satırları eklemek için **Satır ekle**'yi kullanın:

    - Satın alma siparişi satırı 1:

        - **Madde numarası:** *A0001*
        - **Miktar:** *10*

    - Satın alma siparişi satırı 2:

        - **Madde numarası:** *A0002*
        - **Miktar:** *20*

    - Satın alma siparişi satırı 3:

        - **Madde numarası:** *M9215*
        - **Miktar:** *30*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Satın alma siparişi numarasını not edin.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Mobil cihazdan stoğu teslim alma ve yerine koyma

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Stoğu bir kümeye teslim alma ve sıralama

1. Ambar *61* için ayarlanan bir kullanıcı olarak ambarı uygulamasına oturum açın.
1. Ana menüde **Gelen**'i seçin.
1. **Gelen** menüsünde **Teslim al ve kümeyi sırala**'yı seçin.
1. **SAS No** alanına satın alma siparişi numaranızı girin.
1. **Tamam**'ı (onay işareti düğmesi) seçin.
1. **Madde** alanını seçin, *A0001* madde numarasını girin ve ardından **Tamam**'ı seçin.
1. **Miktar** alanını seçin, sayısal tuş takımını kullanarak *10* girin ve ardından onay işareti düğmesini seçin.
1. **Miktar** görev sayfasında, girdiğiniz miktarı onaylamak için **Tamam**'ı (onay işareti düğmesi) seçin.
1. **Madde** görev sayfasında, *A0001* maddesinin girildiğini onaylamak için **Tamam**'ı seçin.
1. **Küme Kimliği** alanını seçin ve oluşturmakta olduğunuz küme için kimlik atamak üzere bir değer girin.

    Buraya girdiğiniz kimlik, satın alma siparişinde kalan iki madde teslim alındığı zaman kullanılacaktır.

1. **Tamam**'ı seçin.

    **SAS numarası** görev sayfası görüntülenir ve "İş tamamlandı" iletisini gösterir.

    *A0001* maddesi artık *RECV* konumuna alınmıştır ve adım 10'da girdiğiniz küme kimliğine atanmıştır.

1. Satın alma siparişindeki kalan iki maddeyi teslim almak ve küme kimliğine atamak için 4 ile 11 arası adımları yineleyin:

    - *A0002* maddesi için *20* miktar
    - *M9215* maddesi için *30* miktar

#### <a name="close-the-cluster"></a>Kümeyi kapatma

Kümedeki maddelerin kaldırılabilmeleri için kümenin kapatılması gerekir.

1. Supply Chain Management'ta, **Ambar yönetimi \> İş \> Giden İş \> İş kümeleri**'ne gidin.
1. **İş kümeleri** sayfasında, **İş kümesi** bölümünde, daha önce girdiğiniz küme kimliği için **Küme Kimliği** alanında arama yapın.
1. Küme gösterilmezse, zaten kapatılmış olabilir. Kümenin kapalı olup olmadığını belirlemek için **Kapalı işleri göster** onay kutusunu seçin ve daha önce girdiğiniz küme kimliğini arayın. Ardından şu adımlardan birini izleyin:

    - Küme kapatıldıysa, bu prosedürün kalan adımlarını atlayın ve bir sonraki prosedüre geçin: [Kümeyi yerine koyma](#put-the-cluster-away).
    - Küme kapatılmadıysa kümeyi el ile kapatmak için bu prosedürün kalan adımlarını izleyin. Ardından sonraki prosedüre geçin.

1. **İş kümesi** bölümünde, daha önce girdiğiniz küme kimliğini seçin.
1. Eylem Bölmesinde **Kümeyi kapat**'ı seçin.

    Küme kapatıldıktan sonra, artık **İş kümesi** bölümünde gösterilmez (**Kapalı işleri göster** onay kutusu seçili değilse).

#### <a name="put-the-cluster-away"></a>Kümeyi yerine koyma

1. Ambar *61* için ayarlanan bir kullanıcı olarak ambarı uygulamasına oturum açın.
1. Ana menüde **Gelen**'i seçin.
1. **Gelen** menüsünden **Küme yerine koyma**'yı seçin.
1. **Küme Kimliği**'ni seçin ve kapalı küme için daha önce girdiğiniz küme kimliğini girin.
1. **Tamam**'ı seçin.

    **Küme yerine koyma: Malzeme çekme** sayfası görüntülenir. Küme kimliğini, malzeme çekme konumunu, maddeleri (*Çoklu* değeri gösterilecek) ve kümedeki çekilmesi gereken toplam miktarı gösterir.

1. **Tamam**'ı seçin.

    **Küme yerine koyma: Yerine koy** sayfası görüntülenir. **Yerine koy** yönergeleri küme kimliğini, yerine koyma konumunu, maddeleri, toplam miktarı ve kümede teslim alınan maddelerin plaka kimliklerini tanımlar.

    Bu adımı geçersiz kılmak veya atlamak için standart seçeneklere sahipsiniz.

    ![Küme yerine koyma: Sayfayı yerine koyma](media/Cluster_putaway-Put.png "Küme yerine koyma: Sayfayı yerine koyma")

1. Kümenin yerine konmasını onaylamak için **Tamam**'ı seçin.

    "Küme tamamlandı" iletisi gösterilir.

## <a name="notes-and-tips"></a>Notlar ve ipuçları

Küme kimliğinin iç içe geçmiş palet için üst plaka olduğu durumlarda, küme kimliği tarandığında yerine koyma konumu otomatik olarak verilir. Plaka üretimi el ile olarak ayarlansa bile başka bir plaka taranmamalıdır.

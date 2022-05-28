---
title: Satış siparişleri ve transfer emirleri için fazla malzeme çekme
description: Bu konuda, satış siparişleri ve transfer emirleri için fazla malzeme çekmenin nasıl etkinleştirileceği açıklanmaktadır.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 52a4225efa88a7b9303dd611d5652f59da1612a4
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678422"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Satış siparişleri ve transfer emirleri için fazla malzeme çekme

[!include [banner](../includes/banner.md)]

Bu konuda, belirli bir çalışanın veya tüm çalışanların fazla malzeme çekmeyi nasıl etkinleştirileceğini gösteren bir senaryo sunulmaktadır. Fazla malzeme çekme işlemi, malzeme çekme işi sırasında denetimli fazla malzeme çekmeye olanak sağlar.

Ambara fazla malzeme çekme, basit bir kavramdır. Sistem, çalışanların sipariş için belirtilenden daha fazla malzeme çekmesine olanak tanır. Ancak transfer emri veya satış siparişi için satır düzeyinde ayarlanan fazla teslimat sınırı yine de dikkate alınır. Bu sınır aşılırsa Warehouse Management uygulaması, çalışanlara fazla teslimat sınırını aştıklarını bildirir.

Fazla malzeme çekme özelliği, bakımın en aza indirilmesine ve ayrıca kurulumunuzun esnek kalmasına yardımcı olur. Bir veya daha fazla mobil cihaz menü öğesi tanımlayabilir ve bunlardan bazıları için fazla malzeme çekmeyi etkinleştirebilirsiniz. Ayrıca menü öğelerini değiştirmeye gerek kalmadan, seçili çalışanların satış siparişleri ve/veya transfer emirleri için fazla malzeme çekmesini de engelleyebilirsiniz. Bunun yerine, ilgili çalışan kurulumlarında bu özelliklerin birini veya ikisini birden kapatabilirsiniz.

Fazla malzeme çekme özelliği, çalışanların malzemeleri çektiklerinde ve sevk ettiklerinde zaman ve çabadan tasarruf etmesine yardımcı olabilir. Örneğin, bu özellik çalışanların şu görevleri gerçekleştirmesine olanak tanır:

- Malzeme çekme veya sevkiyat sırasında fireyi dengeler.
- Malzeme çekme işlemi sırasında bazı ambalaj malzemelerini açmak zorunda kalmamanızı sağlar.
- Taşıma sırasında madde hasarını dengeler.
- Farklı miktar veya ölçü birimleri sevk etmenizi sağlar.
- Plakalarda miktarların bozulmasını en aza indirir.
- Artık malzemeden ve pahalı malzeme azlığını önlemenizi sağlar.
- Malzeme çekme işleminden sonra çekilen miktarı ölçmenizi sağlar (örneğin, kamyon ağırlığı yoluyla).

> [!IMPORTANT]
> Fazla malzeme çekme özelliği yalnızca satış siparişi ve transfer emrinde malzeme çekme ve işleme için geçerlidir. Stok yenileme, fazla malzeme çekmeyi desteklemez. Stok yenileme işi çalıştırıldığında sistem, kullanıcıların fazla malzeme çekmesine izin vermez.

Bu konudaki bu senaryoda, fazla malzeme çekme özelliğinin nasıl ayarlanacağı ve kullanılacağı gösterilmektedir.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Senaryo önkoşulu: Tanıtım verilerini kullanılabilir hale getirme

Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği *USMF* olarak ayarladığınızdan emin olun.

## <a name="scenario-setup"></a>Senaryo kurulumu

Örnek senaryo üzerinden çalışmadan önce ilgili çalışan ve ilgili menü öğesi için fazla malzeme çekme özelliğini etkinleştirmeniz gerekir.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Çalışanı fazla malzeme çekmesine izin verecek şekilde ayarlama

Burada, ayrı ayrı satış siparişleri ve transfer emirleri için fazla malzeme çekmeyi etkinleştirmek üzere bir çalışanı yapılandırma ile ilgili genel yordam bulunmaktadır. Bu yapılandırmada, malzemeyi çeken hangi çalışanının fazla malzeme çekme işlemi yapabileceği ve bu çalışanın hem transfer emirleri hem satış siparişleri için fazla malzeme çekme işlemi yapıp yapamayacağı denetlenir.

1. **Ambar yönetimi \> Kurulum \> Çalışan**'a gidin.
1. Liste bölmesinde, **Julia Funderburk**'u seçin.
1. **Kullanıcılar** hızlı sekmesinde, aşağıdaki değerlere sahip satırı seçin. Bu değerleri içeren mevcut satır yoksa, oluşturun.

    - **Kullanıcı kimliği:** *24*
    - **Kullanıcı adı:** *WH 24*
    - **Varsayılan ambar:** *24*
    - **Menü adı:** *Ana*

1. **İş** hızlı sekmesinde, önceden ayarlanmamışsa Kullanıcı *24* için aşağıdaki değerleri ayarlayın:

    - **Satışta fazla malzeme çekmeye izin ver:** *Evet*
    - **Transfer emrinde fazla malzeme çekmeye izin ver:** *Evet*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Fazla malzeme çekmeye izin vermek için bir mobil cihaz menü öğesi ayarlama

Burada, fazla malzeme çekmeyi etkinleştirmek için bir mobil cihaz menü öğesini yapılandırma ile ilgili genel yordam bulunmaktadır. Mobil cihaz menüsünü kullanacak çalışanın izin düzeyi için iş gereksinimlerinize bağlı olarak, bazı parametreler açılabilir ya da kapatılabilir.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Liste bölmesinde, *Satış Çekme* adlı kaydı seçin. Bu ada sahip bir kayıt yoksa, oluşturun. Kayıt için aşağıdaki değerleri onaylayın veya ayarlayın:

    - **Menü öğesi adı:** *Satış Çekme*
    - **Başlık:** *Satış Çekme*
    - **Mod:** *İş*
    - **Mevcut işi kullan:** *Evet*
    - **Yöneten:** *Kullanıcı tarafından yönetilen*
    - **Hedef plakayı geçersiz kıl:** *Evet*
    - **Yerine koyma sırasında plakayı geçersiz kıl:** *Evet*
    - **Kullanıcı tarafından kilitlenen işi koru:** *Evet*
    - **Fazla malzeme çekmeye izin ver:** *Evet*

> [!IMPORTANT]
> Çalışan ve mobil cihaz menü öğesi için ilgili parametreler etkinleştirildikten sonra fazla malzeme çekme yalnızca mobil cihaz üzerinden işlenebilir.

## <a name="example-scenario"></a>Örnek senaryo

Önkoşullar, çalışan kurulumu ve menü öğesi kurulumu gerçekleştikten sonra bu özellik ile çalışmaya hazır olursunuz.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Fazla teslimata izin veren satış siparişi oluşturma

1. **Satış ve Pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Yeni bir satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *24*

1. **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Madde numarası:** *A0001*
    - **Miktar:** *10*

1. **Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesinde, **Fazla teslimat** alanını *10* olarak ayarlayın.
1. **Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.
1. **Rezervasyon** sayfasını kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

Serbest bırakma işlemi tamamlanınca oluşturulan dalga kimliğini ve yük kimliklerini gösteren bilgi iletileri alırsınız.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Yeni sipariş için iş kodunu ve plaka numarasını alma

Satış siparişini ambara serbest bıraktığınızda sistemde tek bir çekme satırı içeren yeni bir iş kodu oluşturulması gerekir. İş kodunu ve plaka atamasını bulmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. **Genel Bakış** ızgarasında, az önce oluşturduğunuz satış siparişi için **Sipariş numarası** sütununu arayın. Bu satış siparişi için karşılık gelen iş kodunu not edin.
1. **Satırlar** ızgarasında ilgili bilgileri göstermek için yeni satış siparişinin satırını seçin. Malzemenin hangi konumdan çekileceğini not edin.
1. **Stok yönetimi \> Sorgular ve raporlar \>> Eldeki stok** öğesine gidin.
1. Eylem Bölmesinde **Boyutlar** öğesini seçin.
1. **Boyut görünümü** iletişim kutusunda **Plaka**, **Ambar** ve **Madde numarası** onay kutularının işaretlendiğinden emin olun ve ardından **Tamam**'ı seçin.
1. **Filtre** bölmesinde, aşağıdaki filtreleri ayarlayın:

    - **Madde numarası** – **biri** – *A0001*
    - **Ambar** – **ile başlar** - *24*

1. **Uygula**'yı seçin.
1. Gösterilen **Plaka numarası** değerlerini not edin.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulamasını kullanarak siparişte fazla malzeme çekme

1. Ambar *24*'de bir kullanıcı olarak Ambar Yönetimi mobil uygulamasına oturum açın.
1. **Giden \> Satış çekme**'ye gidin.
1. **İş kodunu veya plakayı tara** alanında, satış siparişi için oluşturulan iş kodunu girin.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. **Fazla malzeme çekme**'yi seçin.
1. **Çekme Miktarı** alanını *14* olarak ayarlayın.
1. **Tamam**'ı (onay işareti simgesi) seçin.

    **Fazla malzeme çekme** sayfasında, şu iletiyi alırsınız: "Satırın fazla teslimat yüzdesi 40 ancak izin verilen fazla teslimat yüzdesi 10." Bu ileti, girdiğiniz çekme miktarının fazla teslimat sınırını aştığını belirtir. Satış siparişi satırı için fazla teslimat sınırı yüzde 10'dur. Bu nedenle, belirtilen 10 miktarı için toplam 11 çekme miktarında yalnızca 1 fazla malzeme çekebilirsiniz.

1. **Çekme Miktarı** alanını *11* olarak ayarlayın.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. **Plaka** alanında, önceki bölümde not ettiğiniz plakayı girin.
1. **Hedef plaka** alanında bir hedef plaka girin. Çekme konumu (*FLOOR-001*), malzeme (*A0001*) ve miktarın (*11 adet*) gösterildiğine dikkat edin.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. **Satış siparişleri: Yerine koyma** sayfası hakkındaki bilgileri inceleyin. **Konum** alanı, çekilen malzemelerin *BAYDOOR* konumuna gittiğini göstermelidir.
1. **Tamam**'ı (onay işareti simgesi) seçin.

**İş kodu/plaka kodu tara** sayfasında "İş Tamamlandı" iletisi alırsınız. Bu ileti, satış siparişinin iş kodunun tamamlandığını ve fazla çekilen miktarın yüzde 10'luk fazla teslimat sınırını aşmadığını belirtir.

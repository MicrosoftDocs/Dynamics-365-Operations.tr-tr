---
title: Dalga oluşturma ve işleme
description: Bu konu, bir yükleme, Sevkiyat, üretim emri veya Kanban siparişi için malzeme çekme işi oluşturmak amacıyla bir dalga oluşturma, işleme ve serbest bırakma yöntemini açıklamaktadır.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 349285f089ecab00c4c1c0a0315c4223314e3e79
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687518"
---
# <a name="wave-creation-and-processing"></a>Dalga oluşturma ve işleme

[!include [banner](../includes/banner.md)]

Bu konu, bir yükleme, Sevkiyat, üretim emri veya Kanban siparişi için malzeme çekme işi oluşturmak amacıyla bir dalga oluşturma, işleme ve serbest bırakma yöntemini açıklamaktadır. Aşağıdaki sipariş türleri için dalga oluşturabilirsiniz:

- **Satış siparişleri**: Satış siparişlerinden satırları dahil etmek için sevkiyat dalgasını kullanın. Bir satış siparişi ambara serbest bırakıldığında, satış siparişi satırları dalgaya dahil edilebilir.
- **Üretim emirleri**: Bir ürünün ürün reçetesinden (BOM) satırlarını dahil etmek için üretim dalgalarını kullanın.
- **Kanban siparişleri**: Kanban dalgaları, Kanban siparişlerinden malzeme çekme listesi satırları içerir.

Satış siparişleri ve kanban siparişleri için, sipariş için ambarda serbest bırakılmadan önce stok ayrılmalıdır. Aksi halde, maddeler veya tahsisat satırları dalga içerisinde işlenemez. Ancak, üretim emirleri biraz daha esnektir. Üretim emirleri için, aşağıdaki seçeneklerden birini belirleyebilirsiniz:

- Bir sipariş ambara serbest bırakılmadan önce tüm malzemelerin rezerve edilmesi gerekir.
- Tüm malzemeler rezerve edilmese de üretim emirlerinin ambara serbest bırakılması için izin verin. Bu seçeneği belirlerseniz, ek malzemeler kullanılabilir duruma geldiğinde, ambara serbest bırak işlemini el ile tekrar etmeniz gerekir. Örneğin, üretimi başlatmak için gereken malzemeler varsa ve ek malzemelerin kullanılabilir olmasını bekleyebiliyorsanız bu seçenek kullanışlıdır.

**Üretim Denetim parametreleri** sayfasındaki **malzeme rezervasyonu gereksinimi** alanını kullanarak bu üretim emri seçeneklerinden hangisinin varsayılan olarak kullanılacağını belirtebilirsiniz. Ancak, her belirli üretim emrinin ayarını gerektiği gibi değiştirebilirsiniz. Daha fazla bilgi için bkz. [Dalga işleme için depo parametreleri](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Dalga oluşturma ve işleme

Aşağıdaki diyagramda, Sevkiyat dalgaları oluşturma, işleme ve serbest bırakma akışı gösterilmektedir. Sayılar, bu bölümün ilerleyen bölümlerine karşılık gelir.

![Dalga oluşturma işlemi.](media/wave-processing-diagram.png "Dalga oluşturma işlemi")

### <a name="prerequisites"></a>Önkoşullar

Başlamadan önce oluşturmak istediğiniz dalga türü (sevkiyat, üretim veya Kanban) için bir dalga şablonu bulunmalıdır. Dalga şablonu, hangi adımların elle hangilerinin otomatik olarak gerçekleştirilmesi gerektiği de dahil olmak üzere, dalganın nasıl oluşturulacağı ve işleneceği ile ilgili birçok ayar oluşturur. Daha fazla bilgi için bkz. [Dalga şablonları](wave-templates.md).

### <a name="create-a-wave"></a>Dalga oluştur

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Otomatik olarak ambar ve sipariş türüne dayalı dalgalar oluşturma

Dalgaları otomatik olarak oluşturmak için, her ilgili sipariş türü ve ambar için geçerli olan [dalga şablonları](wave-templates.md) ayarlayın. Her şablonda, **Dalga oluşturmayı otomatik hale getir** seçeneğinin *Evet* olarak ayarlanmış olduğundan emin olun.

#### <a name="manually-create-waves"></a>Dalgaları el ile oluşturma

Elle dalga oluşturmak için şu adımları izleyin:

1. İlgili [dalga şablonlarının](wave-templates.md) ambar ve el ile yapmak istediğiniz sipariş türleri için otomatik olarak bir dalga oluşturacak şekilde ayarlanmadığından emin olun.
1. Oluşturmak istediğiniz dalganın türüne bağlı olarak şunlardan birini yapın:

    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Sevkiyat dalgaları** \> **Tüm dalgalar**'a gidin. Eylem bölmesinde, **Dalga**'yı seçin.
    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Üretim dalgaları** \> **Tüm üretim dalgaları**'na gidin. Eylem bölmesinde, **Üretim Dalgası**'nı seçin.
    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Kanban dalgaları** \> **Tüm kanban dalgaları**'na gidin. Eylem bölmesinde, **Dalga Oluştur**'u seçin.

1. **Açıklama** alanına dalga için kısa bir açıklama girin. Bu, dalga içinde işlediklerinizi belirtmelidir.

1. **Dalga şablonu adı** alanında, oluşturulacak dalga türü için dalga şablonunu seçin. Dalga şablonu, dalga için iş oluşturma gibi eylemleri gerçekleştirecek dalga yöntemlerini içerir. Örneğin, sevkiyat dalgasının dalga şablonu, yük oluşturma, dalgalara satır tahsis etme, stok yenileme ve dalga için malzeme çekme işi oluşturma yöntemleri içerebilir.

1. Dalga için ek sorgu ölçütleri olarak dalga niteliklerini kullanmak istiyorsanız, **dalga öznitelikleri** alanlarında öznitelikleri seçin.

### <a name="specify-what-to-include-in-a-wave"></a>Dalgaya nelerin dahil edileceğini belirtme

Dalga oluşturulduktan sonra dalgaya içerik eklemeye başlamaya hazırsınız.

> [!NOTE]
> Gerekirse, bir dalgaya serbest bırakılmadığı sürece işlendikten sonra da satır ekleyebilirsiniz.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Dalgaya nelerin dahil edileceğini otomatik olarak belirtme

Dalgaları otomatik olarak oluşturmak için, her ilgili sipariş türü ve ambar için geçerli olan [dalga şablonları](wave-templates.md) ayarlayın. Her şablonda, **Dalga oluşturmayı otomatik hale getir** seçeneğinin *Evet* olarak ayarlanmış olduğundan emin olun. Alternatif olarak, **Açık dalgalara ata** ata seçeneği *Evet* olarak ayarlanmışsa, şablonunuz herhangi bir nitelikli açık dalgaya otomatik olarak satırlar atayabilir.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Dalgaya nelerin dahil edileceğini elle belirtme

Bir dalga oluşturulduğunda, ancak henüz serbest bırakılmadığında el ile ne dahil edileceğinizi belirtebilirsiniz. Dalgaya el ile satır eklemek için:

1. Satır eklemek istediğiniz dalganın türüne bağlı olarak şunlardan birini yapın:

    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Sevkiyat dalgaları** \> **Tüm dalgalar**'a gidin. Eylem bölmesinde, **Dalga**'yı seçin.
    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Üretim dalgaları** \> **Tüm üretim dalgaları**'na gidin. Eylem bölmesinde, **Üretim Dalgası**'nı seçin.
    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Kanban dalgaları** \> **Tüm kanban dalgaları**'na gidin. Eylem bölmesinde, **Dalga Oluştur**'u seçin.

1. Dalga seçin. Eylem bölmesinde aşağıdakilerden birini seçin:

      - **Sevkiyatları koru**
      - **Üretimleri koru**
      - **Kanban işi malzeme çekme listelerini koru**

1. Pencerenin üst bölümünde, dalgaya eklenecek satırı seçin ve daha sonra **dalgaya Ekle**'yi seçin. Satır, **dalga satırları** hızlı sekmesi'ne taşınacaktır.

    Eklenecek her satır için bu adımı yineleyin. Tüm satırları eklemek için, **Tümünü Ekle**'yi seçin.

    > [!TIP]
    > Sevkiyat dalgaları için, **dalga filtresi kodu** alanında özel bir filtre seçerek hızlı şekilde belirli bir sipariş bulabilirsiniz. Dalga filtresi kodları, **dalga filtreleri** formunda oluşturulan sevkiyatların Sorgu ölçütlerini içerir. Bu alan, üretim dalgaları veya Kanban dalgaları için kullanılamaz.
    > **Dalga üzerinde** sütununda yeşil onay işareti varsa, sevkiyatın dalgaya eklendiğini gösterir.

### <a name="process-the-wave-to-create-the-picking-work"></a>Malzeme çekme işini oluşturmak için dalga işlemini işleme

Bir dalga oluşturulduktan ve gerekli satırlarının tümünü içerdikten sonra, ilgili malzeme çekme işini oluşturmak için dalgayı işlemeye hazırsınız demektir.

#### <a name="automatically-process-a-wave"></a>Dalgayı Otomatik olarak işleme

Bir dalgayı otomatik olarak işlemek için, ilgili [dalga şablonları](wave-templates.md) gereken otomatik işleme seçenekleriyle ayarlayın.

#### <a name="manually-process-a-wave"></a>Dalgayı el ile işleme

Bir dalga yalnızca, **dalga durumu** *Oluşturuldu* olduğunda işlenebilir. Bir dalgayı işledikten sonra, **dalga durumu**, *tutuluyor* olarak değiştirilecektir.

Tüm gerekli içeriği olan bir dalga öğesini el ile işlemek için şu adımları izleyin:

1. İşleyeceğiniz dalganın türüne bağlı olarak şunlardan birini yapın:

    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Sevkiyat dalgaları** \> **Tüm dalgalar**'ı seçin. Eylem bölmesinde, **Dalga**'yı seçin.
    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Üretim dalgaları** \> **Tüm üretim dalgaları**'nı seçin. Eylem bölmesinde, **Üretim Dalgası**'nı seçin.
    - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Kanban dalgaları** \> **Tüm kanban dalgaları**'nı seçin. Eylem bölmesinde, **Dalga Oluştur**'u seçin.

1. İşlenecek dalgayı seçin. Eylem Bölmesinde, **İşlem**'i seçin.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Malzeme çekme ve paketleme başlatmak için dalgayı ambara serbest bırakma

Bir dalgayı serbest bırakmadan önce işlemeniz gerekir. Dalgayı serbest bıraktığınızda malzeme çekme işi ambarda kullanılabilir. Bir dalgayı serbest bıraktıktan sonra iptal edebilir ve daha fazla satır ekleyebilirsiniz, ancak satırları değiştiremezsiniz.

#### <a name="automatically-release-a-wave"></a>Dalgayı Otomatik olarak serbest bırakma

Bir dalgayı otomatik olarak işlemek için, ilgili [dalga şablonları](wave-templates.md) gereken otomatik işleme seçenekleriyle ayarlayın.

#### <a name="manually-release-a-wave"></a>Dalgayı el ile serbest bırakma

Dalgayı elle serbest bırakmak için şu adımları izleyin:

1. Serbest bırakacağınız dalganın türüne bağlı olarak şunlardan birini yapın:

      - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Sevkiyat dalgaları** \> **Tüm dalgalar**'ı seçin. Eylem bölmesinde, **Dalga**'yı seçin.
      - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Üretim dalgaları** \> **Tüm üretim dalgaları**'nı seçin. Eylem bölmesinde, **Üretim Dalgası**'nı seçin.
      - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Kanban dalgaları** \> **Tüm kanban dalgaları**'nı seçin. Eylem bölmesinde, **Dalga Oluştur**'u seçin.

1. Serbest bırakılacak dalgayı seçin. Eylem bölmesinde, **Dalgayı Serbest bırak**'ı seçin.

## <a name="containerize-a-wave"></a>Bir dalgayı kapsayıcılı hale getirme

Bir dalga işlendiğinde otomatik kapsayıcı hale getirme işlemi, kapsayıcılar ve sevkiyatlara malzeme çekme çalışması oluşturur. Bunu nasıl ayarlayacağınızı öğrenmek için [Kapsayıcı hale getirme](wave-containerization.md) bölümüne bakın.

## <a name="work-with-the-scheduled-work-creation"></a>Planlanan iş oluşturma ile çalışma

*İş oluşturmayı zamanla* işlevi etkinleştirildiğinde dalga işleme, planlı iş oluşturacaktır. Bu da daha sonra yeni iş oluşturma işlemi tarafından kullanılacaktır. İş oluşturma sırasında iş, *Kuruluş genelinde iş engelleme* özelliği kullanılarak engellenir. Daha fazla bilgi için bkz. [Dalga sırasında iş oluşturmayı zamanlama](configure-wave-schedule-work-creation.md).

Aşağıdaki akış çizelgesi, dalga işleme sırasında planlanan işin nasıl oluşturulduğunu gösterir.

![Planlama işi oluşturma.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Planlı iş

**Planlı iş ayrıntıları** sayfası (**Ambar yönetimi \> İş \> Planlı iş ayrıntıları**), dalga işleme sırasında oluşturulan planlı iş hakkında bilgiler gösterir. Aşağıdaki **İşleme durumu** değerleri mevcuttur:

- **Sıraya Alındı**: Planlanan iş, iş oluşturmak için kullanılmak üzere bekliyor.
- **Tamamlandı**: Planlanan iş, iş oluşturmak için kullanıldı.
- **Başarısız**: Dalga işleme başarısız oldu. Planlı işin, ilgili gerçek iş olup olmadığına bakılmaksızın **Başarısız** durumunda olabileceğini unutmayın. Asıl iş oluşturma işlemi başarısız olduğunda asıl iş, *İptal edildi* durumunda kalır.

### <a name="batch-job-for-the-work-creation-process"></a>İş oluşturma işlemi için toplu iş

Dalgaları işlemeye yönelik toplu işleri görüntülemek için **Tüm dalgalar** sayfasındaki Eylem Bölmesinde **Toplu işler**'i seçin.

Buradan, toplu iş kodlarının her biri için tüm toplu görev ayrıntılarını görüntüleyebilirsiniz.

## <a name="cancel-a-wave"></a>Dalga iptal etme

Gerekirse, işlenmiş bir dalgayı iptal edebilirsiniz. Oluşturulan bir dalga ve malzeme çekme işini iptal etmek için şu adımları izleyin:

1. İptal edeceğiniz dalganın türüne bağlı olarak şunlardan birini yapın:

      - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Sevkiyat dalgaları** \> **Tüm dalgalar**'a gidin.
      - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Üretim dalgaları** \> **Tüm üretim dalgaları**'na gidin.
      - **Ambar yönetimi** \> **Ortak** \> **Dalgalar** \> **Kanban dalgaları** \> **Tüm kanban dalgaları**'na gidin.

1. İptal edilecek dalgayı seçin. Eylem Bölmesindeki **İş** sekmesinde, **İptal**'i seçin.

## <a name="review-wave-batch-job-details"></a>Dalga toplu iş ayrıntılarını gözden geçirme

Bir dalgaya ilişkin toplu işleri ve ilgili görevleri denetlemek için **dalga toplu iş ayrıntıları** sayfasını kullanın. Bu, özellikle başarısız olan bir dalgadaki sorunu gidermek için kullanışlıdır. Bu özellik olmadan, yalnızca Yöneticiler toplu iş ayrıntılarına erişebilir. **Dalga toplu iş ayrıntıları** sayfası yönetici olmayan kullanıcılar tarafından kullanılabilir hale getirilebilir ve toplu işlerin ve ilgili görevlerin salt okunur bir görünümünü sağlar.

### <a name="turn-the-wave-batch-job-details-page-on-or-off"></a>Dalga toplu iş ayrıntıları sayfasını açma veya kapatma

Supply Chain Management sürüm 10.0.25 itibarıyla **Dalga toplu iş ayrıntıları** özelliği varsayılan olarak açıktır. Yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Dalga toplu iş ayrıntıları* özelliğini bularak bu işlevi açabilir veya kapatabilir.

### <a name="use-the-wave-batch-job-details-page"></a>Dalga toplu iş ayrıntıları sayfasını kullanma

**Dalga toplu iş ayrıntıları** sayfası toplu işleri ve toplu iş görevlerini birleştirerek, tek bir toplu işle toplu iş görevleri listesi arasında gidip gelmenize gerek kalmadan tüm dalga adımlarını araştırmanıza olanak tanır. Sayfa aynı zamanda toplu iş günlüğüne erişim sağlar ve gerekli izinleriniz varsa, **toplu işler** sayfasına bir bağlantı sağlar.

Bu sayfayı açmak için, birkaç farklı dalga sayfasından bir dalga seçin ve sonra eylem bölmesinden **dalga toplu iş ayrıntılarını** seçin.

## <a name="review-load-validation-and-error-messages"></a>Yük Doğrulama ve hata iletilerini inceleme

Dalga işleme sırasında, sistem, dalga içindeki her yükleme satırının durumunu onaylar ve görüntüler. Hiçbir uyarı oluşmazsa, sonraki dalga adımıyla devam eder. Uyarılar oluşursa, bunun yerine tüm dalgayı doğrulamayı bitirdikten sonra aşağıdaki hatayı gösterir:

> Dalga içinde geçersiz yükleme satırları bulundu. Lütfen geçersiz yükleme satırlarını kaldırın.

Daha sonra, dalga içindeki her yükleme satırının son durumunu gözden geçirebilir ve yeniden denemeden önce tüm uyarıları düzeltebilirsiniz. Bu, daha sonra dalga işlemini yeniden işlemeden önce tüm uyarıları bir defada ele almanızı sağlar. (Önceki sürümlerde, sistem ilk uyarıdan sonra dalga öğesini işlemeyi durdurur; bu nedenle tek seferde yalnızca bir tane uyarı düzeltebilirsiniz.)

Sistemin dalga işleme durumu iletilerinizi görüntüleme şekli, **Ambar yönetimi parametreleri** sayfasında **dalga işleme geçmişi günlüğünü oluşturma** seçeneğini nasıl ayarladığınıza bağlıdır.

- **Dalga işleme geçmişi günlüğü** *Hayır* olarak ayarlandığında, yükleme satırı durum iletileri **bilgi günlüğünde** gösterilir.
- **Dalga işleme geçmişi günlüğü** *Evet* olarak ayarlandığında, yükleme satırı durum iletileri **Dalga işleme geçmişi günlüğünde** gösterilir. Günlüğü görüntülemek için, **Ambar Yönetimi \> giden dalgalar \> dalga işleme geçmişi günlüğü**'ne gidin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Dalga işlemeyi yapılandırma örneği](tasks/configure-wave-processing.md)
- [Dalga şablonları](wave-templates.md)
- [Konteyner Kullanımı](wave-containerization.md)
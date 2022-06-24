---
title: Müşteriye ait kıymetler için bakım faturası
description: Bu makalede, müşterilerinize ait kıymetler üzerinde yapılan bakım işini oluşturma, işleme ve faturlandırma açıklanmaktadır.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d6ad25ec49a329c16b0290278fb614293a507eae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887703"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a>Müşteriye ait kıymetler için bakım faturası

[!include [banner](../../includes/banner.md)]

*İş emri faturalama* özelliği, müşterilerine kıymetler üzerinde yapılan bakım işini oluşturmanıza, işlemenize ve faturalamanıza olanak tanır. Bu özellik, aşağıdaki görevleri yerine getirmenizi sağlar:

- Müşterileri sahip oldukları kıymetlere bağlama.
- İş emri oluştururken müşteri seçme ve müşteriye ait kıymetleri görüntüleme.
- Her müşteri için bir ana proje ayarlama.
- İş emri için saat, malzeme, gider ve ücret kaydetme ve ardından müşteri için fatura teklifi oluşturma.

Ayrıca bu özellik, aşağıdaki işlevleri de sunar:

- Proje sözleşmesi, müşterinin ana projesinden otomatik olarak ilgili iş emri projesine kopyalanır.
- Artık kıymet yönetimi, hem iş emri tahminlerinde hem de iş emri günlüklerinde *ücret* proje hareketi türünü kullanabilir.

## <a name="turn-on-the-customer-billing-feature"></a>Müşteri faturalandırma özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Proje yönetimi ve muhasebe*
- **Özellik adı**: *İş emri faturalama*

## <a name="example-scenario"></a>Örnek senaryo

Bu özelliğin nasıl çalıştığını öğrenmek için aşağıdaki örnek senaryo ile çalışın.

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Bu senaryodan, üretim sisteminde çalışırken özelliği kullanmaya yönelik kılavuz olarak da yararlanabilirsiniz. Ancak, bu durumda kendi değerlerinizi değiştirmeniz gerekir ve standart tanıtım verilerinin sağladığı bazı gerekli kayıt türleri kaybolabilir.

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a>1. Adım: Müşteri için yeni proje sözleşmesi oluşturma

1. **Proje yönetimi ve muhasebe \> Projeler \> Proje sözleşmeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Yeni proje sözleşmesi** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Ad:** *Pelikan Toptan Satış*
    - **Finansman türü**: *Müşteri*
    - **Finansman kaynağı:** *ABD-013* (*Pelikan Toptan Satış*)

1. **Tamam**'ı seçin.

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a>2. Adım: Müşteri için yeni bir ana proje oluşturma

Burada oluşturduğunuz ana proje, müşterinin iş emirleri oluşturulurken kullanılır.

1. **Proje yönetimi ve muhasebe \> Projeler \> Tüm projeler**'e gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Yeni proje** iletişim kutusunda aşağıdaki değerleri ayarlayın.

    - **Proje türü:** *Zaman ve malzeme*
    - **Proje adı:** *Pelikan Toptan Satış iş emirleri*
    - **Proje grubu:** *TM*
    - **Proje sözleşmesi kodu:** *Pelikan Toptan Satış* (daha önce oluşturduğunuz sözleşme)
    - **Başlangıç tarihi:** Bugünün tarihini seçin.

1. **Proje oluştur**'u seçin.
1. Yeni proje açılır. **Proje kodu** değerini not edin. Bu değeri daha sonra girmeniz gerekir.

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a>3. Adım: Kıymet yönetimi'nde yeni iş emri türü oluşturma

1. **Kıymet yönetimi \> Kurulum \> İş emri \> İş emri türleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Listeye yeni bir kayıt eklenir. Bu kayıt için aşağıdaki değerleri ayarlayın:

    - **İş emri türü:** *Servis*
    - **Ad:** *Servis iş emirleri*
    - **İş emri yaşam döngüsü durumu:** *Standart*

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a>4. Adım: Müşteri hesabını ana projeye bağlama

Şimdi Kıymet yönetimi'ndeki proje kurulumunda müşteri hesabını ana projeye bağlamanız gerekir.

1. **Kıymet yönetimi \> Kurulum \> İş emirleri \> Proje kurulumu**'na gidin.
1. **Ana proje** sekmesinde, satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *ABD-013* (*Pelikan Toptan Satış*)
    - **Proje kodu:** Daha önce not ettiğiniz proje kodunu girin.

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a>5. Adım: Proje grubunu ve türünü iş emri projesine bağlama

Hala **Proje kurulumu** sayfasında (**Kıymet yönetimi \> Kurulum \> İş emirleri \> Proje kurulumu**) olmanız gerekir.

1. **Proje grubu** sekmesinde, satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **İş emri türü:** *Servis* (daha önce oluşturduğunuz iş emri türü)
    - **Proje grubu:** *TM*

> [!NOTE]
> İş emri projesindeki proje sözleşmesi her zaman ana projeden devralınır.

### <a name="step-6-link-an-asset-to-the-customer-id"></a>6. Adım: Bir kıymeti müşteri koduna bağlama

1. **Kıymet yönetimi \> Kıymetler \> Etkin kıymetler**'e gidin.
1. **Filtre** alanına *VE-102* ifadesini girin ve **Kıymet**'e göre filtrelemeyi seçin.
1. Ayarlarını açmak için kıymeti seçin.
1. **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-013* (*Pelikan Toptan Satış*) olarak ayarlayın.

    **Ad** alanı, otomatik olarak *Pelikan Toptan Satış* olarak güncelleştirilir.

### <a name="step-7-create-a-new-work-order-on-the-asset"></a>7. Adım: Kıymette yeni iş emri oluşturma

1. **Kıymet yönetimi \> İş emirleri \> Etkin iş emirleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **İş emri oluşturun** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **İş emri türü:** *Servis*
    - **Açıklama:** *Kamyon Onarımı*
    - **Müşteri hesabı:** *ABD-013* (*Pelikan Toptan Satış*)
    - **Kıymet:** *VE-102*

        > [!NOTE]
        > Aramada yalnızca seçili müşteri hesabına bağlı olan kıymetler gösterilir.

    - **Bakım işi türü:** *Onarım*
    - **Meslek:** *Tamirci*
    - **Servis düzeyi:** *4*

1. **Tamam**'ı seçin.

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a>8. Adım: İş emrini inceleme ve üzerinde çalışmaya başlama

Bu bölümde, önceki bölümde oluşturduğunuz iş emri üzerinde çalışacaksınız.

1. Ana projenin *Pelikan toptan satış İş emri* projesi olduğunu doğrulamak için aşağıdaki adımları izleyin:

    1. **İş emri bakım işleri** bölümünde satır seçin.
    1. **Satır ayrıntıları** hızlı sekmesinde **Proje kodu** değerini inceleyin. Bu değer, *\<Parent-Project-ID\>-\<Project-ID\>* biçiminde tireyle ayrılmış bir sayı olmalıdır. Bu değer bir bağlantıdır.
    1. Ana proje ve proje adlarını görüntüleyebileceğiniz bir sayfa açmak için proje kodu bağlantısını seçin.

1. Eylem Bölmesinde **İş emri** sekmesindeki **Yaşam döngüsü durumu** grubunda **İş emri durumunu güncelleştir**'i seçin.
1. **İş emri durumunu güncelleştirin** iletişim kutusundaki **Seç** sütununda, **Yaşam döngüsü durumu** alanının *Devam ediyor* olarak ayarlandığı satır için onay kutusunu seçin.
1. **Tamam**'ı seçin.
1. **Yaşam döngüsü durumu: InProgress** iletişim kutusunda **Tamam**'ı seçin.

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a>9. Adım: İş emrinde harcanan saatleri deftere nakletme ve yeni fatura teklifi oluşturma

Bu bölümde, önceki bölümde üzerinde çalıştığınız iş emri üzerinde çalışmaya devam edeceksiniz.

1. Eylem Bölmesi'nde, **İş emri** sekmesinde, **Proje** grubunda, **Günlükler**'i seçin.

    **İş emri günlükleri** sayfası görüntülenir. Burada, iş emri üzerinde harcadığınız süreyi kaydedebilirsiniz.

1. **Saatler** hızlı sekmesinde **Satır ekle**'yi seçin.
1. Yeni satırda **Saatler** alanını *4* olarak ayarlayın.
1. Eylem Bölmesinde **Günlükleri deftere naklet**'i seçin.
1. İş emrine dönmek için **İş emri günlükleri** sayfasını kapatın.
1. Eylem Bölmesi'ndeki **Faturalama** sekmesinde, **Yeni fatura teklifi**'ni seçin.
1. **Fatura teklifi oluştur** iletişim kutusundaki **Proje hareketleri** bölümünde, faturalandırmak istediğiniz her satır için **Seç** onay kutusunu seçin.
1. İletişim kutusunu kapatmak ve yeni fatura teklifini görüntülemek için **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
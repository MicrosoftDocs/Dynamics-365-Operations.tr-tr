---
title: Ambar yerleştirme
description: Bu konuda ambar yerleştirme hakkında bilgiler verilmektedir. Ambar yerleştirme, talebi Sipariş edilen, Rezerve veya Serbest bırakılmış durumundaki siparişlerden madde ve ölçü birimine göre konsolide etmenize olanak sağlar. Bu, ambar yöneticilerinin, siparişleri ambara serbest bırakmadan ve malzeme çekme işi oluşturmadan önce malzeme çekme yerleşimlerini daha iyi planlamalarına yardımcı olur.
author: mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: d9080f192db0c59b4b4bc74468491e86ba0b7471
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530363"
---
# <a name="warehouse-slotting"></a>Ambar yerleştirme

[!include [banner](../includes/banner.md)]

Ambar yerleştirme, talebi *Sipariş edilen*, *Rezerve* veya *Serbest bırakılmış* durumundaki siparişlerden madde ve ölçü birimine göre konsolide etmenize olanak sağlar. Oluşturulan talep; miktar, birim, fiziksel boyutlar, sabit yerleşimler vb. temelinde malzeme çekme için kullanılacak yerleşimlere uygulanabilir. Yerleştirme planı belirlendikten sonra, her yerleşime uygun stok miktarını getirmek için stok yenileme işi oluşturulabilir.

Bu işlevsellik, ambar yöneticilerinin, siparişleri ambara serbest bırakmadan ve malzeme çekme işi oluşturmadan önce malzeme çekme yerleşimlerini daha iyi planlamalarına yardımcı olur.

## <a name="turn-on-the-warehouse-slotting-feature"></a>Ambar yerleştirme özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ambar yerleştirme özelliği*

## <a name="set-up-warehouse-slotting"></a>Ambar yerleştirmeyi ayarlama

Ambar yerleştirmeyi kullanmak için, sisteminizde aşağıdaki öğeleri ayarlamanız gerekir.

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Yerleştirme için ölçü birimi katmanları oluşturma

Ölçü birimi katmanları, yerleştirme amacıyla birden fazla ölçü biriminin birlikte gruplandırılmasını sağlar. Örneğin aynı kutu çekme alanından birden fazla kutu boyutu çekiliyorsa, tüm boyutlar için bir katman oluşturulabilir. **Katmanın parçası olması gereken her ölçü birimi için bir satır oluşturulmalıdır.**

1. **Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme ölçü birimi katmanları**'na gidin.
1. **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Ölçü birimi katmanı:** *HerKutuPl*
    - **Açıklama:** *Her kutu paleti*

1. **Kaydet**'i seçin.
1. **Ölçü birimi** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Birim:** *Kutu*
    - **Açıklama:** Bu alanı boş bırakın. Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.
    - **Birim sınıfı:** *Miktar*

1. Kılavuza ikinci bir satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Birim:** *ea*
    - **Açıklama:** Bu alanı boş bırakın. Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.
    - **Birim sınıfı:** *Miktar*

1. Kılavuza üçüncü bir satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Birim:** *PL*
    - **Açıklama:** Bu alanı boş bırakın. Değişikliklerinizi kaydettiğiniz zaman otomatik olarak doldurulur.
    - **Birim sınıfı:** *Miktar*

1. Katmanı kaydetmek için **Kaydet**'i seçin.

### <a name="create-a-directive-code-for-slotting"></a>Yerleştirme için yönerge kodu oluşturma

Bir şablonla ilişkilendirilmesi gereken yönerge kodunu seçmeniz gerekir.

1. **Ambar yönetimi \> Kurulum \> Yönerge kodları**'na gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Yönerge kodu**alanına, *Yerleştirme* girin.
1. **Yönerge açıklaması**alanına, *Yerleştirme* girin.

### <a name="set-up-slotting-templates"></a>Yerleştirme şablonlarını ayarlama

Her yerleştirme şablonu, stokun belirli bir ambar için yerleşimlere nasıl atandığını denetler. Her şablon her bir yerleştirme belirtimi için bir satır içermelidir. Yerleştirme şablonlarını ayarlamak için bu bölümdeki yordamları kullanın.

1. **Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme şablonları**'na gidin.
1. Şablon oluşturmak için **Yeni**'yi seçin.

Ardından, aşağıdaki alt bölümlerde anlatıldığı gibi, şablon üst bilgisini, yerleştirme belirtimlerini ve yerleşim yönergelerini ayarlamanız gerekir.

#### <a name="set-up-a-slotting-template-header"></a>Yerleştirme şablon üst bilgisini ayarlama

1. Şablonun üst bilgisinde aşağıdaki değerleri ayarlayın:

    - **Yerleştirme şablonu:** _61_
    - **Açıklama:** _61_
    - **Talep türü:** *Satış siparişi*

        Şu anda, *Satış siparişi* desteklenen tek talep türüdür.

    - **Talep stratejisi:** _Sipariş edilen_

        Bu alanda aşağıdaki değerler kullanılabilir:

        - **Sipariş edilen** – Satış siparişindeki tam sipariş edilen miktar talep olarak kabul edilecektir.
        - **Rezerve** – Yalnızca rezerve edilen (fiziksel ve sipariş edilen) satış siparişi satırı miktarları talep olarak kabul edilecektir.

    - **Ambar:** _61_
    - **Dalga talebinin rezerve edilmemiş miktarları kullanmasına izin ver:** _Evet_

Değerlendirilen talebin kapsamını daraltmak için bir sorgu da belirtebilirsiniz.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Her şablon için yerleştirme belirtimlerini ayarlama

Oluşturduğunuz her şablon için, her yerleştirme belirtimi için bir satır eklemek üzere aşağıdaki adımları izleyin.

1. **Yerleştirme şablonu ayrıntıları** hızlı sekmesinde, şablon satırı oluşturmak için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra:** _1_
    - **Açıklama:** _Sabit yerleşim_
    - **Minimum miktar:** _1_

        Bu alan, satır için gereken minimum talep miktarını tanımlar.

    - **Maksimum miktar:** _1000000_

        Bu alan, satır için geçerli olan maksimum talep miktarını tanımlar.

    - **Birim:** Bu alanı boş bırakın.

        Bu alan, minimum ve maksimum miktarların başvuruda bulunduğu ölçü birimini tanımlar.

    - **Ölçü Birimi Katmanı:** _HerKutuPl_

        Bu alan, satır için geçerli olan talebin ölçü birimlerini tanımlar. (Daha fazla bilgi için bu konuda daha önce işlenen [Yerleştirme için ölçü birimi katmanlarını ayarlama](#unit-tiers) bölümüne bakın.)

    - **Yerleştirme atama ölçütü:** _Miktarı dikkate al_

        Bu alanda aşağıdaki değerler kullanılabilir:

        - **Boş kabul et** – Bu sistem, malzeme çekme alanındaki tüm yerleşimlerin boş olduğunu varsayacak ve bu yerleşimlerde stok denetimi yapmayacaktır.
        - **Miktarı dikkate al** – Sistem, malzeme çekme alanındaki tüm yerleşimlerde stok denetimi yapacak ve boş olmayan yerleşimleri atlayacaktır.

    - **Yönerge kodu:** _Yerleştirme_

        Bu alan, stok yenileme işinin malzeme çekme yerleşimini bulmak için kullanılan yerleşim yönergesini tanımlar.

    - **Taşma konumu:** Bu alanı boş bırakın.

        Bu alan, satırın işlendiği sırada miktar için bir yerleşim bulunamazsa, stokun koyulacağı yerleşimi tanımlar.

    - **Araya izin ver:** _Evet_

        Bu seçenek *Evet* olarak ayarlandığında, herhangi bir talep yerleştirilemezse, stok bulunan ama yerleştirme yapılmayan yerleşimlerden dışarıya stok çekmek için hareket işi oluşturulur. Bunun üzerine şablon yeniden çalıştırılır. Bu kez, yerleşimlerdeki stoku yok sayar. Bu işlevsellik en iyi şekilde, **Yerleştirme atama ölçütü** alanı _Miktarı dikkate al_ olarak ayarlandığı zaman çalışır.

    - **Sabit yerleşim kullanımı:** _Ürün için yalnızca sabit yerleşimler_

        Bu alanda aşağıdaki değerler kullanılabilir:

        - **Sabit ve sabit olmayan yerleşimler** – Sistem sabit yerleşimleri kullanmayla sınırlı kalmaz.
        - **Ürün için yalnızca sabit yerleşimler** – Sistem ürün için yalnızca sabit yerleşimler olan yerleşimlere yerleştirme yapar.
        - **Ürün çeşidi için yalnızca sabit yerleşimler** – Sistem ürün çeşidi için yalnızca sabit yerleşimler olan yerleşimlere yerleştirme yapar.

1. **Kaydet**'i seçin.
1. İkinci bir şablon satırı oluşturmak için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra:** _2_
    - **Açıklama:** _Diğer_
    - **Minimum Miktar:** _1_
    - **Maksimum Miktar:** _1000000_
    - **Birim:** Bu alanı boş bırakın.
    - **Ölçü birimi katmanı:** _HerKutuPl_
    - **Yerleştirme atama ölçütü:** _Miktarı dikkate al_
    - **Yönerge kodu:** _Yerleştirme_
    - **Taşma konumu:** Bu alanı boş bırakın.
    - **Araya izin ver:** _Evet_
    - **Sabit yerleşimleri kullan:** _Sabit ve sabit olmayan yerleşimler_

    İkinci satır için sorguda, o satırla ilgili talebin yerleştirilebileceği yerleşimleri belirlemek için kullanılan ölçütleri belirtirsiniz.

1. **Sıra** alanının *2* olarak ayarlandığı satırı seçin.
1. **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Türetilmiş tablo:** *Yerleşimler*
    - **Alan:** *Yerleşim profili kodu*
    - **Ölçüt:** *Malzeme Çekme-06* (Listeyi genişletmek için alandaki çift artı işaretini \[**++**\] ve ardından *Malzeme Çekme-06* - *Malzeme Çekme Tesisi 6*'yı seçin.)

1. **Tamam**'ı seçin.

#### <a name="set-up-location-directives"></a>Yerleşim yönergelerini kur

Yerleştirme çekme işlemlerini destekleyecek en az bir yerleştirme yönergesi ayarlanmalıdır. Yerleştirme çekme işlemleri için yeni bir *stok yenileme yerleşimi yönergesi* ayarlamak için bu bölümdeki yordamları kullanın.

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Sol bölmedeki **İş emri türü** alanında *Stok yenileme*'yi seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni yerleşim yönergesinin üst bilgisindeki **Ad** alanına *61 Yerleştirme çekme işlemi* girin.

##### <a name="configure-the-location-directives-fasttab"></a>Yerleşim yönergeleri hızlı sekmesini yapılandırma

1. **Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın. Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **İş türü:** _Çekme_
    - **Tesis:** _6_
    - **Ambar:** _61_
    - **Yönerge kodu:** _Yerleştirme_

1. **Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.

##### <a name="configure-the-lines-fasttab"></a>Satırlar hızlı sekmesini yapılandırma

1. **Satırlar** hızlı sekmesinde yeni bir satır oluşturmak için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın. Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Başlangıç miktarı:** _0_
    - **Son miktar:** _1000000_

1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Yerleşim Yönergesi Eylemleri hızlı sekmesini yapılandırma

1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde yeni bir satır oluşturmak için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın. Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Ad:** _Toplu_
    - **Strateji:** _Yok_

1. **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.

##### <a name="edit-the-query"></a>Sorguyu düzenleme

1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Türetilmiş tablo:** *Yerleşimler*
    - **Alan:** *Bölge Kodu*
    - **Ölçüt:** *Toplu* (Listeyi genişletmek için alandaki çift artı işaretini \[**++**\] ve ardından *Toplu*'yu seçin.)

1. **Tamam**'ı seçin.

## <a name="scenario"></a>Senaryo

### <a name="set-up-the-scenario"></a>Senaryoyu ayarlama

Bu senaryo için, yerleşik örnek verileri kullanın ve bu bölümde açıklanan kayıtları oluşturun.

#### <a name="use-the-usmf-sample-data"></a>USMF örnek verilerini kullanın

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

#### <a name="create-demand"></a>Talep oluşturma

Yerleştirme uygulayacağınız talebi oluşturmak için bu adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanında _ABD-007_'yi seçin.
1. **Ambar** alanında _61_'i seçin.
1. **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde boş bir satır bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde:** _L0101_
    - **Miktar:** _20_

1. **Satır ekle**'yi seçerek yeni bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde:** _T0100_
    - **Miktar:** _8_

1. **Kaydet**'i seçin.
1. İkinci bir satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanında _ABD-008_'i seçin.
1. **Ambar** alanında _61_'i seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde boş bir satır bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde:** _T0100_
    - **Miktar:** _1_

1. **Kaydet**'i seçin.

### <a name="walk-through-a-typical-slotting-scenario"></a>Tipik bir yerleştirme senaryosu üzerinden ilerleme

Önceki bölümde açıklandığı gibi, tüm önkoşul öğeleri belirlendikten sonra, bu bölümdeki her alıştırmada çalışarak bu özelliği denemeye hazırsınız demektir.

#### <a name="generate-demand"></a>Talep oluştur

1. **Ambar yönetimi \> Kurulum \> Stok yenileme \> Yerleştirme şablonları**'na gidin ve daha önce oluşturduğunuz yerleştirme şablonunu seçin.
1. Eylem bölmesinde, **Talep oluştur**'u seçin. Bu komut sistemdeki tüm talepleri değerlendirir ve yerleştirme şablon sorgusunu eşleştirir. Böylece tüm siparişlerdeki toplam talep, miktar/ölçü birimi başına tek bir satırda birleştirilir. İşlem tamamlanınca bir bilgi iletisi görüntülenir.

#### <a name="slotting-demand"></a>Yerleştirme talebi

*Yerleştirme talebi*, yerleştirme şablonunun kurulumuna bağlı olarak, talep oluşturma sonuçlarını gösterir.

- Eylem bölmesinde, **Talep oluştur** komutundan elde edilen sonuçları görmek için **Yerleştirme talebi**'ni seçin. Yerleştirme talebindeki satırlar düzenlenebilir. Bir satırı silebilir, yeni bir satır ekleyebilir veya satır ayrıntılarını düzenleyebilirsiniz.

> [!NOTE]
> Talebi el ile düzenleyebilir veya veri yönetimini kullanarak harici bir sistemden içe aktarabilirsiniz. Yerleştirme talebindeki her şey sonraki adımda nereden geldiği dikkate alınmaksızın kullanılır.

#### <a name="locate-demand"></a>Talebi bul

Talep oluşturulduktan sonra, *yerleştirme planı* oluşturmak için **Talep bul** komutunu kullanmanız gerekir.

- Eylem bölmesinde, **Talep bul**'u seçin. Yerleştirme işlemi çalıştırılır. İşlem tamamlanınca bir bilgi iletisi görüntülenir.

#### <a name="slotting-plan"></a>Yerleştirme planı

Yerleştirme planı, her madde/miktarın atandığı yerleşimi, taşma kullanılıp kullanılmadığını, ara işi oluşturulup oluşturulmadığını ve kullanılan şablon satırını gösterir. **Yerleştirilememiş talepler kırmızı renkle vurgulanır.**

- Eylem bölmesinde, sonuçları görüntülemek için **Yerleştirme planı**'nı seçin.

#### <a name="create-replenishment"></a>Stok yenileme oluşturma

Yerleştirme planı oluşturulduktan sonra, plana göre, *stok yenileme işi* oluşturmanız gerekir.

- Eylem bölmesinde **Stok yenilemeyi çalıştır**'ı seçin. İşlem tamamlanınca bir bilgi iletisi görüntülenir. Bu ileti, iş yapı kodu için oluşturulan üst bilgilerin sayısını gösterir.

Kullanılacak yerleşim yönergeleri her bir şablon satırında belirtilen yönerge koduna göre tanımlanır.

## <a name="tips"></a>İpuçları

### <a name="set-up-automatic-slotting"></a>Otomatik yerleştirme ayarlama

Gerekli tüm öğeler belirlendikten sonra, aşağıdaki adımları izleyerek otomatik olarak çalışacak bir yerleştirme ayarlayabilirsiniz.

1. **Ambar yönetimi \> Stok yenileme \> Yerleştirmeyi çalıştır**'a gidin.
1. Çalıştırılacak yerleştirme adımlarını belirtin. Aşağıdaki yerleştirme adımlarından birini veya birkaçını seçin:

    - Talep oluştur
    - Talebi bul
    - Stok yenileme işi oluştur

    > [!NOTE]
    > Yerleştirme adımları aşamalıdır. *Talebi bul*'u seçmek istiyorsanız, önce *Talep oluştur*'u seçmeniz gerekir.

1. Kullanılacak yerleştirme şablonunu belirtin.
1. İsterseniz otomatik çalışma tekrar sayısını belirleyin.

Senaryodaki alıştırmalarda otomatik yerleştirme **ayarlamayın**.

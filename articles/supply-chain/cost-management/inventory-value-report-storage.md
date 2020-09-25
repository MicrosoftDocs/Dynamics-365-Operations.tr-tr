---
title: Stok değeri depolama raporu
description: Bu konuda, Stok değeri depolama raporunun nasıl çalıştırılacağı ve çıktının Microsoft Dynamics 365 Supply Chain Management'ta etkileşimli bir sayfa ya da birkaç biçimden birinde dışa aktarılan belge olarak dijital biçimde nasıl sunulacağı açıklanmaktadır.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f50318e0a955d8244ba854aa1fd73ad7532b9198
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759580"
---
# <a name="inventory-value-storage-report"></a>Stok değeri depolama raporu

Bu konuda, **Stok değeri depolama** raporunun nasıl çalıştırılacağı ve çıktının Microsoft Dynamics 365 Supply Chain Management'ta etkileşimli bir sayfa ya da birkaç biçimden birinde dışa aktarılan belge olarak dijital biçimde nasıl sunulacağı açıklanmaktadır.

Raporu tarayıcınızda görüntülediğinizde, sütunlar ve toplam bakiyeler yapılandırdığınız düzene göre dinamik olarak ayarlanır. Sonuçları sıralayabilir, filtreleyebilir ve verilerde detaya inebilir ve daha fazlasını yapabilirsiniz.

Rapor sonuçları **Stok değeri** veri varlığında depolanır. Bu nedenle, sonuçlara filtre uygulayabilir ve sonuçları virgülle ayrılmış değerler (CSV) veya Microsoft Excel biçimi gibi bir biçimde dışa aktarabilirsiniz.

**Stok değeri depolama** raporu,  çıktı birçok satır içerdiğinde yararlı olur. Örneğin, 50.000 maddeniz ve ambar olarak oluşturulmuş 300 mağazanız var. Bu durumda, stok sona erme bakiyelerini maddeye, tesise ve ambara göre talep ederseniz çıktı birçok satır içerir.

> [!NOTE]
> Rapor, rapor düzeninde tanımlanan alt toplamları içermez. Ayrıca, rapor düzeninde tanımlansa bile genel muhasebe bakiyelerini içermez. Genel muhasebe defterine mutabakat mizan kullanılarak yapılmalıdır.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Stok değeri depolama özelliğini etkinleştirme

**Stok değeri depolama** raporu oluşturabilmek için önce sisteminizde özelliği etkinleştirmelisiniz. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül** - Maliyet yönetimi
- **Özellik adı** - Stok değeri depolama

## <a name="generate-an-inventory-value-storage-report"></a>Stok değeri depolama raporu oluşturma

Bir **Stok değeri depolama** raporu oluşturmak ve depolamak için aşağıdaki adımları izleyin.

1. **Maliyet yönetimi \> Sorgular ve raporlar \> Stok değeri raporu depolama**'ya gidin.
1. **Yeni**'yi seçin.
1. Görüntülenen **Stok değeri** iletişim kutusunda, raporunuza hangi kayıtların ekleneceğini tanımlamak için aşağıdaki değerleri ayarlayın:

    - **Parametreler** hızlı sekmesinde, rapor için benzersiz bir ad girin ve rapora dahil edilen kayıtları tanımlamak için **Tarih aralığı** bölümündeki alanları kullanın. Tarih aralığını tanımlamak için **Tarih aralığı kodu** alanında önceden ayarlanmış bir aralık seçebilirsiniz (rapor oluşturma tarihine göre) veya **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında belirli tarihleri seçebilirsiniz.
    - **Dahil edilecek kayıtlar** hızlı sekmesinde, rapora dahil edilecek verileri tanımlamak için filtreler ve sınırlamalar ayarlayın.
    - **Arka planda çalıştır** hızlı sekmesinde raporun nasıl, ne zaman ve ne sıklıkta oluşturulacağını belirtin.

    > [!NOTE]
    > Bu rapor her zaman bir toplu işin parçası olarak çalıştırılır.

1. Ayarlarınızı uygulayıp iletişi kutusunu kapatmak için **Tamam**'ı seçin.

Toplu iş tamamlandıktan sonra rapor **Stok değeri raporu depolama alanı** sayfasında listelenir. Raporu görmek için sayfayı yenilemeniz gerekebilir.

## <a name="explore-an-inventory-value-storage-report"></a>Stok değeri depolama raporunu keşfetme

Raporu oluşturduktan sonra, istediğiniz zaman aşağıdaki adımları izleyerek görüntüleyebilir ve keşfedebilirsiniz:

1. **Maliyet yönetimi \> Sorgular ve raporlar \> Stok değeri raporu depolama**'ya gidin.
1. Listeden bir rapor seçin.
1. Rapor içeriğini göstermek için **Ayrıntıları görüntüle**'yi seçin.
1. Aşağıdaki adımlardan birini izleyerek raporu keşfedin:

    - Tabloları, Supply Chain Management'taki standart formların çoğunda olduğu gibi, o sütundaki değerlere göre sıralamak veya filtrelemek için neredeyse her sütun başlığını seçebilirsiniz.
    - Raporu kullanılabilir sütunlardan herhangi birinde herhangi bir değere göre filtrelemek için **Filtre** alanını kullanın.
    - Sıralama ve filtreleme seçeneklerinin sık kullanılan birleşimlerini kaydetmek ve yüklemek için görünüm menüsünü (**Filtre** alanının üzerinde) kullanın.

## <a name="export-an-inventory-value-storage-report"></a>Stok değeri depolama raporunu dışa aktarma

Oluşturduğunuz her rapor **Stok değeri** veri varlığında depolanır. Bu varlıktaki verileri CSV veya Excel gibi desteklenen herhangi bir veri biçiminde dışa aktarmak için Supply Chain Management'ın standart veri yönetimi özelliklerini kullanabilirsiniz.

Aşağıdaki örnekte **Stok değeri raporu** raporunun nasıl dışa aktarılacağı gösterilir.

1. **Sistem Yönetimi \> Çalışma alanları \> Veri yönetimi** seçeneğine gidin.
1. **İçe/dışa aktar** bölümünde **Dışa aktar** kutucuğunu seçin. 
1. Görüntülenen **Dışa aktar** sayfasında dışa aktarma işini ayarlarsınız. Öncelikle iş için bir grup adı girin.
1. **Seçili varlıklar** bölümünde, **Varlık ekle**'yi seçin.
1. Görüntülenen iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Varlık adı** - **Stok değeri**'ni seçin.
    - **Hedef veri biçimi** – Verilerin dışa aktarılacağı biçimi seçin.

1. Yeni satırı eklemek için **Ekle**'yi, iletişim kutusunu kapatmak için ise **Kapat**'ı seçin.
1. Genellikle bir seferde tek bir rapor dışa aktarabilirsiniz. Tek bir raporu dışa aktarmak için, **Sorgu** iletişim kutusuna yeni eklediğiniz satır için bir filtre ayarlayın. Bu şekilde, **Stok değeri** varlığındaki hangi raporun dışa aktarma işlemine dahil edileceğini tanımlayabilirsiniz. Tek bir raporu dışa aktarmak için aşağıdaki filtre seçeneklerini ayarlamak üzere bu adımları izleyin:

    1. **Aralık** sekmesinde, satır eklemek için **Ekle**'yi seçin.
    2. **Tablo** alanını **Stok değeri** olarak ayarlayın.
    3. **Türetilen tablo** alanını **Stok değeri** olarak ayarlayın.
    4. **Alan** alanını filtrelemek istediğiniz alan olarak ayarlayın. Genellikle, **Yürütme adı** alanını ve/veya **Yürütme zamanı** alanını kullanırsınız.
    5. **Ölçüt** alanını, seçili alanda aramak istediğiniz değere ayarlayın. (Önceki adımda **Yürütme adı** alanını seçtiyseniz, bu değer raporun adı olacaktır. **Yürütme zamanı** alanını seçtiyseniz, raporun oluşturulduğu saat olacaktır.)
    6. Gerekirse aradığınız raporu benzersiz olarak tanımlayıncaya kadar **Aralık** sekmesine daha fazla satır ekleyin.

1. Ayarlarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Dışa aktarma ayarınızı kaydetmek için **Kaydet**'i seçin.
1. **Dışa aktarma seçenekleri** sekmesinde dışa aktarma dosyasını oluşturmak için **Şimdi dışa aktar**'ı seçin.
1. Görüntülenen **Yürütme özeti** sayfasında dışa aktarma işinizin durumunu ve dışa aktarılan varlıkların listesini görebilirsiniz. **Varlık işleme durumu** bölümünde,  listeden **Stok değeri** varlığını seçin ve ardından söz konusu varlıktan dışa aktarılan verileri indirmek için **Dosyayı indir**'i seçin.

Veri yönetimini kullanarak verileri dışa aktarma hakkında daha fazla bilgi için bkz. [Veri içe ve dışa aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

---
title: Madde fiyatları depolama raporunu karşılaştırma
description: Madde fiyatlarını karşılaştırma depolama raporunun nasıl oluşturulacağını öğrenin ve sonucu bulun ve/veya dışa aktarın.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c6373679299b68413d75236ca8cc18ceba03e091
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335000"
---
# <a name="compare-item-prices-storage-report"></a>Madde fiyatları depolama raporunu karşılaştırma

[!include [banner](../includes/banner.md)]

Bu makalede, **Madde fiyatlarını karşılaştırma** raporunun nasıl çalıştırılacağı ve çıktının Dynamics 365 Supply Chain Management'ta etkileşimli bir sayfa ya da birkaç biçimden birinde dışa aktarılan belge olarak dijital biçimde nasıl sunulacağı açıklanmaktadır.

Raporu tarayıcınızda görüntülediğinizde, sütunlar ve toplam bakiyeler yapılandırılan düzeninize göre dinamik olarak ayarlanır. Sonuçları sıralayabilir, filtreleyebilir ve verilerde detaya inebilir ve daha fazlasını yapabilirsiniz.

Rapor sonuçları, sonuçları filtreleyerek CSV veya Microsoft Excel gibi bir biçimde dışa aktarmanızı sağlayan **Madde fiyatlarını karşılaştır** veri varlığında saklanır.

**Madde fiyatlarını karşılaştırma depolama** raporu, çıktının birçok satır içerdiği durumlarda yararlıdır. Örneğin, maliyetlendirme sürümünde bekleyen bir madde fiyatını tutan 40.000'den fazla maddeye sahipseniz çıkış birçok satır içerir.

## <a name="turn-the-compare-item-prices-storage-feature-on-or-off"></a>Madde fiyatlarını karşılaştır özelliğini açma veya kapatma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz. 10.0.29 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Madde fiyatı depolamasını karşılaştır* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

## <a name="generate-a-compare-item-prices-storage-report"></a>Madde fiyatlarını karşılaştırma depolama raporu oluşturma

Bir **Madde fiyatları karşılaştırma depolama** raporu oluşturmak ve depolamak için aşağıdaki adımları izleyin:

1. **Maliyet yönetimi > Sorgular ve raporlar > Önceden belirlenmiş maliyet raporları > Madde fiyatlarını karşılaştırma depolama** bölümüne gidin.

1. **Yeni**'yi seçerek **Ürün fiyatlarını karşılaştırma** bölmesini açın. Raporunuzda hangi fiyatların karşılaştırılacağını tanımlamak için aşağıdaki seçenekleri ayarlayın:

    - **Parametreler** hızlı sekmesinde, rapora benzersiz bir **Ad** verin ve karşılaştırılacak fiyatları ve tarihleri tanımlamak üzere **Karşılaştırılacak beklemedeki fiyatlar** ve **Karşılaştırma için kullanılan fiyatlar** bölümlerindeki alanları kullanın.
    - **Dahil edilecek kayıtlar** hızlı sekmesinde, rapora dahil edilecek verileri tanımlamak için filtreler ve sınırlamalar ayarlayın.
    - **Arka planda çalıştır** hızlı sekmesinde, raporu nasıl, ne zaman ve ne sıklıkta oluşturmak istediğinizi ayarlayın.
    > [!NOTE]
    > Bu rapor her zaman bir toplu işin parçası olarak yürütülür.

1. Ayarlarınızı uygulayıp bölmeyi kapatmak için **Tamam**'ı seçin.

1. Toplu iş tamamlandıktan sonra, **Madde fiyatlarını karşılaştırma depolama** sayfasında listelenir. Raporu görmek için sayfayı yenilemeniz gerekebilir.

## <a name="explore-the-compare-item-prices-storage-report"></a>Madde fiyatlarını karşılaştırma depolama raporunu keşfedin

Raporu oluşturduktan sonra, istediğiniz zaman aşağıdaki gibi görüntüleyebilir ve keşfedebilirsiniz:

1. **Maliyet yönetimi > Sorgular ve raporlar > Önceden belirlenmiş maliyet raporları > Madde fiyatlarını karşılaştırma depolama** bölümüne gidin.

1. Listeden bir rapor seçin.

1. Aşağıdakilerden birini yapın:

    - Rapor sonuçlarınıza ilişkin bir genel bakış elde etmek için **Genel bakış**'ı seçin.
    - Raporunuzun daha ayrıntılı bir görünümünü elde etmek için **Ayrıntıları görüntüle**'yi seçin

1. Seçili görünüm açıldıktan sonra, aşağıdakileri yapabilirsiniz:

    - Tabloları, Supply Chain Management'taki standart formların çoğunda olduğu gibi, o sütundaki değerlere göre sıralamak veya filtrelemek için neredeyse her sütun başlığını seçin. Hesaplanan bir alan olduğundan, **Net değişiklik fiyatı %'si** sütununu sıralayamazsınız veya filtreleyemezsiniz.
    - Forma eklenecek boyut sütununu seçebileceğiniz bir bölme açmak için **Boyut ekranı**'nı seçin. Sonraki açışınızda korunmaları için bu ayarları kaydetmek istiyorsanız **Ayarı kaydet**'i **Evet** olarak ayarlayın. Ayarlarınızı uygulayıp kapatmak için **Tamam**'ı seçin.
    - Formdaki herhangi bir satırı seçin ve seçili maddeyle ilgili daha fazla bilgi görmek için **Ayrıntıları görüntüle**'yi seçin. Burada, verilerde detaya inebilirsiniz.
    - Formdaki herhangi bir satırı seçin ve ardından sonuçlarınızın etkileşimli grafik sunumunu seçtiğiniz öğeye göre görüntülemek için **Karşılaştırma grafiğini görüntüle**'yi seçin. Bu sonuçları grafik ve grafik göstergesinde çeşitli grafiksel öğeler seçerek keşfedebilirsiniz.
    - Formdaki herhangi bir satırı seçin ve seçili maddeyle ilgili hesaplamalar hakkında daha fazla bilgi görmek için **Hesaplama ayrıntılarını görüntüle**'yi seçin. Burada, verilerde detaya inebilirsiniz.

## <a name="export-the-compare-item-prices-storage-report"></a>Madde fiyatlarını karşılaştırma depolama raporunu dışa aktarma

Oluşturduğunuz her rapor, **Madde fiyatlarını karşılaştır** veri varlığında depolanır. Bu varlıktaki verileri CSV veya Microsoft Excel gibi desteklenen herhangi bir veri biçiminde dışa aktarmak için Supply Chain Management'ın standart veri yönetimi özelliklerini kullanabilirsiniz.

Aşağıda, **Madde fiyatlarını karşılaştırma depolama** raporunun nasıl dışa aktarılacağına ilişkin bir örnek verilmiştir:

1. **Sistem yönetimi > Çalışma alanları > Veri yönetimi** bölümüne gidin.

1. **Veri Yönetimi** bölümünde **Dışa aktar** düğmesini seçin.

1. Dışa aktarma işinizi ayarlamak için kullanacağınız **Dışa aktarma** sayfası açılır. İşinize bir **Grup adı** vererek işe başlayın.

1. **Seçili varlıklar** bölümünde, aşağıdaki seçenekleri ayarlayabileceğiniz iletişim kutusunu açmak için **Varlık Ekle**'yi seçin:

    - **Varlık adı**: **Madde fiyatlarını karşılaştır**'ı seçin.
    - **Hedef veri biçimi**: Dışa aktarmak istediğiniz biçimi seçin.

1. Yeni satırı eklemek için **Ekle**'yi, iletişim kutusunu kapatmak için ise **Kapat**'ı seçin.

1. Genellikle bir seferde tek bir rapor dışa aktarabilirsiniz. Bunu yapmak için **Sorgu** bölmesine yeni eklediğiniz satır için bir **Filtre** ayarlayın. Böylece dışa aktarma işleminize **Madde fiyatlarını karşılaştırma** varlığındaki hangi raporları dahil etmek istediğinizi tanımlayabilirsiniz. Tek bir raporu dışa aktarmak için aşağıdaki filtre seçeneklerini ayarlayın:

    - **Aralık** sekmesinde, yeni satır eklemek için **Ekle**'yi seçin.
    - **Tablo**'yu **Madde fiyatlarını karşılaştır** olarak ayarlayın.
    - **Türetilen tablo**'yu **Madde fiyatlarını karşılaştır** olarak ayarlayın.
    - **Alanı** filtrelemek istediğiniz alan olarak ayarlayın. Genellikle **Yürütme adı** veya **Yürütme zamanı**'nı kullanabilirsiniz.
    - **Ölçütler**'i aramak istediğiniz seçili alandaki değer (raporun adı veya raporun oluşturulduğu saat) olarak ayarlayın.
    - Gerekirse aradığınız raporu benzersiz olarak tanımlayıncaya kadar **Aralık** tablosuna daha fazla satır ekleyin.

1. Ayarlarınızı kaydedip kapatmak için **Tamam**'ı seçin.

1. Dışa aktarma ayarınızı kaydetmek için **Kaydet**'i seçin.

1. **Dışa aktarma seçenekleri** sekmesini açın ve dışa aktarma dosyasını oluşturmak için **Şimdi dışa aktar**'ı seçin.

1. Dışa aktarma işinizin durumunu ve dışa aktarılan varlıkların listesini görebileceğiniz **Yürütme özeti** sayfası açılır. **Varlık işleme durumu** alanında listelenen **Madde fiyatlarını karşılaştır** varlığını seçin ve ardından söz konusu varlıktan dışa aktarılan verileri indirmek için **Dosyayı indir**'i seçin.

Veri yönetimini kullanarak verileri dışa aktarma hakkında daha fazla bilgi için bkz. [Veri içe ve dışa aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
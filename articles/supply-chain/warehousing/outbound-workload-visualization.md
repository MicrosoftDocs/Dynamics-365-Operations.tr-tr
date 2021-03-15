---
title: Giden iş yükü görselleştirmesi
description: Bu konuda giden iş yükü görselleştirmesi hakkında bilgiler verilmiştir. Bu işlevsellik, ambar yöneticilerinin ve denetçilerinin geçerli işin ilerlemesini ve kalan miktarını izlemek için kullanılabilecek özel iş yükü grafikleri oluşturmasına olanak tanır. Ambar yöneticileri birden çok görünüm oluşturabilir ve istedikleri gibi otomatik yenileme ayarlayabilir.
author: Mirzaab
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2515a71297df7213f93a4c619f7eebf1c2411b39
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965564"
---
# <a name="outbound-workload-visualization"></a>Giden iş yükü görselleştirmesi

[!include [banner](../includes/banner.md)]

**Giden iş yükü görselleştirmesi** sayfasından erişilebilen gelişmiş kurulum özellikleri, ambar yöneticilerinin ve denetçilerinin geçerli işin ilerlemesini ve kalan miktarını izlemek için kullanılabilecek özel iş yükü grafikleri oluşturmasına olanak tanır. Ambar yöneticileri birden çok görünüm oluşturabilir ve istedikleri gibi otomatik yenileme ayarlayabilir. Giden iş yükü görselleştirmeleri ambar performansı sayfalarında görüntülenmek için uygundur.

Bu işlevsellik, malzeme çekme işinin ilerlemesini izlemek için kullanılabilir. Özellik, iş gücü yönetimiyle tümleştirilir ve iş gücü yönetimi kurulmuşsa giden iş yükü görselleştirmeleri, gösterilen (filtrelenmiş) malzeme çekme işi için kalan saat sayısının bir hesaplamasını gösterebilir.

## <a name="turn-on-the-outbound-workload-visualization-feature"></a>Giden iş yükü görselleştirmesi özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Giden iş yükü görselleştirmesi*

## <a name="set-up-outbound-workload-visualizations"></a>Giden iş yükü görselleştirmesi görselleştirmesini ayarlama

Görselleştirmelerinizi ayarlamak için bir filtre koleksiyonu (görünümler) oluşturun ve her filtreyi farklı bir analiz türünü gösterecek şekilde tasarlayın. Filtreleri tasarlamak için **Filtreleri yapılandır** sayfasını kullanırsınız.

Bir giden iş yükü görselleştirmesi ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Ambar izleme raporları \> Giden iş yükü görselleştirmesi**'ne gidin.

    **Giden iş yükü görselleştirmesi** sayfası görüntülenir. Bazı filtreler oluşturduktan sonra, bu sayfa, görselleştirmenizi gösterir. İstediğiniz sayıda filtre oluşturabilirsiniz. Oluşturduğunuz tüm filtreler, daha sonra kullanabilmeniz için kullanıcı hesabınıza kaydedilir. Başka bir deyişle, her kullanıcı kendi oluşturduğu filtre kümesine sahip olur. Bu filtreler diğer kullanıcılarla paylaşılmaz.

1. **Giden iş yükü görselleştirmesi** sayfasında, Eylem bölmesinde, **Filtreler** sekmesinde, **Filtreleri Yapılandır**'ı seçin.
1. Filtre eklemek için **Filtreleri yapılandır** sayfasında, Eylem bölmesinde **Yeni**'yi seçin ve sonra filtre için şu alanları ayarlayın:

    - **X ekseni grubu tablosu**: X ekseni değerlerini gruplandırmak için kullanılması gereken alanı içeren tabloyu seçin.
    - **X ekseni grubu alanı**: **X ekseni grubu tablosu** alanında seçtiğiniz tablonun alanları arasından X ekseni değerlerini gruplandırmak için kullanılması gereken alanı seçin.
    - **X ekseni değer tablosu**: Grupları daha ayrıntılı analiz etmek için kullanılması gereken alanı içeren tabloyu seçin.
    - **X ekseni değer alanı**: **X ekseni değer tablosu** alanında seçtiğiniz tablonun alanları arasından, her grup için analiz edilmesi gereken değerleri sağlayan alanı seçin.
    - **Otomatik yenileme**: Görselleştirmenin otomatik olarak yenilenip yenilenmemesi gerektiğini seçin.
    - **Yenileme aralığı (dakika)**: Otomatik yenilemeler arasındaki dakika sayısını girin.
    - **Görüntüleme düzeyi**: Grafiğin açık satırları mı, yoksa açık üst bilgi sayılarını mı göstermesi gerektiğini seçin.
    - **Malzeme çekme türü**: **Görüntüleme düzeyi** alanını _Açık satırlar_ olarak ayarlarsanız grafikteki açık iş satırlarının sayısının ilk malzeme çekmeleri, hazırlama malzeme çekmeleri veya hem ilk malzeme çekmeler hem de hazırlama malzeme çekmeleri içerip içermeyeceğini seçin.
    - **Tesis**: Grafiğin hangi tesis için yükleneceğini seçin.
    - **Ambar**: Grafiğin hangi ambar için yükleneceğini seçin.
    - **Dahil edilecek gün sayısı**: Grafiğin oluşturulması gereken geçmiş gün sayısını girin.
    - **İş emri türü**: Filtre uygulayacak giden iş emri türlerini seçin.

    ![Filtreler sayfasını yapılandırma](media/work-viz-filters-1.png "Filtreler sayfasını yapılandırma")

1. **Giden iş yükü görselleştirmeleri** sayfasına dönmek için **Filtreleri yapılandır** sayfasını kapatın.

    **Giden iş yükü görselleştirmeleri** sayfası artık yeni filtre ayarlarınızı temel alan verileri gösterir. Yeni filtreniz artık kullanılabilir ve **Filtre** alanında seçilidir. Aşağıdaki alanlar grafiğin en üstünde bulunur:

    - **Filtre**: Bu alan, şimdiye kadar oluşturduğunuz tüm filtreleri içerir. Grafikteki verilerini görüntülemek için bir filtre seçin.
    - **Son yenilenme tarihi**: Bu alan, grafikteki bilgilerin en son güncelleştirildiği tarih ve saati gösterir.
    - **Tahmini/fiili süre**: Sisteminizde iş gücü standartları ayarlanmışsa grafikteki her sütunun üst kısmında bulunan toplu tahmini malzeme çekme sürelerini göstermek için bu seçeneği *Evet* olarak ayarlayın. İş gücü standartlarını kullanmıyorsanız bu seçenek kullanılamaz.

    ![Örnek görselleştirme](media/work-viz-chart.png "Örnek görselleştirme")

1. İlişkili iş satırı ayrıntılarını görüntülemek için grafikteki herhangi bir çubuğu seçin.

    ![İş satırı ayrıntıları](media/work-viz-work-details.png "İş satırı ayrıntıları")

## <a name="example-outbound-workload-visualization-for-zones"></a>Örnek: Bölgeler için giden iş yükü görselleştirmesi

Bu örnekte, her bölge için iş satırlarını ve her iş satırının durumunu _(Açık_, _Kapalı_ veya _İptal Edildi)_ gösteren bir görselleştirme ayarlamak istiyorsunuz. Bu durumda, aşağıdaki ayarlara sahip bir filtre ayarlayabilirsiniz:

- **Filtre adı**: Bu filtre için bir ad girin (_Bölge ve iş durumu_ gibi).
- **Açıklama**: Bu filtre için kısa bir açıklama girin (_Bölge ve iş durumu_ gibi).
- **X ekseni grubu tablosu**: _Konumlar_'ı seçin.
- **X ekseni grubu**: _Bölge Kimliği_'ni seçin.
- **X ekseni değer tablosu**: Bölge başına işi görüntülemek istediğiniziçin _İş_'i seçin.
- **X ekseni değer alanı**: İş durumunu görüntülemek istediğiniz _İş durumu_'nu seçin.
- **Otomatik yenileme**: Görselleştirmenin otomatik olarak yenilenip yenilenmemesi gerektiğini seçin.
- **Malzeme çekme türü**: Hem ilk malzeme çekmeleri hem de hazırlama konumlarından çekmeleri eklemek istediğiniz için _İlk malzeme çekmeler ve hazırlama malzeme çekmeleri_'ni seçin. Başka bir deyişle, aslında sahip olduğunuz tüm malzeme çekme işi satırlarını eklemek istersiniz.
- **Görüntüleme düzeyi**: Bilgileri iş üst bilgisine göre değil, satır başına göre görüntülemek istediğiniz için _Açık satırlar_'ı seçin.

Aşağıdaki çizimde örnek bir sonuç grafik verilmektedir.

![Bölge ve iş durumu görselleştirmesi](media/work-viz-chart.png "Bölge ve iş durumu görselleştirmesi")

Bu grafik, **KAT** ve **TOPLU** adlı iki bölge ve **Boş** adlı bir bölge gösterir. **Boş** bölgesi, herhangi bir bölgenin üyesi olmayan tüm iş satırlarını temsil eder. Grafik, her zaman mümkün olduğunca çok görünürlük sağlamak için tüm alakasız filtrelenmiş verileri **Boş** olarak gösterir. **KAT** bölgesinde, grafik üç kapalı satır ve dört açık satır gösterir. **TOPLU** bölgesinde, grafik dört kapalı satır, bir açık satır ve 24 iptal edilmiş satır gösterir. Son olarak, grafik, herhangi bir bölgenin parçası olmayan ve bu nedenle **Boş** olarak listelenen sekiz kapalı satırı gösterir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
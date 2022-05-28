---
title: Dalga işleme için ambar parametreleri
description: Bu konu, dalga işleme için ambar parametrelerinin nasıl ayarlanacağını açıklar. Çoklu iş siparişleri için malzeme çekme işini tek bir dalga içinde gruplamak amacıyla dalga işlemeyi kullanabilirsiniz.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c259ff6c5a2f1190afb82c2ab7ecdc99e2b05846
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695521"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Dalga işleme için ambar parametreleri

[!include [banner](../includes/banner.md)]

Bu konu, dalga işleme için ambar parametrelerinin nasıl ayarlanacağını açıklar. Çoklu iş siparişleri için malzeme çekme işini tek bir dalga içinde gruplamak amacıyla dalga işlemeyi kullanabilirsiniz.

Dalga işlemeyi kullanmak için, **Ambar yönetimi parametreleri** sayfasında aşağıdakileri belirtin:

- Dalgaları toplu iş kullanarak işleyip işleyemediğinizi.
- Dalgalar işlenirken bilgileri bir günlük dosyasında toplayıp toplamadığınızı.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Dalga işleme için ambar yönetimi parametreleri ayarlama

Dalga işleme için ambar parametrelerini ayarlamak üzere şu adımları izleyin:

1. **Ambar yönetimi** \> **Kurulum** \> **Ambar yönetim parametreleri**'ne gidin.

1. **Dalga işleme** hızlı sekmesinde, aşağıdaki ayarları yapın:

    - **Dalga işleme toplu il grubu**: Toplu işleri kullanarak dalgaları işlediğinizde kullanılacak toplu iş grubunu seçin. Toplu iş grubu toplu işlemlerinin çalıştırılacağı sunucuyu belirtir.
    - **Dalgaları toplu işle**: Dalgaların toplu iş tarafından otomatik olarak işlenmesinin etkinleştirilip etkinleştirilmeyeceğini seçin. Paralel işlemeyi kullanmak için bunu *Evet* olarak ayarlamalısınız. Toplu işi **Dalgaları işle** sayfasında ayarlarsınız. (Ayrıca bu listenin sonundaki nota bakın.)
    - **Dalga ilerlemesi günlüğü oluştur**: Sistemin bir maddenin her tahsisatında ve boyutlarının başlayıp sona erdiğinde günlük kaydı oluşturup oluşturmayacağını seçin. Bu günlüğü yalnızca gereksinim duyduğunuzda (örneğin, ilk test sırasında veya sorun giderme için) etkinleştirmelisiniz. Daha fazla bilgi için bkz. [Dalga tahsisatı](wave-allocation-method.md).
    - **Dalga işleme geçmişi günlüğü oluştur**: Bekleyen ayırmaların paralel işlemi sırasında dahil olmak üzere dalga işlendikten sonra bir dalga ile ilgili bilgilerin günlük dosyasına otomatik olarak kaydedilip kaydedilmeyeceğini seçin. Genellikle bunu sorun giderme sırasında etkinleştirmeniz gerekir çünkü ek yük ekler. Günlüğü görüntülemek için, **Ambar Yönetimi \> giden dalgalar \> dalga işleme geçmişi günlüğü**'ne gidin. Daha fazla bilgi için, bkz. [dalga oluşturma ve işleme](wave-processing.md).
    - **Konteyner kullanımı geçmiş günlüğü oluştur**: Dalga işlendikten sonra dalga için konteyner kullanımı hakkındaki bilgilerin bir günlük dosyasına otomatik olarak kaydedilip kaydedilmeyeceğini seçin. Günlüğü görüntülemek için, **Ambar Yönetimi \> Paketleme ve Konteyner kullanımı \> Konteyner kullanımı geçmişi**'ne gidin.
    - **Kilidi bekle (ms)**: Tahsisat adımının, başka bir tahsisat kaynağı tarafından kilitlenmiş olan bir sistem kaynağı için bekleyeceği zamanı, milisaniye cinsinden girin. Bu süre aşıldığında, dalga işlenmez ve bir hata iletisi görüntülenir.

1. **Ambara serbest bırak** hızlı sekmesinde, aşağıdaki ayarı yapın:

    - **Toplu işlemde hata**: Ambara serbest bırakma toplu işi başarısız olduğunda hata oluşturulup oluşturulmayacağını seçin. Bu etkinse, başarısız olan işler *hata* durumuyla sona erer. Bu devre dışıysa başarısız olan işler *Sonlandırıldı* durumuyla sona erer.

> [!NOTE]
> Dalgayı işlemek için kullanılan dalga şablonunda, dalga işlemeyi otomatikleştiren ayarları belirtebilirsiniz. Toplu iş için bir zamanlama ayarladıysanız, dalga şablonunda zamanlama ile otomasyon ayarlarını koordine etmeniz gerekir. Daha fazla bilgi için [Dalga şablonu oluşturma](wave-templates.md) konusuna bakın.
>
> *Taşıma Yönetimi* ve *Gelişmiş ambar yönetimi kullanıyorsanız*, bir dalga işlemi gerçekleştirdiğinizde yükleri konsolide etmek isteyip istemediğiniz belirtebilirsiniz. Örneğin, birkaç küçük yük aynı anda sevk edilebilir olduğunda bu kullanışlı bir seçenektir. Bir dalgayı işlerken yükleri konsolide etmek için, **yükler** sekmesinde, **dalga işleme sırasında yükleri konsolide et** onay kutusunu seçin.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Üretim dalgaları için tam veya kısmi rezervasyonu yapma

Satış siparişleri ve kanban siparişleri için, sipariş için ambarda serbest bırakılmadan önce stok ayrılmalıdır. Aksi halde, maddeler veya tahsisat satırları dalga içerisinde işlenemez. Ancak, üretim emirleri biraz daha esnektir. Üretim emirleri için, aşağıdakileri belirtebilirsiniz:

- Tüm malzemeler rezerve edilmese de üretim emirlerinin ambara serbest bırakılması için izin verin. Bu seçeneği belirlerseniz, ek malzemeler kullanılabilir duruma geldiğinde, ambara serbest bırak işlemini el ile tekrar etmeniz gerekir. Örneğin, üretimi başlatmak için gereken malzemeler varsa ve ek malzemelerin kullanılabilir olmasını bekleyebiliyorsanız bu seçenek kullanışlıdır.
- Bir sipariş ambara serbest bırakılmadan önce tüm malzemelerin rezerve edilmesi gerekir.

Tam ayırma istemek veya kısmi rezervasyona izin vermek için şu adımları izleyin:

1. **Üretim denetimi** \> **Kurulum** \> **Üretim denetimi parametreleri** öğesine gidin.
1. **Genel** sekmesinde, **ambara serbest bırak** alanında varsayılan ayarı seçin.

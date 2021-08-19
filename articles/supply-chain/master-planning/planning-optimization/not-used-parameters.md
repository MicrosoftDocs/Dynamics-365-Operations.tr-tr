---
title: Planlamayı En İyi Duruma Getirme tarafından kullanılmayan parametreler
description: Bu konu, Planlamayı En İyi Duruma Getirme işleminin operasyon sırasında dikkate almadığı parametreleri listeler.
author: crytt
ms.date: 6/29/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1992523ae10f30196ebe55d7c7fe6a2549a3a12853da261bd4a129523b8e4ea2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714295"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Planlamayı En İyi Duruma Getirme tarafından kullanılmayan parametreler

[!include [banner](../../includes/banner.md)]

Bu konu, Planlamayı En İyi Duruma Getirme işleminin operasyon sırasında dikkate almadığı parametreleri listeler. Örneğin ilgili işlevler henüz desteklenmediğinden planlama hizmeti bir parametreyi atlayabilir. Alternatif olarak, işlev değişiklikleri nedeniyle parametre geçersiz hale gelebilir.

Aşağıdaki bölümler, Planlamayı En İyi Duruma Getirme işleminin belirli sayfalardaki kullanmadığı parametreleri listeler. Ayrıca, her bir parametrenin niçin kullanılmadığını da açıklar.

## <a name="master-planning-parameters-page"></a>Master planlama parametreleri sayfası

Planlamayı En İyi Duruma Getirme, **Master planlama parametreleri** sayfasında bulunan aşağıdaki parametreleri veya seçenekleri kullanmaz:

- **Genel** sekmesi:

    - **Geçerli tahmin planı** – Bekleyen *Tahmin* desteği.
    - **Geçerli statik master plan** - *Statik planı dinamik plana kopyala* desteği bekleniyor.
    - **Geçerli dinamik master plan** - *Statik planı dinamik plana kopyala* desteği bekleniyor.
    - **Tam ve güncelleştirilmiş statik master planı dinamik master plana kopyala** - *Statik planı dinamik plana kopyala* desteği bekleniyor.
    - **Hesaplanan gecikmeler için başlangıç zamanı** – *Hesaplanan gecikmeler* desteği bekleniyor.
    - **Dinamik negatif günleri kullan** – Planlamayı En İyi Duruma Getirme, her zaman *Dinamik negatif günler* yaklaşımını kullanır.
    - **Bugünün tarihi takvimi** – *Planlama* desteği bekleniyor.
    - **Önbellek kullanımı** – Microsoft Azure aboneliğin yapılandırması performans noktalarını işler.
    - **Yardımcı görev paketi içindeki görev sayısı** - Azure abonelik yapılandırması performans noktalarını işler.
    - **Ön işleme: Doğrudan talep içeren öğelere göre otomatik filtre uygula** – Azure aboneliği yapılandırması performans noktalarını işler.
    - **Sonrada işleme: Doğrudan talep içeren öğelere göre otomatik filtre uygula** – Azure aboneliği yapılandırması performans noktalarını işler.
    - **Kesinleştirme paketindeki sipariş sayısı** - Azure abonelik yapılandırması performans noktalarını işler.
    - **İŞ parçacığı sayısı** - Azure abonelik yapılandırması performans noktalarını işler.
    - **Dakika cinsinden planlama işleme zaman aşımı** - Azure abonelik yapılandırması performans noktalarını işler.
    - **Planlama başlangıç saati** – *Planlama* desteği bekleniyor.

- **Planlı siparişler** sekmesi:

    - **Giriş saati** - *Planlama* desteği bekleniyor.
    - **Üretim** - *Planlama* desteği bekleniyor.
    - **Proje** bölümündeki alanlar – *Planlama* desteği bekleniyor.

- **Standart güncelleştirme** sekmesi:

    - **İşaretlemeyi güncelleştir** – *Kesinleştirme* desteği bekleniyor.
    - **Hata oluşursa kesinleştirmeyi durdur** – *Kesinleştirme* desteği bekleniyor.
    - **Satıcıya göre grupla** – *Kesinleştirme* desteği bekleniyor.
    - **Alıcı grubuna göre grupla** – *Kesinleştirme* desteği bekleniyor.
    - **Satınalma sözleşmesine göre grupla** – *Kesinleştirme* desteği bekleniyor.
    - **Döneme göre grupla** – *Kesinleştirme* desteği bekleniyor.
    - **Satınalma sözleşmesi bul** – *Kesinleştirme* desteği bekleniyor.
    - **Planlama önceliğine göre grupla** – *Kesinleştirme* desteği bekleniyor.
    - **Döneme göre grupla** – *Kesinleştirme* desteği bekleniyor.

## <a name="coverage-groups-page"></a>Karşılama grupları sayfası

Planlamayı En İyi Duruma Getirme, **Karşılama grupları** sayfasında bulunan aşağıdaki parametreleri veya seçenekleri kullanmaz:

- **Genel** FastTab'i:

    - **Pozitif gün sayısı** – *Pozitif gün sayısı* desteği bekleniyor.
    - **Eldeki stoğu kullan** – *Eldeki stok tüketimi* desteği bekleniyor.
    - **Belirtilen ürün reçetesi veya formül sürümünü kullan** - *Ortak/Yan ürün ile formül sürümleri* desteği bekleniyor.
    - **Belirtilen rota sürümünü kullan** – *Tanımlanmış özel ürün reçetesi veya rota gereksinimleri olan istek* desteği bekleniyor.

- **Eylem** hızlı sekmesi:

    - **Eylem iletisi** - *Eylemler* desteği bekleniyor.
    - **Eylem zaman aralığı** - *Eylemler* desteği bekleniyor.
    - **Erteleme marjı** - *Eylemler* desteği bekleniyor.
    - **Öne alma marjı** - *Eylemler* desteği bekleniyor.
    - **Esas tarih** *Eylemler* desteği bekleniyor.
    - **Öne al** - *Eylemler* desteği bekleniyor.
    - **Ertele** - *Eylemler* desteği bekleniyor.
    - **Azalt** - *Eylemler* desteği bekleniyor.
    - **Artır** - *Eylemler* desteği bekleniyor.
    - **Türetilen eylemler** - *Eylemler* desteği bekleniyor.

- **Diğer** hızlı sekmesi:

    - **Dondurma zaman dilimi (gün)** – *Dondurma zaman dilimi* desteği Planlamayı En İyi Duruma Getirme'de planlanmıyor.
    - **Ürün reçetesi açılımı zaman dilimi (gün)** – *Planlama* desteği bekleniyor.
    - **Kapasite planlama zaman dilimi (gün)** – *Planlama* desteği bekleniyor.
    - **Onaylanan istek zaman dilimi (gün)** – *İstek* desteği bekleniyor.
    - **Tahmin planı zaman dilimi** – *Tahmin* desteği bekleniyor.

- **Gecikmeler** Hızlı sekmesi:

    - **Hesaplanan gecikmeler** – *Hesaplanan gecikmeler* desteği bekleniyor.
    - **Hesaplanan gecikmeler zaman dilimi (gün)** – *Hesaplanan gecikmeler* desteği bekleniyor.

## <a name="item-coverage-page"></a>Madde karşılama sayfası

Planlamayı En İyi Duruma Getirme, **Madde karşılama** sayfasında bulunan aşağıdaki parametreleri veya seçenekleri kullanmaz:

- **Genel** sekmesi:

    - **Planlı sipariş türü** – Planlamayı En İyi Duruma Getirme, *Kanban* seçeneğini desteklemiyor, *Kanban* desteği bekleniyor.
    - **Dondurma zaman dilimi (gün)** – *Dondurma zaman dilimi* desteği Planlamayı En İyi Duruma Getirme'de planlanmıyor.
    - **Ürün reçetesi açılımı zaman dilimi (gün)** – *Planlama* desteği bekleniyor.
    - **Kapasite planlama zaman dilimi (gün)** – *Planlama* desteği bekleniyor.
    - **Onaylanan istek zaman dilimi (gün)** – *İstek* desteği bekleniyor.
    - **Minimumu karşıla**: Planlamayı En İyi Duruma Getirme *Bugünün tarihi*, *İlk çıkış* ve *Karşılama zaman dilimi* seçeneklerini desteklemez. Daima *Bugünün tarihi + tedarik süresi* seçeneğini kullanır.
    - **Minimum dönemler** - *Minimum stok düzeyi* desteği bekleniyor.
    - **Planlama formülü** - *Ortak/yan ürünler içeren formül sürümleri* desteği bekleniyor.
    - **Varsayılan öncelik** - *Ortak/yan ürünler içeren formül sürümleri* desteği bekleniyor.
    - **Geçerli öncelik** - *Ortak/yan ürünler içeren formül sürümleri* desteği bekleniyor.
    - **Değiştirilen tarih** - *Ortak/yan ürünler içeren formül sürümleri* desteği bekleniyor.
    - **Eldeki stoğu kullan** – *Eldeki stok tüketimi* desteği bekleniyor.

## <a name="master-plans-page"></a>Master planlar sayfası

Planlamayı En İyi Duruma Getirme, **Master planlar** sayfasında bulunan aşağıdaki parametreleri veya seçenekleri kullanmaz:

- **Genel** FastTab'i:

    - **Eldeki stoğu dahil et** – *Eldeki stok tüketimi* desteği bekleniyor.
    - **Eldeki stoğu geçersiz kıl** – *Eldeki stok tüketimi* desteği bekleniyor.
    - **Eldeki stoğu kullan** – *Eldeki stok tüketimi* desteği bekleniyor.
    - **Stok hareketlerini dahil et** – *Eldeki stok tüketimi* desteği bekleniyor.
    - **Satış tekliflerini dahil et** *Satış teklifi* desteği bekleniyor.
    - **Teklif taleplerini dahil et** - *Teklif talebi* desteği bekleniyor.
    - **Raf ömrü tarihlerini kullan** – *Raf ömrü* desteği bekleniyor.
    - **Devamlık planını dahil et** *Devamlık planlama* desteği bekleniyor.
    - **Planlama yöntemi** – *Planlama* desteği bekleniyor.
    - **Sınırlı özellik** - *Planlama* desteği bekleniyor.
    - **Geriye dönük planlama kapasitesi zaman dilimi** – *Planlama* desteği bekleniyor.
    - **Sınırlı kapasite** - *Planlama* desteği bekleniyor.
    - **Sınırlı kapasite zaman dilimi** - *Planlama* desteği bekleniyor.
    - **Performans sorunu olan kaynaklar için sınırlı kapasite** - *Planlama* desteği bekleniyor.
    - **Performans sorunu olan kaynaklar için kapasite zaman dilimi** - *Planlama* desteği bekleniyor.
    - **Planlı siparişler** – Planlamayı En İyi Duruma Getirme sabit numara sıraları kullanır.
    - **Oturum** – Planlamayı En İyi Duruma Getirme sabit numara sıraları kullanır.
    - **Devamlılık planı** – Planlamayı En İyi Duruma Getirme sabit numara sıraları kullanır.

- **Gün cinsinden zaman dilimleri** hızlı sekmesi:

    - **Dondur** – *Dondurma zaman dilimi* desteği Planlamayı En İyi Duruma Getirme'de planlanmıyor.
    - **Açılım** - *Planlama* desteği bekleniyor.
    - **Tahmin planı** – Ek *Tahmin* desteği bekleniyor.
    - **Kapasite** - *Planlama* desteği bekleniyor.
    - **Devamlık planı** *Devamlık planlama* desteği bekleniyor.
    - **Eylem iletisi** - *Eylemler* desteği bekleniyor.
    - **Hesaplanan gecikmeler** – Ek *Hesaplanan gecikmeler* desteği bekleniyor.
    - **Sıralama** - *Üretim* desteği bekleniyor.

- **Hesaplanan gecikmeler** Hızlı sekmesi:

    - **Planlanan siparişlerin master planlama çalıştırma tarihinden önce oluşturulmadığından emin ol** *Hesaplanan gecikmeler* desteği bekleniyor.
    - **Hesaplanan gecikmeyi gereksinim tarihine ekle** (**Planlanan satınalma siparişleri** bölümünde) – *Hesaplanan gecikmeler* desteği bekleniyor.
    - **Hesaplanan gecikmeyi gereksinim tarihine ekle** (**Planlanan üretim emirleri** bölümünde) – *Hesaplanan gecikmeler* desteği bekleniyor.
    - **Hesaplanan gecikmeyi gereksinim tarihine ekle** (**Planlanan transfer** bölümünde) – *Hesaplanan gecikmeler* desteği bekleniyor.
    - **Hesaplanan gecikmeyi gereksinim tarihine ekle** (**Planlı kanban** bölümünde) – *Hesaplanan gecikmeler* desteği bekleniyor.

- **Sıralama** Hızlı sekmesi:

    - **Master planlama sonrasında planlanmış siparişleri sırala** *Sıralama* desteği bekleniyor.
    - **Demet türü** – *Sıralama* desteği bekleniyor.
    - **Dönem türü** – *Sıralama* desteği bekleniyor.
    - **Kampanya döngüsündeki demetlerin sayısı** - *Sıralama* desteği bekleniyor.

## <a name="released-product-details-page"></a>Serbest bırakılan ürün ayrıntıları sayfası

Planlamayı En İyi Duruma Getirme, **Serbest bırakılan ürün ayrıntıları** sayfasında bulunan aşağıdaki parametreyi kullanmaz:

- **Mühendis** Hızlı sekmesi:

    - **Üretim türü** - Planlamayı En İyi Duruma Getirme, *Madde planlama* seçeneğini desteklemez, *Maddeleri planlama* desteği bekleniyor.

## <a name="default-order-settings-page"></a>Varsayılan sipariş ayarları sayfası

Planlamayı En İyi Duruma Getirme, **Varsayılan sipariş ayrıntıları** sayfasında bulunan aşağıdaki parametreyi kullanmaz:

- **Stok** Hızlı sekmesi:

    - **Teslimat tarihi denetimi** – Planlamayı En İyi Duruma Getirme *CTP* seçeneğini desteklemez, *CTP* desteği bekleniyor.

## <a name="working-time-calendars-page"></a>Çalışma zamanı takvimleri sayfası

Planlamayı En İyi Duruma Getirme, **Çalışma zamanı takvimleri** sayfasında bulunan aşağıdaki parametreyi kullanmaz:

- **Temel takvim** – *Temel takvimler* desteği bekleniyor.

## <a name="batch-disposition-master-page"></a>Toplu iş değerlendirme ana sayfası

Planlamayı En İyi Duruma Getirme, **Toplu iş değerlendirme ana verileri** sayfasında bulunan aşağıdaki parametreyi kullanmaz:

- **Kurulum** Hızlı sekmesi:

    - **Netleştirilebilir** *Toplu iş değerlendirme kodları* desteği bekleniyor.

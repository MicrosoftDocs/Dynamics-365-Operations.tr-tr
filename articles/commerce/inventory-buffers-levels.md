---
title: Stok arabelleklerini ve stok düzeylerini konfigüre et
description: Bu konu, Microsoft Dynamics 365 Commerce sitelerinde stok kullanılabilirliği iletilerini belirleyen stok arabelleklerinin ve stok düzeylerinin konfigüre nasıl yapılandırılacağını açıklamaktadır.
author: boycezhu
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: c519095d174414d6d4a8c86bc171ea62e1c72582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012454"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Stok arabelleklerini ve stok düzeylerini konfigüre et

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce sitelerinde stok kullanılabilirliği iletilerini belirleyen stok arabelleklerinin ve stok düzeylerinin konfigüre nasıl yapılandırılacağını açıklamaktadır.

## <a name="overview"></a>Özet

Dynamics 365 Commerce yönetim Merkezi, stok verilerini ve satış noktası (POS) uygulamaları, e-ticaret mağazaları ve zaman uyumsuz şekilde envanter çekme ve iletme gibi çeşitli kanalları içerir. Bu nedenle, Commerce merkezdeki eldeki stok sayfası aracılığıyla, POS Kullanıcı arabirimi (UI) aracılığıyla ve e-ticaret stok kullanılabilirlik API 'Leri aracılığıyla elde edilen kullanılabilir stok değerleri, gerçek zamanlı olarak yüzde 100 doğru sonuç vermez.

Çeşitli perakendeciler, e-ticaret mağazalarının içinde gerçek stok değerlerini göstermek yerine, stok kullanılabilirliği durumu hakkındaki iletileri (örneğin, "kullanılabilir" veya "stokta değil") göstermek için, bir maddenin satın alma veya potansiyel olarak stokta bulunup bulunmadığını bildirmek amacıyla, müşterileri bilgilendirmek için tercih eder. Bu yaklaşım için stok kullanılabilirliği iletileşme kullanılabilirliğini belirleyen stok arabelleklerinin ve stok düzeylerinin kullanılabilir ve konfigüre edilmiş olması gerekir.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Önkoşul: stok arabelleklerini ve stok düzeyleri özelliğini etkinleştirin

Stok arabelleklerinin ve stok düzeylerinin özelliği Commerce Headquarters 'da özellik yönetimi aracılığıyla denetlenir. Özelliği açmak için aşağıdaki adımları izleyin.

1. **Sistem Yönetimi** \> **Çalışma alanları** \> **Özellik yönetimi** seçeneğine gidin.
1. **Stok arabelleklerini ve stok düzeylerini etkinleştir** özelliğini arayın ve satırını seçin ve **Şimdi etkinleştir** 'i seçin.

Özellik etkinleştirildikten sonra, **Retail ve Commerce \> stok yönetiminde** stok düzeylerini bulabilirsiniz.

## <a name="create-and-configure-an-inventory-level-profile"></a>Stok düzeyi profili oluştur ve konfigüre et

*Stok düzeyi profili* belirli bir ürün miktarı durumunun stokta, stokta yok veya başka bir özel durumda dikkate alınıp alınmayacağını belirler. Her bir yasal varlık için birden fazla stok düzeyi profili oluşturabilir ve konfigüre edebilirsiniz. Her profil bir dizi stok düzeyinden oluşur ve her düzey bir *Aralık*, bir *kod* ve bir *etiket* tarafından tanımlanır.

- **Aralık** – Her Aralık bir *Başlangıç miktarı* ve bir *bitiş miktarı* ile tanımlanır. Miktar değeri, o aralıktaki başlangıç miktarından daha fazla ise ve bitiş miktarından fazla değil de bir aralığa karşılık gelir.
- **Kod** – Kod, düzeyi gösteren bir iç kısaltmadır. Doğrudan stok API 'Leriyle birleşen müşteriler, belirli bir stok düzeyi için ek mantık oluşturmak amacıyla kodlar kullanabilir. Örneğin, bu, stok düzeyi kodu **OOS** ("stokta değil") olduğunda ürünün satın alma yeteneğini kapatabilir.
- **Etiket** – Bir etiket, bir e-ticaret sitesindeki müşterilere stok düzeyi ilettiği anlamlı bir iletidir.

### <a name="create-an-inventory-level-profile"></a>Stok düzeyi profili oluştur

Envanter düzeyi profili oluşturmak için bu adımları izleyin.

1. **Retail ve Commerce** \> **Stok Yönetimi** \> **stok düzeylerine** gidin.
1. Eylem bölmesinde, **Yeni**'yi seçin ve **profil kodu** ve **Açıklama** alanlarına değerleri girin.
1. **Aralıklar** hızlı sekmesinde, Yeni bir düzey eklemek için **Ekle**'yi seçin ve sonra **Başlangıç miktarı**, **bitiş miktarı**, **kod** ve **etiket** sütunlarına bu düzeyin değerlerini girin. Daha fazla düzey eklemek için bu adımı tekrarlayın. Gerektiğinde, veri kılavuzundaki değerleri düzenleyebilir veya bir düzeyi kaldırmak için **Sil**'i seçebilirsiniz.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Yeni bir profil oluşturulduğunda, iki stok düzeyi otomatik olarak başlatılır:

- **OOS** – Aralığın alt sınırının negatif sonsuzluk olduğu "stok dışı" düzeyi. Başlangıç miktarı ve kod bu düzey için düzenlenemez.
- **KULLN** – aralığın üst sınırının sonsuz olduğu "kullanılabilir" düzey. Bitiş miktarı ve kod bu düzey için düzenlenemez.

> [!NOTE]
> Profil tanımında aralıklar arasında boşluk veya örtüşme olabilir.

Etiket iletisi için yerelleştirilmiş dizeleri yapılandırmak üzere, eylem bölmesindeki **Çeviriler** düğmesini kullanabilirsiniz. Yerelleştirilmiş dizeleri kanallara eşitlemek için **1110** (**genel yapılandırma**) dağıtım zamanlama işini çalıştırmalısınız.

### <a name="configure-an-inventory-level-profile"></a>Stok düzeyi profili yapılandır

Stok düzeyi profilini ürün kategori düzeyinde veya bağımsız ürün düzeyinde konfigüre edebilirsiniz. Bir ürün için stok düzeyi profili konfigüre edildiğinde stok düzeyi, bağlantılı profilde tanımlanan aralıklara göre belirlenir. Aksi takdirde, "kullanılabilir" veya "stok dışı" stok düzeyi, ürünün artı eldeki miktarına sahip olup olmadığına göre belirlenir.

Bir kategori için envanter düzeyi profili yapılandırma için bu adımları izleyin.

1. **Retail ve Commerce** \> **Ürünler ve kategoriler** \> **Commerce ürün hiyerarşisi**'ne gidin.
1. Envanter düzeyi profili yapılandıracak kategoriyi seçin.
1. **Satan ürün özellikleri** hızlı sekmesinde, yasal bir varlığı seçin.
1. **Commerce stok** bölümünde, **stok düzeyi profili** alanında, önceden tanımlanmış stok düzeyi profillerden birini seçin.

Kategori düzeyi profilin değerini kategorinin temel ürünlerine yaymak Için, eylem bölmesindeki ürünleri **Güncelleştir düğmesini** kullanabilirsiniz. Daha fazla bilgi için bkz. [ürün kategorilerini ve ürünleri yönet](category-management-product-creation.md).

Bir satışa sunulan ürün için envanter düzeyi profili yapılandırma için bu adımları izleyin.

1. **Retail ve Commerce** \> **Ürünler ve kategoriler** \> **Kategoriye göre serbest bırakılmış ürünler**'e gidin.
1. Bir ürün seçin ve ürün ayrıntıları sayfasını açın.
1. **Satış** hızlı sekmesinde **Commerce stok** bölümünde, stok düzeyi profili alanında, önceden tanımlanmış **stok düzeyi profillerden** birini seçin.

Yeni bir ürün oluşturulduğunda, başka bir ürün düzeyi özniteliği gibi **stok düzeyi profil** alanı, ürünün ilişkilendirildiği kategori için konfigüre edilmiş değere ayarlanır.

> [!NOTE]
> Stok düzeyi profili tüzel kişiliği özgü bir özniteliktir. Aynı kategori veya ürün için, stok düzeyi profil değeri yasal varlıklarda farklılık gösterebilir.

Stok düzeyi profillerinin yapılandırmalarını kanallara eşitlemek için, aşağıdaki adımları izleyin.

1. **Retail ve Commerce** \> **Retail ve Commerce BT** \> **Dağıtım planı**'na gidin.
1. **1040** (**ürün**) dağıtım zamanlamasını çalıştırın.

## <a name="configure-an-inventory-buffer"></a>Stok tamponu konfigüre et

*Stok tamponu*, maddenin ek miktarını orijinal miktardan çıkaran ve tahmin edilen miktarı hesaplamak için kullanılan Kullanıcı tanımlı bir değerdir. Bu tahmin edilen miktar, gerçek eldeki stoklarından daha fazla satış yaparak bir ürünün fazla satılmaması için perakendecilere güvenli tampon sağlar. Stok tamponu ürün kategori düzeyinde veya bağımsız ürün düzeyinde konfigüre edebilirsiniz. Herhangi bir stok tamponu belirtilmezse, varsayılan değer olan **0** (sıfır) değeri kullanılır.

Bir kategori için envanter tamponu yapılandırma için bu adımları izleyin.

1. **Retail ve Commerce** \> **Ürünler ve kategoriler** \> **Commerce ürün hiyerarşisi**'ne gidin.
1. Envanter tamponu yapılandıracak kategoriyi seçin.
1. **Satan ürün özellikleri** hızlı sekmesinde, yasal bir varlığı seçin.
1. **Commerce stoku** bölümünde, **Stok tamponu** alanına pozitif bir değer girin.

Kategori düzeyi tamponunun değerini kategorinin temel ürünlerine yaymak Için, eylem bölmesindeki ürünleri **Güncelleştir düğmesini** kullanabilirsiniz. Daha fazla bilgi için bkz. [ürün kategorilerini ve ürünleri yönet](category-management-product-creation.md).

Bir sunulan ürün için envanter tamponu yapılandırma için bu adımları izleyin.

1. **Retail ve Commerce** \> **Ürünler ve kategoriler** \> **Kategoriye göre serbest bırakılmış ürünler**'e gidin.
1. Bir ürün seçin ve ürün ayrıntıları sayfasını açın.
1. **Satış** hızlı sekmesinde **Commerce stoku** bölümünde, **Stok tamponu** alanına pozitif bir değer girin.

Yeni bir ürün oluşturulduğunda, **stok tamponu** alanı, ürünün ilişkilendirildiği kategori için konfigüre edilmiş değere ayarlanır.

> [!NOTE]
> Stok tamponu ve stok düzeyi profillerinin her ikisi de bir ürün için konfigüre edilebilir ise, maddenin tahmini miktarı (yani orijinal miktar eksi tampon değeri) stok düzeyini belirlemek için Aralık hesaplaması olarak kullanılacaktır.

Stok tamponu yapılandırmalarını kanallara eşitlemek için, aşağıdaki adımları izleyin.

1. **Retail ve Commerce** \> **Retail ve Commerce BT** \> **Dağıtım planı**'na gidin.
1. **1040** (**ürün**) dağıtım zamanlamasını çalıştırın.

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>E-ticaret senaryosunda stok arabelleklerini ve stok düzeylerini kullan

Commerce Site Builder, Commerce Headquarters 'da bulunan ve e-ticaret sitelerindeki stok kullanılabilirliği iletilerini belirlemek için stok tamponu ve stok düzeyi yeteneklerini kullanır. Daha fazla bilgi için, [Envanter ayarları uygula](inventory-settings.md) konusuna bakın.

Alternatif olarak, üçüncü taraf bir e-ticaret çözümüyle entegre ediyorsanız, e-ticaret senaryonuza bir ürünün stok kullanılabilirliğini göstermek için **GetEstimatedAvailability** ve **GetEstimatedProductWarehouseAvailability** API'lerini kullanabilirsiniz. Bu API 'Ler hakkında daha fazla bilgi için bkz [Perakende kanalları için envanter kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md).

Stok arabelleklerinin ve stok düzeylerinin girişi, bu API 'Lerin toplam kullanılabilir ve kullanılabilir fiziksel değerlere göre belirlenen stok düzeyi kodları ve etiket iletileri döndürmesini sağlar. API, stok miktarının iletiyle birlikte iade edilmiş olup olmadığını ve kullanılabilir miktarın stok tampon değeri tarafından azaltılıp azaltılamayacağını belirlemek için daha da konfigüre edilebilir.

Ürün kullanılabilirliği API 'Lerinin yanıtını konfigüre etmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce** \> **Genel merkez ayarı** \> **Parametreler** \> **Commerce parametreleri**'ne gidin.
1. **Mağaza Stoku** bölümünde, **Stok** sekmesinde, **e-ticaret için ürün kullanılabilirliği API'lerinde** bir değer seçin.
1. Ayarları kanallara uygulamak için, **1110** (**genel yapılandırma**) dağıtım zamanlaması işini çalıştırın.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün kategorilerini ve ürünleri yönetme](category-management-product-creation.md)

[Stok ayarlarını uygula](inventory-settings.md)

[Perakende kanalları için stok kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md)

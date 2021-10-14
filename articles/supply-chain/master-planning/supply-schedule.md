---
title: Tedarik planı
description: Bu konuda, Tedarik planı sayfası ve özellikleri hakkında bilgi sağlanmaktadır.
author: ChristianRytt
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d2f0f38d86ae307ef80bd02901e19a08d5e30ae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578380"
---
# <a name="supply-schedule"></a>Tedarik planı

[!include [banner](../includes/banner.md)]

**Tedarik planı** sayfası, bir ürün veya ürün ailesi için arz ve talebe ilişkin kapsamlı bir genel bakış gösterir. Bilgiler konuma, master plana ve dönemlere göre filtrelenir. Sayfayı yeni siparişler oluşturmak, mevcut planlı siparişleri değiştirmek ve master planlama çalıştırmak için de kullanabilirsiniz.

## <a name="open-the-supply-schedule-page"></a>Tedarik planı sayfasını açma

**Tedarik planı** sayfasını aşağıdaki yollardan biriyle açabilirsiniz:

- **Master planlama \> Master planlama \> Tedarik planı**'na gidin. **Filtreyi değiştir** iletişim kutusunda, sağlanan alanlara filtre değerleri girerek aradığınız planı ve ürünü belirtin. (Bu konunun geri kalanında, girdiğiniz filtre değerleri koleksiyonuna "filtre" veya "geçerli filtre" adı verilir.) Bitirdiğinizde, **Tamam**'ı seçin.
- **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin. Bir ürün seçin veya açın. Ardından, Eylem Bölmesi'nde, **Plan** sekmesindeki **Görüntüleme** gurubunda **Tedarik planı**'nı seçin.
- **Master planlama \> Kurulum \> Talep tahmini \> Madde tahsisat anahtarları**'na gidin. Ürün ailesi olarak kullanılan bir madde tahsisat anahtarı seçin. Eylem Bölmesi'nde **Tedarik planı**'nı seçin.
- **Master planlama \> Master planlama \> Planlı siparişler** öğesine gidin. Planlanan bir sipariş seçin veya açın. Ardından, Eylem Bölmesi'nde, **Görüntüle** sekmesindeki **Görüntüle** gurubunda **Tedarik planı**'nı seçin.

> [!NOTE]
> Üründen, ürün ailesinden veya planlı siparişten **Tedarik planı** sayfasını açtığınızda, filtre değerleri girmeniz gerekmez. Sistem varsayılan dönem şablonunu kullanır.

## <a name="use-the-supply-schedule-page"></a>Tedarik planı sayfasını kullanma

**Tedarik planı** sayfası bir üst bölümden, **Dönem bitiş stok** hızlı sekmesinden, üst bölümde seçilen satıra göre görünür hale gelen ek bir hızlı sekmeden ve Bilgi kutusu bölmesinden oluşur. (Bilgi Kutusu bölmesini açmak ve Bilgi Kutusunu görüntülemek için sayfanın sağ kenarında **İlgili bilgiler** öğesini seçin.)

### <a name="upper-section"></a>Üst bölüm

**Tedarik planı** sayfasının üst bölümü, bir ürün veya ürün ailesi için aşağıdaki verileri gösteren bir ızgara içerir. Bu veriler, filtreden **Dönem şablonu** değeriyle tanımlanan dönemlere göre ayrılır.

- **Dönem başlangıç stok**: Bu satırda, sistemdeki tüm siparişlerin gerçekleşmesi durumunda dönem başında beklenen stok bakiyesi gösterilir.
- **Dönem bitiş stok**: Bu satırda, sistemdeki tüm siparişlerin gerçekleşmesi durumunda dönem sonunda beklenen stok bakiyesi gösterilir.
- **Dönem ilişkilendirilmiş stok**: Bu satırda, dönem sonunda gelecekteki talebe göre ilişkilendirilen stok miktarını gösterilir.
- **Dönem net tedarik**: Bu satırda, arz ve talep arasındaki fark gösterilir.
- **Minimum stok miktarı**: Bu düğümde, bir ürün veya ürün ailesi için emniyet stoğu gösterilir. Bu düğümü genişletmek veya daraltmak için seçin ve ardından araç çubuğunda **Genişlet** veya **Daralt**'ı seçin. Bu düğüm yalnızca ürün veya ürün ailesi için emniyet stoğu olduğunda gösterilir.
- **Talep**: Bu düğümde bir ürün veya ürün ailesinin talebi gösterilir. Talep, hareket türüne göre gruplandırılır. Bu düğümü genişletmek veya daraltmak için seçin ve ardından araç çubuğunda **Genişlet** veya **Daralt**'ı seçin. Talep hareketi türlerine satışlar, transferler ve stok günlükleri dahildir. Bu düğüm yalnızca ürün veya ürün ailesi için talep olduğunda gösterilir.
- **Tedarik**: Bu düğümde bir ürün veya ürün ailesinin tedariği gösterilir. Tedarik, hareket türüne göre gruplandırılır. Bu düğümü genişletmek veya daraltmak için seçin ve ardından araç çubuğunda **Genişlet** veya **Daralt**'ı seçin. Tedarik hareket türlerine üretim, satınalma ve transferler dahildir. Bu düğüm yalnızca ürün veya ürün ailesi için tedarik olduğunda gösterilir.

Kullanılabilir araç çubuğu düğmelerinin, Bilgi kutusu ve hızlı sekmesi görüntülerinin çoğu, üst bölümdeki seçimlerinize bağlıdır. Genellikle, **Tedarik** veya **Talep** düğümünün altındaki satırlardan birini seçerek bir hareket türü belirlersiniz. Ardından, seçili satır için belirli bir sütunu seçerek bir dönem seçeceksiniz.

**Tedarik planı** sayfasının üst bölümünde yer alan ızgaranın üzerindeki araç çubuğunda aşağıdaki düğmeler sunulur:

- **Genişlet/Daralt**: **Talep** düğümü, **Tedarik** düğümü ve bunların alt düğümleri gibi seçili bir düğümü genişletin veya daraltın. (Düğümlerde şu anda daraltılmış veya genişletildiklerini belirten bir **\[+\]** veya **\[-\]** öneki gösterilir.)
- **Yeni**: Her komutun sırayla seçim için belirli bir öğe türü eklemenizi sağlayan bir iletişim kutusu veya sayfa açtığı bir menü açın. Kullanılabilir komutlar şunları içerir: **Tedarik tahmini**, **Planlı sipariş**, **Planlanmış kanban**, **Yeni üretim emri**, **Satınalma siparişi** ve **Transfer emri**.
- **Master planlama**: Master planlamayı çalıştırın. Çalıştırılacak planı belirleyebileceğiniz bir iletişim kutusu görüntülenir. Varsayılan olarak, **Master plan** alanını geçerli filtreyle eşleşecek şekilde ayarlayın.
- **Maksimum tamamlandı bildirimi**: Mevcut filtrede tanımlanan ürün için **Maksimum tamamlandı bildirimi** sayfasını açın.
- **Planlı siparişleri güncelleştir**: Geçerli filtrede tanımlanan ürün veya ürün ailesi için planlı siparişleri gösteren **Planlı siparişler** sayfasını açın.
- **Düzey**: Açılan iletişim kutusundan ayarlara göre planlı siparişleri yayın.
- **Konuma göre malzeme planı ilkesi**: Geçerli filtrede tanımlanan ürün için **Madde karşılama** sayfasını açın.
- **Kanban kuralı**: Geçerli filtrede tanımlanan ürün için **Kanban kuralları** sayfasını açın.

### <a name="fasttabs"></a>Hızlı sekmeler

**Tedarik planı** sayfası aşağıdaki hızlı sekmeleri içerebilir:

- **Dönem bitiş stok**: Bu hızlı sekmede, dönem sonu stok verileri grafik biçiminde gösterilir.
- **Tedarik profili**: Bu hızlı sekmede, tedarik verileri grafiksel bir biçimde gösterilir. Üst kısımda **Tedarik** düğümünü veya altındaki bir satırı seçtiğinizde görünür hale gelir.
- **Özet**: Bu hızlı sekmede, üst kısımda seçtiğiniz hareket türüyle ilişkili özet ayrıntıları gösterilir. Örneğin, **Talep** düğümü altında **Satış**'ı seçerseniz bu hızlı sekmede, **İstenen satış siparişi satırları** veya **Toplam tutar** gibi satış siparişleriyle ilgili alanlar gösterilir. **Tedarik** düğümünün **Üretim** alt düğümü altında **Üretim emirleri**'ni seçerseniz bu hızlı sekme, üretim siparişleriyle ilgili alanları gösterir; örneğin **Planlanan üretim siparişleri** veya **Toplam planlanan**. Alan değerleri, üst bölümde seçtiğiniz döneme bağlıdır. 
- **\[Hareket türü \] - \[Dönem \]**: Bu hızlı sekmede, üst bölümde seçtiğiniz hareket türü ve dönem için emirler gösterilir. Hızlı sekmenin adı bu seçimleri yansıtır. Örneğin, **Satış siparişleri - Bekleme listesi** veya **Üretim emirleri - 37. hafta** olarak adlandırılabilir.

### <a name="action-pane"></a>Eylem Bölmesi

Aşağıdaki düğmeler Eylem Bölmesi'nde kullanılabilir:

- **Filtreyi değiştir**: Filtre değerlerini güncelleştirebileceğiniz **Filtreyi değiştir** iletişim kutusunu açın ve ardından güncelleştirilmiş filtre ayarlarını yansıtan **Tedarik planı** sayfasını yeniden açın.
- **Gecikmeleri göster**: Bu hareket türü için gecikmiş bir sipariş varsa üst bölümdeki ilgili satırları vurgulayın.

### <a name="factbox-pane"></a>Bilgi Kutusu bölmesi

Bilgi Kutusu bölmesini açmak ve Bilgi Kutusunu görüntülemek için sayfanın sağ kenarında **İlgili bilgiler** öğesini seçin. **Tedarik planı** sayfasında aşağıdaki Bilgi Kutuları kullanılabilir:

- **Madde ayrıntıları**: Bu Bilgi Kutusu, geçerli filtrede tanımlanan ürünle ilgili temel bilgileri gösterir. Filtrede bir ürün ailesi tanımladıysanız boştur.
- **Eylemler**: Bu Bilgi Kutusu, üst bölümde seçtiğiniz hareket türündeki emirler için eylemleri gösterir.
- **Gecikmeler**: Bu Bilgi Kutusu, üst bölümde seçtiğiniz hareket türündeki emirler için gecikmeleri gösterir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

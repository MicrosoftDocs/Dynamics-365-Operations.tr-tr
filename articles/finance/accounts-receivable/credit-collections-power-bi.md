---
title: Alacak ve tahsilat yönetimi Power BI içeriği
description: Bu konu, Power BI Kredi ve Tahsilatlar Yönetimi'nde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.
author: ShivamPandey-msft
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 65423f49ba106a152f58c92533c4f1a16d47a318982cfe69bb23f9091fa09846
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763226"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Alacak ve tahsilat yönetimi Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Power BI **Kredi ve Tahsilatlar Yönetimi**'nde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Kredi ve tahsilatlar yönetimi** Power BI içeriği, kredi ve tahsilatlar yöneticileri ve tahsilat elemanları için oluşturulmuştur. Bekleyen satış gün sayısı, vadesi geçmiş bakiye, kredi riski ve kredi limitini aşan müşteriler gibi önemli kredi ve tahsilatlar ölçümleri sağlar. Hareket verileri kullanır ve kredi ve tahsilatların tüm şirket içindeki toplam görünümünü sağlar. Şirket, müşteri grubu ve müşteri başına çözümleme de sağlar.

Bu Power BI içeriği 10 rapor sayfasından oluşur:

- İki genel bakış sayfası (kredi genel bakışı için bir sayfa ve tahsilatlar genel bakışı için bir sayfa)
- Çeşitli boyutların dilimlenmiş kredi ve tahsilatlar ölçümlerinin ayrıntılarını sağlayan sekiz sayfa

Gösterilen tüm tutarlar sistem para birimi cinsindendir. Sistem para birimini **Sistemler parametreleri** sayfasından ayarlayabilirsiniz.

Şirket için kredi ve tahsilatlar verisi varsayılan olarak gösterilir. Tüm şirketler arasında veriyi görmek için **CustCollectionsBICrossCompany** görevini role ekleyin.

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI içeriğini görüntülemek için kurulum gerekiyor

Verilerin **müşteri alacak ve tahsilatları** Power BI görsellerinde görüntülenmesi için aşağıdaki kurulumun tamamlanması gereklidir.

1. **Sistem para birimi** ve **Sistem döviz kuru**'nu ayarlamak için **Sistem yönetimi > Kurulum > Sistem Paramatreleri**'ne gidin.
2. Etkin döneme atanan mali takvim tarihlerini doğrulamak için **Genel muhasebe > Takvimler > Mali takvimler**'e gidin.
3. **Genel Muhasebe > Ayarlar > Muhasebe**'ye gidin ve **Muhasebe Para Birimi** ve **Döviz Kuru Türü**'nü ayarlayın.
4. Hareket para birimleri ile muhasebe para birimi, muhasebe para birimi ve sistem para birimi arasındaki döviz kurlarını tanımlayın. Bunu yapmak için **Genel Muhasebe > Para Birimleri > Para birimi döviz kurları**'na gidin.
5. **CustCollectionsBIMeasurementsV2** toplam ölçümünü Varlık Deposu sayfası üzerinde yenilemek için **Sistem yönetimi > Ayarlar > Varlık Deposu**'na gidin.

>[!NOTE] 
> Yaşlandırma verilerini Power BI içeriğinde etkinleştirmek için yaşlandırma dönemi tanımları **Alacak hesapları parametreleri > koleksiyonlar > koleksiyon varsayılanları** bölümünde ayarlanmalıdır.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim

**Alacak ve tahsilatlar yönetimi** Power BI içeriği **Müşteri alacak ve tahsilatları** çalışma alanında gösterilir.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan raporlar

The **CustCollectionsBICrossCompany** Power BI içeriği, bir dizi ölçümden oluşan bir rapor içerir. Bu ölçümler grafikler, kutucuklar ve tablolar şeklinde görüntülenir. Aşağıdaki tablo **CustCollectionsBICrossCompany** Power BI içeriğindeki görselleştirmelere bir bakış sağlar.

| Rapor sayfası                 | Gözde canlandırma |
|-----------------------------|---------------|
| Tahsilatlar genel bakışı        | <ul><li>Vadesi geçmiş müşteriler</li><li>Müşteri fazla kredi limiti</li><li>DSO 30 gün</li><li>Açık servis talepleri</li><li>Vakanın kapatılacağı ortalama gün sayısı</li><li>Açık faaliyetler</li><li>Etkinliklerin kapatılacağı ortalama gün sayısı</li><li>Vade farkı dekontlarını aç</li><li>Tahsilatlar mektuplarını aç</li><li>Müşteri bekletme</li><li>Satış bekletme</li><li>Yaşlandırılmış bakiyeler</li><li>Tahsilatların durum tutarları</li><li>Tahsilatların kod tutarları</li><li>Sebebine göre silme nedeni</li><li>Bölgeye göre borç bakiyesi</li><li>Beklenen ödemeler</li></ul> |
| Kredi genel bakışı             | <ul><li>Vadesi geçmiş müşteriler</li><li>Kredi limiti ve kalan bakiye karşılaştırması</li><li>Kredi limitini aşan müşteriler kılavuzu</li><li>Şirket başına müşterilerin fazla kredi limiti</li><li>Kullanılan kredi ve toplam kredi limiti karşılaştırması</li><li>Kredi limiti ve Bölgeye göre kullanılan kredi karşılaştırması</li><li>Kredi notuna göre müşteriler</li></ul> |
| Kredi limiti                | <ul><li>Kredi limiti</li><li>Kredi limiti ayrıntıları</li><li>Müşteri başına kredi limiti</li><li>Müşteri grubu başına kredi limiti</li><li>Şirket başına kredi notuna göre kredi limiti</li><li>Kredi limiti ve bölgeye göre kullanılan kredi karşılaştırması</li></ul> |
| Müşteri fazla kredi limiti | <ul><li>Müşteri fazla kredi limiti</li><li>Müşteri fazla kredi limiti ayrıntısı</li><li>Şirket başına müşterilerin fazla kredi limiti</li><li>Müşteri grubu başına müşteri fazla kredi limiti</li><li>Bölgeye göre müşteri fazla kredi limiti</li></ul> |
| Vadesi geçmiş müşteriler          | <ul><li>Vadesi geçmiş müşteriler</li><li>Vadesini geçirmiş müşterilerin ayrıntıları</li><li>Şirket başına vadesi geçmiş müşteri</li><li>Müşteri grubu başına vadesi geçmiş müşteri</li><li>Bölgeye göre vadesi geçmiş müşteri</li></ul> |
| Yaşlandırılmış bakiyeler               | <ul><li>Yaşlandırılmış bakiyeler</li><li>Yaşlandırılmış bakiyelerin ayrıntıları</li><li>Şirket başına yaşlandırılmış bakiyeler</li><li>Müşteri grubu başına yaşlandırılmış bakiyeler</li></ul> |
| Beklenen ödemeler           | <ul><li>Beklenen ödemeler</li><li>Beklenen ödemelerin ayrıntıları</li><li>Şirkete göre beklenen ödemeler</li><li>Müşteri grubu başına beklenen ödemeler</li><li>Bölgeye göre beklenen ödemeler</li></ul> |
| Silmeler                  | <ul><li>Bölgeye göre silmeler</li><li>Silmelerin ayrıntıları</li><li>Ana hesaba göre silmeler</li><li>Şirkete göre silmeler</li><li>Müşteri grubuna göre silmeler</li><li>Bölgeye göre silmeler</li></ul> |
| Tahsilat durumu          | <ul><li>İhtilaflı</li><li>Ödeme taahhüdü yerine getirilmedi</li><li>Ödeme taahhüdü</li><li>Tahsilatların durum ayrıntıları</li><li>Tahsilatların durum tutarları</li><li>Açık servis talepleri</li><li>Açık faaliyetler</li></ul> |
| Tahsilatlar mektupları         | <ul><li>Tahsilat kodu tutarları</li><li>Tahsilatlar kodu tutar ayrıntıları</li><li>Şirkete göre tahsilat mektubu tutarı</li><li>Müşteri grubuna göre tahsilat mektubu tutarı</li><li>Bölgeye göre tahsilat mektup tutarı</li></ul> |

Tüm bu raporlardaki grafikler ve kutucuklar filtrelenebilir ve panoya sabitlenebilir. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano oluşturma ve yapılandırma](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Altta yatan veriyi Dışa aktar işlevini de görselleştirmede özetlenen altta yatan veriyi dışa aktarmak için kullanabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
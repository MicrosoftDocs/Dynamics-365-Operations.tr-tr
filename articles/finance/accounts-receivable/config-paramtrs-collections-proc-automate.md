---
title: Tahsilat işlemi otomasyonu için parametreleri yapılandırma
description: Bu makalede, otomatik tahsilat işlemlerini etkileyen parametreler açıklanmakta ve otomatik işlemin amaçlarınızı ve beklentilerinizi yansıtması için parametreleri ayarlamak üzere rehberlik sağlanmaktadır.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c5d0f801c47ef2d98d8ba410dc593bd7640839c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900056"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Tahsilat işlemi otomasyonu için parametreleri yapılandırma

[!include [banner](../includes/banner.md)]

Bu makalede, otomatik tahsilat işlemlerini etkileyen parametreler açıklanmakta ve otomatik işlemin amaçlarınızı ve beklentilerinizi yansıtması için parametreleri ayarlamak üzere rehberlik sağlanmaktadır. Otomatik tahsilat işlemleri hakkında bilgi için bkz. [Tahsilat işlemi otomasyonu](collections-process-automate.md).

## <a name="general"></a>Genel
Otomatik işlem başına toplu iş görevi sayısını belirlemek için **Toplu iş görevi başına müşteri yüzdesi**'nde bir sayı girin. Tahsilat mektubu eylem türü otomasyon sırasında mektubu deftere nakledecek şekilde **Tahsilat mektuplarını otomatik olarak deftere naklet** seçeneğini **Evet** olarak ayarlayın. Bir hesapta alınan tüm otomatik adımları görüntülemek için etkinlik dışı eylem türlerine ait etkinlikler oluşturmak ve kapatmak üzere **Otomasyonlar için faaliyetler oluştur** seçeneğini **Evet** olarak ayarlayın. **Tahsilat işlemi otomasyon geçmişinin tutulacağı gün sayısı**'nda saklanan tahsilat geçmişi gün sayısını tanımlayın. Fatura, tahsilat işleminin son adımına ulaştığında **Son işlem adımını etkinleştirdikten sonra faturayı hariç tut** seçeneği **Evet** olarak ayarlanırsa gelecekteki işlem otomasyonu eylem türlerini oluşturmak için kullanılmaz. Sonraki en eski fatura, tahsilat işlemi otomasyon eylemlerinin devam etmesini sağlamak için sonraki işlem otomasyonu adımını belirler. 

## <a name="payment-predictions"></a>Ödeme tahminleri
Sürüm 10.0.21'den itibaren, Finance Insights'ta bulunan Müşteri ödeme tahminleri bir faturanın zamanında, geç veya çok geç ödeneceğini belirtir. Finance Insights'ta bu kategorilerin her birini yapılandırabilirsiniz. Faturaların geç ödeneceği tahmin ediliyorsa faturanın vadesi dolmadan önce tahsilat işlemini başlatmak önemlidir. Bu tahminler, Tahsilat işlemi otomasyonları çalıştırıldığında tahsilat faaliyetleri oluşturmak için kullanılabilir. Faturanın geç ödenmesi olasılığına bağlı olarak tahsilat faaliyetleri oluşturmak için müşteri ödeme tahminlerini kullanmak üzere **Ödeme tahminlerini etkinleştir** seçeneğini **Evet** olarak ayarlayın. 

Müşteri ödeme tahminleri ve Finance Insights hakkında daha fazla bilgi için bkz. [Müşteri ödeme tahminleri](payment-insights-overview.md).

Müşteri ödeme tahminleri modeli çalıştırıldığında bu model zamanında, geç veya çok geç ödenen fatura tahmini için bir yüzde atar. Geç ödemenin beklendiği durumlarda Tahsilat işlemi otomasyonunu kullanarak tahsilat faaliyetlerini otomatik olarak başlatmak için bu bilgileri kullanabilirsiniz. **Alacak ve tahsilatlar > Tahsilatlar** altındaki **Müşteri başına ödeme tahminleri** veya **Hareket başına ödeme tahminleri** sayfalarında bu yüzdeleri görüntüleyebilirsiniz. 

Müşteri faturasının ortalama ödeme tahmini kıyaslama yüzdesinden daha küçükse faaliyet oluşturulmaz. Fatura tahmini kıyaslama yüzdesinden büyükse veya buna eşitse müşteri başına bir faaliyet oluşturulur. **Tahmin: Geç** için, tahsilat işlemi otomasyonunun tahsilat faaliyetleri oluşturması gereken zamana dair **Kıyaslama yüzdesi**'ni girin. Bu, geç ve çok geç tahminine dair toplam değerdir. Oluşturulan faaliyet için kullanmak veya yeni bir faaliyet oluşturmak üzere bir **İş belgesi şablonu** seçin. Bu; **Tür**, **Amaç** ve **Faaliyet kapatılana kadar geçecek gün sayısı**'nı tanımlar. Faaliyet oluşturulduğunda açıklama için varsayılan olacak **Notlar** girin. **Tahmin: Çok Geç** için, tahsilat işlemi otomasyonunun faturaları çok geç ödeyeceği tahmin edilen bir müşterinin tahsilat faaliyetlerini oluşturması gereken zamana dair **Kıyaslama yüzdesi**'ni girin. Oluşturulan faaliyet için kullanmak üzere bir **İş belgesi şablonu** seçin. Bu; **Tür**, **Amaç** ve **Faaliyet kapatılana kadar geçecek gün sayısı**'nı tanımlar. Faaliyet oluşturulduğunda açıklama için varsayılan olacak **Notlar** girin. 

### <a name="example"></a>Örnek
Geç kıyaslama yüzdesi %60 olarak ayarlanırsa. Müşteri ödeme tahminleri her fatura için çalıştırıldığında sistem zamanında, geç veya çok geç ödemeye dair bir yüzde tahmini atar. Faturanın geç ödeneceği ödeme tahmini %59'sa veya daha küçükse otomatik tahsilat işlemi tarafından fatura için tahsilat faaliyeti oluşturulmaz. Fatura için müşteri ödeme tahmini %60'tan yüksekse veya buna eşitse tahsilat işlemi otomasyonu sırasında tahsilat faaliyeti oluşturulur. 

> [!NOTE]
> Çok geç tahmini, geç ödenmesi tahmin edilen faturaları içerdiğinden geç tahmininden önce değerlendirilir. Tahsilat işlemi yalnızca faturanın geç ve çok geç kıyaslamalarına girmesi durumunda bir faaliyet oluşturur. Bu durumda sistem, çok geç yüksek öncelikli olduğundan çok geç faaliyetini ve iş belgesini kullanır. Önceden oluşturulmuş diğer eylemler ikinci kez oluşturulmaz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Dynamics 365 Supply Chain Management 10.0.21 önizlemesi (Ekim 2021)
description: Bu konuda, Dynamics 365 Supply Chain Management 10.0.21'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 08/02/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 517411512760374f1d1fd3b8ea3615563c47202c2e847569d00cb17a94657630
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012049"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Dynamics 365 Supply Chain Management 10.0.21 önizlemesi (Ekim 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management önizleme sürümü 10.0.21'deki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.960 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Ağustos 2021
- **Sürüm genel kullanılabilirliği (kendi kendini güncelleştirme):** Eylül 2021
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Ekim 2021

## <a name="known-deployment-issue"></a>Bilinen dağıtım sorunu
IaaS üzerinde sürüm 10.0.21'i dağıtırken aşağıdaki dağıtım uyarısını alabilirsiniz:

**Uyarı kodu:** 95017

**Uyarı iletisi:** [SetupDiagnostics] komut dosyası, VM'ye karşı yürütmede başarısız oldu

Dağıtım, uyarıya rağmen çalışır ancak Lifecycle Services'te (LCS) aşağıdaki bilinen sorunlar gerçekleşebilir:

-   **Ortam izleme** sayfasında, **Ayrıntılı sürüm bilgilerini görüntüle** bağlantısı görünmez. Bu nedenle, ortamınızda yüklü modüllerin belirli sürümlerini göremezsiniz. Bu veriler olmadan, düzeltmeleri uygulayan işlem, modül sürümü önkoşullarının karşılandığını doğrulamak için bu verileri kullandığından sonraki düzeltmeler başarısız olabilir. Üretimde oluşturulan PEAP/Önizlemeyi kullanmak veya düzeltmeleri uygulamak mümkün olmadığından etki minimum olmalıdır.
-   SQL ile İlgili Bilgiler altında **Ortam İzleme** sayfasındaki **Performans Ölçüleri** ve **Dizin Analizi** sekmelerinde veri görüntülenmez. Diğer tüm **Ortam İzleme** özellikleri istendiği gibi çalışır.
-   **Tam Sistem Tanılama** sayfasına erişilemez. Gecelik toplayıcı çalıştırmalarının durumuyla ilgili veriler ve kuralları tarafından algılanan sorunlar da gösterilmez.

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürümde yer alan özellikler yer almaktadır. *Özellik* sütunu, her bir özellik için resmi kullanıma sunma tarihlerini görebileceğiniz [kullanıma sunma planına](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) bağlantılar sağlar. *Ek bilgi* sütunu, ilgili belgelerin diğer ayrıntılrını ve/veya bağlantılarını sağlar.

Bu özelliklerin çoğunun kullanılabilmesi için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanılarak etkinleştirilmesi gerekir. Listelenen özelliklerden bazıları hala önizleme görünümünde, bazılaru genel olarak kullanılabilir durumda olabilir.

| Özellik alanı | Özellik | Daha fazla bilgi |
|---|---|---|
| Stok&nbsp;ve&nbsp;lojistik | [Dynamics 365 Supply Chain Management için Genel Stok Muhasebesi Eklentisi](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Genel Stok Muhasebesi giriş sayfası](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Stok&nbsp;ve&nbsp;lojistik | [Mahsup hesaplarla bağlantılı kodları kullanarak eldeki stok ayarlamalarını deftere nakletme](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Stok sayımı neden kodları](../warehousing/reason-codes-for-counting-journals.md) |
| Stok&nbsp;ve&nbsp;lojistik | [Satış teklifinin başvurulan veri dışarı aktarma ilkesi](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Teklifler tarafından başvurulan verilerdeki değişikliklerin bu tekliflerin (veya satırların) sonraki artımlı dışarı aktarma işlemine eklenmesine neden olup olmayacağını seçin. Bu tür teklifleri veya satırları eklemeyi seçmezseniz artımlı dışarı aktarma işlemleri daha hızlı çalışır.<br><br>Bu özellik, **Alacak hesapları parametreleri** sayfasına **Değişiklik izleme sırasında satış teklifi başvurulan verilerini atla** adlı bir ayar ekler. |
| Stok&nbsp;ve&nbsp;lojistik | [GS1 biçimi standartlarını kullanarak ambarda barkodları tarama](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | *Çok yakında*<!-- KFM: Add doc link when ready. --> |
| Stok&nbsp;ve&nbsp;lojistik | Kapalı teklif <!-- KFM: Add RP link when available --> | *Çok yakında*<!-- KFM: Add doc link when ready. --> |
| Stok&nbsp;ve&nbsp;lojistik | [İndirim yönetimi için kesinti ve fiili ağırlık geliştirmeleri](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Kesinti workbench'ini kullanarak kesintileri yönetme](../rebate-management/deduction-workbench.md )<br><br>[İndirimleri işleme, inceleme ve deftere nakletme](../rebate-management/process-review-post.md)<br><br>[İndirim yönetimi anlaşmaları](../rebate-management/rebate-management-deals.md) |
| Stok&nbsp;ve&nbsp;lojistik | [Ambar uygulaması adım yönergeleri](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | *Çok yakında*<!-- KFM: Add doc link when ready --> |
| Stok&nbsp;ve&nbsp;lojistik | [Son teslim alma maliyeti için molalar ve izleme güncelleştirmeleri](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Yerine koyma için izlemeyi güncelleştir](../landed-cost/update-tracking-putaway.md )<br><br>[Transitteki malları işleme](../landed-cost/in-transit-processing.md) |
| Master planlama | [Planlama Optimizasyonu için Negatif günler](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Gecikme toleransı (negatif günler)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde yer alan özellik iyileştirmeleri yer almaktadır. Bunların her biri varolan bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca geliştirmeler olduğundan, [sürüm planında](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmezler. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe). Bu özelliklerden herhangi birini kullanmak istiyorsanız, bunları [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'nde açıkça etkinleştirmeniz gerekir.

| Özellik alanı | Özellik&nbsp;yönetiminde&nbsp;özellik&nbsp;adı | Daha fazla bilgi |
|---|---|---|
| Maliyet yönetimi | Stok kapanışının ilerlemesiyle ilgili ayrıntılar | Bu önizleme özelliği, stok kapanışı ilerlemesinin ayrıntılı bir görünümünü sağlar. |
| Master planlama | (Önizleme) Planlama İyileştirme için önceliği temel alan MRP desteği | Bu Planlama Optimizasyonu önizleme özelliği, sipariş yenileme noktasıyla önceliği planlayarak yapılan master planlamayı etkinleştirir. Öne çıkan değişiklikler şunlardır: Satış siparişi satırlarında **Planlama önceliği** alanı, satınalma siparişi satırları, talep tahmini ve planlı siparişler; yeni bir karşılama kodu seçeneği; sipariş yenileme noktası için **Madde karşılama** alanı; planlama önceliği kurulumunu denetlemek için Master planlama kurulumu formları ve planlama önceliğini ayarlamak ve karşılamak için Planlama Optimizasyonu hesaplama mantığı. |
| Tedarik ve kaynak atama | İş akışında birden fazla satın alma talebi olduğunda genel bütçe ayırmalarının aşırı kullanımını engelle | Bu önizleme özelliği, kullanıcılar bir genel bütçe ayırma satırının kalan bakiyesini aşan satınalma taleplerini gönderip onayladığında hata denetimini iyileştirir. Bu, iş akışında çoklu satınalma talepleri olduğunda genel bütçe ayırmalarının aşırı tüketimini önlemeye yardımcı olur. |
| Üretim denetimi | Üretim katı yürütme arabiriminde seri, toplu iş ve plaka numaralarının tamamını göster | Bu özellik, üretim katı yürütme arabiriminde seri numara, toplu iş ve plaka numarası listelerini görüntülemek için iyileştirilmiş bir deneyim sağlar. Ekran, sınırlı sayıda karakter bulunan bir kart görünümünden tam değerleri göstermek için yeterli alan sağlayan bir liste görünümüne dönüşür. Liste ayrıca belirli numaraları arama olanağı da sağlar. |
| Ambar yönetimi | Yerine koyma işini ÖSB'lerden ayır | Bu özellik, bir ölçek biriminde (dağıtılmış karma topolojinin parçası olarak) ambar yönetimi iş yükü çalıştırırken önceden sevkiyat bildirimleri (ÖSB'ler) göndermek ve almak için gereklidir. Bu, yerine koyma işi hakkında bilgi toplamaya yönelik yeni bir veritabanı tablosu ekler. Daha önce bu bilgiler ayrıca ÖSB'ler kullanılan tablolarda depolanıyordu. |
| Ambar yönetimi | Karışık birimleri yerleştir | Sistemin, öğeleri karma birimler (kutular ve servis talepleri gibi) içeren konumlara yerleştirmesine olanak tanır. Her yerleştirme şablonu satırı için bu özellik, satırın öğeleri karışık veya tek birimli konumlara yerleştirmesi gerekip gerekmediğini seçmenize olanak tanır. |
| Ambar yönetimi | Sevk istasyonunda konteyner kapatma/yeniden açma için daha hızlı API kullanın | Bu önizleme özelliği etkinleştirildiğinde kapsayıcılarla ilgili stok hareketleri, el ile paketleme istasyonu işlemesi sırasında kapsayıcıları kapatma veya yeniden açma performansını iyileştiren yeni bir hafif işlem kullanarak oluşturulur. |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki yardım konularını yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Önceki bölümde listelendiği gibi, bunların bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez ancak var olan özelliklerden daha fazla bilgi almanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş konular |
|---|---|
| Master planlama | [Stok tahminleri](../master-planning/inventory-forecast.md) |
| Master planlama | [Planlama Optimizasyonu tarafından kullanılmayan parametreler](../master-planning/planning-optimization/not-used-parameters.md) |
| Master planlama | [Stok yenileme yöntemleri ve miktar değişikliği](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Master planlama | [Sonsuz kapasiteyle planlama](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Master planlama | [Plan geçmişini ve planlama günlüklerini görüntüleme](../master-planning/planning-optimization/plan-history-logs.md) |
| Ambar yönetimi | [Konteyner ambalaj stratejileri](../warehousing/container-packing-strategy-overview.md) |
| Ambar yönetimi | [Döngü sayımı örnek senaryoları](../warehousing/cycle-counting-scenarios.md) |
| Ambar yönetimi | [Gelen ÖSB'leri v2 veri varlığı aracılığıyla içeri aktarma](../warehousing/import-asn-v2-data-entity.md) |
| Ambar yönetimi | [Satış siparişleri ve transfer emirleri için fazla malzeme çekme](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Ambar yönetimi | [Dalga sırasında dalga etiketi yazdırmayı zamanlama](../warehousing/configure-task-based-wave-label-printing.md) |
| Ambar yönetimi | [Warehouse Management mobil uygulamasındaki yenilikler veya değiştirmeler](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.21 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.21 sürümü için platform güncelleştirmeleri (Ekim 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.21'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 ve sektör bulutları: 2021 sürüm dalgası 2 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2021 sürüm dalgası 2 planına](/dynamics365-release-plan/2021wave2/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) konusu Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) konusunda duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

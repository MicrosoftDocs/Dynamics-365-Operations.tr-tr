---
title: Dynamics 365 Finance'te kaldırılan veya kullanım dışı bırakılan özellikler
description: Bu makale, Dynamics 365 Finance'ten kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: kfend
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 4f2a1984d39713daa84f15422d7e0680b7f6c601
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219583"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance'te kaldırılan veya kullanım dışı bırakılan özellikler

[!include [banner](../includes/banner.md)]

Bu makale, Dynamics 365 Finance'ten kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!NOTE]
> Finans ve operasyon uygulamalarındaki nesneler hakkında ayrıntılı bilgiye [Teknik referans raporları](/dynamics/s-e/global/axtechrefrep_61) altından ulaşabilirsiniz. Finans ve operasyon uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Finance 10.0.29 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Transfer fiyatı vergi içeren stok transfer emirleri

[Transfer fiyatı vergi içeren stok transfer emirleri](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Kullanımı sonlandırma/kaldırma nedeni** | İyileştirilmiş işlevsellik olan [Hindistan için stok transfer emirleri](../../finance/localizations/apac-ind-stock-transfer.md) ile değiştirildi|
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları** | Uygulama |
| **Dağıtım seçeneği** | Tümü |
| **Çalıştırma Durumu** | Kullanım dışı bırakıldı: 2023 Nisan tarihinden sonra, **Transfer fiyatı vergi içeren stok transfer emirleri** işlevi artık hata düzeltmeleri ve güvenlik düzeltmeleriyle ilgili destek almayacaktır. Müşterilerin [Hindistan için stok transfer emirleri](../../finance/localizations/apac-ind-stock-transfer.md) iyileştirilmiş işlevini kullanmaları istenecektir. 2023 Ekim tarihinden sonra, **Transfer fiyatı vergi içeren stok transfer emirleri** işlevi artık kullanılamayacak ve müşterilerin geliştirilmiş işleve geçiş yapması istenecektir. |

## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Finance 10.0.26 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Finlandiya için satış vergisi raporu (raporlama kodlarına dayalı tasarım)

[Finlandiya için satış vergisi raporu](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni bir KDV beyannamesi tasarımı olan [Finlandiya için KDV beyannamesi](../localizations/emea-fin-vat-declaration.md) ile değiştirildi. |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kullanım dışı: 1 Mart 2023 tarihine kadar, Finlandiya için satış vergisi raporunu (Fince rapor düzeni) artık desteklememeyi planlıyoruz. Yeni **KDV beyannamesi TXT (FI**) ve **KDV beyannamesi Excel'i (FI)** Elektronik raporlama (ER) biçimleri, **Vergi beyanı** modeli altında sunulmaktadır. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Finance 10.0.24 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>İsveç için satış vergisi raporu (raporlama kodlarına dayalı tasarım)

[İsveç için satış vergisi raporları](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni bir KDV beyannamesi tasarımı olan [İsveç için KDV beyannamesi](../localizations/emea-swe-vat-declaration-sweden.md) ile değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kullanım dışı: 1 Aralık 2022 tarihine kadar, İsveç için satış vergisi raporunu (İsveç rapor düzeni) artık desteklememeyi planlıyoruz. Yeni **KDV beyannamesi XML'i (SE)** ve **KDV beyannamesi Excel'i (SE)** Elektronik raporlama (ER) biçimleri, **Vergi beyanı** modeli altında sunulmaktadır. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Avusturya için KDV beyannamesi (raporlama kodlarına dayalı tasarım)

[Avusturya için KDV beyannamesi ayrıntıları](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni bir KDV beyannamesi tasarımı olan [Avusturya için KDV beyannamesi](../localizations/emea-aut-vat-declaration-austria.md) ile değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kullanım dışı: 1 Aralık 2022 tarihine kadar, **KDV beyannamesi modeli** altındaki **KDV beyannamesi (AT)** Elektronik raporlama (ER) biçimini artık desteklememeyi planlıyoruz. **Vergi beyannamesi** modeli kapsamında, yeni **KDV beyannamesi XML (AT)** ve **KDV beyannamesi Excel (AT)** biçimleri tanıtıldı. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>Almanya için ELSTER beyannamesi (raporlama kodlarına dayalı tasarım)

[KDV beyanı](../localizations/emea-de-vat-declaration.md)</br>
[Almanya için elektronik vergi beyannamesini ayarlama](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[KDV beyannamesinin elektronik iletimi (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni bir KDV beyannamesi tasarımı olan [Almanya için KDV beyannamesi](../localizations/emea-deu-vat-declaration-germany.md) ile değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kullanım dışı: 1 Aralık 2022 tarihine kadar **Elster (DE)** ve **Elster modeli** elektronik raporlama (ER) biçimleri için desteği kaldırmayı planlıyoruz. **Vergi beyannamesi** modeli kapsamında, yeni **KDV beyannamesi XML (DE)** ve **KDV beyannamesi Excel (DE)** biçimleri tanıtıldı. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>Hollanda için OB beyannamesi (raporlama kodlarına dayalı tasarım)

[OB beyannamesi](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni bir KDV beyannamesi tasarımı olan [Hollanda için KDV beyannamesi](../localizations/emea-nl-vat-declaration-netherlands.md) ile değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kullanım dışı: 1 Aralık 2022 tarihine kadar **OB beyanı (NL)** ve **OB beyan modeli** elektronik raporlama (ER) biçimleri için desteği kaldırmayı planlıyoruz. **Vergi beyannamesi** modeli kapsamında, yeni **KDV beyannamesi XML (NL)** ve **KDV beyannamesi Excel (NL)** biçimleri tanıtıldı. |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Finance 10.0.20 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>"RTIR Sorgusu Fatura Ayrıntısı İsteği (HU)" Elekronik raporlama (ER) biçimi yapılandırması

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Macarca çevrimiçi faturalama sistemiyle birlikte çalışabilirlik elektronik ileti işleme işlemi dışında bırakıldı |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 15 Nisan 2022 itibarıyla, "RTIR Sorgusu Fatura Verileri İsteği (HU)" biçimi yapılandırması desteğini sonlandırmayı planlıyoruz. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>"Alman denetim dosyası çıktısı" biçimi altında "Fransız FEC denetim dosyası" Fransa için Elektronik raporlama (ER) biçimi

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni "FEC denetim dosyası (FR)" biçimiyle değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı bırakılma tarihi: 1 Mayıs 2022. "Almanca denetim dosyası çıktısı" biçimi altındaki "Fransız FEC denetim dosyası" Fransa için Elektronik raporlama (ER) biçimini artık desteklememeyi planlıyoruz. Bunun yerine, "Veri dışa aktarma modeli" altında yeni FEC denetim dosyası (FR) biçimini kullanıma sunuyoruz. |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Finance 10.0.17 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>Elektronik raporlama yapılandırmaları için depolama seçeneği olarak LCS deposu

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni Regulatory Configuration Service (RCS) genel deposu ile değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Dynamics 365 Finance, Supply Chain Management ve Project Operations ürünleri|
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Nisan 2022 tarihinden itibaren Microsoft Dynamics Lifecycle Services (LCS) deposunu Elektronik raporlama (ER) yapılandırmaları için bir depolama seçeneği olarak desteklememeyi planlıyoruz. Yeni Microsoft ER yapılandırmaları Global depodan özel olarak indirilmek üzere yayımlanacaktır. Global depoya Dynamics 365 ürünlerinden ve RCS'den erişilebilir. Daha fazla bilgi için bkz. [RCS'den ER yapılandırmalarını içe aktarma](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) ve [Regulatory Configuration Service - Lifecycle Services depolamanın kullanımdan kaldırılması](../localizations/rcs-lcs-repo-dep-faq.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Finance 10.0.16 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>Çek Cumhuriyeti için "KDV beyannamesi (CZ)" ve "Denetim ifadesi dışarı aktarma (CZ)" elektronik raporlama biçimleri

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni biçimlerle değiştirildi |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 22 Ocak 2022 tarihine kadar "KDV beyannamesi (CZ)", "Denetim ifadesi dışarı aktarma (CZ)" elektronik raporlama (ER) biçimleri için desteği kaldırmayı planlıyoruz. Bunun yerine yeni KDV beyannamesi XML'i (CZ), KDV beyanname Excel'i (CZ), KDV denetim ekstresi XML'i (CZ) biçimleri, "Vergi beyanı" modeli altında sunulmaktadır. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"Genel muhasebe defteri hareketi dışarı aktarma biçimi (BE)" Belçika için elektronik raporlama biçimi ve ilgili "Genel muhasebe defteri hareketi dışarı aktarma (BE)" modeli

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | "Standart Denetim Dosyası (SAF-T)" modeli altındaki yeni ER biçimi ile değiştirildi.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Aralık 2021'e kadar "Genel muhasebe defteri hareketi dışarı aktarma biçimi (BE)" Elektronik raporlama biçimi ve ilgili "Genel muhasebe defteri hareketi dışarı aktarma (BE)" modeli için sunduğumuz desteği kaldırmayı planlıyoruz. "Standart Denetim Dosyası (SAF-T)" modeli kapsamında, bunun yerine "Genel muhasebe veri modeli eşleme" ile birlikte yeni bir "Genel muhasebe veri dışarı aktarma (BE) biçimi" sunulmuştur. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>Birleşik Krallık için SSRS biçiminde "KDV 100" raporu

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | "Vergi beyannamesi modeli" kapsamında yeni ER biçimi - "KDV Beyannamesi Excel (UK)" biçimi ile değiştirilmiştir.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Aralık 2021'e kadar, SSRS biçimindeki "KDV 100 raporu" için sunduğumuz desteği kaldırmayı planlıyoruz. [MTD KDV özelliğinde](../localizations/emea-gbr-mtd-vat-integration.md) "Vergi beyanı modeli" kapsamında yeni bir "KDV Beyannamesi Excel (UK)" biçimi kullanıma sunulmuştur. |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Finance 10.0.15 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 için Internet Explorer 11 desteği kullanım dışı bırakılmıştır

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aralık 2020 itibarıyla geçerli olmak üzere, tüm Dynamics 365 ürünleri için Microsoft Internet Explorer 11 desteği kullanım dışı, bırakılacaktır ve Internet Explorer 11, Ağustos 2021'den sonra desteklenmeyecektir.<br><br>Bu, Internet Explorer 11 arabirimi aracılığıyla kullanılmak üzere tasarlanmış olan Dynamics 365 ürünlerini kullanan müşterileri etkileyecektir. Ağustos 2021'den sonra, Internet Explorer 11, bu tür Dynamics 365 ürünleri için desteklenmeyecektir. |
| **Başka bir özellikle mi değiştirildi?**   | Müşterilerin Microsoft Edge'e geçiş yapması önerilir.|
| **Etkilenen ürün alanları**         | Tüm Dynamics 365 ürünleri |
| **Dağıtım seçeneği**              | Tümü|
| **Durum**                         | Kaldırıldı. Internet Explorer 11 Ağustos 2021'den sonra desteklenmeyecektir.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance 10.0.12 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Kullanımdan kaldırılmadı: Lehçe SSRS raporları: Satış KDV kaydı, Satınalma KDV kaydı, AB Özeti KDV kaydı – Özellik referansı PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yasal olarak gerekli değildir.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet (KDV beyannamesiyle Standart Denetim Dosyası için Excel biçimi - JPK_VDEK) |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırılmadı: 27 Nisan 2021 itibarıyla, SSRS raporlarını desteklemeye devam etmeyi planlıyoruz: **Satış KDV kaydı, Satınalma KDV kaydı, AB Özet KDV kaydı – Özellik referansı PL-00014**. Bunun yerine, KDV beyannamesi ile Standart Denetim Dosyası (JPK_VDEK) için Excel biçiminde bir örnek kullanıma sunuldu. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance 10.0.11 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="norwegian-standard-main-accounts"></a>Norveç Standart ana hesapları

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeniden tasarla  |
| **Başka bir özellikle mi değiştirildi?**   | Evet (ER biçimi uygulamaya özgü parametreleriyle değiştirildi) |
| **Etkilenen ürün alanları**         | Uygulama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Nisan 2021 itibarıyla Standart ana hesaplarla ilgili işlevleri desteklememeyi planlıyoruz: Referans alanı, ilgili tablo, veri varlığı. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance 10.0.7 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>İş akışı isteği değişikliği iletişim kutusu artık kullanıcı seçimi açılan listesini içermiyor

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Hesap grupları seçimine sahip özellik olarak değiştirildi.  |
| **Başka bir özellikle mi değiştirildi?**   | Evet |
| **Etkilenen ürün alanları**         | İş Akışı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 1 Aralık 2020 itibarıyla, Hesap grupları seçimi içermeyen Çince fiş türleri kurulumunu desteklememeyi planlıyoruz. [10.0.7'deki Yenilikler](whats-new-changed-10-0-7.md)'de yeni tasarım hakkında daha fazla bilgi bulabilirsiniz. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) bakın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]


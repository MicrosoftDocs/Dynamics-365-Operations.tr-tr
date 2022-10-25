---
title: Invoice Capture çözümüne genel bakış
description: Bu makalede, Invoice Capture çözümü hakkında bilgi sağlanmaktadır.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691246"
---
# <a name="invoice-capture-solution"></a>Invoice Capture çözümü

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makale, dijital fatura görüntülerinden otomatik olarak satıcı faturaları oluşturan Invoice Capture çözümü hakkında bilgi sağlar.

Borç hesapları (AP) departmanı, alınan mal ve servislerle ilgili faturaları yönetir ve işler. AP muhasebecisi aşağıdaki nedenlerden dolayı satıcı faturalarındaki verileri doğrular:

- Dönem kapanışı sırasında ayarlamalar veya düzeltmeler gerekliyse fazladan çaba sarf edilmesini önlemek
- Satıcı faturalarını zamanında ödemek ve hata veya dolandırıcılık nedeniyle mali kaybı önlemek

Optik karakter tanıma (OCR), geçmişteki yıllarda farklı endüstriler tarafından yaygın olarak kullanılmaya başlanmıştır. Basılı metinlerin elektronik olarak düzenlenebilmesi, aranabilmesi, daha kompakt şekilde saklanabilmesi ve çevrimiçi olarak görüntülenebilmesi için dijital ortalama aktarılması artık yaygın bir uygulamadır. Dijital metin, bilişim hesaplama, makine çevirisi, metin okuma, anahtar verileri ve metin araştırma gibi makine işlemlerinde kullanılabilir.

Yapay zeka (AI) teknolojisinin evrimi, modern OCR çözümlerinin farklı satıcılardan gelen farklı fatura formatlarını fazla insan müdahalesi gerektirmeden okumasını sağlamaktadır. Eskisinden daha fazla şirket, manuel işlem yapmak yerine otomasyon yoluyla faturaları işleyerek çabadan tasarruf edebileceklerini ve doğruluğu artırabileceklerini kabul ediyor.

## <a name="system-landscape"></a>Sistem yatay

Aşağıdaki resimde, Invoice Capture çözümü ana bileşenleri ve adımları göstermektedir.

[![Invoice Capture çözümünde bileşenler ve adımlar.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Gerekli roller

Aşağıdaki tabloda, Invoice Capture çözümünü ayarlamak ve kullanmak için gerekli olan roller gösterilmektedir.

| Rol          | Eylemler | Sistemler | Rol adları |
|---------------|---------|---------|-----------|
| Yönetici | <ul><li>Microsoft Power Platform'da ortamları ayarlayın.</li><li>Microsoft Power Platform'da çözümleri dağıtın.</li><li>Dynamics 365 ve AI Builder arasındaki bağlantıları ayarlayın.</li><li>Azure Data Lake Storage konumları ayarlayın.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365 yöneticisi</li><li>Power Platform yöneticisi</li><li>Depolama Blobu veri sahibi</li></ul> |
| AI üreticisi      | <ul><li>Akışlara devam edin.</li><li>Özel AI modelleri oluşturun.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Vatandaş oluşturucuları</li></ul> |
| AP memuru      | <ul><li>Satıcı fatura hazırlama alanında inceleme yapın ve aksiyon alın.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Power Platform'da yeni AP memuru rolü</li></ul> |
| AP memuru      | <ul><li>Günlük operasyonları bir AP memuru olarak gerçekleştirin.</li><li>Satıcı faturası hazırlama alanına gidin.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Borç hesapları memuru</li></ul> |
  
Invoice Capture kurulumu hakkında daha fazla bilgi için bkz. [Invoice Capture kurma](../accounts-payable/install-invoice-capture.md).  

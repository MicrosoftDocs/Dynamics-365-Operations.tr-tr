---
title: Çevrimiçi satışlar ve ödemeler deftere naklediliyor
description: Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbc85b957e716d07d9073d889c47f157ea0ead01
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982305"
---
# <a name="posting-of-online-sales-and-payments"></a>Çevrimiçi satışlar ve ödemeler deftere naklediliyor

[!include [banner](../includes/banner.md)]

Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.

Çevrimiçi satış ve Ödemelerin deftere nakledilmesi iki aşamalı bir işlemdir.

- HQ içindeki çevrimiçi ticaret hareket verileri çekiliyor.
- HQ'da satış siparişleri oluşturmak için Siparişler eşitleniyor.

Çevrimiçi hareket verilerini çekme işlemi, P-iş ya el ile çalıştırarak ya da tekrarlayan bir toplu iş oluşturarak yapılabilir.

### <a name="manually-running-the-p-job"></a>P işi el ile çalıştırılıyor

1. Tüm iş yerleri > Perakende ve Ticaret BT'ye gidin.
2. Dağıtım planı'na tıklayın.
3. P-0001'i seçin.
4. Gerekiyorsa kanal veritabanı gruplarını ayarlayın.
5. Şimdi çalıştır üzerine tıklayın.
6. Evet'i tıklatın.

### <a name="scheduling-a-recurring-p-job"></a>Tekrarlayan bir P-iş planlama çizelgeleme

1. Tüm iş yerleri > Perakende ve Ticaret BT'ye gidin.
2. Dağıtım planı'na tıklayın.
3. P-0001'i seçin.
4. Toplu iş oluştur'a tıklayın.
5. Arka planda çalıştır'a tıklayın.
5. Toplu işlemi etkinleştirin.
6. Yineleme'ye tıklayın.
7. Bitiş tarihi yok seçeneğini seçin.
8. Sayım alanına, dakika cinsinden çalışma arasındaki aralığı girin. Bu genellikle 5-10 olabilir.
9. Tamam'a tıklayın.
10. Tamam'a tıklayın.

Siparişler, "Siparişleri eşitle" işini manuel olarak çalıştırarak veya yinelenen bir toplu iş oluşturarak eşitlenebilir.

### <a name="manually-running-order-synchronization"></a>El ile çalıştırılan siparişi eşitleme 

"Siparişleri Eşitle" işini bir kez el ile çalıştırmak için bu adımları izleyin.

1. Tüm çalışma alanları > Mağaza mali öğeleri'ne gidin.
2. Siparişleri eşitle'ye tıklayın.
3. Kuruluş hiyerarşisi alanında 'Bölgeye göre Mağazalar'ı seçin.
    * Belirli bir çevrimiçi mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.  
    * Seçiminizi eklemek için oka tıklayın.  
4. Arka planda çalıştır sekmesine tıklayın.
5. Toplu işlemini devre dışı bırakın
6. Yineleme'ye tıklayın.
7. Bu tarihten sonra biter seçeneğini belirleyin
8. Bu tarihten sonra biter alanına 1 girin.
9. Tamam'a tıklayın.
10. Tamam'a tıklayın.

### <a name="scheduling-recurring-order-synchronization"></a>Tekrarlanan sipariş eşitlemesini planlama

Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir. Bu yordam USRT demo veri şirketini kullanır.

1. Tüm çalışma alanları > Mağaza mali öğeleri'ne gidin.
2. Siparişleri eşitle'ye tıklayın.
3. Kuruluş hiyerarşisi alanında 'Bölgeye göre Mağazalar'ı seçin.
    * Belirli bir çevrimiçi mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.  
    * Seçiminizi eklemek için oka tıklayın.  
4. Arka planda çalıştır sekmesine tıklayın.
5. Toplu işlemi etkinleştirin
6. Yineleme'ye tıklayın.
7. Bitiş tarihi yok seçeneğini seçin.
8. Sayım alanına, dakika cinsinden çalışma arasındaki aralığı girin. Bu genellikle 2-20 olabilir
9. Tamam'a tıklayın.
10. Tamam'a tıklayın.

## <a name="data-entities-involved-in-the-process"></a>İşlemde yer alan veri varlıkları

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
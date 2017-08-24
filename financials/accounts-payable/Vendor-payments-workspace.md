---
title: "Satıcı ödemeleri çalışma alanı"
description: "Bu konu Satıcı ödemeleri çalışma alanı hakkında bilgiler sağlar. Satıcı ödemeleri çalışma alanı satıcı ödemelerinin işlenmesiyle ilgili bilgileri gösterir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: Shiva-Pandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: 4011a2383fe4556b730fa0b6353ba0b9773a4eec
ms.contentlocale: tr-tr
ms.lasthandoff: 06/14/2017

---

# <a name="vendor-payments-workspace"></a>Satıcı ödemeleri çalışma alanı

[!include[banner](../includes/banner.md)]

**Satıcı ödemeleri** çalışma alanı satıcı ödemelerinin işlenmesiyle ilgili bilgileri gösterir. Bu çalışma alanı bir **İşim** görünümü ve bir **Analiz** sayfası içerir. **İşim** görünümü özet kutucuklarını, satıcı hareketi ızgaralarını ve ilgili satıcı bilgilerini gösterir. **Analiz** sayfası, Microsoft Power BI yeteneklerini, satıcı ödemeleriyle ilgili görselleri göstermek için kullanır.

## <a name="my-work-view"></a>İşim görünümü

### <a name="summary-tiles"></a>Özet kutucukları

**Özet** bölümündeki kutucuklar ödeme bilgilerinizin durumuna genel bir bakış sağlar. Henüz deftere nakledilmeyen ödeme günlüklerini, vadesi geçmiş faturaları, tüm satıcıları ve beklemede olan satıcıları görebilirsiniz. **Özet** bölümünden, yeni bir ödeme işlemi oluşturabilirsiniz.

**Özet** bölümündeki bilgiler oturum açtığınız şirketle ilgilidir.

### <a name="vendor-transactions-grids"></a>Satıcı hareketleri ızgaraları

**Satıcı hareketleri** bölümü vadesi geçen faturaları ve kapatılmamış ödemeleri gösteren ızgaralar içerir. **Vadesi geçmiş faturalar** ızgarasından seçilen bir fatura için kapama geçmişini görebilirsiniz. **Kapatılmamış ödemeler** ızgarasından seçilen bir fatura için kapama geçmişini görebilir ve bir faturayı kapatabilirsiniz.

Merkezi ödeme elemanları şirket seçmek için her kılavuzun üstünde görünen filtreyi kullanabilir. Izgara, yalnızca merkezi ödeme elemanının görüntüleme hakkına sahip olduğu merkezi ödeme kuruluş hiyerarşisinde tanımlanan şirketleri gösterecek şekilde filtrelenir.

**Satıcı hareketleri** bölümündeki **Hareketleri bul** sekmesi bir satıcı hareketini aramanıza olanak sağlar.

### <a name="related-information"></a>İlgili bilgiler

Çalışma alanının **İlgili bilgiler** bölümündeki bağlantıları kullanarak **Satıcı yaşlandırma** raporunu ve **Tarihe göre ödeme özeti** raporunu görüntüleyebilirsiniz.

## <a name="analytics-page"></a>Analiz sayfası

**Analiz** sayfası vadesi geçen veya vadesi gelecekte olan satıcı faturaları gibi önemli ölçümleri sağlar. Bu sayfa dokuz rapor sayfası içerir. Bir sayfa genel bakış sağlarken ve diğer sekiz sayfa Borç hesapları ödeme ölçümleri hakkında ayrıntılı bilgiler sağlar.

Aşağıdaki tablo, her bir rapor sayfasında kullanılabilen görselleştirmeleri gösterir.

| Rapor sayfası | Gözde canlandırma |
|-------------|---------------|
| Satıcı ödemeleri özeti | <ul><li>Vadesi geçmiş faturalar</li><li>Vadesi bugün olan faturalar</li><li>Alınan iskontolar / kayıp iskontolar</li><li>Nakit iskontosu tarihine göre vadesi gelecekte olan faturalar</li><li>Vade tarihine göre vadesi gelecekte olan faturalar</li><li>Geç ödenen faturalar ile zamanında ödenen faturalar</li><li>Ödeme iş akışı ataması</li><li>Müşteri / satıcı bakiyesi</li><li>Ödemesi beklemede olan açık faturalar</li></ul> |
| Vadesi geçmiş faturalar | <ul><li>Vadesi geçmiş faturalar</li><li>Vadesi geçmiş faturaların ayrıntıları</li><li>Toplam açık fatura</li><li>Satıcı grubuna göre vadesi geçmiş faturalar</li><li>Şirkete göre vadesi geçmiş faturalar</li></ul> |
| Vadesi bugün olan faturalar | <ul><li>Vadesi bugün olan faturalar</li><li>Vadesi bugün olan faturaların ayrıntıları</li><li>Şirkete göre vadesi bugün olan faturalar</li><li>Satıcı grubuna göre vadesi bugün olan faturalar</li></ul> |
| Alınan iskontolar / kayıp iskontolar | <ul><li>Alınan iskontolar / kayıp iskontolar</li><li>Alınan iskontolar / kayıp iskonto ayrıntıları</li><li>Şirkete göre alınan iskontolar / kayıp iskonto</li><li>Satıcı grubuna göre alınan iskontolar / kayıp iskonto</li></ul> |
| Gelecekte ödenecek faturaları | <ul><li>Gelecekte ödenecek faturaları</li><li>Gelecekte ödenecek faturaların ayrıntıları</li><li>Şirkete göre gelecekte ödenecek faturalar</li><li>Satıcı grubuna göre gelecekte ödenecek faturalar</li><li>Nakit iskontosu tarihine göre vadesi gelecekte olan faturalar</li><li>Vade tarihine göre vadesi gelecekte olan faturalar</li></ul> |
| Geç ödenen faturalar | <ul><li>Vade tarihinden sonra ödenen faturalar</li><li>Vade tarihinden sonra ödenen faturaların ayrıntıları</li><li>Şirkete göre Vade tarihinden sonra ödenen faturalar</li><li>Satıcı grubuna göre vade tarihinden sonra ödenen faturalar</li><li>Geç ödenen faturalar ile zamanında ödenen faturalar</li></ul> |
| Ödeme iş akışı | <ul><li>Satıcı ödeme iş akışı örnekleri</li><li>Onaylayana göre satıcı ödeme iş akışı örnekleri</li><li>Şirkete göre satıcı ödeme iş akışı örnekleri</li><li>Onaylana göre iş akışındaki ortalama gün sayısı</li></ul> |
| Müşteri / satıcı bakiyesi | <ul><li>Müşteri / satıcı bakiyesi</li><li>Şirkete göre satıcı / müşteri bakiyesi</li><li>Satıcı / müşteri bakiyesi ayrıntıları</li></ul> |
| Ödemesi beklemede olan faturalar | <ul><li>Ödemesi beklemede olan faturalar</li><li>Ödemesi beklemede olan faturaların ayrıntıları</li><li>Şirkete göre ödemesi beklemede olan faturalar</li><li>Satıcı grubuna göre ödemesi beklemede olan faturalar</li></ul> |


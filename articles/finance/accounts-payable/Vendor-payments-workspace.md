---
title: Satıcı ödemeleri çalışma alanı
description: Bu makale Satıcı ödemeleri çalışma alanı hakkında bilgiler sağlar. Satıcı ödemeleri çalışma alanı satıcı ödemelerinin işlenmesiyle ilgili bilgileri gösterir.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.assetid: ''
ms.search.form: VendPaymentWorkspace
ms.openlocfilehash: 13d86c037dccf23725bc8bdce268ed9fada3c5cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288616"
---
# <a name="vendor-payments-workspace"></a>Satıcı ödemeleri çalışma alanı

[!include [banner](../includes/banner.md)]

**Satıcı ödemeleri** çalışma alanı satıcı ödemelerinin işlenmesiyle ilgili bilgileri gösterir. Bu çalışma alanı bir **İşim** görünümü ve bir **Analiz** sayfası içerir. **İşim** görünümü özet kutucuklarını, satıcı hareketi ızgaralarını ve ilgili satıcı bilgilerini gösterir. **Analiz** sayfası, Microsoft Power BI yeteneklerini, satıcı ödemeleriyle ilgili görselleri göstermek için kullanır.

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI içeriğini görüntülemek için kurulum gerekiyor

Verilerin **Satıcı ödemeleri** Power BI görsellerinde görüntülenmesi için aşağıdaki kurulumun tamamlanması gereklidir.
1. **Sistem para birimi** ve **Sistem döviz kuru**'nu ayarlamak için **Sistem yönetimi > Kurulum > Sistem Paramatreleri**'ne gidin.
2. Etkin döneme atanan mali takvim tarihlerini doğrulamak için **Genel muhasebe > Takvimler > Mali takvimler**'e gidin.
3. **Muhasebe Para Birimi** ve **Döviz Kuru Türü**'nü ayarlamak için **Genel Muhasebe > Ayarlar > Muhasebe**'ye gidin 
4. Hareket para birimleri ile muhasebe para birimi, muhasebe para birimi ve sistem para birimi arasındaki döviz kurlarını tanımlayın. Bunu yapmak için **Genel Muhasebe > Para Birimleri > Para birimi döviz kurları**'na gidin.
5. **VendPaymentBIMeasureV2** toplam ölçümünü yenilemek için **Sistem yönetimi > Ayarlar > Varlık Deposu**'na gidin.

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


|            Rapor sayfası            |                                                                                                                                                                                Gözde canlandırma                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Satıcı ödemeleri özeti      | <ul><li>Vadesi geçmiş faturalar</li><li>Vadesi bugün olan faturalar</li><li>Alınan iskontolar / kayıp iskontolar</li><li>Nakit iskontosu tarihine göre vadesi gelecekte olan faturalar</li><li>Vade tarihine göre vadesi gelecekte olan faturalar</li><li>Geç ödenen faturalar ile zamanında ödenen faturalar</li><li>Ödeme iş akışı ataması</li><li>Müşteri / satıcı bakiyesi</li><li>Ödemesi beklemede olan açık faturalar</li></ul> |
|         Vadesi geçmiş faturalar         |                                                                                             <ul><li>Vadesi geçmiş faturalar</li><li>Vadesi geçmiş faturaların ayrıntıları</li><li>Toplam açık fatura</li><li>Satıcı grubuna göre vadesi geçmiş faturalar</li><li>Şirkete göre vadesi geçmiş faturalar</li></ul>                                                                                              |
|        Vadesi bugün olan faturalar         |                                                                                                         <ul><li>Vadesi bugün olan faturalar</li><li>Vadesi bugün olan faturaların ayrıntıları</li><li>Şirkete göre vadesi bugün olan faturalar</li><li>Satıcı grubuna göre vadesi bugün olan faturalar</li></ul>                                                                                                          |
| Alınan iskontolar / kayıp iskontolar |                                                                             <ul><li>Alınan iskontolar / kayıp iskontolar</li><li>Alınan iskontolar / kayıp iskonto ayrıntıları</li><li>Şirkete göre alınan iskontolar / kayıp iskonto</li><li>Satıcı grubuna göre alınan iskontolar / kayıp iskonto</li></ul>                                                                              |
|      Gelecekte ödenecek faturaları       |                                                 <ul><li>Gelecekte ödenecek faturaları</li><li>Gelecekte ödenecek faturaların ayrıntıları</li><li>Şirkete göre gelecekte ödenecek faturalar</li><li>Satıcı grubuna göre gelecekte ödenecek faturalar</li><li>Nakit iskontosu tarihine göre vadesi gelecekte olan faturalar</li><li>Vade tarihine göre vadesi gelecekte olan faturalar</li></ul>                                                  |
|        Geç ödenen faturalar         |                                                         <ul><li>Vade tarihinden sonra ödenen faturalar</li><li>Vade tarihinden sonra ödenen faturaların ayrıntıları</li><li>Şirkete göre Vade tarihinden sonra ödenen faturalar</li><li>Satıcı grubuna göre vade tarihinden sonra ödenen faturalar</li><li>Geç ödenen faturalar ile zamanında ödenen faturalar</li></ul>                                                          |
|         Ödeme iş akışı          |                                                                                <ul><li>Satıcı ödeme iş akışı örnekleri</li><li>Onaylayana göre satıcı ödeme iş akışı örnekleri</li><li>Şirkete göre satıcı ödeme iş akışı örnekleri</li><li>Onaylana göre iş akışındaki ortalama gün sayısı</li></ul>                                                                                |
|    Müşteri / satıcı bakiyesi     |                                                                                                                   <ul><li>Müşteri / satıcı bakiyesi</li><li>Şirkete göre satıcı / müşteri bakiyesi</li><li>Satıcı / müşteri bakiyesi ayrıntıları</li></ul>                                                                                                                    |
|    Ödemesi beklemede olan faturalar     |                                                                                         <ul><li>Ödemesi beklemede olan faturalar</li><li>Ödemesi beklemede olan faturaların ayrıntıları</li><li>Şirkete göre ödemesi beklemede olan faturalar</li><li>Satıcı grubuna göre ödemesi beklemede olan faturalar</li></ul>                                                                                          |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

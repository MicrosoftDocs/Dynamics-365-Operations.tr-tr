---
title: "Genel muhasebe günlük tabloları"
description: "Bu makale, finansal günlükleriniz için ayarlayabileceğiniz günlük türleri açıklanmaktadır. Microsoft Dynamics 365 for Finance and Operations'ta kullanabileceğiniz günlükleri ayarlamak için **Günlük adları** sayfasını kullanın."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9f8fc40f199b83a9e0cb36ce905163c3ed547057
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="ledger-journal-types"></a>Genel muhasebe günlüğü türleri

[!INCLUDE [banner](../includes/banner.md)]

Bu makale, finansal günlükleriniz için ayarlayabileceğiniz günlük türleri açıklanmaktadır. Microsoft Dynamics 365 for Finance and Operations'ta kullanabileceğiniz günlükleri ayarlamak için **Günlük adları** sayfasını kullanın.

| Günlük türü:                      | Amaç                       | Bu sayfada hareketleri girin                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Tahsisat                        | Bir tahsisat günlüğünde tahsisat hareketleri oluşturun. Bir tahsisat günlüğü oluşturmadan önce, **Genel muhasebe tahsisat kuralı** sayfasında tahsisat kuralı oluşturmalısınız.      | Tahsisat talebini işleme koy             |
| Onay                          | Onaylanan satıcı faturalarını uygun genel muhasebe hesaplarına nakledin.  | Fatura onay günlüğü                                       |
| Banka çeki ters işlemi               | Gönderilen çeke ters işlem uygulayın. Bu günlük tipi kullanmak için **ödeme iptalleri için inceleme işlemi kullan** seçeneğini **nakit ve Banka yönetimi parametreleri** sayfasında seçin.   | Çek ters işlemleri, Ödeme ters kaydı                   |
| Banka depozit makbuzu iptali    | Bir havale makbuzu iptal edin. Bu günlük tipi kullanmak için **Havale makbuzu ödeme iptalleri için inceleme işlemi kullan** seçeneğini **nakit ve Banka yönetimi parametreleri** sayfasında seçin.   | Havale makbuzu ödeme iptalleri            |
| Bütçe                            | Bütçe tahsisatlarını işleyin. Bu günlük tipi kullanmak için **bütçe tahsisatı etkinleştir** seçeneğini **genel muhasebe parametreleri** sayfasında seçin. Bütçe günlük girişleri **tanımları nakil** sayfasında tanımlanan genel muhasebe hesaplarını temel alan bilgiler içerir.                                                        |                                                                |
| Müşteri kabullü kambiyo senedi  | Kambiyo senetleri için müşteri kabul hareketlerini oluştur.             | Kambiyo senedi günlüğünü düzenle, kambiyo senetlerini yeniden düzenle |
| Müşteri banka havalesi          | Kuruluşunuzun Bankasına gönderilen bir kambiyo senedini Havale dosyası oluşturun. Bu günlük tipi kullanmak için **otomatik kapatma** seçeneğini **Alacak** **hesapları parametreleri** sayfasında temizleyin.            | Havale                                                     |
| Müşteriye keşide edilen kambiyo senedi    | Müşteriye düzenlenen kambiyo senedi hareketleri oluşturun. Bu günlük tipi kullanmak için **Faturaları naklederken düzenleme günlüğünü otomatik olarak oluştur ve naklet** seçeneğini **ödeme yöntemleri - müşteriler** sayfasında temizleyin.   | Düzenlenen kambiyo senetleri günlüğü                                  |
| Müşteri ödemesi                  | Müşteri ödeme hareketlerini oluşturun.                             | Ödeme günlüğü             |
| Müşteri protestolu kambiyo senedi | Müşteri protestolu kambiyo senedi hareketlerini oluşturun.                    | Protestolu kambiyo senetleri günlüğü                               |
| Müşteriye yeniden düzenlenen kambiyo senedi  | Müşteriye yeniden düzenlenen kambiyo senedi hareketleri oluşturun.                     | Yeniden düzenlenen kambiyo senetleri günlüğü                                |
| Müşteri tarafından ödenen kambiyo senedi  | Müşteri tarafından ödenen kambiyo senedi hareketleri oluşturun.                       | Kambiyo senetleri kapatma günlüğü                                |
| Günlük                             | Günlük hareketleri yevmiye defterinde oluşturun.                          | Genel günlük                                                |
| Eleme                       | Bir eleme günlüğünde eleme hareketleri oluşturun. Bu günlük tipi kullanmak için **mali eleme işlemi için kullan** ve **mali konsolidasyon sürecinde kullan** seçeneklerini **tüzel kişilikler** sayfasında seçin. Bu günlük tipi kullanmadan önce **genel muhasebe eliminasyon kuralı** sayfasında genel muhasebe eliminasyon kuralı oluşturmanız gerekir. | Eleme                                                    |
| Sabit kıymet bütçesi                | Sabit kıymetler bütçe kayıt girişleri oluşturun.                                                                                                                                                                                                                                                                                                                 | Sabit kıymet bütçesi                                             |
| Fatura defteri                  | Satıcı faturaları hakkındaki temel bilgileri kaydedin.                                                                                                                                                                                                                                                                                                           | Fatura defteri                                               |
| Bordro tediyesi              | Bordro üzerindeki ifadelere dayalı ödemeleri gönderin. Bu günlükte hareketleri el ile giremezsiniz. Ödeme deyimleri oluşturmanız ve sonra bu deyimleri ödeme göndermek gerekir.                                                                                                                                                              |                                                                |
| Dönemsel                          | Periyodik günlük için Dönemsel hareketleri oluşturun.                                                                                                                                                                                                                                                                                                      | Periyodik günlükler                                              |
| Sabit kıymetleri naklet                 | Sabit kıymet nakil hareketleri gönderin.                                                                                                                                                                                                                                                                                                                              | Sabit kıymetler                                                   |
| Proje - giderler                | Proje gider hareketlerini oluşturun.                                                                                                                                                                                                                                                                                                                        | Gider                                                        |
| İstatistik hareketleri            | İstatistik hareketleri oluşturun.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Satıcı banka havalesi            | Kuruluşunuzun Bankasına gönderilen bir senet Havale dosyası oluşturun.                                                                                                                                                                                                                                                                      | Havale günlüğü                                             |
| Satıcıya ödeme               | Satıcıya ödeme hareketleri oluşturun.                                                                                                                                                                                                                                                                                                                    | Ödeme günlüğü                                                |
| Satıcıya düzenlenen senet       | Ödeme yöntemi olarak Satıcı senetlerini düzenleyin. Bu günlük tipi kullanmak için **Faturaları naklederken düzenleme günlüğünü otomatik olarak oluştur ve naklet** seçeneğini **ödeme yöntemleri - satıcılar** sayfasında temizleyin.                                                                                                                                          | Düzenlenen senet günlüğü                                   |
| Satıcı fatura havuzu hariç bırakma nakli | Henüz geçici varış hesabına nakledilmeyen satıcı fatura hareketleri oluşturun.                                                                                                                                                                                                                                                             | Deftere nakledilen ayrıntılar hariç satıcı faturası havuzu                  |
| Satıcı fatura havuzu               | Satıcı fatura havuz hareketleri oluşturun.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Satıcı faturası kaydı          | Defterde olan satıcı faturalarını nakledin.                                                                                                                                                                                                                                                                                                                 | Fatura günlüğü                                                |
| Satıcı yeniden düzenlenen senedi     | Daha önce bankanız tarafından kabul edilip ödenmiş bir senedi yeniden düzenleyin.                                                                                                                                                                                                                                                                      | Yeniden düzenlenen senet günlüğü                                 |
| Satıcıya ödenen vadeli senet     | Satıcıya ödenen vadeli senet hareketleri oluşturun.                                                                                                                                                                                                                                                                                                          | Senet kapatma günlüğü                                 |







---
title: Ambar performansı Power BI içeriği
description: Bu konu, Ambar performansı Power BI içeriğinde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.
author: Mirzaab
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c5d07cb9fbb32a2d9b8be11179dbba00ee73d28b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850217"
---
# <a name="warehouse-performance-power-bi-content"></a>Ambar performansı Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, **Ambar performansı** Microsoft Power BI içeriğinde nelerin bulunduğunu açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="overview"></a>Genel bakış

**Ambar performansı** Power BI içeriği, ambar ve operasyon yöneticilerinin önemli gelen, giden ve stok ölçümlerini izleyebilmeleri için oluşturulmuştur. Sisteminizden Ambar yönetimi, ürün ve diğer hareket verilerini kullanır ve hem ambar performansının toplam görünümünü hem de satıcılar, ürün grupları ve ürünler ile tesisler ve ambarlar için çözümleme sağlar.

Ambar yöneticileri, **Ambar performansı** Power BI içeriğini aşağıdaki üç alanı ölçmek için kullanabilirler:

- **Gelen performans** - Bir satıcının bir müşteri gereksinimlerine karşı ne kadar iyi performans gösterdiğini ölçer (başka bir deyişle, teslimat performansını ölçer) ve yerine koyma performansını ölçer, böylece işçi veya öğeleri kapsayan sorunları bir dönem boyunca belirleyebilirsiniz. Hangi satıcıların zamanında, erken veya geç teslimat yaptığını bilmeniz önemlidir, böylece satıcı performansının genel yerine koyma performansını nasıl etkilediğini anlayabilirsiniz. Üzerinde anlaşılmış olan tarih aralığının dışında teslimat yapan bir satıcı, beklenmeyen iş ve artan ortalama yerine koyma zamanı nedeniyle ambara ek yük bindirebilir.
- **Sevkiyat performans** - Ambarın müşterilere tam ve zamanında sevkiyat yapıp yapmadığını ölçmek (başka bir deyişle, dışarı giden sevkiyat ve teslimat performansının ölçümü), böylece ürünleri, siteleri, ambarları veya adanmış müşterileri kapsayan sorunları tanımlayabilirsiniz. Çeşitli şehirlere veya bölgelere geç teslimat yaptığınızı bulursanız, nakliye veya hesap yönetimine daha fazla dikkat etmeniz gerekebilir.
- **Yerleşim stok doğruluğu** - Stok doğruluğu, önemli bir dahili ambar iş zekâsıdır (BI). Genel olarak ne kadar doğru sayım yaptığınızı belirlemeniz çok önemlidir. Ancak, maddeleri doğru konumlarda depolama konusunda ne kadar isabetli olduğunuzu belirlemek ve tutarsız verilerin altını çizebilmeniz de önemlidir, böylece maddeler için daha iyi konumlar bulabilir veya belirli maddelerde toplam sayımları başlatabilirsiniz. (Şu anda, maddeye dayalı yeni sayım işlevi bir düzeltme olarak sunulmaktadır.) Bu Power BI içeriğini, eldeki stokun konuma göre doğruluğunu bulmakta kullanıyorsanız, mağazalarınızdaki hırsızlığı da tespit edebilirsiniz. Ayrıca, herhangi bir konumun eldeki stokun, kuruluş kaynak planlaması (ERP) verisinden farklı olduğunu da belirleyebilirsiniz. Bu konumlar çok büyük olabilir veya sayılmaları imkansız olabilir. Alternatif olarak, bazı fiziksel konumlandırmalar hatalı olabilir, bu yüzden de tek bir madde türünü eldeki veri ile eşleştirilmiş tutmak zordur.

## <a name="accessing-the-power-bi-content-pack"></a>Power BI içerik paketine erişmek
**Ambar performansı** Power BI içeriği **Ambar performansı** sayfasında gösterilir (**Ambar yönetimi** \> **Sorgular ve raporlar** \> **Ambar performansı analizi** \> **Ambar performansı**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan ölçümler
**Ambar performansı** Power BI içeriği, bir raporu içerir. Bu rapor grafikler, döşemeler ve tablolar ile görselleştirilen bir dizi ölçüm kümesinden oluşur. Aşağıdaki tablo **Ambar performansı** Power BI içeriğindeki görselleştirmelere bir bakış sağlar.

| Rapor sayfası                 | Grafikler                                   | Açıklama |
|-----------------------------|------------------------------------------|-------------|
| Gelen Performans         | Toplam yerine koymalar                          | Belirli bir sürede işlenen, toplam yerine koyma iş hatları. |
| Gelen Performans         | Ortalama yerine koyma süresi                    | Maddelerin kaydından son yerine koyma işlenene kadar, işlenen tüm satınalma siparişleri için yerine koyma ortalama süresi, saat cinsinden. |
| Gelen Performans         | Erken alındı                           | Erken alınan satınalma siparişi satırlarının sayısı. |
| Gelen Performans         | Zamanında alındı                         | Zamanında alınan satınalma siparişi satırlarının sayısı. |
| Gelen Performans         | Gecikmeyle alındı                            | Geç alınan satınalma siparişi satırlarının sayısı. |
| Gelen Performans         | Satıcı tarafından zamanında                        | Bir satıcı veya satıcı grubu tarafından erken, geç veya zamanında alınan satınalma siparişi satırlarının bir görünümü. |
| Gelen Performans         | Limandan stoka ortalama yerine koyma (saat) | Zaman içerisinde limandan stoka yerine koymanın ortalaması, saat cinsinden. |
| Gelen Performans         | İşçiye göre ortalama yerine koyma               | Bir işçinin, satınalma sipariş satırlarının yerine koymasını işlerken geçirdiği sürenin saat cinsinden ortalaması. |
| Gelen Performans         | Satıcı tarafından saatlik ortalama yerine koyma          | Satıcı veya satıcı grubu tarafından, saat cinsinden ortalama yerine koyma süresi. |
| Gelen Performans         | Ürüne göre saatlik ortalama yerine koyma         | Madde veya madde grubu tarafından, saat cinsinden ortalama yerine koyma süresi. |
| Konum stok doğruluğu | Toplam sayı                              | Belirli bir süre için işlenen sayım iş hatlarının sayısı. |
| Konum stok doğruluğu | Uyuşmazlık oranı                         | Belirli bir sürede sayılan tüm hatların yüzdesi olarak toplam uyuşmazlık oranı. |
| Konum stok doğruluğu | Uyuşmazlık olmadan sayım                | İşlenen sayım iş hatlarının toplam sayısından, herhangi bir uyuşmazlık olmadan işlenen hatların sayısı. |
| Konum stok doğruluğu | Zaman içinde sayılan maddeler                  | Zaman içinde uyumsuzluk olan veya olmadan sayılan maddelerin yüzdesi. |
| Konum stok doğruluğu | %'den büyük madde miktarı uyumsuzluğu | Belirli bir yüzdeyi geçen uyumsuzluğa sahip sayım satırlarının bir tablo görünümü. Tablo; konumlar, maddeler, ortalama uyumsuzluk, sayılan toplam sayım iş hatları, konum için uyumsuzluğa sahip sayım satırlarının sayısı, sayılan ortalama miktar, sayılacak toplam miktar beklentisi ve sayılan gerçek madde miktarına dair bilgiler içermektedir. |
| Konum stok doğruluğu | İşçiye göre madde sayımı                     | İşçilerin sayım performansı. Performans, uyumsuzluğa sahip olan veya olmayan sayım iş satırlarının yüzdesi ile ifade edilir. |
| Konum stok doğruluğu | Siteye / ambara göre madde sayımı           | Siteye veya ambara göre, uyumsuzluk dahil veya hariç işlenmiş sayım iş satırlarına göre sayım performansı. |
| Konum stok doğruluğu | Ürüne göre uyumsuzluk oranı              | Sayım performansı için uyumsuzluk oranı. Oran, madde veya madde grubu başına işlenen sayım işi hattının yüzdesi olarak ifade edilir. |
| Sevkiyat performansı        | Sevk edilen satırlar                            | Belirli bir süre içinde sevk edilen sevkiyat hatlarının toplam sayısı. |
| Sevkiyat performansı        | Erken                                    | Erken sevk edilen sevkiyat hatlarının yüzdesi. |
| Sevkiyat performansı        | Zamanında                                  | Zamanında sevk edilen sevkiyat hatlarının yüzdesi. |
| Sevkiyat performansı        | Geç                                     | Geç sevk edilen sevkiyat hatlarının yüzdesi. |
| Sevkiyat performansı        | Zamana göre sevkiyatlar                      | Belirli bir dönem boyunca zamanında, erken veya geç sevk edilen sevk satırlarının yüzdesi. Bir trend çizgisi, vaktinde sevk edilen hatların trendini gösterir. |
| Sevkiyat performansı        | Şehre göre geç sevkiyat                     | Geç sevkiyatlardan etkilenen şehirler ve bölgelerin haritalı görselleştirmesi. |
| Sevkiyat performansı        | Ürüne göre sevkiyat                       | Madde veya madde grubuna göre erken, zamanında veya geç sevkiyatın yüzdesi. |
| Sevkiyat performansı        | Müşteriye göre sevkiyat                      | Müşteri veya müşteri grubuna göre erken, zamanında veya geç sevkiyatın yüzdesi. |
| Sevkiyat performansı        | Tesise / ambara göre sevkiyat              | Tesis veya ambara göre erken, zamanında veya geç sevkiyatın yüzdesi. |

## <a name="understanding-the-data-model-and-calculations"></a>Veri modellerini ve hesaplamalarını anlama
Aşağıdaki veriler **Ambar performansı** Power BI içeriğindeki rapor sayfalarını doldurmak için kullanılır. Bu veri, Varlık mağazasında hazırlanan toplam ölçümler olarak sunulur. Varlık mağazası, analizler için en iyi duruma getirilmiş bir Microsoft SQL Server veritabanıdır. Daha fazla bilgi için, bkz. [Varlık mağazası ile Power BI tümleştirmesine genel bakış](power-bi-integration-entity-store.md).

Aşağıdaki önemli toplam ölçümler, içeriğin temeli olarak kullanılır.

| Rapor sayfası                 | Grafikler                                   | Tablolar                                | Hesaplama açıklamaları |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Gelen Performans         | Toplam yerine koymalar                          | WHSWorkLine                           | İş türünün **yerine koyma** olduğu iş satırlarının sayısı. |
| Gelen Performans         | Ortalama yerine koyma süresi                    | WHSWorkLine                           | İş satırlarının maksimum zamanının toplamının, iş satırlarının maksimum zamanının sayısına bölünmesi; burada iş satırları maksimum zamanı, işin oluşturulması ve kapanış tarih arasındaki zamandır. |
| Gelen Performans         | Erken alındı                           | WHSWorkLine                           | İşin oluşturulma tarihinin, kullanılan teslimat tarihinden daha erken olduğu iş satırlarının toplamı. Onaylanmış teslimat tarihi ayarlanmamışsa, varsayılan teslimat tarihini kullanın. |
| Gelen Performans         | Zamanında alındı                         | WHSWorkLine                           | İşin oluşturulma tarihinin, kullanılan teslimat tarihine eşit olduğu iş satırlarının toplamı. Onaylanmış teslimat tarihi ayarlanmamışsa, varsayılan teslimat tarihini kullanın. |
| Gelen Performans         | Gecikmeyle alındı                            | WHSWorkLine                           | İşin oluşturulma tarihinin, kullanılan teslimat tarihinden daha sonra olduğu iş satırlarının toplamı. Onaylanmış teslimat tarihi ayarlanmamışsa, varsayılan teslimat tarihini kullanın. |
| Gelen Performans         | Satıcı tarafından zamanında                        | WHSWorkLine                           | Erken alınan, Zamanında alınan ve Geç alınan (bkz. bu tablonun başındaki açıklamalar.) |
| Gelen Performans         | Limandan stoka ortalama yerine koyma (saat)   | WHSWorkLine                           | Ortalama yerine koyma süresi (Bu tablonun başındaki tanıma bakınız.) |
| Gelen Performans         | İşçiye göre ortalama yerine koyma               | WHSWorkLine                           | Ortalama yerine koyma süresi (Bu tablonun başındaki tanıma bakınız.) |
| Gelen Performans         | Satıcı tarafından saatlik ortalama yerine koyma          | WHSWorkLine                           | Ortalama yerine koyma süresi (Bu tablonun başındaki tanıma bakınız.) |
| Gelen Performans         | Ürüne göre saatlik ortalama yerine koyma         | WHSWorkLine                           | Ortalama yerine koyma süresi (Bu tablonun başındaki tanıma bakınız.) |
| Konum stok doğruluğu | Toplam sayı                              | WHSWorkLineCycleCount                 | Mutlak uyumsuzluk miktarının 0 (sıfır) veya daha fazlasına eşit olduğu döngü sayısı. |
| Konum stok doğruluğu | Uyuşmazlık oranı                         | WHSWorkLineCycleCount                 | Uyumsuzluğa sahip döngü sayılarının sayısı, toplam sayıya bölünmüş olarak. Bir döngü sayısı, mutlak uyumsuzluk miktarı 0'dan (sıfır) fazla ise uyumsuzluğa sahip olarak kabul edilir. |
| Konum stok doğruluğu | Uyuşmazlık olmadan sayım                | WHSWorkLineCycleCount                 | Mutlak uyumsuzluk miktarının 0'dan (sıfır) daha fazlasına eşit olduğu döngü sayısı. |
| Konum stok doğruluğu | Uyumsuzluk ile sayım                   | WHSWorkLineCycleCount                 | Mutlak uyumsuzluk miktarının 0'a (sıfır) eşit olduğu döngü sayısı. |
| Konum stok doğruluğu | Zaman içinde sayılan maddeler                  | WHSWorkLineCycleCount                 | Uyumsuzluk olmayan döngü ve uyumsuzluğa sahip döngü (Bu tablonun başındaki açıklamalara bakın.) |
| Konum stok doğruluğu | %'den büyük madde miktarı uyumsuzluğu | WHSWorkLineCycleCount                 | Ortalama uyumsuzluk, mutlak uyumsuzluk miktarının, mutlak uyumsuzluk miktarının 0'dan (sıfır) fazla olanına bölünmesidir. Ortalama uyumsuzluk miktarı, mutlak uyumsuzluk miktarının, mutlak uyumsuzluk miktarının 0'dan (sıfır) fazlasının ortalamasıdır. Uyumsuzluğa, Toplam sayıma, Beklenen miktara ve Toplam miktarın madde ve konuma göre gruplandığı sayılan miktara göre (bu tablonun başındaki açıklamalara bakınız). |
| Konum stok doğruluğu | İşçiye göre madde sayımı                     | WHSWorkLineCycleCount                 | Uyumsuzluk olmayan döngü ve uyumsuzluğa sahip döngü (Bu tablonun başındaki açıklamalara bakın). |
| Konum stok doğruluğu | Siteye / ambara göre madde sayımı           | WHSWorkLineCycleCount                 | Uyumsuzluk olmayan döngü ve uyumsuzluğa sahip döngü (Bu tablonun başındaki açıklamalara bakın). |
| Konum stok doğruluğu | Ürüne göre uyumsuzluk oranı              | WHSWorkLineCycleCount                 | Uyuşmazlık oranı (Bu tablonun başındaki açıklamaya bakınız). |
| Sevkiyat performansı        | Sevk edilen satırlar                            | SalesLine               | Satış hatlarının sevk edildiği satış hatlarının sayısı. |
| Sevkiyat performansı        | Erken                                    | CustPackingSlipOnTimeStatus           | Teslimat tarihi durumunun **1 (Erken)** olduğu satış satırları. Erken, sevk irsaliyesinin sevkiyat tarihinin, satış satırı üzerindeki onaylanan sevk tarihinden erken olduğu anlamına gelir. Onaylanan sevk tarihi ayarlanmamışsa, talep edilen sevk tarihini kullanın. |
| Sevkiyat performansı        | Zamanında                                  | CustPackingSlipOnTimeStatus           | Teslimat tarihi durumunun **2 (Zamanında)** olduğu satış satırları. Zamanında, sevk irsaliyesinin sevkiyat tarihinin, satış satırı üzerindeki onaylanan sevk tarihine eşit olduğu anlamına gelir. Onaylanan sevk tarihi ayarlanmamışsa, talep edilen sevk tarihini kullanın. |
| Sevkiyat performansı        | Geç                                     | CustPackingSlipOnTimeStatus           | Teslimat tarihi durumunun **3 (Geç)** olduğu satış satırları. Geç, sevk irsaliyesinin sevkiyat tarihinin, satış satırı üzerindeki onaylanan sevk tarihinden geç olduğu anlamına gelir. Onaylanan sevk tarihi ayarlanmamışsa, talep edilen sevk tarihini kullanın. |
| Sevkiyat performansı        | Zamana göre sevkiyatlar                      | SalesLine CustPackingSlipOnTimeStatus | Satış satırının tüm miktarının sevk edildiği, tümüyle sevk edilen siparişler, artı Erken, Zamanında ve Geç (bu tablonun başındaki açıklamalara bakınız). |
| Sevkiyat performansı        | Şehre göre geç sevkiyat                     | CustPackingSlipOnTimeStatus           | Geç (Bu tablonun başındaki açıklamalara bakınız). |
| Sevkiyat performansı        | Ürüne göre sevkiyat                       | CustPackingSlipOnTimeStatus           | Erken, Zamanında ve Geç (bkz. bu tablonun başındaki açıklamalar). |
| Sevkiyat performansı        | Müşteriye göre sevkiyat                      | CustPackingSlipOnTimeStatus           | Erken, Zamanında ve Geç (bkz. bu tablonun başındaki açıklamalar). |
| Sevkiyat performansı        | Tesise / ambara göre sevkiyat              | CustPackingSlipOnTimeStatus           | Erken, Zamanında ve Geç (bkz. bu tablonun başındaki açıklamalar). |

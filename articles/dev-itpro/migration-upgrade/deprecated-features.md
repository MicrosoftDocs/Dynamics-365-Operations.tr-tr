---
title: "Kaldırılan veya artık kullanılmayan özellikler"
description: "Bu konu kaldırılmış veya kaldırılması planlanan özellikleri açıklar."
author: sericks007
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d6b7b1219974cb5de1a625d87c3bce2a4439470b
ms.openlocfilehash: ea24d6d63edc6f3bb1bf4a99d24d348af0d6cdbf
ms.contentlocale: tr-tr
ms.lasthandoff: 10/01/2018

---

# <a name="removed-or-deprecated-features"></a>Kaldırılan veya kullanımına son verilen özellikler

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 for Finance and Operations'dan kaldırılmış veya kullanımına son verilmiş özellikler açıklanmaktadır.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!Note]
> Platform güncelleştirmesi 8 ile Dynamics 365 for Finance and Operations Temmuz 2017 sürümünden başlayarak, kaldırılan veya kullanımına son verilen her özellik için dağıtımların türü not edilmiştir. Bu konuda söz edilen önceki tüm sürümler yalnızca desteklenen bulut dağıtımlarıdır.

> [!Note]
> Finance and Operations içindeki nesneler hakkında ayrıntılı bilgiye [Teknik referans raporları](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) altından ulaşabilirsiniz. Finance and Operations'ın her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="dynamics-365-for-finance-and-operations-81-with-platform-update-20"></a>Dynamics 365 for Finance and Operations 8.1, platform güncelleştirmesi 20 ile

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Muavin defteri günlüğü hesap girişleri için toplu transfer kuralları
Zaman uyumlu aktarım modunu genel muhasebe parametrelerinde kaldırılıyor.  Bu mod, halihazırda transfer için seçenek olarak mevcut olan Asenkron ve zamanlanan toplu iş ile değiştiriliyor. 

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sistem performansı üzerindeki etkisi nedeniyle zaman uyumlu seçeneği kaldırıyoruz. |
| **Başka bir özellikle mi değiştirildi?**   | Asenkron ve zamanlanan toplu iş seçenekleri, zaman uyumlu yerine kullanılacak seçeneklerdir.   |
| **Etkilenen ürün alanları**         | Genel muhasebe, Borç hesapları, Alacak Hesapları, satın alma, gider    |
| **Dağıtım seçeneği**              | Tümü  |
| **Durum**                         | Kullanımı sonlandırıldı - İşlevin kaldırılması hedeflenen zaman aralığı 10.0 sürümüdür.|

### <a name="electronic-reporting-for-russia"></a>Rusya için Elektronik raporlama
.txt ve .xml dosya biçimlerini bildirimler için yapılandırma özelliği. 

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Elektronik raporlama ile değiştirildi. |
| **Başka bir özellikle mi değiştirildi?**   | Evet. |
| **Etkilenen ürün alanları**         | Genel Muhasebe |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Dynamics 365 for Finance and Operations 8.1'de platform güncelleştirmesi 20 ile kaldırıldı. |

### <a name="financial-reports-generator-for-russia"></a>Rusya için finansal raporlar oluşturucusu
Muhasebe ve vergi raporları için veri toplamak ve XLS ve DOC rapor şablonlarına dışa veri aktarmak için bir araç. İşlevsel parçalar: XLS ve DOC rapor şablonlarına, sorgularına ve sabit gereksinimlerine veri dışa aktarma kaldırıldı. 

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kaldırılan bölümler Elektronik Raporlama ile değiştiriliyor. |
| **Başka bir özellikle mi değiştirildi?**   | Evet. Finansal raporlar kullanıcı ayarı arabirimi, GL hesapları veya vergi kayıtları için veri toplama kuralları ayarlamak için kullanılmalıdır. Muhtelif veri türlerine, sabit gereksinimlere ve sorgu benzeri veri toplama kurallarına veri dışa aktarma, Elektronik raporlamada yapılandırılmalıdır. |
| **Etkilenen ürün alanları**         | Genel muhasebe. |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Dynamics 365 for Finance and Operations 8.1'de platform güncelleştirmesi 20 ile kaldırıldı. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Rusya için iletişim kanalları üzerinden elektronik raporlama göndermek için dış sağlayıcılar ile tümleştirme
Dışa aktarma özelliğini klasörüne bildirimlerinin elektronik dosyalar daha ayrıntılı olarak elektronik raporlama durumuna geri alma resmi sağlayıcı göndermek için oluşturulur.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Elektronik iletiler yapılandırılabilir özelliği ile değiştirildi. |
| **Başka bir özellikle mi değiştirildi?**   | Evet.  |
| **Etkilenen ürün alanları**         | Genel Muhasebe, Vergi |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Dynamics 365 for Finance and Operations 8.1'de platform güncelleştirmesi 20 ile kaldırıldı. |

## <a name="dynamics-365-for-finance-and-operations-80-with-platform-update-15"></a>Dynamics 365 for Finance and Operations 8.0, platform güncelleştirmesi 15 ile
Bu sürümle hiçbir özellik kaldırılmamış veya kullanım dışı bırakılmamıştır. Platform Güncelleştirmesi 15 toplu güncelleştirmedir ve Platform Güncelleştirmesi 13, Platform Güncelleştirmesi 14 ve Platform Güncelleştirmesi 15'deki yeni veya değiştirilmiş özellikleri içerir.

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Dynamics 365 for Finance and Operations, Enterprise edition 7.3, platform güncelleştirmesi 12 ile

### <a name="personalized-product-recommendations"></a>Kişiselleştirilmiş ürün önerileri 
15 Şubat 2018 tarihinden itibaren perakendeciler artık satış noktası cihazındaki (POS) kişiselleştirilmiş ürün önerilerini görüntüleyemeyecektir. Daha fazla bilgi için bkz. [Kişiselleştirilmiş ürün önerileri](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).  

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu özelliği daha iyi bir algoritma ve daha yeni perakende odaklı yeteneklerle yeniden tasarladığımızdan ürün öneri hizmetinin geçerli sürümünü kaldırıyoruz.  |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Ancak, 2018 yılı bahar aylarından sonra yeni bir öneri hizmetinden yararlanmak için bu özelliği geri getirmeyi planlıyoruz.   |
| **Etkilenen ürün alanları**         | POS'ta kişiselleştirilmiş ürün önerileri.                                                    |
| **Dağıtım seçeneği**              | Tümü                                                                                      |
| **Durum**                         |15 Şubat 2018 itibarıyla kaldırıldı. Bu, Dynamics 365 for Operations 1611 ve sonraki sürümleri çalıştıran müşterileri etkiler.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Elektronik raporlama (ER) işlev listesi genişletmesi
ER ifade oluşturucuda kullanılmak üzere özel işlevler sağlama olasılığı (daha fazla bilgi için bkz. [Elektronik raporlama işlev listesini genişletme](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) artık desteklenmemektedir. ER API'larındaki değişiklikler nedeniyle, ER ifade oluşturucudan yerleşik işlevleri çağırmak için kullanılan API dahili hale gelmiştir ve artık genişletilemez.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Kod kapama girişimi  |
| **Başka bir özellik ile değiştirildi?**   | Hiçbiri. Yeni bir yerleşik işlev gerektiğinde, yeni genişletme talebinin ER altyapısı ekibine bildirilmesi gerekir.<br><br>İstenen işlev ER ekibi tarafından geliştirilirken geçici bir çalışma olarak, talep edilen mantık özel uygulama sınıfı yöntemi olarak programlanabilir. Bu yönteme, eklenen ve özel uygulama sınıfına başvuruda bulunan **Application\Class** türündeki ER veri kaynağının bir özelliği olarak ER ifadesinden erişilebilir.  |
| **Etkilenen ürün alanları**         | Elektronik raporlama çerçevesi                                                      |
| **Dağıtım seçeneği**              | Tümü                                                                                      |
| **Durum**                         | Dynamics 365 for Finance and Operations, Enterprise edition 7.3 sürümünden itibaren kaldırılmıştır.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Madde grubuna göre stok ve stok boyutu yaşlandırmasına göre stok raporları

Bu iki rapor artık Finance and Operations'da desteklenmemektedir. Bunun yerine, **Stok yaşlandırma** raporu kullanıcı deneyimini geliştirmek için kullanılabilir.

|   |  |
|--------------|-----------------------|
| **Kaldırılma nedeni**       | Tekrar eden işlevsellik  |
| **Başka bir özellik ile değiştirildi?** | Evet. İki rapor **Stok yaşlandırma** raporuyla değiştirilmiştir.     |
| **Etkilenen ürün alanları**       | Stok yönetimi, Maliyet yönetimi        |
| **Dağıtım seçeneği**        | Tümü|
| **Durum**                       | Kullanımı sonlandırıldı: Her iki raporun da menü öğeleri 7.3 sürümünde kaldırıldı. Ancak, raporların kodu üründe kaldı. Plan kodu sonraki bir sürümde kaldırmaktır. |

### <a name="power-bi-content-packs-available-on-appsource"></a>AppSource'ta bulunan Power BI içerik paketleri
[Microsoft AppSource](https://appsource.microsoft.com)'ta yayımlanmış olan **Maliyet yönetimi**, **Mali performans** ve **Perakende kanalı performansı** içerik paketleri, Microsoft Power BI'deki ürün güncelleştirmelerinin sonucu olarak kullanımdan kaldırıldı. PowerBI.com'da bu içerik paketlerini dağıtmak için kullanılan sistem yönetim formlarının kullanımı da Finance and Operations'ta sonlandırıldı.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Microsoft Power BI'deki ürün güncelleştirmeleri. |
| **Başka bir özellik ile değiştirildi?**   | [AppSource](https://appsource.microsoft.com) sitesinde bulunan **Yönetimi maliyet**, **Mali performans** ve **Perakende kanal performansı** içerik paketleri, veritabanı düzeyinde çözüm tümleştirmelerine olanak tanıyan analiz uygulamalarıyla değiştirilmektedir. Analiz uygulamaları hakkında daha fazla bilgi için bkz. [Çalışma alanlarına katıştırılmış Power BI](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Etkilenen ürün alanları**         | Maliyet yönetimi, Finans ve Perakende                                                                                               |
| **Dağıtım seçeneği**              | Yalnızca bulut(PowerBI.com ile tümleştirme şirket içi dağıtımlarda desteklenmez.)                                                                                                            |
| **Durum**                         | Kullanımı sonlandırıldı: İşlevin kaldırılması hedeflenen zaman aralığı 2018 yılı 2. çeyreğidir.    |

### <a name="standard-ui-in-data-management-workspace"></a>Veri yönetimi çalışma alanında standart kullanıcı arabirimi

Veri yönetimindeki standart kullanıcı arabirimi, veri yönetimi çalışma alanını ziyaret ettiklerinde kullanıcılara sunulan varsayılan kullanıcı arabirimi olan eski kullanıcı arabirimidir.

|   |  |
|------------------|-------------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni kullanıcı arabiriminde yeni kullanıcı deneyimleri sunmak için çalışıyoruz.             |
| **Başka bir özellik ile değiştirildi?**   | *Gelişmiş görünümler* adlı yeni kullanıcı arabirimi eski kullanıcı arabiriminin yerini aldı.            |
| **Etkilenen ürün alanları**         | Veri yönetimi çalışma alanı                                                     |
| **Dağıtım seçeneği**              | Tümü                                                                           |
| **Durum**                         | Kullanımı sonlandırıldı: İşlevin kaldırılması hedeflenen zaman aralığı 2018 yılı 2. çeyreğidir. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Hindistan için Tüketim, Satış Vergisi, Hizmet Vergisi

Bu vergiler Hindistan GST içine eklendi.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Kullanımı sonlandırma veya kaldırma nedeni**       | Bu vergiler Hindistan GST içine eklendi.                          |
| **Başka bir özellik ile değiştirildi?**            | Hindistan GST                                                              |
| **Etkilenen ürün alanları**                  | Vergi                                                                     |
| **Dağıtım seçeneği**                       | Tüm modüller                                                   |
| **Durum**                                  | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |    

### <a name="file-validation-utility-fvu-for-india"></a>Hindistan için Dosya Doğrulama Yardımcı Programı (FVU)

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Kullanımı sonlandırma veya kaldırma nedeni**       | Müşteri kullanım eksikliği                                                  |
| **Başka bir özellik ile değiştirildi?**            | Hayır                                                                      |
| **Etkilenen ürün alanları**                  | Hindistan stopaj vergisi                                                  |
| **Dağıtım seçeneği**                       | Tüm modüller                                                                    |
| **Durum**                                  | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |        

### <a name="tdstcs-certificate-for-india"></a>Hindistan için TDS/TCS sertifikası

Kullanıcılar bu formu resmi devlet portalından indirebilir.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Kullanımı sonlandırma veya kaldırma nedeni**       | Müşteri kullanım eksikliği                                                  |
| **Başka bir özellik ile değiştirildi?**            | Hayır                                                                      |
| **Etkilenen ürün alanları**                  | Hindistan stopaj vergisi                                                  |
| **Dağıtım seçeneği**                       | Tüm modüller                                                                   |
| **Durum**                                  | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Hindistan için ihracat/ithalat (EXIM) girişimi şeması


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Kullanımı sonlandırma veya kaldırma nedeni**       | Müşteri kullanım eksikliği                                                  |
| **Başka bir özellik ile değiştirildi?**            | Hayır                                                                      |
| **Etkilenen ürün alanları**                  | İçe ve dışa aktar                                                       |
| **Dağıtım seçeneği**                       | Tüm modüller                                                                    |
| **Durum**                                  | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Kişiselleştirilmiş ürün önerileri 
15 Şubat 2018 tarihinden itibaren perakendeciler artık satış noktası cihazındaki (POS) kişiselleştirilmiş ürün önerilerini görüntüleyemeyecektir. Daha fazla bilgi için bkz. [Kişiselleştirilmiş ürün önerileri](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/personalized-product-recommendations).  

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu özelliği daha iyi bir algoritma ve daha yeni perakende odaklı yeteneklerle yeniden tasarladığımızdan ürün öneri hizmetinin geçerli sürümünü kaldırıyoruz.  |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Ancak, 2018 yılı bahar aylarından sonra yeni bir öneri hizmetinden yararlanmak için bu özelliği geri getirmeyi planlıyoruz.   |
| **Etkilenen ürün alanları**         | POS'ta kişiselleştirilmiş ürün önerileri.                                                    |
| **Dağıtım seçeneği**              | Tümü                                                                                      |
| **Durum**                         |15 Şubat 2018 itibarıyla kaldırıldı. Bu, Dynamics 365 for Retail 7.2 ve sonraki sürümleri çalıştıran müşterileri etkiler. |


## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Dynamics 365 for Finance and Operations, Enterprise edition Temmuz 2017, platform güncelleştirmesi 8 ile

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Muhasebe ve raporlama para birimleri için para birimi dönüştürme

Muhasebe ve raporlama para birimleri için para birimi dönüştürme, avro çıktığı zaman kullanıma sunulmuştur.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tüzel kişilik kopyalama işlevselliğinin bir değişiklik olarak sınırlı kullanımı ve eklenmesi.      |
| **Başka bir özellikle mi değiştirildi?**   | Hayır, ancak Tüzel kişilik kopyalama ve Yapılandırmalar özellikleri, temel gereksinimlerini değiştiren bir şirkete taşımayı kolaylaştırmak için eklendi. |
| **Etkilenen ürün alanları**         | Mali yönetim     |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |


### <a name="warehouse-mobile-devices-portal"></a>Ambar mobil cihazlar portalı

Ambar mobil cihazlar portalı (WMDP), yerinde kendi kedine dağıtım için amaçlanmış bir tek bileşendir. Bu bileşen artık Finance and Operations'da desteklenmemektedir. Kullanıcı deneyimini iyileştiren bir yerel uygulama, WMDP'nin işlevinin yerini almıştır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tekrar eden işlevsellik.       |
| **Başka bir özellik ile değiştirildi?**   | Evet. Bu özellik Finance and Operations - Ambarlama ile değiştirilmiştir. Kurulum ve önkoşulları hakkında daha fazla bilgi için, bkz. [Microsoft Dynamics 365 for Finance and Operations - Ambarlama için kurulum ve yapılandırma](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Etkilenen ürün alanları**         | Ambar yönetimi, Taşıma yönetimi     |
| **Dağıtım seçeneği**              | Ambar mobil cihazlar portalı (WMDP), yerinde kendi kedine dağıtım için amaçlanmış bir tek bileşendir.               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>El ile eşleştirme için gelişmiş banka mutabakatı eşleştirme kuralı

Bir mutabakat kuralı, belgeler el ile mutabakat çalışma sayfasında eşleştirildiğinde bir banka belgesini seçmek ve işaretlemek için kullanılmıştır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sınırlı kullanım.                                                                         |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Sütun filtreleme yetenekleri, mutabakat için belgeleri bulmakta kullanılmalıdır. |
| **Etkilenen ürün alanları**         | Nakit ve banka yönetimi                                                               |
| **Dağıtım seçeneği**              | Tümü                                                                                    |
| **Durum**                         | Temmuz 2017 itibarıyla kaldırıldı.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611, platform güncelleştirmesi 3 ile

### <a name="aeb-payment-formats-for-spain"></a>İspanya için AEB ödeme biçimleri

Consejo Superior Bancario ödeme biçimleri, müşteri ödemeleri ve satıcı ödemeleri için havale dosyalarını bankaya göndermek amacıyla kullanılıyordu. Bu biçimlerin içeriği Asociación Española de Banca tarafından belirlenmiştir. Cuaderno 19, 32, 58, 34'ü kapsar.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                                  |
| **Başka bir özellik ile değiştirildi?**   | Evet, İspanya için ISO20022 Alacak transferi ve Otomatik ödeme biçimleri |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları                                    |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Litvanya için banka ödemeleri transferi

Litvanya için banka ödeme transferleri, Ödeme transferi (LT) dışa aktarma biçimi kullanarak oluşturuluyor ve yazdırılıyordu. Litvanya pazarı 2005'te birleştirilmiş elektronik bankacılık sistemi olan LİTAS'ı kullanmaya başladı.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Litvanya için ISO20022 Alacak transferi ödeme biçimi     |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Norveç için BBS Direkte Remittering ödeme biçimleri

BBS Direkte Remittering ödeme biçimleri, müşteri ödeme tahsilatını dışa aktarmayı (otomatik ödeme) ve geri dönen iletiyi içe aktarmayı içerir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.  |
| **Başka bir özellik ile değiştirildi?**   | Norveç için AvtaleGiro müşteri ödeme biçimi otomatik ödeme iletileri oluşturmak için kullanılabilir. Geri dönen iletiyi içe aktarma gelecek sürümlerde uygulanacaktır. |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>İspanya için Hesap Planı aracı

Bu araç, İspanya'da bir hesap planında büyük değişiklikler yapılması gerektiğinde kullanılır. Kullanıcılar Microsoft Excel'de veya metin biçiminde yeni bir hesap planını ve ayrıca mali tabloları içe aktarabilir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sınırlı kullanım                                                  |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                             |
| **Etkilenen ürün alanları**         | Genel muhasebe                                                 |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="dom80-payment-format-for-belgium"></a>Belçika için Dom80 ödeme biçimi

Ödeme tahsilatı (otomatik ödeme) için eski Belçika ödeme biçimi.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                          |
| **Başka bir özellik ile değiştirildi?**   | Evet, Belçika için ISO 20022 Otomatik ödeme biçimi         |
| **Etkilenen ürün alanları**         | Alacak hesapları                                            |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>İsviçre için DTA/EZAG ödeme biçimleri

DTA/EZAG biçimleri, referans numarası ile ilişkili oldukları için ESR sistemine tümleştirilmiştir. Referans numarası zorunlu olmadığından bu biçimler her türlü satıcı ödemesini işlemek için kullanılabilir. Bu biçimler “Postfinance” dışında bir konumda banka hesabı bulunan şirketler tarafından kullanılır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, İsviçre için ISO20022 Alacak transferi ödeme biçimi   |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Avusturya için EDIFACT DIRDEB ödeme biçimi

Ödeme tahsilatı (otomatik ödeme) için EDIFACT-DIRDEB ödeme biçimi.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                          |
| **Başka bir özellik ile değiştirildi?**   | Evet, Avusturya için ISO 20022 Otomatik ödeme biçimi         |
| **Etkilenen ürün alanları**         | Alacak hesapları                                            |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="edivat-for-belgium"></a>Belçika için EDIVAT

EDIVAT güvenli posta yoluyla elektronik beyanname için geçersiz bir Belçika standardıdır. Microsoft Dynamics AX 2012 geçmiş veriye erişim sağlamak için salt okunur çözüm içerir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşlev artık kullanılmamaktadır.                           |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                             |
| **Etkilenen ürün alanları**         | Genel muhasebe                                                 |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Norveç için eGiro EDIFACT CREMUL ödeme içe aktarma biçimi

eGiro müşteri ödemelerinin otomatik deftere nakil işleminde kullanılan uluslararası UN EDIFACT CREMUL (Birden Fazla Alacak Dekontu İletisi) standardını temel alır. eGiro, Microsoft Dynamics AX'te müşteri ödemesi içe aktarma biçimi olarak uygulanır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Biçim gelecekteki sürümlerde ISO 20022 ekstre içe aktarma biçimleri ile değiştirilecektir. |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                                       |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                            |

### <a name="external-inventory-for-poland"></a>Polonya için harici stok

Satınalma olmadan satış için bir satıcıdan alınan malların kanıtı. Dış stokta işlenen mallar standart stoğu etkilemez, satılabilir ve ardından otomatik olarak satın alınabilir. Bu işlem gerçek stok hareketleri oluşturur.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Başka bir özellik ile değiştirildi                                    |
| **Başka bir özellik ile değiştirildi?**   | Evet, çekirdek Gelen konsinye işlevselliği                |
| **Etkilenen ürün alanları**         | Borç hesapları, Stok yönetimi                         |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Doğu Avrupa için mali rapor oluşturucusu

Muhasebe ve vergi raporları için veri toplamak ve XLS ve DOC rapor şablonlarına veri dışa aktarmak için bir araç kullanılır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sınırlı kullanım                                                                            |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Araç gelecekteki sürümlerde Elektronik raporlama yapılandırmaları ile değiştirilecektir. |
| **Etkilenen ürün alanları**         | Genel Muhasebe                                                                           |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Finlandiya için müşteri ödeme hareketlerini içe aktarma

Finlandiya ödemelerinde müşteri ödeme hareketlerini banka tarafından sağlanan harici bir dosyadan içe aktarmak için bir içe aktarma biçimi seçebilirsiniz.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Biçim gelecekteki sürümlerde ISO 20022 ekstre içe aktarma biçimleri ile değiştirilecektir. |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                                       |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Finlandiya için ödeme hareketlerini genel muhasebe günlüğüne içe aktarma

Muhasebe hareketlerini genel muhasebeye içe aktarmak için Finlandiya'ya özgü bir biçim kullanılır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Biçim gelecekteki sürümlerde ISO 20022 ekstre içe aktarma biçimleri ile değiştirilecektir. |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                                       |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Belçika için Isabel ile tümleştirme eşitlendi (CIS)

Isabel, elektronik bankacılık için Avrupa'daki çerçevedir ve Belçika'da fiili bir standarttır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Isabel istemcisi ile tümleştirme kaldırıldı.   |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Belçika için artık kullanılmayan ödeme biçimleri, ISO20022 Alacak transferi ödeme biçimi ile değiştirildi. |
| **Etkilenen ürün alanları**         | Borç hesapları     |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>İspanya için hesap planı ve muhasebe kurallarındaki değişiklikler

Bu özellik, İspanya için hesap planında ve muhasebe kurallarındaki değişiklikler için kullanılır. Eski hesap planını yeni hesap planına dönüştürmeye yardımcı olmak için hesapları eşler ve farklı hesap numaralarına nakledilseler bile önceki mali yıl ile yeni mali yılı karşılaştırır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Sınırlı kullanım                                                  |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                             |
| **Etkilenen ürün alanları**         | Genel muhasebe                                                 |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori satıcı ödemesi biçimi

Alacak transferleri için eski İtalyan ödeme biçimi.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimi artık kullanılmamaktadır.                          |
| **Başka bir özellik ile değiştirildi?**   | Evet, İtalya için ISO20022 Alacak transferi ödeme biçimi         |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="payment-export-formats-for-estonia"></a>Estonya için ödemeleri dışa aktarma biçimleri

Telehansa ve Teleservice biçimleri banka ödemesi dışa aktarımı için kullanılır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Estonya için ISO20022 Alacak transferi ödeme biçimi       |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="payment-file-archive-for-norway"></a>Norveç için ödeme dosya arşivi

Ödeme dosyaları oluşturulduğunda dosya arşivi, dosyalar önceden yazılmış veya okunmuş olsalar bile oluşturulan tüm dosyaları otomatik olarak arşivler.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Başka bir özellik ile değiştirildi                                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Arşivlenen elektronik raporlama işleri                            |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları, Organizasyon yönetimi |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.     |

### <a name="payment-import-formats-for-estonia"></a>Estonya için ödemeleri içe aktarma biçimleri

Telehansa ve TeleTeenus biçimleri banka ödemesi içe aktarımı için kullanılır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                                                    |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Biçimler gelecekteki sürümlerde ISO 20022 ekstre içe aktarma biçimleri ile değiştirilecektir. |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                                        |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                             |

### <a name="payroll-information-in-human-resources"></a>İnsan Kaynakları'ndaki bordro bilgileri

İnsan Kaynakları bordro bilgileri

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlevin yerini temel Bordro ve İnsan Kaynakları sayfaları almıştır.  |
| **Başka bir özellik ile değiştirildi?**   | **Avantajlar**, **Kazançlar** ve daha önce ABD Bordro'da olan diğer ilgili sayfalar yeniden yapılandırıldı ve artık harici bordro işlemeyi desteklemeye yardımcı olacak temel İnsan Kaynakları yapılandırmasının bir parçasılar. Bu işleve **İnsan Kaynakları 1** \> **Bordro** konfigürasyon anahtarı kullanılarak erişilir. |
| **Etkilenen ürün alanları**         | İnsan kaynaklarını, Bordro   |
| **Durum**                         | Dynamics 365 for Operations 1611 sürümü itibarıyla kaldırıldı.    |

### <a name="performance-management-goal-workflow"></a>Performans yönetimi hedefi iş akışı

Performans yönetimi, hedef yönetimini ve performans gözden geçirmeleri ile tümleştirmeyi içerir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Performans yönetimi yeniden tasarlanmıştır ve hedef sayfalarının sayısı işlemi basitleştirecek şekilde azaltılmıştır.                 |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Hedefler yöneticiler tarafından Yönetici Self Servis portalından görülebilir, değiştirilebilir ve görüntülenebilir. |
| **Etkilenen ürün alanları**         | İnsan sermayesi yönetimi       |
| **Durum**                         | Dynamics 365 for Operations 1611 sürümü itibarıyla kaldırıldı.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>İsveç için Postgirot ve Postgirot Utland ödeme biçimleri

İsveç için Postgirot ve Postgirot Utland ödeme biçimleri.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, İsveç için ISO20022 Alacak transferi ödeme biçimi        |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="radio-frequency-identifier"></a>Radyo frekansı kimlik tanımlayıcı

Radyo Frekans Kimlik Belirleme (RFID), kimlik bilgilerini saklamak için elektronik etiket kullanan ve okuyucunun kimlik saptama verisini yakalaması için doğrudan yöneltmeye gerek duymayan bir veri toplama teknolojisidir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük müşteri kullanımı ve sınırlı özellik kümesi.   |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                              |
| **Etkilenen ürün alanları**         | Stok Yönetimi                            |
| **Durum**                         | Dynamics 365 for Operations 1611 itibarıyla kaldırıldı. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Letonya için Fatura numarasının belirtilmesi hakkında rapor

Letonya mevzuatı satış faturalarının numaralandırılması hakkında belirli kurallar sağlar. İşlev, kullanıcı veya kullanıcı grubuna göre satış faturalarına belirli numaralar atamanızı sağlar. Ardından bir rapor veya bir XML dosyası oluşturabilirsiniz. Ayrıca, kullanılan fatura numaraları hakkında bir rapor yazdırabilirsiniz.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Artık fatura numarasının belirtilmesinin saklanması gerekmez. Kullanılan fatura numaraları hakkında rapor artık gerekli değildir. |
| **Başka bir özellik ile değiştirildi?**   | Hayır       |
| **Etkilenen ürün alanları**         | Alacak hesapları    |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Litvanya için yönetici adları ve bir şirketin genel muhasebesini ayarlama

Yönetici adları ve şirketin genel muhasebesi şirket bilgilerinde belirtilebilir ve farklı yerel rapor çıktılarında kullanılabilir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Başka bir özellik ile değiştirildi                                     |
| **Başka bir özellik ile değiştirildi?**   | Evet, yetkililer kurulumu aynı amaç için kullanılabilir.   |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları, Nakit ve banka yönetimi |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |

### <a name="shipping-carrier-interface"></a>Sevkiyat taşıyıcısı arabirimi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tekrar eden işlevsellik   |
| **Başka bir özellik ile değiştirildi?**   | Kısmen Taşıma yönetimiyle değiştirildi |
| **Etkilenen ürün alanları**         | Satış ve pazarlama, Stok Yönetimi  |
| **Durum**                         | Dynamics 365 for Operations 1611 sürümü itibarıyla kaldırıldı.  |

### <a name="telepay-payment-formats-for-norway"></a>Norveç için Telepay ödeme biçimleri

Telepay ödeme biçimleri, satıcı ödemesi dışa aktarımını (alacak transferi) ve müşteri ödeme tahsilatını (otomatik ödeme) içerir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                                                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Norveç için ISO20022 Alacak transferi ödeme biçimi ve AvtaleGiro müşteri ödeme biçimi |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları                                                          |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Finlandiya için satıcı ödeme dışa aktarma biçimleri

Finlandiya için ödemeleri dışa aktarmak üzere iki biçim kullanılabilir. Yurtiçi ödemeleri için kullanılan LM02 (FI) ve yurtdışı ödemeleri için kullanılan LUM2 (FI).

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ödeme biçimleri artık kullanılmamaktadır.                        |
| **Başka bir özellik ile değiştirildi?**   | Evet, Finlandiya için ISO20022 Alacak transferi ödeme biçimi       |
| **Etkilenen ürün alanları**         | Borç hesapları                                               |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="warehouse-management-ii"></a>Ambar yönetimi II

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | **Stok yönetimi** modülünde bulunan Ambar yönetimi II çözümü (WMS II), Microsoft Dynamics AX 2012 R3'te yayınlanmış olan **Ambar yönetimi** modülündeki işlevi kopyalamaktadır.                                                                         |
| **Başka bir özellik ile değiştirildi?**   | AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 ve Dynamics AX 2012 R3 CU9'da yayınlanmış olan **Ambar yönetimi** modülü, Ambar yönetimi II özelliklerinin yerini almıştır. Yeni modül Ambar yönetimi II'dekinden daha gelişmiş özelliklere ve daha esnek ambar yönetim süreçlerine sahiptir. |
| **Etkilenen ürün alanları**         | Stok Yönetimi, satış ve pazarlama, tedarik ve kaynak atama   |
| **Durum**                         | Dynamics 365 for Operations 1611 sürümü itibarıyla kaldırıldı.    |

### <a name="worker-reminders-in-human-resources"></a>İnsan Kaynakları'ndaki çalışan anımsatıcıları

İnsan Kaynakları bordro bilgileri

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım                                                           |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                                  |
| **Etkilenen ürün alanları**         | İnsan kaynakları                                                     |
| **Durum**                         | Dynamics 365 for Operations 1611 sürümü itibarıyla kaldırıldı |

### <a name="workflow-for-creating-goals"></a>Hedefleri oluşturmak için iş akışı

Personel hedeflerini oluşturmayı yöneten iş akışı, performans yönetim işleminin düzenlenmesine yardımcı olan birkaç iş akışından biridir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Performans yönetimi, Microsoft Dynamics 365 for Finance and Operations'da tamamen yeniden tasarlanmıştır.     |
| **Başka bir özellik ile değiştirildi?**   | Yeniden tasarlanan Performans yönetimi özelliği hedef içeriği, ilerlemeyi izlemek için kullanılan ölçümler ve destekleyici belge eki üzerinde daha fazla kontrol sağlar. Hedefler şablon olarak saklanabilir ve daha sonra yeniden kullanılabilir. Bu özellik personeliniz için ek hedefleri daha hızlı bir şekilde ayarlamanıza yardımcı olabilir. |
| **Etkilenen ürün alanları**         | İnsan sermayesi yönetimi                 |
| **Durum**                         | Dynamics 365 for Operations 1611 sürümü itibarıyla kaldırıldı. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Satıcı faturasında yapılan değişiklikleri iptal yeteneği

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Performans geliştirmesi        |
| **Başka bir özellik ile değiştirildi?**   | Hayır                             |
| **Etkilenen ürün alanları**         | Borç hesapları               |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD ve AxBC entegrasyonlar

Uygulama Tümleştirme Çerçevesi (AIF) içerisinde veriler, hizmetler olarak gösterilen iş mantığı üzerinden dış sistemlerle değiştirilebilir. Dynamics AX, .NET Business Connector (AxBC) ve belgelere dayanan hizmetleri içerir. Bir belge, XML kullanılarak oluşturulur. XML, bir *ileti* oluşturmak için eklenen ve Dynamics AX içine veya dışına transfer edilebilen üstbilgi bilgilerini içerir. Belgelerin örnekleri satınalma siparişleri ve satış siparişlerini içerir. Ancak, bir müşteri gibi hemen hemen her varlık, bir belge tarafından temsil edilebilir. Belgelere dayanan hizmetler **Axd \<Belge\>** sınıflarını kullanır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | AIF ve AxDs mimarileri bir bulut hizmetine ölçeklenmiş değildirler. Toplu alma etrafında performans sorunları vardı.                                        |
| **Başka bir özellik ile değiştirildi?**   | Bu özelliğin yerini tekrar eden toplu içe aktarma/dışa aktarma işlemlerini destekleyen, Veri İçe Aktarma/Dışa Aktarma çerçevesi almıştır. AxBC için gerçek tabloları kullanmanızı öneririz. |
| **Etkilenen ürün alanları**         | AxDs, AxBCs ve AIF   |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="boms-without-bom-versions"></a>Ürün reçetesi sürümleri olmayan ürün reçeteleri

**BOM sürümleri** yapılandırma anahtarı devre dışı bırakıldığında, ürün reçetesi (BOM) sürümleri tüm formlarda gizleniyordu ve sistem serbest bırakılan ürünler ve ürün reçeteleri arasında bir 1:1 ilişkisini zorluyordu. **BOM sürümleri** yapılandırma anahtarı, Dynamics AX'in geçerli sürümünde devre dışı bırakılamaz.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ürün reçetesi sürümlerini denetlemek için konfigürasyon anahtarı kullanmak bir bulut ortamında ölçeklendirilemez. |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                                                      |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi, Stok Yönetimi                                    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                          |

### <a name="brazilian-bordero"></a>Brazilian Bordero

Brezilya şirketleri için belirli ödeme yöntemi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Brazilian Bordero ödeme yöntemi için destek Brezilya yerelleştirmesinden kaldırılmıştır |
| **Başka bir özellik ile değiştirildi?**   | Hayır   |
| **Etkilenen ürün alanları**         | Borç hesapları   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="brazilian-sintegra-statement"></a>Brazilian Sintegra ekstresi

ICMS vergisi için federal vergi ekstresi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu ekstre bazı Brezilya eyaletlerinde artık kullanılmamaktadır. |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Kullanıcılar Genel Elektronik raporlama aracını belirli durumlarda gerektiğinde ekstreyi yapılandırmak için kullanabilir. |
| **Etkilenen ürün alanları**         | Mali defterler    |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>NF-e için Brezilya SCAN yedeği modu

(SCAN) yedeği ortamı, Secretaria da Fazenda (SEFAZ) ortamı kullanılabilir olmadığında bir Nota Fiscal eletrônica (NF-e) durumunu oluşturmak, dışa aktarmak ve içe aktarmak için kullanılır.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu yedek yöntem, Brezilya eyaletlerinin tamamında artık geçersizdir |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                                          |
| **Etkilenen ürün alanları**         | Alacak hesapları                                                         |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.              |

### <a name="business-analyzer"></a>İş Çözümleyicisi

Bu mobil uygulama kullanıcıların anahtar iş ölçümlerini gözden geçirmelerini sağlar.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlev başka bir özellik ile değiştirilmiştir.   |
| **Başka bir özellik ile değiştirildi?**   | Microsoft Power BI için Finansal performans içeriği izleme paketi, daha önce Business Analyzer'da bulunan önemli mali ölçümleri içerecektir. |
| **Etkilenen ürün alanları**         | Genel muhasebe      |
| **Durum**                         | Kullanımı sonlandırıldı: İş Çözümleyicisi kullanımı sonlandırıldı.    |

### <a name="business-statistics"></a>İşletme istatistikleri

Kuruluşun performansını analiz etmenize yardımcı olabilecek iş istatistiği sorgularının kurulumu

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İş zekasına (BI) eski yaklaşım, düşük müşteri kullanımı ve sınırlı özellik kümesine |
| **Başka bir özellik ile değiştirildi?**   | Dynamics AX'in geçerli sürümü için yeni BI çözümleri                                      |
| **Etkilenen ürün alanları**         | Tedarik ve kaynak hizmeti, Borç hesapları, Satış ve pazarlama, Alacak hesapları         |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Fatura onay günlüğündeki belge tarihi değiştirme işlevi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım                                                               |
| **Başka bir özellik ile değiştirildi?**   | Evet. Deftere nakledilen satıcı hareketi üzerindeki belge tarihi değiştirilebilir. |
| **Etkilenen ürün alanları**         | Borç hesapları                                                        |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Hollanda için ClieOp03 ödeme biçimi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Hollanda'da artık geçerli değildir. |
| **Başka bir özellik ile değiştirildi?**   | SEPA ödemeleri dışa aktarımı  |
| **Etkilenen ürün alanları**         | Tüm modüller     |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |

### <a name="compliance-center"></a>Uyumluluk Merkezi

Uyumluluk Merkezi, Sarbanes-Oxley Yasası ilgili uyumluluk girişimleriyle belgelerine gereksinimlerini yönetmek kullanılan bir Kurumsal Portal sitesiydi.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Müşteri kullanım eksikliği. Microsoft SharePoint Uyumluluk Merkezi'nde sunulmuş olanlarla aynı özellikleri içerir. |
| **Başka bir özellik ile değiştirildi?**   | Hayır   |
| **Etkilenen ürün alanları**         | Uyumluluk ve dahili kontroller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.    |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamics için Bağlayıcı

Bu araç, anahtar verileri Microsoft Dynamics CRM'den Microsoft Dynamics ERP uygulamalarına tümleştirmek için kullanıldı.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlev başka bir özellik ile değiştirilmiştir. |
| **Başka bir özellik ile değiştirildi?**   | Common data service                                      |
| **Etkilenen ürün alanları**         | Microsoft Dynamics için Bağlayıcı                         |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Eldeki konteyner birimi ve çoklu boyut

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tekrar eden işlevsellik |
| **Başka bir özellik ile değiştirildi?**   | Evet. AX 2012'den itibaren bu işlevin yerini konsolide toplu iş siparişleri özellik kümesi almıştır. Bu özellik kümesi konsolide eldeki görünümünü içerir. |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi, Üretim kontrol, Stok Yönetimi, Satış ve pazarlama  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı. |

### <a name="cue-group-metadata"></a>İşaret Grup meta verileri

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşaret grupları, bilgi alanında bir veya daha fazla ipucu görüntülemek için kullanılıyordu. Sınırlı kullanım vardı ve ayrıca performans kaygıları da mevcuttu çünkü bir üst formdaki değişiklik, her İşaret grubundaki her bir İşarette bir sorguya sebep oluyordu. |
| **Başka bir özellik ile değiştirildi?**   | Hayır      |
| **Etkilenen ürün alanları**         | Tüm modüller    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.  |

### <a name="cue-metadata"></a>İşaret meta verileri

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşaret meta veriler, sayma ve toplama bilgileri ile sınırlıydı.    |
| **Başka bir özellik ile değiştirildi?**   | Döşeme meta veri modelleme için daha fazla esneklik sağlamak amacıyla kullanılmaya başlandı. Örneğin, geçerli sayma, gezinti ve anahtar performans göstergeleri (APG) modelleyebilirsiniz. Sayım döşeme meta verileri, işaret meta verilerinin doğrudan yerini almıştır. |
| **Etkilenen ürün alanları**         | Tüm modüller           |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı      |

### <a name="danish-check-format"></a>Danimarka çek biçimi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Danimarka çek biçimi düzeni için destek kaldırılmıştır ve rapor DK yerelleştirmeden silinmiştir. |
| **Başka bir özellik ile değiştirildi?**   | Hayır    |
| **Etkilenen ürün alanları**         | Tüm modüller    |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |

### <a name="data-partitions"></a>Veri bölümleri

Veri bölümleri, Microsoft Dynamics AX veritabanındaki verinin mantıksal bir ayrımını sağlar.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Veri bölümleri, veri yalıtımı sağlamak için Microsoft Dynamics AX 2012 R2'de kullanılmaya başlanmıştır. Yaygın bir senaryoda, bir şirketin bağlı kuruluşları vardır ve her iki bağlı kuruluş da aynı BT departmanı tarafından yönetilseler bile bir bağlı kuruluşun verisinin diğer bağlı kuruluşa görünür olmaması gerekir. Ancak, yeni bölümler oluşturmak, bunları veri ile doldurmak ve bölüm verilerini yedeklemek için ekstra kodlar ve program boyunca genel yönetim giderleri gerekir. Hizmet olarak platform (PaaS) veritabanına (Microsoft Azure SQL veritabanı) erişimimizin olduğu bulutta, veritabanını bir yalıtım konteyneri olarak kullanmak program içinde yalıtmaya göre çok daha etkilidir. Veri bölümlemenin bağlı kuruluşlar, çoklu kiracılar veya yalnızca ölçek için gerekli olup olmadığına bakılmaksızın, senaryoların birden çok veritabanı veya birden çok Finance and Operations kurulumları ile daha iyi işlenebileceğine inanırız. |
| **Başka bir özellik ile değiştirildi?**   | Veritabanı düzeyinde ayırma önemli bir sorunsa, veri bölümleri kullanan müşterilerin birden çok Finance and Operations kurulumu kullanması gerekir.    |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Ekler için veritabanı ve dosya paylaşım depolama

Microsoft Dynamics AX 2012, eklerin veritabanında ve dosya paylaşımında depolanmasına izin vermekteydi. Bu seçeneklerin her ikisi de artık desteklenmiyor.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dosya paylaşım depolaması, bulutta barındırılan ortamlar yerel dosya paylaşımlarıyla iletişim kuramadığı için artık desteklenmiyor. Veritabanı depolama, Azure Blob depolama kullanıldığından kullanım dışı bırakıldı. Azure Blob depolama, veritabanında depolamaya eşdeğerdir çünkü belgeler yalnızca Dynamics 365 for Finance and Operations istemci formları üzerinden erişilebilir. Bu, veritabanı performansını olumsuz etkilemeyen depolama sağlama faydasını sunar. Blob depolama, Belge Yönetimi için varsayılan mekanizmadır ve hemen çalışır. |
| **Başka bir özellik ile değiştirildi?**   | Veritabanı depolama, Azure Blob depolama kullanıldığından kullanım dışı bırakıldı.   |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="delimitation"></a>Sınırlandırma

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşlev için kullanım bulunamadı. |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                     |
| **Etkilenen ürün alanları**         | Saat ve işe devam                    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.         |

### <a name="desktop-client"></a>Masaüstü istemcisi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dynamics AX İstemci deneyimi, platformlar ve aygıtlar üzerinde kullanılabilirliğini artırmak için tasarlanmıştır.                      |
| **Başka bir özellik ile değiştirildi?**   | Yeni web istemci masaüstü formu meta verileri ve zengin web platformu sunmak için değiştirilmiş programlama modeline dayanır. |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="direct-database-connection"></a>Doğrudan veritabanı bağlantısı

Dynamics AX 2012 R3 içerisinde, Perakende Modern POS, Kanal Veritabanına, Kuruluş POS'a benzer şekilde doğrudan bağlanamadı. Bu, Perakende Modern POS'un, Perakende Sunucusu üzerinden iletişim kurarken standart iletişim yöntemine ek olarak oluştu.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Doğrudan veritabanı bağlantısı, daha düşük güvenlik protokolleri gerektirdi ve öncelikli olarak en yüksek seviye performansı elde etmek için kullanıldı. Finance and Operations içerisinde gerçekleşen performans ve güvenlik geliştirmeleri yüzünden, bu işlev artık çözdüğünden daha fazla soruna neden olmaktadır. |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Artık yalnızca standart Perakende Sunucu iletişimi desteklenmektedir.  |
| **Etkilenen ürün alanları**         | Kanal Veritabanı/Perakende Modern POS   |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.  |

### <a name="dutch-swift-mt940"></a>Felemenkçe SWIFT MT940

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yerelleştirilmiş işlevsellik yerine artık genel işlevler kullanılır.                    |
| **Başka bir özellik ile değiştirildi?**   | Evet, bu işlevin yerini Gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen ürün alanları**         | Tüm modüller                                                                              |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (Almanya için XBRL)

Bu işlev Alman eBilanz taksonomisi için özel olarak tasarlanmış olan Genişletilebilir İş Raporlama Dili (XBRL) çıkışı sağlamaktaydı.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Müşteri kullanım eksikliği  |
| **Başka bir özellik ile değiştirildi?**   | Bu özelliğin yerini bir başkası almadı ancak Almanya pazarı için zengin XBRL işlevselliği sağlayan birden çok özelleşmiş XBRL paketi sunulmuştur. |
| **Etkilenen ürün alanları**         | Management Reporter      |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.  |

### <a name="enterprise-portal-client"></a>Kurumsal Portal istemcisi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bir tek istemci platformu sağlandı.  |
| **Başka bir özellik ile değiştirildi?**   | Yeni web istemci masaüstü formu meta verileri ve zengin web platformu sunmak için değiştirilmiş programlama modeline dayanır. |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="environmental-sustainability"></a>Ortam sürdürülebilirliği

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük müşteri kullanımı ve sınırlı özellik kümesi  |
| **Başka bir özellik ile değiştirildi?**   | Hayır              |
| **Etkilenen ürün alanları**         | Uyumluluk ve dahili kontroller, Borç hesapları  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı. |

### <a name="form-activex-and-managed-host-controls"></a>Form ActiveX ve yönetilen konak denetimleri

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | ActiveX ve yönetilebilir konak denetimleri artık kullanılmayan masaüstü istemciyi temel alır. |
| **Başka bir özellik ile değiştirildi?**   | Genişletilebilir denetim çerçevesi HTML, CSS ve JavaScript'e dayanan yeni denetimleri oluşturmayı destekler ve Microsoft Visual Studio Tooling ortamındaki birinci sınıf bir denetimdir. |
| **Etkilenen ürün alanları**         | Tüm modüller     |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Bir toplu işlem kullanarak açık provizyon oluşturmak

Açık provizyon oluşturma, bir toplu iş kullanarak yapılamaz ancak hala bir kullanıcı tarafından yapılabilir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Toplu iş kullanılarak oluşturulduğunda, ortaya çıkan açık provizyon dosyasını ısrar edip görüntülemek için form bulunmamaktadır. |
| **Başka bir özellik ile değiştirildi?**   | Açık provizyonlar hala oluşturulabilir ve kullanıcı dosyanın kaydedildiği yeri denetleyebilir.   |
| **Etkilenen ürün alanları**         | Borç hesapları, Alacak hesapları, Nakit ve banka yönetimi  |
| **Durum**                         | AX 7.0 itibarıyla kaldırıldı.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Almanca DTAUS ödeme dışa aktarma ve hesap ekstresi içeri alma (toplamları ve hareketler)

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Almanya'da artık geçerli değildir.                    |
| **Başka bir özellik ile değiştirildi?**   | Evet, bu özelliğin yerini SEPA ödeme dışa aktarma ve hesap ekstrelerini içeri aktarma için gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen ürün alanları**         | Tüm modüller  |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="german-dtazv-payment-format"></a>Alman DTAZV ödeme biçimi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Almanya'da artık geçerli değildir. |
| **Başka bir özellik ile değiştirildi?**   | SEPA ödemeleri dışa aktarımı    |
| **Etkilenen ürün alanları**         | Tüm modüller   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.    |

### <a name="german-mt940-import"></a>Almanca MT940 içe aktarımı

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yerelleştirilmiş işlevsellik yerine artık genel işlevler kullanılır.                    |
| **Başka bir özellik ile değiştirildi?**   | Evet, bu işlevin yerini Gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen ürün alanları**         | Tüm modüller                                                                              |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.                           |

### <a name="german-xml-eu-sales-list"></a>Alman XML AB Satışlar listesi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Almanca AB Satış Listesi raporlaması için XML biçimi artık desteklenmiyor. Alman Vergi Dairesi'ne AB Satış Listesi raporunu göndermek için yalnızca ELMA5 metin dosyası biçimi kullanılabilir. |
| **Başka bir özellik ile değiştirildi?**   | Hayır         |
| **Etkilenen ürün alanları**         | Vergi        |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.   |

### <a name="gl-ssrs-reports"></a>GL SSRS raporları

Aşağıdaki menü öğelerini içeren raporlar kaldırıldı: **Özet mizan**, **ayrıntılı mizan**, **hesap planı**, **denetim izi**, **bakiyeler**, ve **bakiye listesi**.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Mali Microsoft SQL Server Raporlama Servisleri (SSRS) raporlarının yeri, Yönetimi Raporlayıcı'sı yetenekleri ve varsayılan raporlar tarafından alınmıştır. |
| **Başka bir özellik ile değiştirildi?**   | Yönetim Raporlayıcı (Dynamics AX'ın geçerli sürümünde **finansal raporlama** etiketli)    |
| **Etkilenen ürün alanları**         | Genel muhasebe   |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart ve FormPart meta verileri

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | InfoPart ve FormPart meta verileri, iki farklı istemci için bilgi kutularının oluşturulması sağlardı. |
| **Başka bir özellik ile değiştirildi?**   | Basitleştirilmiş form tanımı olan InfoPart meta verileri, forma yükseltme araç kullanımı tarafından dönüştürülür. Bir forma referans gösteren FormPart meta verileri, yükseltme araçları tarafından daha doğrudan bir referans ile değiştirildi. |
| **Etkilenen ürün alanları**         | Tüm modüller    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.        |

### <a name="main-account-list-page"></a>Ana hesap liste sayfası

Tüzel kişilik ve ilgili bakiye bilgilerini hesapların listesi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bakiye bilgisi **Mizan** liste sayfasında hesap ve boyut olarak bulunabilir.  |
| **Başka bir özellik ile değiştirildi?**   | **Ana hesaplar**,**Ana hesap** sayfasında yer alan hesapların listesinin aynısını içerir. **Ana hesaplar**'daki ızgara görünümü daha da küçük ızgaraya benzer bir görünümü gösterir. |
| **Etkilenen ürün alanları**         | Genel muhasebe      |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malezya ve Singapur banka nakit akışı raporu

Seçili banka hesapları için belirli bir tarih aralığındaki hareketlerin nakit giriş ve çıkış ayrıntılarını gösteren bir nakit akış raporu kullanıcı tarafından yazdırılabilir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aynı bilgileri sorgulama banka hareketinden de elde edilebilir. |
| **Başka bir özellik ile değiştirildi?**   | Sorgulama banka hareketi                                            |
| **Etkilenen ürün alanları**         | Nakit ve banka yönetimi                                                |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi.          |

### <a name="mexican-cfd-electronic-invoice"></a>Meksika CFD elektronik fatura

Bu özellik, şirketin faturayı hükümetten ilgili izni isteyerek imzaladığı Comprobante Fiscal Digital (CFD) yöntemini kullanarak Meksika elektronik fatura oluşturmayı etkinleştirir. Bu özellik ayrıca bir dönemde çıkarılan tüm elektronik faturaları içeren aylık bir rapor sunar.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yöntemi artık geçerli değil. CFG yöntemini kullanarak elektronik faturaların oluşturulması vergi otoriteleri tarafından kaldırılıp yerine imzalamanın üçüncü taraf bir sağlayıcıya (PAC) devredildiği Comprobante Fiscal Digital a través de Internet (CFDI) metodu getirilmiştir. Aylık rapor kaldırıldı ve kullanıcıların geçmiş hareketler hakkında bilgi alması için sorgu seçeneği geliştirildi. |
| **Başka bir özellik ile değiştirildi?**   | Hayır    |
| **Etkilenen ürün alanları**         | Alacaklar hesabı, Proje   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksika gerçekleşmiş ve gerçekleşmemiş KDV

Microsoft Dynamics AX 2012, gerçekleşmemiş katma değer vergisini (KDV) Meksika'ya özgü gerçekleşmemiş vergi işlevini kullanarak yönetiyordu.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Tekrar eden işlevsellik  |
| **Başka bir özellik ile değiştirildi?**   | Evet, bu işlevin yerini Çekirdek tarafından sağlanan standart koşullu satış vergisi işlevleri aldı. |
| **Etkilenen ürün alanları**         | Vergi   |
| **Durum**                         | Kullanımı sonlandırıldı: Bu özellik için kaldırma tarihi belirlenmedi. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook entegrasyonu


|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu işlevin yerini Microsoft Exchange Server tümleştirmesi almıştır. |
| **Başka bir özellik ile değiştirildi?**   | Evet                                                                            |
| **Etkilenen ürün alanları**         | Satış ve pazarlama                                                            |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Stok ve Ambar yönetim günlüklerinin özel durdurması

Stok ve Ambar günlükleri, günlüğün seçili kullanıcı için özel olarak işaretleme özelliğini artık desteklememektedir. Yalnızca kullanıcı grupları için özel olarak günlükleri engelleme ve düzenleme sırasında engelleme işlemi desteklenir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | İşlev için kullanım bulunamadı. |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                     |
| **Etkilenen ürün alanları**         | Stok Yönetimi                   |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.         |

### <a name="product-builder"></a>Ürün oluşturucu

Ürün Oluşturucu, bir satış siparişi, satınalma siparişi, üretim emri, satış teklifi, proje teklifi veya madde gereksinimi öğelerinden dinamik olarak ürün yapılandırmak için kullanılıyordu. Model oluşturma değişkenleri olan bir ürün modeline bağlı olarak, kullanıcı, müşteri gereksinimlerini karşılamak için bir ürün reçetesi ve rotası olan benzersiz bir ürün çeşidi sağlamak için değerler seçebiliyordu.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Ürün Oluşturucu X ++ kodunu son kullanıcılara yansıtıyordu ve Dynamics AX'ın geçerli sürümünde desteklenmiyor. Büyük ve kesişen kod tabanlarında sürdürme çabalarının ikiye katlanmaması için kaldırıldı.  |
| **Başka bir özellik ile değiştirildi?**   | Evet. Kısıtlama tabanlı yapılandırma Dynamics AX 2012'de sunuldu ve Ürün oluşturucunun gelecekteki sürümlerde kullanımdan kaldırılacağı zaten açıklandı. Kısıtlama tabanlı yapılandırma teknolojisi yapılandırmayı etkinleştirmek ana ürünlerde seçilir. Daha fazla bilgi için bkz. [Ürün yapılandırma modeli oluşturma](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model). |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi, satış ve pazarlama  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.      |

### <a name="rename-product-dimension"></a>Ürün boyutunu yeniden adlandır

Bu özellik, üç standart ürün boyutundan (boyut, renk veya stil) birinin adını işletme gereksinimlerinize daha iyi uygun bir adla değiştirmenize olanak sağlar. Yeniden adlandırma, ürün boyut adının kullanıldığı tüm etiketlere dahildir.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dynamics AX geçerli sürümününde, çalıştırma sırasında etiket değişikliklerini desteklemez. |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                                                            |
| **Etkilenen ürün alanları**         | Ürün bilgileri yönetimi                                                |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                                |

### <a name="retail-server-connectivity-using-http"></a>HTTP kullanarak Perakende Sunucu bağlantısı

Dynamics AX 2012 R3 içerisinde, Perakende Sunucu, HTTP iletişimi (güvenli olmayan) kullanarak işlev sağlayamıyordu. Bu, HTTPS kullanan standart iletişime ek olarak oluştu.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni güvenlik gereksinimleri nedeniyle, yalnızca TLS 1.2 (veya kullanılabilir olduğu takdirde üstü) artık desteklenmektedir. Self servis yükleyici, bilgisayarı bu iletişim için otomatik yapılandıracaktır. |
| **Başka bir özellik ile değiştirildi?**   | Hayır. Artık yalnızca standart HTTPS iletişimi desteklenmektedir. |
| **Etkilenen ürün alanları**         | Retail Server  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı. |

### <a name="role-center-pages"></a>Rol Merkezi sayfaları

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Rol Merkezi sayfaları, kaldırılan Enterprise Portal platformu üzerine kurulmuştu ve Dynamics AX'ın geçerli sürümünde yeni web istemci platformu tarafından yenilendi. |
| **Başka bir özellik ile değiştirildi?**   | Yeni çalışma alanı form düzeni kullanıcılara işlem merkezli tasarıma sahip, sık kullanılan işlemlere kolay erişim sağlayan bir işlem merkezli tasarımı sağlar.                       |
| **Etkilenen ürün alanları**         | Tüm modüller    |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı   |

### <a name="sales-tax-jurisdictions"></a>Satış vergi daireleri

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük müşteri kullanımı ve sınırlı özellik kümesi |
| **Başka bir özellik ile değiştirildi?**   | Hayır                                           |
| **Etkilenen ürün alanları**         | ABD satış vergisi                                 |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.               |

### <a name="sites-services"></a>Site Servisleri

Site Hizmetleri, BT desteği olmadan iş süreçlerinizi internete genişleten web siteleri kurmanıza olanak sağlar.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dynamics AX tarafından kullanılan Microsoft Azure altyapısı, alternatif olarak kullanılabilecek yeni özelliklere sahiptir (örneğin, Azure siteleri). |
| **Başka bir özellik ile değiştirildi?**   | Hayır   |
| **Etkilenen ürün alanları**         | İK işe alma, Servis talebi yönetimi, Teklif talebi, Satıcı kaydı, Fırsatlar ve kampanyalar için ortak çalışma alanları  |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSASS talep tahmin stratejisi

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Özelliğin tasarımı yeni bulut mimarisinde desteklenemez. |
| **Başka bir özellik ile değiştirildi?**   | Azure Makine Öğrenimi talep tahmini stratejisi                           |
| **Etkilenen ürün alanları**         | Master planlama                                                              |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Deftere nakledilen ayrıntılar hariç satıcı faturası havuzu

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım. Bu özelliğin yerini iş akışı işlevine sahip Fatura günlüğü almıştır. |
| **Başka bir özellik ile değiştirildi?**   | Fatura günlüğünün iş akışı özellikleri.     |
| **Etkilenen ürün alanları**         | Borç hesapları |
| **Durum**                         | Dynamics AX 7.0 itibarıyla kaldırıldı.    |


### <a name="virtual-company-accounts"></a>Sanal şirket hesapları

Sanal şirketler özelliği, Dynamics AX uygulamasında artık desteklenmiyor. Sanal şirketler özelliği, kullanıcılara bir dizi şirket tarafından paylaşılabilecek tablolar ayarlama olanağı sağlar. Özelliğin açıklaması için bkz. [Şirket hesapları ve Sanal şirket hesapları](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Bu özellik, tabloları, varolan "gerçek" şirketlerin grupları olan sanal şirketlere atanan koleksiyonlara gruplayarak çalışmaktadır. Sanal şirketteki tüm şirketlerin ilişkilendirilen tablo koleksiyonlarının tabloları içindeki verilere erişebileceği şekilde sorgular oluşturulur.

|   |  | 
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | - Tablolarda verilerin depolanmasından önce sanal şirketlerin ayarlanmış olması gerekir. Sanal şirketleri mevcut bir uygulamaya uyarlamak oldukça güçtür.<br><br>- Dynamics AX'in geçerli sürümünde çok fazla veri normalleştirmesi olduğundan, tablo koleksiyonlarına nelerin eklenmesi gerektiğini bilmek çok zor hale geldi. Örneğin, hangi tabloların paylaşılacağını bilmek zor. Bir sanal şirketteki tablolardan referans alınan tüm tabloların da ayrıca eklenmesi gerekir. Tablo normalleştirmesi nedeniyle, çok sayıda tabloya yayılan basit master verilerin bile sanal şirketin parçası haline gelmesi gerekiyor. Burada yapılan herhangi bir hata, işlevsel sorunlara neden olur.<br><br>- Bir tablo bir sanal şirketin parçası olduğunda, veri kaynağı hakkındaki bilgiyi kaybeder ve sadece sanal şirket kaydedilir.   |
| **Başka bir özellik ile değiştirildi?** | Tabloları tüm şirketlerden erişebilir hale getirmek için global tablolar kullanılabilir. Şu anda bir değişiklik yoktur. |   
| **Etkilenen ürün alanları**       | Tüm modüller |   
| **Durum**                       | Dynamics AX 7.0 itibarıyla kaldırıldı.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 tablet uygulaması

Windows 8 tablet uygulaması, gider girişi ve onayı için işlevler sağlardı.

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Finance and Operations tabletlerle uyumludur. Tablet uygulaması artık gerekli değildir.    |
| **Başka bir özellik ile değiştirildi?**   | Hayır.          |
| **Etkilenen ürün alanları**         | Gider yönetimi   |
| **Durum**                         | Kaldırıldı: Bu işlev yalnızca Dynamics AX 2012 R3 için kullanılabilir. |

### <a name="workplanner"></a>İş planlayıcısı

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Düşük kullanım |
| **Başka bir özellik ile değiştirildi?**   | Hayır, ama **Profil grupları** sayfasından açılan **Profil ilişkisi** sayfası, kaldırılan **İş planlayıcısı** sayfası ile aynı iş senaryosunu destekler. |
| **Etkilenen ürün alanları**         | Saat ve işe devam     |
| **Durum**                         | Kod kaldırılmadı. Bununla birlikte, JmgWorkPlanner formunun geçişi yapılmadı.    |

### <a name="x-financial-statements"></a>X++ mali tablolar

|                                                 |                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Kullanımı sonlandırma/kaldırma nedeni</strong> |                         Bu işlev başka bir özellik ile değiştirilmiştir.                         |
|  <strong>Başka bir özellik ile değiştirildi?</strong>  | Yönetim Raporlayıcı (Dynamics AX'ın geçerli sürümünde <strong>finansal raporlama</strong> etiketli) |
|     <strong>Etkilenen ürün alanları</strong>     |                                              Genel muhasebe                                              |
|             <strong>Durum</strong>             |                                      Dynamics AX 2012 itibarıyla kaldırıldı                                      |



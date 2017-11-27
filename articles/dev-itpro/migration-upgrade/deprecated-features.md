---
title: "Kaldırılan özellikler"
description: "Bu konu kaldırılmış veya kaldırılması planlanan özellikleri açıklar."
author: sericks007
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: HT
ms.sourcegitcommit: 9ee81bbdd22fed4ef6ea97080fe1f6b3d82bcaf5
ms.openlocfilehash: ee051bbf50a6124fe1700a244b36b5f9c599e714
ms.contentlocale: tr-tr
ms.lasthandoff: 11/06/2017

---

# <a name="deprecated-features"></a>Kaldırılan özellikler

[!include[banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'dan kaldırılmış veya kaldırılması planlanan özellikler açıklanmaktadır.

## <a name="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Dynamics 365 for Finance and Operations, Enterprise edition platform güncelleştirmesi 8 ile (Temmuz 2017) kaldırılmış özellikler

### <a name="warehouse-mobile-devices-portal"></a>Ambar mobil cihazlar portalı

Ambar mobil cihazlar portalı (WMDP), yerinde kendi kedine dağıtım için amaçlanmış bir tek bileşendir. Bileşen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içinde artık desteklenmemektedir. Kullanıcı deneyimini iyileştiren bir yerel uygulama, WMDP'nin işlevinin yerini almıştır. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Kaldırılma nedeni**       | Tekrar eden işlevsellik.                        |
| **Başka bir özellik ile değiştirildi?** | Evet. Bu özellik Finance and Operations - Ambarlama ile değiştirilmiştir. Kurulum ve önkoşulları hakkında daha fazla bilgi için, bkz. [Microsoft Dynamics 365 for Finance and Operations - Ambarlama için kurulum ve yapılandırma](../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Etkilenen modüller**             | Ambar yönetimi, Taşıma yönetimi |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>El ile eşleştirme için gelişmiş banka mutabakatı eşleştirme kuralı

Bir mutabakat kuralı, belgeler el ile mutabakat çalışma sayfasında eşleştirildiğinde bir banka belgesini seçmek ve işaretlemek için kullanılmıştır.

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Sınırlı kullanım.                                                                         |
| **Başka bir özellik ile değiştirildi?** | Hayır. Sütun filtreleme yetenekleri, mutabakat için belgeleri bulmakta kullanılmalıdır. |
| **Etkilenen modüller**             | Nakit ve banka yönetimi                                                               |

### <a name="windows-8-tablet-app"></a>Windows 8 tablet uygulaması

Windows 8 tablet uygulaması, gider girişi ve onayı için işlevler sağlardı.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Finance and Operations tabletlerle uyumludur. Tablet uygulaması artık gerekli değildir. |
| **Başka bir özellik ile değiştirildi?** | Hayır.                                                                                      |
| **Etkilenen modüller**             | Gider yönetimi                                                                       |


## <a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Platform güncelleştirmesi 3'e sahip Microsoft Dynamics 365 for Operations 1611 sürümünde kaldırılan özellikler

### <a name="aeb-payment-formats-for-spain"></a>İspanya için AEB ödeme biçimleri

Consejo üst Bancario ödeme biçimleri, müşteri ödemeleri ve satıcı ödemeleri için havale dosyalarını bankaya göndermek amacıyla kullanılır. Bu biçimlerin içeriği Asociación Española de Banca tarafından belirlenir. Cuaderno 19, 32, 58, 34'ü kapsar.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimleri artık kullanılmamaktadır.                                  |
| **Başka bir özellik ile değiştirildi?** | Evet, İspanya için ISO20022 Alacak transferi ve Otomatik ödeme biçimleri |
| **Etkilenen modüller**             | Borç hesapları, Alacak hesapları                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Litvanya için banka ödemeleri transferi

Litvanya için banka ödeme transferleri, Ödeme transferi (LT) dışa aktarma biçimi kullanarak oluşturulur ve yazdırılır. Litvanya pazarı 2005'te birleştirilmiş elektronik bankacılık sistemi olan LİTAS'ı kullanmaya başladı.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimleri artık kullanılmamaktadır.                    |
| **Başka bir özellik ile değiştirildi?** | Evet, Litvanya için ISO20022 Alacak transferi ödeme biçimi |
| **Etkilenen modüller**             | Borç hesapları                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Norveç için BBS Direkte Remittering ödeme biçimleri

BBS Direkte Remittering ödeme biçimleri, müşteri ödeme tahsilatını dışa aktarmayı (otomatik ödeme) ve geri dönen iletiyi içe aktarmayı içerir.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimleri artık kullanılmamaktadır.                                                                                                                        |
| **Başka bir özellik ile değiştirildi?** | Norveç için AvtaleGiro müşteri ödeme biçimi otomatik ödeme iletileri oluşturmak için kullanılabilir. Geri dönen iletiyi içe aktarma gelecek sürümlerde uygulanacaktır. |
| **Etkilenen modüller**             | Borç hesapları, Alacak hesapları                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>İspanya için Hesap Planı aracı

Bu araç, İspanya'da bir hesap planında büyük değişiklikler yapılması gerektiğinde kullanılır. Kullanıcılar Microsoft Excel'de veya metin biçiminde yeni bir hesap planını ve ayrıca mali tabloları içe aktarabilir.

|                              |                |
|------------------------------|----------------|
| **Kaldırılma nedeni**       | Sınırlı kullanım  |
| **Başka bir özellik ile değiştirildi?** | Hayır             |
| **Etkilenen modüller**             | Genel muhasebe |

### <a name="dom80-payment-format-for-belgium"></a>Belçika için Dom80 ödeme biçimi

Ödeme tahsilatı (otomatik ödeme) için eski Belçika ödeme biçimi.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Kaldırılma nedeni**      | Ödeme biçimi artık kullanılmamaktadır.                  |
| **Başka bir özellik ile değiştirildi?** | Evet, Belçika için ISO 20022 Otomatik ödeme biçimi |
| **Etkilenen modüller**            | Alacak hesapları                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>İsviçre için DTA/EZAG ödeme biçimleri

DTA/EZAG biçimleri, referans numarası ile ilişkili oldukları için ESR sistemine tümleştirilmiştir. Referans numarası zorunlu olmadığından bu biçimler her türlü satıcı ödemesini işlemek için kullanılabilir. Bu biçimler “Postfinance” dışında bir konumda banka hesabı bulunan şirketler tarafından kullanılır.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimleri artık kullanılmamaktadır.                      |
| **Başka bir özellik ile değiştirildi?** | Evet, İsviçre için ISO20022 Alacak transferi ödeme biçimi |
| **Etkilenen modüller**             | Borç hesapları                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Avusturya için EDIFACT DIRDEB ödeme biçimi

Ödeme tahsilatı (otomatik ödeme) için EDIFACT-DIRDEB ödeme biçimi.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimi artık kullanılmamaktadır.                  |
| **Başka bir özellik ile değiştirildi?** | Evet, Avusturya için ISO 20022 Otomatik ödeme biçimi |
| **Etkilenen modüller**             | Alacak hesapları                                    |

### <a name="edivat-for-belgium"></a>Belçika için EDIVAT

EDIVAT güvenli posta yoluyla elektronik beyanname için geçersiz bir Belçika standardıdır. Microsoft Dynamics AX 2012 geçmiş veriye erişim sağlamak için salt okunur çözüm içerir.

|                              |                                      |
|------------------------------|--------------------------------------|
| **Kaldırılma nedeni**       | İşlev artık kullanılmamaktadır. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                   |
| **Etkilenen modüller**             | Genel muhasebe                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Norveç için eGiro EDIFACT CREMUL ödeme içe aktarma biçimi

eGiro müşteri ödemelerinin otomatik deftere nakil işleminde kullanılan uluslararası UN EDIFACT CREMUL (Birden Fazla Alacak Dekontu İletisi) standardını temel alır. eGiro, Microsoft Dynamics AX'te müşteri ödemesi içe aktarma biçimi olarak uygulanır.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellik ile değiştirildi?** | Hayır. Biçim gelecekteki sürümlerde ISO 20022 ekstre içe aktarma biçimleri ile değiştirilecektir. |
| **Etkilenen modüller**             | Alacak hesapları                                                                       |

### <a name="external-inventory-for-poland"></a>Polonya için harici stok

Satınalma olmadan satış için bir satıcıdan alınan malların kanıtı. Dış stokta işlenen mallar standart stoğu etkilemez, satılabilir ve ardından otomatik olarak satın alınabilir. Bu işlem gerçek stok hareketleri oluşturur.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| **Kaldırılma nedeni**       | Başka bir özellik ile değiştirildi                     |
| **Başka bir özellik ile değiştirildi?** | Evet, çekirdek Gelen konsinye işlevselliği |
| **Etkilenen modüller**             | Borç hesapları, Stok yönetimi          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Doğu Avrupa için mali rapor oluşturucusu

Muhasebe ve vergi raporları için veri toplamak ve XLS ve DOC rapor şablonlarına veri dışa aktarmak için bir araç kullanılır.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Sınırlı kullanım                                                                            |
| **Başka bir özellik ile değiştirildi?** | Hayır. Araç gelecekteki sürümlerde Elektronik raporlama yapılandırmaları ile değiştirilecektir. |
| **Etkilenen modüller**             | Genel Muhasebe                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Finlandiya için müşteri ödeme hareketlerini içe aktarma

Finlandiya ödemelerinde müşteri ödeme hareketlerini banka tarafından sağlanan harici bir dosyadan içe aktarmak için bir içe aktarma biçimi seçebilirsiniz.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellik ile değiştirildi?** | Hayır. Biçim gelecekteki sürümlerde ISO 20022 ekstre içe aktarma biçimleri ile değiştirilecektir. |
| **Etkilenen modüller**             | Alacak hesapları                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Finlandiya için ödeme hareketlerini genel muhasebe günlüğüne içe aktarma

Muhasebe hareketlerini genel muhasebeye içe aktarmak için Finlandiya'ya özgü bir biçim kullanılır.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimi artık kullanılmamaktadır.                                                     |
| **Başka bir özellik ile değiştirildi?** | Hayır. Biçim gelecekteki sürümlerde ISO 20022 ekstre içe aktarma biçimleri ile değiştirilecektir. |
| **Etkilenen modüller**             | Alacak hesapları                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Belçika için Isabel ile tümleştirme eşitlendi (CIS)

Isabel, elektronik bankacılık için Avrupa'daki çerçevedir ve Belçika'da fiili bir standarttır.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Isabel istemcisi ile tümleştirme kaldırıldı.                                                                |
| **Başka bir özellik ile değiştirildi?** | Hayır. Belçika için artık kullanılmayan ödeme biçimleri, ISO20022 Alacak transferi ödeme biçimi ile değiştirildi. |
| **Etkilenen modüller**             | Borç hesapları                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>İspanya için hesap planı ve muhasebe kurallarındaki değişiklikler

Bu özellik, İspanya için hesap planında ve muhasebe kurallarındaki değişiklikler için kullanılır. Eski hesap planını yeni hesap planına dönüştürmeye yardımcı olmak için hesapları eşler ve farklı hesap numaralarına nakledilseler bile önceki mali yıl ile yeni mali yılı karşılaştırır.

|                              |                |
|------------------------------|----------------|
| **Kaldırılma nedeni**       | Sınırlı kullanım  |
| **Başka bir özellik ile değiştirildi?** | Hayır             |
| **Etkilenen modüller**             | Genel muhasebe |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Pagamento Fornittori satıcı ödemesi biçimi

Alacak transferleri için eski İtalyan ödeme biçimi.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimi artık kullanılmamaktadır.                  |
| **Başka bir özellik ile değiştirildi?** | Evet, İtalya için ISO20022 Alacak transferi ödeme biçimi |
| **Etkilenen modüller**             | Borç hesapları                                       |

### <a name="payment-export-formats-for-estonia"></a>Estonya için ödemeleri dışa aktarma biçimleri

Telehansa ve Teleservice biçimleri banka ödemesi dışa aktarımı için kullanılır.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Kaldırılma nedeni**      | Ödeme biçimleri artık kullanılmamaktadır.                  |
| **Başka bir özellik ile değiştirildi?** | Evet, Estonya için ISO20022 Alacak transferi ödeme biçimi |
| **Etkilenen modüller**             | Borç hesapları                                         |

### <a name="payment-file-archive-for-norway"></a>Norveç için ödeme dosya arşivi

Ödeme dosyaları oluşturulduğunda dosya arşivi, dosyalar önceden yazılmış veya okunmuş olsalar bile oluşturulan tüm dosyaları otomatik olarak arşivler.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Başka bir özellik ile değiştirildi                                        |
| **Başka bir özellik ile değiştirildi?** | Evet, Arşivlenen elektronik raporlama işleri                            |
| **Etkilenen modüller**             | Borç hesapları, Alacak hesapları, Organizasyon yönetimi |

### <a name="payment-import-formats-for-estonia"></a>Estonya için ödemeleri içe aktarma biçimleri

Telehansa ve TeleTeenus biçimleri banka ödemesi içe aktarımı için kullanılır.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimleri artık kullanılmamaktadır.                                                    |
| **Başka bir özellik ile değiştirildi?** | Hayır. Biçimler gelecekteki sürümlerde ISO 20022 ekstre içe aktarma biçimleri ile değiştirilecektir. |
| **Etkilenen modüller**             | Alacak hesapları                                                                        |

### <a name="performance-management-goal-workflow"></a>Performans yönetimi hedefi iş akışı

Performans yönetimi, hedef yönetimini ve performans gözden geçirmeleri ile tümleştirmeyi içerir.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Performans yönetimi yeniden tasarlanmıştır ve hedef sayfalarının sayısı işlemi basitleştirecek şekilde azaltılmıştır.                 |
| **Başka bir özellik ile değiştirildi?** | Hayır. Hedefler yöneticiler tarafından Yönetici Self Servis portalından görülebilir, değiştirilebilir ve görüntülenebilir. |
| **Etkilenen modüller**             | İnsan sermayesi yönetimi                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>İsveç için Postgirot ve Postgirot Utland ödeme biçimleri

İsveç için Postgirot ve Postgirot Utland ödeme biçimleri.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimleri artık kullanılmamaktadır.                 |
| **Başka bir özellik ile değiştirildi?** | Evet, İsveç için ISO20022 Alacak transferi ödeme biçimi |
| **Etkilenen modüller**             | Borç hesapları                                        |

### <a name="radio-frequency-identifier"></a>Radyo frekansı kimlik tanımlayıcı

Radyo Frekans Kimlik Belirleme (RFID), kimlik bilgilerini saklamak için elektronik etiket kullanan ve okuyucunun kimlik saptama verisini yakalaması için doğrudan yöneltmeye gerek duymayan bir veri toplama teknolojisidir.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Kaldırılma nedeni**       | Düşük müşteri kullanımı ve sınırlı özellik kümesi. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                            |
| **Etkilenen modüller**             | Stok Yönetimi                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Letonya için Fatura numarasının belirtilmesi hakkında rapor

Letonya mevzuatı satış faturalarının numaralandırılması hakkında belirli kurallar sağlar. İşlev, kullanıcı veya kullanıcı grubuna göre satış faturalarına belirli numaralar atamanızı sağlar. Ardından bir rapor veya bir XML dosyası oluşturabilirsiniz. Ayrıca, kullanılan fatura numaraları hakkında bir rapor yazdırabilirsiniz.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Artık fatura numarasının belirtilmesinin saklanması gerekmez. Kullanılan fatura numaraları hakkında rapor artık gerekli değildir. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                                                       |
| **Etkilenen modüller**             | Alacak hesapları                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Litvanya için yönetici adları ve bir şirketin genel muhasebesini ayarlama

Yönetici adları ve şirketin genel muhasebesi şirket bilgilerinde belirtilebilir ve farklı yerel rapor çıktılarında kullanılabilir.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Kaldırılma nedeni**       | Başka bir özellik ile değiştirildi                                     |
| **Başka bir özellik ile değiştirildi?** | Evet, yetkililer kurulumu aynı amaç için kullanılabilir.   |
| **Etkilenen modüller**             | Borç hesapları, Alacak hesapları, Nakit ve banka yönetimi |

### <a name="telepay-payment-formats-for-norway"></a>Norveç için Telepay ödeme biçimleri

Telepay ödeme biçimleri, satıcı ödemesi dışa aktarımını (alacak transferi) ve müşteri ödeme tahsilatını (otomatik ödeme) içerir.

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimleri artık kullanılmamaktadır.                                                        |
| **Başka bir özellik ile değiştirildi?** | Evet, Norveç için ISO20022 Alacak transferi ödeme biçimi ve AvtaleGiro müşteri ödeme biçimi |
| **Etkilenen modüller**            | Borç hesapları, Alacak hesapları                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Finlandiya için satıcı ödeme dışa aktarma biçimleri

Finlandiya için ödemeleri dışa aktarmak üzere iki biçim kullanılabilir. Yurtiçi ödemeleri için kullanılan LM02 (FI) ve yurtdışı ödemeleri için kullanılan LUM2 (FI).

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Kaldırılma nedeni**       | Ödeme biçimleri artık kullanılmamaktadır.                  |
| **Başka bir özellik ile değiştirildi?** | Evet, Finlandiya için ISO20022 Alacak transferi ödeme biçimi |
| **Etkilenen modüller**            | Borç hesapları                                         |

### <a name="workflow-for-creating-goals"></a>Hedefleri oluşturmak için iş akışı

Personel hedeflerini oluşturmayı yöneten iş akışı, performans yönetim işleminin düzenlenmesine yardımcı olan birkaç iş akışından biridir.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Performans yönetimi, Microsoft Dynamics for Finance and Operations'da tamamen yeniden tasarlanmıştır.                                                                                                                                                                                                                                        |
| **Başka bir özellik ile değiştirildi?** | Yeniden tasarlanan Performans yönetimi özelliği hedef içeriği, ilerlemeyi izlemek için kullanılan ölçümler ve destekleyici belge eki üzerinde daha fazla kontrol sağlar. Hedefler şablon olarak saklanabilir ve daha sonra yeniden kullanılabilir. Bu özellik personeliniz için ek hedefleri daha hızlı bir şekilde ayarlamanıza yardımcı olabilir. |
| **Etkilenen modüller**            | İnsan sermayesi yönetimi                                                                                                                                                                                                                                                                                                               |

## <a name="features-that-have-been-deprecated-in-dynamics-ax-70-releases"></a>Dynamics AX 7.0 sürümlerinde kaldırılmış olan özellikler

### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Satıcı faturasında yapılan değişiklikleri iptal yeteneği

|                              |                         |
|------------------------------|-------------------------|
| **Kaldırılma nedeni**       | Performans geliştirmesi |
| **Başka bir özellik ile değiştirildi?** | Hayır                      |
| **Etkilenen modüller**            | Borç hesapları        |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD ve AxBC entegrasyonlar

Uygulama Tümleştirme Çerçevesi (AIF) içerisinde veriler, hizmetler olarak gösterilen iş mantığı üzerinden dış sistemlerle değiştirilebilir. Dynamics AX, .NET Business Connector (AxBC) ve belgelere dayanan hizmetleri içerir. Bir belge, XML kullanılarak oluşturulur. XML, bir *ileti* oluşturmak için eklenen ve Dynamics AX içine veya dışına transfer edilebilen üstbilgi bilgilerini içerir. Belgelerin örnekleri satınalma siparişleri ve satış siparişlerini içerir. Ancak, bir müşteri gibi hemen hemen her varlık, bir belge tarafından temsil edilebilir. Belgelere dayanan hizmetler **Axd &lt;*Belge*&gt;** sınıflarını kullanır.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | AIF ve AxDs mimarileri bir bulut hizmetine ölçeklenmiş değildirler. Toplu alma etrafında performans sorunları vardı.                                                                               |
| **Başka bir özellik ile değiştirildi?** | Dynamics AX'in geçerli sürümünde, bu özelliğin yerini tekrar eden toplu alma/vermeleri destekleyen Veri Alma/Verme çerçevesi almıştır. AxBC için gerçek tabloları kullanmanızı öneririz. |
| **Etkilenen modüller**             | AxDs, AxBCs ve AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Ürün reçetesi sürümleri olmayan ürün reçeteleri

**BOM sürümleri** yapılandırma anahtarı devre dışı bırakıldığında, ürün reçetesi (BOM) sürümleri tüm formlarda gizleniyordu ve sistem serbest bırakılan ürünler ve ürün reçeteleri arasında bir 1:1 ilişkisini zorluyordu. **BOM sürümleri** yapılandırma anahtarı, Dynamics AX'in geçerli sürümünde devre dışı bırakılamaz.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**      | Ürün reçetesi sürümlerini denetlemek için konfigürasyon anahtarı kullanmak bir bulut ortamında ölçeklendirilemez. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                      |
| **Etkilenen modüller**            | Ürün bilgileri yönetimi, Stok Yönetimi                                    |

### <a name="brazilian-bordero"></a>Brazilian Bordero

Brezilya şirketleri için belirli ödeme yöntemi

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Brazilian Bordero ödeme yöntemi için destek Brezilya yerelleştirmesinden kaldırılmıştır |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                                    |
| **Etkilenen modüller**             | Borç hesapları                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brazilian Sintegra ekstresi

ICMS vergisi için federal vergi ekstresi

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Bu ekstre bazı Brezilya eyaletlerinde artık kullanılmamaktadır.                                                     |
| **Başka bir özellik ile değiştirildi?** | Hayır. Kullanıcılar Genel Elektronik raporlama aracını belirli durumlarda gerektiğinde ekstreyi yapılandırmak için kullanabilir. |
| **Etkilenen modüller**             | Mali defterler                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>NF-e için Brezilya SCAN yedeği modu

(SCAN) yedeği ortamı, Secretaria da Fazenda (SEFAZ) ortamı kullanılabilir olmadığında bir Nota Fiscal eletrônica (NF-e) durumunu oluşturmak, dışa aktarmak ve içe aktarmak için kullanılır.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Bu yedek yöntem, Brezilya eyaletlerinin tamamında artık geçersizdir |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                          |
| **Etkilenen modüller**             | Alacak hesapları                                                         |

### <a name="business-analyzer"></a>İş Çözümleyicisi

Bu mobil uygulama kullanıcıların anahtar iş ölçümlerini gözden geçirmelerini sağlar.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Bu işlev başka bir özellik ile değiştirilmiştir.                                                                                                      |
| **Başka bir özellik ile değiştirildi?** | Microsoft Power BI için Finansal performans içeriği izleme paketi, daha önce Business Analyzer'da bulunan önemli mali ölçümleri içerecektir. |
| **Etkilenen modüller**             | Genel muhasebe                                                                                                                                                |

### <a name="business-statistics"></a>İşletme istatistikleri

Kuruluşun performansını analiz etmenize yardımcı olabilecek iş istatistiği sorgularının kurulumu

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | İş zekasına (BI) eski yaklaşım, düşük müşteri kullanımı ve sınırlı özellik kümesine |
| **Başka bir özellik ile değiştirildi?** | Dynamics AX'in geçerli sürümü için yeni BI çözümleri                                      |
| **Etkilenen modüller**             | Tedarik ve kaynak hizmeti, Borç hesapları, Satış ve pazarlama, Alacak hesapları         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Fatura onay günlüğündeki belge tarihi değiştirme işlevi

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Düşük kullanım                                                               |
| **Başka bir özellik ile değiştirildi?** | Evet. Deftere nakledilen satıcı hareketi üzerindeki belge tarihi değiştirilebilir. |
| **Etkilenen modüller**             | Borç hesapları                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Hollanda için ClieOp03 ödeme biçimi

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Hollanda'da artık geçerli değildir. |
| **Başka bir özellik ile değiştirildi?** | SEPA ödemeleri dışa aktarımı                                                                                       |
| **Etkilenen modüller**             | Tümü                                                                                                        |

### <a name="compliance-center"></a>Uyumluluk Merkezi

Uyumluluk Merkezi, Sarbanes-Oxley Yasası ilgili uyumluluk girişimleriyle belgelerine gereksinimlerini yönetmek kullanılan bir Kurumsal Portal sitesiydi.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Müşteri kullanım eksikliği. Microsoft SharePoint Uyumluluk Merkezi'nde sunulmuş olanlarla aynı özellikleri içerir. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                                                     |
| **Etkilenen modüller**             | Uyumluluk ve dahili kontroller                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamics için Bağlayıcı

Bu araç, anahtar verileri Microsoft Dynamics CRM'den Microsoft Dynamics ERP uygulamalarına tümleştirmek için kullanıldı.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Kaldırılma nedeni**       | Bu işlev başka bir özellik ile değiştirilmiştir. |
| **Başka bir özellik ile değiştirildi?** | Dynamics integral alıcı                                      |
| **Etkilenen modüller**             | Microsoft Dynamics için Bağlayıcı                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Eldeki konteyner birimi ve çoklu boyut

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Tekrar eden işlevsellik                                                                                                                                         |
| **Başka bir özellik ile değiştirildi?** | Evet. AX 2012'den itibaren bu işlevin yerini konsolide toplu iş siparişleri özellik kümesi almıştır. Bu özellik kümesi konsolide eldeki görünümünü içerir. |
| **Etkilenen modüller**             | Ürün bilgileri yönetimi, Üretim kontrol, Stok Yönetimi, Satış ve pazarlama                                                                   |

### <a name="cue-group-metadata"></a>İşaret Grup meta verileri

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | İşaret grupları, bilgi alanında bir veya daha fazla ipucu görüntülemek için kullanılıyordu. Sınırlı kullanım vardı ve ayrıca performans kaygıları da mevcuttu çünkü bir üst formdaki değişiklik, her İşaret grubundaki her bir İşarette bir sorguya sebep oluyordu. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                                                                                                                                                            |
| **Etkilenen modüller**             | Tümü                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>İşaret meta verileri

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | İşaret meta veriler, sayma ve toplama bilgileri ile sınırlıydı.                                                                                                                                                                                   |
| **Başka bir özellik ile değiştirildi?** | Döşeme meta veri modelleme için daha fazla esneklik sağlamak amacıyla kullanılmaya başlandı. Örneğin, geçerli sayma, gezinti ve anahtar performans göstergeleri (APG) modelleyebilirsiniz. Sayım döşeme meta verileri, işaret meta verilerinin doğrudan yerini almıştır. |
| **Etkilenen modüller**             | Tümü                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Danimarka çek biçimi

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Danimarka çek biçimi düzeni için destek kaldırılmıştır ve rapor DK yerelleştirmeden silinmiştir. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                                                      |
| **Etkilenen modüller**             | Tümü                                                                                                                     |

### <a name="data-partitions"></a>Veri bölümleri

Veri bölümleri, Microsoft Dynamics AX veritabanındaki verinin mantıksal bir ayrımını sağlar.

|   |   |
|---|---|
| **Kaldırılma nedeni**       | Veri bölümleri, veri yalıtımı sağlamak için Microsoft Dynamics AX 2012 R2'de kullanılmaya başlanmıştır. Yaygın bir senaryoda, bir şirketin bağlı kuruluşları vardır ve her iki bağlı kuruluş da aynı BT departmanı tarafından yönetilseler bile bir bağlı kuruluşun verisinin diğer bağlı kuruluşa görünür olmaması gerekir. Ancak, yeni bölümler oluşturmak, bunları veri ile doldurmak ve bölüm verilerini yedeklemek için ekstra kodlar ve program boyunca genel yönetim giderleri gerekir. Hizmet olarak platform (PaaS) veritabanına (Microsoft Azure SQL veritabanı) erişimimizin olduğu bulutta, veritabanını bir yalıtım konteyneri olarak kullanmak program içinde yalıtmaya göre çok daha etkilidir. Veri bölümlemenin bağlı kuruluşlar, çoklu kiracılar veya yalnızca ölçek için gerekli olup olmadığına bakılmaksızın, senaryoların birden çok veritabanı veya birden çok Dynamics AX kurulumları ile daha iyi işlenebileceğine inanırız. |
| **Başka bir özellik ile değiştirildi?** | Veri bölümleri, birden çok veritabanı veya Dynamics AX kurulumları için destek aracılığıyla ileriki bir sürümde değiştirilecektir.    |
| **Etkilenen modüller**             | Tümü  |

### <a name="database-and-file-share-storage-for-attachments"></a>Ekler için veritabanı ve dosya paylaşım depolama
Microsoft Dynamics AX 2012, eklerin veritabanında ve dosya paylaşımında depolanmasına izin vermekteydi. Bu seçeneklerin her ikisi de artık desteklenmiyor.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Kaldırılma nedeni**       | Dosya paylaşım depolaması, bulutta barındırılan ortamlar yerel dosya paylaşımlarıyla iletişim kuramadığı için artık desteklenmiyor. Veritabanı depolama, Azure Blob depolama kullanıldığından kullanım dışı bırakıldı. Azure Blob depolama, veritabanında depolamaya eşdeğerdir çünkü belgeler yalnızca Dynamics 365 for Finance and Operations istemci formları üzerinden erişilebilir. Bu, veritabanı performansını olumsuz etkilemeyen depolama sağlama faydasını sunar. Blob depolama, Belge Yönetimi için varsayılan mekanizmadır ve hemen çalışır. |
| **Başka bir özellik ile değiştirildi?** | Veritabanı depolama, Azure Blob depolama kullanıldığından kullanım dışı bırakıldı.       |
| **Etkilenen modüller**             | Tümü                   |

### <a name="delimitation"></a>Sınırlandırma

|                              |                                        |
|------------------------------|----------------------------------------|
| **Kaldırılma nedeni**       | İşlev için kullanım bulunamadı. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                     |
| **Etkilenen modüller**             | Saat ve işe devam                    |

### <a name="desktop-client"></a>Masaüstü istemcisi

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Dynamics AX İstemci deneyimi, platformlar ve aygıtlar üzerinde kullanılabilirliğini artırmak için tasarlanmıştır.                      |
| **Başka bir özellik ile değiştirildi?** | Yeni web istemci masaüstü formu meta verileri ve zengin web platformu sunmak için değiştirilmiş programlama modeline dayanır. |
| **Etkilenen modüller**             | Tümü                                                                                                                                    |

### <a name="direct-database-connection"></a>Doğrudan veritabanı bağlantısı

Dynamics AX 2012 R3 içerisinde, Perakende Modern POS, Kanal Veritabanına, Kuruluş POS'a benzer şekilde doğrudan bağlanamadı. Bu, Perakende Modern POS'un, Perakende Sunucusu üzerinden iletişim kurarken standart iletişim yöntemine ek olarak oluştu.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Doğrudan veritabanı bağlantısı, daha düşük güvenlik protokolleri gerektirdi ve öncelikli olarak en yüksek seviye performansı elde etmek için kullanıldı. Finance and Operations içerisinde gerçekleşen performans ve güvenlik geliştirmeleri yüzünden, bu işlev artık çözdüğünden daha fazla soruna neden olmaktadır. |
| **Başka bir özellik ile değiştirildi?** | Hayır. Artık yalnızca standart Perakende Sunucu iletişimi desteklenmektedir.    |
| **Etkilenen modüller**             | Kanal Veritabanı/Perakende Modern POS                                    |

### <a name="dutch-swift-mt940"></a>Felemenkçe SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Yerelleştirilmiş işlevsellik yerine artık genel işlevler kullanılır.                                                                                                                                                                 |
| **Başka bir özellik ile değiştirildi?** | Evet, bu işlevin yerini Gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen modüller**             | Tümü                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (Almanya için XBRL)

Bu işlev Alman eBilanz taksonomisi için özel olarak tasarlanmış olan Genişletilebilir İş Raporlama Dili (XBRL) çıkışı sağlamaktaydı.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Müşteri kullanım eksikliği                                                                                                                                                 |
| **Başka bir özellik ile değiştirildi?** | Bu özelliğin yerini bir başkası almadı ancak Almanya pazarı için zengin XBRL işlevselliği sağlayan birden çok özelleşmiş XBRL paketi sunulmuştur. |
| **Etkilenen modüller**             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Kurumsal Portal istemcisi

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Bir tek istemci platformu sağlandı.                                                                                            |
| **Başka bir özellik ile değiştirildi?** | Yeni web istemci masaüstü formu meta verileri ve zengin web platformu sunmak için değiştirilmiş programlama modeline dayanır. |
| **Etkilenen modüller**             | Tümü                                                                                                                                    |

### <a name="environmental-sustainability"></a>Ortam sürdürülebilirliği

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| **Kaldırılma nedeni**       | Düşük müşteri kullanımı ve sınırlı özellik kümesi       |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                 |
| **Etkilenen modüller**             | Uyumluluk ve dahili kontroller, Borç hesapları |

### <a name="form-activex-and-managed-host-controls"></a>Form ActiveX ve yönetilen konak denetimleri

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | ActiveX ve yönetilebilir konak denetimleri artık kullanılmayan masaüstü istemciyi temel alır.                                                                                                             |
| **Başka bir özellik ile değiştirildi?** | Genişletilebilir denetim çerçevesi HTML, CSS ve JavaScript'e dayanan yeni denetimleri oluşturmayı destekler ve Microsoft Visual Studio Tooling ortamındaki birinci sınıf bir denetimdir. |
| **Etkilenen modüller**             | Tümü                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Bir toplu işlem kullanarak açık provizyon oluşturmak

Açık provizyon oluşturma, bir toplu iş kullanarak yapılamaz ancak hala bir kullanıcı tarafından yapılabilir.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Toplu iş kullanılarak oluşturulduğunda, ortaya çıkan açık provizyon dosyasını ısrar edip görüntülemek için form bulunmamaktadır. |
| **Başka bir özellik ile değiştirildi?** | Açık provizyonlar hala oluşturulabilir ve kullanıcı dosyanın kaydedildiği yeri denetleyebilir.   |
| **Etkilenen modüller**             | Borç hesapları, Alacak hesapları, Nakit ve banka yönetimi                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Almanca DTAUS ödeme dışa aktarma ve hesap ekstresi içeri alma (toplamları ve hareketler)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Almanya'da artık geçerli değildir.                                                                                                                                                                 |
| **Başka bir özellik ile değiştirildi?** | Evet, bu özelliğin yerini SEPA ödeme dışa aktarma ve hesap ekstrelerini içeri aktarma için gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen modüller**             | Tümü                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Alman DTAZV ödeme biçimi

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Biçim, artık tek Euro ödemeleri alan (SEPA) işlevi tarafından değiştirildiğinden, Almanya'da artık geçerli değildir. |
| **Başka bir özellik ile değiştirildi?** | SEPA ödemeleri dışa aktarımı                                                                               |
| **Etkilenen modüller**             | Tümü                                                                                                |

### <a name="german-mt940-import"></a>Almanca MT940 içe aktarımı

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Yerelleştirilmiş işlevsellik yerine artık genel işlevler kullanılır.                                                                                                                                                                 |
| **Başka bir özellik ile değiştirildi?** | Evet, bu işlevin yerini Gelişmiş banka mutabakatı işlevi aldı. |
| **Etkilenen modüller**             | Tümü                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Alman XML AB Satışlar listesi

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Almanca AB Satış Listesi raporlaması için XML biçimi artık desteklenmiyor. Alman Vergi Dairesi'ne AB Satış Listesi raporunu göndermek için yalnızca ELMA5 metin dosyası biçimi kullanılabilir. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                                                                                                                 |
| **Etkilenen modüller**             | Vergi                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>GL SSRS raporları

Aşağıdaki menü öğelerini içeren raporlar kaldırıldı: **Özet mizan**, **ayrıntılı mizan**, **hesap planı**, **denetim izi**, **bakiyeler**, ve **bakiye listesi**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Mali Microsoft SQL Server Raporlama Servisleri (SSRS) raporlarının yeri, Yönetimi Raporlayıcı'sı yetenekleri ve varsayılan raporlar tarafından alınmıştır. |
| **Başka bir özellik ile değiştirildi?** | Yönetim Raporlayıcı (Dynamics AX'ın geçerli sürümünde **finansal raporlama** etiketli)                                                  |
| **Etkilenen modüller**            | Genel muhasebe                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>InfoPart ve FormPart meta verileri

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | InfoPart ve FormPart meta verileri, iki farklı istemci için bilgi kutularının oluşturulması sağlardı.                                                                                                                                    |
| **Başka bir özellik ile değiştirildi?** | Basitleştirilmiş form tanımı olan InfoPart meta verileri, forma yükseltme araç kullanımı tarafından dönüştürülür. Bir forma referans gösteren FormPart meta verileri, yükseltme araçları tarafından daha doğrudan bir referans ile değiştirildi. |
| **Etkilenen modüller**             | Tümü                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Ana hesap liste sayfası

Tüzel kişilik ve ilgili bakiye bilgilerini hesapların listesi

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Bakiye bilgisi **Mizan** liste sayfasında hesap ve boyut olarak bulunabilir.                                                                                      |
| **Başka bir özellik ile değiştirildi?** | **Ana hesaplar**,**Ana hesap** sayfasında yer alan hesapların listesinin aynısını içerir. **Ana hesaplar**'daki ızgara görünümü daha da küçük ızgaraya benzer bir görünümü gösterir. |
| **Etkilenen modüller**             | Genel muhasebe                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malezya ve Singapur banka nakit akışı raporu

Seçili banka hesapları için belirli bir tarih aralığındaki hareketlerin nakit giriş ve çıkış ayrıntılarını gösteren bir nakit akış raporu kullanıcı tarafından yazdırılabilir.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Aynı bilgileri sorgulama banka hareketinden de elde edilebilir. |
| **Başka bir özellik ile değiştirildi?** | Sorgulama banka hareketi                                            |
| **Etkilenen modüller**             | Nakit ve banka yönetimi                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Meksika CFD elektronik fatura

Bu özellik, şirketin faturayı hükümetten ilgili izni isteyerek imzaladığı Comprobante Fiscal Digital (CFD) yöntemini kullanarak Meksika elektronik fatura oluşturmayı etkinleştirir. Bu özellik ayrıca bir dönemde çıkarılan tüm elektronik faturaları içeren aylık bir rapor sunar.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Yöntemi artık geçerli değil. CFG yöntemini kullanarak elektronik faturaların oluşturulması vergi otoriteleri tarafından kaldırılıp yerine imzalamanın üçüncü taraf bir sağlayıcıya (PAC) devredildiği Comprobante Fiscal Digital a través de Internet (CFDI) metodu getirilmiştir. Aylık rapor kaldırıldı ve kullanıcıların geçmiş hareketler hakkında bilgi alması için sorgu seçeneği geliştirildi. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Etkilenen modüller**             | Alacaklar hesabı, Proje                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksika gerçekleşmiş ve gerçekleşmemiş KDV

Microsoft Dynamics AX 2012 gerçekleşmemiş katma değer vergisi (KDV) Meksika özgü "gerçekleşmemiş vergi için" işlevselliğini kullanarak yönetiyordu.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Tekrar eden işlevsellik                                                                                             |
| **Başka bir özellik ile değiştirildi?** | Evet, bu işlevin yerini Çekirdek tarafından sağlanan standart koşullu satış vergisi işlevleri aldı. |
| **Etkilenen modüller**             | Vergi                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook entegrasyonu

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Bu işlevin yerini Microsoft Exchange Server tümleştirmesi almıştır. |
| **Başka bir özellik ile değiştirildi?** | Evet                                                                            |
| **Etkilenen modüller**             | Satış ve pazarlama                                                            |

### <a name="payroll-information-in-human-resources"></a>İnsan Kaynakları'ndaki bordro bilgileri

İnsan Kaynakları bordro bilgileri

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Bu işlevin yerini temel Bordro ve İnsan Kaynakları sayfaları almıştır.                                                                                                                                                                                                                                              |
| **Başka bir özellik ile değiştirildi?** | **Avantajlar**, **Kazançlar** ve daha önce ABD Bordro'da olan diğer ilgili sayfalar yeniden yapılandırıldı ve artık harici bordro işlemeyi desteklemeye yardımcı olacak temel İnsan Kaynakları yapılandırmasının bir parçasılar. Bu işleve **İnsan Kaynakları 1** &gt; **Bordro** konfigürasyon anahtarı kullanılarak erişilir. |
| **Etkilenen modüller**             | İnsan kaynaklarını, Bordro                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Stok ve Ambar yönetim günlüklerinin özel durdurması

Stok ve Ambar günlükleri, günlüğün seçili kullanıcı için özel olarak işaretleme özelliğini artık desteklememektedir. Yalnızca kullanıcı grupları için özel olarak günlükleri engelleme ve düzenleme sırasında engelleme işlemi desteklenir.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Kaldırılma nedeni**       | İşlev için kullanım bulunamadı. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                     |
| **Etkilenen modüller**             | Stok yönetimi                   |

### <a name="product-builder"></a>Ürün oluşturucu

Ürün Oluşturucu, bir satış siparişi, satınalma siparişi, üretim emri, satış teklifi, proje teklifi veya madde gereksinimi öğelerinden dinamik olarak ürün yapılandırmak için kullanılıyordu. Model oluşturma değişkenleri olan bir ürün modeline bağlı olarak, kullanıcı, müşteri gereksinimlerini karşılamak için bir ürün reçetesi ve rotası olan benzersiz bir ürün çeşidi sağlamak için değerler seçebiliyordu.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Ürün Oluşturucu X ++ kodunu son kullanıcılara yansıtıyordu ve Dynamics AX'ın geçerli sürümünde desteklenmiyor. Büyük ve kesişen kod tabanlarında sürdürme çabalarının ikiye katlanmaması için kaldırıldı. |
| **Başka bir özellik ile değiştirildi?** | Ürün yapılandırması                                                                                                                                                                                   |
| **Etkilenen modüller**             | Ürün bilgileri yönetimi, satış ve pazarlama                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Ürün boyutunu yeniden adlandır

Bu özellik, üç standart ürün boyutundan (boyut, renk veya stil) birinin adını işletme gereksinimlerinize daha iyi uygun bir adla değiştirmenize olanak sağlar. Yeniden adlandırma, ürün boyut adının kullanıldığı tüm etiketlere dahildir.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Dynamics AX geçerli sürümününde, çalıştırma sırasında etiket değişikliklerini desteklemez. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                            |
| **Etkilenen modüller**             | Ürün bilgileri yönetimi                                                |

### <a name="retail-server-connectivity-using-http"></a>HTTP kullanarak Perakende Sunucu bağlantısı

Dynamics AX 2012 R3 içerisinde, Perakende Sunucu, HTTP iletişimi (güvenli olmayan) kullanarak işlev sağlayamıyordu. Bu, HTTPS kullanan standart iletişime ek olarak oluştu.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Yeni güvenlik gereksinimleri nedeniyle, yalnızca TLS 1.2 (veya kullanılabilir olduğu takdirde üstü) artık desteklenmektedir. Self servis yükleyici, bilgisayarı bu iletişim için otomatik yapılandıracaktır. |
| **Başka bir özellik ile değiştirildi?** | Hayır. Artık yalnızca standart HTTPS iletişimi desteklenmektedir.                                                                           |
| **Etkilenen modüller**             | Perakende Sunucusu                                                |

### <a name="role-center-pages"></a>Rol Merkezi sayfaları

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Rol Merkezi sayfaları, kaldırılan Enterprise Portal platformu üzerine kurulmuştu ve Dynamics AX'ın geçerli sürümünde yeni web istemci platformu tarafından yenilendi. |
| **Başka bir özellik ile değiştirildi?** | Yeni çalışma alanı form düzeni kullanıcılara işlem merkezli tasarıma sahip, sık kullanılan işlemlere kolay erişim sağlayan bir işlem merkezli tasarımı sağlar.                       |
| **Etkilenen modüller**             | Tümü                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Satış vergi daireleri

|                              |                                              |
|------------------------------|----------------------------------------------|
| **Kaldırılma nedeni**       | Düşük müşteri kullanımı ve sınırlı özellik kümesi |
| **Başka bir özellik ile değiştirildi?** | Hayır                                           |
| **Etkilenen modüller**             | ABD satış vergisi                                 |

### <a name="shipping-carrier-interface"></a>Sevkiyat taşıyıcısı arabirimi

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Tekrar eden işlevsellik                                                                                                                         |
| **Başka bir özellik ile değiştirildi?** | Evet, bu özellik kısmen Taşıma yönetimi ile değiştirildi ancak henüz temel Ambar yönetimi (WMS I) ile değiştirilmedi. |
| **Etkilenen modüller**             | Satış ve pazarlama, Stok Yönetimi                                                                                                       |

### <a name="sites-services"></a>Site Servisleri

Site Hizmetleri, BT desteği olmadan iş süreçlerinizi internete genişleten web siteleri kurmanıza olanak sağlar.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Dynamics AX tarafından kullanılan Microsoft Azure altyapısı, alternatif olarak kullanılabilecek yeni özelliklere sahiptir (örneğin, Azure siteleri). |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                                                                                                       |
| **Etkilenen modüller**             | İK işe alma, Vaka yönetimi, Teklif talebi, Satıcı kaydı                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSASS talep tahmin stratejisi

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Özelliğin tasarımı yeni bulut mimarisinde desteklenemez. |
| **Başka bir özellik ile değiştirildi?** | Azure Makine Öğrenimi talep tahmini stratejisi                           |
| **Etkilenen modüller**             | Planlama                                                                     |

### <a name="travel-requisitions"></a>Seyahat talepleri

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Kaldırılma nedeni**       | Düşük kullanım ve Kurumsal Portal içinde işlevlerin çoğunun mevcut olması. |
| **Başka bir özellik ile değiştirildi?** | Hayır                                                              |
| **Etkilenen modüller**             | Gider yönetimi                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Deftere nakledilen ayrıntılar hariç satıcı faturası havuzu

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Düşük kullanım. Bu özelliğin yerini iş akışı işlevine sahip Fatura günlüğü almıştır. |
| **Başka bir özellik ile değiştirildi?** | Fatura günlüğünün iş akışı özellikleri.                                                           |
| **Etkilenen modüller**             | Borç hesapları                                                                                        |

### <a name="virtual-company-accounts"></a>Sanal şirket hesapları

Sanal şirketler özelliği, Dynamics AX uygulamasında artık desteklenmiyor. Sanal şirketler özelliği, kullanıcılara bir dizi şirket tarafından paylaşılabilecek tablolar ayarlama olanağı sağlar. Özelliğin açıklaması için bkz. [Şirket hesapları ve Sanal şirket hesapları](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Bu özellik, tabloları, varolan "gerçek" şirketlerin grupları olan sanal şirketlere atanan koleksiyonlara gruplayarak çalışmaktadır. Sanal şirketteki tüm şirketlerin ilişkilendirilen tablo koleksiyonlarının tabloları içindeki verilere erişebileceği şekilde sorgular oluşturulur.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><b>Kaldırılma nedeni</b></td>
<td><ul>
<li>Tablolarda verilerin depolanmasından önce sanal şirketlerin ayarlanmış olması gerekir. Sanal şirketleri mevcut bir uygulamaya uyarlamak oldukça güçtür.</li>
<li>Dynamics AX'in geçerli sürümünde çok fazla veri normalleştirmesi olduğundan, tablo koleksiyonlarına nelerin eklenmesi gerektiğini bilmek çok zor hale geldi. Örneğin, hangi tabloların paylaşılacağını bilmek zor. Bir sanal şirketteki tablolardan referans alınan tüm tabloların da ayrıca eklenmesi gerekir. Tablo normalleştirmesi nedeniyle, çok sayıda tabloya yayılan basit master verilerin bile sanal şirketin parçası haline gelmesi gerekiyor. Burada yapılan herhangi bir hata, işlevsel sorunlara neden olur.</li>
<li>Bir tablo bir sanal şirketin parçası olduğunda, veri kaynağı hakkındaki bilgiyi kaybeder ve sadece sanal şirket kaydedilir.</li>
</ul></td>
</tr>
<tr class="even">
<td><b>Başka bir özellik ile değiştirildi?</b></td>
<td>Tabloları tüm şirketlerden erişebilir hale getirmek için global tablolar kullanılabilir. Şu anda bir değişiklik yoktur.</td>
</tr>
<tr class="odd">
<td><b>Etkilenen modüller</b></td>
<td>Geçerli değil</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Ambar yönetimi II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | **Stok yönetimi** modülünde bulunan Ambar yönetimi II çözümü (WMS II), Microsoft Dynamics AX 2012 R3'te yayınlanmış olan **Ambar yönetimi** modülündeki işlevi kopyalamaktadır.                                                                         |
| **Başka bir özellik ile değiştirildi?** | AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 ve Dynamics AX 2012 R3 CU9'da yayınlanmış olan **Ambar yönetimi** modülü, Ambar yönetimi II özelliklerinin yerini almıştır. Yeni modül Ambar yönetimi II'dekinden daha gelişmiş özelliklere ve daha esnek ambar yönetim süreçlerine sahiptir. |
| **Etkilenen modüller**             | Stok Yönetimi, satış ve pazarlama, tedarik ve kaynak atama                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>İnsan Kaynakları'ndaki çalışan anımsatıcıları

İnsan Kaynakları bordro bilgileri

|                              |                 |
|------------------------------|-----------------|
| **Kaldırılma nedeni**       | Düşük kullanım       |
| **Başka bir özellik ile değiştirildi?** | Hayır              |
| **Etkilenen modüller**             | İnsan kaynakları |

### <a name="workplanner"></a>İş planlayıcısı

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Düşük kullanım                                                                                                                                                            |
| **Başka bir özellik ile değiştirildi?** | Hayır, ama **Profil grupları** sayfasından açılan **Profil ilişkisi** sayfası, kaldırılan **İş planlayıcısı** sayfası ile aynı iş senaryosunu destekler. |
| **Etkilenen modüller**             | Saat ve işe devam                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++ mali tablolar

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| **Kaldırılma nedeni**       | Bu işlev başka bir özellik ile değiştirilmiştir.                                    |
| **Başka bir özellik ile değiştirildi?** | Yönetim Raporlayıcı (Dynamics AX'ın geçerli sürümünde **finansal raporlama** etiketli) |
| **Etkilenen modüller**             | Genel muhasebe                                                                              |


